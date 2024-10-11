---
title: "Implementación y Medidas de Seguridad del ENS"
subtitle: "🛡️ Comprendiendo los componentes clave de la implementación y las medidas de seguridad en el Esquema Nacional de Seguridad (ENS) de España"
tags: ["ENS", "ciberseguridad"]
authors: ["alesanchezr"]

---

# Implementación y Medidas de Seguridad del ENS

> Antes de comenzar, cubrimos exhaustivamente el ENS (Esquema Nacional de Seguridad) en varias lecciones. Esta lección se centra únicamente en las medidas de seguridad y la implementación.
> Lee una [Introducción al ENS](https://4geeks.com/es/lesson/introduccion-al-ens-esquema-nacional-de-seguridad) y aprende más sobre el [Marco organizativo y operativo del ENS](https://4geeks.com/es/lesson/marco-organizacional-y-operacional-del-ens).

Para implementar el Esquema Nacional de Seguridad (ENS) de España 🇪🇸, primero necesitamos nombrar un comité que será responsable de la implementación del esquema.

![Implementación del ENS](https://github.com/4GeeksAcademy/cybersecurity-syllabus/raw/main/assets/12-ens/esquema-nacional-de-seguridad.jpg?raw=true)

## ¿Quién es responsable de la implementación del ENS dentro de una organización?

Desde 2022, el ENS se rige por el [Real Decreto 311/2022](https://www.boe.es/buscar/act.php?id=BOE-A-2022-12345) y establece 4 roles en 2 niveles según su artículo 11. Estos roles también se detallan en [la Guía 801 del Centro Criptológico Nacional](https://www.ccn-cert.cni.es/es/series-ccn-stic/800-guia-esquema-nacional-de-seguridad/501-ccn-stic-801-responsabilidades-y-funciones-en-el-ens/file?format=html).

### Composición del comité

> 💡 Aunque el ENS define roles distintos con responsabilidades específicas, es importante tener en cuenta que en la práctica, especialmente en organizaciones más pequeñas o aquellas con recursos limitados

Este comité estará compuesto por un presidente que tendrá el papel de moderador de las reuniones y en caso de empate en la votación, tendrá el voto de calidad, algunos miembros que tendrán voz y voto dentro de las reuniones y un secretario del comité que se encarga de las convocatorias y lee las actas de las últimas reuniones:

### Responsable de la Información 🧑‍💼📊

Determina los requisitos de seguridad de la información tratada según los parámetros del Anexo I del ENS. Puede ser una persona o un órgano colegiado.

### Responsable del Servicio 🛠️👨‍💼

- Ayuda a determinar los requisitos de seguridad de los servicios que se prestan, identificando los niveles de seguridad de estos mediante la evaluación del impacto de los incidentes sobre ellos, y proporcionando la información necesaria para realizar los respectivos análisis de riesgos para establecer las salvaguardas a implementar.
- Cuenta con la ayuda del responsable del sistema para realizar sus tareas.

### Responsable de Seguridad (CISO) 🕵️‍♂️🔒

- Desarrolla Planes con Medidas para gestionar los riesgos detectados.
- Supervisa y desarrolla políticas, normativas y procedimientos de seguridad, su eficacia... Realizando controles periódicos.
- Prepara el documento de Declaración de Aplicabilidad de medidas de seguridad.
- Promueve y forma sobre las "mejores prácticas" de la organización en materia de ciberseguridad.
- Presenta notificaciones de incidentes con efectos adversos a la autoridad competente.
- Recibe, interpreta y supervisa la aplicación de instrucciones y directrices de la autoridad competente.
- Recopila y proporciona información o documentación a la autoridad competente.

### Responsable del Sistema 💻🛠️

- Desarrolla, opera y mantiene el sistema.
- Define la tipología y política de Gestión del Sistema.
- La conexión/desconexión de equipos/usuarios.
- Aprueba cambios operativos que afecten al sistema.
- Decide sobre las medidas de seguridad a aplicar por los proveedores de componentes.
- Implementa, controla e integra medidas de seguridad específicas.
- La configuración autorizada y la aprobación de modificaciones sustanciales de hardware y software.
- Mantiene actualizado el Análisis de Riesgos en el sistema.
- Determina la Categoría del Sistema (proceso en Anexo I ENS) y las medidas de seguridad que deben aplicarse (Anexo II ENS).
- Elabora y aprueba la documentación del sistema y determina las responsabilidades de los implicados en el mantenimiento, explotación, implantación y supervisión del sistema.
- Investiga Incidentes de Seguridad y los comunica a quien corresponda si procede.
- Establece Planes de Contingencia o Emergencia y realiza ejercicios programados.
- Acuerda el uso de cierta información o prestación de servicio si existen vulnerabilidades graves en el sistema, decisión acordada previamente con el Responsable de Seguridad.

## Implementación del ENS

![Implementación del ENS](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/12-ens/proceso-ens.png?raw=true)

Para implementar un Sistema de Gestión de Seguridad de la Información (SGSI) que cumpla con el Esquema Nacional de Seguridad (ENS) de España, necesitarás seguir un enfoque estructurado que se alinee con el marco regulatorio. A continuación, se presenta un plan de implementación paso a paso:

### 1. **Comprender los requisitos del ENS**

- **Clasificación de sistemas:** El ENS define diferentes niveles de seguridad (Básico, Medio y Alto). Comienza clasificando tus sistemas de información basándote en la sensibilidad y criticidad de los datos manejados.
- **Medidas de Seguridad:** Cada nivel requiere medidas de seguridad específicas (administrativas, técnicas y operativas). Revisa el Anexo II y el Anexo III del ENS para los requisitos detallados.
- **Revisión Legal:** Estado actual del cumplimiento de la organización con las leyes españolas relacionadas (por ejemplo, RGPD, Ley Orgánica de Protección de Datos).

### 2. **Análisis de Brechas**

- **Evaluación del Estado Actual:** Realiza un análisis exhaustivo de tu postura de seguridad actual. Evalúa las medidas, políticas y procedimientos de seguridad existentes.
- **Identificación de Brechas:** Compara tus controles de seguridad actuales con los requisitos del ENS. Identifica las brechas tanto en aspectos técnicos (por ejemplo, firewalls, encriptación) como organizativos (por ejemplo, políticas, gestión de riesgos).

### 3. **Establecer un Marco de Gobernanza de Seguridad**

- **Nombrar un Responsable de Seguridad:** Designa un responsable de seguridad encargado del cumplimiento del ENS y asegúrate de que esté adecuadamente formado.
- **Crear un Comité de Seguridad:** Establece un comité con representantes de TI, legal, RRHH y otros departamentos relevantes para supervisar el programa de seguridad.

### 4. **Desarrollar el Marco del SGSI**

- **Desarrollo de Políticas:** Crea o actualiza las políticas de seguridad de la información para reflejar los requisitos del ENS. Incluye políticas sobre control de acceso, gestión de incidentes y clasificación de datos.
- **Proceso de Gestión de Riesgos:** Implementa un proceso formal de gestión de riesgos, incluyendo identificación, evaluación y tratamiento de riesgos. Asegúrate de que la estrategia de gestión de riesgos se alinee con las directrices del ENS.
- **Gestión de Activos:** Identifica y clasifica los activos (hardware, software, datos) según su importancia para tu organización. Define medidas de protección apropiadas para cada activo.

### 5. **Implementación de Controles de Seguridad Técnicos**

- **Encriptación:** Utiliza encriptación fuerte para datos sensibles en almacenamiento y tránsito.
- **Control de Acceso:** Implementa controles de acceso basados en roles (RBAC) y autenticación de dos factores (2FA) para todos los sistemas críticos.
- **Monitoreo y Detección de Incidentes:** Instala herramientas de monitoreo (SIEM, IDS/IPS) para detectar y responder a incidentes. Alinea esto con los requisitos regulatorios españoles para la notificación de incidentes.
- **Copia de Seguridad y Recuperación:** Establece un sistema fiable de copia de seguridad y recuperación ante desastres. Asegúrate de que las copias de seguridad estén encriptadas y se prueben regularmente.
- **Seguridad Perimetral:** Refuerza las defensas perimetrales utilizando firewalls, sistemas de detección de intrusiones y segmentación de red.

### 6. **Medidas Administrativas y Organizativas**

- **Programas de Concienciación y Formación:** Desarrolla y ejecuta un programa de concienciación en seguridad para todos los empleados, cubriendo temas como phishing, manejo seguro de datos y notificación de incidentes.
- **Plan de Respuesta a Incidentes:** Crea un plan de respuesta a incidentes que cumpla con las directrices del ENS. Asegúrate de que cubra la detección, respuesta, recuperación y notificación de incidentes.
- **Monitoreo Continuo:** Establece un proceso de monitoreo de amenazas de seguridad, asegurando que se realicen auditorías periódicas y evaluaciones de vulnerabilidades.

### 7. **Gestión de Terceros y Proveedores**

- **Evaluación de Riesgos de Proveedores:** Evalúa las medidas de seguridad de los proveedores de servicios externos para asegurar que cumplan con los requisitos del ENS.
- **Obligaciones Contractuales:** Incorpora cláusulas relacionadas con el ENS en los contratos con proveedores y socios, especialmente aquellos que manejan información sensible.

### 8. **Auditoría y Certificación**

- **Auditoría Interna:** Realiza auditorías internas regulares para asegurar el cumplimiento continuo del ENS. Aborda cualquier no conformidad identificada durante las auditorías.
- **Certificación ENS:** Involucra a auditores acreditados para obtener la certificación ENS. Este paso es crucial para las administraciones públicas y los proveedores que trabajan con el sector público.
- **Auditoría Externa:** Dependiendo de tu nivel de seguridad, es posible que necesites someterte a una auditoría externa para la certificación oficial (particularmente para los niveles Medio y Alto).

### 9. **Gestión y Notificación de Incidentes**

- **Proceso de Manejo de Incidentes:** Implementa un proceso formal para la notificación y respuesta a incidentes. Asegúrate de que los incidentes se notifiquen a las autoridades pertinentes, siguiendo las directrices del ENS.
- **Mejora Continua:** Después de los incidentes, realiza un análisis post-mortem para actualizar el SGSI y prevenir incidentes similares en el futuro.

### 10. **Documentación e Informes**

- **Plan de Seguridad:** Documenta el plan de seguridad, que debe incluir objetivos, enfoques de gestión de riesgos y medidas de seguridad en línea con el ENS.
- **Informes de Conformidad:** Produce informes regulares de conformidad que demuestren la adherencia a los requisitos del ENS.
- **Comunicación con las Autoridades:** Asegura una comunicación regular con las autoridades reguladoras para la notificación de incidentes y certificaciones.

### 11. **Mejora Continua**

- **Revisión Regular:** Revisa y actualiza periódicamente tu SGSI para alinearlo con las amenazas en evolución y las actualizaciones del ENS.
- **Pruebas de Penetración:** Realiza pruebas de penetración anuales para evaluar la efectividad de tus controles de seguridad.
- **Re-formación de Empleados:** Actualiza regularmente la concienciación de seguridad de los empleados a través de programas de formación continuos.

## Medidas de Protección del ENS

La siguiente es una lista de todas las medidas de protección que debemos implementar para cumplir con el ENS.

### Protección de instalaciones 🔒🏢

La protección de instalaciones se erige como un pilar fundamental en el Esquema Nacional de Seguridad, desempeñando un papel crítico en la preservación de la integridad y la información de una entidad pública. Este componente, que abarca desde infraestructuras estratégicas hasta edificios clave, se convierte en un eslabón esencial para el desarrollo seguro y sostenible.

La protección de instalaciones se refiere a la aplicación de medidas y estrategias destinadas a salvaguardar física y estratégicamente los lugares y estructuras considerados cruciales para el funcionamiento y bienestar de una sociedad. Estas instalaciones pueden abarcar desde centrales eléctricas y plantas de tratamiento de agua hasta edificios gubernamentales y centros de investigación.

Entre sus controles tenemos:

#### Áreas separadas con control de acceso 🔒🚧

Según el ENS, la infraestructura de todos los sistemas debe seguir una distribución de zonas separadas según su función y tener control de acceso para estas zonas

| Dimensiones |  |  | Medidas de protección |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Marco operacional |
| Aplica | = | = | mp.if.1 | Áreas separadas con control de acceso |

#### Identificación de personas 🧑‍💼🚧

Todas las entidades deben tener control de acceso a las instalaciones y con registro de entrada y salida

| Dimensiones |  |  | Medidas de protección |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Marco operacional |
| Aplica | = | = | mp.if.2 | Identificación de personas |

#### Acondicionamiento de los locales 🌡️💧

Todas las instalaciones deben tener condiciones favorables de temperatura y humedad, y tener protección contra amenazas obtenidas del análisis de riesgos

| Dimensiones |  |  | Medidas de protección |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Marco operacional |
| Aplica | = | = | mp.if.3 | Acondicionamiento de los locales |

#### Energía eléctrica 🔌💡

Según el ENS, las instalaciones deben tener suministro de energía en caso de fallo eléctrico o al menos garantizar el correcto funcionamiento de las luces de emergencia

| Dimensiones |  |  | Medidas de protección |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Marco operacional |
| Aplica | + | = | mp.if.4 | Energía eléctrica |

#### Protección frente a incendios 🔥🚨

Las instalaciones deben tener protección contra incendios, así como equipos para extinguir el fuego

| Dimensiones |  |  | Medidas de protección |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Marco operacional |
| Aplica | = | = | mp.if.5 | Protección frente a incendios |

#### Protección frente a inundaciones 🌊🚨

Al igual que en el punto anterior, debe haber protección en caso de inundaciones, podemos referenciar esta protección según la normativa industrial seguida en la instalación y adecuación del edificio para incendios e inundaciones

En este caso, los controles deben aplicarse en entidades de categoría media y alta.

| Dimensiones |  |  | Medidas de protección |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Marco operacional |
| No aplica | Aplica | = | mp.if.6 | Protección frente a inundaciones |

#### Registro de entrada y salida de equipamiento 📦🚧

Todo equipo que salga y entre debe ser identificado y documentado, así como quién lo autorizó, la fecha de salida y el tiempo estimado.

| Dimensiones |  |  | Medidas de protección |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Marco operacional |
| Aplica | = | = | mp.if.7 | Registro de entrada y salida de equipamiento |

#### Instalaciones alternativas 🚧🚨

Las entidades públicas con sistemas de categoría alta deben tener instalaciones alternativas en caso de que un incidente deje fuera de funcionamiento la instalación principal, estas instalaciones alternativas deben tener las mismas garantías de seguridad que las habituales

| Dimensiones |  |  | Medidas de protección |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Marco operacional |
| No aplica | No aplica | Aplica | mp.if.1 | Instalaciones alternativas |

### Protección de activos y personal

La protección de activos y personal implica la implementación de estrategias y medidas destinadas a salvaguardar tanto los recursos críticos de las entidades públicas del país, como la información estratégica y la seguridad de sus ciudadanos.

Dentro del ENS, la gestión y protección del personal está mayormente relacionada con la función y obligaciones dentro de su puesto de trabajo así como la formación y concienciación respecto a la seguridad, sus controles son:

#### Caracterización del puesto de trabajo 🧑‍💼📄

En este control se debe estipular documentación con las responsabilidades de seguridad de cada empleado según su puesto de trabajo, así como los requisitos que se deben cumplir para ocupar el puesto de trabajo y en la selección de personal.

| Dimensiones |  |  | Medidas de protección |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Marco operacional |
| No aplica | Aplica | = | mp.if.1 | Caracterización del puesto de trabajo |

#### Deberes y obligaciones 🧑‍💼🔒

Se deben explicar los deberes y responsabilidades respecto a la seguridad en el puesto de trabajo. También se deben tomar medidas disciplinarias en caso de incumplimiento de deberes en el puesto de trabajo

| Dimensiones |  |  | Medidas de protección |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Marco operacional |
| Aplica | = | = | mp.per2 | Deberes y obligaciones |

#### Concienciación 🧑‍🏫🔒

El ENS explica que se deben dar charlas periódicamente al personal para recordar la normativa de seguridad y los procedimientos de gestión de incidentes

| Dimensiones |  |  | Medidas de protección |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Marco operacional |
| Aplica | = | = | mp.per3 | Concienciación |

#### Formación 🧑‍🏫🔒

Este control implica gestionar correctamente la información de la institución y formar al personal para que sepa cómo reaccionar ante diferentes tipos de incidentes

| Dimensiones |  |  | Medidas de protección |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Marco operacional |
| Aplica | = | = | mp.per4 | Formación |

#### Personal alternativo 🧑‍💼🚨

Debe haber personal que se haga cargo de las funciones en caso de cualquier indisponibilidad del personal habitual.

| Dimensiones |  |  | Medidas de protección |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Marco operacional |
| No aplica | No aplica | Aplica | mp.per5 | Personal alternativo |

En cuanto a la protección de activos, la norma está más orientada hacia los puestos de trabajo y su manipulación y protección

#### Puesto de trabajo despejado 🧑‍💼🚧

Este control establece la política de que el puesto de trabajo debe estar limpio y solo se debe realizar la actividad que se está llevando a cabo en el momento, el material que no se esté utilizando debe guardarse en un lugar cerrado

| Dimensiones |  |  | Medidas de protección |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Marco operacional |
| No aplica | No aplica | Aplica | mp.eq1 | Puesto de trabajo despejado |

#### Bloqueo de puesto de trabajo 🔒🧑‍💻

En sistemas de categoría media, los puestos de trabajo deben tener un bloqueo tras un periodo de inactividad y requerir autenticación para ser reactivados, principalmente con el fin de cerrar sesiones abiertas.

| Dimensiones |  |  | Medidas de protección |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Marco operacional |
| No aplica | No aplica | Aplica | mp.eq2 | Bloqueo de puesto de trabajo |

#### Protección de equipos portátiles 📱🚧

Este es el control más riguroso dentro de los controles de protección de activos y es que debe haber un inventario de todos los equipos portátiles que salen de la instalación junto con el responsable del mismo, y debe haber documentación de todos los procedimientos de información sobre cualquier incidente que pueda existir con dicho equipo

Estos equipos también deben tener limitación de información accesible y almacenamiento de información sensible, es aconsejable manejar información con un alto nivel de cifrado

| Dimensiones |  |  | Medidas de protección |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Marco operacional |
| No aplica | No aplica | Aplica | mp.eq3 | Protección de equipos portátiles |

#### Medios alternativos 🚧🚨

Debe haber disponibilidad de equipos alternativos en caso de que fallen los equipos habituales.

| Dimensiones |  |  | Medidas de protección |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Marco operacional |
| No aplica | No aplica | Aplica | mp.per4 | Medios alternativos |

### Protección de la información y los servicios

Es importante tener protección de la información que se puede manejar dentro de una entidad pública, así como sus servicios, es por ello que el ENS mantiene controles respecto a estas áreas que veremos a continuación

#### Datos de carácter personal 🧑‍💼📄

Este control se basa en los sistemas con datos de carácter personal, los cuales deben cumplir los requisitos de la Ley Orgánica de Protección de Datos y Garantía de los Derechos Digitales

| Dimensiones |  |  | Protección de la información |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Marco operacional |
| Aplica | = | = | mp.info1 | Datos de carácter personal |

#### Calificación de la información 🧑‍💼📄

Esta política da al responsable de la información la responsabilidad de determinar su clasificación y describir los criterios para etiquetar la información según su nivel de seguridad

| Dimensiones |  |  | Protección de la información |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Marco operacional |
| Aplica | + | = | mp.info2 | Calificación de la información |

#### Cifrado 🔒🔑

Debe haber cifrado de alto nivel para la información almacenada y transmitida

| Dimensiones |  |  | Protección de la información |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Marco operacional |
| No aplica | No aplica | Aplica | mp.info3 | Cifrado |

#### Firma electrónica 🔑🖋️

La firma electrónica debe existir dentro de sistemas y documentos para verificar su integridad y autenticidad

| Dimensiones |  |  | Protección de la información |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Marco operacional |
| Aplica | + | ++ | mp.info4 | Firma electrónica |

#### Sellos de tiempo 🕒🔑

Los sellos de tiempo ayudan a analizar la integridad de la información cuando se requiere temporalmente, generalmente orientado a datos utilizados como evidencia electrónica

| Dimensiones |  |  | Protección de la información |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Marco operacional |
| Aplica | = | = | mp.info5 | Sellos de tiempo |

#### Limpieza de documentos 🧑‍💼📄

Se debe eliminar la información en campos ocultos, metadatos y revisiones especiales especialmente cuando el documento se hace público

| Dimensiones |  |  | Protección de la información |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Marco operacional |
| Aplica | = | = | mp.info6 | Limpieza de documentos |

#### Copias de seguridad 💾📄

Debe haber copias de seguridad que tengan el mismo nivel de seguridad que los datos originales y deben cubrir tanto la información de trabajo como las aplicaciones y claves

| Dimensiones |  |  | Protección de la información |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Marco operacional |
| Aplica | = | = | mp.info9 | Copias de seguridad |

Dentro de la protección de servicios se establecen los siguientes controles

#### Protección del correo electrónico 📧🔒

Debe haber medidas de seguridad que se utilizarán para prevenir incidentes como SPAM o malware, además de documentación que explique el uso seguro del correo electrónico

Es aconsejable utilizar un proveedor de correo electrónico de confianza

| Dimensiones |  |  | Protección de servicios |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Marco operacional |
| Aplica | = | = | mp.s.1 | Protección del correo electrónico |

#### Protección de servicios y aplicaciones web 📧🧑‍💻

Debe haber medidas de seguridad para prevenir incidentes como manipulación de URL y cookies, escalada de privilegios, entre otros. Para sistemas de categoría alta, se recomienda el uso de certificados de autenticación cualificados

| Dimensiones |  |  | Protección de servicios |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Marco operacional |
| Aplica | = | + | mp.s.2 | Protección de servicios y aplicaciones web |

#### Protección frente a la denegación de servicio 🚨🧑‍💻

Debe haber protección contra este tipo de ataques, como control de solicitudes y balanceadores de carga, así como sistemas para detectar el ataque y procedimientos para reaccionar al ataque

| Dimensiones |  |  | Protección de servicios |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Marco operacional |
| No aplica | Aplica | + | mp.s.8 | Protección frente a la denegación de servicio |

#### Medios alternativos 🚨🧑‍💻

Debe haber disponibilidad de medios alternativos para prestar el servicio de aplicaciones con las mismas garantías que los medios habituales, esto puede incluirse en el plan de continuidad del negocio

| Dimensiones |  |  | Protección de servicios |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Marco operacional |
| No aplica | No aplica | Aplica | mp.s.9 | Medios alternativos |
