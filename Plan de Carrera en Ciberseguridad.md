# Informe Estratégico de Mercado y Plan de Carrera en Ciberseguridad: Argentina 2024-2025

## 1. Resumen Ejecutivo y Visión Estratégica

El presente informe técnico analiza exhaustivamente el ecosistema laboral de la ciberseguridad en la República Argentina para el periodo 2024-2025, diseñado específicamente para un perfil con base académica en programación. En un contexto macroeconómico caracterizado por una alta volatilidad inflacionaria y una dispersión salarial sin precedentes entre el mercado local e internacional, la elección de la especialización y la estrategia de inserción laboral resultan determinantes para la viabilidad financiera y profesional del candidato.

La investigación, fundamentada en datos de encuestas salariales locales como Sysarmy y Openqube, reportes globales de ISC2 y Fortinet, y análisis de tendencias en comunidades técnicas, revela una bifurcación crítica en el mercado. Mientras que los roles operativos de defensa (SOC Nivel 1) y los roles ofensivos iniciales (Junior Pentester) muestran signos de saturación y estancamiento salarial en moneda local, las posiciones que hibridan el desarrollo de software con la seguridad (AppSec, DevSecOps, Product Security) presentan una demanda insatisfecha estructural y una prima salarial significativa.1

Los hallazgos indican que la capacidad de operar en inglés (nivel B2/C1) actúa como el mayor multiplicador de ingresos, permitiendo el acceso a posiciones Contractor con remuneraciones que superan en hasta un 200% a sus contrapartes locales en pesos argentinos (ARS).4 Este documento desglosa la arquitectura salarial, contrasta las trayectorias de carrera y culmina con un roadmap de empleabilidad de seis meses diseñado para transformar las competencias de programación en un perfil de Ingeniería de Seguridad de alto valor, evitando la competencia masiva de los roles de entrada tradicionales.

## 2. Análisis Macroeconómico del Mercado IT en Argentina (2024-2025)

El mercado laboral tecnológico en Argentina no puede analizarse aisladamente de su coyuntura económica. La dinámica inflacionaria y la brecha cambiaria han configurado un escenario dual donde coexisten dos realidades laborales distintas: el mercado pesificado y el mercado dolarizado (o bimonetario).

### 2.1. Evolución Salarial y Poder Adquisitivo Local

Según los resultados de la Encuesta de Sueldos de Sysarmy (2025.1) y el análisis de Openqube, el mercado local ha realizado esfuerzos significativos para acompañar la inflación, aunque con resultados dispares según el nivel de seniority.

- Ajustes vs. Inflación: En el primer semestre de 2025, se registró una inflación acumulada del 15% según el INDEC. En contraste, la mediana salarial del sector IT aumentó aproximadamente un 26% en el mismo período, lo que sugiere una recuperación leve del poder adquisitivo para los roles registrados en blanco.2 Sin embargo, esta estadística agregada enmascara la realidad de los roles Junior, donde la oferta masiva de candidatos egresados de bootcamps mantiene los salarios de entrada comprimidos.

- La Brecha de Género: Un dato estructural preocupante es la persistencia de la brecha salarial. Actualmente, por cada peso que gana un hombre cis, una mujer cis gana aproximadamente 83 centavos en posiciones equivalentes.2 Este factor es relevante para la planificación de carrera, indicando la necesidad de una negociación salarial más agresiva y fundamentada en datos de mercado por parte de las profesionales mujeres.

### 2.2. El Fenómeno de la Dolarización

La "dolarización de facto" de los salarios IT se ha consolidado como el principal mecanismo de retención de talento y protección contra la devaluación.

- Prevalencia: El 34% de los profesionales encuestados en Argentina reporta tener su sueldo dolarizado, ya sea parcial o totalmente. De este grupo, un 14% cobra el 100% en moneda dura, mientras que un 13% recibe una parte en dólares y el resto en pesos.2

- Impacto en la Estrategia de Carrera: Para un estudiante, esto implica que el objetivo de mediano plazo no debe ser solo conseguir un empleo, sino conseguir un empleo con estructura de pago bimonetaria o full contractor. Las empresas locales que pagan 100% en pesos enfrentan una rotación altísima, lo que paradójicamente abre oportunidades para Juniors que buscan su primera experiencia ("escuela"), pero limita el crecimiento financiero a largo plazo si no se pivota hacia el mercado internacional.

