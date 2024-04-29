# **Lectura 3 Marco operacional**

## Planificación de Seguridad

Cuando hablamos de los marcos operacionales, nos referimos a una serie de medidas que se deben tomar para proteger la operación del sistema como conjunto integral de componentes para un fin; Este marco desempeña un papel esencial al proporcionar la estructura necesaria para implementar y gestionar eficazmente las medidas de seguridad ya que son guías detalladas que permiten a las organizaciones públicas adaptarse a los requisitos específicos del ENS, asegurando la protección integral de la información y los sistemas.

La planificación de seguridad dentro del marco operacional es uno de los componentes más importante dentro del ENS y trata de un proceso estratégico que guía a las organizaciones en la identificación y gestión de riesgos, también en la implementación de medidas de seguridad y la preparación para responder a incidentes, ayudando así a fortalecer los sistemas de información del sector público.

La planificación de la seguridad consta de varias etapas las cuales tenemos:

### Análisis de Riesgos:

Implica una evaluación exhaustiva de los riesgos a los que se enfrenta la información y los sistemas. Este análisis, identifica las amenazas potenciales, evalúa su impacto y determina la probabilidad de ocurrencia. La comprensión de estos riesgos sienta las bases para la toma de decisiones informada en la implementación de medidas de seguridad.

Dentro del los controles de ENS se plantea lo siguiente para tratar las dimensiones del análisis de riesgos

**Sistemas de Categoría básica basta con un análisis que muestre:**

1. Identifique los activos más valiosos del sistema
2. Identifique las amenazas más probables.
3. Identifique las salvaguardas que protegen de dichas amenazas.
4. Identifique los principales riesgos residuales.

**Sistemas de categoría media deben realizar un análisis semi formal junto a una presentación en tablas que describa:**

1. Identifique y valore cualitativamente los activos más valiosos del sistema.
2. Identifique y cuantifique las amenazas más probables.
3. Identifique y valore las salvaguardas que protegen de dichas amenazas.
4. Identifique y valore el riesgo residual.

**Sistemas de categoría alta deberán realizar un análisis formal conjunto a un cálculo matemático que cubra:**

1. Identifique y valore cualitativamente los activos más valiosos del sistema.
2. Identifique y cuantifique las amenazas posibles.
3. Identifique las vulnerabilidades habilitantes de dichas amenazas.
4. Identifique y valore las salvaguardas adecuadas.
5. identifique y valore el riesgo residual.

Así tal cual lo establecido en la clasificación anterior, el análisis de riesgo se aplica en un sistema de dimensiones bajo, y con incremento en su nivel medio e incremento mayor en un nivel alto.

| Dimensiones |  |  | Medidas de seguridad |  |
| --- | --- | --- | --- | --- |
| B | M | A | Org | Marco Operacional |
| Aplica | + | ++ | op.pl.1 | Análisis de riesgo |

### Arquitectura de seguridad:

Es la estructura fundamental que respalda la salvaguarda de la información sensible en el ámbito de las administraciones públicas. Está diseñada para establecer un entorno seguro, garantizando la confidencialidad, integridad y disponibilidad de los sistemas y datos en un contexto digital en constante evolución. Los aspectos que hay que detallar en estos controles están:

**Sistemas de categoría básica**

1. Documentación de las instalaciones: Áreas y punto de accesos
2. Documentación del sistema: Equipos, redes internas y conexiones al exterior
3. Esquema de líneas de defensa: punto de interconexión a otros sistemas, cortafuegos y DMZ
4. Sistema de identificación y autenticación de usuarios: claves concertadas, contraseñas, tarjetas de identificación y ficheros o directorios para autenticar al usuario y determinar sus derechos de acceso.

**Sistemas de categoría media**

1. Sistema de gestión, relativo a la planificación, organización y control de los recursos relativos a la seguridad de la información

**Sistemas de categoría Alta**

1. Sistema de gestión de seguridad de la información con actualización y aprobación periódica
2. Controles técnicos internos: Validación de datos de entrada, salida y datos intermedios.

Así tal cual lo establecido en la clasificación anterior, el análisis de riesgo se aplica en un sistema de dimensiones bajo, y con incremento en su nivel medio e incremento mayor en un nivel alto.

| Dimensiones |  |  | Medidas de seguridad |  |
| --- | --- | --- | --- | --- |
| B | M | A | Org | Marco Operacional |
| Aplica | + | ++ | op.pl.2 | Arquitectura de seguridad |

### Adquisición de nuevos componentes:

Este proceso se hace con la finalidad de fortalecer la infraestructura de seguridad dentro de la administración pública, estos componentes deben estar conformes con los estándares del ENS, y se debe asegurar que estos componentes se puedan tanto integrar al sistema existente, como capacitar al personal que manejara estos equipos. Este proceso debe atender las conclusiones del análisis de riesgos así como ser acorde a la arquitectura de seguridad escogida

