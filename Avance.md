# 📈 Registro de Avance - Plan de Carrera AppSec / DevSecOps

**Estudiante:** Desarrollador Java/Backend  
**Meta:** Rol Junior en AppSec / DevSecOps (12 Meses)  
**Última Actualización:** 24 de Septiembre, 2026  

---

## 📌 Estado de Situación Actual

* **ESTADO ACTUAL:** 🎓 **Estudiando y preparando intensivamente el examen para la Certificación Oficial ISC2 Certified in Cybersecurity (CC)**.
* **FASE ANTERIOR (COMPLETADA):** 🛡️ Auditoría práctica completa realizada sobre la aplicación `proyectoweb`.

---

## ✅ Fases y Hitos Completados

### 1. Fase 1 - Fundamentos Web & Hacking Básico (Semanas 1-4)
- [x] Estudio de protocolo HTTP/HTTPS, headers de seguridad (CSP, HSTS), cookies (`Secure`, `HttpOnly`).
- [x] Laboratorios completos nivel *Apprentice* en **PortSwigger Web Security Academy** (SQLi, Auth, Access Control, XSS, Path Traversal, API Testing, Business Logic).
- [x] Interceptación y análisis de tráfico con **Burp Suite Community Edition**.

### 2. Fase 1.5 - Primera Auditoría Práctica Real (Semanas 5-8)
- [x] Auditoría completa a la aplicación `proyectoweb` (Node.js/Express + PostgreSQL en Docker/WSL2).
- [x] Explotación de 5 vulnerabilidades clave con Burp Suite:
  - **VULN-001 (Crítica)**: Authentication Bypass en Login de Google por falta de verificación de ID Token.
  - **VULN-002 (Alta)**: Exposición de datos sensibles (Fuga de hashes de contraseña Bcrypt en respuestas API).
  - **VULN-003 (Alta)**: Escalación de privilegios por Broken Function Level Authorization (BFLA) en rutas de empleados y auditorías.
  - **VULN-004 (Media)**: Exposición de secretos y API Keys de OpenRouteService/RapidAPI en texto plano en código versionado.
  - **VULN-005 (Alta)**: Broken Object Level Authorization (BOLA / IDOR) en la consulta de pedidos por ID.
- [x] Informe formal generado y guardado con evidencias en: [`auditorias/proyectoweb/auditoria_proyectoweb.md`](auditorias/proyectoweb/auditoria_proyectoweb.md).

---

## 🔄 Fase Activa / En Curso

### 3. Fase 2 - Preparación y Rendición ISC2 CC (Semanas 9-12 / ENFOQUE ACTUAL)
- [ ] **Dominio 1**: Security Principles (Triada CIA, Riesgos, Controles).
- [ ] **Dominio 2**: Business Continuity (BC), Disaster Recovery (DR) & Incident Response (IR).
- [ ] **Dominio 3**: Access Controls Concepts (Autenticación, RBAC, DAC, MAC).
- [ ] **Dominio 4**: Network Security (Capa OSI, Firewalls, Subredes, TLS/SSL).
- [ ] **Dominio 5**: Security Operations (Seguridad de datos, Políticas, Hardening).
- [ ] **Objetivo Inmediato**: Agendar y aprobar el examen oficial bonificado al 100% (*One Million Certified Candidates*).

---

## 🚀 Próximos Pasos (Fase 2.5 & Fase 3)

- [ ] **DevSecOps & CI/CD**: Crear pipelines en GitHub Actions para automatizar escaneos SAST (Semgrep) y SCA (Snyk).
- [ ] **Remediación de Código Backend**: Implementar parches en código Java / Spring Boot y Node.js para blindar las vulnerabilidades encontradas.
- [ ] **Portafolio Público**: Publicar repositorio DevSecOps en GitHub y optimizar perfil de LinkedIn.