### 2.3. La Demanda de Talento y la Escasez de Habilidades

A pesar de la contracción en otros sectores, la ciberseguridad mantiene una demanda robusta impulsada por la digitalización forzada y el aumento de ciberataques en la región.

- Brecha en Latinoamérica: Reportes de Fortinet y ISC2 indican que la escasez de profesionales en ciberseguridad en Latinoamérica sigue siendo crítica, con un déficit de millones de puestos.6 Sin embargo, esta escasez es cualitativa, no cuantitativa. Faltan perfiles con experiencia en arquitectura de nube, seguridad de aplicaciones y automatización; sobran perfiles con conocimientos básicos de hacking ético sin base técnica sólida.

- El Rol de la IA: La adopción de IA para la detección y prevención de amenazas es una prioridad para el 71% de las organizaciones en LATAM.6 Esto revaloriza al profesional que entiende cómo funcionan estos modelos y cómo integrarlos vía API, una ventaja competitiva directa para un estudiante de programación frente a un analista tradicional.

## 3. La Gran Divergencia: Blue Team vs. Red Team

Una de las decisiones estratégicas más importantes para el estudiante es definir su "bando". El análisis de foros especializados (Reddit r/cybersecurity, r/netsec) y ofertas laborales muestra una discrepancia masiva entre la percepción popular (impulsada por series y medios) y la realidad operativa de las empresas.

### 3.1. Red Team y Pentesting: El Espejismo de la Entrada

El lado ofensivo (Red Team, Pentesting) es a menudo el más atractivo para los estudiantes debido a su mística, pero presenta las barreras de entrada más altas y el menor volumen de ofertas Junior.

- Ratio de Oferta: El consenso en la industria, respaldado por discusiones de veteranos, establece una proporción aproximada de 1 puesto ofensivo por cada 10 puestos defensivos.7

- Naturaleza de la Demanda: La mayoría de las empresas no tienen un Red Team interno permanente. Contratan servicios de pentesting una o dos veces al año a consultoras especializadas o MSSPs (Managed Security Service Providers). Esto concentra las ofertas laborales en un número reducido de firmas de consultoría, aumentando la competencia.7

- Saturación Junior: Existe una sobreoferta de candidatos Junior con certificaciones teóricas (como CEH) que carecen de experiencia real en administración de sistemas o desarrollo. Los reclutadores señalan que el "Hacking Ético" está sobresaturado en los niveles iniciales, donde "cada joven de 20 años quiere ser un hacker cool".9

- Requisitos Reales: Para ser efectivo atacando un sistema, primero se debe entender profundamente cómo se construye y defiende. Por ello, los mejores Red Teamers suelen ser ex-desarrolladores o ex-administradores de sistemas con años de experiencia. Intentar entrar directamente como Junior Pentester sin este background a menudo resulta en estancamiento laboral o trabajos de baja calidad (correr escáneres automáticos y generar reportes genéricos).10

### 3.2. Blue Team y Defensa: La Necesidad Operativa

El Blue Team (Defensa) representa la columna vertebral de la seguridad corporativa.

- Demanda Estructural: A diferencia del pentesting, la defensa es una operación 24/7. Las empresas necesitan monitorear redes, gestionar identidades, parchar vulnerabilidades y responder a incidentes continuamente. Esto genera un flujo constante y masivo de vacantes.7

- Estabilidad: En tiempos de recesión, las empresas pueden recortar el presupuesto de auditorías externas (Pentesting), pero difícilmente desmantelen su centro de operaciones de seguridad (SOC) o sus ingenieros de seguridad de infraestructura, ya que esto implicaría quedar ciegos ante ataques.

- Evolución hacia Purple Teaming: La tendencia actual es la colaboración. Los roles defensivos modernos no son estáticos; implican emular ataques para mejorar las defensas. Comenzar en el Blue Team permite al profesional adquirir el conocimiento profundo de la infraestructura que eventualmente le permitiría transicionar a un rol ofensivo de élite (Purple Team) con mucha mayor credibilidad.12

Tabla 1: Comparativa de Mercado - Ofensiva vs. Defensa

| Dimensión | Red Team / Pentesting | Blue Team / Defensa |

| --- | --- | --- |

| Volumen de Ofertas | Bajo (Nicho) | Alto (Estructural) |

| Competencia Junior | Muy Alta (Saturado) | Media (Falta talento cualificado) |

