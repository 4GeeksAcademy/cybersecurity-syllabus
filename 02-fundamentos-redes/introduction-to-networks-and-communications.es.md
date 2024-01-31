# Lectura 1 📕: Introducción a las redes y comunicaciones

## **Introducción a las Redes: Un Viaje a través de la Conectividad**

Las redes han revolucionado la forma en que el mundo se comunica y comparte información. Estas estructuras interconectadas permiten la transmisión de datos, recursos y servicios entre dispositivos electrónicos, independientemente de su ubicación física. Desde los inicios modestos de la comunicación electrónica hasta las vastas redes globales que definen la era moderna, la evolución de las redes ha sido un viaje fascinante.

## **Historia de las Redes: Los Primeros Pasos**

La historia de las redes se remonta a mediados del siglo XX, cuando los científicos comenzaron a explorar formas de conectar computadoras y compartir información. Uno de los hitos clave en esta evolución fue la creación de ARPANET (Advanced Research Projects Agency Network) en la década de 1960. ARPANET, financiada por el Departamento de Defensa de los Estados Unidos, fue la primera red en utilizar el protocolo de conmutación de paquetes, un método que dividía los datos en paquetes más pequeños para su transmisión, lo que resultaba en una mayor eficiencia y robustez en comparación con los métodos de conmutación de circuitos utilizados en las redes telefónicas tradicionales.

## **ARPANET: Los Inicios de Internet**

ARPANET se estableció en 1969 y enlazó inicialmente a cuatro universidades de los Estados Unidos: la Universidad de California en Los Ángeles (UCLA), el Instituto de Investigación Stanford, la Universidad de California en Santa Bárbara y la Universidad de Utah. El primer mensaje transmitido a través de ARPANET fue "LOGIN", pero el sistema se bloqueó después de solo dos letras, lo que resultó en la primera vez que se envió "LO". A pesar de este comienzo modesto, ARPANET creció rápidamente y estableció los fundamentos de lo que eventualmente se convertiría en Internet.

A medida que avanzaban los años 70, ARPANET siguió creciendo y más instituciones académicas y de investigación se unieron a la red. La creación del protocolo TCP/IP (Transmission Control Protocol/Internet Protocol) en la década de 1980 fue un paso crucial para conectar diferentes redes en un sistema interconectado. TCP/IP permitió que diversas redes se comunicaran entre sí sin importar las diferencias en sus tecnologías subyacentes.

En 1983, ARPANET adoptó oficialmente el protocolo TCP/IP, lo que marcó el nacimiento de la Internet tal como la conocemos hoy en día. A medida que la tecnología evolucionó y se hizo más accesible, la década de 1990 vio la popularización de Internet en todo el mundo, y la World Wide Web (WWW) se convirtió en una interfaz gráfica para acceder a la información en línea.

Las comunicaciones en redes informáticas se basan en el intercambio de información entre dispositivos conectados, como computadoras, servidores, dispositivos móviles y más. Este intercambio se logra mediante el uso de protocolos y tecnologías que permiten la transmisión y recepción de datos de manera eficiente y confiable.

- **Protocolos de Comunicación:** Los protocolos son conjuntos de reglas y estándares que definen cómo los dispositivos en una red deben comunicarse entre sí. Estos protocolos aseguran que los datos se transmitan correctamente y se interpreten de la misma manera en ambos extremos de la comunicación. Ejemplos de protocolos comunes son el TCP/IP, utilizado en Internet, y el HTTP (Hypertext Transfer Protocol) para la navegación web.

- **Paquetización de Datos:** La información se divide en paquetes más pequeños antes de ser enviada a través de la red. Cada paquete contiene una parte de los datos, así como información de control, como la dirección de origen y destino. Esto permite que los paquetes se envíen independientemente y se reensamblen en el destino final.

- **Enrutamiento y Conmutación:** Los dispositivos en una red, como enrutadores y conmutadores, se encargan de dirigir los paquetes hacia su destino. Los enrutadores determinan la ruta más eficiente para que los paquetes viajen de un punto a otro en la red. Los conmutadores, por otro lado, gestionan el flujo de datos dentro de una red local.

