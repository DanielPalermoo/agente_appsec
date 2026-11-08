# 🎓 Banco de Preguntas - Examen ISC2 CC

Este archivo contiene el historial de preguntas del examen **ISC2 Certified in Cybersecurity (CC)** realizadas durante las sesiones de estudio, clasificadas por módulo para evitar repeticiones.

---

## 🌐 Módulo: Network Security & Access Controls

### Pregunta 1
**Enunciado:** ¿Por qué un firewall o mecanismo de control de acceso a nivel de red bloquea por defecto el tráfico entrante dirigido hacia interfaces internas no enrutadas (como la subred privada de WSL2)?

**Opciones:**
- A) Porque utiliza filtrado stateless basado únicamente en protocolos de capa 2 (MAC Address).
- B) Por el principio de Mínimos Privilegios y Defensa en Profundidad (Implicit Deny por defecto en interfaces no confiables).
- C) Porque las subredes privadas RFC 1918 están estrictamente prohibidas en entornos locales.
- D) Porque Docker deshabilita automáticamente el enrutamiento IP en el Kernel Linux.

**Respuesta Correcta:** B  
**Explicación:** El principio fundamental en cortafuegos es el **Implicit Deny** (bloquear todo el tráfico por defecto a menos que exista una regla explícita). La interfaz virtual de WSL2 pertenece a un segmento aislado por defecto para prevenir que servicios expuestos en Linux queden vulnerables a la red física sin consentimiento del administrador.

---

## 🛡️ Módulo: Security Operations & CIA Triad

### Pregunta 2
**Enunciado:** Un auditor de seguridad observa que una API REST transmite tokens JWT y credenciales de autenticación en cabeceras HTTP sin cifrado TLS (http://). ¿Qué pilar de la Triada CIA se está violando principalmente y qué ataque permite?

**Opciones:**
- A) Disponibilidad — Permite ataques de denegación de servicio (DoS).
- B) Confidencialidad — Permite ataques de interceptación de tráfico (Man-in-the-Middle / Sniffing).
- C) No Repudio — Evita rastrear qué usuario ejecutó la transacción.
- D) Integridad — Invalida la firma digital de los hashes SHA-256.

**Respuesta Correcta:** B  
**Explicación:** El tráfico en texto plano (HTTP) compromete la **Confidencialidad**, ya que cualquier intermediario en la ruta de red (como un Wi-Fi público o un router comprometido) puede leer las credenciales y reutilizar los tokens JWT de sesión.

---

## 🎓 Módulo: Security Principles & Access Controls

### Pregunta 3
**Enunciado:** Durante la migración de un servicio monolítico Java a microservicios REST, el equipo decide implementar autenticación centralizada mediante tokens OAuth2/JWT. Un desarrollador sugiere omitir la verificación criptográfica de la firma del JWT en cada microservicio interno si la petición proviene de la red corporativa. ¿Qué principio de seguridad revisado en el examen ISC2 CC se está violando y por qué representa un riesgo severo en AppSec?

**Opciones:**
- A) Principio de Alta Disponibilidad — Porque aumenta el tiempo de latencia en la red interna.
- B) Principio de Zero Trust (Confianza Cero) y Defensa en Profundidad — Porque asume erróneamente que el perímetro interno es 100% seguro, permitiendo movimiento lateral si un servicio es comprometido.
- C) Principio de No Repudio — Porque desactiva los registros de auditoría en los controladores de Spring Boot.
- D) Principio de Mínimo Privilegio — Porque los microservicios solo deben procesar verbos HTTP GET.

**Respuesta Correcta:** B  
**Explicación:** El modelo **Zero Trust** establece "nunca confiar, siempre verificar". Confiar ciegamente en la red interna viola la Defensa en Profundidad; si un atacante compromete un contenedor o microservicio interno, podrá forjar tokens JWT y suplantar cualquier rol o usuario si los demás servicios no verifican la firma del token.

---

### Pregunta 4
**Enunciado:** Un usuario con un rol operativo estándar en un sistema Web de inventarios logra listar todos los registros de auditoría y sesiones activas de los administradores simplemente enviando una petición HTTP directa a un endpoint de la API (`/api/empleados/historial-login`). ¿Qué principio de Control de Acceso se incumplió a nivel de diseño de la aplicación?

**Opciones:**
- A) Control de Acceso Discrecional (DAC) a nivel de archivo físico.
- B) Control de Acceso Basado en Roles (RBAC) con aplicación del Principio de Mínimo Privilegio en el backend.
- C) Filtrado de direcciones IP en la capa de red del Firewall.
- D) Autenticación Multifactor (MFA) en el navegador del cliente.

**Respuesta Correcta:** B  
**Explicación:** El **Control de Acceso Basado en Roles (RBAC)** y el **Principio de Mínimo Privilegio** exigen que el backend valide el rol asignado al usuario antes de permitirle ejecutar funciones administrativas. Omitir la validación de rol en endpoints sensibles permite a usuarios con bajos privilegios acceder a funciones restringidas (BFLA).

---

## 🎓 Módulo: Business Continuity (BC) & Disaster Recovery (DR) Concepts

### Pregunta 5
**Enunciado:** Durante una interrupción severa en los servidores centrales de un banco, el equipo de ciberseguridad activa sus procedimientos de respuesta. ¿Cuál es la diferencia fundamental entre el Plan de Continuidad del Negocio (BCP) y el Plan de Recuperación ante Desastres (DRP) según los estándares de ISC2?

**Opciones:**
- A) El BCP se enfoca únicamente en la infraestructura tecnológica de servidores, mientras que el DRP se enfoca en el personal operativo.
- B) El BCP busca mantener operativas las funciones críticas del negocio durante y después de una interrupción, mientras que el DRP se centra en restaurar la infraestructura de TI a su estado normal.
- C) El DRP se ejecuta preventivamente antes del incidente y el BCP solo se activa tras la evacuación del edificio.
- D) El BCP suspende temporalmente las políticas de control de acceso para acelerar los procesos de negocio.

**Respuesta Correcta:** B  
**Explicación:** El **BCP (Business Continuity Plan)** abarca una visión holística para garantizar que las operaciones críticas de la organización sigan funcionando (incluso con procesos manuales o alternativos), mientras que el **DRP (Disaster Recovery Plan)** es un subconjunto enfocado en la restauración y recuperación técnica de la infraestructura, sistemas de TI y datos dañados por el evento.