| Barrera de Entrada | Alta (Requiere experiencia previa en IT) | Media (Accesible con base técnica) |

| Estabilidad Laboral | Variable (Depende de contratos/proyectos) | Alta (Roles internos permanentes) |

| Valor de la Programación | Alto (Exploit development, scripting) | Muy Alto (Automatización, Detección) |



## 4. Análisis de Roles: La Encrucijada del Programador

Para un estudiante de programación, la elección no es solo "Atacar o Defender", sino "Operar o Construir". Aquí analizamos dos trayectorias divergentes: el Analista de SOC (Operaciones) y el Ingeniero de AppSec/DevSecOps (Ingeniería).

### 4.1. Analista de SOC (Security Operations Center)

Es el rol de entrada por excelencia ("la trinchera"), pero puede ser una trampa profesional para un desarrollador si se permanece demasiado tiempo.

- Descripción del Puesto: Monitoreo de consolas SIEM (Security Information and Event Management), análisis de alertas, triaje inicial de incidentes y escalamiento a niveles superiores (Tier 2/3).

- Realidad Diaria: Trabajo por turnos rotativos (incluyendo noches y feriados), tareas repetitivas y alto riesgo de burnout por "fatiga de alertas".13

- Desajuste con el Perfil: Un programador encontrará que sus habilidades de creación de software se atrofian. Si bien se usa algo de scripting (Python/Bash) para automatizar tareas simples, el núcleo del trabajo es analítico y procedimental, no creativo ni constructivo.

- Salario: Es el más bajo dentro del espectro de ciberseguridad debido a la menor barrera de entrada técnica.

### 4.2. Application Security (AppSec) y DevSecOps

Estos roles representan la "Ingeniería de Seguridad". Son el punto dulce donde la programación y la seguridad convergen.

- AppSec: Se enfoca en la seguridad del código fuente.

- Tareas: Realizar revisiones de código (Secure Code Review), modelado de amenazas (Threat Modeling), gestión de programas de Bug Bounty, y capacitación a desarrolladores en prácticas de codificación segura.

- La Ventaja del Programador: Para decirle a un desarrollador cómo arreglar una vulnerabilidad de inyección SQL en una API Java, uno debe entender Java y APIs. Un profesional de seguridad sin base de programación no puede hacer esto eficazmente. La experiencia previa desarrollando es, de hecho, el requisito número uno en muchas ofertas de AppSec.14

- DevSecOps: Se enfoca en la seguridad de la infraestructura y el pipeline de despliegue.

- Tareas: Integrar herramientas de seguridad (SAST, DAST, SCA) en pipelines de CI/CD (Jenkins, GitHub Actions), asegurar contenedores (Docker, Kubernetes) y gestionar infraestructura como código (Terraform).

- Sinergia: Requiere un dominio fuerte de Linux, scripting y herramientas de nube, habilidades que un estudiante de programación moderno ya está desarrollando.16

Conclusión del Análisis de Roles: Para maximizar el retorno de inversión de los estudios de programación, el camino óptimo es AppSec/DevSecOps. Entrar en un SOC sería infrautilizar el capital técnico y competir en desventaja salarial. Los roles de ingeniería de seguridad valoran y pagan por la capacidad de construir seguridad, no solo monitorearla.

## 5. Arquitectura Salarial: Local vs. Contractor y el Factor Inglés

El análisis cuantitativo de las remuneraciones revela tres estratos salariales bien definidos en el mercado argentino para el periodo 2024-2025. Los datos se han normalizado utilizando las medianas reportadas por Sysarmy, Openqube y plataformas de contratación internacional como Levels.fyi.

### 5.1. Estrato 1: Mercado Local en Pesos (Sin Inglés)

Este segmento abarca empresas nacionales, sector público y consultoras pequeñas que operan exclusivamente en el mercado interno.

- Junior (0-2 años):

- La remuneración promedio se sitúa en el rango de $800.000 a $1.200.000 ARS brutos mensuales.5

- Observación: Este salario compite directamente con puestos administrativos no técnicos, lo que refleja la compresión salarial en la entrada. La inflación (15% semestral) obliga a revisiones constantes, y la capacidad de ahorro es mínima.

- Semi-Senior (2-5 años):

