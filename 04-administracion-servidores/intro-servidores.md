### **Lectura 0:**

Felicitaciones por haber llegado hasta aquí, mientras más vamos avanzando en los módulos más cosas aprenderemos y pondremos en práctica lo aprendido, en este modulo pondremos en práctica todo lo aprendido en Linux para asi saber como manejar y administrar servidores de Linux.

Generalmente en los servidores almacenan y procesan datos críticos para las organizaciones. Por lo tanto, comprender cómo administrarlos de manera segura es crucial para proteger la información y garantizar la integridad de los sistemas. Así que en el siguiente módulo aprenderemos todo lo necesario para saber cómo administrar servidores, desde instalarlos y configurarlos hasta gestionar los permisos y usuarios y monitorear las actividades y rendimiento del servidor.

# **Lectura 1📕: Introducción a la administración de servidores Linux:**

## **Qué es un servidor y su importancia en los entornos de red**

Un servidor es un equipo de computación dedicado a proporcionar servicios, recursos y almacenamiento a otros dispositivos conectados en la red. El servidor es un componente fundamental en los entornos de red ya que actúa como un intermediario entre los usuarios y los recursos que necesitan acceder.

El propósito principal de un servidor es gestionar y facilitar el acceso a los recursos y servicios que ofrece. Estos recursos pueden incluir archivos, aplicaciones, bases de datos, servicios de correo electrónico, páginas web y mucho más.

Entre los diferentes tipos de servidores que existen, podemos conseguir:

- **Servidores de archivos**: Almacenan y comparten archivos en una red, permitiendo a los usuarios acceder y compartir información de manera centralizada.
- **Servidores web**: Albergan y sirven páginas web a los usuarios que las solicitan a través de un navegador. Estos servidores son esenciales para que los sitios web sean accesibles en Internet.
- **Servidores de correo electrónico**: Gestionan el envío, recepción y almacenamiento de correos electrónicos. Permiten a los usuarios enviar y recibir mensajes a través de una red.
- **Servidores de bases de datos**: Almacenan y gestionan grandes cantidades de datos estructurados. Estos servidores permiten el acceso y la manipulación eficiente de la información almacenada en las bases de datos.

Los servidores son una pieza importante en el departamento IT y en una empresa gracias a su capacidad para centralizar y gestionar eficientemente los recursos de una red, tales como archivos, aplicaciones, bases de datos, correo electrónico, entre otros. Al utilizar un servidor, los usuarios pueden acceder a estos recursos de una manera rápida y segura, sin la necesidad de tenerlos almacenados localmente en sus propios dispositivos.

Otro atributo o beneficio que podemos tener gracias a los servidores es la capacidad de compartir recursos. Por ejemplo: en una red de oficina, varios usuarios pueden acceder y compartir archivos almacenados en un servidor central, esto facilita la colaboración y el intercambio de información entre los miembros del equipo.

En cuanto a la seguridad, cuando centralizamos los recursos de la empresa en un servidor, es posible implementar medidas de seguridad más robustas, como firewalls, sistema de autenticación, cifrados de datos y software de seguridad, y así proteger la información sensible y prevenir accesos no autorizados, centralizar los recursos nos puede ayudar a simplificar la gestión y mantenimiento de la red, entre ellas tareas como la asignación de permisos de acceso y la realización monitoreo del rendimiento de la red.

Durante este módulo vamos a explorar todas las ventajas que vamos a tener al trabajar con un servidor y cómo administrar sus recursos para así sacar el mayor rendimiento de su funcionamiento.

### **Ventajas de linux como sistema operativo de servidor.**

Como administradores de servidores es normal preguntarse cuál es el mejor sistema operativo para usar en nuestro servidor, en módulos anteriores hemos hablado de GNU/Linux y mencionamos que es un sistema operativo de código abierto basado en unix, la realidad es que GNU/Linux se ha convertido en una opción popular para servidores en entornos empresariales y de desarrollo, principalmente para las pequeñas y medianas empresas que dependen en gran medida de la estabilidad de sus sitios web, una de las ventajas que ofrece linux es una mayor estabilidad y seguridad, además de permitir manejar con fluidez un mayor número de procesos

Estas son las ventajas que podemos tener al utilizar Linux como sistema operativo en un servidor:

| Estabilidad y fiabilidad | Una de las características más conocidas de Linux es su estabilidad y su fiabilidad. Esto es especialmente importante en entornos de servidor, ya que la disponibilidad y el tiempo de actividad es un elemento crítico dentro del entorno. |
| --- | --- |
| Seguridad | Linux es conocido por tener sistema operativo robusto en términos de seguridad. Al ser de código abierto, miles de desarrolladores en todo el mundo trabajan constantemente para identificar y solucionar vulnerabilidades, además, la estructura de permisos y la capacidad de personalizar la configuración de seguridad, hacen de Linux una opción segura para servidores. |
| Flexibilidad y personalización | Linux nos ofrece una gran flexibilidad y capacidad de personalización, estas características hacen que los administradores de servidores puedan elegir entre una amplia variedad de distribuciones y configurar el sistema según sus necesidades específicas, así, optimizando el rendimiento y adaptar el sistema a los requisitos del sistema |
| Costo |  Al ser un sistema operativo de código abierto, Linux no requiere el pago de licencias, lo que puede suponer en un ahorro significativo en comparación con otros sistemas operativos comerciales, además, los usuarios pueden tener acceso al código fuente y así modificarlo y adaptarlo según sus necesidades. |
| Comunidad y soporte |  Linux cuenta con una gran comunidad de usuarios y desarrolladores que ofrecen soporte y asistencia, podemos conseguir una amplia gama de recursos en línea, foros y documentación disponible para resolver problemas y obtener ayuda en caso de necesitarlo. |

### **Conceptos básicos para administración de servidores.**

Podemos definir a la administración de servidores como un conjunto de prácticas y conocimientos necesarios para gestionar y mantener eficientemente los servidores en un entorno de red.

Algunos conceptos que tenemos que tener claros al momento de hablar de administración de servidores son:

1. **Sistema operativo:** Es el software fundamental que permite el funcionamiento del servidor. Es importante tener un buen conocimiento del sistema operativo utilizado en el servidor, como Linux, Windows Server, macOS Server, entre otros. Esto incluye la instalación, configuración y actualización del sistema operativo.
2. **Roles y servicios**: Los servidores pueden desempeñar diferentes roles y ofrecer diversos servicios. Algunos ejemplos comunes son servidores web, servidores de correo electrónico, servidores de bases de datos, servidores de archivos, entre otros. Es importante comprender los roles y servicios que se necesitan en la red y cómo configurarlos adecuadamente en el servidor.
3. **Seguridad:** La seguridad es un aspecto crítico en la administración de servidores, ya que implica implementar medidas de seguridad como firewalls, sistemas de detección de intrusiones, cifrado de datos y políticas de contraseñas seguras. También es importante mantener el sistema operativo y las aplicaciones actualizadas para protegerse contra vulnerabilidades conocidas.
4. **Copias de seguridad**: Realizar copias de seguridad periódicas es esencial para proteger los datos almacenados en el servidor. Esto implica establecer una estrategia de respaldo adecuada, que incluya la frecuencia de las copias de seguridad, los medios de almacenamiento utilizados y la verificación regular de la integridad de los datos de respaldo.
5. **Monitoreo de procesos**: Es importante monitorear el rendimiento del servidor para garantizar su correcto funcionamiento. Esto implica supervisar el uso de recursos como la CPU, la memoria y el almacenamiento, así como el tráfico de red. El monitoreo permite identificar posibles cuellos de botella y tomar medidas para optimizar el rendimiento del servidor.
6. **Administración remota**: La administración remota permite gestionar el servidor desde cualquier ubicación. Esto se logra a través de herramientas de administración remota como SSH (Secure Shell) o herramientas de administración centralizada. La administración remota facilita la configuración, el monitoreo y la solución de problemas sin necesidad de estar físicamente en el lugar donde se encuentra el servidor.
7. **Servidor de nube:** Es un recurso de servidor centralizado y agrupado que se aloja y distribuye a través de una red y al que pueden acceder múltiples usuarios cuando lo necesiten. Los servidores de nube pueden realizar las mismas funciones que un servidor físico tradicional, proporcionando potencia de procesamiento, almacenamiento y aplicaciones. Para su funcionamiento se instalan un software de gestión llamado hipervisor en servidores físicos para conectarlos y virtualizarlos, los recursos combinados se desvinculan y se agrupan para crear servidores virtuales.
