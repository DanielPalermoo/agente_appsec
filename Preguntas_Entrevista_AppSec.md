# 🛡️ Banco de Preguntas - Entrevista Técnica AppSec / DevSecOps

Este archivo contiene el historial de preguntas de **Entrevista Técnica AppSec y DevSecOps** realizadas durante las sesiones de estudio, clasificadas por módulo para evitar repeticiones.

---

## 📦 Módulo: Seguridad en Contenedores & Docker

### Pregunta 1
**Enunciado:** Durante una auditoría de infraestructura a un entorno contenedorizado con Docker en la nube, descubres que la base de datos MySQL expone el puerto "3306:3306" al exterior. ¿Por qué esto representa un hallazgo de severidad Media/Alta y cuál es la remediación siguiendo el principio de Mínimo Privilegio de Red?

**Opciones:**
- A) Es de riesgo bajo porque las bases de datos siempre requieren puerto público para funcionar.
- B) Es un riesgo Medio/Alto porque expone la BD a ataques de fuerza bruta y RCEs. Se remedia eliminando la exposición pública o usando binding a 127.0.0.1.
- C) Es un riesgo Alto porque Docker desactiva el cifrado de datos cuando se expone un puerto.
- D) No es un riesgo si la contraseña de root es compleja.

**Respuesta Correcta:** B  
**Explicación:** Exponer puertos de BD a 0.0.0.0 permite que cualquier actor en Internet intente ataques de fuerza bruta o explote vulnerabilidades no parcheadas en el motor de BD. La remediación es mantener la BD en la red interna de Docker (`bridge`) sin directiva `ports` pública o restringida a `127.0.0.1`.

---

## 📦 Módulo: OWASP API Top 10 & Remediación Backend

### Pregunta 2
**Enunciado:** Al auditar la API REST de registro de usuarios (POST /api/register), inyectas en el cuerpo JSON el parámetro "role": "ADMIN". La API responde 201 Created y te otorga permisos de administrador. ¿Qué vulnerabilidad es esta y cómo se corrige en el backend (Node/Java)?

**Opciones:**
- A) BOLA (Broken Object Level Authorization).
- B) Mass Assignment (Asignación Masiva / Auto-Promoción de Privilegios).
- C) Server-Side Request Forgery (SSRF).
- D) Cross-Site Scripting (XSS Stored).

**Respuesta Correcta:** B  
**Explicación:** **Mass Assignment** ocurre cuando el backend mapea directamente el JSON entrante a la entidad/modelo de la base de datos sin usar un **DTO (Data Transfer Object)** restringido o una lista blanca (whitelist) de campos permitidos. Se corrige usando DTOs de entrada que omitan el campo `role` y asignándolo explícitamente en el código de servicio.

---

### Pregunta 3
**Enunciado:** Un desarrollador argumenta que un endpoint `POST /api/empleados` no necesita validación de DTO/campos (Mass Assignment) porque la ruta tiene un middleware que verifica que solo un usuario con rol `ADMIN` puede invocarla (`verifyRole('ADMIN')`). Como profesional de AppSec, ¿por qué su razonamiento viola el principio de "Defensa en Profundidad" (*Defense in Depth*)?

**Opciones:**
- A) Porque el rol ADMIN no debería poder crear otros usuarios bajo ningún concepto.
- B) Porque si falla el middleware de autenticación/rol o un Admin envía campos no deseados/maliciosos, la app queda desprotegida. La seguridad debe ser multicapa.
- C) Porque Mass Assignment solo aplica a bases de datos NoSQL como MongoDB.
- D) Porque los administradores siempre deben registrarse mediante scripts SQL directos.

**Respuesta Correcta:** B  
**Explicación:** El principio de **Defensa en Profundidad** exige múltiples capas de seguridad. Depender únicamente del middleware de autenticación es un único punto de fallo (Single Point of Failure). Si hay un bypass en el middleware, o si un admin ingresa datos malformados/inyectados, la falta de validación/DTO en la capa de datos permite la corrupción de la BD.

---

### Pregunta 4
**Enunciado:** Durante una auditoría a una API REST que ofrece inicio de sesión con proveedores de identidad (OAuth Google/Facebook), se descubre que el backend expone un endpoint `/api/auth/login-google` que acepta un JSON con el parámetro `{"email": "victima@empresa.com"}` y devuelve inmediatamente un token JWT válido de sesión sin validar el `id_token` firmado por Google. ¿Qué vulnerabilidad crítica se está presentando y cómo se debe remediar en el backend?

**Opciones:**
- A) Cross-Site Scripting (XSS Reflejado). Se arregla escapando caracteres HTML en el correo.
- B) Bypass de Autenticación por Falta de Validación de Proveedor OAuth. Se arregla verificando la firma del `id_token` usando las librerías oficiales del proveedor antes de emitir la sesión.
- C) Session Fixation (Fijación de Sesión). Se arregla regenerando el ID de la cookie en cada petición.
- D) Inyección SQL de segundo orden. Se arregla mediante procedimientos almacenados en la base de datos.