- **Modelo Cliente-Servidor:** En muchas redes, se utiliza el modelo cliente-servidor. Los servidores almacenan y proporcionan recursos, como páginas web, archivos y servicios, a los clientes que solicitan dichos recursos. Los clientes pueden ser computadoras personales, dispositivos móviles u otros dispositivos conectados.

> 💡 Una red ocurre cuando un dispositivo logra conectarse a otro e intercambiar información con él. Esto no es algo que ocurra mágicamente ya que existe una serie de condiciones para que esta comunicación sea posible. Antes de conocer esas condiciones, conozcamos los tipos de redes que podemos encontrarnos en nuestro primer empleo:

1. **Redes de Área Local (LAN):** Son redes que abarcan un área geográfica limitada, como una oficina, un edificio o una casa. Las LAN permiten la comunicación directa y rápida entre dispositivos cercanos.
2. **Redes de Área Extensa (WAN):** Estas redes cubren distancias más grandes, como ciudades, países o incluso continentes. Internet es un ejemplo de una WAN global.
3. **Redes de Área Metropolitana (MAN):** Estas redes están diseñadas para cubrir áreas metropolitanas, como una ciudad. Proporcionan una mayor cobertura que una LAN pero no tan extensa como una WAN.
4. **Redes Inalámbricas:** Utilizan tecnologías de transmisión inalámbrica, como Wi-Fi y Bluetooth, para conectar dispositivos sin necesidad de cables físicos.
5. **Redes de Almacenamiento (SAN):** Están diseñadas para compartir dispositivos de almacenamiento, como discos duros y cintas magnéticas, entre servidores.
6. **Redes P2P (Peer-to-Peer):** En estas redes, los dispositivos comparten recursos directamente entre sí, sin depender de un servidor central. Es común en aplicaciones de intercambio de archivos.

## Topologías de red

Las topologías de red se refieren a cómo están dispuestos y conectados los dispositivos en una red informática. Hay varias topologías comunes, cada una con sus propias ventajas y desventajas. Aquí tienes una explicación clara de cada una:

**1. Topología de Estrella:**

![Topología de Estrella](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/topologia-estrella.png?raw=true)

- **Descripción**: En esta topología, todos los dispositivos de la red están conectados a un punto central, como un concentrador o un switch. Los dispositivos no están conectados directamente entre sí; en su lugar, se comunican a través del punto central.
- **Ventajas**:
    - Facilidad para agregar o quitar dispositivos sin interrumpir la red.
    - El fallo de un dispositivo no afecta a los demás.
    - Buen rendimiento en redes pequeñas y medianas.
- **Desventajas**:
    - Si el punto central falla, toda la red se ve afectada.
    - Puede requerir más cableado que otras topologías.

**2. Topología de Bus:**

![Topología de Bus](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/topologia-bus.png?raw=true)

- **Descripción**: En esta topología, todos los dispositivos están conectados a un solo cable compartido. Los datos se transmiten a lo largo de este cable, y cada dispositivo lee todos los datos, pero solo procesa los destinados a él.
- **Ventajas**:
    - Simple y fácil de instalar.
    - Buen rendimiento en redes pequeñas.
- **Desventajas**:
    - Si el cable principal se rompe o falla, toda la red puede dejar de funcionar.
    - El rendimiento puede degradarse en redes grandes o congestionadas.

**3. Topología de Anillo:**

![Topología de Anillo](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/topologia-anillo.png?raw=true)

- **Descripción**: En esta topología, los dispositivos están conectados en un bucle cerrado. Cada dispositivo está conectado al siguiente y el último se conecta al primero. Los datos circulan en un solo sentido a través del anillo hasta llegar al dispositivo de destino.
- **Ventajas**:
    - Buen rendimiento y velocidad de transmisión.
    - Cada dispositivo tiene igual acceso a la red.
- **Desventajas**:
    - Si un dispositivo o el cable se avería, puede afectar toda la red.
    - Menos común que otras topologías.
    
**4. Topología de Malla:**

![Topología de Malla](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/topologia-malla.png?raw=true)

- **Descripción**: En una topología de malla, cada dispositivo está conectado directamente a todos los demás dispositivos. Esto proporciona múltiples rutas para la comunicación.
- **Ventajas**:
    - Alta redundancia y confiabilidad, ya que las fallas en un enlace no afectan la conectividad.
    - Buena para redes críticas donde la confiabilidad es primordial.
