Guía de Estudio Priorizada: Protocolo HTTP para Ciberseguridad

Objetivo: Filtrado de la documentación oficial (MDN Web Docs) enfocado exclusivamente en perfiles AppSec (Seguridad de Aplicaciones) y Blue Team (Defensa).

1. Nivel Prioritario: Fundamentos Teóricos (Sección "Guides")

Estas guías establecen la base conceptual. Deben leerse completas para comprender la lógica de los ataques y la defensa.

HTTP messages ✔

Importancia: Crítica.

Objetivo: Entender la anatomía de una petición. Diferenciar claramente entre la línea de inicio, las cabeceras (headers) y el cuerpo (body). Es vital para identificar inyecciones.

HTTP authentication ✔

Importancia: Alta.

Objetivo: Comprender los esquemas de desafío/respuesta y cómo viajan las credenciales (Basic, Bearer, Digest) para auditar sistemas de login.

Using HTTP cookies ✔

Importancia: Crítica.

Objetivo: Comprender el manejo de estado y sesiones. Base fundamental para entender el Secuestro de Sesión (Session Hijacking) y ataques CSRF.

Redirections in HTTP✔

Importancia: Alta.

Objetivo: Identificar flujos de redirección para detectar Phishing y vulnerabilidades de Open Redirect.

2. Nivel Prioritario: Referencia Técnica (Sección "Reference")

Esta sección funciona como un diccionario. No se lee linealmente, se consultan puntos específicos.

A. Métodos de Petición (HTTP Request Methods) ✔

Centrarse únicamente en los verbos que permiten interacción de datos:

GET: Recuperar datos.

POST: Enviar datos.

PUT / DELETE: Modificar o borrar recursos (vectores de ataque comunes si están mal configurados).

B. Códigos de Estado (HTTP Status Codes) ✔

Comprender las clases de respuesta para el análisis de logs:

2xx: Éxito (ej. 200 OK).

3xx: Redirección (ej. 301, 302).

4xx: Errores del cliente (ej. 401 Unauthorized vs 403 Forbidden).

5xx: Errores del servidor (ej. 500 Internal Server Error).

C. Cabeceras HTTP (HTTP Headers)

Dentro de la lista masiva de headers, estudiar solo los siguientes grupos:

Authentication: Específicamente el header Authorization. ✔

Cookies: Específicamente Set-Cookie y Cookie. ✔

CORS: Entender Access-Control-Allow-Origin. ✔

Security: Los escudos defensivos: Content-Security-Policy (CSP), Strict-Transport-Security (HSTS) y X-Frame-Options.

3. Nivel Secundario: Contexto Útil (Leer si sobra tiempo)

Lecturas que ayudan a conectar conceptos, pero no son bloqueantes.

Overview of HTTP: Visión general de la arquitectura Cliente-Servidor.

Media types: Tipos MIME. Útil para vulnerabilidades de subida de archivos (File Upload).

Proxy servers and tunneling: Importante para Blue Team (rastreo de IPs reales y logs).

4. Material a Omitir (Por ahora)

Temas avanzados, de optimización o históricos que pueden distraer del objetivo principal de seguridad inicial.

Caching / HTTP caching / Conditionals

Compression / Transfer coding

Content negotiation

Range requests / Downloads

Evolution of HTTP (Historia)

WebSockets (Protocolo distinto)

Connection management