**Respuesta Correcta:** B  
**Explicación:** Permitir que el cliente simplemente declare su `email` sin aportar una prueba criptográfica verificable (como un `id_token` firmado por Google y verificado en el backend con las claves públicas de Google) permite a cualquier usuario suplantar la identidad de cualquier cuenta en el sistema (Authentication Bypass).

---

### Pregunta 5
**Enunciado:** Durante una prueba de penetración a una API Spring Boot / Express, encuentras que la ruta `GET /api/empleados/todos` requiere token JWT de autenticación pero no exige el rol `ADMIN`. Un usuario con rol `EMPLEADO` puede obtener la lista de todos los usuarios y sus hashes de contraseñas. ¿Cómo se categoriza esta falla en OWASP API Top 10 y cómo se soluciona adecuadamente en código Java (Spring Security)?

**Opciones:**
- A) API1:2023 – Broken Object Level Authorization (BOLA). Se arregla ocultando la URL en el Frontend.
- B) API5:2023 – Broken Function Level Authorization (BFLA). Se arregla aplicando `@PreAuthorize("hasRole('ADMIN')")` o configurando `.requestMatchers("/api/empleados/todos").hasRole("ADMIN")` en la cadena de filtros de Spring Security.
- C) API8:2023 – Security Misconfiguration. Se arregla deshabilitando CORS en el servidor Tomcat.
- D) API10:2023 – Unsafe Consumption of APIs. Se arregla reiniciando la base de datos PostgreSQL.

**Respuesta Correcta:** B  
**Explicación:** **BFLA (Broken Function Level Authorization)** ocurre cuando los controles de acceso para funciones administrativas o sensibles se definen de forma inconsistente entre rutas. En Spring Security, se resuelve aplicando anotaciones de autorización por método (`@PreAuthorize("hasRole('ADMIN')")`) o reglas explícitas de autorización en la configuración de la cadena de filtros (`SecurityFilterChain`).

---

## 🛡️ Módulo: Gestores de Secretos y Hardcoded Credentials

### Pregunta 6
**Enunciado:** Durante la auditoría de código fuente de un backend Spring Boot, encuentras claves secretas de producción de Cloudflare R2 y contraseñas SMTP de correo dentro del archivo `application.properties`. ¿Por qué esto representa un riesgo Crítico en AppSec/DevSecOps y cómo debe remediarse correctamente?

**Opciones:**
- A) Es un riesgo bajo porque `application.properties` no se incluye dentro de los archivos compilados `.jar`.
- B) Es un riesgo Crítico porque las credenciales quedan expuestas permanentemente en el historial de commits de Git a cualquier desarrollador o atacante con acceso. Se remedia inyectando secretos mediante Variables de Entorno (`${CLOUDFLARE_R2_SECRET_KEY}`) y revocando/rotando las claves expuestas.
- C) Es un riesgo Medio que solo afecta si la base de datos se ejecuta en modo H2 en memoria.
- D) Se soluciona renombrando el archivo a `application.yml` sin necesidad de modificar el contenido.

**Respuesta Correcta:** B  
**Explicación:** Las credenciales embebidas en código/configuración (*Hardcoded Credentials*) son una de las principales causas de filtración de datos e infraestructura. La buena práctica de DevSecOps exige extraer todos los secretos a Variables de Entorno o a un Secret Manager (como HashiCorp Vault o AWS Secrets Manager), rotar/invalidar inmediatamente las credenciales comprometidas y purgar el historial de Git.

---

## 🛡️ Módulo: DevSecOps & Análisis de Dependencias (SCA)

### Pregunta 7
**Enunciado:** Durante un escaneo de SCA (Software Composition Analysis como Snyk o OWASP Dependency-Check) en un pipeline de CI/CD para un backend Java Spring Boot, la herramienta detecta una vulnerabilidad crítica (CVSS 9.8) en una librería transitiva de `jackson-databind`. ¿Cuál es el procedimiento correcto de remediación que debes seguir como ingeniero AppSec / Backend?

**Opciones:**
- A) Desactivar el paso de SCA en el pipeline de GitHub Actions para evitar que bloquee el despliegue a producción.
- B) Evaluar si la función vulnerable es alcanzable, actualizar la dependencia directa en `pom.xml` / `build.gradle` (o forzar la versión corregida mediante `dependencyManagement`), ejecutar tests de integración y verificar que el escaneo pase limpio.
- C) Renombrar el archivo `.jar` resultante dentro del contenedor Docker para que el escáner no detecte el nombre del paquete.
- D) Modificar la severidad del CVE manualmente a "Baja" en la base de datos de la empresa sin realizar cambios en el código.

**Respuesta Correcta:** B  
**Explicación:** En DevSecOps, cuando SCA detecta un CVE crítico en dependencias de terceros, la solución consiste en actualizar la librería a una versión donde el parche esté aplicado. En Maven/Gradle se puede overridear la versión transitiva usando `dependencyManagement` o actualizando el paquete padre. Además, se deben ejecutar pruebas para garantizar que la actualización no introduzca *breaking changes*.




