🌐 Filtro "Need to Know" para la Web Security Academy

No sigas el orden de esa lista. Como recién estás empezando a "romper", vamos a ir de lo más familiar a lo más abstracto. Enfócate solo en los laboratorios de nivel Apprentice de estas 4 categorías iniciales:

- 📦 SQL Injection (SQLi): Vienes del mundo Java/SQL, así que esto te resultará natural. Aquí vas a ver cómo una mala sanitización en el backend permite inyectar comandos directamente a la base de datos. ✔

- 🛡️ Authentication & Access control vulnerabilities: Esto conecta directamente con tu estudio de HTTP. Vas a ver en la práctica qué pasa cuando fallan los HTTP Status Codes (ej. devolver un 200 OK en lugar de un 401 Unauthorized o 403 Forbidden) y cómo se abusa de los esquemas de login. ✔

- 🍪 Cross-site scripting (XSS): Fundamental. Aunque es un ataque que ocurre en el cliente (navegador), es culpa del backend por no filtrar. Conexión con la teoría: Aquí verás en acción el Session Hijacking. Si una Cookie no tiene el flag HttpOnly, un ataque XSS puede leerla mediante JavaScript y robártela. (Analogía: La Cookie es como el ticket de guardarropas de la discoteca; el XSS es el ladrón que te saca el ticket del bolsillo para llevarse tu abrigo). ✔

- 📦 Path traversal & OS command injection: Son ataques puros de infraestructura y backend. Vas a aprovechar los verbos HTTP (GET/POST) para intentar leer archivos del sistema operativo (como /etc/passwd en Linux) o ejecutar comandos de consola. ✔

Omitir por ahora: Ignora completamente cosas avanzadas como HTTP request smuggling, WebSockets, Web cache poisoning o Insecure deserialization (esta última es el talón de Aquiles de Java, pero requiere una base más sólida antes de tocarla).

🌐 Sobre tu cuenta y los beneficios de estudiante

La Web Security Academy de PortSwigger es el recurso de aprendizaje de AppSec más completo disponible públicamente y es 100% gratuito para todo el mundo.



No hay un nivel "Premium" de la academia ni beneficios adicionales por usar un correo estudiantil (.edu) para iniciar sesión allí. Puedes usar tu correo personal o el de Gmail sin problemas. Todo el contenido y los laboratorios están desbloqueados.

(Nota rápida de mentor: Guarda tus beneficios de estudiante para herramientas de infraestructura, como los créditos de DigitalOcean o Azure que sacaste con el GitHub Student Developer Pack, ya que ahí sí marcan la diferencia económica).

Para resolver los laboratorios, lo único que necesitas es tener Burp Suite Community Edition instalado (que también es gratis). Más adelante, si decides ir por la certificación oficial BSCP, ten en cuenta que el examen cuesta $99 USD y requiere la versión Profesional de Burp Suite, pero podrás usar legalmente la versión de prueba (Trial) de 30 días para rendirlo.



¿Ya tienes descargado y configurado Burp Suite Community en tu navegador, o prefieres que repasemos cómo interceptar tu primera petición HTTP antes de que te lances al primer laboratorio de SQL Injection?