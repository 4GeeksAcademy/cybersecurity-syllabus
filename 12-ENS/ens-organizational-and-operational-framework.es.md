---
title: "Marco Organizacional y Operacional del ENS"
subtitle: "🏛️ Understanding the key components of the organizational and operational framework in Spain's National Security Scheme (ENS)"
tags: ["ENS", "ciberseguridad"]
authors: ["alesanchezr"]

---

Antes de leer este artículo, asumimos que ya tienes algunos conocimientos sobre el ENS y lo que implica. De no ser así, te recomendamos leer nuestra [introducción al Esquema Nacional de Seguridad de España](https://4geeks.com/es/lesson/introduccion-al-ens-esquema-nacional-de-seguridad).

## Marco Organizativo del ENS

El Marco Organizativo del Esquema Nacional de Seguridad (ENS), regulado por el Real Decreto 311/2022, define las funciones, responsabilidades, políticas y medidas necesarias para organizar la seguridad en una entidad. Su objetivo es establecer una estructura clara que facilite la gestión diaria de la seguridad y la respuesta ante incidentes.

![Cybersecurity Framework](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/ens/cybersecurity-framework.jpg?raw=true)

### Políticas de Seguridad (Org.1)

Las políticas de seguridad son el eje central del marco organizativo. Establecen las directrices generales para proteger la información y los activos frente a amenazas. Estas políticas deben incluir:

- Objetivos y misión de la organización en materia de seguridad  
- Roles y responsabilidades  
- Comité de seguridad y estructura de gobernanza  
- Documentación de seguridad y procedimientos de acceso  
- Revisión periódica de su eficacia

| Nivel | Bajo | Medio | Alto |
|-------|------|-------|------|
| Org.1 | ✓    | =     | =    |

> Esta medida se aplica en todos los niveles. El símbolo `=` indica que no hay requisitos adicionales para niveles superiores.

### Normativas y Procedimientos de Seguridad (Org.2 y Org.3)

Las medidas **Org.2** y **Org.3** forman parte del conjunto de controles organizativos fundamentales del ENS. Estas medidas establecen las reglas de uso de los sistemas de información, así como las instrucciones detalladas para operarlos de manera segura.

#### Org.2 – Normativas de Seguridad

Las normativas de seguridad son **documentos normativos internos** que fijan las condiciones de uso aceptable de los sistemas, servicios y recursos tecnológicos de la organización. Su propósito es:

- Prevenir comportamientos indebidos por parte del personal.  
- Establecer **derechos y deberes** de los usuarios.  
- Definir el marco de **responsabilidad disciplinaria** en caso de incumplimiento.  
- Homogeneizar el uso seguro de los activos en toda la entidad.

Estas normativas deben ser conocidas, comprendidas y aceptadas por todos los usuarios con acceso a los sistemas. Su cumplimiento es obligatorio.

#### Org.3 – Procedimientos de Seguridad

Los procedimientos de seguridad detallan **cómo deben ejecutarse de forma segura** tareas específicas dentro del sistema. Actúan como guías operativas que:

- Describen paso a paso las acciones requeridas.  
- Identifican qué roles o perfiles deben ejecutarlas.  
- Incluyen criterios para **detectar comportamientos anómalos** o fallos de seguridad.  
- Favorecen la continuidad operativa y la trazabilidad de acciones.

Estos procedimientos deben ser actualizados periódicamente, fácilmente accesibles y compatibles con las normativas y políticas existentes.

#### Tabla de aplicabilidad:

| Nivel de seguridad | Bajo | Medio | Alto |
|--------------------|------|-------|------|
| Org.2 - Normativas | ✓    | +     | ++   |
| Org.3 - Procedimientos | ✓ | +     | ++   |

> En nivel **Bajo**, se exige al menos una normativa y un procedimiento base.  
> En **Medio y Alto**, se requiere mayor granularidad, segmentación por perfiles, escenarios específicos (como emergencia o administración remota) y auditoría formal de su eficacia.


### Procesos de Autorización (Org.4)

La medida **Org.4** regula los mecanismos mediante los cuales se concede o deniega acceso a los distintos componentes del sistema. Esta medida abarca tanto **personas como equipos, software o enlaces de comunicación**, y es clave para prevenir accesos no autorizados.

Los procesos de autorización deben:

- Estar documentados formalmente.  
- Incluir criterios claros de evaluación y aprobación.  
- Garantizar la trazabilidad de todas las autorizaciones concedidas o revocadas.  
- Aplicarse de forma coherente en situaciones regulares y extraordinarias (por ejemplo, reemplazos, subcontrataciones, movilidad).

#### Algunos elementos típicos que deben estar sujetos a autorización previa:

- **Instalaciones físicas** (acceso a CPDs, oficinas seguras, áreas restringidas).  
- **Equipos en producción**, especialmente los que contienen datos sensibles o funciones críticas.  
- **Aplicaciones y actualizaciones** que se incorporan al entorno activo.  
- **Conexiones externas**, como túneles VPN o enlaces con otros sistemas.  
- **Medios de almacenamiento**, como discos duros, pendrives o backups en la nube.  
- **Dispositivos móviles**, como portátiles, tablets o smartphones corporativos.  
- **Servicios de terceros**, especialmente si manejan datos clasificados o realizan tareas sensibles.

#### Tabla de aplicabilidad:

| Nivel de seguridad | Bajo | Medio | Alto |
|--------------------|------|-------|------|
| Org.4 - Procesos de Autorización | ✓ | =     | =    |

> Esta medida se aplica de forma uniforme en todos los niveles, aunque el grado de control, automatización y trazabilidad puede incrementarse según la criticidad del entorno.

## Perfil de cumplimiento

Las medidas del ENS no se aplican de forma rígida, sino que están condicionadas por el **perfil de cumplimiento** del sistema, definido según:

- Nivel de seguridad del sistema (bajo, medio o alto)  
- Riesgo asociado a los servicios y datos tratados  
- Madurez organizativa y recursos disponibles

Este enfoque permite **ajustar la aplicación de las medidas de forma proporcional y razonable**, evitando cargas innecesarias en sistemas de bajo impacto.

## Marco Operacional

El Marco Operacional se refiere a una serie de medidas que deben tomarse para proteger el funcionamiento del sistema como un conjunto integral de componentes para un propósito. Este marco juega un papel esencial en proporcionar la estructura necesaria para implementar y gestionar eficazmente las medidas de seguridad.


### Planificación de la Seguridad

La planificación de la seguridad dentro del marco operacional es uno de los componentes más importantes del ENS. Implica un proceso estratégico que guía a las organizaciones en la identificación y gestión de riesgos, la implementación de medidas de seguridad y la preparación para responder a incidentes. La planificación de la seguridad consta de varias etapas:

#### Análisis de Riesgos (op.pl.1)

El análisis de riesgos es el proceso que permite a la organización **identificar, evaluar y priorizar amenazas y vulnerabilidades** que afectan a la información y los sistemas. Este análisis debe incluir:

- Identificación de activos (datos, servicios, infraestructuras).
- Evaluación de amenazas (internas, externas, accidentales o maliciosas).
- Valoración de vulnerabilidades y su explotabilidad.
- Estimación del **impacto potencial** y la **probabilidad de ocurrencia**.
- Identificación de salvaguardas existentes y **riesgos residuales**.
- Recomendaciones de medidas de mitigación adaptadas al perfil del sistema.

La profundidad del análisis dependerá del nivel de seguridad asignado al sistema:

| Nivel de seguridad | Requisito |
|--------------------|-----------|
| Bajo               | Evaluación simple, cualitativa, basada en activos clave. |
| Medio              | Análisis semiformal, con representación tabular y valores cualitativos. |
| Alto               | Análisis formal, con métricas cuantitativas y herramientas especializadas. |

| Nivel | Bajo | Medio | Alto |
|-------|------|-------|------|
| op.pl.1 | ✓  | +     | ++   |

---

#### Arquitectura de Seguridad (op.pl.2)

La arquitectura de seguridad define la **estructura técnica, lógica y organizativa** que protege los sistemas de la entidad frente a ataques o fallos.

Esta medida abarca:

- Diseño de la **topología de red segura** (segmentación, zonas desmilitarizadas, firewalls).
- Mecanismos de **autenticación e identificación** robustos.
- Control de accesos y privilegios (principio de menor privilegio).
- Uso de **líneas de defensa** (defensa en profundidad).
- Gestión de identidades y ciclo de vida de usuarios.
- Supervisión y mantenimiento de las configuraciones seguras.

La complejidad y profundidad de esta arquitectura aumentan según el nivel de seguridad:

| Nivel de seguridad | Requisitos clave |
|--------------------|------------------|
| Bajo               | Documentación básica de sistemas, autenticación básica. |
| Medio              | Gestión organizada de configuraciones y actualizaciones. |
| Alto               | SGSI integrado con controles internos y planes de mejora continua. |

| Nivel | Bajo | Medio | Alto |
|-------|------|-------|------|
| op.pl.2 | ✓  | +     | ++   |

---

#### Adquisición de Nuevos Componentes (op.pl.3)

Esta medida exige que **todo nuevo elemento tecnológico** (hardware, software, servicios) adquirido o desarrollado por la organización **cumpla con los requisitos de seguridad establecidos por el ENS** antes de ser desplegado.

Incluye:

- Validación de seguridad en la fase de **adquisición o contratación**.  
- Evaluación de cumplimiento normativo del proveedor.  
- Revisión de **licencias, actualizaciones y ciclo de vida** del producto.  
- Integración segura en el entorno de la organización (evitar introducir vulnerabilidades).  
- Registro y control de cambios en el inventario de activos.

| Nivel | Bajo | Medio | Alto |
|-------|------|-------|------|
| op.pl.3 | ✓  | =     | =    |

> El símbolo "=" indica que el mismo conjunto de requisitos debe cumplirse en todos los niveles de seguridad.

---

#### Gestión de Capacidades (op.pl.4)

Esta medida garantiza que la organización disponga de las **capacidades humanas, técnicas y operativas suficientes** para mantener la seguridad de sus sistemas y servicios.

Abarca:

- Formación continua del personal en ciberseguridad, concienciación y buenas prácticas.
- Dotación adecuada de **herramientas y recursos técnicos**.
- Asignación de responsabilidades claras y perfiles cualificados.
- Evaluación periódica de **capacidades internas y externas** para responder a incidentes.
- Preparación ante la evolución de amenazas y tecnologías emergentes.

| Nivel | Bajo | Medio | Alto |
|-------|------|-------|------|
| op.pl.4 | —  | ✓     | =    |

> En nivel **Bajo**, esta medida no es obligatoria.  
> En **Medio y Alto**, se exige implementar programas formativos y estructuras organizativas que respalden eficazmente la gestión de la seguridad.

### Otros controles operacionales (referencia al Anexo II)

El ENS incluye otras medidas clave que también deben implementarse según el perfil de cumplimiento. Algunas de ellas son:

- **Gestión de la configuración** (`op.ex.1`)  
- **Mantenimiento seguro** (`op.ex.3`)  
- **Gestión de cambios** (`op.ex.4`)  
- **Protección contra malware** (`op.pro.1`)  
- **Gestión de incidentes** (`op.mon.6`)  
- **Registro y monitoreo de actividad** (`op.mon.1`, `op.mon.4`)  
- **Gestión de claves criptográficas** (`op.pro.5`)  
- **Control de servicios externos** (`op.ext.1`)

Cada una tiene una aplicabilidad distinta según el nivel del sistema.


Al implementar estos marcos organizacional y operacional, las administraciones públicas pueden asegurar un enfoque integral para la seguridad de la información, alineándose con los requisitos del Esquema Nacional de Seguridad.
