---
title: Seguridad básica de redes
tags:
  - redes
  - ciberseguridad
authors:
  - blindma1den
  - lorenagubaira
description: >-
  Aprende los fundamentos de la seguridad de redes. Descubre cómo los firewalls
  protegen contra accesos no autorizados y ataques DDoS, y conoce los
  protocolos de cifrado WiFi (WEP, WPA, WPA2, WPA3).
---
## Que es un Firewall

Un firewall es un sistema de seguridad en la red, el cual restringe el tráfico de internet entrante, saliente o dentro de una red privada, el término proviene del concepto de paredes físicas que actúan como barreras para ralentizar la propagación del fuego hasta que los servicios de emergencia puedan extinguir.

Los firewalls pueden ser un software o una unidad de hardware y software dedicado que funciona bloqueando o permitiendo el acceso a los paquetes de datos de forma selectiva.

Una explicación más simple es considerarlo como fronteras o puertas que se van a delimitar en una red privada o los dispositivos host para administrar el flujo de la actividad que se permite o se prohíbe en dicha red, podemos decir que están destinados a ralentizar la propagación de las amenazas en la red.

Estas barreras por lo general se encuentran en dos ubicaciones: En dispositivos específicos dentro de la red y en otros puntos de conexión (hosts).

## La función de los Firewall en las redes

El firewall o cortafuego es una herramienta esencial en la seguridad de redes ya que su función principal es proteger toda la red informática al controlar el tráfico de datos que entra y sale de ella, Actúa como especie de barrera entre la red interna y el mundo exterior, filtrando y bloqueando el acceso no autorizado y potencialmente peligroso, Una de sus funciones más importantes es la prevención de intrusiones, es decir, detecta y bloquea intentos de acceso no autorizado a la red ya sea desde el exterior o desde dispositivos internos comprometidos, y lo más importante es que un firewall puede evitar ataques de denegación de servicio (DDoS) al limitar el tráfico que puede ingresar a la red.

## ¿Cómo funcionan los firewall?

El firewall decide que tráfico de red se admite o se considera peligroso, básicamente separa el tráfico bueno del malo, o el seguro del no fiable. Su objetivo principal es proteger las redes privadas y los dispositivos de punto de conexión que se encuentran en ellas, conocidos como hosts de red. Estos hosts se comunican con otros hosts en la red, envían y reciben tráfico entre las redes internas y también pueden recibir tráfico de redes externas.

Las computadoras y otros dispositivos de punto de conexión utilizan redes para acceder a Internet y comunicarse entre ellos. Sin embargo, el mismo internet está segmentado en subredes por motivos de seguridad y privacidad

En un firewall el filtrado del tráfico se logra mediante reglas preestablecidas o aprendidas dinámicamente para permitir y denegar los intentos de conexión. Estas reglas determinan cómo el firewall regula el flujo de tráfico web a través de la red privada y los dispositivos informáticos privados. Independientemente del tipo, todos los firewalls pueden realizar el filtrado mediante una combinación de lo siguiente:

- **Origen**: lugar desde donde se intenta establecer la conexión.
- **Destino:** lugar al que se intenta dirigir la conexión.
- **Contenido**: información que la conexión está intentando enviar.

**Protocolos del paquete**: el “lenguaje” que se utiliza para transmitir el mensaje al intentar establecer la conexión. Entre los protocolos de red que los hosts utilizan para “comunicarse” entre sí, los protocolos TCP/IP se usan principalmente para comunicarse por Internet y entre intranets o subredes.

**Protocolos de aplicaciones:** los protocolos comunes incluyen HTTP, Telnet, FTP, DNS y SSH.

## Tipos de firewall

Los tipos de firewall incluyen varios métodos de filtrado y se distinguen según su método en relación a lo siguiente.

- Seguimiento de la conexión.
- Reglas de filtrado.
- Registro de auditoría.

Por lo general los firewall más comunes en el mercado son:

### Firewall de filtrado de paquetes

Su función es filtrar los paquetes con base en direcciones de red, protocolos o puertos. Las reglas para el filtrado se establecen según una lista de control de acceso creada manualmente. Estas reglas son muy rígidas y es difícil abordar correctamente el tráfico no deseado, sin poner en riesgo la usabilidad de la red.

La incapacidad de leer protocolos de aplicación significa que no pueden leerse los contenidos de un mensaje enviado dentro de un paquete. Sin leer el contenido, los firewalls con filtrado de paquete tienen una calidad de protección limitada.

### Firewall de puerta de enlace

Estos firewalls comprueban si hay paquetes funcionales en el intento de conexión y, si funciona correctamente, permiten establecer una conexión abierta persistente entre las dos redes. Después de esto, el firewall deja de supervisar la conexión.

Aparte de su estrategia en cuanto a las conexiones, la puerta de enlace de nivel de circuito puede ser similar a los firewalls proxy.

### Firewall de inspección con estado

