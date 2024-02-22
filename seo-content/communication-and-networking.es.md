---
title: "Redes y comunicaciones"
subtitle: "Explora los fundamentos de las redes informáticas, desde diferentes tipos hasta protocolos clave y dispositivos esenciales. ¡Obtén más información sobre direcciones IP, enrutadores y conmutadores!"
tags: ["networking", "ciberseguridad"]
authors: ["blindma1den", "lorenagubaira"]

---

Podemos definir a la red como la tecnología que permite que las computadoras se conecten entre sí, para poder compartir y enviar datos entre ellas, en la actualidad no solo podemos conectar computadoras, podemos conectar en la red cualquier dispositivo inteligente desde teléfonos hasta televisores.

Existen varios tipos de redes tales como:

| Red de área local (Local Área Network ò Lan) | Una red LAN o “Local área Network”, es una red de comunicaciones construida mediante la interconexión de nodos mediante cables o medios inalámbricos. El ámbito de conexión está limitado por medios físicos, ya sea un edificio, planta o nuestra propia habitación. En ellas, la principal característica es que existen una serie de recursos compartidos accesibles solamente por los usuarios que pertenecen a ella, sin posibilidad de acceso externo. |
| --- | --- |
| Red de área Metropolitana (Metropolitan area network o MAN) | Una red LAN o “Local área Network”, es una red de comunicaciones construida mediante la interconexión de nodos mediante cables o medios inalámbricos. El ámbito de conexión está limitado por medios físicos, ya sea un edificio, planta o nuestra propia habitación. En ellas, la principal característica es que existen una serie de recursos compartidos accesibles solamente por los usuarios que pertenecen a ella, sin posibilidad de acceso externo. |
| Red de area extensa (Wide area network o WAN) | No tiene límite predefinido, sino que es la red que permite conectar distintos puntos del mundo compuestos por áreas LAN o MAN, a través de enlaces troncales de alta capacidad. Por ejemplo. Internet es una red WAN. |
| WLAN (Red de área local inalámbrica) | En esta red nos podemos ingresar sin necesitar de estar físicamente conectados a ella, gracias a un dispositivo llamado router que emite la señal de la red a través de ondas que recibirán los dispositivos a través de una tarjeta de red el cual capta esta señal y hace la conexión. |

Gracias a estas redes podemos enviar información de un lugar a otro, mediante protocolos de red los cuales nos dictaran las normas y reglas de cómo los dispositivos intercambiaran información.

**Los protocolos de red más utilizados son:**

- **TCP/IP (Transmission Control protocol/ internet protocol)**

Este protocolo es un conjunto de reglas estandarizadas que permiten a los equipos comunicarse en una red como Internet y cómo se envían y reciben los paquetes informativos, esta explicación es conocida como el modelo *TCP/IP*.

El modelo TCP/IP es usado para comunicaciones en redes y, como todo protocolo, describe un conjunto de guías generales de operación para permitir que un equipo pueda comunicarse en una red. TCP/IP provee conectividad de extremo a extremo especificando cómo los datos deberían ser formateados, direccionados, transmitidos, enrutados y recibidos por el destinatario.

Para conseguir un intercambio fiable de datos entre dos equipos, se deben llevar a cabo muchos procedimientos separados. El resultado es que el software de comunicaciones es complejo. Con un modelo en capas o niveles resulta más sencillo agrupar funciones relacionadas e implementar el software modular de comunicaciones.

Las capas están jerarquizadas, es decir, cada capa se construye sobre su predecesora. El número de capas y, en cada una de ellas, sus servicios y funciones son variables con cada tipo de red. Sin embargo, en cualquier red, la misión de cada capa es proveer servicios a las capas superiores haciéndoles transparentes el modo en que esos servicios se llevan a cabo. De esta manera, cada capa debe ocuparse exclusivamente de su nivel inmediatamente inferior, a quien solicita servicios, y del nivel inmediatamente superior, a quien devuelve resultados.

**El modelo TCP/IP consta de 4 capas:**