- El rango asciende a $1.800.000 - $2.800.000 ARS brutos mensuales.5 Aquí se empieza a notar la fuga de talento; los profesionales que alcanzan este nivel suelen migrar al Estrato 2 o 3, dejando vacantes difíciles de cubrir en el mercado local.

### 5.2. Estrato 2: Mercado Local "Premium" / Bimonetario

Empresas grandes de tecnología (Unicornios), filiales de multinacionales y software factories de primer nivel que exportan servicios.

- Esquema: Sueldos pagados parcialmente en dólares (10% al 50% del salario) o pegados al tipo de cambio oficial/MEP.

- Junior: $1.200.000 - $1.800.000 ARS (equivalente mixto). Ofrecen beneficios robustos (prepaga de primer nivel, bonos).

- Semi-Senior: $3.000.000+ ARS o su equivalente en esquema mixto.20

### 5.3. Estrato 3: Mercado Contractor (Inglés B2/C1)

Trabajo remoto directo para empresas en EE.UU., Europa o Startups globales. Este es el objetivo financiero final.

- El Multiplicador del Inglés: El dominio del idioma inglés no es un "plus", es una llave de acceso a una economía diferente. Un profesional Junior con inglés fluido puede acceder a salarios que un Senior local envidiaría.

- Junior (Entry-Level Global):

- Rango: $1.500 - $2.500 USD mensuales.18

- Análisis: Un salario de $2.000 USD (aprox. $2.200.000 - $2.400.000 ARS al cambio libre) duplica el techo salarial del mercado local junior.

- Semi-Senior / Senior:

- Rango: $3.500 - $6.000+ USD mensuales.21

- Para roles de nicho como AppSec Engineer, los salarios base en EE.UU. para posiciones remotas comienzan frecuentemente por encima de los $100.000 USD anuales ($8.300 USD/mes), aunque desde LATAM se suele aplicar un ajuste regional, situando ofertas competitivas en el rango de $4.000 - $7.000 USD.23

Tabla 2: Proyección Salarial Comparativa (Estimada Octubre 2024 - Marzo 2025)

| Rol | Seniority | Mercado Local (ARS) | Mercado Contractor (USD) | Diferencial (Aprox.) |

| --- | --- | --- | --- | --- |

| Analista SOC | Junior | $950.000 - $1.200.000 | $1.200 - $1.800 | +80% |

| DevSecOps / AppSec | Junior | $1.200.000 - $1.600.000 | $2.000 - $3.000 | +150% |

| Analista de Seguridad | Semi-Senior | $2.200.000 - $3.000.000 | $3.500 - $5.000 | +130% |



Insight Clave: La inversión en aprender inglés (llevándolo de un nivel técnico a conversacional) tiene un ROI (Retorno de Inversión) superior a cualquier certificación técnica en el corto plazo. Un DevSecOps Junior que habla inglés gana más que un CISO (Gerente de Seguridad) en una PYME local que solo habla español.

## 6. Networking Estratégico y Comunidades Locales

En Argentina, el networking no es solo socialización; es el mecanismo principal de acceso al "mercado oculto" de ofertas laborales que nunca se publican en portales tradicionales.

### 6.1. Ecosistema de Comunidades

- Sysarmy: El corazón de la comunidad IT argentina.

- Canales: Su Slack y Discord son vitales. El canal #seguridad es una fuente constante de consultas técnicas y ofertas laborales informales. El canal #sueldos provee un reality check constante de las remuneraciones.1

- Acción: Unirse a Sysarmy es el paso cero. Participar en las discusiones técnicas demuestra interés y conocimiento ante pares que eventualmente pueden ser quienes recomienden al candidato.

- OWASP Buenos Aires: Capítulo local de la Open Worldwide Application Security Project.

- Relevancia: Al estar enfocado en seguridad de aplicaciones, es la comunidad natural para un programador. Sus meetups son técnicos y específicos.26

- Oportunidad: Asistir a sus reuniones permite conectar directamente con líderes de AppSec de empresas locales importantes.

- Ekoparty: La conferencia de seguridad más grande de Latinoamérica.

- Fechas: Se celebra anualmente, típicamente en octubre/noviembre (Fechas confirmadas para 2025: 22, 23 y 24 de Octubre en el Centro de Convenciones de Buenos Aires).28

