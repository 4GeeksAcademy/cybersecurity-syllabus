## Intrusion prevention systems (IPS)

Los IPS son dispositivos de hardware o software encargados de revisar el tráfico de red con el propósito de detectar y responder a posibles ataques o intrusiones. La respuesta consiste en descartar o modificar los paquetes procedentes del ataque de tal manera que se anule su propósito. Este comportamiento los clasifica como dispositivos proactivos debido a su reacción automática a situaciones anómalas.

Los IPS se asemejan el comportamiento de los cortafuegos, ambos toman decisiones sobre la aceptación de paquetes en un sistema. Sin embargo, los cortafuegos basan sus decisiones en los encabezados de paquetes entrantes, capas de red y de transporte, mientras que los IPS basan sus decisiones tanto en los encabezados como en el contenido de datos del paquete.

![intrucion prevension system](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/7intrucion-prevension-system.png?raw=true)

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

![ventajas intrusion prevesion system](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/8ventajas-intrusion-prevesion-system.png?raw=true)

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