1. **Capa de acceso**: La capa de acceso a la red, también conocida como la capa de enlace a los datos, gestiona la infraestructura física que permite a los ordenadores comunicarse entre sí por Internet. Esto abarca, entre otros elementos, cables Ethernet, redes inalámbricas, tarjetas de interfaz de red y controladores de dispositivos en el ordenador. 
La capa de acceso a la red también incluye la infraestructura técnica, como el código que convierte datos digitales en señales transmisibles, que hacen posible una conexión.
2. **Capa de internet:** La capa de Internet, también llamada la capa de red, controla el flujo y el enrutamiento de tráfico para garantizar que los datos se envían de forma rápida y correcta. Esta capa también es responsable de volver a juntar el paquete de datos en el destino. Si hay mucho tráfico en Internet, esta capa puede tardar un poco más en enviar un archivo, pero es menos probable que el archivo se dañe.
3. **Capa de transporte:** La capa de transporte es la que proporciona una conexión de datos fiable entre dos dispositivos de comunicación. Es como enviar un paquete asegurado: la capa de transporte divide los datos en paquetes, confirma los paquetes que ha recibido del remitente y se asegura de que el destinatario confirme los paquetes recibidos por su parte.
4. **Capa de aplicación:** La capa de aplicaciones es el grupo de aplicaciones que permite al usuario acceder a la red. Para la mayoría de nosotros, esto significa el correo electrónico, las aplicaciones de mensajería y los programas de almacenamiento en la nube. Esto es lo que el usuario final ve y con lo que interactúa al recibir y enviar datos.

> 🏋️ **Ejercicio:** Existe un modelo de red llamado OSI el cual explica todo el proceso de envio de informacion por la red mucho mas detalla, es un modelo de estudio el cual consta de 7 capas. - Investiga sobre ese modelo y cada una de sus capas para asi tener una mejor comprension. 

- **DNS (Domain system name)**

Este protocolo se encarga de la resolución de nombres de las páginas web con respecto a sus direcciones numéricas de IP, es decir traducir nombres fáciles de comprender para las personas en identificadores IP con los equipos conectados a la red, esto con el propósito de poder localizar y direccionar estos equipos mundialmente.

El servidor DNS utiliza una base de datos distribuida y jerárquica que almacena información asociada a nombres de dominio en redes como Internet. Aunque como base de datos el DNS es capaz de asociar diferentes tipos de información a cada nombre, los usos más comunes son la asignación de nombres de dominio a direcciones IP y la localización de los servidores de correo electrónico de cada dominio.