De acuerdo a sus controles, este proceso de debe aplicar tanto en los sistemas de categoría básica, media y alta de igual forma

| Dimensiones |  |  | Medidas de seguridad |  |
| --- | --- | --- | --- | --- |
| B | M | A | Org | Marco Operacional |
| Aplica | = | = | op.pl.3 | Adquisición de nuevos componentes |

### Gestión de capacidades:

Se enfoca en identificar, adquirir y desarrollar las capacidades necesarias para asegurar la integridad, confidencialidad y disponibilidad de la información, enfrentando así los desafíos cambiantes del entorno cibernético.

**En este control comenzamos a aplicarlo a partir de los sistemas de categoria media donde haremos un estudio de los siguientes aspectos:**

1. Necesidades de procesamiento.
2. Necesidades de almacenamiento de información: durante su procesamiento y durante el periodo que deba retenerse.
3. Necesidades de comunicación.
4. Necesidades de personal: cantidad y cualificación profesional.
5. Necesidades de instalaciones y medios auxiliares.

| Dimensiones |  |  | Medidas de seguridad |  |
| --- | --- | --- | --- | --- |
| B | M | A | Org | Marco Operacional |
| No Aplica | Aplica | = | op.pl.4 | Gestión de capacidades |

### Componentes certificados:

Estos son los estándares y requisitos que deben tener los componentes para que puedan asegurar que la infraestructura de seguridad sea sólida y confiable. Estos requisitos son definidos por el Centro Criptológico Nacional (CCN) y se basan en estándares nacionales e internacionales. La certificación garantiza que los componentes han sido sometidos a pruebas rigurosas y cumplen con los estándares de seguridad requeridos.

Este control sólo se aplicará en sistemas de categorías altas donde es necesario utilizar sistemas o equipos que hayan sido certificados bajo normas europeas o internacionales y estén reconocidos por el ENS como la ISO/IEC 15408.

| Dimensiones |  |  | Medidas de seguridad |  |
| --- | --- | --- | --- | --- |
| B | M | A | Org | Marco Operacional |
| No Aplica | No Aplica | = | op.pl.4 | Componentes certificados |

### Control de acceso:

Esta es una estrategia planteada el cual garantiza que solo los usuarios autorizados tengan acceso a información clasificada y protegida, uno de los principales objetivos es mantener la confidencialidad, integridad y disponibilidad de los datos

### Identificación

La finalidad de este control es lograr una identificación única de cada usuario para así quien ha realizado actividades dentro del sistema y que actividades y mantener una trazabilidad, confidencialidad y autenticidad, además podremos contar con requisitos de accesos los cuales pueden impedir la utilización del sistema.