Los firewalls de inspección con estado, también llamados firewalls de filtrado dinámico de paquetes, son únicos en comparación al filtrado estático debido a su capacidad para supervisar conexiones en curso y recordar las anteriores. Comenzaron actuando en la capa de transporte , pero en la actualidad, estos firewalls pueden supervisar muchas capas, incluida la capa de aplicación.

Del mismo modo que el firewall de filtrado estático, los firewalls de inspección con estado permiten o bloquean el tráfico en función de las propiedades técnicas, como los protocolos de paquete específicos, las direcciones IP o los puertos

### Firewall de última generación (NGFW)

La constante evolución de las amenazas implica contar con soluciones más sólidas. Los firewalls de última generación superan este problema porque combinan las funciones de un firewall tradicional con sistemas de prevención de intrusiones en la red.

Los firewalls de última generación están diseñados para examinar e identificar amenazas específicas, como malware avanzado, en un nivel más detallado. Este es el tipo de firewall más utilizado por empresas y redes sofisticadas, ya que proporciona una solución integral para filtrar y descartar cualquier amenaza.

## Seguridad en redes wifi

Una red inalámbrica o una red wifi es una señal de frecuencia por ondas, que puede conectar a los equipos en internet sin necesidad de usar cables, como esta conexión es por transmisión en vez de cables, es posible que usuarios no autorizados puedan acceder a esta red. Esto puede reducir la velocidad de la conexión o generar vulnerabilidad en situaciones como robo de identidad. Por lo que es necesario tomar ciertas medidas de seguridad para proteger nuestra información en WiFi tales como:

### Encriptación

La encriptación de las redes inalámbricas se utilizan para añadir seguridad mediante un protocolo de autenticación, el cual solicita una contraseña o una clave de red cuando un usuario o dispositivo intenta conectarse. Si la red Wifi no está asegurada con algún tipo de cifrado, es posible que algún usuario no autorizado pueda acceder a ella y obtener información personal, además de reducir la velocidad y el rendimiento de la red.

> 💡 Existen diferentes tipos de cifrados para redes LAN inalámbricas (WIFI)

- **Wired Encryption Protocol (WEP)**

Este protocolo utiliza una clave secreta compartida entre un punto de acceso y un host, y todos los datos enviados y recibidos pueden ser cifrados utilizando esta clave compartida.

El estándar 802.11 no especifica cómo se establece la clave privada, pero permite que haya una tabla que asocia una clave exclusiva con cada estación. Sin embargo, en práctica general, una misma clave es compartida entre todas las estaciones y puntos de acceso.

**WEP proporciona dos tipos de autenticación:**

1. Un sistema abierto, en el que todos los usuarios tienen permiso para acceder a la WLAN.
2. Una autenticación mediante clave compartida, que controla el acceso a la WLAN y evita accesos no autorizados a la red.

> 👉 De los dos niveles, la autenticación mediante clave compartida es el modo seguro, en el que se utiliza una clave privada compartida entre todas las estaciones y puntos de acceso al sistema WLAN.

Para proteger el texto cifrado frente a modificaciones no autorizadas mientras está en tránsito, WEP aplica un algoritmo de comprobación de integridad (CRC-32) al texto en claro.

La autenticación mediante clave compartida funciona sólo si está habilitado el cifrado WEP, de no estarlo, el sistema revertirá de manera predeterminada al modo de sistema abierto

Según el estándar, WEP debe proporcionar confidencialidad, autenticación y control de acceso en redes WLAN.

WEP utiliza una misma clave simétrica y estática en las estaciones y el punto de acceso. El estándar no contempla ningún mecanismo de distribución automática de claves, lo que obliga a escribir la clave manualmente en cada uno de los elementos de red.

Esto genera varios inconvenientes, por un lado la clave está almacenada en todas las estaciones, aumentando las posibilidades de que sea comprometida.

Por otro lado, la distribución manual de claves provoca un aumento de mantenimiento por parte del administrador de red, lo que conlleva, en la mayoría de las ocasiones, que la clave se cambie poco o nunca

### WiFi Protected Access (WPA)

Este sistema de cifrado surgió para solucionar los problemas de seguridad que ofrecía el sistema WEP.Para ello hace uso del TKIP (Temporal Key Integrity Protocol). Este protocolo sirve para gestionar claves dinámicas por lo que resuelve muchos de los problemas que tenía el WEP como la longitud de la clave.

En líneas generales, podemos decir que la WPA funciona similar a WEP, pero usando las claves dinámicas, además utiliza el algoritmo RC4 para generar un flujo de bits que se usan para cifrar.

WPA adopta la autenticación de usuarios mediante el uso de un servidor, donde se almacenan las credenciales y contraseñas de los usuarios en la red. y para no obligar al uso de tal servidor para el despliegue de redes, WPA permite la autenticación mediante una clave precompartida.

De un modo similar al WEP, requiere introducir la misma clave en todos los equipos de la red, por tanto, con WPA al estar la clave cambiando constantemente, las incursiones en la red inalámbrica es más difícil que con WEP.