- Estrategia: No asistir solo a las charlas principales. El valor real está en los Villages (espacios temáticos). Para un programador, pasar tiempo en el AppSec Village, DevSecOps Village o participar en los CTF (Capture The Flag) es donde se demuestra habilidad práctica. También es crucial visitar los stands de las empresas en la feria de empleo, donde los ingenieros técnicos (no solo RRHH) suelen estar presentes.30

- Nerdearla: Evento masivo y gratuito organizado por Sysarmy (Septiembre 23-27, 2025).32

- Foco: Aunque es generalista de IT, tiene tracks fuertes de seguridad e infraestructura. Es el lugar ideal para entender cómo la seguridad se integra en el ciclo de vida del desarrollo en empresas como Mercado Libre, Despegar o Naranja X.

### 6.2. Canales Digitales

- Telegram: Existen grupos activos como "Ciberseguridad Argentina" donde la dinámica es rápida e informal. Son excelentes para resolver dudas puntuales y enterarse de eventos de último minuto.34

- LinkedIn: Es fundamental seguir a referentes locales y recruiters especializados en IT de LATAM. La visibilidad aquí se logra compartiendo los proyectos del portafolio (ver sección 8) y comentando con criterio en publicaciones del sector.

## 7. Veredicto: El Área Ganadora

Considerando el perfil del usuario (Estudiante de Programación) y las condiciones de mercado 2024-2025, el área ganadora es indiscutiblemente:

### Application Security (AppSec) / DevSecOps

Justificación basada en datos:

- Apalancamiento de Habilidades: Utiliza directamente el activo más valioso del estudiante: saber leer y escribir código. Un analista de SOC no necesita saber cómo funciona un framework como React o Spring Boot; un ingeniero de AppSec sí.

- Menor Competencia, Mayor Valor: Mientras cientos de juniors pelean por un puesto de monitoreo en un SOC, hay una escasez aguda de profesionales que puedan automatizar pruebas de seguridad en un pipeline de Jenkins o GitHub Actions.

- Resiliencia ante la IA: La IA (Copilot, ChatGPT) está automatizando la generación de código y el análisis básico de logs. Sin embargo, la integración arquitectónica de la seguridad, la decisión de qué controles implementar y la auditoría lógica de aplicaciones complejas siguen requiriendo criterio humano experto.

- Techo Salarial Superior: Al ser considerado un rol de ingeniería (Security Engineer) y no de soporte (Security Analyst), las bandas salariales se alinean con las de los Desarrolladores de Software Senior, que históricamente son más altas que las de Operaciones.3

## 8. Roadmap de Empleabilidad: De Estudiante a AppSec Junior (6 Meses)

Este plan de acción está diseñado para ejecutarse en paralelo a los estudios, con una carga estimada de 15 horas semanales. El objetivo es construir un perfil que grite "Desarrollador con especialización en Seguridad", el perfil híbrido más buscado.

### Mes 1: Fundamentos de Seguridad Web y HTTP

- Objetivo: Entender cómo se rompen las aplicaciones que sabes construir.

- Conceptos Clave:

- Protocolo HTTP/HTTPS en profundidad (Headers, Métodos, Cookies, CORS).

- OWASP Top 10: No solo memorizar la lista, sino entender la mecánica de ejecución de cada vulnerabilidad (SQLi, XSS, IDOR, SSRF).

- Práctica:

- PortSwigger Web Security Academy (Gratis): Completar todos los laboratorios del nivel "Apprentice". Es el recurso de aprendizaje práctico más respetado en la industria hoy en día.

- Leer "The Web Application Hacker's Handbook" (los conceptos siguen vigentes aunque las tecnologías cambien).

### Mes 2: Herramientas DAST y Hacking Manual

- Objetivo: Aprender a usar las herramientas que simulan ataques.

- Herramientas:

- Burp Suite Community: Aprender a interceptar tráfico, modificar peticiones y usar el Repeater.

- OWASP ZAP: La alternativa Open Source. Aprender a configurar un escaneo automático básico.36

- Proyecto: Levantar un entorno local con OWASP Juice Shop (una aplicación intencionalmente vulnerable). Intentar explotar 5 vulnerabilidades diferentes usando Burp Suite y documentar el proceso paso a paso (capturas de pantalla, payload usado, impacto).

### Mes 3: Automatización y CI/CD (El Diferencial DevSecOps)

- Objetivo: Integrar seguridad en el ciclo de desarrollo. Esto es lo que diferencia a un "hacker" de un "DevSecOps Engineer".

