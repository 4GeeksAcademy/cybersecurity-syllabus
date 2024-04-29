# **Lectura 6: Análisis de riesgos dentro del ENS**

## Tratamientos a activos y amenazas

En nuestro trabajo como analistas de seguridad es importante tener conocimiento de cómo darle un tratamiento adecuado a los activos y a la amenazas, esto es esencial para poder proteger la confidencialidad, integridad y disponibilidad de toda la información crítica de la organización, es por eso que el Esquema Nacional de seguridad establece directrices y normativas que nos pueden orientar a la gestión de los activos de informacion de la organizacion, asi como la identificación y mitigación de amenazas.

Principalmente hay que recordar que tenemos que realizar análisis de riesgos dependiendo a la categoría del sistema que tengamos. Cuando tenemos un sistema de categoría Básica el análisis de riesgo será informal, mientras que el para los sistemas de categoría Media será semi-informal y para los sistemas de categoría alta será Formal. La herramienta Pilar nos servirá de gran ayuda para realizar estos análisis de riesgos.

¿Cuáles son los pasos a seguir en un análisis de riesgos? Te los dejamos a continuación:

1. Definir el alcance:

En este paso o fase identificamos todos los activos que van a abarcar en este análisis de riesgos. Estos activos pueden incluir hardware software, bases de datos, documentos, procesos y personas involucradas en el tratamiento de la información. Se debe realizar un inventario exhaustivo de estos activos para comprender su importancia y aplicar medidas de seguridad adecuadas. Este inventario se puede ser de forma informal, semiformal o formal dependiendo la categoría del sistema.

1. Identificar los activos.

En esta fase se deben clasificar todos los activos según su importancia y sensibilidad, principalmente se busca identificar cuáles son los activos esenciales para las organización para poder darle un tratamiento distinto al resto de los activos que los clasificaremos como activos de soporte. El ENS proporciona pautas específicas para esta clasificación, facilitando la toma de decisiones informadas sobre la gestión de riesgos.

1. Identificar las amenazas

En esta fase tendremos que identificar todos los posibles eventos que pueden comprometer a nuestros activos, estas se pueden clasificar de acuerdo a su origen que puede ser

- Natural: En el caso de inundaciones, incendios o desastres naturales
- Industrial: Fallas eléctricas en el servicio.
- Defectos de aplicación: Bugs o cualquier vulnerabilidad en el sistema que pueda permitir explotar una amenaza
- Causadas por personas: Ataques cibernéticos, malwares, acceso no autorizado, situaciones intencionales o no intencionales.

Es muy importante evaluar continuamente el entorno de amenazas para así adaptar las medidas de seguridad de forma proactiva

1. Identificar vulnerabilidades y salvaguardas

En esta fase debemos estudiar las características de todos nuestros activos para asi poder identificar sus vulnerabilidades, por ejemplo, ordenadores o servidores en nuestra red que no tengan un antivirus actualizado.

También un paso importante dentro de esta fase es la de analizar y documentar medidas de seguridad implantadas que puedan contribuir a reducir el riesgos de las amenazas, debemos tener toda esta informacion en cuenta para seguir al próximo paso

1. Evaluar el riesgo

De acuerdo a toda la información que hemos obtenido hasta este punto, ahora tendremos que evaluar el riesgo que pueda haber para cada activo. Se debe estimar la probabilidad de que la amenaza se materialice y el impacto que pueda llevar sobre la organización en el caso de que ocurra.

Este cálculo de riesgos lo tomaremos más adelante en la lectura

1. Tratar el riesgo

Una vez hayamos hecho todo el cálculo de riego, debemos tratar aquellos riesgos que superen un límite establecido por nosotros mismos mediante el cálculo de riesgo, por ejemplo:

- Transferir el riesgo a un tercero. *Por ejemplo*, contratando un seguro que cubra los daños a terceros ocasionados por fugas de información.
- Eliminar el riesgo. *Por ejemplo,* eliminando un proceso o sistema que está sujeto a un riesgo elevado. En el caso práctico que hemos expuesto, podríamos eliminar el wifi de cortesía para dar servicio a los clientes si no es estrictamente necesario.
- Asumir el riesgo, siempre justificadamente. *Por ejemplo,* el coste de instalar un grupo electrógeno puede ser demasiado alto y por tanto, la organización puede optar por asumirlo.
- Implantar medidas para mitigarlo. *Por ejemplo,* contratando un acceso a internet de respaldo para poder acceder a los servicios en la nube en caso de que la línea principal haya caído.

## Cálculo de riesgos

Este paso del análisis de riesgos ayuda a las organizaciones a identificar, evaluar y mitigar los riesgos asociados con la seguridad de la información de manera efectiva.

Las fases del Cálculo de Riesgos son:

- Identificación de Activos:

Antes de calcular riesgos, es esencial identificar y catalogar todos los activos de información. Esto incluye hardware, software, datos y personal. La comprensión completa de los activos proporciona la base para evaluar su importancia y priorizar los esfuerzos de protección.

- Identificación de Amenazas y Vulnerabilidades:

La siguiente etapa implica la identificación de posibles amenazas y las vulnerabilidades asociadas a los activos. Las amenazas pueden ser variadas, desde ciberataques hasta desastres naturales. Las vulnerabilidades son debilidades potenciales que podrían ser explotadas por las amenazas.

- Evaluación de Impacto y Probabilidad:

Una vez identificadas las amenazas y vulnerabilidades, se evalúa el impacto potencial de la materialización de los riesgos y la probabilidad de que ocurran. Este análisis permite clasificar los riesgos en función de su gravedad y probabilidad, facilitando la priorización de las acciones de mitigación.

- Cálculo del Riesgo:

El cálculo del riesgo implica combinar la evaluación de impacto y probabilidad para asignar un valor numérico al riesgo, este valor sería del 1 al 4 y esta cuantificación ayuda a las organizaciones a comprender la magnitud de cada riesgo y a priorizar las intervenciones de seguridad según su impacto potencial.

- Selección de Medidas de Mitigación:

Con base en el cálculo de riesgos, se seleccionan medidas de mitigación adecuadas. Estas pueden incluir controles técnicos, políticas y procedimientos de seguridad, así como la implementación de salvaguardas físicas. La efectividad de estas medidas se evalúa continuamente en un ciclo de mejora continua.

- Herramienta PILAR

La herramienta pilar emerge como un elemento clave en el fortalecimiento de la seguridad de la información. Esta herramienta, diseñada para ofrecer una estructura integral y coherente, proporciona un marco sólido para que las organizaciones gestionen sus sistemas y datos de manera segura, cumpliendo con los estándares y requisitos establecidos por el ENS.

Uno de los beneficios de Pilar es que organiza los principios y requisitos del ENS de manera estructurada, facilitando su implementación paso a paso. Proporciona un marco claro que guía a las organizaciones a través de los aspectos clave de la seguridad de la información, además cuenta con una capacidad para adaptarse a una variedad de contextos y sectores. Se concibe como una herramienta escalable, permitiendo su implementación efectiva tanto en pequeñas empresas como en grandes organizaciones del sector público y privado.

La herramienta Pilar integra principios de gestión de riesgos de manera intrínseca. Facilita la identificación, evaluación y tratamiento de los riesgos asociados a la seguridad de la información, promoviendo una cultura organizacional centrada en la prevención y respuesta proactiva a posibles amenazas.

Otros de los beneficios de Pilar es que asegura que las organizaciones estén en conformidad con las directrices establecidas. Esto no solo fortalece la seguridad interna, sino que también contribuye al cumplimiento de estándares nacionales en materia de seguridad de la información.

## **Laboratorio Herramienta Pilar**

Felicidades, fuiste contratado en una entidad pública para hacer una implementación del ENS, tu jefe te sugiere usar la herramienta Pilar para hacer el análisis de riesgo, y te explica como hacer las instalaciones

Para la instalación podemos dirigirnos a la pagina de pilar tools y seleccionar el la version y sistema operativo que vamos a usar

[https://www.pilar-tools.com/es/tools/pilar/v74/down.html](https://www.pilar-tools.com/es/tools/pilar/v74/down.html*)

![ENS 1](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/ens1.png?raw=true)

Una vez descargado procedemos con su instalación y tendremos este recuadro donde tendremos que insertar la licencia que tengamos de la herramienta

![ENS 2](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/ens2.png?raw=true)

Una vez con la licencia puesta, podemos abrir un nuevo proyecto dentro de la herramienta en donde llenaremos la información como el código del proyecto el nombre del que realizara el análisis de riesgo y la clasificación del proyecto

![ENS 3](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/ens3.png?raw=true)

Asignamos el perfil de seguridad, en este caso usaremos en el ENS

![ENS 4](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/ens4.png?raw=true)

Confirmamos la biblioteca y los niveles del proyecto

![ENS 5](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/ens5.png?raw=true)

![ENS 6](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/ens6.png?raw=true)

Seleccionamos los activos que evaluaremos en el análisis de riesgos en la ventana de proyectos y sección dominios de seguridad. Este dominio es una colección de activos protegidos bajo una única autoridad para diferenciar entre zonas el sistema de información

![ENS 7](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/ens7.png?raw=true)

Ahora podemos generamos los informes, seleccionamos la opcion analisis de riesgos

![ENS 8](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/ens8.png?raw=true)

Ya de esta manera podremos tener nuestro primer informe para el análisis de riesgo con la herramienta pilar