PSK o Pre Shared Key (clave compartida previamente), se basa en la seguridad de una contraseña compartida formada entre 8 y 63 caracteres. Es un sistema fácil de utilizar y configurar, por lo que es recomendable en entornos familiares o pequeñas empresas. Cualquier equipo que tenga la clave podrá conectarse a la red.

La principal debilidad que presenta WPA-PSK es precisamente el uso de clave compartida entre estaciones ya que cuando un sistema basa su seguridad en una contraseña, siempre es susceptible de sufrir un ataque de fuerza bruta, aunque si la longitud de la contraseña es adecuada y además está bien elegida no debería suponer mayor problema.

### WiFi Protected Access 2 (WPA2)

WPA2 es un protocolo de cifrado WiFi que surge con la finalidad de solucionar los problemas de vulnerabilidad detectados en la primera versión (WAP).

Las especificaciones de WPA2, no son públicas por lo que la cantidad de información disponible es realmente escasa. Se sabe que WPA2 incluye el algoritmo de cifrado AES (Advanced Encryption Standard), desarrollado por el NIS.

Como ya se ha comentado, se trata de un algoritmo de cifrado WiFi de bloque con clave de 128 bits.

Es necesario un hardware potente para realizar los algoritmos de WPA2, lo que significa que dispositivos antiguos sin suficientes capacidades de procesamiento no podrán incorporar WPA2.

El modo personal o Pre-Shared Key (PSK) funciona igual que en la seguridad WAP, y es el protocolo de cifrado WiFi más fácil de instalar ya que requiere que se cree una contraseña simple. Aunque WPA2 proporciona una fuerte encriptación y seguridad, y es “potencialmente indescifrable” por los atacantes si se utiliza una contraseña larga y fuerte.

### Filtrado MAC

La misión del filtrado MAC es restringir el acceso a la red a un dispositivo en concreto o un grupo de equipos. Pongamos por ejemplo que tenemos un ordenador y no queremos que se conecte a la red doméstica. Tendríamos que saber cuál es su dirección MAC y crear un filtro en el router.

Podríamos crear un filtrado MAC en el router para que determinados dispositivos no puedan conectarse cuando lo activemos. Por ejemplo, si vamos a estar fuera de casa durante un tiempo prolongado y no queremos que la televisión o cualquier aparato se conecte al router y que pueda suponer un problema de seguridad en caso de que aparezca alguna vulnerabilidad.

Por tanto, un filtrado MAC tiene un doble enfoque. Si solo nos interesa bloquear un dispositivo en concreto o unos cuantos, lo mejor es crear una lista negra e incluirlos. En cambio, si lo que queremos es bloquear todas las conexiones y solo permitir los equipos de nuestra confianza, tendríamos que crear una lista blanca e incluirlos allí.

Lo que hace el router es identificar cada dispositivo según su dirección MAC. Si encuentra que esa dirección está en alguna lista que hemos creado, entonces es cuando actuaría. Esa dirección es única para cada tarjeta de red que tiene un dispositivo. Por ejemplo un simple reloj inteligente que tenga Wi-Fi, va a tener una MAC única

### SSID Oculto

El ssid wifi oculto es uno de los mecanismos de seguridad que implementan las redes Wifi ocultando su nombre, de este modo, sólo si conoces el SSID podrás conectarte a ella.

Para poder conectarnos a una red, lo primero que necesitamos es saber que está disponible. Esto es posible gracias a que la tecnología wifi (802.11) especifica que para dar a conocer una red se han de enviar paquetes de balizamiento (Management Beacon) ininterrumpidamente. De este modo los dispositivos cercanos con capacidades WiFi reciben estos paquetes de modo que saben que la red está disponible.

De este modo cuando en un dispositivo quiera visualizar la lista de redes disponibles, aparecerán aquellas de las cuales se ha recibido un paquete de este tipo, teniendo el listado siempre actualizado, útil cuando nos desplazamos o cambiamos de ubicación.

Cuando activamos el filtrado por ocultar SSID, todos los equipos que reciban los paquetes de balizamiento, recibirán el paquete vacío, por lo que los usuarios que quieran conectarse a la red, tendrían que agregar el SSID manualmente. Esto no significa que este método sea 100% efectivo ya que existen algunos software que pueden capturar todos los paquetes en la red, analizarlos y extraer el nombre de la red para que aparezca en la interfaz.

## VPN (Virtual Private Network)

Una VPN o red privada virtual crea una conexión de red privada entre dispositivos a través de Internet. Las VPN se utilizan para transmitir datos de forma segura y anónima a través de redes públicas. Su funcionamiento consiste en ocultar las direcciones IP de los usuarios y cifrar los datos para que nadie que no esté autorizado a recibirlos pueda leerlos.

Sus tres funciones principales son:

1. Privacidad

Las VPN utilizan el cifrado para mantener la privacidad de esta información confidencial, en especial cuando se conecta a través de redes wifi públicas.

2. Anonimato

Una conexión VPN oculta su dirección IP para que permanezca en el anonimato en Internet.

3. Seguridad

Las VPN utilizan la criptografía para proteger su conexión a Internet de accesos no autorizados.