Dentro del ENS se plantea en todas las categorías de sistemas y plantea que se pueden utilizar como identificador único los sistemas previstos dentro de la normativa, y cuando el usuario del sistema tenga diferentes roles frente al sistema (un ciudadano, un trabajador y el administrador de sistema no pueden tener el mismo rol, recibirá identificadores singulares para tener limitado privilegios y registros de actividad y así saber:

- Cuantas veces se intentó acceder
- Cuál fue el último acceso al sistema

| Dimensiones |  |  | Medidas de seguridad |  |
| --- | --- | --- | --- | --- |
| B | M | A | Org | Marco Operacional |
| Aplica | = | = | op.acc.1 | Identificación |

### Requisitos de acceso:

En este proceso se recomienda en todas las categorías el uso de mecanismos de protección el cual pueda impedir la utilización de algún activo en caso de sospecha de un incidente, y poder tener sistemas que otorguen derecho de acceso según las decisiones de la persona responsable de este recurso, todo esto nos ayudará a tener un buen control de acceso al sistema.

| Dimensiones |  |  | Medidas de seguridad |  |
| --- | --- | --- | --- | --- |
| B | M | A | Org | Marco Operacional |
| Aplica | = | = | op.acc.2 | Requisitos de acceso |

### Segregación de funciones y tareas:

En este proceso se recomienda una segmentación de tareas y funciones en toda la entidad, es decir, separar las funciones de distintos departamentos por ejemplo, se deben tener diferentes tareas y funciones de seguridad en un departamento de operacion, departamento de mantenimiento y de auditoría, todas este proceso se recomienda que documentado y explicado

Este control se aplica en sistemas de categoría medio y alto y exige que existan dos o más personas para realizar tareas críticas para así evitar que un solo individuo autorizado pueda abusar de sus derechos para cometer acciones ilegales.

Por lo menos se debe separar las siguientes funciones

1. Desarrollo de operaciones
2. Configuración y mantenimiento del sistema de operación
3. Auditoría y supervisión de funciones.

| Dimensiones |  |  | Medidas de seguridad |  |
| --- | --- | --- | --- | --- |
| B | M | A | Org | Marco Operacional |
| No Aplica | Aplica | = | op.acc.3 | Segregación de funciones y tareas |

### Proceso de gestión de derechos de acceso:

En este proceso aplicamos el derecho acceso al mínimo privilegio, es decir cuidamos que los usuarios del sistema tengan el mínimo acceso a la información necesaria y puedan contar con permiso de autorización solo para el personal con competencia en el area, asi evitar que cualquier usuario pueda acceder a información confidencial de la entidad

**Este control se aplica en los todos los sistemas**

| Dimensiones |  |  | Medidas de seguridad |  |
| --- | --- | --- | --- | --- |
| B | M | A | Org | Marco Operacional |
| Aplica | = | = | op.acc.4 | Proceso de gestión de derecho de acceso |

### Mecanismos de autenticación

En este control documentamos y explicamos con qué mecanismos de autenticación protegemos los sistemas, estos mecanismos se dividen en tres grupos que se aplican dependiendo la categoría del sistema.

- Sistema de categoría baja: Se aplicar como factor “Algo que sabe” es decir se puede usar una contraseña o unas credenciales que estará bajo control exclusivo del usuario, estas credenciales se cambiarán de manera periódica y se deshabilitará cuando el usuario termine relación el sistema
- Sistema de categoría media: Se usarán al menos dos factores de autenticación, entre el “algo que se” y “algo que tengo” que tratan de componentes lógicos como tokens de seguridad o certificados de software
- Sistemas de categoría alto: Contará con al menos dos o los tres factores de autenticación y estas credenciales se suspende tras un periodo definido de no utilización y en el caso del “Algo que se tiene” se usarán elementos criptográficos y parámetros acreditados por el CCN

| Dimensiones |  |  | Medidas de seguridad |  |
| --- | --- | --- | --- | --- |
| B | M | A | Org | Marco Operacional |
| Aplica | + | ++ | op.acc.5 | Mecanismo de autenticación |

### Explotación de servicios internos y externos

Estos controles van más orientados al uso y gestión de los activos tecnológicos dentro de la organización así como los servicios externos o de terceros. Los principales controles que podemos tratar

Dentro de los servicios internos tenemos

- Inventario de activos:

Dentro del ENS se contempla que una entidad pública debe tener dentro de todos sistemas un inventario de activos actualizados junto a los responsables de cada activo

| Dimensiones |  |  | Medidas de seguridad |  |
| --- | --- | --- | --- | --- |
| B | M | A | Org | Marco Operacional |
| Aplica | = | = | op.exp. 1 | Inventario de activos |

### Configuración de seguridad:

Se debe asegurarse de varias cosas, como la retirada de cuentas o contraseñas fáciles de conseguir, que los usuarios puedan tener la mínima funcionalidad posible y que el sistema pueda tener configuraciones de seguridad por defecto

| Dimensiones |  |  | Medidas de seguridad |  |
| --- | --- | --- | --- | --- |
| B | M | A | Org | Marco Operacional |
| Aplica | = | = | op.exp.2 | Configuración de seguridad |

### Gestión de la configuración:

Este control se toma para los sistemas de categoría media y se toman acciones y monitoriza todos los controles dentro de la configuración de seguridad aplicando la regla de la funcionalidad mínima y la real de seguridad por defecto en donde todos los activos de la empresa tenga un alto nivel de seguridad por defecto, también se busca que el sistema pueda reaccionar a las vulnerabilidades reportadas a los incidentes

| Dimensiones |  |  | Medidas de seguridad |  |
| --- | --- | --- | --- | --- |
| B | M | A | Org | Marco Operacional |
| No Aplica | Aplica | = | op.acc.3 | Proceso de gestión de derecho de acceso |

### Mantenimiento:

El ENS contempla que en caso de mantenimiento de los equipos se debe seguir las pautas de mantenimiento e instalación del fabricante así como seguir los procedimientos de actualizaciones según el tipo de riesgo que pueda representar dicha información

| Dimensiones |  |  | Medidas de seguridad |  |
| --- | --- | --- | --- | --- |
| B | M | A | Org | Marco Operacional |
| Aplica | = | = | op.acc.4 | Mantenimiento |

### Gestión de cambios:

Para todos los sistemas de categoría Media es necesario tener un control sobre todos los cambios que pueda haber en los activos información así como hacer seguimientos a nuevas versiones que existan para ir actualizando este activo tanto en el software como en la seguridad.

| Dimensiones |  |  | Medidas de seguridad |  |
| --- | --- | --- | --- | --- |
| B | M | A | Org | Marco Operacional |
| No aplica | aplica | = | op.acc.5 | Gestión de cambios |

### Protección frente a código dañino:

Todos los sistemas de la organización debe demostrar que tiene protección frente a código maligno como gusanos, malware o virus

| Dimensiones |  |  | Medidas de seguridad |  |
| --- | --- | --- | --- | --- |
| B | M | A | Org | Marco Operacional |
| Aplica | = | = | op.acc.6 | Proteccion frente a código dañino |

### Gestión de incidentes:

Estos son procedimientos para reportar dentro de los sistemas de categoría media todos los incidentes que pueda ocurrir en el sistema, esto incluye los activos que fueron afectados, análisis de cómo pudo ocurrir el incidente y las medidas que se puedan tomar para evitar futuros incidentes similares (Puede ir de la mano del plan de continuidad de negocio)

| Dimensiones |  |  | Medidas de seguridad |  |
| --- | --- | --- | --- | --- |
| B | M | A | Org | Marco Operacional |
| Aplica | = | = | op.acc.7 | Mantenimiento |
- Registro de la actividad de los usuarios: Se hace revisión de los logs del sistema para saber la actividad de los usuarios dentro del sistema.

> Dentro de los sistemas de nivel bajo se activaran los registros de actividad en los servidores, mientras que en los sistemas de nivel medio se revisaran más exhaustivamente buscando patrones anormales y en sistemas de nivel alto se dispondrá de un sistema automático de recolección de registros y correlación de eventos (SIEM)
> 

| Dimensiones |  |  | Medidas de seguridad |  |
| --- | --- | --- | --- | --- |
| B | M | A | Org | Marco Operacional |
| Aplica | + | ++ | op.acc.8 | Registro de actividad de los usuarios |

### Registro de la gestión de incidentes:

La organización debe demostrar que guarda la información del incidente y todas las consecuencias que tuvo, así como registro de evidencias para algún caso legal.

| Dimensiones |  |  | Medidas de seguridad |  |
| --- | --- | --- | --- | --- |
| B | M | A | Org | Marco Operacional |
| No aplica | Aplica | ++ | op.acc.9 | Registro de actividad de los usuarios |

### Protección de los registros de actividades:

Todos los registros de las actividades se tienen que cuidar y mantener, desde un periodo de retención de información acorde, documentación de quién puede acceder a estos registros hasta una gestión correcta de las copias de seguridad , estos registros no podran ser modificados ni eliminados por personal no autorizado.

| Dimensiones |  |  | Medidas de seguridad |  |
| --- | --- | --- | --- | --- |
| B | M | A | Org | Marco Operacional |
| No aplica | No aplica | Aplica | op.acc.10 | Protección de los registros de actividades |

### Protección de claves criptográficas:

En este control se atiende la protección de las claves de seguridad, como su generación, su almacenamiento y su destrucción en caso que ya no se requiera el uso de dicha clave

Para los sistemas de categoría básica los medios de generación estarán aislados de los medios de explotación mientras que para los sistemas de categoría media, se emplean algoritmos acreditados por el CCN.

| Dimensiones |  |  | Medidas de seguridad |  |
| --- | --- | --- | --- | --- |
| B | M | A | Org | Marco Operacional |
| Aplica | + | = | op.acc.11 | Proteccion de claves criptograficas |

En cuanto a los servicios de externos contamos con

### Contratación y acuerdos a nivel de servicios:

En este control debemos establecer un contrato o acuerdos del servicio y los requisitos a nivel de seguridad donde se plantee las responsabilidades y consecuencias de incumplimiento

| Dimensiones |  |  | Medidas de seguridad |  |
| --- | --- | --- | --- | --- |
| B | M | A | Org | Marco Operacional |
| No Aplica | Aplica | = | op.ext.1 | Contratacion y acuerdos a nivel de servicios |

### Gestión diaria:

Se debe hacer una medición rutinaria sobre todos los acuerdos llegados a nivel de contratación y acuerdos a nivel de servicios , y se debe tener la documentación de todos los mecanismos y procedimientos de coordinación para llevar a cabo la tarea de mantenimiento de los sistemas afectados por el acuerdo

| Dimensiones |  |  | Medidas de seguridad |  |
| --- | --- | --- | --- | --- |
| B | M | A | Org | Marco Operacional |
| No Aplica | Aplica | = | op.ext.2 | Gestión diaria |

## Quiz Marco operacional

1. ¿Cuál control de la planificación de la seguridad establece una infraestructura de seguridad dentro del sistema?
    1. Análisis de riesgos
    2. Adquisición de nuevos componentes
    3. arquitectura de seguridad
    4. Gestión de capacidades
2. ¿Cuál es el control que establece que se deben documentar todos los incidentes que ocurran en la organización?
    1. Mantenimiento
    2. Gestión de incidentes
    3. gestión de cambio
    4. Configuración de seguridad