La asignación de nombres a direcciones IP es ciertamente la función más conocida de los protocolos DNS. Por ejemplo, si la dirección IP del sitio Google es 216.58.210.163, la mayoría de la gente llega a este equipo especificando [www.google.com](http://www.google.com/) y no la dirección IP. Además de ser más fácil de recordar, el nombre es más fiable. La dirección numérica podría cambiar por muchas razones, sin que tenga que cambiar el nombre del sitio web. Incluso, en el caso de que una página web utilice una red de distribución de contenidos (Content delivery network o CDN, por sus siglas en inglés) por medio del DNS el usuario recibirá la dirección IP del servidor más cercano según su localización geográfica (cada CDN a su vez tiene sus propios servidores DNS).

- **DCPH (Dynamic Host Configuration Protocol)**

Es un protocolo de red  mediante el cual un servidor **DHCP** asigna dinámicamente una dirección IP y otros parámetros de configuración de red a cada dispositivo en una red para que puedan comunicarse con otras redes IP. Este servidor posee una lista de direcciones IP dinámicas y las va asignando a los clientes conforme éstas van quedando libres, sabiendo en todo momento quién ha estado en posesión de esa IP, cuánto tiempo la ha tenido y a quién se la ha asignado después. Así los clientes de una red IP pueden conseguir sus parámetros de configuración automáticamente.

Cada dirección IP debe configurarse manualmente en cada dispositivo y, si el dispositivo se mueve a otra subred, se debe configurar otra dirección IP diferente. El DHCP le permite al administrador supervisar y distribuir de forma centralizada las direcciones IP necesarias y, automáticamente, asignar y enviar una nueva IP si fuera el caso en que el dispositivo esté conectado en un lugar diferente de la red.

- **Dirección IP**

Una dirección IP tiene dos funciones principales: identificación de la interfaz de red y direccionamiento para su ubicación.

La dirección IP puede cambiar a menudo debido a cambios en la red, o porque el dispositivo encargado dentro de la red de asignar las direcciones IP, decida asignar otra IP (por ejemplo, con el protocolo DHCP). A esta forma de asignación de dirección IP se le denomina también dirección IP dinámica (normalmente abreviado como IP dinámica). Los sitios de Internet que por su naturaleza necesitan estar permanentemente conectados, generalmente tienen la necesidad de una dirección IP fija (comúnmente, IP fija o IP estática). Esta no cambia con el tiempo. Los servidores de correo, DNS, FTP públicos y servidores de páginas web necesariamente deben contar con una dirección IP fija o estática, ya que de esta forma se permite su localización en la red.

Los dispositivos se conectan entre sí mediante sus respectivas direcciones IP. Sin embargo, para las personas es más fácil recordar un nombre de dominio que los números de la dirección IP. Los servidores de nombres de dominio DNS, "traducen" el nombre de dominio en una dirección IP. Si la dirección IP dinámica cambia, es suficiente actualizar la información en el servidor DNS. El resto de las personas seguirán accediendo al dispositivo por el nombre de dominio.

Las direcciones IPV4 se expresan mediante un número binario de 32 bits permitiendo un espacio de direcciones de hasta 4.294.967.296 (2^32) direcciones posibles.

Las direcciones IP se pueden expresar como números de notación decimal: se dividen los 32 bits de la dirección en cuatro octetos. El valor decimal de cada octeto está comprendido en el intervalo de 0 a 255 [el número binario de 8 bits más alto es 11111111 y esos bits, de derecha a izquierda, tienen valores decimales de 1, 2, 4, 8, 16, 32, 64 y 128, lo que suma 255].

### Dispositivos de red

Un **enrutador** es un dispositivo que conecta dos o más redes o subredes de conmutación de paquetes. Cumple dos funciones principales: gestionar el tráfico entre estas redes mediante el reenvío de paquetes de datos a sus direcciones IP previstas, y permite que varios dispositivos utilizan la misma conexión a Internet.

Hay varios tipos de routers, pero la mayoría de ellos pasan datos entre las **LAN** (redes de área local) y las **WAN** (redes de área amplia). Una LAN es un grupo de dispositivos conectados restringidos a una zona geográfica concreta. Una LAN suele necesitar un solo router.

Los datos se mueven a lo largo de cualquier red en forma de paquetes de datos. Cada paquete de datos tiene un encabezado que contiene información sobre el destino previsto del paquete. Cuando un paquete viaja a su destino, varios enrutadores pueden dirigirlo varias veces. Los enrutadores realizan este proceso millones de veces por segundo con millones de paquetes.

Cuando llega un paquete de datos, el enrutador primero busca su dirección en una tabla de enrutamiento. Luego, el enrutador reenvía o mueve el paquete hacia el siguiente punto de la red.

Existen dos tipos diferentes de enrutamiento, que se basan en la forma en que el enrutador crea sus tablas de enrutamiento:

- **Enrutamiento estático**

En el enrutamiento estático, un administrador de red utiliza tablas estáticas para configurar y seleccionar manualmente las rutas de red. El enrutamiento estático es útil en situaciones en las que se espera que el diseño o los parámetros de la red permanezcan constantes.

La naturaleza estática de esta técnica de enrutamiento conlleva los inconvenientes esperados, como la congestión de la red. Si bien los administradores pueden configurar rutas de respaldo en caso de que se produzca un error en un enlace, el enrutamiento estático generalmente disminuye la adaptabilidad y la flexibilidad de las redes, lo que resulta en un rendimiento limitado de la red.

- **Enrutamiento dinámico**

En el enrutamiento dinámico, los enrutadores crean y actualizan las tablas de enrutamiento en tiempo de ejecución según las condiciones reales de la red. Intentan encontrar la ruta más rápida desde el origen hasta el destino mediante un protocolo de enrutamiento dinámico, que es un conjunto de reglas que crean, mantienen y actualizan la tabla de enrutamiento dinámico.

La mayor ventaja del enrutamiento dinámico es que se adapta a las condiciones cambiantes de la red, incluidos el volumen de tráfico, el ancho de banda y las fallas de la red.

Otro dispositivo que puede realizar el enrutamiento son los **switches**. Los switches son bloques de construcción clave para cualquier red. Conectan múltiples dispositivos, como computadoras, puntos de acceso inalámbrico , impresoras y servidores; en la misma red dentro de un edificio o campus. Un interruptor permite que los dispositivos conectados compartan información y se comuniquen entre sí.

**Existen varios tipos de switches:**

**a)** **Conmutadores no administrados**: Un conmutador de red no administrado está diseñado para que simplemente pueda enchufar y funcionar, sin necesidad de configuración. Los conmutadores no administrados suelen ser para conectividad básica. A menudo son utilizados en redes domésticas o donde se necesiten algunos puertos más, como en un escritorio, en un laboratorio o en una sala de conferencias.

**b)** **Conmutadores gestionados**: Los conmutadores administrados le brindan mayor seguridad y más funciones y flexibilidad porque puede configurarlos para que se ajusten a su red. Con este mayor control, puede proteger mejor su red y mejorar la calidad del servicio para quienes acceden a la red.
