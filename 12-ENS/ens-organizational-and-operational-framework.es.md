---
title: "Marco Organizacional y Operacional del ENS"
subtitle: "🏛️ Understanding the key components of the organizational and operational framework in Spain's National Security Scheme (ENS)"
tags: ["ENS", "cybersecurity"]
authors: ["alesanchezr"]

---



## Marco Organizacional

El Marco Organizacional del Esquema Nacional de Seguridad (ENS) es un conjunto de documentos, directrices y medidas relacionadas con la organización de la seguridad de la entidad. Este marco define las funciones, responsabilidades y políticas que permiten la gestión diaria y la resolución de incidentes.

![Cybersecurity Framework](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/ens/cybersecurity-framework.jpg?raw=true)

### Políticas de Seguridad

Las políticas de seguridad son un componente clave del Marco Organizacional. Son documentos que establecen directrices, normas y procedimientos a seguir para garantizar la protección de la información, sistemas, activos y recursos frente a amenazas y riesgos de seguridad.

De acuerdo con el artículo 11 del Real Decreto 3/2010, todos los órganos superiores de la Administración Pública deben contar con una política de seguridad que incluya de manera clara y precisa:

- Objetivos y misión de la organización
- Roles y funciones de seguridad, definiendo los deberes y responsabilidades de los cargos, así como los procedimientos de asignación y renovación
- Marco legal y normativo en el que se desarrollarán las actividades
- Estructura del comité de gestión y coordinación de la seguridad, detallando responsabilidades
- Directrices para estructurar la documentación de seguridad del sistema, su gestión y acceso

También se recomienda establecer planes de concienciación y formación del personal sobre las acciones de seguridad, contar con un plan de gestión de riesgos y saber cómo manejar posibles incidentes de seguridad. Estas políticas deben someterse a revisiones periódicas para mejorar su efectividad.

El ENS establece que las políticas de seguridad deben aplicarse en niveles bajo, medio y alto:

| Dimensiones |  |  | Medidas de Seguridad |  |
| --- | --- | --- | --- | --- |
| B | M | A | Org | Marco Organizacional |
| Aplica | = | = | Org.1 | Políticas de Seguridad |

**Explicación de Org.1 Políticas de Seguridad:**

Esta medida requiere que las políticas de seguridad se implementen en todos los niveles de seguridad (Bajo, Medio y Alto). El "Aplica" en la columna Bajo (B) y los signos "=" en las columnas Medio (M) y Alto (A) indican que los mismos requisitos básicos se aplican en todos los niveles, sin requisitos adicionales para los niveles superiores.

En términos más simples:
- Cada organización, independientemente de su nivel de seguridad, debe tener políticas de seguridad claramente definidas.
- Estas políticas deben describir los objetivos de seguridad, roles, responsabilidades y directrices de la organización.
- Las políticas deben ser apropiadas para el tamaño y la complejidad de la organización, pero el requisito básico de tenerlas existe en todos los niveles de seguridad.

### Normativas y Procedimientos de Seguridad

Las normativas de seguridad son otro control crucial dentro del marco organizacional. Establecen el uso correcto de los sistemas de información y los activos, así como las responsabilidades del personal en cuanto al cumplimiento o incumplimiento de estas normas establecidas.

El ENS establece que las normativas de seguridad deben abordar:

1. Uso correcto de los equipos, servicios e instalaciones
2. Qué se considera un uso indebido
3. Responsabilidad del personal en cuanto al cumplimiento o incumplimiento de estas normas: derechos, deberes y medidas disciplinarias de acuerdo con la legislación vigente

Los procedimientos de seguridad son documentos que describen paso a paso cómo realizar ciertas actividades. El ENS establece que estos documentos deben incluir:

1. Cómo llevar a cabo las tareas rutinarias
2. Quién debe realizar cada tarea
3. Cómo identificar y reportar comportamientos anómalos

Tanto las normativas de seguridad como los procedimientos deben aplicarse en todos los niveles:

| Dimensiones |  |  | Medidas de Seguridad |  |
| --- | --- | --- | --- | --- |
| B | M | A | Org | Marco Organizacional |
| Aplica | = | = | Org.2 | Normativas de Seguridad |
| Aplica | = | = | Org.3 | Procedimientos de Seguridad |

En resumen:
- Org.1 (Políticas) se aplica a todos los niveles y establece la dirección general de seguridad.
- Org.2 (Normativas) añade reglas más detalladas para los niveles Medio y Alto.
- Org.3 (Procedimientos) proporciona las instrucciones de seguridad más detalladas, requeridas solo para entornos de seguridad de nivel Alto.

### Procesos de Autorización

El último control establecido dentro del marco organizacional son los procesos de autorización. Estos tienen como objetivo establecer cómo será el proceso para autorizar a un usuario o componente para que ingrese y forme parte del sistema de la entidad.

Según el ENS, estos procesos deben cubrir:

1. Uso de las instalaciones, tanto regulares como alternativas
2. Ingreso de equipos a producción, en particular los que involucran criptografía
3. Ingreso de aplicaciones a producción
4. Establecimiento de enlaces de comunicación con otros sistemas
5. Uso de medios de comunicación, tanto regulares como alternativos
6. Uso de soportes de información
7. Uso de equipos móviles (portátiles, PDAs, etc.)
8. Uso de servicios de terceros, bajo contrato o acuerdo

Los procesos de autorización deben aplicarse en todos los niveles:

| Dimensiones |  |  | Medidas de Seguridad |  |
| --- | --- | --- | --- | --- |
| B | M | A | Org | Marco Organizacional |
| Aplica | = | = | Org.4 | Procesos de Autorización |

## Marco Operacional

El Marco Operacional se refiere a una serie de medidas que deben tomarse para proteger el funcionamiento del sistema como un conjunto integral de componentes para un propósito. Este marco juega un papel esencial en proporcionar la estructura necesaria para implementar y gestionar eficazmente las medidas de seguridad.

### Planificación de la Seguridad

La planificación de la seguridad dentro del marco operacional es uno de los componentes más importantes del ENS. Implica un proceso estratégico que guía a las organizaciones en la identificación y gestión de riesgos, la implementación de medidas de seguridad y la preparación para responder a incidentes.

La planificación de la seguridad consta de varias etapas:

#### Análisis de Riesgos

Esto implica una evaluación integral de los riesgos que enfrentan la información y los sistemas. El análisis identifica posibles amenazas, evalúa su impacto y determina la probabilidad de que ocurran.

El ENS establece diferentes requisitos para el análisis de riesgos según la categoría del sistema:

- Sistemas de Categoría Básica: Un análisis simple que muestre los activos más valiosos, las amenazas más probables, las salvaguardas que protegen contra estas amenazas y los principales riesgos residuales.
- Sistemas de Categoría Media: Un análisis semiformal con una presentación tabular que describa y valore cualitativamente los activos, cuantifique las amenazas, valore las salvaguardas y evalúe el riesgo residual.
- Sistemas de Categoría Alta: Un análisis formal con cálculos matemáticos que cubra la valoración de activos, amenazas posibles, vulnerabilidades habilitantes, salvaguardas adecuadas y evaluación de riesgos residuales.

| Dimensiones |  |  | Medidas de Seguridad |  |
| --- | --- | --- | --- | --- |
| B | M | A | Org | Marco Operacional |
| Aplica | + | ++ | op.pl.1 | Análisis de Riesgos |

#### Arquitectura de Seguridad

Esta es la estructura fundamental que respalda la salvaguarda de la información sensible en las administraciones públicas. Está diseñada para establecer un entorno seguro, garantizando la confidencialidad, integridad y disponibilidad de los sistemas y datos en un contexto digital en constante evolución.

El ENS establece diferentes requisitos para la arquitectura de seguridad según la categoría del sistema:

- Sistemas de Categoría Básica: Documentación de instalaciones, documentación del sistema, esquema de líneas de defensa y sistema de identificación y autenticación de usuarios.
- Sistemas de Categoría Media: Sistema de gestión relacionado con la planificación, organización y control de los recursos de seguridad de la información.
- Sistemas de Categoría Alta: Sistema de gestión de seguridad de la información con actualización y aprobación periódica, y controles técnicos internos.

| Dimensiones |  |  | Medidas de Seguridad |  |
| --- | --- | --- | --- | --- |
| B | M | A | Org | Marco Operacional |
| Aplica | + | ++ | op.pl.2 | Arquitectura de Seguridad |

#### Adquisición de Nuevos Componentes

Este proceso se realiza con el objetivo de fortalecer la infraestructura de seguridad dentro de la administración pública. Estos componentes deben cumplir con las normas del ENS y deben poder integrarse en el sistema existente.

| Dimensiones |  |  | Medidas de Seguridad |  |
| --- | --- | --- | --- | --- |
| B | M | A | Org | Marco Operacional |
| Aplica | = | = | op.pl.3 | Adquisición de Nuevos Componentes |

#### Gestión de Capacidades

Esto se enfoca en identificar, adquirir y desarrollar las capacidades necesarias para garantizar la integridad, confidencialidad y disponibilidad de la información, enfrentando así los desafíos cambiantes del entorno cibernético.

| Dimensiones |  |  | Medidas de Seguridad |  |
| --- | --- | --- | --- | --- |
| B | M | A | Org | Marco Operacional |
| N/A | Aplica | = | op.pl.4 | Gestión de Capacidades |

### Otros Controles Operacionales

El ENS también establece otros controles operacionales como:

- Gestión de la Configuración
- Mantenimiento
- Gestión de Cambios
- Protección contra Código Malicioso
- Gestión de Incidentes
- Registro de Actividad de Usuarios
- Protección de Registros de Actividad
- Protección de Claves Criptográficas
- Gestión de Servicios Externos

Cada uno de estos controles tiene requisitos específicos y aplicabilidad según lacategoría del sistema (Bajo, Medio, Alto).

Al implementar estos marcos organizacional y operacional, las administraciones públicas pueden asegurar un enfoque integral para la seguridad de la información, alineándose con los requisitos del Esquema Nacional de Seguridad.