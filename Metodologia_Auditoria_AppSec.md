# 🛡️ Protocolo y Metodología de Auditoría AppSec Iterativa

Este documento define la metodología oficial de trabajo para el Agente AppSec y el Estudiante durante las sesiones prácticas de pentesting y auditoría de código fuente en aplicaciones web y APIs REST.

---

## 📌 Principios de la Metodología

1. **Alineación con el Perfil Backend (Java / Node.js / Multi-lenguaje)**:
   Cada hallazgo se analiza desde la perspectiva de desarrollo backend, conectando la explotación práctica en la API con el código fuente defectuoso y su remediación segura (*Code Remediation*).

2. **Flujo Iterativo "Una Vulnerabilidad a la Vez"**:
   - El Agente analiza el código del proyecto y propone **una única vulnerabilidad por turno**.
   - Se provee el objetivo, la explicación técnica, el código vulnerable y la guía paso a paso para probarla con Burp Suite o Postman desde la VM de Ubuntu.

3. **Pausa Obligatoria y Validación del Estudiante**:
   - El Agente no avanza a la siguiente vulnerabilidad hasta que el estudiante ejecute la prueba, tome las capturas de pantalla de evidencia y confirme que comprendió el fallo.

4. **Documentación e Informes por Demanda**:
   - El Agente **nunca** crea ni edita el informe en formato `.md` de manera automática.
   - La redacción se realiza **únicamente cuando el estudiante lo solicita explícitamente** (ejemplo: *"Escribí el informe de esta vulnerabilidad"*).

5. **Estructura Estándar de Almacenamiento**:
   - Informe `.md`: `auditorias/informes/<nombre_proyecto>/auditoria_<nombre_proyecto>.md`
   - Imágenes de evidencia: `auditorias/informes/<nombre_proyecto>/imagenes/vulnXXX_<descripcion>.png`
   - Las imágenes se enlazan automáticamente en el `.md` usando rutas relativas.

---

## 📄 Requisitos Obligatorios y Estructura Formal del Informe de Auditoría

Cada reporte redactado debe incluir rigurosamente las siguientes secciones para asegurar un estándar profesional y comprensible para equipos de desarrollo:

1. **Metadatos y Alcance Formal**:
   - Proyecto, componentes evaluados (backend, frontend), tipo de auditoría (Caja Blanca / Gris), acceso a código fuente y período de fechas de ejecución.
2. **Metodología de Auditoría**:
   - Explicación de los marcos utilizados (OWASP WSTG v4.2, OWASP API Security Top 10 2023) y fases del proceso (reconocimiento, análisis estático, DAST, causa raíz y remediación).
3. **Entorno de Pruebas e Infraestructura**:
   - Detalle de la máquina atacante (VM Ubuntu), host objetivo (Windows / WSL2), servicios, bases de datos (PostgreSQL, MySQL), contenedores Docker, puertos y topología de red.
4. **Herramientas Utilizadas**:
   - Inventario de herramientas aplicadas (Burp Suite, Postman, cURL, jwt.io, Docker Compose, etc.).
5. **Alcance Detallado (Scope)**:
   - Inventario exhaustivo de archivos analizados (rutas, controladores, modelos, servicios de integración y configuraciones).
6. **Revisión de Dependencias (SCA - Software Component Analysis)**:
   - Tabla de paquetes (`package.json` / `pom.xml`) con versiones exactas, análisis de riesgos y librerías de seguridad faltantes.
7. **Resumen Ejecutivo de Hallazgos**:
   - Tabla consolidada con ID, Título, Severidad CVSS v3.1, Categoría OWASP, Estado y Fecha de detección.
8. **Detalle Exhaustivo por Vulnerabilidad**:
   - **Explicación didáctica para desarrolladores**: Redactada pensando en programadores sin conocimientos previos de seguridad (qué significa el fallo, por qué ocurrió, cómo se interpreta la respuesta y su impacto en el negocio).
   - **Evidencia visual irrefutable**: Priorizar capturas de pantalla reales (prints) de Burp Suite / herramientas en lugar de solo bloques JSON crudos.
   - **Análisis de código vulnerable**: Fragmento del código fuente comentado señalando el error técnico.
   - **Solución y remediación definitiva**: Explicación de la solución y bloque de código seguro corregido listo para producción (Node.js y/o Java Spring Boot).
9. **Conclusiones y Recomendaciones DevSecOps**:
   - Guía estratégica para integrar seguridad en el ciclo de vida del desarrollo (SDLC).