- **Desventajas**:
    - Requiere mucho cableado y puede ser costoso de implementar.
    - La administración y el mantenimiento pueden ser complicados en redes grandes. 

**5. Topología de Árbol:**

![Topología de Árbol](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/topologia-arbol.png?raw=true)

- **Descripción**: En esta topología, los dispositivos se organizan en una estructura jerárquica similar a un árbol, con un nodo raíz que se conecta a subnodos y así sucesivamente.
- **Ventajas**:
    - Permite la expansión de la red de manera sencilla.
    - Ofrece cierta redundancia.
- **Desventajas**:
    - Si el nodo raíz falla, puede afectar a toda la red.
    - No es tan robusta como la topología de malla en términos de redundancia.

## **Servidores en Redes Informáticas: Potencia detrás de la conectividad**

Los servidores son componentes esenciales en una red informática. Estos potentes equipos están diseñados para ofrecer servicios, recursos y datos a otros dispositivos conectados en la red. Los servidores desempeñan un papel fundamental en la infraestructura de TI de muchas organizaciones, ya que permiten la comunicación eficiente, el almacenamiento de datos y la administración de recursos compartidos.

### **Tipos de Servidores:**

| Servidor de Archivos | Almacena y administra archivos que pueden ser accedidos y compartidos por usuarios y otros dispositivos en la red. Este tipo de servidor es común en entornos empresariales donde se necesita compartir documentos y recursos de manera centralizada. |
| --- | --- |
| Servidor Web | Alberga sitios web y aplicaciones web. Responde a las solicitudes de los navegadores de los usuarios y entrega contenido web, como páginas HTML, imágenes, videos y más. |
| Servidor de Correo Electrónico | Administra el correo electrónico para una organización. Recibe, almacena y envía mensajes de correo electrónico, permitiendo que los usuarios accedan a sus bandejas de entrada y envíen mensajes. |
| Servidor de Base de Datos | Almacena y administra bases de datos que contienen información estructurada. Permite el acceso, la consulta y la manipulación de datos por parte de aplicaciones y usuarios autorizados. |
| Servidor de Aplicaciones | Ejecuta aplicaciones empresariales y proporciona servicios de procesamiento de aplicaciones para usuarios y otros sistemas en la red. |
| Servidor Proxy | Actúa como intermediario entre los dispositivos de la red local y los recursos en Internet. Puede mejorar la seguridad y el rendimiento al cachear contenido y filtrar tráfico. |
| Servidor DNS (Domain Name System) | Traduce nombres de dominio legibles para los humanos en direcciones IP utilizables por las computadoras para localizar recursos en la red. |
| Servidor VPN (Virtual Private Network) | Proporciona conexiones seguras a través de Internet, permitiendo a los usuarios acceder a recursos de la red desde ubicaciones remotas como si estuvieran en la red local. |

## **Papel de los Servidores en una Red Informática Empresarial**

En una red informática empresarial, los servidores desempeñan un papel crucial en la gestión de recursos y servicios compartidos. Algunas funciones clave incluyen:

1. **Centralización de Recursos:** Los servidores permiten que los recursos, como archivos, aplicaciones y bases de datos, estén centralizados y disponibles para los usuarios autorizados en toda la organización.
2. **Gestión de Usuarios:** Los servidores pueden implementar políticas de seguridad y autenticación para garantizar que solo los usuarios autorizados accedan a los recursos de la red.
3. **Respaldos y Almacenamiento:** Los servidores de archivos y almacenamiento permiten la copia de seguridad y recuperación de datos críticos, asegurando la integridad de la información empresarial.
4. **Comunicaciones Internas y Externas:** Los servidores de correo electrónico y colaboración facilitan la comunicación y la colaboración entre empleados, así como con clientes y socios externos.
5. **Publicación Web:** Los servidores web permiten que las empresas presenten su presencia en línea y ofrezcan servicios y contenido a través de la World Wide Web.
6. **Gestión de Aplicaciones:** Los servidores de aplicaciones permiten la implementación y administración de aplicaciones empresariales críticas para el funcionamiento de la organización.

### ⚡️QUIZ

1. Una red LAN abarca un espacio geográfico reducido (Verdadero)
2. La topología BUS es la más simple de todas las estudiadas (Verdadero)
3. Un servidor Proxy es un tipo de VPN (Falso)