- Skills:

- GitHub Actions: Aprender a crear flujos de trabajo (workflows) básicos.

- SAST (Static Application Security Testing): Integrar herramientas como Semgrep o SonarCloud en un pipeline.

- SCA (Software Composition Analysis): Integrar Snyk (capa gratuita) u OWASP Dependency Check para detectar librerías vulnerables.

- Tutorial de Referencia: Estudiar implementaciones de pipelines DevSecOps con Node.js y GitHub Actions que integren ZAP y Snyk.38

### Mes 4: Contenedores y Nube (Cloud Security)

- Objetivo: Salir del "localhost" y entender entornos modernos.

- Skills:

- Docker: Aprender a escribir Dockerfiles seguros (no correr como root, usar imágenes distroless).

- Escaneo de Imágenes: Integrar Trivy en el pipeline para escanear vulnerabilidades en contenedores.

- Conceptos Cloud (AWS/Azure): Entender qué es IAM, Security Groups y S3 Buckets.

- Certificación (Hito): Preparar y rendir la ISC2 Certified in Cybersecurity (CC). Es gratuita con la promoción "One Million Certified", reconocida por RRHH y valida los conocimientos fundamentales.

### Mes 5: El "Portfolio Project" (La Prueba de Competencia)

- Objetivo: Crear la evidencia tangible que se mostrará en las entrevistas.

- Proyecto "DevSecOps-Demo": Crear un repositorio público en GitHub.

- Subir una aplicación web sencilla (ej: una API en Python/Flask o Node.js).

- Configurar un pipeline de CI/CD en GitHub Actions.

- El pipeline debe incluir: Linter, Test Unitarios, Escaneo SAST (Semgrep/Sonar), Escaneo de Dependencias (Snyk), Escaneo de Contenedores (Trivy) y un escaneo DAST ligero (ZAP Baseline Scan).

- Documentación: Escribir un README.md impecable en inglés y español explicando la arquitectura del pipeline, las herramientas elegidas y cómo cada una mitiga riesgos. Este repositorio vale más que un título junior para un reclutador técnico.39

### Mes 6: Estrategia de Búsqueda y Marca Personal

- CV y LinkedIn:

- Título: "Software Developer | Aspiring AppSec Engineer".

- Skills: Destacar CI/CD, GitHub Actions, Docker, OWASP, Python/Java.

- Inglés: Listar claramente el nivel (ej: "English: B2 - Professional Working Proficiency").

- Networking Activo:

- Asistir a un meetup de Sysarmy o OWASP. Presentarse no como "estudiante que busca trabajo", sino como "Developer pivotando a seguridad, buscando feedback sobre mi proyecto de DevSecOps".

- Aplicación:

- Filtrar búsquedas por: Junior AppSec, Security Champion, Junior DevOps, Product Security.

- Evitar la "trampa de la experiencia": Si una oferta pide 2 años de experiencia pero tenés el portafolio del Mes 5, aplica igual. El portafolio es experiencia demostrable.

## 9. Conclusiones

La ciberseguridad en Argentina para el ciclo 2024-2025 ofrece una oportunidad generacional para los estudiantes de programación que sepan leer el mercado. La estrategia ganadora no consiste en abandonar el código para aprender redes desde cero y competir por puestos saturados en un SOC, sino en capitalizar el conocimiento de desarrollo para automatizar la seguridad.

Al enfocarse en AppSec y DevSecOps, dominar el inglés para acceder al mercado global y construir un portafolio técnico tangible en GitHub, el estudiante no solo se diferencia del 90% de los candidatos junior, sino que se posiciona en el segmento de mayor crecimiento salarial y estabilidad profesional de la industria. Las herramientas están disponibles y son gratuitas; el factor determinante será la disciplina para ejecutar este plan de transición.

#### Obras citadas

- Resultados de la Encuesta de sueldos 2025.1 :: Sysarmy — El blog ..., fecha de acceso: diciembre 8, 2025,

- openqube: Resultados de la encuesta de sueldos de Junio - Julio 2025, fecha de acceso: diciembre 8, 2025,

- How niche is AppSec? Are there a lot of jobs? - cybersecurity - Reddit, fecha de acceso: diciembre 8, 2025,

- Analista de Ciberseguridad Salario en Argentina - Levels.fyi, fecha de acceso: diciembre 8, 2025,

