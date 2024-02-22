# Intrusion detection systems (IDS)

**IDS** (*Intrusion Detection System*) el sistema de detección de intrusiones consiste en un conjunto de métodos y técnicas para revelar actividad sospechosa sobre un recurso o recursos informáticos. Es decir, eventos que sugieran un comportamiento anómalo, incorrecto o inapropiado sobre un sistema.

Un sistema de detección de intrusiones puede ser descrito como un proceso de detección y monitorización de eventos que suceden en una red. Este sistema escucha y analiza toda la información que circula por una red, permite ayudar a entender los ataques, estimar los daños causados y tratar de prevenir otros ataques. Para detectar intrusiones en un sistema, los IDS utilizan tres tipos de información: un histórico de eventos, la configuración actual del sistema y, finalmente, procesos activos del sistema o reglas.

![Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image19.png](Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image19.png)

## **¿En qué consiste un IDS y cómo funciona?**

Hemos de partir de la base que aunque tengamos el cortafuegos habilitado, por normal general, tendremos muchos puertos abiertos, como por ejemplo el 80 y el 443 para las aplicaciones web. Por lo que debemos tener un sistema adicional que nos ayude a controlar estas puertas abiertas. Por lo que para llevar un mayor control debemos de utilizar un sistema IDS, esto es, un sistema de detección de intrusos y también de vulnerabilidades. Existen los IDS activos y los pasivos. Con los primeros se genera entradas en el registro y se generan alertas. Con los segundos en cambio, además de realizar las mismas funciones que con el pasivo, también se generarían acciones, como bloquear direcciones IP o cerrar el acceso a puertos restringidos.

Además desde el punto de vista del programación (*software*) existen diferentes tipos de herramienta, los sistemas de detección de intrusos (HIDS), sistemas de detección de intrusos en red (IDPS), los sistemas de detección de intrusos basados en firmas (SIDS) y por último los sistemas de detección de intrusos basados en anomalías.

![Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image20.png](Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image20.png)

Los sistemas IDS utilizan tres métodos para detectar el tráfico. Estos son la detección de anomalías, el análisis de protocolos y el análisis de firmas.

- Con la detección de anomalías tenemos como objetivo detectar un comportamiento anormal. Ejemplo de ello sería un volumen de tráfico ICMP (el que usa ping) inusual y muy elevado, que nos indicaría que somos el blanco o el emisor de un ataque de DDoS (Denegación de servicio)
- Respecto al análisis de protocolos se busca un tráfico de aplicación que no cumple el estándar del protocolo habitual.
- Por último, el análisis de firmas permite identificar ataques o comportamientos perjudiciales ya publicados. Suele ser la técnica más eficaz y la que no está sujeta a errores, ya que sólo se generan ataques o intrusiones que ya han tenido éxito en otro lugar, por lo que, pueden ser fácilmente identificados.

Es importante que nuestro IDS actualice la información de forma habitual, para así tener actualizadas siempre sus técnicas de análisis así como de las bases de datos de firmas.

Existen una serie de organizaciones, asociaciones y empresas que nos permiten estar al corriente de las evoluciones en materia de técnicas de intrusión y ataques. Las principales son:

- Bugtraq: Es una lista de difusión dedicada a la publicación de vulnerabilidades, su uso y corrección. ( [https://www.securityfocus.com/](https://www.securityfocus.com/))
- CERT: *Computer Emergency Response Team*. Se trata de una organización que estudia las vulnerabilidades, investiga las evaluaciones en términos de redes y seguridad y ofrece servicios relacionados con la seguridad. ([Entrada de Wikipedia al respecto](https://es.wikipedia.org/wiki/Equipo_de_Respuesta_ante_Emergencias_Inform%C3%A1ticas))
- CIAC: Computer Incident Advisory Capability. Una organización de alerta e investigación gestionado por el departament de energía de Estados Unidos. ( [https://www.energy.gov/cio/about-our-services/integrated-joint-cybersecurity-coordination-center](https://www.energy.gov/cio/about-our-services/integrated-joint-cybersecurity-coordination-center))

**Tareas de un IDS**

Un IDS realiza dos tareas fundamentales:

- Prevención: se realiza por medio de herramientas que escuchan el tráfico en la red o en un ordenador, denominados sensores, e identifican los ataques aplicando reglas, reconocimiento de patrones o técnicas inteligentes.
- Reacción: trata de detectar patrones de intrusión en las trazas de los servicios de red o en el comportamiento del sistema.

Existen indicadores estadísticos de sensibilidad, especificidad y precisión que permiten comprobar la efectividad del IDS, se basan en los siguientes conceptos:

- Verdaderos positivos (TP): Intrusión existente y correctamente detectada.
- Falsos positivos (FP): Intrusión no existente e incorrectamente detectada.
- Falsos negativos (FN): Intrusión existente y no detectada.
- Verdaderos negativos (TN): Intrusión no existente y no detectada.

**Tipos de IDS**

Existen distintas clasificaciones de los IDS, según sea su enfoque, origen de datos, estructura y comportamiento

![Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image21.png](Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image21.png)

## **En función del enfoque**

Se presentan dos grupos: Los sistemas de detección de usos indebidos, que comparan las firmas con la información recogida; y los de detección de anomalías, que usan técnicas estadísticas para distinguir el comportamiento usual del anormal.

**Detección de anomalías:** Es necesario definir cuál es el comportamiento normal de un sistema por medio de un aprendizaje de actividades, para clasificar los comportamientos que se desvíen de lo normal como sospechosos. Estos sistemas son propensos a dar falsos positivos, que son producidos cuando se dispara una alerta con actividad normal. Tienen la desventaja de que depende de la calidad del proceso de aprendizaje. Existen tres técnicas diferentes para realizar la detección de anomalías en un sistema:

- **Sistemas basados en conocimiento:** Representa el inicio en los IDS, y se basa en las violaciones de seguridad detectadas mediante el uso de reglas. Resultan más fiables y proporcionan mejores rendimientos frente a ataques conocidos, con el inconveniente de su baja capacidad para detectar nuevos ataques no incluidos en la base de datos de firmas.
- **Sistemas basados en métodos estadísticos**: Basado en perfiles de actividad que vienen definidos por el comportamiento del usuario, con respecto a ficheros, programas, registros, etc. Se realiza mediante el establecimiento de métricas y modelos estadísticos.
- **Sistemas basados en aprendizaje automático:** Son los más desarrollados para el modelado de comportamientos normales y buscan mejorar los resultados en cuanto a detección, reducción de falsos positivos y tiempo de computación. Una ventaja reside en recoger las características de un ataque y añadirlo a una base de datos como firmas nuevas, permitiendo actualizar la base de firmas en un breve lapso de tiempo.
- **Detección de usos incorrectos (detección por firma/regla):** Los sistemas de detección basados en uso indebido monitorizan las actividades que ocurren en un sistema y las compara con una base de datos de firmas de ataques. Cuando se encuentra una actividad que coincide con una de estas firmas, se genera una alarma. Presentan una facilidad de adaptación ya que basta con actualizar la base de datos, ya sea, escribiendo la nueva regla u obteniéndola de un tercero.
- **Sistemas Expertos:** Conocimiento codificado mediante reglas de implicación (condición-acción), si se cumplen todas las condiciones se aplica la acción o regla. Presenta la desventaja de que las reglas no son secuenciales, lo que dificulta aislar pasos de intrusiones en el tiempo.
- **Detección de firmas:** Realiza comparaciones entre los eventos que ocurren en el sistema y las firmas almacenadas en la base de datos en busca de similitudes.
- **Análisis de transacción de estados:** Los ataques se representan como una secuencia de transiciones (máquina de estados finitos). Cuando se alcanza un estado considerado como intrusión se lanza una alarma.
- **Híbridos:** Los IDS basados en firmas resultan más fiables y proporcionan mejores rendimientos frente a ataques conocidos, pero presentan una deficiencia ante nuevos ataques. Los IDS basados en anomalías presentan la capacidad de detectar ataques desconocidos, pero su rendimiento es inferior. Los sistemas híbridos serán una mezcla de ambos, y por lo tanto, pueden ajustarse para operar como ambos tipos de detectores, mejorando la funcionalidad, la detección de ataques y la mejora de rendimiento.

## **En función del origen de los datos**

Se encuentran tres tipos de IDS atendiendo a las fuentes de información que se utilicen:

**HIDS (*Host-based Intrusion Detection Systems*):** Los IDS basados en el host solo procesan información de las actividades de los usuarios y servicios en una máquina determinada. Permite monitorizar los datos generados por un usuario, mediante el uso de *syslog1*, e identificar amenazas e intrusiones a nivel de host. Una desventaja proviene del requerimiento de confianza en el sistema, que puede estar infectado anteriormente a la instalación, y lo hace vulnerable ante ataques directos.

**NIDS (*Network Intrusion Detection Systems*):** Los NIDS son instalados en un dispositivo en modo promiscuo, realizan una escucha pasiva sobre la red de forma que no interfieren en su uso, analizando el tráfico en tiempo real, pero por contra, resultan inútiles ante ataques locales. Los nuevos sistemas, basados en agentes inteligentes, permiten una detección de nuevos ataques usando el concepto de centinelas, que supervisan el sistema para recoger toda la información necesaria para la detección.

![Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image22.png](Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image22.png)

**IDS Híbridos:** Los sistemas híbridos recogen lo mejor de ambos tipos HIDS y NIDS. Permiten una detección local de los sistemas y un sensor en cada segmento de red se encarga de la vigilancia. De esta forma se cubren las necesidades HIDS con las del NIDS, permitiendo el aprovechamiento de las ventajas de ambas arquitecturas.

## **En función de su estructura**

Clasificación basada en las estrategias de control:

**Sistema de Detección de Intrusión Distribuido (DIDS):** Se basa en la instalación en un sistema distribuido, ubicando sensores repartidos por varios equipos de la red. Estos sensores se comunican con un nodo central donde se recibirá toda la información y donde se cruzan los datos, lo que nos permitirá detectar los ataques con fiabilidad y obtener una visión global mejorando la detección de incidentes.

![Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image23.png](Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image23.png)

**Sistema de Detección de Intrusión Centralizado:** Emplea sensores que transmiten información a un sistema central que realiza el control, permitiendo ahorrar en equipamientos.

![Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image24.png](Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image24.png)

**En función de su comportamiento**

Encontramos dos tipos de IDS según si realizan la prevención escuchando el tráfico o si se elabora una respuesta defensiva cuando se detecta un ataque.

**IDS Pasivo:** Sólo notifican al administrador de la red pero no actúan sobre el ataque. Únicamente procesan la información en busca de intrusiones, y una vez detectada se genera una alerta.

**IDS Activos:** Es un tipo de IDS denominado Sistema de Prevención de Intrusión (IPS). A diferencia de los IDS, esta tecnología no se limita a escuchar el tráfico de la red y a mandar alertas, sino que permite establecer reglas, como se lo hace en los cortafuegos, para detener las intrusiones.

Intrusion prevention systems (IPS)

Los IPS son dispositivos de hardware o software encargados de revisar el tráfico de red con el propósito de detectar y responder a posibles ataques o intrusiones. La respuesta consiste en descartar o modificar los paquetes procedentes del ataque de tal manera que se anule su propósito. Este comportamiento los clasifica como dispositivos proactivos debido a su reacción automática a situaciones anómalas.

Los IPS se asemejan el comportamiento de los cortafuegos, ambos toman decisiones sobre la aceptación de paquetes en un sistema. Sin embargo, los cortafuegos basan sus decisiones en los encabezados de paquetes entrantes, capas de red y de transporte, mientras que los IPS basan sus decisiones tanto en los encabezados como en el contenido de datos del paquete.

![Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image25.png](Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image25.png)

***Encabezado y contenido de paquetes dependiendo del protocolo.***

La tecnología IPS ofrece una visión más exhaustiva de las operaciones de la red proporcionando información sobre todo tipo de actividades maliciosas, malas conexiones, contenido inapropiado y otras funciones, con una mínima vigilancia. Las principales características de esta tecnología son:

- Capacidad de reacción automática ante incidentes.
- Aplicación de nuevos filtros conforme detecta ataques en progreso.
- Bloqueo automático frente a ataques efectuados en tiempo real.
- Disminución de falsas alarmas de ataques a la red.
- Protección de sistemas no parcheados.
- Optimización en el rendimiento del tráfico de la red.

**Los IPS como evolución de los IDS**

Mientras el IDS se limita a detectar y notificar la intrusión al administrador del sistema, y éste se encarga de recibir y responder las alertas; el IPS detecta la intrusión y la detiene de algún modo ya predefinido, comprobando ciertos comportamientos en la red previamente configurados como anómalos. Gracias a este hecho, el nivel de alertas de un IPS es considerablemente menor que el nivel de alertas producido por un IDS. La diferencia principal entre los IDS activos y los IPS es que estos últimos están en capacidad de inutilizar los paquetes involucrados en el ataque modificando su contenido.

Una desventaja de los IPS viene por parte de la reacción proactiva ante las intrusiones. Por una parte, se tiene una disminución en el tiempo de reacción ante un ataque, pero también puede provocar efectos inesperados e inconvenientes cuando éste reacciona ante un falso positivo (FP), lo que podría llevar a una denegación de servicio o incluso al aislamiento de la máquina. Por ello, el uso de IPS en sistemas de control industrial ha de ser bien estudiado o en su defecto utilizar un cortafuego que posea inspección profunda de paquetes para mayor seguridad en las comunicaciones. Las arquitecturas actuales centralizan el funcionamiento del IPS, lo que facilita su operación y administración, pero disminuye la escalabilidad del sistema y convierte al IPS en un punto crítico.

![Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image26.png](Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image26.png)

***Ventajas de los IPS***

## **Tipos de IPS**

Básicamente, los diferentes tipos de IPS se distinguen por su ubicación.

- **IPS basados en host (HIPS):** Esta aplicación de prevención de intrusiones reside en la dirección IP específica de un solo equipo, permite prevenir posibles ataques en los host.
- **IPS basadas en red (NIPS):** Monitorizan la red en busca de tráfico sospechoso.
- **IPS basado en red Wireless (WIPS):** Monitorizan redes inalámbricas, al igual que hacen los NIPS con redes LAN.
- **IPS basado en Análisis de Comportamiento de Red (NBA):** Examina el tráfico de red para identificar amenazas que generan tráfico inusual, como ataques de DoS o malware.

### **IPS basado en red (NIPS) vs IPS basado en host (HIPS)**

Un HIPS puede manejar el tráfico cifrado y sin cifrar por igual, ya que puede analizar los datos después de que hayan sido descifrados en el host. Por otra parte, un NIPS no utiliza el procesador y la memoria del host, por lo que no impacta en el rendimiento de la máquina.

Un NIPS puede detectar eventos dispersos a través de la red y puede reaccionar fácilmente, mientras que con un HIPS se tardaría demasiado tiempo en informar a un motor central y posteriormente informar al resto de los equipos.

### **La evolución y las categorías de los IPS**

Es posible distinguir dos generaciones históricas de los IPS:

- Los IPS de primera generación, al detectar un ataque proveniente de una dirección IP determinada, descartaban todos los paquetes de esa dirección, estuvieran o no involucrados en el ataque.
- La evolución de los IPS se debe a la capacidad de descartar únicamente los paquetes relacionados con el ataque identificado, permitiendo el tráfico de otros paquetes provenientes de la IP del atacante, siempre y cuando no estuvieran relacionados con el ataque.

Se pueden distinguir cinco categorías de IPS dependiendo de su funcionamiento, sus capacidades y su ubicación en la arquitectura de la red.

- **IPS *inline***

Estos IPS suponen la evolución de los NIDS basados en firmas y hacen la función de un Bridge a nivel de capa dos, revisando todos los paquetes que circulan por la red en busca de firmas. En caso de detectar alguna anomalía automáticamente es almacenado en un log, o incluso puede permitir el paso de un paquete alterando su contenido para de esta manera frustrar un ataque, sin que el atacante se dé cuenta. Este proceso es realizado mediante *Scrubbing*5, que consiste en la detección de errores por medio de verificación *checksum* o por redundancia con copias de datos. Habitualmente son conocidos como IPS de red o NIPS.

- **Switches a nivel de la capa de Aplicación (nivel 7 del modelo OSI)**

Los switches trabajan de forma habitual en el nivel 2 (enlace) pero cada vez son más habituales también los switches a nivel 7 o aplicación debido a la alta demanda de ancho de banda. La tarea principal de estos switches es balancear la carga de las aplicaciones distribuidas entre varios servidores, tomando decisiones de enrutamiento o conmutación a partir del contenido de los datos de la capa de aplicación. Hasta este punto no hay diferencia con un balanceador de carga.

El funcionamiento como IPS es similar a un NIPS basado en firmas, sirviendo para bloquear ataques. La posición de estos equipos suele ser delante de los cortafuegos, de manera que protejan la red completa. Al ser similares a un NIPS, sólo pueden parar ataques que conocen, pero permiten bloquear ataques de tipo DoS o DDoS que el resto de IPS no pueden parar y sin afectar al resto de la red. Se pueden configurar de forma redundante, en modo levantamiento en caliente o como balanceador de carga (característica que los diferencia de cualquier otro IPS).

- **Cortafuegos/IDS de Aplicación**

Los cortafuegos/IDS de aplicación se instalan en cada host que se desea proteger, teniendo en cuenta las aplicaciones que corren en él, por lo que también son conocidos como HIPS. Para su correcto funcionamiento será necesario hacer una fase de entrenamiento, que consiste en el proceso de identificación de patrones normales de funcionamiento en el host. Por medio de este entrenamiento se crea un perfil de relaciones frecuentes entre las aplicaciones y los componentes del sistema, como: el sistema operativo, otras aplicaciones, la memoria y los usuarios.

Los HIPS se comportan de forma similar a los IDS basados en detección de anomalías a la hora de detectar las intrusiones, pero deben identificar todos los procesos exhaustivamente, puesto que de no ser así pueden bloquear una aplicación válida.

Debido a que se apoyan en la detección de comportamientos anómalos y no en la coincidencia de firmas, es posible prevenir intrusiones muy recientes para las cuales todavía no existe una definición de sus firmas específicas.

- **Switches Híbridos**

Los switches híbridos son una combinación entre los HIPS y los switches de nivel de aplicación. Son dispositivos hardware como los switches de nivel de aplicación pero usan políticas similares a las utilizadas por los HIPS.

Los switches híbridos se basan en el análisis de patrones de comportamiento. La fortaleza radica en el conocimiento detallado del tráfico que debe aceptar.

- **Aplicaciones engañosas**

Este tipo de tecnología analiza todo el tráfico de red y de cada dispositivo en particular para disponer de un conocimiento de cuál es el tráfico permitido y correcto, similar a como realiza los patrones un HIPS. En el modo de funcionamiento, cuando detecta un tráfico que no está permitido para la red (acceso a un puerto no permitido) o para un servidor concreto (acceso a un puerto SSH a un servidor que no lo tiene abierto), envía una respuesta marcada al atacante, de manera que el IPS puede detectar otro tráfico de esa misma fuente y bloquearlo.

## **Herramientas IDS/IPS**

Ya hablamos ampliamente de Snort y Suricata veamos algunas otras opciones.

- **Quickdraw**

Quickdraw es un conjunto de reglas para Snort realizado por la empresa Digital Bond, y sirve para aprovechar los IDS existentes mediante el desarrollo de firmas para el control del tráfico de determinados protocolos utilizados en los sistemas de control. Además, también incluye reglas para detectar dispositivos y vulnerabilidades.

Las firmas Quickdraw (reglas en el argot de Snort), identifican solicitudes no autorizadas, solicitudes y respuestas erróneas del protocolo, comandos peligrosos, y otras situaciones que son probables o posibles ataques. En este momento tienen firmas disponibles para cuatro protocolos de sistemas de control, un conjunto de firmas para identificar los ataques a las vulnerabilidades del sistema de control, y un grupo de firmas que identifican eventos de seguridad.

- **Bro**

Bro es otra herramienta que sirve de IDS/IPS, debido a sus características de análisis de red, al igual que Snort y Suricata. Se basa en un potente motor de análisis que permite un alto rendimiento en la monitorización de la red, analiza protocolos, y la información de la capa de aplicación en tiempo real

![Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image27.png](Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image27.png)

***Arquitectura de Bro***

Al igual que otras herramientas, Bro también hace uso de la librería libpcap para su funcionamiento, además es capaz de funcionar en varias redes. Además de la portabilidad adquirida mediante el uso de libpcap, Bro también puede ser una herramienta de red pasiva, lo que significa que puede actuar supervisando una red sin que sea un nodo con una dirección IP asignada. Bro está conceptualizado en dos capas:

> n Motor de eventos: Analiza y guarda el tráfico de la red para generar eventos neutros, que se basan en inicios o paradas de transmisiones, detección de puertos y protocolos.
> 
> 
> n **Política de programa**: Analiza los acontecimientos para crear políticas de acción.
> 

Bro registra los eventos, pero también puede ser configurado para tomar acciones como el envío de alertas, ejecuciones de comandos, actualizaciones y llamadas a otros programas.

- **OSSEC**

OSSEC es un IDS basado en Hosts (HIDS). Realiza análisis de logs, comprobación de la integridad, la supervisión del registro de eventos de Windows, detección de rootkits, alerta basada en tiempo y respuesta activa. Proporciona detección de intrusiones para la mayoría de sistemas operativos, incluyendo Linux, OpenBSD, FreeBSD, OS X, Solaris y Windows. OSSEC tiene una arquitectura centralizada, multiplataforma que permite a varios sistemas ser controlados y manejados fácilmente.

OSSEC se basa en nombrar a cada hosts como server o sensor, según sean sus características. Será necesario un sensor en cada zona que se quiera inspeccionar la red en busca de amenazas, y un servidor al menos para poder leer los datos que llegan de los sensores.

- **Arquitectura OSSEC**

OSSEC se compone de múltiples piezas:

n Servidor: El servidor es la pieza central del despliegue OSSEC. Almacena la integridad de los archivos de bases de datos, comprobación de los registros, eventos y entradas de auditoría del sistema. Todas las reglas, decodificadores, y las principales opciones de configuración se almacenan de forma centralizada en el administrador; por lo que es fácil de administrar incluso con un gran número de agentes.

n **Agentes/sensores:** El agente es un pequeño programa o conjunto de programas, instalado en el sistema que va a ser monitorizado. El agente recopilará información y la transmitirá al gestor para su análisis y para llevar a cabo una correlación de información. Parte de la información se recoge en tiempo real, otra será recogida periódicamente. Tiene un pequeño uso de memoria y CPU por defecto, que no afecta el uso del sistema.

![Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image28.png](Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image28.png)

- **OSSEC en redes industriales**

A modo de resumen, e implementando este sistema en una red industrial, se puede incluir una lista blanca con la IP de cada equipo industrial, routers y switches que puedan estar conectados a la red, denegando la inyección de tráfico a cualquier otro equipo que no esté registrado en esta lista.

De esta forma, se consigue una seguridad efectiva, de forma gratuita y sencilla. Igualmente se puede crear en otros sistemas operativos, en un Linux como se ha visto, o en Windows, que se presenta a continuación. Al funcionar adecuadamente con equipos con bajo rendimiento, nos permite realizar la instalación en redes industriales donde se suelen encontrar equipos más antiguos.

La inclusión de integridad del servidor, detección de rootkits y detección activa, es un añadido a la seguridad de una red industrial, siendo un requisito indispensable para aumentar la defensa de una empresa.

## **Comparación entre varios IDS/IPS**

La Tabla 1 refleja una comparación de las características de algunos de los sistemas IDS/IPS que se han tratado en este estudio.

Módulo 3: Seguridad en redes inalámbricas

## **Protección de las redes inalámbricas**

Las redes inalámbricas domésticas te permiten utilizar el ordenador virtualmente desde cualquier lugar de la casa, además de conectarte con otros ordenadores de la red o acceder a Internet. No obstante, si la red inalámbrica no es segura, existen riesgos muy importantes. Por ejemplo, un hacker podría:

- Interceptar los datos que envíes o recibas
- Acceder a tus archivos compartidos

Secuestrar tu conexión a Internet y utilizar todo el ancho de banda o límite de descargas

### **Consejos de seguridad en Internet para proteger la red inalámbrica**

A continuación se incluyen varios pasos sencillos que puedes seguir para proteger tu red y routers inalámbricos:

- **Evita la utilización de la contraseña predeterminada:** Es muy fácil para un hacker descubrir cuál es la contraseña predeterminada del fabricante de tu router inalámbrico y utilizarla para acceder a la red inalámbrica. Por lo tanto, es conveniente que cambies la contraseña de administrador de tu router inalámbrico. A la hora de establecer la contraseña nueva, trata de elegir una serie compleja de números y letras, e intenta evitar la utilización de una contraseña que pueda adivinarse fácilmente.

<aside>
⚠️ **No permitas que el dispositivo inalámbrico indique su presencia - d**esactiva la difusión del identificador de red SSID (Service Set Identifier) para evitar que el dispositivo inalámbrico anuncie su presencia al mundo que te rodea.

</aside>

- **Cambia el nombre SSID del dispositivo:** Al igual que antes, es muy fácil para un hacker descubrir cuál es el nombre SSID predeterminado del fabricante del dispositivo y utilizarlo para localizar la red inalámbrica. Cambia el nombre SSID predeterminado del dispositivo e intenta evitar la utilización de un nombre que pueda adivinarse fácilmente.
- **Cifra los datos:** En la configuración de la conexión, asegúrate de que activas el cifrado. Si el dispositivo es compatible con el cifrado WPA, utilízalo; en caso contrario, utiliza el cifrado WEP.
- **Protección contra los ataques de malware e Internet:** Asegúrate de que instalas un programa antimalware eficaz en todos los ordenadores y demás dispositivos. Con el fin de mantener actualizada la protección antimalware, selecciona la opción de actualización automática en el producto.

## Estándares de seguridad inalámbrica

### **¿Por qué es importante la seguridad inalámbrica?**

La seguridad inalámbrica es importante porque las vulnerabilidades de la red pueden exponer datos no seguros que posteriormente pueden robarle para usarlos en su contra. Aunque su equipo tenga una fuerte protección, otros dispositivos conectados a su red inalámbrica podrían verse comprometidos si la propia red no es segura.

Su router de Internet no es solo el lugar donde puede aumentar la potencia de la conexión Wi-Fi en casa. También es un centro de seguridad crítico. Y si el router tiene vulnerabilidades, podrían secuestrar la configuración de sus DNS, entre otros problemas, y podría acabar visitando, sin saberlo, sitios web falsos o peligrosos.

Las redes Wi-Fi públicas (como las de los restaurantes y cafeterías) también pueden dejarle expuesto. Sin protocolos de seguridad sólidos, puede dejar por error las contraseñas e incluso la información de los pagos en línea a disposición de alguien de la misma red que esté husmeando en busca de datos personales.

A menos que cuente con la mejor seguridad inalámbrica, cualquier dispositivo en línea puede ser hackeado. Afortunadamente, los estándares de cifrado han mejorado a lo largo de los años para minimizar las vulnerabilidades y neutralizar las amenazas. El mejor protocolo de seguridad de Wi-Fi evitará que ataquen su router y le ayudará a navegar de forma segura en la Wi-Fi pública. Echemos un vistazo a los diferentes tipos de seguridad de Wi-Fi implementados a lo largo de los años.

### **Tipos de protocolos de seguridad de Wi-Fi**

Los tipos de protocolo de seguridad inalámbrica más comunes hoy en día son WEP, WPA y WPA2. Cada protocolo usa un tipo de cifrado diferente para reforzar la seguridad de la red. Los protocolos más recientes, incluido el más reciente WPA3, han demostrado ser muy robustos, y los hackers lo tienen más difícil para aplicar soluciones alternativas.

### Privacidad equivalente por cable (WEP)

La Privacidad equivalente por cable (WEP) era la forma estándar de cifrado, pero ya no es segura, porque la potencia de cálculo ha mejorado y ahora los hackers pueden crackearla fácilmente. La seguridad WEP se cifra con una clave estática, una de las principales razones por las que ya no se considera segura.

WEP, que se introdujo en 1997, usa una única clave para garantizar la seguridad de toda una red. Si un usuario está comprometido, todos los de la red lo están. Cuando se introdujo la seguridad WEP, la cadena de 64 o 128 bits era difícil de crackear, creando un formidable muro entre una red de usuarios y los hackers que intentaban interceptar las señales inalámbricas.

Ahora, ejecutar los cálculos necesarios para descifrar una clave WEP es una cuestión trivial para incluso un equipo doméstico. El protocolo de seguridad WEP se retiró en 2004, por lo que los sistemas que aún lo usen deben actualizarse.

**A favor:**

- La mayoría de los dispositivos reconocen WEP, lo que significa que fue sencillo de configurar y usar.
- Su objetivo era igualar las ventajas de seguridad de las conexiones a Internet por cable.
- Cuando se introdujo, el algoritmo de cifrado era lo suficientemente complejo como para mantener alejados a los usuarios desconocidos.
- WEP protegía contra los ataques «man in the middle».

**En contra:**

- Usaba una clave de cifrado estática que debía cambiarse manualmente y actualizarse en cada máquina individual para garantizar las ventajas de seguridad de los protocolos posteriores.
- Parte de la clave se transmitía como texto plano fácilmente descifrable.
- Se han descubierto incontables agujeros de seguridad a lo largo de los años.

### Acceso Wi-Fi protegido (WPA)

La seguridad WPA (acceso Wi-Fi protegido) se diseñó para solucionar muchos de los problemas que surgieron con WEP. WPA se convirtió en el estándar en 2003 y cifra la clave de acceso a la red de forma dinámica, cambiándola regularmente con TKIP (Temporal Key Integrity Protocol). Así, los hackers ya no pueden crackear la clave recopilando los datos transmitidos durante un largo periodo de tiempo.

TKIP creó un entorno de seguridad dinámico, pero todavía no era suficiente. Los expertos en seguridad descubrieron rápidamente que TKIP se podía crackear incluso con pequeñas cantidades de datos.

Como resultado, se solicitó a criptógrafos de todo el mundo un cifrado (o algoritmo de cifrado) que sustituyera al cifrado RC4 de WEP y WPA, y el cifrado AES, de fabricación belga, resultó ser el más seguro durante el proceso de selección competitivo. AES encontró una amplia adopción con el sucesor de WPA, WPA2, del que hablaremos en la siguiente sección.

**A favor:**

- Introdujo el TKIP, o cifrado de clave dinámica, que cambia regularmente la clave de acceso a la red.
- Todos los dispositivos de la red reconocen la nueva clave cuando se genera.
- Aumentó la complejidad de las claves de seguridad y su autenticación.

**En contra:**

- TKIP ha demostrado ser vulnerable y puede hackearse con facilidad.
- La complejidad del algoritmo puede superarse con la potencia de procesamiento moderna.
- A menos que los usuarios y los administradores de la red crearan contraseñas seguras, los datos eran vulnerables.
- Si se compara WPA frente a WEP, las ventajas de seguridad de WPA eran significativas, pero los propios defectos de WPA se volvieron evidentes muy rápido.

### Acceso Wi-Fi protegido II (WPA2)

El protocolo de seguridad WPA2 aumentó la complejidad de su predecesor (WPA) y ha sido el estándar de seguridad de la red durante más de una década. Usa el cifrado AES, un proceso de cifrado que incluso un ordenador avanzado necesitaría miles de millones de años para descifrarlo.

Pero WPA2 también tiene sus fallos de seguridad. Un [ataque KRACK](https://www.wired.com/story/krack-wi-fi-wpa2-vulnerability/) puede obtener acceso durante el establecimiento de comunicación, el momento en que una red autentifica la conexión de un dispositivo, dejando las contraseñas y otros datos de la víctima vulnerables. Para llevar a cabo un ataque de este tipo, el hacker debe estar muy cerca de la red, lo cual no resulta ideal ni siquiera para los mejores hackers.

Las importantes diferencias de seguridad entre WPA y WPA2 han hecho que el protocolo WPA2 dure más que cualquier otro protocolo de seguridad anterior.

**A favor:**

- Conserva las mismas ventajas introducidas con WPA.
- Suele usar el cifrado AES, un cifrado extremadamente robusto.
- Requiere que las contraseñas sean más largas, lo que añade seguridad adicional.

**En contra:**

- Requiere una mayor cantidad de potencia de procesamiento (ahora insignificante con la tecnología actual).
- Puede ser vulnerable a los ataques «man in the middle».
- Después de más de una década desde su introducción, finalmente se descubrió una grieta.

### ¿Y el protocolo WPA3?

WPA3 se introdujo en 2018 y se convirtió en un protocolo de seguridad estándar en 2020, pero puede tardar en producirse una adopción generalizada. La mayoría de los hogares y empresas siguen usando WPA2, y el hardware compatible con WPA3 puede ser costoso. Con WPA3, el cifrado entre el dispositivo del usuario y la red es específico e individualizado, y los usuarios ni siquiera tendrán que introducir una contraseña.

Con WPA2, un dispositivo y sus datos pueden verse comprometidos una vez que un hacker rompa el cifrado de la red. Eso ya no será posible con WPA3, debido a la capa añadida de cifrado individualizado.

WPA3 también soluciona el fallo de seguridad de WPA2 que permite los ataques KRACK. Y el algoritmo de cifrado es mucho más complejo, tanto que los ordenadores modernos necesitarían **miles de millones de años de cálculos** para entrar en una sola red protegida por WPA3.

- **WPA frente a WPA2**

Resumamos las diferencias entre WPA y WPA2.

|  | WPA | WPA2 |
| --- | --- | --- |
| Fecha de introducción | 2003 | 2004 |
| El mejor método
de codificación disponible | TKIP, un sistema imperfecto
que se puede crackear | AES, el cifrado
más seguro ampliamente
disponible |
| Longitud de la contraseña | La longitud mínima es muy corta,
lo cual compromete la seguridad | La longitud mínima es larga,
lo cual refuerza la seguridad |
| Opciones para el hogar
y para el negocio | Solo para el hogar | Opción para empresas |
| Potencia de procesamiento
requerida | Mínima | Más que WPA,
pero insignificante según
los estándares actuales |
| Fecha de descubrimiento
del fallo de seguridad | 2008 | 2018 |

En la actualidad, WPA2 sigue siendo el protocolo estándar para la seguridad de Wi-Fi, especialmente debido a su sólido método de cifrado AES.

- **WEP frente a WPA y WPA2**

WPA2 es la mejor opción de protocolo de seguridad disponible hoy en día, y todos seguiremos usando contraseñas WPA2 en los hogares y cafeterías durante varios años. WPA2 usa una clave de acceso a la red dinámica y múltiples capas de protección para cualquier red que esté protegiendo. Mientras tanto, el antiguo estándar WEP tiene una clave estática que es fácilmente crackeable.

De todos los tipos de seguridad de Wi-Fi, el WPA2 es el que más tarda en crackearse. Y esta vulnerabilidad es todavía solo teórica: aún no se ha visto en el mundo real. Se ha demostrado que los protocolos WEP y WPA se pueden crackear en cuestión de minutos, por lo que ni los hogares ni las empresas deberían usarlos.

- **WEP, WPA o WPA2, ¿qué protocolo de seguridad de Wi-Fi es mejor para mi router?**

La mejor opción de seguridad de Wi-Fi para su router es **WPA2-AES**. Puede que vea WPA2-TKIP como opción, pero no es tan seguro. Sin embargo, WPA2-TKIP es el segundo más seguro, seguido de WPA y WEP.

WPA3 se convertirá pronto en la opción más segura, una vez que se adopte de forma generalizada, y debería cambiar a ese protocolo cuando esté disponible.

Aquí tiene las normas de seguridad clasificadas de mejor a peor. Siga las recomendaciones de seguridad adecuadas y la Wi-Fi de su casa o negocio será lo más segura posible.

- WPA2 + AES
- WPA2 + TKIP
- WPA + AES
- WPA + AES/TKIP (TKIP se usa como método de reserva)
- WPA + TKIP
- WEP
- Red abierta

Incluso **algo de seguridad es mejor que nada**, así que asegúrese de implementar una de estas opciones, aunque la mejor no esté disponible para usted. Utilice una contraseña larga y compleja y cámbiela con regularidad para mantener una conexión WEP o WPA un poco más segura de lo que sería de otro modo.

<aside>
👉 Si quiere comprar un nuevo router o conectarse a Internet con un nuevo proveedor, compruebe si puede conseguir un router con certificación Wi-Fi WPA3. No debe preocuparse de periodos de transición ni problemas de incompatibilidad: estará todo listo para usar la opción más capaz y segura una vez que WPA3 esté disponible para su red.

</aside>

Esperemos que esa inestimable cajita haga lo que debe y la eliminación de los virus del router se convierta en algo del pasado. Y tal vez ninguno de nosotros tenga que preocuparse nunca más de cómo arreglar una Wi-Fi que no funciona.

## **¿Cómo puedo encontrar mi protocolo de seguridad de Wi-Fi actual?**

Aquí le explicamos cómo encontrar el protocolo de seguridad de Wi-Fi que está usando:

1. Haz clic en el menú **Inicio** de Windows y seleccione **Configuración** (el icono del engranaje).
2. Selecciona **Red e Internet**.
3. Elije **Wi-Fi** en el panel de la izquierda.
4. Haz clic en el nombre de la **red** inalámbrica a la que está conectado.
5. Junto a **Tipo de seguridad** verás el protocolo de red inalámbrica que esté usando.

![Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image30.png](Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image30.png)

Si estás usando WPA2 frente a WPA3, pero quiere cambiar a WPA3, primero tienes que asegurarte de que el campo de **Protocolo** en la configuración de su red Wi-Fi diga *Wi-Fi 6*.

## Vulnerabilidades de seguridad inalámbrica

### **Riesgos y amenazas comunes**

Las redes Wi-Fi, aunque proporcionan una gran comodidad, no están exentas de riesgos y amenazas que podrían comprometer nuestra seguridad en línea y **volverse inseguras**. Entre las amenazas más comunes que acechan en el mundo de las redes inalámbricas se encuentra el acceso no autorizado. Esto significa que los intrusos pueden aprovecharse de redes Wi-Fi desprotegidas o con contraseñas débiles para conectarse sin permiso, lo que podría resultar en el robo de ancho de banda, la interceptación de datos y la explotación de vulnerabilidades en los dispositivos conectados. Pero esto no significa que la tecnología **Wi-Fi no es segura.**

Además, el phishing Wi-Fi se ha convertido en una táctica cada vez más sofisticada utilizada por ciberdelincuentes. Mediante la creación de redes falsas que imitan nombres de redes legítimas, los atacantes engañan a los usuarios para que se conecten a ellas y divulguen información confidencial, como contraseñas y datos bancarios.

Los ataques de fuerza bruta también son una preocupación, ya que los atacantes intentan adivinar contraseñas débiles a través de la repetición de combinaciones hasta obtener acceso no autorizado a la red. Estas amenazas pueden tener graves consecuencias, desde la pérdida de datos personales hasta el secuestro de cuentas en línea, por lo que es esencial estar consciente de los peligros que acechan en el mundo de la Wi-Fi y tomar medidas para protegerse contra ellos para que nuestras **redes Wi-Fi sean lo más seguras posibles**.

Otro tipo de ataques comunes son los del tipo “**[deauthentication](https://en.wikipedia.org/wiki/Wi-Fi_deauthentication_attack)**”, este ataque se basa en enviar tramas de “deautenticacion” a los usuarios validos de la red para intentar desconectarlos de un punto de acceso e intentar capturar los mensajes con el AP, con el objetivo de obtener la clave de acceso a la red. Sin embargo, cuando se habla de **Wi-Fi** **insegura** debemos tomar en cuenta que muchos de los estándares nuevos añaden nuevas funciones de seguridad, de la misma forma lo hacen los distintos fabricantes.

El estándar **[802.11W](https://es.wikipedia.org/wiki/IEEE_802.11w-2009)** es una de las formas nuevas de protección para este tipo de ataques, logrando que cada estándar nuevo **la tecnología Wi-Fi sea cada vez menos insegura.**

### **Vulnerabilidades en las redes Wi-Fi**

Las vulnerabilidades en las redes Wi-Fi son pequeñas secciones invisibles en la conectividad inalámbrica, que los ciberdelincuentes pueden explotar. Una de las vulnerabilidades más notorias y peligrosas es el uso de contraseñas débiles o predecibles. Muchos usuarios aún utilizan contraseñas simples como «123456» o «password» para proteger sus redes Wi-Fi, lo que facilita enormemente el acceso no autorizado. En estos casos particulares, es el usuario quien define si su **red Wi-Fi no es segura**.

Otro punto de vulnerabilidad es el uso del protocolo de seguridad WEP (Wired Equivalent Privacy), que se ha vuelto obsoleto y es susceptible a ataques de descifrado relativamente sencillos. Ya no es común ver este tipo de protocolos de seguridad en redes Wi-Fi de producción, ya que sería una **red Wi-Fi insegura**.

Las redes Wi-Fi también pueden ser vulnerables debido a configuraciones incorrectas del Access point. Esto incluye el uso de configuraciones predeterminadas que son conocidas por los atacantes, como nombres de red (SSID) o contraseñas preestablecidas que no se han cambiado. Además, no mantener actualizado el firmware del Access point puede dejar la puerta abierta a vulnerabilidades conocidas que los fabricantes corrigen en las actualizaciones.

<aside>
📖 Estas vulnerabilidades son puntos débiles que los ciberdelincuentes pueden aprovechar para comprometer la seguridad de tu red Wi-Fi. Para protegerse adecuadamente, es esencial reconocer estas vulnerabilidades y tomar medidas para corregirlas, como el uso de contraseñas fuertes y únicas, la actualización del protocolo de seguridad a WPA3 y la configuración adecuada del Access point o router para minimizar riesgos. Con un enfoque proactivo en la seguridad, puedes fortalecer la integridad de tu red Wi-Fi y garantizar una experiencia de navegación más segura. Si no aplicas medidas a tu red inalámbrica la misma podría ser una **red Wi-Fi no segura.**

</aside>

### **Consejos para proteger tu red inalámbrica**

**La seguridad de tu red Wi-Fi** es una prioridad crucial para proteger tus datos y privacidad en el mundo conectado de hoy. Afortunadamente, existen una serie de consejos prácticos que puedes seguir para fortalecer la seguridad de tu red inalámbrica y dejar de lado una **red Wi-Fi insegura**. En primer lugar, la elección de una contraseña segura y única es esencial. Evita contraseñas obvias o predecibles y opta por combinaciones de letras, números y caracteres especiales que sean difíciles de adivinar. Cambiar regularmente tu contraseña también es una buena práctica de seguridad.

Actualizar el firmware de tu Access point de acuerdo al fabricante de hardware, este es otro paso importante. Los fabricantes suelen lanzar actualizaciones para solucionar vulnerabilidades y mejorar la seguridad, por lo que mantener tu Access point o router actualizado es esencial para no tener una **red Wi-Fi insegura.**

Habilitar el cifrado WPA3 (o WPA2 si tu dispositivo no es compatible) es fundamental para proteger la comunicación entre tu dispositivo y el enrutador. **WPA3 ofrece un mayor nivel de seguridad para tu red Wi-Fi** y encriptación que sus predecesores. También puedes aumentar la seguridad configurando filtros de direcciones MAC, que permiten que solo los dispositivos autorizados se conecten a tu red. No olvides cambiar el nombre predeterminado de tu red (SSID) y desactivar la difusión de este. Esto dificulta que los intrusos identifiquen tu red.

Finalmente, considera la posibilidad de establecer una red de invitados separada para visitantes, con acceso limitado a tus recursos principales. Siguiendo estos consejos, puedes fortalecer significativamente la seguridad de tu red Wi-Fi y reducir los riesgos de ataques y accesos no autorizados, asegurando una experiencia de navegación más segura y confiable para ti y tus dispositivos conectados. El uso VLANS es una recomendación común para redes de invitados y el aislamiento de capa 2 (en caso de que tu equipo lo soporte, también es importante).

Los estándares como 802.11w hacen que las redes Wi-Fi aumenten su seguridad, y a medida que la tecnología siga creciendo tendremos **redes Wi-Fi más efectivas y seguras.**

## Medidas de seguridad para redes inalámbricas

Las redes WiFi se han labrado un hueco importante en nuestros hogares y empresas. Llevan con nosotros pocos años, pero en ese tiempo se han vuelto casi imprescindibles en múltiples actividades cotidianas que van más allá de la conectividad con Internet, ya que además nos permiten manejar todo tipo de gadgets y dispositivos a distancia.

A pesar de su creciente importancia, muchos usuarios apenas prestan atención a la configuración de su red inalámbrica. Simplemente enchufan el router de la operadora y ya está, a empezar a navegar. En general no debería haber mayor problema, pero si no tomamos unas ciertas precauciones, puede que algún intruso entre en nuestra red y nos ocasione más de un quebradero de cabeza.

Normalmente no se tratará de espías o *hackers* malvados como los que aparecen en las películas que tratan por todos los medios de aprovecharse de nuestra WiFi para cometer delitos, aunque haberlos haylos. Lo habitual es que sea algún vecino el que intenta colarse en nuestra red para ahorrase la conexión, haciéndonos de paso responsables en primera instancia de las páginas que visite.

<aside>
📖 ¿Cómo evitar estas intrusiones no deseadas en nuestra WiFi? Pues aunque la seguridad total no existe (para eso tendríamos que apagar la red, claro), podemos seguir una serie de consejos y trucos, tanto sencillos como algo más complejos, que pasamos a explicar a continuación.

</aside>

## **Blinda el acceso a tu router**

![Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image31.png](Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image31.png)

En primer lugar, tenemos que asegurarnos de que nadie ajeno a nosotros va a poder acceder al router para controlar nuestra WiFi. De lo contrario, todo lo que hagamos no servirá de nada, ya que podrán entrar y revertirlo o incluso denegarnos el acceso a nuestra propia red.

Por ello, el primer paso consiste en actualizar el firmware del router a la última versión disponible para corregir posibles vulnerabilidades que se hayan detectado, proceso que dependerá de cada marca y modelo concreto, y después comenzaremos por cambiar la contraseña de acceso por defecto que normalmente viene dada por el fabricante o por la operadora.

No dejes que la puerta a tu centro de conexiones del hogar se abra con el clásico 1234/1234 o admin/admin. Busca un nombre de usuario y una clave personalizada que recuerdes bien o que puedas dejar apuntados en algún lugar que conozcas por si los olvidas. También puede ser útil cambiar la dirección IP por defecto del router. Normalmente suele ser 192.168.1.1, primeras cifras que todo usuario ávido de piratear tu WiFi tecleará en su navegador. Simplemente cambiando la última cifra podrás lograr retrasar o echar para atrás a los hackers menos experimentados o a ese vecino gorrón que quiere aprovecharse de tu conexión.

### **Cambia el nombre de la SSID**

![Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image32.png](Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image32.png)

La [SSID (Service Set Identifier)](https://en.wikipedia.org/wiki/Service_set_%28802.11_network%29) o identificador de la red inalámbrica sirve precisamente para eso, para identificarla entre otras muchas. Lo habitual es que por defecto venga dado por la operadora que nos proporciona el router, mostrando a veces más información de la que debería sobre el tipo de router que tenemos y sus posibles vulnerabilidades.

Lo ideal es que usemos un nombre sencillo de recordar o al que le encontremos alguna relación personal pero que no haga referencia a nosotros directamente ni a nuestra vivienda. Podemos ser todo lo creativos que queramos, incluso ocultar del todo la SSID si el router lo permite o crear varias con diferentes permisos de acceso para invitados.

Pero nunca le pongamos nuestro nombre, nick o dirección física (WiFi del 4º B) o de correo electrónico (sí, parece absurdo pero pasa), ya que estaremos dando pistas innecesarias sobre de quién es la red.

### **Elige el mejor sistema de cifrado y cambia la clave por defecto**

![Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image33.png](Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image33.png)

Un aspecto básico de la seguridad en las redes inalámbricas es el cifrado de los datos que se van a transmitir por ellas. Existen principalmente tres sistemas o protocolos diferentes que podemos encontrar en la mayoría de routers modernos: WEP, WPA y WPA2.

WEP ha quedado obsoleto. Siempre que puedas elige el sistema de cifrado WPA o mejor aún WPA2 para mayor seguridad

[WEP](https://es.wikipedia.org/wiki/Wired_Equivalent_Privacy) es el más básico de los tres, proporciona un cifrado de nivel 2 y ha quedado obsoleto al poderse romper la protección con un ordenador o dispositivo de potencia media en pocos minutos. La siguiente opción es [WPA](https://es.wikipedia.org/wiki/Wi-Fi_Protected_Access), que nace justo como solución a las vulnerabilidades más obvias de WEP. Sus siglas significan algo como “Acceso Protegido Wi-Fi” y es un sistema mucho más seguro ante los ataques de contraseñas no estando tan limitado en el número de caracteres que podemos introducir.

Por último tenemos [WPA2](https://es.wikipedia.org/wiki/WPA2), la evolución de WPA y que ofrece el nivel más alto de protección de los tres. Siempre que podamos deberemos elegirlo, aunque hay que tener cuidado de que todos los equipos de la red lo soporten (los más antiguos puede que no sean compatibles) o si no, no podrán comunicarse.

Por supuesto, elijamos el que elijamos, debemos poner una clave lo suficientemente compleja como para que nadie pueda o por lo menos le resulte cómodo asaltarla por fuerza bruta, pero que nos sea relativamente fácil de recordar, sobre todo si vamos a querer usar nuevos dispositivos con frecuencia que requerirán de la inserción de la clave al conectarse por primera vez. Tampoco está de más cambiar esta contraseña de vez en cuando para evitar posibles intrusiones con ataques de fuerza bruta.

### **Utiliza el filtrado MAC**

Otra medida de seguridad que puede resultar útil es el llamado filtrado MAC (no se trata de no dejar conectarse a los equipos de Apple, no). Las [direcciones MAC](https://es.wikipedia.org/wiki/Direcci%C3%B3n_MAC) o también llamadas direcciones físicas son las que tiene asignada cada tarjeta de red grabada directamente en su hardware y que la identifican unívocamente del resto. Es algo así como una dirección IP pero de más bajo nivel y sólo se utiliza dentro de la misma subred.

El filtrado MAC te permite crear una especie de lista de equipos de red permitidos Está compuesta por 48 bits y se representa en 6 grupos de números hexadecimales separados por dos puntos o guiones. Es algo como esto: 01:23:45:67:89:AB o bien expresado como 01-23-45-67-89-AB.

¿Dónde la encuentro? Pues depende del dispositivo y del sistema operativo que utilicemos. Incluso en algunos gadgets la podemos ver en una pegatina o en la propia caja del aparato. En este artículo tenéis varios ejemplos sobre dónde y cómo buscarla. El filtrado MAC va a consistir en crear una especie de lista de equipos de red permitidos para conectarse a nuestra WiFi. Para ello deberemos entrar a la opción correspondiente del router e introducir las direcciones que deseemos autorizar en nuestra red.

Dependiendo del modelo, también podremos hacer listas negras de equipos bloqueados, impidiendo así el acceso a dispositivos que sepamos a ciencia cierta son intrusos o gorrones de nuestra WiFi. En este artículo tenéis más detalles sobre cómo realizar correctamente este filtrado MAC con un caso concreto.

### **Reduce los rangos de direcciones IP permitidas**

Si siempre vamos a tener los mismos equipos conectados a la red, podemos utilizar la opción de deshabilitar el funcionamiento automático del [servicio DHCP](https://es.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol) (Dynamic Host Configuration Protocol) en el router que se encarga de asignar direcciones IP a cada equipo conectado a la red.

Esto nos obligará a tener que configurar los valores de forma manual en todos los dispositivos que tengamos en casa, pero puede aportar un grado más de seguridad. También podemos jugar con el rango de direcciones IP permitidas y restringirlo hasta los valores que queramos evitando que queden multitud de direcciones libres.

Es muy sencillo de hacer. Solo hay que buscar en el router la opción dentro de la configuración de la LAN en la que ponga algo como Start IP Address/End IP Address y ahí especificar los valores deseados (por ejemplo de la 192.168.1.33 a la 192.168.1.35, lo que nos permitiría conectar tres equipos a la red). Si además el router nos permite cambiar el tiempo de validez de esta asignación, podemos también indicarle una cifra muy alta y así no dejar ninguna disponible para un intruso, ya que no quedarán huecos libres.

### **Limita la potencia de emisión de las antenas**

![Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image34.png](Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image34.png)

## **Simulación de la potencia radiada por una señal WiFi**

Puede parecer obvio, pero es el método más eficaz para evitar una intrusión o el uso no permitido de tu red inalámbrica. Si no llega la señal, difícilmente alguien podrá localizar tu red y mucho menos conectarse a ella. La mayoría de los routers permiten gestionar de algún modo la potencia emitida por las antenas y así manejar el radio de cobertura de la red de forma aproximada. Lo habitual es que nos encontremos con alguna opción en la que se nos permita variar el porcentaje de nivel de señal o la potencia transmitida.

Aquí debemos procurar bajar la intensidad para que sigamos pudiendo conectarnos a la red dentro de casa, pero para que la potencia decaiga mucho fuera de ella. Podemos ir comprobándolo simplemente moviéndonos con el móvil por la casa y sus alrededores y viendo qué cobertura WiFi tenemos.

**¿Cuánto tengo que disminuirla?** Pues todo lo que puedas mientras no te perjudique ni se te corte la conexión. También puede resultar útil orientar las antenas del router, si es que nos permite hacerlo, hacia el interior de casa para ofrecer la máxima potencia dentro y que salga la menos posible hacia el exterior y ya si somos algo paranoicos utilizar algún reflector metálico para modificar la dirección del haz de energía o incluso usar algún tipo de pintura anti-radiación electromagnética en alguna de las paredes por donde no queramos que salga la señal WiFi.

## **Resumiendo**

Aunque la seguridad total no existe, siguiendo los sencillos consejos comentados anteriormente podrás mantener un buen grado de privacidad en tu red inalámbrica que seguro echará para atrás a la mayoría de vecinos y posibles espías. ¿Qué pasos tienes que seguir? Aquí tienes un resumen:

- Blinda el acceso a tu router cambiando las contraseñas y su dirección IP por defecto
- Cambia el nombre de la SSID o bien ocúltalo por completo
- Elige el sistema de cifrado WPA o mejor aún WPA2 y una calve alfanumérica larga
- Utiliza el filtrado MAC y crea una lista de equipos permitidos en tu red
- Reduce los rangos de direcciones IP admitidas en tu red local
- Limita la potencia de emisión de las antenas hacia el exterior de casa

Seguridad en la nube

Conceptos de la seguridad en la nube

La seguridad de nube empresarial es el conjunto de prácticas, protocolos, políticas y controles que las organizaciones implementan para proteger sus activos digitales en la nube. La seguridad en la nube empresarial está diseñada para proteger los entornos cloud, los datos que residen en la nube, las aplicaciones que se ejecutan en la nube y los usuarios que interactúan con los activos de la nube. En la mayoría de los entornos cloud, la seguridad es una responsabilidad compartida entre el proveedor de nube y el cliente.

## **Definición de la seguridad en la nube**

La seguridad en la nube es una disciplina de la ciberseguridad dedicada a asegurar los sistemas informáticos en la nube. Incluye mantener los datos privados y seguros a través de la infraestructura, las aplicaciones y las plataformas en línea. Asegurar estos sistemas implica los esfuerzos de los proveedores de la nube y de los clientes que los utilizan, bien se trate de una persona, una pequeña o mediana empresa o una organización.

Los proveedores de servicios en la nube alojan los servicios en sus servidores a través de conexiones de Internet siempre activas. Debido a que su negocio depende de la confianza de los clientes, se utilizan métodos de seguridad en la nube para que los datos de los clientes se mantengan privados y almacenados de forma segura. No obstante, la seguridad en la nube también está parcialmente en manos del cliente. Comprender ambas facetas es fundamental para una solución saludable de seguridad en la nube.

En su núcleo, la seguridad en la nube se compone de las siguientes categorías:

- Seguridad los datos
- Gestión de identidades y accesos (IAM, por sus siglas en inglés)
- Gobernanza (políticas de prevención, detección y mitigación de amenazas)
- Planificación de la retención de datos (DR) y la continuidad del negocio (BC)
- Cumplimiento legal

La seguridad en la nube puede parecer como la seguridad informática heredada, pero esta plataforma exige en realidad un enfoque diferente.

## **¿Qué es la seguridad en la nube?**

La seguridad en la nube es toda la tecnología, los protocolos y las buenas prácticas que protegen los entornos informáticos en la nube, las aplicaciones que se ejecutan en la nube y los datos almacenados en ella. La seguridad de los servicios en la nube comienza por comprender qué se está asegurando exactamente, así como los aspectos del sistema que se deben administrar.

A modo de resumen, el desarrollo del soporte contra las vulnerabilidades de seguridad está en gran medida en manos de los proveedores de servicios en la nube. Aparte de elegir un proveedor consciente de la seguridad, los clientes deben centrarse sobre todo en la configuración adecuada del servicio y en los hábitos de uso seguro. Además, los clientes deben asegurarse de que el hardware y las redes de los usuarios finales estén debidamente asegurados.

El alcance total de la seguridad en la nube está diseñado para proteger lo siguiente, independientemente de sus responsabilidades:

- **Redes físicas**: enrutadores, energía eléctrica, cableado, controles de clima, etc.
- **Almacenamiento de datos**: discos duros, etc.
- **Servidores de datos**: hardware y software informáticos de la red central
- **Plataformas de virtualización de equipos informáticos**: software de máquinas virtuales, máquinas anfitrionas y máquinas invitadas
- **Sistemas operativos (OS)**: software que soporta todas las funciones informáticas
- **Middleware**: gestión de la interfaz de programación de aplicaciones (API),
- **Entornos de ejecución**: ejecución y mantenimiento de un programa en ejecución
- **Datos**: toda la información almacenada, modificada y a la que se ha accedido
- **Aplicaciones**: servicios tradicionales de software (correo electrónico, software de impuestos, paquetes de productividad, etc.)
- **Hardware de usuario final**: computadoras, dispositivos móviles, dispositivos de Internet de las cosas (IoT), etc.

Con la informática en la nube, la propiedad de estos componentes puede variar ampliamente. Esto puede hacer que no esté claro el alcance de las responsabilidades de seguridad del cliente. Dado que asegurar la nube puede parecer diferente en función de quién tiene autoridad sobre cada componente, es importante entender cómo se suelen agrupar.

Para simplificar, los componentes informáticos en la nube están asegurados desde dos puntos de vista principales:

## **Los tipos de servicios en la nube**

son servicios ofrecidos por proveedores externos como módulos utilizados para crear el entorno de la nube. Dependiendo del tipo de servicio, se puede gestionar un grado diferente de los componentes dentro del servicio:

- **El núcleo de cualquier servicio de la nube de terceros** implica que el proveedor administre la red física, el almacenamiento de datos, los servidores de datos y las plataformas de virtualización de los ordenadores. El servicio se almacena en los servidores del proveedor y se virtualiza a través de su red administrada internamente para entregarse a los clientes para su acceso remoto. Esto transfiere los costes de hardware y otras infraestructuras para proporcionar a los clientes acceso a sus necesidades informáticas desde cualquier lugar a través de su conexión a Internet.
- **Los servicios en la nube de software como servicio (SaaS)** proporcionan a los clientes acceso a aplicaciones que están puramente alojadas y se ejecutan en los servidores del proveedor. Los proveedores administran las aplicaciones, los datos, el tiempo de ejecución, el middleware y el sistema operativo. Los clientes solamente se encargan de obtener y utilizar las aplicaciones. *Algunos ejemplos de SaaS incluyen Google Drive, Slack, Salesforce, Microsoft 365, Cisco WebEx y Evernote.*
- **Los servicios en la nube de plataforma como servicio** proporcionan a los clientes un host para el desarrollo de sus propias aplicaciones, que se ejecutan dentro del propio espacio “sandbox” del cliente en los servidores del proveedor. Los proveedores administran el tiempo de ejecución, el middleware y el sistema operativo. Los clientes se encargan de gestionar sus aplicaciones, datos, acceso de usuarios, dispositivos de usuarios finales y redes de usuarios finales. *Algunos ejemplos de PaaS incluyen Google App Engine y Windows Azure.*
- **Los servicios en la nube de infraestructura como servicio (IaaS)** ofrecen a los clientes hardware y plataformas de conectividad remota para alojar la mayor parte de sus tareas informáticas, incluido el sistema operativo. Los proveedores solo administran los servicios básicos en la nube. Los clientes se encargan de asegurar todo lo que se apila en un sistema operativo, incluidas las aplicaciones, los datos, los tiempos de ejecución, el middleware y el propio sistema operativo. Además, los clientes deben gestionar el acceso de los usuarios, los dispositivos de usuarios finales y las redes de usuarios finales. *Algunos ejemplos de IaaS incluyen Microsoft Azure, Google Compute Engine (GCE) y Amazon Web Services (AWS).*

## **Los entornos de la nube**

Son modelos de implementación en los que uno o más servicios en la nube crean un sistema para los usuarios finales y las empresas. Estos segmentan las responsabilidades de gestión, incluida la seguridad, entre los clientes y los proveedores.

Los entornos de la nube que se utilizan en la actualidad son:

- **Entornos** de **nubes públicas**, compuestos por servicios en la nube de varios usuarios en los que un cliente comparte los servidores de un proveedor con otros clientes, como un edificio de oficinas o un espacio de trabajo. Se trata de servicios de terceros dirigidos por el proveedor para dar acceso a los clientes a través de la web.
- **Entornos** de **nubes privadas** de terceros, que se basan en el uso de un servicio en la nube que proporciona al cliente el uso exclusivo de su propia nube. Estos entornos de un solo usuario normalmente son propiedad de un proveedor externo, y se administran y operan fuera del sitio.
- **Entornos de nubes privadas internas**, que también se componen de servidores de servicios en la nube de un solo usuario, pero se operan desde su propio centro de datos privado. En este caso, este entorno de la nube es gestionado por las propias empresas para permitir la configuración completa de cada elemento.
- **Entornos de varias nubes**, que incluyen el uso de dos o más servicios en la nube de proveedores independientes. Estos pueden ser cualquier combinación de servicios públicos o privados en la nube.
- **Entornos** de **nubes híbridas**, que consisten en el uso de una combinación de nube privada de terceros o centro de datos de nubes privadas in situ con una o más nubes públicas.

<aside>
💡 Al enfocarlo desde esta perspectiva, podemos entender que la seguridad basada en la nube puede ser un poco diferente según el tipo de espacio de nubes en el que trabajen los usuarios. No obstante, los efectos se sienten tanto en los clientes individuales como en las empresas.

</aside>

## **¿Cómo funciona la seguridad en la nube?**

Cada medida de seguridad en la nube funciona para lograr uno o más de los siguientes objetivos:

- Permitir la recuperación de datos en caso de pérdida de datos
- Proteger el almacenamiento y las redes contra el robo de datos malicioso
- Evitar los errores humanos o negligencias que causan la fuga de datos
- Reducir el impacto de cualquier compromiso de datos o sistemas

### **La seguridad de los datos**

Es un aspecto de la seguridad en la nube que implica el fin técnico de la prevención de amenazas. Existen herramientas y tecnologías que permiten a los proveedores y los clientes insertar barreras entre el acceso y la visibilidad de los datos confidenciales. Entre ellas, el *cifrado* es una de las herramientas más potentes disponibles. El cifrado codifica los datos para que solo los pueda leer alguien que tenga la clave de cifrado. En caso de pérdida o robo de los datos, no será posible leerlos ni interpretarlos. *Las protecciones para el tráfico de datos*, tales como las redes privadas virtuales (VPN), también ganan importancia en las redes de la nube.

### **La gestión de identidades y accesos (IAM)**

Se refiere a los privilegios de acceso que se ofrecen a las cuentas de los usuarios. La gestión de la autenticación y la autorización de las cuentas de usuario también se aplica aquí. *Los controles de acceso* son fundamentales para restringir a los usuarios, tanto a los legítimos como a los maliciosos, el acceso y el compromiso de los datos confidenciales y sistemas. La gestión de contraseñas, la autenticación de varios factores y otros métodos entran en el alcance de la IAM.

### **La gobernanza**

Se centra en las políticas de prevención, detección y mitigación de amenazas. Con PYMES y empresas, aspectos como la *información sobre amenazas* pueden ayudar a rastrear y priorizar las amenazas para mantener los sistemas esenciales vigilados cuidadosamente. Sin embargo, incluso los clientes individuales de la nube podrían beneficiarse de la valoración de las *políticas y la formación sobre el comportamiento seguro del usuario*. Estas se aplican sobre todo en los entornos empresariales, pero las normas para el uso seguro y la respuesta a las amenazas pueden ser útiles para cualquier usuario.

### **La planificación de la retención de datos (DR) y la continuidad del negocio (BC)**

Implica medidas técnicas de recuperación de desastres en caso de pérdida de datos. Los métodos para la *redundancia de datos*, como las copias de seguridad, son fundamentales para cualquier plan de DR y BC. Además, disponer de sistemas técnicos para garantizar la continuidad de las operaciones puede ser de gran ayuda. Las plataformas para *probar la validez de las copias de seguridad* y las instrucciones detalladas de recuperación de los empleados son igual de valiosas para un plan de BC completo.

### **El cumplimiento legal**

Gira en torno a la protección de la privacidad del usuario, tal como lo establecen los órganos legislativos. Los gobiernos asumieron la importancia de proteger la información de los usuarios privados para que no sea explotada con fines de lucro. Por lo tanto, las empresas deben seguir los reglamentos para cumplir con estas políticas. Uno de los enfoques es el uso del *enmascaramiento de datos*, que oculta la identidad dentro de los datos mediante métodos de cifrado*.*

## **¿Qué hace que la seguridad en la nube sea diferente?**

La seguridad informática tradicional ha experimentado una inmensa evolución debido al cambio a la informática basada en la nube. Si bien los modelos de la nube permiten una mayor comodidad, la conectividad siempre activa requiere nuevas consideraciones para mantenerlas seguras. La seguridad en la nube, como una solución de ciberseguridad modernizada, se distingue de los modelos informáticos heredados en algunos aspectos.

### **Almacenamiento de datos:**

La mayor distinción es que los modelos antiguos de TI dependían en gran medida del almacenamiento de datos in situ. Las empresas han descubierto desde hace mucho tiempo que la creación de todas las plataformas informáticas internas para los controles de seguridad detallados y personalizados es costosa y rígida. Las plataformas basadas en la nube han ayudado a transferir los costes de desarrollo y mantenimiento de los sistemas, pero también a eliminar cierto control de los usuarios.

### **Velocidad de escalada:**

De manera similar, la seguridad en la nube exige una atención única al escalar los sistemas de TI de la empresa. La infraestructura y las aplicaciones centradas en la nube son muy modulares y se movilizan rápidamente. Si bien esta capacidad mantiene los sistemas uniformemente ajustados a los cambios empresariales, también plantea problemas cuando la necesidad de mejoras y comodidad de una empresa supera su capacidad para mantenerse al día en materia de seguridad.

### **Interfaz del sistema de usuarios finales:**

Tanto para las empresas como para los usuarios individuales, los sistemas de nubes también se conectan con muchos otros sistemas y servicios que se deben asegurar. Los permisos de acceso deben mantenerse desde el nivel de dispositivo de usuario final hasta el nivel de software e incluso el nivel de red. Además, tanto proveedores como usuarios deben estar atentos a las vulnerabilidades que pueden causar a través de comportamientos de configuración y acceso al sistema inseguros.

### **Proximidad a otros datos y sistemas en red:**

Dado que los sistemas en la nube son una conexión persistente entre los proveedores de la nube y todos sus usuarios, esta importante red puede comprometer incluso al propio proveedor. En los entornos de redes, un solo dispositivo o componente débil se puede explotar para infectar al resto. Los proveedores de la nube se exponen a las amenazas de muchos usuarios finales con los que interactúan, bien sea que estén proporcionando almacenamiento de datos u otros servicios. Las responsabilidades adicionales en materia de seguridad de la red recaen en los proveedores cuyos productos entregados de otro modo se basarían exclusivamente en los sistemas de los usuarios finales y no en los propios.

Resolver la mayoría de los problemas de seguridad en la nube significa que tanto los usuarios como los proveedores de la nube, tanto en entornos personales como en empresariales, deben ser proactivos en cuanto a sus propias funciones en la ciberseguridad. Este doble enfoque significa que los usuarios y los proveedores deben abordar lo siguiente:

- Configuración y mantenimiento seguros del sistema.
- Educación sobre seguridad del usuario, tanto a nivel de comportamiento como a nivel técnico.

Por último, los proveedores y los usuarios de la nube deben tener transparencia y responsabilidad para garantizar que ambas partes estén seguras.

## **Riesgos de seguridad en la nube**

¿Cuáles son los problemas de seguridad en la informática en la nube? Si no es consciente de su existencia ¿cómo se supone que va a tomar las medidas adecuadas? Después de todo, una seguridad débil en la nube puede exponer a los usuarios y proveedores a todo tipo de amenazas de ciberseguridad. Algunas amenazas comunes a la seguridad en la nube incluyen:

- **Riesgos de la infraestructura basada en la nube**, incluidas las plataformas informáticas heredadas incompatibles y las interrupciones de los servicios de almacenamiento de datos de terceros.
- **Amenazas internas debidas a errores humanos** como, por ejemplo, la mala configuración de los controles de acceso de los usuarios.
- **Amenazas externas** causadas casi exclusivamente por actores maliciosos, como malware, phishing y ataques de DDoS.

El mayor riesgo que plantea la nube es que no existe un perímetro. La ciberseguridad tradicional se centraba en proteger el perímetro, pero los entornos en la nube están altamente conectados, lo que conlleva que las interfaces de programación de aplicaciones (API) sean inseguras y los secuestros de cuentas puedan plantear problemas reales. Frente a los riesgos para la seguridad que afectan a la computación en la nube, los profesionales de la ciberseguridad deben adoptar un planteamiento más centrado en los datos.

La interconexión también plantea problemas para las redes. Los actores maliciosos a menudo acceden a las redes debido a credenciales comprometidas o débiles. Una vez que un hacker consigue acceder a una red, puede propagarse fácilmente y utilizar las interfaces mal protegidas de la nube para localizar datos en diferentes bases de datos y nodos. Incluso puede utilizar sus propios servidores en la nube como destino donde exportar y almacenar los datos robados. La seguridad tiene que estar en la nube y no servir como elemento exclusivo para proteger frente al acceso a los datos que allí se almacenan.

El almacenamiento de los datos por parte de terceros y el acceso a través de Internet también plantean sus propias amenazas. Si, por algún motivo, estos servicios se interrumpen, podría perderse el acceso a los datos. Por ejemplo, un corte en la red telefónica podría significar que no se puede acceder a la nube en un momento esencial. Alternativamente, un corte de energía podría afectar al centro de datos donde se almacenan los datos, lo que podría conllevar una pérdida de datos permanente.

Dicho tipo de interrupciones podrían tener repercusiones a más largo plazo. Un reciente corte del suministro eléctrico en una instalación de datos en la nube de Amazon resultó en la pérdida de los datos de algunos clientes debido a los desperfectos que se ocasionaron en el hardware de los servidores. Este es un buen ejemplo de por qué conviene tener copias de seguridad locales de al menos algunos de sus datos y aplicaciones.

## **¿Por qué es importante la seguridad en la nube?**

En la década de 1990, los datos comerciales y personales se almacenaban y gestionaban a nivel local, y la seguridad también era local. Los datos se encontraban en el almacenamiento interno de un PC en casa, y en los servidores de la empresa, si trabajaba para una empresa.

La introducción de la tecnología de la nube ha obligado a todos a reevaluar la ciberseguridad. Los datos y aplicaciones pueden estar flotando entre sistemas locales y remotos, y estar siempre accesibles por Internet. Si accede a Google Docs desde el teléfono o PC esos datos pueden guardarse en cualquier parte.

De ahí que protegerlos sea más difícil que cuando solo se trataba de impedir que usuarios no deseados accedieran a su red. La seguridad en la nube requiere ajustar algunas prácticas informáticas previas, pero se ha vuelto más esencial por dos razones clave:

### **Comodidad por encima de la seguridad.**

La informática en la nube está creciendo de forma exponencial como método principal tanto para el lugar de trabajo como para el uso individual. La innovación ha permitido que la nueva tecnología se implemente más rápido de lo que avanzan las normas de seguridad de la industria, lo que hace que los usuarios y los proveedores tengan más responsabilidad a la hora de considerar los riesgos de la accesibilidad.

### **Centralización y almacenamiento para múltiples usuarios.**

Cada componente, desde la infraestructura básica hasta pequeños datos como correos electrónicos y documentos, puede ahora localizarse y accederse de forma remota e ininterrumpida a través de conexiones basadas en la web. Toda esta recopilación de datos en los servidores de unos pocos proveedores de servicios importantes puede ser muy peligrosa. Los actores de amenazas pueden atacar ahora a grandes centros de datos de varias empresas y causar importantísimas filtraciones de datos.

Lamentablemente, los actores maliciosos se dan cuenta del valor de los objetivos basados en la nube y los investigan cada vez más para encontrar sus vulnerabilidades de seguridad. A pesar de que los proveedores de la nube asumen muchas funciones de seguridad de los clientes, no lo gestionan todo. Esto deja incluso a los usuarios no técnicos con el deber de auto educarse sobre la seguridad en la nube.

Dicho esto, los usuarios no están solos en lo que respecta a las responsabilidades de seguridad en la nube. Ser consciente del alcance de sus deberes de seguridad ayudará a que todo el sistema esté mucho más seguro.

## **Preocupaciones de la seguridad en la nube: privacidad**

Se han promulgado nuevas leyes para ayudar a proteger a los usuarios finales frente a la venta y el intercambio de sus datos confidenciales. El [Reglamento general de protección de datos (GDPR)](https://gdpr-info.eu/) y la [Ley de portabilidad y responsabilidad del seguro médico (HIPAA)](https://en.wikipedia.org/wiki/Health_Insurance_Portability_and_Accountability_Act) cumplen cada uno con sus propios deberes de protección de la privacidad, al limitar la forma en que se pueden almacenar los datos y acceder a ellos.

Se han utilizado métodos de administración de identidades, como el enmascaramiento de datos, para separar las características identificables de los datos de los usuarios, a fin de cumplir con el GDPR. En lo que respecta al cumplimiento de la HIPAA, las empresas como los centros de atención médica deben asegurarse de que su proveedor también haga su parte en cuanto a la restricción del acceso a los datos.

La [ley CLOUD](https://www.congress.gov/bill/115th-congress/house-bill/4943) otorga a los proveedores de servicios en la nube sus propias limitaciones legales que deben cumplir, potencialmente a costa de la privacidad del usuario. La ley federal de EE. UU. ahora permite a las fuerzas policiales a nivel federal exigir los datos solicitados de los servidores del proveedor de la nube. Si bien esto puede permitir que las investigaciones procedan de manera eficaz, puede eludir algunos derechos a la privacidad y causar un posible abuso de poder.

## **Cómo asegurar la nube**

Por suerte, existen muchas opciones para proteger sus propios datos en la nube. Veamos algunos de los métodos más conocidos.

El **cifrado** es una de las mejores maneras de proteger sus sistemas de informática en la nube. Existen diversas maneras de usar el cifrado, y puede ofrecerlas el proveedor de servicios en la nube o un proveedor de soluciones de seguridad en la nube independiente:

- **Cifrado de las comunicaciones** con la nube en su totalidad.
- **Cifrado de datos especialmente confidenciales**, como las credenciales de las cuentas.
- **Cifrado de extremo a extremo** de todos los datos que se suben a la nube.

En la nube, los datos corren más riesgo de ser interceptados cuando están en movimiento. Cuando se están trasladando entre dos ubicaciones de almacenamiento o cuando se transmiten a su aplicación local, los datos son más vulnerables. Por este motivo, el cifrado de extremo a extremo es la mejor solución de seguridad en la nube para los datos esenciales. Con el cifrado de extremo a extremo, en ningún momento su comunicación se pone a disposición de personas que no dispongan de la clave de cifrado.

Puede cifrar los datos usted mismo antes de guardarlos en la nube o usar un proveedor de servicios en la nube que los cifre como parte de los servicios que le ofrece. Sin embargo, si solo utiliza la nube para almacenar sus datos no sensibles, como, por ejemplo, el material gráfico o los vídeos de su empresa, el cifrado de extremo a extremo podría ser excesivo. Por otro lado, en el caso de la información financiera, confidencial o comercialmente sensible, este tipo de cifrado es vital.

Si utiliza cifrado, recuerde que es fundamental manejar de manera segura su clave de cifrado. Guarde una copia de seguridad de la clave y, si es posible, no la guarde en la nube. Asimismo, puede que sea de utilidad cambiar las claves de cifrado de manera periódica para que, si alguien consigue acceder a ellas, quede desconectado del sistema cuando realice el cambio.

La **configuración** es otra herramienta de enorme utilidad en la seguridad en la nube. Muchas infracciones de datos en la nube se deben a vulnerabilidades básicas, tales como errores de configuración. Al prevenirlas, está disminuyendo enormemente el riesgo de seguridad en la nube. Si no se siente seguro/a al hacerlo, plantéese utilizar un proveedor de soluciones de seguridad en la nube.

A continuación le indicamos algunos de los principios que puede seguir:

1. **Nunca deje sin modificar la configuración predeterminada**. Utilizar la configuración predeterminada permite al hacker entrar por la puerta principal: es como dejarse la llave puesta en la puerta de casa. Evite hacerlo para complicar el acceso a su sistema.
2. **Nunca deje un sector de almacenamiento en la nube abierto.** Los hackers podrían ver el contenido con solo abrir la URL del sector de almacenamiento.
3. **Si el proveedor de servicios en la nube le proporciona controles de seguridad que puede activar**, utilícelos. No seleccionar las opciones de seguridad correctas podría ponerle en riesgo.

## **Los consejos básicos de ciberseguridad**

También se deben incorporar en cualquier implementación de la nube. Si utiliza la nube, conviene que no pase por alto las prácticas estándar de ciberseguridad. Merece la pena que tenga en cuenta los siguientes aspectos si desea contar con la máxima seguridad en Internet:

- **Utiliza contraseñas seguras: c**ombinar letras, números y caracteres especiales hará que resulte más difícil descifrar una contraseña. Procure evitar opciones previsibles, como reemplazar una S por el símbolo del dólar ($). Cuanto más aleatoria sea la secuencia de una contraseña, mejor.
- **Utiliza un administrador de contraseñas:** podrás asignar a cada aplicación, base de datos y servicio que utilice una contraseña propia, sin necesidad de recordarlas todas. No obstante, es esencial que se asegure de proteger su administrador de contraseñas con una contraseña maestra segura.
- **Protege todos los dispositivos:** para acceder a los datos en la nube, incluidos los smartphones y tablets. Si tienes los datos sincronizados en varios dispositivos, cualquiera de ellos podría ser un eslabón débil que ponga toda su huella digital en riesgo.
- **Haz una copia de seguridad de sus datos periódicamente:** para que, en caso de producirse un apagón en la nube o una pérdida de datos en su proveedor de servicios en la nube, pueda restaurarlos completamente. Puede guardar la copia de seguridad en un equipo en su casa, en un disco duro externo, o incluso de nube a nube, siempre y cuando esté seguro/a de que los dos proveedores de nube no comparten la infraestructura.
- **Modifica los permisos:** para evitar que ningún dispositivo o persona acceda a todos sus datos a menos que sea necesario. Por ejemplo, las empresas lo hacen configurando los permisos de sus bases de datos. Si tiene una red doméstica, utilice redes de invitados para sus hijos, para sus dispositivos IoT y para la televisión. Guarde su permiso «acceso a todas las zonas» para su uso personal.
- **Protégete con un buen software antivirus y antimalware: l**os hackers podrán acceder fácilmente a su cuenta si un malware se abre camino en su sistema.
- **Evita acceder a sus datos a través de una Wi-Fi pública:** sobre todo si no está protegida por una autenticación segura. Utilice una red privada virtual (VPN) para proteger su acceso a la nube.

## **Almacenamiento y uso compartido de archivos en la nube**

Los riesgos de seguridad de la informática en la nube pueden afectar a todos, desde las empresas hasta los consumidores individuales. Los usuarios pueden utilizar la nube para guardar archivos y copias de seguridad (en servicios como Dropbox), así como para servicios como el correo electrónico y aplicaciones de ofimática, o para rellenar formularios de impuestos y llevar a cabo su contabilidad.

También deberían pensar en cómo comparte los datos en la nube con los demás, sobre todo si trabaja como asesor o por cuenta propia. Si bien compartir archivos en Google Drive u otro servicio puede ser un modo fácil de trabajar con clientes, debe asegurarse de que está gestionando correctamente los permisos. Después de todo, querrá asegurarse de que sus diferentes clientes no puedan ver los nombres o los directorios de los demás ni alterar sus archivos.

Recuerda que muchos de estos servicios de almacenamiento en la nube de uso generalizado no cifran los datos. Si quiere mantener sus datos seguros mediante el cifrado, deberá usar un software específico para cifrarlos antes de cargarlos. A continuación, tendrás que facilitar a sus clientes una clave, ya que, de otro modo, no podrán leer los archivos.

## **Comprueba la seguridad de su proveedor de servicios en la nube**

La seguridad debe ser uno de los principales puntos a considerar a la hora de elegir un proveedor de seguridad en la nube. La ciberseguridad de sus datos no es solo asunto suyo; un proveedor de servicios en la nube debe velar por crear un entorno seguro en la nube y compartir la responsabilidad por la seguridad de los datos.

Desafortunadamente, las empresas de la nube no le darán los planos de seguridad de su red. Esto equivaldría a que un banco le diese sus datos de seguridad, incluidos los números de combinación de la caja fuerte.

Sin embargo, obtener las respuestas correctas a algunas preguntas básicas le dará una mayor confianza de que sus activos en la nube estarán seguros. Además, será más consciente de si su proveedor ha abordado adecuadamente los riesgos obvios de seguridad en la nube.

Te recomendamos plantearle a tu proveedor cloud algunas de las siguientes preguntas:

- **Auditorías de seguridad**: “¿realiza regularmente auditorías externas de su seguridad?”
- **Segmentación de los datos:** "¿los datos de los clientes se segmentan de forma lógica y se mantienen separados?"
- **Cifrado:** "¿están cifrados los datos? ¿Qué partes de los datos están cifradas?”
- **Retención de datos del cliente:** "¿qué políticas de retención de datos de clientes se están siguiendo?"
- **Retención de datos del usuario:** "¿mis datos se borrarán correctamente si dejo de utilizar su servicio en la nube?"
- **Gestión del acceso:**"¿cómo se controlan los derechos de acceso?"

También querrás asegurarse de haber leído las condiciones de servicio (TOS) de su proveedor. Leer las condiciones de servicio es esencial para comprender si está recibiendo exactamente lo que quiere y necesita.

Asegúrate de comprobar que también conoce todos los servicios utilizados con su proveedor. Si sus archivos están en Dropbox o guarda una copia de seguridad en iCloud (el almacenamiento en la nube de Apple), podría significar perfectamente que se almacenan en servidores de Amazon. Por lo tanto, le convendría comprobar AWS, además del servicio que utiliza directamente.

### **Soluciones de seguridad en la nube híbrida**

Los servicios de seguridad en la nube híbrida pueden ser una opción muy inteligente para los clientes en los espacios de las PYMES y las empresas. Son más viables para las aplicaciones de las PYMES y las empresas, ya que generalmente son demasiado complejos para el uso personal. No obstante, estas empresas podrían utilizar la combinación de escala y accesibilidad de la nube con el control in situ de los datos específicos. Estos son algunos de los beneficios de seguridad de los sistemas de seguridad en la nube híbrida:

### **La segmentación de los servicios**

Puede ayudar a una empresa a controlar la forma en que se accede a sus datos y se almacenan. Por ejemplo, guardar los datos más confidenciales in situ mientras se transfieren otros datos, aplicaciones y procesos a la nube puede ayudar a separar correctamente en capas la seguridad. Además, la separación de los datos puede mejorar la capacidad de su empresa para cumplir legalmente con los reglamentos de datos.

### **La redundancia**

También se puede lograr a través de entornos de la nube híbrida. Al utilizar las operaciones diarias de los servidores de la nube pública y al hacer copias de seguridad de los sistemas en los servidores de datos locales, las empresas pueden mantener sus operaciones en movimiento en caso de que un centro de datos se desconecte o se infecte con ransomware.

### **Soluciones de seguridad en la nube para PYMES**

Si bien las empresas pueden insistir en tener una nube privada, el equivalente en Internet a tener su propio campus o edificio de oficinas, las personas, a título individual, así como las pequeñas empresas, tienen que trabajar con servicios en la nube pública. Vendría a ser como compartir una oficina o vivir en un edificio con centenares de vecinos. De ahí que su seguridad deba ser una de sus principales preocupaciones.

En las aplicaciones de las pequeñas y medianas empresas, descubrirá que la seguridad en la nube reside en gran medida en los proveedores públicos que utiliza. Sin embargo, hay medidas que puede tomar para mantenerse a salvo:

- **Segmentación de datos de varios usuarios:** las empresas deben asegurarse de que ningún otro cliente de su proveedor de servicios en la nube pueda acceder a sus datos. Bien sea que estén alojados en servidores segmentados o cuidadosamente codificados, asegúrese de que se aplique correctamente las medidas de segmentación adecuadas.
- **Controles de acceso de los usuarios:** los permisos de control pueden significar que el acceso de los usuarios se reduzca a un nivel que resulte incómodo. Sin embargo, ser restrictivo y trabajar de forma segura para encontrar un equilibrio puede ser mucho más seguro que permitir que los permisos sin asignar se filtren en su red.
- **Cumplimiento legal de los datos:** mantener los datos de conformidad con los reglamentos internacionales como el GDPR es crítico para evitar importantes sanciones y daños a la reputación. Asegúrese de que las medidas como el enmascaramiento de datos y la clasificación de datos confidenciales sean una prioridad para su empresa.
- **Escalada cuidadosa de los sistemas de la nube:** con la rápida implementación de los sistemas de la nube, asegúrese de tomarse el tiempo necesario para revisar los sistemas de su empresa para obtener seguridad por encima de la comodidad. Los servicios en la nube pueden extenderse rápidamente hasta el punto de carecer de reglamento.

## **Soluciones de seguridad en la nube para empresas**

Dado que hoy en día más del 90 % de las grandes empresas utilizan la computación en la nube, la seguridad en la nube se ha convertido en un aspecto esencial de la ciberseguridad corporativa. Los servicios en la nube privada y otras infraestructuras más costosas pueden ser viables para las organizaciones de nivel empresarial. Sin embargo, deberá asegurarse de que su TI interna se encargue de mantener toda la superficie de sus redes.

Para el uso de empresas a gran escala, la seguridad en la nube puede ser mucho más flexible si realiza algunas inversiones en infraestructura. Existen algunos principios fundamentales que debe tener en cuenta:

- **Administra activamente sus cuentas y servicios:** si ya no utilizas un servicio o software, desactívelo y ciérrelo correctamente. Los hackers pueden acceder fácilmente a toda una red de la nube a través de cuentas obsoletas e inactivas por medio de vulnerabilidades sin parches.
- **Autenticación de varios factores (MFA):** podría tratarse de datos biométricos, como huellas dactilares, o de una contraseña y el envío de un código independiente a su dispositivo móvil. Lleva más tiempo, pero es útil para proteger los datos más sensibles.
- **Evalúa los costes y los beneficios de la nube híbrida:** la segmentación de los datos es mucho más importante en el uso empresarial, ya que manejará cantidades mucho mayores de datos. Debe asegurarse de que sus datos estén separados de los de otros usuarios, bien sea cifrados por separado o segmentados lógicamente para un almacenamiento aparte. Los servicios en la nube híbrida pueden ser de gran ayuda.
- **Desconfía de la TI en la sombra**: es esencial educar a sus empleados para evitar el uso de servicios en la nube no autorizados en sus redes o para el trabajo de la empresa. Si se comunican datos confidenciales or canales no seguros, su empresa puede estar expuesta a actores maliciosos o a problemas jurídicos.

Por lo tanto, bien sea un usuario individual, un usuario de una PYME o incluso un usuario de la nube a nivel empresarial, es importante asegurarte de que su red y sus dispositivos sean lo más seguros posible. Esto comienza con una buena comprensión de la ciberseguridad básica a nivel de usuario individual, así como con la garantía de que su red y todos los dispositivos están protegidos por una solución de seguridad robusta diseñada para la nube.

## **¿Qué nivel de seguridad tienen las nubes públicas frente a las privadas?**

![Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image35.png](Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image35.png)

Los servicios en la nube pública los presta un proveedor externo desde un depósito virtualizado de recursos en el que varios clientes o "inquilinos" pueden alquilar recursos informáticos en el mismo servidor físico. Esto puede añadir un ligero riesgo de seguridad a los activos de un cliente que se ejecutan en la nube. Además, los equipos de seguridad tienen una visibilidad limitada de las cargas de trabajo que se ejecutan en soluciones de nube pública, lo que dificulta garantizar la protección.

Por otro lado, una nube privada puede ofrecer un mayor control y seguridad, ya que todos los recursos de la nube están dedicados a un único cliente. Los clientes de nube privada tienen acceso a servidores bare metal dentro de la nube que ayudan a garantizar que no compitan por ancho de banda con otros clientes y evitan los riesgos de seguridad que otros clientes pueden representar. Además, los equipos de seguridad tienen una mayor visibilidad de la infraestructura subyacente de una nube privada.

## **¿Qué son las amenazas para la seguridad de nube empresarial?**

Los entornos de nube empresarial se enfrentan a una amplia variedad de desafíos y posibles amenazas de seguridad.

- **Configuración incorrecta**. Si los ajustes de seguridad se configuran incorrectamente o no se implementan, puede provocar que los agentes maliciosos aprovechen las vulnerabilidades y obtengan fácilmente acceso no autorizado a los datos, las aplicaciones y los sistemas.
- **Ataques de denegación de servicio (DoS)**. Los ataques DoS y los ataques distribuidos de denegación de servicio (DDoS) están diseñados para ralentizar o bloquear un equipo o red. Los ataques DoS suelen ser un preámbulo de ataques más devastadores.
- **Ciberataques**. Las amenazas de ciberseguridad como el ransomware, el malware y las filtraciones de datos, son comunes y potentes, lo que a menudo da lugar a daños de millones de dólares para las empresas.
- **API desprotegidas**. Cuando las APIs que permiten que los programas de software se comuniquen entre sí quedan desprotegidas, suponen un punto de entrada fácil para los agentes maliciosos.
- **Robo de cuentas**. Los atacantes pueden utilizar credenciales robadas para acceder y secuestrar una cuenta de usuario, haciéndose pasar por el usuario para robar dinero o acceder a datos confidenciales.
- **Filtraciones de datos**. Las filtraciones de datos maliciosas o accidentales pueden poner en peligro la seguridad de los datos y exponer información confidencial o datos de clientes almacenados en la nube.
- **Error humano**. Las investigaciones demuestran que la mayoría de los fallos de seguridad en la nube son el resultado de errores humanos, como visitar un sitio web malicioso, compartir credenciales de inicio de sesión, caer en una estafa de phishing o no [practicar una buena higiene de seguridad](https://www.gartner.com/smarterwithgartner/is-the-cloud-secure).

## **¿Cuáles son los desafíos de la seguridad de nube empresarial?**

- **Entornos de nube multicliente**. Los clientes en entornos de nube pública utilizan recursos de nube que pueden compartir un servidor físico con otros clientes o inquilinos, lo que aumenta la preocupación de que los activos de un cliente puedan verse comprometidos por ataques maliciosos contra otro inquilino.
- **Falta de visibilidad**. La visibilidad puede ser un problema para las organizaciones que utilizan varios proveedores de nube. Este enfoque descentralizado de la gestión de la nube puede crear puntos ciegos, como terminales, cargas de trabajo y tráfico, que no se gestionan o protegen correctamente.
- **TI en la sombra**. Con la tendencia a lugares de trabajo remotos e híbridos y el uso de dispositivos personales, existe un mayor riesgo de que los usuarios empleen TI en la sombra o recursos de nube no autorizados, ya que buscan acceder a los datos y recursos que necesitan para mantener su productividad.
- **Cargas de trabajo dinámicas**. Las cargas de trabajo en la nube implican diversos procesos y recursos, como máquinas virtuales, contenedores, bases de datos, etc. Garantizar la protección de cada parte de la carga de trabajo puede ser una tarea compleja.
- **Cumplimiento de normativas**. Los marcos normativos, como HIPAA y PCI DSS, tienen requisitos estrictos para el almacenamiento, uso y protección de los datos de los clientes y la información de los pacientes por parte de las empresas. Cuando los datos se almacenan en la nube, las organizaciones pueden encontrar más difícil garantizar el cumplimiento de los requisitos de residencia y soberanía de dichos datos.

## **¿Cuál es el modelo de responsabilidad compartida para la seguridad empresarial?**

La mayoría de los proveedores de servicios en la nube abordan la seguridad de nube empresarial con un modelo de responsabilidad compartida. En virtud de este acuerdo, el proveedor de nube es responsable de proteger la infraestructura subyacente que pone a disposición de los clientes como servicios en la nube, y el cliente es responsable de proteger cualquier parte del entorno de nube sobre la que tenga el control.

Si los equipos de TI y las organizaciones no tienen claras sus responsabilidades en este modelo, puede dar lugar a brechas en los controles y programas de seguridad que los agentes maliciosos pueden aprovechar fácilmente.

## **¿Cómo funciona la responsabilidad compartida en diferentes entornos de nube?**

El nivel de responsabilidad que tienen las empresas para proteger sus activos en la nube depende del tipo de modelo de prestación de servicios en la nube. En las soluciones de infraestructura como servicio (IaaS), el proveedor de nube es responsable de proteger la infraestructura como los componentes de servidores, almacenamiento y red, mientras que el cliente es responsable de proteger las aplicaciones, los terminales, las cargas de trabajo y los datos.

En las ofertas de plataforma como servicio (PaaS), el proveedor de nube protege todo el hardware y el software, mientras que el cliente es responsable de proteger todas las aplicaciones desarrolladas en la plataforma, así como los terminales, las cargas de trabajo y la seguridad de los usuarios y de la red. En las soluciones de software como servicio (SaaS), el proveedor de servicios en la nube protege toda la infraestructura y las aplicaciones, mientras que el cliente es responsable de proteger solo los terminales, las cargas de trabajo, los datos y la seguridad de los usuarios y la red.

## **¿Cuáles son las claves de la seguridad de nube empresarial?**

Para mantener una estrategia de seguridad sólida, la seguridad de nube empresarial requiere un enfoque multicapa de la estrategia de seguridad. Las soluciones de seguridad basada en la nube más comunes incluyen:

- **Gestión de acceso e identidades**. Las soluciones de control de acceso sólido, permisos estrictos y autenticación multifactor dificultan a los atacantes el uso de credenciales robadas para acceder a los entornos de nube.
- **Supervisión continua**. Las soluciones de seguridad que permiten a los equipos de TI supervisar continuamente las plataformas y los servicios en la nube pueden ayudar a identificar y corregir rápidamente las posibles amenazas.
- **Seguridad de red de nube**. Las soluciones para segmentar los activos en la nube pueden reducir el impacto de una filtración. La tecnología de seguridad de red en la nube también puede supervisar el tráfico y proteger los datos y los activos digitales contra la explotación y el movimiento lateral.
- **Protección de datos**. El cifrado de datos en tránsito y en reposo puede proteger los datos almacenados en la nube y simplificar el cumplimiento de una amplia gama de leyes y normativas.
- **Inteligencia sobre amenazas**. El acceso a información actualizada sobre amenazas puede ayudar a las organizaciones a identificar y defenderse de las ciberamenazas emergentes.
- **Agentes seguros de acceso a la nube (CASB)**. Un CASB se sitúa entre los clientes y sus servicios en la nube para ayudar a aplicar políticas de seguridad y añadir una capa de seguridad.
- **Acceso de red Zero Trust (ZTNA)**. Las soluciones ZTNA proporcionan un acceso remoto seguro a los activos en la nube con cada solicitud, lo que garantiza que los usuarios o las aplicaciones que solicitan se autentican continuamente.

## **¿Cuáles son las ventajas de la seguridad basada en la nube?**

Las soluciones de seguridad basada en la nube proporcionan servicios de seguridad desde servidores en centros de datos remotos a través de una conexión a Internet. Con las soluciones basadas en la nube, las empresas pueden evitar el coste y el esfuerzo de implementar equipos en entornos locales. Los equipos de seguridad pueden gestionar los programas de seguridad de forma remota desde un único panel, desde cualquier parte del mundo. Las soluciones de seguridad basada en la nube ofrecen una escalabilidad mucho mayor que la tecnología de entorno local, y elegir soluciones basadas en la nube ayuda a preparar los sistemas de seguridad para el futuro.

## **Preguntas frecuentes**

**¿Son más seguras las nubes públicas o las privadas?**

Con los servicios de nube pública, varios clientes o inquilinos pueden compartir recursos informáticos en el mismo servidor físico, lo que aumenta el riesgo de los activos en la nube. Además, los equipos de seguridad tienen una visibilidad limitada de las cargas de trabajo que se ejecutan en soluciones de nube pública, lo que dificulta garantizar la protección. Los entornos de nube privada más control y seguridad, ya que todos los recursos de la nube están dedicados a un único cliente y los equipos de seguridad tienen una mayor visibilidad de la infraestructura subyacente de una arquitectura de nube privada.

**¿Qué es la optimización de la nube?**

La optimización de la nube es el proceso de determinar la mejor forma de elegir y asignar recursos de nube para maximizar el rendimiento, racionalizar los recursos y minimizar los costes. Al ayudar a mitigar la propagación no controlada de instancias, servicios o proveedores de nube en una organización, la optimización de la nube puede ayudar a mejorar la estrategia de seguridad.

**¿Cuáles son las ventajas de la seguridad basada en la nube?**

Las soluciones de seguridad basada en la nube proporcionan servicios de seguridad desde servidores en centros de datos remotos a través de una conexión a Internet. Con las soluciones basadas en la nube, las empresas pueden evitar el coste y el esfuerzo de implementar equipos en entornos locales.

**¿Son las nubes privadas más seguras que los servicios de nube pública?**

Las nubes públicas y privadas son formas de almacenar datos en Internet. Los servicios en la nube pública se comparten entre varios clientes, lo que significa que pueden ser menos seguros. Las nubes privadas son solo para un cliente y le proporcionan más control y seguridad.

## Amenazas y vulnerabilidades de la seguridad en la nube

Casi todas las organizaciones han adoptado la computación en la nube en distintos grados dentro de sus negocios. Sin embargo, con esta adopción de la nube surge la necesidad de garantizar que la estrategia de seguridad en la nube de la organización sea capaz de proteger contra las principales amenazas a la seguridad en la nube.

### **Mal configuración**

Las configuraciones incorrectas de los ajustes de seguridad en la nube son una de las principales causas de las filtraciones de datos en la nube. Las estrategias de gestión de la postura de seguridad en la nube de muchas organizaciones son inadecuadas para proteger su infraestructura basada en la nube.

Varios factores contribuyen a esto. La infraestructura de la nube está diseñada para ser fácilmente utilizable y permitir compartir datos fácilmente, lo que dificulta que las organizaciones garanticen que solo las partes autorizadas puedan acceder a los datos. Además, las organizaciones que utilizan una infraestructura basada en la nube tampoco tienen visibilidad y control completos sobre su infraestructura, lo que significa que deben depender de los controles de seguridad proporcionados por su proveedor de servicios en la nube (CSP) para configurar y asegurar su implementación en la nube.

Dado que muchas organizaciones no están familiarizadas con la seguridad de la infraestructura de la nube y, a menudo, tienen implementación de múltiples nubes (cada una con una gama diferente de controles de seguridad proporcionados por el proveedor), es fácil que una mala configuración o una supervisión de la seguridad dejen los recursos basados en la nube de una organización expuestos a los atacantes.

### **Acceso no autorizado**

A diferencia de la infraestructura local de una organización, su implementación basada en la nube está fuera del perímetro de la red y es directamente accesible desde la Internet pública. Si bien esto es un activo para la accesibilidad de esta infraestructura para empleados y clientes, también facilita que un atacante obtenga acceso no autorizado a los recursos basados en la nube de una organización. La seguridad configurada de manera incorrecta o las credenciales comprometidas pueden permitir que un atacante obtenga acceso directo, potencialmente sin el conocimiento de una organización.

### **Interfaces/API inseguras**

Los CSP suelen proporcionar una serie de interfaces de programación de aplicaciones (API) e interfaces para sus clientes. En general, estas interfaces están bien documentadas en un intento de hacerlas fácilmente utilizables para los clientes de un CSP. Sin embargo, esto crea problemas potenciales si un cliente no ha protegido adecuadamente las interfaces para su infraestructura basada en la nube. Un ciberdelincuente también puede utilizar la documentación diseñada para el cliente para identificar y explotar métodos potenciales para acceder y extraer datos confidenciales del entorno de nube de una organización.

Actualmente los servicios en la Nube ofrecen APIs. Las cuales son las interfaces **que son diseñadas para protegerse contra intentos accidentales y malintencionados.** Los equipos de TI utilizan interfaces y APIs para administrar e interactuar con servicios en la Nube.

Tanto la seguridad y disponibilidad de los servicios, la autenticación y control de acceso depende de la seguridad API, las interfaces y APIs débiles exponen a las organizaciones a las cuestiones de seguridad relacionadas con la confidencialidad, integridad, disponibilidad y responsabilidad.

Las APIs e interfaces tienden a ser la parte más expuesta de un sistema, ya que por lo general son accesibles desde la Internet abierta, por eso se recomienda controles adecuados y revisiones de código centrados en la seguridad y pruebas de penetración rigurosa.

### **Secuestro de cuentas**

Muchas personas tienen una seguridad de contraseñas extremadamente débil, lo que incluye la reutilización de contraseñas y el uso de contraseñas débiles. Este problema exacerba el impacto de los ataques de phishing y las filtraciones de datos, ya que permite el uso de una sola contraseña robada en varias cuentas diferentes.

El secuestro de cuentas es uno de los problemas de seguridad en la nube más graves, ya que las organizaciones dependen cada vez más de la infraestructura y las aplicaciones basadas en la nube para las funciones comerciales principales. Un atacante con las credenciales de un empleado puede acceder a datos o funcionalidades confidenciales, y las credenciales de clientes comprometidas brindan control total sobre su cuenta en línea. Además, en la nube, las organizaciones a menudo carecen de la capacidad de identificar y responder a estas amenazas con la misma eficacia que en la infraestructura local.

Por lo general, las brechas de datos y otros ataques son el resultado de contraseñas débiles o pobres. Las claves deben ser protegidas de manera adecuada, y es necesaria una infraestructura de clave pública bien asegurada, También necesitan las claves o contraseñas deben ser cambiadas periódicamente para hacer que a los atacantes les resulte más difícil utilizar las claves que han obtenido sin autorización.

Hoy en día, los fraudes y explotaciones siguen teniendo éxito, y ahora los servicios en la Nube son una nueva amenaza, ya que los atacantes pueden espiar actividades, manipular transacciones y hasta modificar los datos.

Las estrategias comunes de protección y defensa pueden contener los daños sufridos por una violación. Las organizaciones deben prohibir que se compartan las credenciales de cuenta entre los usuarios y los servicios, así como permitir los esquemas de autenticación multifactoriales donde estén disponibles. Las cuentas, incluso las cuentas de servicio, deben ser controladas de manera que cada transacción se pueda remontar a una sola persona.

### **Falta de visibilidad**

Los recursos basados en la nube de una organización están ubicados fuera de la red corporativa y se ejecutan en una infraestructura que la empresa no posee. Como resultado, muchas herramientas tradicionales para lograr visibilidad de la red no son efectivas para entornos de nube y algunas organizaciones carecen de herramientas de seguridad centradas en la nube. Esto puede limitar la capacidad de una organización para monitorear sus recursos basados en la nube y protegerlos contra ataques.

### **Intercambio externo de datos**

La nube está diseñada para facilitar el intercambio de datos. Muchas nubes ofrecen la opción de invitar explícitamente a un colaborador por correo electrónico o de compartir un enlace que permite que cualquier persona con la URL acceda al recurso compartido.

Si bien este fácil intercambio de datos es una ventaja, también puede ser un problema importante de seguridad en la nube. El uso del uso compartido basado en enlaces, una opción popular ya que es más fácil que invitar explícitamente a cada colaborador previsto, dificulta el control del acceso al recurso compartido. El enlace compartido puede ser reenviado a otra persona, robado como parte de un ataque cibernético o adivinado por un ciberdelincuente, proporcionando acceso no autorizado al recurso compartido. Además, el uso compartido basado en enlaces hace que sea imposible revocar el acceso a un solo destinatario del enlace compartido.

### **Insiders maliciosos**

Las amenazas internas son un problema de seguridad importante para cualquier organización. Un interno malintencionado ya tiene acceso autorizado a la red de una organización y a algunos de los recursos confidenciales que contiene. Los intentos de obtener este nivel de acceso son lo que revela a la mayoría de los atacantes a su objetivo, lo que dificulta que una organización no preparada detecte una información privilegiada maliciosa.

En la nube, la detección de un usuario interno malintencionado es aún más difícil. Con implementaciones en la nube, las empresas carecen de control sobre su infraestructura subyacente, lo que hace que muchas soluciones de seguridad tradicionales sean menos eficaces. Esto, junto con el hecho de que se puede acceder a la infraestructura basada en la nube directamente desde la internet pública y de que a menudo dicha infraestructura presenta configuraciones incorrectas de seguridad, hace que sea aún más difícil detectar a usuarios internos malintencionados.

Las actitudes maliciosas van desde el robo de datos hasta la venganza. En un escenario de Nube, un vengador interno puede destruir infraestructuras enteras o manipular los datos. Los sistemas que dependen únicamente de la empresa de servicios en la nube para la seguridad, como el cifrado, se encuentran en mayor riesgo. Se recomienda que las organizaciones controlen el proceso de cifrado y las claves, la segregación de funciones y la reducción al mínimo del acceso a los usuarios. Son también críticos el registro eficaz, la vigilancia y la auditoría de las actividades del administrador.

### **DDOS y DOS, Ataques de denegación de servicio**

La nube es esencial para la capacidad de muchas organizaciones de hacer negocios. Utilizan la nube para almacenar datos críticos para el negocio y ejecutar importantes aplicaciones internas y de cara al cliente.

Esto significa que un ataque de denegación de servicio (DoS) exitoso contra la infraestructura de la nube probablemente tendrá un impacto importante en varias empresas diferentes. Como resultado, los ataques DoS en los que el atacante exige un rescate para detener el ataque representan una amenaza importante para los recursos basados en la nube de una organización.

Estos tipos de ataques han existido durante muchos años, sin embargo, en los últimos años ha tomado más protagonismo debido a la computación en la Nube, ya frecuentemente afecta la disponibilidad. Según un estudio: “Experimentar un ataque de denegación de servicio es como estar atrapado en el tráfico en hora punta; hay una manera de llegar a su destino y no hay nada que pueda hacer al respecto, salvo sentarse y esperar”.

### **Fuga de datos**

Los entornos basados en la nube facilitan el intercambio de datos que están almacenados en ellos. Estos entornos son accesibles directamente desde la internet pública e incluyen la capacidad de compartir datos fácilmente con otras partes a través de invitaciones directas por correo electrónico o mediante un enlace público a los datos.

La facilidad para compartir datos en la nube, si bien es un activo importante y clave para la colaboración en la nube, genera serias preocupaciones con respecto a la pérdida o fuga de datos. De hecho, el 69% de las organizaciones señalan esto como su mayor preocupación en materia de seguridad en la nube. El intercambio de datos mediante enlaces públicos o la configuración de un repositorio basado en la nube como público los hace accesibles a cualquier persona con conocimiento del enlace, y existen herramientas específicas para buscar en Internet estas implementaciones en la nube no seguras.

Esto puede venir de un error humano como de un ataque dirigido, es producido por vulnerabilidades de aplicaciones o seguridad deficiente. Por otro lado, debido a la cantidad de datos almacenados en los servidores de la Nube, los proveedores se convierten en un objetivo atractivo, por eso para no incurrir en multas o enfrentar demandas por la valoración de datos, se recomienda a las organizaciones que utilicen la autenticación de factores múltiples y la encriptación para protegerse contra las violaciones de datos.

### **Vulnerabilidad del sistema explotado**

Esta amenaza, no es algo nuevo que suceda, sin embargo, se han convertido en un problema grave debido a la capacidadmultiusuario de la Nube. Las organizaciones comparten la memoria, bases de datos y otros recursos en estrecha proximidad entre sí, creando nuevas áreas de ataque.

Pero, estos ataques pueden ser minimizados gracias a prácticas que incluyen la exploración regular de la vulnerabilidad, la gestión de parches del sistema, y un rápido seguimiento de las amenazas reportadas.

### **Amenazas Persistentes Avanzadas (APT)**

Se llaman así por sus siglas en inglés, estas amenazas se filtran en los sistemas para establecer un punto de apoyo, poco a poco se van filtrando en los datos y la propiedad intelectual durante un largo tiempo, los APTs son difíciles de detectar ya que se van moviendo lateralmente a través de la red y se mezclan con el tráfico normal. Los principales proveedores de las Nubes, están utilizando técnicas avanzadas para evitar que los APTs se filtren en las infraestructuras, por lo que los clientes tienen que ser tan diligentes en la detección de los compromisos de las APTs en las cuentas de la nube como lo harían en los sistemas de correo locales.

### **Pérdida de datos Permanente.**

El objetivo principal de los hackers maliciosos es eliminar permanentemente los datos de la nube para dañar a las empresas, y los centros de datos en la nube son tan vulnerables a los desastres naturales como cualquier instalación.

Los proveedores de nube recomiendan distribuir los datos y las aplicaciones a través de múltiples zonas para una mayor protección. Las medidas adecuadas de respaldo de datos son esenciales, así como la adhesión a las mejores prácticas en la continuidad del negocio y la recuperación de desastres. La copia de seguridad diaria y el almacenamiento fuera de las instalaciones siguen siendo importantes en los entornos de nube.

### **Tecnología compartida = peligros compartidos**

Una amenaza importante para la Nube, es el intercambio de la tecnología. Por lo general, los proveedores de servicio de la Nube comparten infraestructura, plataformas y aplicaciones, y si se presenta una vulnerabilidad en cualquiera de estas capas, podría afectar a todos los que están incluidos.

Para disminuir los riesgos de forma rentable al aplicar controles de seguridad para disminuir las probabilidades de que puedan explotarse las vulnerabilidades del bien y derivar en la implementación de amenazas.

## Medidas de seguridad para la seguridad en la nube

Cloud Security abarca las tecnologías, los controles, los procesos y las políticas que se combinan para proteger sus sistemas, datos e infraestructura basados en la nube. Es un subdominio de la seguridad informática y, más ampliamente, de la seguridad de la información.

Es una responsabilidad compartida entre usted y su proveedor de servicios en la nube. Usted implementa una estrategia de Cloud Security para proteger sus datos, cumplir con las normas y proteger privacidad de sus clientes. Lo que a su vez lo protege de las ramificaciones de reputación, financieras y legales de las violaciones y pérdidas de datos.

![Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image36.jpeg](Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image36.jpeg)

***Modelo de Responsabilidad Compartida de Cloud Security (Fuente de la imagen: Sinopsis)***

Cloud Security es un requisito crítico para todas las organizaciones. Especialmente con la última [investigación del (ISC)2](https://www.isc2.org/Resource-Center/Reports/Cloud-Security-Report) que informa que el 93% de las organizaciones están moderada o extremadamente preocupadas por Cloud Security, y una de cada cuatro organizaciones que confirman un incidente de Cloud Secutity en los últimos 12 meses.

Exploramos los riesgos de seguridad al trasladarse a la nube, comprenderá por qué es necesario Cloud Security y descubrirá las mejores prácticas de Cloud Security. También cubriremos temas como la forma de evaluar la seguridad de un proveedor de servicios en la nube e identificar las certificaciones y la formación para mejorar su Cloud Secutity.

## **¿Cómo funciona Cloud Security?**

Cloud Security es una compleja interacción de tecnologías, controles, procesos y políticas. Una práctica que está altamente personalizada a los requerimientos únicos de su organización.

Como tal, no hay una sola explicación que abarque cómo «funciona» Cloud Security

![Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image37.png](Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image37.png)

Un modelo para asegurar las cargas de trabajo de las nubes (Fuente de la imagen: HyTrust)

Afortunadamente, hay un conjunto de estrategias y herramientas ampliamente establecidas que se pueden utilizar para lograr una sólida configuración de Cloud Security, entre ellas:

### **Gestión de la identidad y el acceso**

Todas las empresas deberían tener un [sistema de gestión de la identidad y el acceso (IAM)](https://www.csoonline.com/article/2120384/what-is-iam-identity-and-access-management-explained.html) para controlar el acceso a la información. Su proveedor de nubes se integrará directamente con su IAM u ofrecerá su propio sistema incorporado. Un IAM combina la autenticación multifactorial y las políticas de acceso de los usuarios, ayudándole a controlar quién tiene acceso a sus aplicaciones y datos, a qué pueden acceder y qué pueden hacer con sus datos.

### **Seguridad física**

[La seguridad física](https://www.ibm.com/blogs/cloud-computing/2012/02/22/cloud-physical-security-considerations/) es otro pilar de la Cloud Security. Es una combinación de medidas para prevenir el acceso directo y la interrupción del hardware alojado en el centro de datos de su proveedor de nube. La seguridad física incluye el control de acceso directo con puertas de seguridad, fuentes de alimentación ininterrumpida, CCTV, alarmas, filtración de aire y partículas, protección contra incendios y más.

### **Inteligencia, vigilancia y prevención de amenazas**

[La Inteligencia de Amenazas](https://www.forcepoint.com/cyber-edu/threat-intelligence), los Sistemas [de Detección de Intrusos (IDS)](https://www.barracuda.com/glossary/intrusion-detection-system) y los [Sistemas de Prevención de Intrusos (IPS)](https://www.forcepoint.com/cyber-edu/intrusion-prevention-system-ips) forman la columna vertebral de Cloud Security. La Inteligencia de Amenazas y las herramientas de IDS ofrecen funcionalidad para identificar a los atacantes que actualmente tienen como objetivo sus sistemas o que serán una amenaza futura. Las herramientas de IPS implementan funcionalidad para mitigar un ataque y avisarle de su ocurrencia para que usted también pueda responder.

### **Cifrado**

Usando la tecnología de la nube, usted está enviando datos hacia y desde la plataforma del proveedor de la nube, a menudo almacenándolos dentro de su infraestructura. [El cifrado](https://searchsecurity.techtarget.com/definition/encryption) es otra capa de Cloud Security para proteger sus activos de datos, codificándolos cuando están en reposo y en tránsito. Esto asegura que los datos sean casi imposibles de descifrar sin una clave de descifrado a la que sólo usted tiene acceso.

### **Pruebas de vulnerabilidad y penetración de las nubes**

Otra práctica para mantener y mejorar la Cloud Security es la [prueba de vulnerabilidad y penetración](https://www.hitachi-systems-security.com/blog/penetration-testing-vs-vulnerability-assessment/). Estas prácticas implican que usted – o su proveedor – ataque su propia infraestructura de nube para identificar cualquier debilidad o explotación potencial. A continuación, puede implementar soluciones para parchear estas vulnerabilidades y mejorar su posición de seguridad.

### **Microsegmentación**

[La microsegmentación](https://www.networkworld.com/article/3247672/what-is-microsegmentation-how-getting-granular-improves-network-security.html) es cada vez más común en la implementación de Cloud Security. Es la práctica de dividir el despliegue de la nube en distintos segmentos de seguridad, hasta el nivel de la carga de trabajo individual. Al aislar las cargas de trabajo individuales, se pueden aplicar políticas de seguridad flexibles para minimizar los daños que un atacante podría causar, en caso de que obtuviera acceso.

### **La próxima generación de cortafuegos**

[Los cortafuegos de última generación](https://digitalguardian.com/blog/what-next-generation-firewall-learn-about-differences-between-ngfw-and-traditional-firewalls) son otra pieza del rompecabezas de Cloud Security. Protegen sus cargas de trabajo usando la funcionalidad de los cortafuegos tradicionales y las nuevas características avanzadas. La protección de los cortafuegos tradicionales incluye filtrado de paquetes, inspección de estado, proxy, bloqueo de IP, bloqueo de nombres de dominio y bloqueo de puertos.

<aside>
👉 Los cortafuegos de última generación añaden un sistema de prevención de intrusiones, inspección profunda de paquetes, control de aplicaciones y análisis del tráfico cifrado para proporcionar una detección y prevención integral de amenazas.

</aside>

![Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image38.png](Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image38.png)

Arquitectura de alojamiento (fuente: Kinsta)

En este ejemplo, en Kinsta aseguran todos los sitios web detrás del [Firewall de Google Cloud Platform (GCP)](https://kinsta.com/es/changelog/optimizaciones-automaticas-de-bases-de-datos-mysql-auto-recuperacion-php-firewall-gcp/#now-secured-behind-google-cloud-platform-firewall). Ofreciendo una protección de última generación y la capacidad de integrarse más estrechamente con otras soluciones de seguridad de GCP.

## **7 Riesgos de seguridad de la computación en nube**

Ya sea que esté o no operando en la nube, la seguridad es una preocupación para todos los negocios. Se enfrentará a riesgos como la denegación de servicio, el malware, la inyección SQL, las brechas de datos y la pérdida de datos. Todo ello puede tener un impacto significativo en la reputación y los resultados de su empresa.

Cuando se mueve a la nube introduce un nuevo conjunto de riesgos y cambia la naturaleza de los demás. Eso no significa que la computación en la nube no sea segura. De hecho, muchos proveedores de nubes introducen el acceso a herramientas y recursos de seguridad altamente sofisticados a los que de otra manera no podrías acceder. Simplemente significa que hay que ser consciente del cambio en los riesgos para mitigarlos. Así que, echemos un vistazo a los riesgos de seguridad únicos de la computación en nube.

**1. Pérdida de visibilidad**

La mayoría de las empresas accederán a una gama de servicios de nube a través de múltiples dispositivos, departamentos y geografías. Este tipo de complejidad en una configuración de computación en nube – sin las herramientas apropiadas en su lugar – puede causar que pierda la visibilidad del acceso a su infraestructura. Sin los procesos correctos en su lugar, puede perder de vista quién está usando sus servicios en la nube. Incluyendo qué datos están accediendo, subiendo y bajando. Si no puede verlo, no puede protegerlo. Aumentando el riesgo de violación y pérdida de datos.

**2. Violaciones del cumplimiento**

Con el aumento del control reglamentario, es probable que tenga que cumplir una serie de requisitos de cumplimiento muy estrictos. Al pasar a la nube, se introduce el riesgo de violaciones de cumplimiento si no se tiene cuidado. Muchos de estos reglamentos exigen que su empresa sepa dónde están sus datos, quién tiene acceso a ellos, cómo se procesan y cómo se protegen. Otras regulaciones requieren que su proveedor de nube tenga ciertas credenciales de cumplimiento. Una transferencia descuidada de datos a la nube, o el traslado al proveedor equivocado, puede poner a su organización en un estado de incumplimiento. Introduciendo repercusiones legales y financieras potencialmente graves.

**3. Falta de estrategia y arquitectura de Cloud Security**

Este es un riesgo de Cloud Security que puede ser fácilmente evitado, pero muchos no lo hacen. En su prisa por migrar los sistemas y datos a la nube, muchas organizaciones empiezan a funcionar mucho antes de que los sistemas y estrategias de seguridad estén en funcionamiento para proteger su infraestructura. Asegúrese de implementar una estrategia de seguridad e infraestructura diseñada para que la nube funcione en línea con sus sistemas y datos.

**4. Amenazas internas**

Sus empleados de confianza, contratistas y socios comerciales pueden ser algunos de sus mayores riesgos de seguridad. Estas amenazas internas no tienen por qué tener un propósito malicioso para causar daños a su negocio. De hecho, la mayoría de los incidentes internos se deben a la falta de formación o a la negligencia.

Mientras que actualmente se enfrenta a este problema, el traslado a la nube cambia el riesgo. Usted entrega el control de sus datos a su proveedor de servicios en la nube e introduce una nueva capa de amenaza interna de los empleados del proveedor.

**5. Incumplimientos contractuales**

Cualquier sociedad contractual que tenga incluirá restricciones sobre cómo se utilizan los datos compartidos, cómo se almacenan y quién está autorizado a acceder a ellos. Sus empleados, al trasladar involuntariamente datos restringidos a un servicio en la nube sin autorización, podrían crear un incumplimiento de contrato que podría dar lugar a acciones legales.

Asegúrese de leer los términos y condiciones de sus proveedores de nubes. Incluso si tiene autorización para mover datos a la nube, algunos proveedores de servicios incluyen el derecho de compartir cualquier dato cargado en su infraestructura. Por ignorancia, usted podría involuntariamente violar un acuerdo de no divulgación.

**6. Interfaz de usuario de aplicaciones inseguras (API)**

Cuando se operan sistemas en una infraestructura de nube, se puede utilizar una API para implementar el control. Cualquier API incorporada a sus aplicaciones web o móviles puede ofrecer acceso interno por parte del personal o externo por parte de los consumidores.

Son las API de cara al exterior las que pueden introducir un riesgo de Cloud Security Cualquier API externa insegura es una puerta de entrada que ofrece acceso no autorizado a los ciberdelincuentes que buscan robar datos y manipular servicios.

El ejemplo más destacado de una API externa insegura es el [escándalo de Facebook – Cambridge Analytica](https://www.nytimes.com/2018/04/04/us/politics/cambridge-analytica-scandal-fallout.html). La API externa insegura de Facebook le dio a Cambridge Analytica un acceso profundo a los datos de los usuarios de Facebook.

**7. Desconfiguración de los servicios de la nube**

La configuración errónea de los servicios de la nube es otro posible riesgo para Cloud Security. Con el aumento de la gama y la complejidad de los servicios, este es un problema creciente. La configuración errónea de los servicios en la nube puede hacer que los datos se expongan públicamente, se manipulen o incluso se eliminen.

Entre las causas más comunes se encuentran el mantenimiento de la seguridad predeterminada y la configuración de la gestión del acceso a datos altamente confidenciales. Otras incluyen una gestión de acceso mal ajustada que da acceso a personas no autorizadas, y el acceso a datos manipulados en los que los datos confidenciales se dejan abiertos sin necesidad de autorización.

## **¿Por qué se requiere Cloud Security?**

La adopción masiva de la tecnología de nubes combinada con un volumen y una sofisticación cada vez mayores de las amenazas cibernéticas es lo que impulsa la necesidad de Cloud Security. Reflexionando sobre los riesgos de seguridad de la adopción de la tecnología de nubes – esbozados anteriormente – el fracaso en la mitigación de los mismos puede tener implicaciones significativas.

### **Beneficios de la Cloud Security**

Más allá de la protección contra las amenazas y de evitar las consecuencias de las malas prácticas, cloud security ofrece beneficios que la convierten en un requisito para las empresas. Entre ellos se incluyen:

**1. Seguridad centralizada**

De la misma manera que la computación en la nube centraliza las aplicaciones y los datos, cloud security centraliza la protección. Ayudándole a mejorar la visibilidad, implementar controles y protegerse mejor contra los ataques. También mejora la continuidad de su negocio y la recuperación de desastres al tenerlo todo en un solo lugar.

**2. Costo reducido**

Un reputado proveedor de servicios de nube ofrecerá hardware y software incorporado dedicado a asegurar sus aplicaciones y datos las 24 horas del día. Esto elimina la necesidad de una inversión financiera significativa en su propia configuración.

**3. Administración reducida**

El paso a la nube introduce un modelo de responsabilidad compartida para la seguridad. Esto puede proporcionar una reducción significativa de la cantidad de tiempo y recursos invertidos en la administración de la seguridad. El proveedor de servicios de la nube asumirá la responsabilidad de asegurar su infraestructura – y a usted – a través del almacenamiento, la computación, las redes y la infraestructura física.

**4. Aumento de la fiabilidad**

Un proveedor líder de servicios de nube ofrecerá hardware y software de Cloud Security de última generación en el que se puede confiar. Tendrá acceso a un servicio continuo en el que sus usuarios podrán acceder de forma segura a los datos y aplicaciones desde cualquier lugar y en cualquier dispositivo.

## **Mejores prácticas para Cloud Security**

Al mover sus sistemas a la nube, muchos procesos de seguridad y mejores prácticas siguen siendo los mismos. Sin embargo, se encontrará con un nuevo conjunto de desafíos que deberá superar para mantener la seguridad de sus sistemas y datos basados en la nube.

Para ayudarle con este desafío, hemos compilado una serie de mejores prácticas de seguridad para despliegues basados en la nube.

- **Elije un proveedor de confianza**

La base de las mejores prácticas de cloud security se basa en la selección de un proveedor de servicios de confianza. Usted desea asociarse con un proveedor de nubes que ofrezca los mejores protocolos de seguridad incorporados y que se ajuste a los niveles más altos de las mejores prácticas de la industria. Un proveedor de servicios que le extiende un mercado de socios y soluciones para mejorar aún más la seguridad de su despliegue.

La marca de un proveedor de confianza se refleja en el rango de cumplimiento de la seguridad y las certificaciones que poseen. Algo que cualquier buen proveedor pondrá a disposición del público. Por ejemplo, todos los proveedores líderes como [Amazon Web Services](https://aws.amazon.com/compliance/programs/), [Alibaba Cloud](https://www.alibabacloud.com/trust-center), [Google Cloud](https://cloud.google.com/security/compliance/) (que impulsa a Kinsta) y [Azure](https://azure.microsoft.com/en-gb/overview/trusted-cloud/compliance/) ofrecen un acceso transparente en el que se puede confirmar su cumplimiento de seguridad y sus certificaciones.

- **Comprender su modelo de responsabilidad compartida**

Cuando se asocia con un proveedor de servicios en la nube y se trasladan los sistemas y datos a la nube, se entra en una asociación de responsabilidad compartida para la implementación de la seguridad. Una parte crítica de las mejores prácticas implica revisar y comprender su responsabilidad compartida. Descubrir qué tareas de seguridad permanecerán con usted y cuáles serán ahora manejadas por el proveedor. Esta es una escala móvil dependiendo de si se opta por el Software como Servicio (SaaS), Plataforma como Servicio (PaaS), Infraestructura como Servicio (IaaS), o en un centro de datos en las instalaciones.