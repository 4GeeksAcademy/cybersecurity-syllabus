---
title: "Principios del Marco de Ciberseguridad de NIST"
subtitle: "🛡️ Comprendiendo los componentes clave y funciones del Marco de Ciberseguridad NIST para una gestión efectiva de la seguridad de la información"
tags: ["NIST", "cybersecurity"]
authors: ["alesanchezr"]

---

El **marco de Ciberseguridad** ó **NIST Framework** es una guía desarrollada para proporcionar un enfoque estructurado para gestionar y mejorar ciberseguridad de una organización. Este framework consta de tres componentes principales: el Núcleo, los perfiles y los planes de acción.

El núcleo del [NIST Cybersecurity Framework 2.0](https://www.nist.gov/cyberframework) (también conocido como Core) es un conjunto estructurado de resultados deseados y buenas prácticas para gestionar los riesgos de ciberseguridad. Se organiza en seis funciones clave: Gobernar, identificar, proteger, detectar, responder y recuperar. Estas funciones se dividen a su vez en **categorías** y **subcategorías** que ayudan a establecer prioridades, medir capacidades y definir planes de mejora.

El núcleo se divide en seis funciones principales:

- Gobernar
- Identificar
- Proteger
- Detectar
- Responder
- Recuperar


![Marco de Ciberseguridad de NIST](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/marco-de-ciberseguridad-de-nist.png)

Cada función del Core contiene **categorías** y **subcategorías** que permiten detallar acciones específicas y objetivos de seguridad, ofreciendo así una estructura flexible pero clara para su aplicación práctica.

## Funciones del NIST Cybersecurity Framework 2.0

El **CSF 2.0** introduce una estructura actualizada con **seis funciones clave** que representan el ciclo completo de gestión del riesgo cibernético. Cada función se compone de **categorías** (grupos temáticos) y **subcategorías** (resultados deseados específicos). Esta organización permite a cualquier organización, pública o privada, adaptarlo según su realidad y madurez.

### 1. Gobernar – Gobernanza de la Ciberseguridad

| Categoría | Descripción | Subcategorías (ejemplos) |
|-----------|-------------|---------------------------|
| GV.RM - Estrategia de Gestión de Riesgos | Estrategia formalizada y comunicada | GV.RM-1: La estrategia de riesgo está documentada y alineada con los objetivos organizacionales |
| GV.OV - Contexto Organizacional | Comprensión de misión, entorno y obligaciones legales | GV.OV-1: Se identifican responsabilidades y límites regulatorios |
| GV.PO - Políticas y Procedimientos | Políticas y procedimientos establecidos | GV.PO-1: Las políticas están documentadas y se revisan regularmente |
| GV.SU - Gestión de Riesgos en la Cadena de Suministro | Riesgos de terceros gestionados eficazmente | GV.SU-1: Existen acuerdos y monitoreo sobre seguridad con proveedores |


### 2. Identificar – Comprensión del contexto

| Categoría | Descripción | Subcategorías (ejemplos) |
|-----------|-------------|---------------------------|
| ID.AM - Gestión de Activos | Inventario completo de activos físicos y digitales | ID.AM-1: Se identifican los dispositivos físicos<br>ID.AM-2: Se identifican los activos de software |
| ID.BE - Entorno Empresarial | Identificación de funciones y dependencias críticas | ID.BE-1: Se comprenden las funciones críticas<br>ID.BE-2: Se documentan dependencias internas y externas |
| ID.RA - Evaluación de Riesgos | Evaluación continua de amenazas y vulnerabilidades | ID.RA-1: Se identifican amenazas relevantes<br>ID.RA-2: Se evalúan vulnerabilidades existentes |
| ID.RM - Gestión de Riesgos | Priorización de riesgos | ID.RM-1: Se determinan niveles aceptables de riesgo<br>ID.RM-2: Se documentan respuestas ante riesgos priorizados |


### 3. Proteger – Implementación de salvaguardas

| Categoría | Descripción | Subcategorías (ejemplos) |
|-----------|-------------|---------------------------|
| PR.AC - Control de Acceso | Gestión de identidades y control de accesos | PR.AC-1: Solo usuarios autorizados pueden acceder a sistemas |
| PR.AT - Concientización y Capacitación | Formación continua del personal | PR.AT-1: Se brinda capacitación periódica sobre ciberseguridad |
| PR.DS - Seguridad de los Datos | Protección de datos en tránsito y reposo | PR.DS-1: La información está cifrada y protegida |
| PR.IP - Procesos de Protección de la Información | Procedimientos definidos para proteger activos | PR.IP-1: Se aplican configuraciones seguras y gestión de cambios |
| PR.MA - Mantenimiento | Mantenimiento seguro y documentado | PR.MA-1: Se realizan mantenimientos con control de acceso |
| PR.PT - Tecnologías de Protección | Tecnologías de protección implementadas | PR.PT-1: Se utilizan firewalls, antivirus, IDS/IPS y control de ejecución |


### 4. Detectar – Identificación de anomalías

| Categoría | Descripción | Subcategorías (ejemplos) |
|-----------|-------------|---------------------------|
| DE.AE - Anomalías y Eventos | Detección de actividades anómalas | DE.AE-1: Se definen comportamientos esperados<br>DE.AE-2: Se detectan desviaciones |
| DE.CM - Monitoreo Continuo | Monitoreo continuo de redes y sistemas | DE.CM-1: Se monitorean eventos de seguridad<br>DE.CM-2: Se recogen y analizan logs |
| DE.DP - Procesos de Detección | Evaluación de efectividad de detección | DE.DP-1: Se revisan los procesos de detección periódicamente |


### 5. Responder – Respuesta ante incidentes

| Categoría | Descripción | Subcategorías (ejemplos) |
|-----------|-------------|---------------------------|
| RS.RP - Planificación de respuesta | Preparación para responder a incidentes | RS.RP-1: Existe un plan de respuesta documentado y aprobado |
| RS.CO - Comunicaciones | Comunicación interna y externa durante incidentes | RS.CO-1: Se establecen contactos para reportar incidentes<br>RS.CO-2: Se informa a las partes interesadas |
| RS.AN - Análisis | Análisis del impacto del incidente | RS.AN-1: Se analiza el incidente para determinar alcance y causa |
| RS.MI - Mitigación | Reducción del impacto | RS.MI-1: Se mitigan los efectos del incidente |
| RS.IM - Mejora | Lecciones aprendidas | RS.IM-1: Se actualizan planes y procedimientos post-incidente |

### 6. Recuperar – Restauración de capacidades

| Categoría | Descripción | Subcategorías (ejemplos) |
|-----------|-------------|---------------------------|
| RC.RP - Planificación de Recuperación | Planes formales para restauración de servicios | RC.RP-1: Se documentan y prueban planes de recuperación |
| RC.IM - Mejoras | Mejora continua tras incidentes | RC.IM-1: Se aplican lecciones aprendidas en futuros planes |
| RC.CO - Comunicaciones | Comunicación efectiva durante recuperación | RC.CO-1: Se comunica el estado de recuperación a partes interesadas |

> 💡 Esta estructura actualizada permite a las organizaciones realizar diagnósticos más precisos, construir perfiles personalizados y aplicar el Framework como una hoja de ruta realista para mejorar su postura de seguridad cibernética.

Además de las funciones, el NIST Framework define cuatro niveles de implementación o madurez organizacional, llamados **Tiers**, que permiten entender hasta qué punto una organización ha integrado la gestión de riesgos en su cultura y operaciones.

## Tiers o niveles de madurez del riesgo

Los *Tiers* ayudan a una organización a evaluar el grado en que su gestión de riesgos cibernéticos está formalizada, integrada y adaptativa. No representan niveles de madurez obligatorios, sino puntos de referencia para guiar mejoras.

- **Tier 1 – Parcial (Partial)**
    - La gestión de riesgos es improvisada y sin planificación: se actúa solo cuando ocurre un problema, sin medidas preventivas establecidas.
    - La organización no tiene procesos formalizados.
    - No hay una integración entre los objetivos de ciberseguridad y los objetivos del negocio.
    - La alta dirección rara vez está involucrada.

- **Tier 2 – Informado (Risk Informed)**
    - Existen procesos de gestión de riesgos, pero no están implementados de manera uniforme.
    - Algunas funciones están informadas sobre los riesgos cibernéticos.
    - Las decisiones sobre ciberseguridad se toman parcialmente en base al conocimiento del riesgo.
    - Falta una alineación clara entre todas las áreas de la organización.

- **Tier 3 – Repetible (Repeatable)**
    - La organización ha desarrollado políticas y procedimientos formales.
    - Las prácticas de ciberseguridad están documentadas, revisadas y mantenidas.
    - Hay integración con los objetivos estratégicos.
    - Se revisan y actualizan planes de respuesta y recuperación.

- **Tier 4 – Adaptativo (Adaptive)**
    - La organización tiene una cultura de mejora continua.
    - Se adapta dinámicamente a cambios en el entorno y nuevas amenazas.
    - Utiliza inteligencia de amenazas para anticiparse a incidentes.
    - La ciberseguridad es una prioridad en todos los niveles de decisión.


> Estos niveles no son una escala de calidad, sino una herramienta para ayudar a cada organización a entender su punto de partida y planificar mejoras.

## ¿Qué es un perfil en el NIST Cybersecurity Framework?

Un **perfil** en el contexto del NIST CSF es una representación personalizada del **Core** del framework, adaptada a la realidad específica de una organización. No todas las organizaciones enfrentan los mismos riesgos ni disponen de los mismos recursos, por lo que el perfil permite alinear los objetivos de ciberseguridad con las prioridades operativas.

Por ejemplo un perfil podria reflejar lo siguiente:

- Las **prioridades del negocio**: ejemplo, si la continuidad del servicio es más crítica que la confidencialidad de los datos.
- El **entorno operativo**: incluyendo sector, tamaño, normativas aplicables y complejidad tecnológica.
- La **tolerancia al riesgo**: cuánto riesgo está dispuesta a aceptar la organización según su apetito y capacidades.
- Los **recursos disponibles**: tanto humanos como técnicos y presupuestarios.

#### Tipos de perfiles

- **Perfil actual** (*Current Profile*): Describe el estado real de la organización frente a cada subcategoría del Core. Se basa en evidencias, prácticas existentes y evaluaciones internas o externas.
- **Perfil objetivo** (*Target Profile*): Representa la situación ideal que la organización quiere alcanzar. Se basa en su estrategia, políticas y objetivos de gestión de riesgos.

### ¿Para qué sirve comparar perfiles?

La comparación entre el perfil actual y el perfil objetivo permite:

- Identificar brechas y vulnerabilidades.
- Priorizar acciones de mejora de acuerdo con el impacto y el esfuerzo.
- Justificar presupuestos y estrategias de implementación.
- Medir el progreso a lo largo del tiempo.

> 💡 El perfil es un **instrumento dinámico**, que debe actualizarse regularmente a medida que cambian las amenazas, los recursos o los objetivos del negocio.

## ¿Por qué adoptar el NIST CSF?

- Proporciona un lenguaje común entre equipos técnicos y ejecutivos.
- Es adaptable a cualquier tamaño o sector organizacional.
- Permite priorizar inversiones en ciberseguridad según el riesgo.
- Facilita auditorías y alineación con otras normas como ISO/IEC 27001.
- Mejora la resiliencia organizacional y la respuesta ante incidentes.

Además que comprender y aplicar estos principios permitirá a los profesionales de ciberseguridad implementar una postura sólida, medible y evolutiva dentro de cualquier organización. Incluso en entornos donde no existen controles previos, el [NIST CSF 2.0](https://www.nist.gov/cyberframework/quick-start-guides) actúa como una hoja de ruta clara y efectiva para comenzar desde cero o mejorar continuamente.