- Salancy - Encuesta de Salarios IT en Argentina, fecha de acceso: diciembre 8, 2025,

- 2025 Cybersecurity Skills Gap Global Research Report - Fortinet, fecha de acceso: diciembre 8, 2025,

- the demand: Red Team vs Blue Team : r/cybersecurity - Reddit, fecha de acceso: diciembre 8, 2025,

- Red team vs Blue team job demand. : r/cybersecurity - Reddit, fecha de acceso: diciembre 8, 2025,

- Red Team jobs in 2025 : r/cybersecurity - Reddit, fecha de acceso: diciembre 8, 2025,

- Red Team or Blue Team, I'm confused about choosing : r/CyberSecurityJobs - Reddit, fecha de acceso: diciembre 8, 2025,

- Will the demand for pentest decline in the future - Reddit, fecha de acceso: diciembre 8, 2025,

- Blue Team vs Red Team 2025 — Which Cybersecurity Path Should You Choose?, fecha de acceso: diciembre 8, 2025,

- SOC analyst vs. security analyst: What's the difference? | Elastic Blog, fecha de acceso: diciembre 8, 2025,

- 25 Years in Appsec, willing to provide some career advice : r/SecurityCareerAdvice - Reddit, fecha de acceso: diciembre 8, 2025,

- fecha de acceso: diciembre 8, 2025,

- fecha de acceso: diciembre 8, 2025,

- $48k-$190k Junior Devsecops Engineer Jobs (NOW HIRING) Dec 25 - ZipRecruiter, fecha de acceso: diciembre 8, 2025,

- Análisis Sueldos Developers Argentina (en base al thread mensual de salarios) - Reddit, fecha de acceso: diciembre 8, 2025,

- Honorarios Recomendados – CPCI - cpcipc, fecha de acceso: diciembre 8, 2025,

- Thread mensual de sueldos - 01/2025 : r/devsarg - Reddit, fecha de acceso: diciembre 8, 2025,

- ¿Cuánto DINERO se gana en CIBERSEGURIDAD? Ciberseguridad en Argentina y LATAM, fecha de acceso: diciembre 8, 2025,

- Remote Application Security Jobs in Argentina - Himalayas.app, fecha de acceso: diciembre 8, 2025,

- Red Team vs. Blue Team: Which Cybersecurity Role Pays More in 2025? - Hackzone, fecha de acceso: diciembre 8, 2025,

- Salary: Remote Cyber Security Analyst (Dec, 2025) US - ZipRecruiter, fecha de acceso: diciembre 8, 2025,

- Support for those who give support - sysarmy, fecha de acceso: diciembre 8, 2025,

- Chapter Status | OWASP Foundation, fecha de acceso: diciembre 8, 2025,

- OWASP Buenos Aires - Meetup, fecha de acceso: diciembre 8, 2025,

- fecha de acceso: diciembre 8, 2025,

- Ekoparty Security Conference 2025: Call for Speakers - Sessionize, fecha de acceso: diciembre 8, 2025,

- Ekoparty 2025, fecha de acceso: diciembre 8, 2025,

- Villages 2025 - ekoparty security conference, fecha de acceso: diciembre 8, 2025,

- Nerdearla 2025 - September 23 to 27 - Buenos Aires, fecha de acceso: diciembre 8, 2025,

- Nerdearla 2025, fecha de acceso: diciembre 8, 2025,

- Telegram and Discord groups to learn about cybersecurity : r/ciberseguridad - Reddit, fecha de acceso: diciembre 8, 2025,

- Top 10 Telegram Cybersecurity Groups You Should Join : r/netsecstudents - Reddit, fecha de acceso: diciembre 8, 2025,

- Building a Free Python DevSecOps Pipeline with GitHub Actions and OWASP ZAP - Medium, fecha de acceso: diciembre 8, 2025,

- OWASP ZAP with Github Actions | Welcome to Nishanth's Blog, fecha de acceso: diciembre 8, 2025,

- DevSecOps code security Pipeline for a Node.js Application using GitHub Actions - Medium, fecha de acceso: diciembre 8, 2025,

- davraops/devsecops-portfolio - GitHub, fecha de acceso: diciembre 8, 2025,

- NotHarshhaa/DevOps-Projects: DevOps Real World Projects for Aspiring DevOps Engineers [Beginner to Advanced] - GitHub, fecha de acceso: diciembre 8, 2025,