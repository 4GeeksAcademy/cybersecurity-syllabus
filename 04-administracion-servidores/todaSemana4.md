# administracionDeServidores

1. Introducción a la administración de servidores Linux:
    - Qué es un servidor y su importancia en los entornos de red.
    - Ventajas de utilizar Linux como sistema operativo de servidor.
    - Conceptos básicos de administración de servidores.
2. Instalación de Linux en una máquina virtual para servidores:
    - Preparación del entorno de virtualización.
    - Descarga e instalación de una distribución de Linux para servidores.
    - Configuración inicial del sistema operativo.
3. Administración básica de usuarios y grupos:
    - Creación y gestión de cuentas de usuario.
    - Asignación de permisos y privilegios.
    - Configuración de grupos y asignación de usuarios a grupos.
4. Gestión de archivos y directorios:
    - Navegación y manipulación de archivos y directorios.
    - Configuración de permisos y atributos de archivos.
    - Búsqueda y filtrado de archivos.
5. Configuración de servicios de red:
    - Configuración de la interfaz de red.
    - Configuración de la resolución de nombres (DNS).
    - Configuración de servicios de red (por ejemplo, HTTP, FTP, SSH).
6. Gestión de paquetes y software:
    - Uso de gestores de paquetes para la instalación y actualización de software.
    - Búsqueda y eliminación de paquetes.
    - Configuración de repositorios de software.
7. Configuración de seguridad del servidor:
    - Configuración del firewall.
    - Gestión de usuarios y autenticación segura.
    - Configuración de registros de auditoría (logs) del sistema.
8. Programación de tareas automatizadas:
    - Uso de cron para programar tareas.
    - Creación y edición de archivos crontab.
    - Monitoreo y verificación de tareas programadas.
9. Respaldo y recuperación de datos:
    - Planificación de respaldos y políticas de retención.
    - Uso de herramientas de respaldo y recuperación.
    - Pruebas y verificación de los respaldos.
10. Monitoreo y optimización del rendimiento del servidor:
    - Uso de herramientas de monitoreo del sistema.
    - Identificación y solución de cuellos de botella del sistema.
    - Optimización de recursos y configuraciones del servidor.

# **Semana : Administración de sistemas**

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

### **⚡️QUIZ Introducción a la administración de servidores Linux:**

1. **¿Qué servicio podemos gestionar en un servidor?**
    - **Bases de datos,**
    - **Sistemas de seguridad**
    - **Virtualización de sistema operativo**
2. **Que sistema operativo de servidor no requiere licencias por lo que no tendríamos un gasto por su instalación**
    - **MacOs Server**
    - **Linus**
    - **Windows Server**
3. **¿Qué herramienta nos permite poder acceder a nuestro servidor de manera remota?**
    - **Secure Shell (SSH)**
    - **Bash**
    - **Virtualización en al nube**

# **Lectura 2 📕: Instalación de Linux en Maquina virtual**

## **Preparación del entorno de virtualización.**

Aunque ya hayamos tocado el tema de virtualización anteriormente, recordaremos brevemente el concepto. La virtualización es una tecnología que permite la creación de múltiples entornos virtuales en un solo servidor físico. Estos entornos virtuales, también conocidos como máquinas virtuales, son independientes entre sí y pueden ejecutar diferentes sistemas operativos y aplicaciones.

Preparar un entorno para virtualización puede constar de diferentes pasos, tales como:

- **Hardware adecuado**: Antes de comenzar, asegúrate de contar con un hardware adecuado para la virtualización. Esto incluye un servidor potente con suficiente capacidad de almacenamiento, memoria RAM y capacidad de procesamiento para soportar las máquinas virtuales que planeas crear.
- **Selección del software de virtualización**: Existen diferentes opciones de software de virtualización, como VMware, VirtualBox y Hyper-V. Es importante investigar y seleccionar el software que mejor se adapte a tus necesidades y requisitos.
- **Instalación del software**: Una vez que hayas seleccionado el software de virtualización, deberás instalarlo en el servidor. Podemos seguir la documentacion de la empresa desarrolladora del software o conseguir documentacion en linea
- **Configuración de la red**: Este paso es esencial para permitir la comunicación entre las máquinas virtuales y el resto de la red. Configura las interfaces de red de acuerdo con tus necesidades y asegúrate de asignar direcciones IP únicas a cada máquina virtual.
- **Creación de máquinas virtuales**: Una vez que el entorno de virtualización esté configurado, podrás crear las máquinas virtuales. Define los recursos asignados a cada máquina virtual, como la cantidad de memoria RAM, espacio en disco y número de núcleos de procesador.
- **Instalación de sistemas operativos y aplicaciones**: Después de crear las máquinas virtuales, deberás instalar los sistemas operativos y las aplicaciones necesarias en cada una de ellas. Esto se puede hacer utilizando imágenes ISO o discos de instalación.
- **Configuración de seguridad**: No olvides configurar medidas de seguridad adecuadas para proteger tu entorno de virtualización. Esto incluye la configuración de firewalls, actualizaciones de seguridad y políticas de acceso.

La preparación de un entorno de virtualización es un proceso que requiere planificación y ejecución cuidadosa. Sin embargo, los beneficios de la virtualización pueden ser significativos, por lo que vale la pena invertir el tiempo y los recursos necesarios para preparar un entorno adecuado.

## **Descarga e instalación de una distribución de Linux en servidores**

Recordemos que una distribución de Linux es un sistema operativo que puede usar el kernel de Linux, el cual cada versión puede variar en su sistema de gestión de paquetes y librerías.

Entre las distribuciones de Linux más populares para servidores tenemos:

- **Ubuntu Server:**

Ubuntu server es una de las distribuciones más conocidas y usadas para servidores actualmente en el mercado, es una variación de los sistemas operativos basados en Debian, esto significa que pueden tener una arquitectura similar y el mismo sistema manejador de paquetes, aunque en un ambiente profesional, Ubuntu Server puede tener un manejo mucho más fácil y una más alta compatibilidad del hardware.

Su instalación y configuración del sistema operativo son relativamente sencillas, y cuenta con una gran cantidad de documentación y recursos en línea para ayudarte en el proceso. Además, es compatible con una amplia gama de arquitecturas de hardware, lo que te brinda flexibilidad al elegir el servidor adecuado para tus necesidades.

La principal desventaja que puede tener Ubuntu server es que es un sistema operativo que ocupa mucho espacio en la máquina, y que las personalizaciones del sistema son posibles solo dentro de un marco limitado

<aside>
👉 Ubuntu Server es una gran opción cuando se busca administrar un servidor dentro de una estructura más fácil de manejar, sobre todo si se está en cambio desde windows.

</aside>

- **Red Hat Enterprise Linux (RHEL)**

Este sistema operativo es otra de las plataformas más usadas en servidores y en entornos empresariales, también hay que mencionar que está certificado en cientos de nubes, RHEL se destaca por su enfoque en la estabilidad, seguridad y rendimiento.

Una de las características clave de RHEL para servidores es su capacidad para manejar cargas de trabajo críticas y de alto rendimiento. Está diseñado para ofrecer un rendimiento óptimo y una alta disponibilidad, lo que lo convierte en una opción confiable para aplicaciones empresariales y servicios en línea también ofrece una amplia gama de herramientas y servicios para facilitar la administración y el despliegue de servidores.

La empresa detrás de RHEL, Red hat ofrece soporte técnico y servicios profesionales, lo que brinda a las empresas la tranquilidad de contar con asistencia experta en caso de problemas o necesidades específicas. También hay una gran comunidad de usuarios y desarrolladores de RHEL que proporcionan recursos y soporte adicional en línea.

Entre las desventajas que ofrece RHEL tenemos que no un sistema gratuito, ya que se maneja por suscripciones y además, no es un sistema solamente basado en línea de comando por lo que no lo hace ideal para principiantes

Si bien mencionamos como desventaja que RHEL no es un sistema gratuito, esto lo podemos tomar también como una ventaja ya que en seguridad, ofrece varias soluciones como Security-Enhanced Linux (SELinux) y los controles de acceso obligatorios (MAC), que le permiten evitar las intrusiones y cumplir con la normativa vigente. La plataforma también está certificada conforme a los Estándares Federales de Procesamiento de la Información (FIPS) 140-2, y es el primer soporte de los marcos de contenedores de Linux en obtener la certificación de Common Criteria (v7.1).

Este sistema operativo es ideal cuando queremos trabajar en un amplio ecosistema de software, hardware y nube (AWS, Microsoft Azure, Oracle Cloud Infrastructure).

- **CentOs**

CentOS está basado en Red Hat Enterprise Linux (RHEL) desde 2009, pero es de código abierto y gratuito. El sistema operativo es compatible con RHEL y destaca por su facilidad de uso. Especialmente en el ámbito de las distribuciones de servidores Linux, CentOS siempre ha sido convincente y se consideraba una solución de entrada que era válida para muchos usuarios. Sin embargo, Red Hat ha anunciado que la compatibilidad con CentOS finalizará en 2024. El sucesor CentOS Stream es visto con recelo por muchos desarrolladores, ya que es muy experimental y no es totalmente compatible con RHEL. La nueva solución funciona más bien como un entorno de prueba para el sistema.

CentOS es y fue considerado una solución gratuita a nivel básico que podía ofrecer las características de RHEL. El sistema operativo funciona de forma muy estable y es muy seguro gracias a una fuerte supervisión y a los parches regulares de la comunidad.

Sin embargo, CentOS no es una solución para el futuro, ya que la compatibilidad del sistema operativo se interrumpirá en un futuro cercano. Aunque muchas aplicaciones de RHEL también funcionan en CentOS, esto no siempre está garantizado porque faltan muchas certificaciones necesarias.

CentOS solo es apto para principiantes que quieran conocer RHEL sin pagar por él. Para proyectos a largo plazo, recomendamos otras distribuciones de Linux.

- **Debian**

Debian es una de las distribuciones para servidores web clásicas y de larga duración. El sistema existe desde 1993 y cuenta con una enorme comunidad en todo el mundo. Esta comunidad no solo utiliza Debian, sino que también mantiene el sistema. Debian es la base de muchas otras distribuciones de Linux, pero también está siendo constantemente optimizado por más de 1000 desarrolladores oficiales. El sistema operativo es igualmente recomendable para servidores, ordenadores de mesa y portátiles.

Además de su disponibilidad gratuita, la estabilidad y versatilidad de Debian hablan por sí mismas. El sistema operativo no solo es fiable, sino que también es compatible con numerosas arquitecturas de hardware y permite a los usuarios realizar numerosos ajustes individuales

Los principiantes pueden tener dificultades con Debian, ya que la instalación y la configuración pueden resultar complejas. Las actualizaciones no se producen a intervalos fijos y, por tanto, son difíciles de planificar. No se admiten archivos de paquetes personales. Además, la interfaz es clara, pero no muy moderna.

Debian es una solución fiable para los desarrolladores experimentados que se dediquen principalmente al sector del software y el hardware.

Existen distintas maneras de instalar una distribución de linux para un servidor. Para hacer una instalación directa debemos contar con la imagen ISO que descargamos en el paso anterior, y lo convertimos en un medio de instalación con un CD o una memoria USB para instalarlo directamente a la máquina que queramos usar en nuestro servidor, la ventaja de este método es que estaremos aprovechando el 100% de todos los recursos dedicados al servicio o servicios que queramos usar.

Otro de los metodos de instalacion que nos puede resultar bastante útil es la virtualización, el cual anteriormente hemos mencionado que permite crear versiones virtuales de recursos informáticos, como servidores, redes, almacenamiento y sistemas operativos y así en lugar de depender de una única instancia física, la virtualización permite la creación de múltiples instancias virtuales que se ejecutan de manera independiente en un entorno compartido, la virtualización implica la creación de servidores virtuales que se ejecutan en un servidor físico subyacente.

Para este módulo vamos a instalar ubuntu server en una máquina virtual para familiarizarnos con este entorno

Así como haciamos la instalación de una distribución de Linux, podemos descargar el sistema operativo a través de la página web de soporte de la distribución, para efecto de este módulo vamos a instalar Ubuntu server ingresando a [https://ubuntu.com/download/server](https://ubuntu.com/download/server) y descargando la version LTS (Long Term Support). Si quieres probar con otra distribución para servidor, puedes investigar cual es la página de descarga para la distribución que quieras usar.

Una vez descargado abrimos nuestro software de virtualización, para este módulo seguiremos con Virtual Box. Si no lo has descargado, puedes hacerlo a través de [https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads).

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image1.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image1.png)

Para comenzar la configuración de nuestro servidor seleccionamos la opción nueva y llenar la información de las características que queremos colocar a nuestra máquina virtual:

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image2.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image2.png)

1. Asignamos 2 GB de ram y dos procesadores.

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image3.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image3.png)

1. Seleccionamos la opción de crear un disco duro virtual y asignamos la cantidad de memoria.

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image4.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image4.png)

1. Vemos el resumen de cómo estará configurada nuestra máquina virtual y aceptamos.

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image5.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image5.png)

<aside>
👉 Ya tenemos nuestra máquina virtual configurada y lista para funcionar, en la próxima lectura aprenderemos como configurar ubuntu server y por primera vez ver el entorno de un servidor.

</aside>

## **Configuración inicial del sistema operativo**

Aca te dejamos una pequeña guia de como configurar inicialmente ubuntu server dentro de nuestra máquina virtual:

- Antes de comenzar la instalación tenemos que hacer una previa configuración de la red por lo que entraremos en la seccion de configuracion del menu

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image6.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image6.png)

- Seleccionaremos la opción de red y en la opción de *Conectado a:* seleccionamos la opción *Adaptador puente*. Esto nos permite que nuestra máquina virtual pueda conectarse a la tarjeta de red que tengamos en la máquina host y seleccionamos aceptar

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image7.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image7.png)

- Una vez configurado la red, le damos click en iniciar y se nos abrirá una nueva ventana con la maquina virtual

### **Laboratorio 1** Escenario:

Acabas de ser contratado por la start-up D´sistemas cta para ser su administrador de sistemas, esta empresa necesita montar unos servidores para poder operar y facilitar el acceso a su información, aunque no tengas muchos conocimiento de como instalar un sistema operativo en un servidor, tu jefe decide acompañarte y explicarte en todo momento el paso a paso para la instalacion de nuestro servidor ubuntu.

1. Una vez arrancada la instalacion seleccionamos la primera opción “Try or install Ubuntu Server”

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image8.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image8.png)

1. Lo primero que configuraremos será el idioma, por lo que seleccionaremos el idioma en el que nos queramos manejar en nuestro servidor.
2. La próxima ventana nos indicará la configuración de idioma del teclado, por lo que también seleccionaremos el idioma que queramos usar en nuestro teclado.
3. En la próxima ventana nos dara a seleccionar el tipo de instalación que queremos hacer
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image9.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image9.png)
    
4. Ubuntu Server instalará una serie de paquetes que nos ayudará en el manejo de nuestro sistema operativo.
5. Ubuntu server (Minimized) es una versión más adaptable para ambientes de pruebas donde se espera algún tipo de ingreso de usuario.
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image10.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image10.png)
    
6. Seleccionaremos la primera opción.
7. El próximo paso configuramos un adaptador de red, gracias a la configuración de red de adaptador puente que hicimos previamente podemos seleccionar nuestra tarjeta de red de nuestra máquina host.
8. Luego debemos que configurar un servidor Proxy en el caso que tengamos uno disponible, de no tener podemos saltar este paso
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image11.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image11.png)
    
9. Después de la configuración de un proxy, tendremos que configurar el archivo Mirror, este es el archivo al cual nos vamos a conectar para obtener los repositorios del gestor de paquetes de archivos, ahi nos van a dar una opción por defecto la cual vamos a aceptar
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image12.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image12.png)
    
10. El próximo paso paso será configurar un disco en el que vamos a almacenar nuestro Sistema operativo, en este caso de virtualización, tendremos la opción de un disco virtual, después tendremos el resumen de las particiones del disco en el cual tendremos dos particiones, partition 1 que tendremos el grub, y la partition 2 donde tendremos nuestro Sistema operativo
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image13.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image13.png)
    
11. En la próxima ventana nos pedirá que le coloquemos los nombres a la máquina y al servidor junto a su contraseña.
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image14.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image14.png)
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image15.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image15.png)
    
12. El próximo paso nos preguntará si queremos instalar el servicio OpenSSH, recordemos que SSH es un protocolo el cual nos permitirá que podamos acceder a nuestro servidor de manera remota por lo que lo recomendable es aceptar.
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image16.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image16.png)
    
13. Seleccionaremos algunos paquetes que queramos tener en nuestro sistema operativo, estas selecciones son opcionales por lo que no aceptaremos ninguno para esta práctica.
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image17.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image17.png)
    
14. Después del último paso comienza la instalación del sistema operativo por lo que esperaremos unos minutos a que se termine una vez finalizada la instalación, seleccionamos la opción reboot now.
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image18.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image18.png)
    

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image19.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image19.png)

<aside>
💭 Una vez terminada la instalacion tu jefe se sienta contigo y te hace ciertas preguntas saber que tanto aprendiste en este proceso.

</aside>

- ¿Por que se elegio el tipo de instalacion?
- De tener un proxy para el servidor, ¿se puede agregar al momento de instalar?
- ¿Que beneficio podemos tener al instalar openssh?

# **Lectura 3 📕: Administración básica de usuarios y grupos**

## **Creación y gestión de cuentas de Usuario.**

Dentro del sistema, el administrador de sistema tiene el privilegio de ser el usuario root el cual significa que es el único usuario autorizado todos la creación de usuario y grupos y administración de todos estos archivos. Esta práctica no es recomendable ya que en algún caso de error, podemos causar fallas graves al sistema por lo que en el transcurso de las siguientes prácticas estamos bajo un usuario de sistema y le otorgamos privilegios de superusuarios con sudo.

Como administradores de sistemas, saber como crear y gestionar las cuentas de los usuarios de nuestro sistema es algo que necesitamos conocer y dominar, ya que los usuarios son las personas o entidades que van a interactuar con el servidor y van a requerir acceso a recursos y servicios específicos. Crear una cuenta de usuario no es algo difícil en Linux, involucra también crear contraseña y asignarlo a un grupo y permisos. Aquí les dejamos un ejemplo de como crear y gestionar una cuenta de usuario, para ello abriremos la máquina virtual de nuestro servidor y seguiremos los siguientes pasos:

- Para crear a un usuario, usaremos el comando **“useradd”** seguido del nombre de usuario, una vez ingresado el comando se pedirá que ingrese una contraseña para el usuario

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image20.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image20.png)

- Si queremos cambiar la contraseña lo hacemos con el comando **passwd** seguido del usuario de la contraseña que queremos cambiar

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image21.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image21.png)

- Una forma de facilitar la administración de permisos de directorios y archivos son a través de los grupos, podemos crear grupos con el comando **groupadd** y asignar al usuario en el grupo con el comando **usermod** junto a las flags **a** (para agregar a grupo) y **G** para agregar a grupo secundario, si queremos ver los grupos al que pertenece el usuario en el sistema usamos el comando groups.

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image22.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image22.png)

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image23.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image23.png)

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image24.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image24.png)

- Si queremos ver los grupos que existen en el sistema podemos conseguir en la ruta /etc/group

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image25.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image25.png)

- Cuando necesitemos eliminar un usuario del sistema lo haremos con el comando userdel seguido del nombre del usuario.

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image26.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image26.png)

**Es recomendable gestionar y crear los usuarios usando los privilegios de usuario sudo y no desde el usuario root ya que a la hora de un error desde el usuario root puede ser fatal para el sistema.**

<aside>
⚠️ Recuerda que la creación y gestión de cuentas de usuario en servidores Linux debe realizarse de manera segura y siguiendo las mejores prácticas de seguridad. Esto incluye el uso de contraseñas fuertes, la asignación adecuada de permisos y la implementación de políticas de seguridad.

</aside>

## **Asignación de permisos y privilegios.**

Como administradores de sistema, es importante saber y conocer cómo gestionar y asignar permisos y privilegios a cada usuario del sistema, ya que los permisos pueden determinar qué acciones pueden realizar los usuarios y los privilegios definen el nivel de acceso y control sobre el sistema.

Cuando manejamos un servidor una de las mejores prácticas para proteger la información es poniendo en práctica el principio del menor privilegio, el cual consiste en asignarle los permisos de accesos mínimos necesarios para que pueda desempeñar actividades en el sistema, para ello es necesario conocer sobre los permisos y cómo gestionarlos.

En linux, lectura (r), escritura (w) y ejecución (x). Estos permisos se asignan a tres grupos de usuarios: el propietario del archivo, el grupo al que pertenece el archivo y otros usuarios. podemos ver estos permisos en los directorios o archivos con el comando: ***`ls -l`***

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image27.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image27.png)

En la siguiente imagen podemos ver como tenemos un archivo llamado `text.txt` el cual cuenta con sus permisos agrupado en tres grupos:

- Los primeros tres permisos son los permisos que tiene el propietario del archivo (“usuario"). En este caso tenemos permiso de lectura (r) y escritura (w) pero no de ejecución. rw-
- El segundo grupo de permisos son los permisos que tienen los usuarios del grupo (“departamentoIT), en este caso tenemos los mismos permisos de lectura y escritura pero no de ejecución. rw-
- El tercer grupo de de permiso son los permisos para el resto de los usuarios del sistema el cual solo podrán leer el archivo mas no podrán ni escribir o editar sobre el ni ejecutarlos

<aside>
💡 Es normal que a todos los usuarios del sistema los separamos por grupos para que así puedan acceder únicamente a los archivos que necesitan leer, escribir o ejecutar de acuerdo al nivel de privilegios que tenga tal usuario, y así proteger información confidencial de otros departamentos de la organización, una vez que creamos un usuario, es necesario darle permisos de acuerdo a las labores que vaya a realizar en la organización.

</aside>

Con el comando `chmod` podemos cambiar y otorgar permisos a los usuarios sobre un archivo.

- Si queremos dar permiso a un usuario (u), a un grupo (g) o a otros usuarios del sistema (o) colocamos la flag seguido de un + y el permiso que vayamos a asignar.
- En este caso, gestionamos permisos de lectura, escritura y ejecución solo para el propietario del archivo (u).

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image28.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image28.png)

<aside>
💡 Podemos generar permisos esenciales con los bits de ejecución setuid (suid), el bit de ejecución setgid (sgid) y el bit de ejecución sticky. El bit suid permite que un archivo se ejecute con los privilegios del propietario, mientras que el bit sgid permite que un archivo se ejecute con los privilegios del grupo. El bit sticky se utiliza principalmente en directorios para evitar que los usuarios eliminen archivos de otros usuarios

</aside>

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image29.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image29.png)

En este caso, generamos permisos de suid de privilegio de usuario y grupo al archivo `text.txt`

Otra manera de gestionar los permisos es asignarlos con la cantidad de bits de los permisos. Tomando en cuenta que cada permiso tiene una cantidad de bits podemos sacarlos como:      

- Lectura r (4)
- Escritura w (2)
- Ejecución x (1)
1. Si queremos gestionar permisos por bits esta cuenta te puede resultar útil
    - Lectura (r), Escritura (w) Ejecución (x) rwx = 7
    - Lectura (r), Escritura (w) rw- =6
    - Lectura (r), Ejecución (x) r-x = 5
    - Lectura (r) r– = 4
    - Escritura (w), Ejecución -wx = 3
    - Escritura (w) -w- = 2
    - Ejecución (x) –x = 1
2. Colocaremos la cantidad de bits que los permisos que queramos otorgar de acuerdo a la posición de usuario, grupo y otros.
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image30.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image30.png)
    
    <aside>
    💡 La asignación de permisos y privilegios en linux es esencial para así garantizar al seguridad y el control adecuado sobre los recursos del sistema
    
    </aside>
    

## **Configuración de grupos y asignación de usuarios a grupos.**

Saber cómo configurar y asignar un usuario a un grupo en específico es ideal cuando queremos ganar tiempo y tenemos un sistema con muchos usuarios, ya que una manera rápida de hacerlo es ir asignando a los usuarios a un grupo con los permisos de usuarios mínimos de acuerdo a su labor. Por ejemplo podemos tener un grupo de departamentoIT que pueda tener acceso ejecutar a los scripts de automatización de tareas del sistema y asi, que los usuarios de departamento de marketing no puedan tener acceso a dichos scripts.

Para ello tenemos comandos que nos pueden ayudar tales como **`groupadd`** para crear un grupo.

Para este ejercicio hemos creado un grupo llamado departamentomarketing, ya una vez creado podremos agregar al usuario al grupo con el comando adduser seguido del nombre de usuario y el grupo al cual queremos que pertenezca.

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image31.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image31.png)

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image32.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image32.png)

En este comando hicimos que el usuario1 pasará a ser del grupo de departamentomarketing.

Si queremos remover a un usuario del grupo lo podemos lograr con el comando deluser seguido del nombre del usuario y el grupo del cual queremos removerlo.

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image33.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image33.png)

Una forma de ver los grupos en el sistema es accediendo a la ruta /etc/group usando el comando cat. Ahí podemos ver todos los grupos que tenemos seguido de un número o identificador de grupo (gid). Por lo general, al momento de crear grupos, el sistema le asigna un gid de 1000 en adelante. Los gid menores a 100 son reservados para uso del sistema y sus grupos especiales.

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image34.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image34.png)

Si queremos modificar el gid o el nombre del grupo podemos hacerlo a través del comando groupmod seguido del nuevo gid o el nombre y el gid o nombre anterior.

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image35.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image35.png)

### **⚡️QUIZ Administración básica de usuarios y grupos**

- **¿Cual comando nos permite crear un usuario en el sistema?**
    - **useradd**
    - **adduser**
    - **deluser**
- **¿Cual comando nos permite asignar un usuario dentro de un grupo?**
    - **groupadd**
    - **useradd**
    - **usermod**
- **¿Cual comando nos permite cambiar los permisos dentro de un directorio o archivo?**
    - **groupadd**
    - **chmod**
    - **deluser**
    

# **Lectura 4 📕: Gestión de archivos y directorios:**

## **Navegación y manipulación de archivos y directorios.**

Para un administrador de sistema, tener conocimiento de navegación y manipulación de archivos y directorios es una parte fundamental del trabajo, en linux todo esto lo podemos lograr desde la misma línea de comandos, a través de ciertos comandos y herramientas, podemos navegar por el sistema de archivos, crear, copiar mover y eliminar archivos y directorios.

Para comenzar, es importante comprender la estructura de directorios. El sistema de archivos se organiza jerárquicamente, con un directorio raíz representado por "/". A partir de ahí, los directorios se organizan en una estructura de árbol, lo que permite una fácil navegación y ubicación de archivos.

Dentro de los comandos básicos tenemos:

| Comando | Flags | Funcion |
| --- | --- | --- |
| pwd |  | Imprime el directorio actual de trabajo |
| cd |  | Cambiar el directorio de trabajo |
| ls |  | Listar contenido del directorio |
|  | -R | Listara todos los archivos dentro de los subdirectorios |
|  | -a | Mostrará todos los archivos ocultos |
|  | -al | Mostrará la información detallada de los archivos y directorios |
| head |  | Permite ver hasta las primeras 10 lineas de texto de un archivo |
|  | -n o -lines | Nos imprime un numero de lineas personalizado (hasta 10) |
| tail |  | Permite ver las ultimas 10 lineas de texto de un archivo |
|  | -n o -lines | Nos permite ver un numero de lineas personalizado |
| (hasta 10) |  |  |
| cat |  | Concatena y escribe contenido de los archivos en su salida estanadar, tambien se puede usar para el contenido de los archivos |
| cp |  | Copia archivos o directorios y su contenido. |
| Se coloca el nombre del archivo a copiar y el directorio destino |  |  |
| cp nombrearchivo.txt /inicio/nombredeusuario/Documentos |  |  |
| mv |  | Mueve uno o mas archivos o directorio y su contenido a otro directorio |
| Se coloca el nombre del archivo a mover y el directorio destino |  |  |
| mv nombrearchivo.txt /inicio/nombredeusuario/Documentos. |  |  |
| rm |  | Se utiliza para eliminar un archivo o directorio del sistema |
|  | -i | Pide confirmacion del sistema antes de borrar un archivo |
|  | -f | Permite al sistema eliminar sin confirmación |
|  | -r | Borra archivos y directorios de forma recursivas |
| touch |  | Crea un archivo en blanco |
| mkdir |  | Crea un directorio |
|  |  |  |

<aside>
⚠️ Es importante tener precaución al utilizar comandos de manipulación de archivos y directorios, ya que las acciones son irreversibles y pueden afectar los datos de manera permanente. Siempre asegúrate de tener copias de seguridad actualizadas y de verificar dos veces antes de ejecutar comandos que puedan tener consecuencias no deseadas.

</aside>

## **Configuración de permisos y atributos de archivos**

Recordemos que los permisos son un conjunto de reglas y configuraciones que determinan qué tipo de acciones puede realizar un usuario y grupos sobre un archivo o directorio dentro del sistema. Estos son necesarios ya que permiten aumentar la seguridad del sistema y tener un mayor control de acceso. Linux es un sistema operativo multiusuario, por lo que es normal acceder de forma simultánea con varios usuarios registrados localmente en nuestro sistema, por lo tanto, como administradores de sistema, dentro de nuestras labores debe estar realizar una revisión periódica de los permisos existentes.

Imaginemos que tenemos un servidor FTP y diferentes usuarios y grupos, si todos los usuarios tuvieran permisos de administrador, pudieran escribir, leer y ejecutar cualquier archivo que tengamos dentro de las carpetas, por lo que es muy importante gestionar adecuadamente los permisos a todos los usuarios y grupos para que solamente puedan acceder a los archivos y directorio que queramos que accedan, sin importar que puedan autenticarse en el sistema.

Entre las distintas cuentas que podemos tener dentro del sistema Linux tenemos;

- Usuario con mayor privilegio:  **Root**, generalmente se le asigna este usuario al administrador de sistema
- *Usuario normal*: ls

Previamente hablamos sobre los permisos en Linux, recordemos cuales son:

- **Lectura (r):** Es el primer permiso que podemos encontrarnos. Este nos da la opción de que un usuario pueda ver el contenido al que quiere acceder.
- **Escritura (w):** Nos da la posibilidad de otorgar poder sobre un archivo. De esta forma podrá ser modificado, al igual que un directorio.
- **Ejecución (x):** Permite a los usuarios ejecutar diferentes parámetros dentro del equipo.
- **Sin permisos (-)**: Nos indica que el usuario no tiene ningún tipo de permiso sobre el recurso de red o contenido compartido También podemos tocar nuevamente los niveles de permisos, los cuales van a definir algunos parámetros en cuanto a las posibilidades de uno o más usuarios sobre los archivos.
- **Permisos de propietario**: Se trata del usuario que crea el archivo desde su equipo. Linux asigna a este usuario el acceso a la información creada, y la posibilidad de realizar cambios sobre el mismo. Este se identifica con el parámetro «u».
- **Permisos de grupo**: Cuando un usuario pertenece a un grupo dentro del directorio de Linux, quiere decir que se le otorgan los mismos permisos que tienen los demás usuarios que pertenecen a ese mismo grupo. El sistema identifica esto con el parámetro «g».
- **Permisos del resto de usuarios:** En este caso nos referimos a los usuarios que no son los creadores del archivo, ni pertenecen al grupo que hemos indicado anteriormente. Los permisos y accesos de estos usuarios los puede establecer el propietario. El sistema los establece con el parámetro «o». Algunas técnicas que podemos usar a la hora de asignar permisos y así garantizar una mayor seguridad dentro del sistema son:
- **Implementar el principio de privilegio mínimo:** Este principio se basa en otorgar sólo los permisos necesarios para que los usuarios o grupos realicen sus tareas específicas. Evitar dar permisos innecesarios ayuda a reducir el riesgo de acceso no autorizado o cambios no deseados en los recursos.
- **Utilizar ACL (Listas de Control de Acceso)**: Las ACL permiten un mayor nivel de control sobre los permisos en Linux, ya que permiten definir permisos más detallados para usuarios y grupos específicos. Con las ACL, es posible otorgar o denegar permisos de acceso individualmente para diferentes usuarios y grupos, aumentando así la complejidad de los permisos.
- **Utilizar grupos de usuarios**: Crear grupos de usuarios y asignar permisos a esos grupos puede facilitar la administración de permisos y aumentar la complejidad. Los usuarios pueden ser miembros de diferentes grupos y, dependiendo de los permisos asignados a cada grupo, tendrán diferentes niveles de acceso a los recursos.
- **Limitar el acceso a recursos sensibles**: Es recomendable restringir el acceso a recursos sensibles, como archivos de configuración o directorios críticos del sistema, solo a usuarios o grupos autorizados. Esto se puede lograr mediante la asignación adecuada de permisos y el uso de herramientas como SELinux (Security-Enhanced Linux) para aplicar políticas de seguridad adicionales.
- **Monitorizar y auditar los cambios:** Es importante establecer mecanismos de monitorización y auditoría para realizar un seguimiento de los cambios en los permisos de los recursos. Esto ayuda a identificar posibles infracciones de seguridad o cambios no autorizados, permitiendo tomar acciones correctivas de manera oportuna.

<aside>
💡 Si queremos ver los permisos que tiene un usuario dentro de un archivo, lo podemos ver con el comando ls -l, nos mostrará los distintos tipos de permisos que tiene el directorio o el archivo.

</aside>

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image36.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image36.png)

En la siguiente imagen podemos ver como tenemos 5 directorios en los cuales los propietarios de los grupos se separan por los distintos grupos. Donde el usuario propietarios tiene privilegios completos, el grupo propietario tiene permisos de lectura y escritura y los otros usuarios solo tienen permisos de lectura

Si queremos cambiar los permisos dentro de un archivo o directorio, lo hacemos mediante el comando chmod el cual va seguido de los permisos que queremos asignar y el archivo o directorio al cual se asignaremos los permisos

Existen dos formas de asignar permisos:

### Mediante letras usando primero los roles de usuarios del sistema como:

- **u**: usuario
- **g**: grupo
- **o**: otros
- **a:** todos (all), si necesitas aplicar el mismo permiso a usuario, grupos y otros, usa «a» para ahorrar tiempo.

Luego agregamos si queremos añadir o quitar permisos

- **+:** añadir permisos
- **:** quitar permisos
- **=:** especifica los permisos fijados.

Y después colocamos los permisos que queremos asignar

1. **r:** lectura: Permite a los usuarios la lectura de un determinado archivo o directorio.
2. **w:** Escritura: Da al usuario la posibilidad de modificar el archivo sobre el cual se le han dado permisos.
3. **x**: ejecución: Otorga la posibilidad de ejecutar un archivo.

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image37.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image37.png)

En el directorio IT tenemos un archivo llamado [script.sh](http://script.sh/), el cual tiene permisos de lectura pero no de escritura ni de ejecucion para el grupo propietario , esto lo podemos cambiar usando el comando chmod y asignando los permisos

### Mediante números basados en el octal

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image38.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image38.png)

- Lectura (r), Escritura (w) Ejecución (x) rwx = 7
- Lectura (r), Escritura (w) rw- =6
- Lectura (r), Ejecución (x) r-x = 5
- Lectura (r) r– = 4
- Escritura (w), Ejecución -wx = 3
- Escritura (w) -w- = 2
- Ejecución (x) –x = 1

Podemos realizar el mismo ejercicio anterior, esta vez cambiaremos los permisos de forma octal

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image39.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image39.png)

- Otro comando que aprenderemos es el **mkdir** el cual nos permitirá crear un directorio
- **chown** nos permitirá cambiar el propietario del archivo o directorio
- chgrp nos permitirá cambiar el grupo propietario del archivo o directorio

## **Búsqueda y filtrado de archivos**

Una tarea común que nos conseguiremos en la administración de sistemas es la de la búsqueda y filtrado de archivos, a medida que los archivos en un servidor aumenta, se hace más esencial poder encontrar rápidamente los archivos que necesitamos. A través de la terminal tenemos varios comandos que nos pueden ayudar a hacer búsquedas y filtrados eficientes

- `find`

Este comando es uno de los más usados para buscar archivos y directorios en función de diferentes criterios como el nombre del archivo, tamaño, fecha de última modificación entre otros.

Por ejemplo, necesitamos encontrar todos los archivos .txt dentro de una ruta, hacemos el siguiente comando.

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image40.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image40.png)

> Otras formas de buscar con el comando find son:

- Por el tipo, si es archivo (f) o directorio (d).
- Por el tamaño del archivo.
- Por el usuario o grupo propietario.

- `Grep`

Esta es una herramienta útil para filtrar archivos en Linux es el comando "grep". A diferencia de "find", "grep" se utiliza para buscar contenido dentro de archivos en lugar de buscar archivos en sí. Puedes buscar palabras o patrones específicos en uno o varios archivos utilizando el siguiente comando:

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image41.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image41.png)

En este ejemplo, buscamos si dentro del archivo [script.sh](http://script.sh/) hay una palabra prueba. el cual nos la devuelve en el resultado.

- `locate`

Este comando utiliza una base de datos para realizar búsquedas rápidas de archivos en todo el sistema. Este comando se especialmente útil cuando necesitas buscar archivos de forma frecuente y en grandes volúmen

### **⚡️Quiz Gestion de archivos y directorios.**

1. **Que número debemos asignar si queremos otorgar estos permisos rwxrw-r–**
    - **533**
    - **764**
    - **754**
2. **Que comando usamos para conseguir un archivo por su nombre**
- **locate**
- **find -name**
- **find -type**

**3. Cual es el tipo de usuario que tendremos si somos administradores de sistemas**

- **root**
- **usuario normal**
- **usuario de ejecucion**

# **Lectura 5📕: Configuración de servicios de red:**

## **Configuración de la interfaz de red**

La interfaz de red y su configuración es una de las partes más importantes de un servidor y las labores de un administrador de sistemas, ya que con la interfaz de red podemos establecer la conectividad y permitir que el servidor se comunique con otros dispositivos en la red.

Para poder entablar una conexión con otros dispositivos lo primero que tenemos que hacer es asignarle una IP a nuestro servidor bien sea de una forma estática en la cual nosotros le asignamos la IP y la agregamos manualmente, ò dinámica donde dejamos que un servidor DHCP sea que asigne una dirección IP temporal.

La elección entre una dirección IP dinámica o estática para un servidor depende de varios factores y requisitos específicos. Aquí hay algunas consideraciones que pueden ayudarte a tomar una decisión informada:

- **Estabilidad y disponibilidad**: Si necesitas que tu servidor esté siempre disponible y accesible, una dirección IP estática puede ser más adecuada. Con una dirección IP estática, la dirección del servidor no cambiará, lo que facilita la conexión y el acceso constante.
- **Servicios y aplicaciones**: Si tu servidor aloja servicios o aplicaciones que requieren una dirección IP constante, como servidores web, bases de datos o servidores de correo electrónico, una dirección IP estática es recomendable. Esto garantiza que los clientes y usuarios siempre puedan acceder a tus servicios utilizando la misma dirección IP.
- **Seguridad:** Una dirección IP estática puede facilitar la implementación de medidas de seguridad, como el filtrado de direcciones IP o la configuración de reglas de firewall específicas. Esto puede ayudar a proteger tu servidor y los servicios que ofrece
- **Flexibilidad y movilidad:** Si necesitas flexibilidad para cambiar la ubicación física de tu servidor o si tu proveedor de servicios de Internet (ISP) requiere el uso de direcciones IP dinámicas, una dirección IP dinámica puede ser más conveniente. Las direcciones IP dinámicas se asignan automáticamente y pueden cambiar con el tiempo.

Después de estas consideraciones podemos indicar que la mejor configuración de IP es estática para nuestro servidor, para lograr esta configuración hacemos los siguientes pasos.

Usamos el comando `ifconfig` para conocer cuál es nuestra interfaz de red.

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image42.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image42.png)

lo podemos identificar como la primera interfaz que tenemos del resultado “enp0s3”

Generalmente en las distribuciones debian, las interfaces de red se configuraban a través del archivo **/etc/network/interfaces**, en el caso de ubuntu, desde la version 17.10, se cambio las configuraciones de la interfaz de red a la utilidad netplan, el cual genera un archivo YAML para facilitar la configuraciones de red. Accederemos a este archivo con un editor de código a la ruta `/etc/netplan/00-installer-config-yaml`

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image43.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image43.png)

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image44.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image44.png)

Asignamos una `IP 192.168.1.10` a nuestro servidor y el resto de las configuraciones.

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image45.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image45.png)

Ya una vez asignado los valores, aplicamos el comando

**`netplan apply`**

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image46.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image46.png)

Corroboramos que nuestra IP ya sea la que le asignamos y listo, ya tenemos la interfaz de red de nuestros servidores configurada.

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image47.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image47.png)

## **Configuración de la resolución de nombres (DNS)**

Otra configuración esencial para la conexión de la red es la configuración de la DNS (Domain Name System), recordemos que este protocolo es el encargado de traducir los nombres de los dominios que utilizamos en nuestro navegador como por ejemplo [www.google.com](http://www.google.com/) en las direcciones IP de los servidores web de que queremos acceder.

Este proceso se da cuando ingresamos una dirección web en nuestro navegador, éste envía una solicitud a un servicio DNS para obtener la dirección IP asociada a ese nombre del dominio, el servidor DNS busca en su base de dato devuelve la dirección IP correspondiente, permitiendo que el navegador establezca una conexión con el servidor web que aloja el sitio.

Además de su función principal de traducción de nombres de dominio, las DNS también desempeñan un papel importante en la seguridad y la optimización de la navegación. Por ejemplo, las DNS pueden implementar medidas de seguridad, como el filtrado de contenido malicioso o la detección de sitios web fraudulentos, ayudando a proteger a los usuarios de posibles amenazas en línea.

Es importante tener configurado la DNS de nuestro servidor ya que es el que nos va a permitir que los usuarios accedan a los servicios y aplicaciones alojados en el servidor mediante los nombres del dominio, aparte también se utiliza para redireccionar el tráfico a diferentes servidores en función de la carga o la disponibilidad. Esto permite distribuir la carga de trabajo entre varios servidores y garantizar un rendimiento óptimo.

La DNS también desempeña un papel importante en la seguridad de un servidor al implementar medidas de seguridad en la configuración de la DNS, como el filtrado de contenido malicioso o la detección de sitios web fraudulentos, se puede proteger al servidor y a los usuarios de posibles amenazas en línea.

Para configurar la DNS de nuestro servidor Ubuntu repetiremos el mismo proceso que hicimos al configurar nuestra IP estática ingresando a la ruta **/etc/netplan/00-installer-config.yaml** desde un editor de código.

De acuerdo a la documentación de netplan la forma de agregar nuestras DNS es a través del valor

**nameservers:**

Ya que estamos trabajando con un servidor, la DNS principal que usaremos sera la misma IP de nuestro servidor, la alternativa sera una DNS publica

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image48.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image48.png)

Les dejamos una lista de DNS públicas que pueden usar para la red

| Nombre DNS | IP principal | IP alternativa |
| --- | --- | --- |
| Cloudflare | 1.1.1.1 | 1.0.0.1 |
| OpenDNS | 208.67.222.222 | 208.67.220.220 |
| Google | 8.8.8.8 | 8.8.4.4 |

Para esta configuración usaremos la DNS google

Una vez editado el archivo YAML aplicamos el comando netplan apply

Si queremos corroborar que tenemos conexion, usamos el comando ping junto a nuestro servidor alternativo

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image49.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image49.png)

## **Configuración de servicios de red**

Cuando hablamos de los servicios de red en los referimos hablamos de las aplicaciones que se ejecutan en un segundo plano, habilitando ciertas capacidades cuando sean necesarias, estas aplicaciones son componentes fundamentales que permiten la comunicación y el intercambio de información en una red.

Uno de los servicios de red más comunes en servidores Linux es el servidor web, que permite alojar y entregar páginas web a través del protocolo HTTP. El servidor web más popular en Linux es Apache, aunque también existen otras opciones como Nginx. Estos servidores web permiten a los usuarios acceder a sitios web y aplicaciones en línea, brindando una experiencia de navegación fluida y segura

Vamos a configurar nuestro servidor HTTP con Apache aplicando los siguientes pasos:

- Instalamos Apache habiendo actualizando los paquetes locales previamente con **sudo apt update.**
- Una vez actualizados los paquetes instalamos nuestro servidor apache **sudo apt install apache2.**
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image50.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image50.png)
    
- Antes de probar apache, es necesario modificar unos ajustes de firewall para permitir acceso externo a los puertos web predeterminados, durante la instalación, Apache se registra con UFW para proporcionar algunos perfiles de aplicaciones que pueden utilizarse para habilitar o deshabilitar el acceso a Apache a través del firewall.
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image51.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image51.png)
    
- Con el comando sudo ufw app list tendremos una lista de los perfiles de aplicación.
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image52.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image52.png)
    
    En el resultado tendremos tres perfiles disponibles para Apache.
    
    - **Apache**: este perfil abre solo el puerto 80 (tráfico web normal no cifrado)
    - **Apache Full**: este perfil abre el puerto 80 (tráfico web normal no cifrado) y el puerto 443 (tráfico TLS/SSL cifrado)
    - **Apache Secure**: este perfil abre solo el puerto 443 (tráfico TLS/SSL cifrado)
    - Habilitamos el perfil más restrictivo el cual sería Apache permitiendo el tráfico en el puerto 80 (puerto http)

### sudo ufw allow “Apache”

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image53.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image53.png)

Podemos corroborar los cambios usando el comando sudo ufw status

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image54.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image54.png)

En algunos casos podemos tener una respuesta de Status: Inactive, esto ocurre porque el firewall está inactivo, para activarlo usamos el comando sudo ufw enable, y volvemos a chequear el status

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image55.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image55.png)

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image56.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image56.png)

- Ya una vez habiendo permitido el tráfico al puerto HTTP revisamos el estatus de nuestro servidor con el comando sudo systemctl status apache2

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image57.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image57.png)

Podemos ver que su estado es activo y corriendo.

- Otra forma de comprobar que nuestro servidor está activo es haciendo una solicitud de página, si no estamos seguro de la dirección IP de nuestro servidor, usamos el comando hostname -I y nos devolverá la IP la cual abriremos en un navegador web para comprobar que esté activo.

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image58.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image58.png)

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image59.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image59.png)

Otro de los servicios necesarios para nuestro servidor es el FTP (File Transfer Protocol) el cual lo usamos como un medio para enviar recibir archivos a través de una conexion de red usando un marco de referencia de cliente/servidor y seguridad SSL/TLS que permite a los usuarios compartir archivos y recibir desde computadoras remotas a través de una transferencia de datos segura, eficiente y confiable.

FTP funciona de la misma manera que HTTP(HypertText Transfer Protocol) o SMTP(Simple Mail Transfer Protocol). La diferencia es que el FTP se encarga de transportar archivos a través de Internet, mientras que el HTTP y el SMTP se encargan de transferir páginas web y correos electrónicos, respectivamente.

Para instalar este servicio en nuestro servidor podemos seguir los siguientes pasos:

- Antes de instalar nuestro servicio, lo recomendable es actualizar nuestro sistema operativo con sudo apt update y sudo apt upgrade.

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image60.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image60.png)

- Procederemos a instalar vsftpd (Very Secure FTP Daemon por sus siglas en inglés) el cual es un servidor FTP para los sistemas tipo unix incluido Linux, este lo haremos con el comando sudo apt install vsftpd

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image61.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image61.png)

- Una vez completada la instalación, tendremos que editar el archivo de configuración, lo recomendable en estos casos es crear una copia de seguridad del archivo original para así comenzar la configuración en blanco si cometemos algún error

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image62.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image62.png)

- Ya configurado el tenemos la copia creada comenzamos a permitir el trafico FTP desde el firewall usando los siguientes comandos

      `sudo ufw allow 20/tcp`

`sudo ufw allow 21/tcp`

`sudo ufw allow 990/tcp`

`sudo ufw allow 40000:50000/tcp`

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image63.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image63.png)

Estos comandos abrirán varios puertos

- **OpenSSH** es necesario si todavía quieres acceder a tu servidor a través de SSH. A veces, esta opción está activada por defecto.
- los puertos **20** y **21** para el tráfico FTP.
- los puertos **40000:50000** se reservarán para el rango de puertos pasivos que eventualmente se establecerá en el archivo de configuración.
- el puerto **990** se utilizará cuando se active el TLS.

**Ya una vez agregadas las reglas revisamos el estatus del firewall**

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image64.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image64.png)

- Abrimos el archivo **/etc/vsftpd.conf** con el editor de codigo de nuestra elección y ya dentro del archivo habilitamos la opcion
- write_enable=yes eliminando el **#,**
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image65.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image65.png)
    
- Agregamos unos valores nuevos al final del archivo. En primer lugar, se agregará un user_sub_token en la ruta del directorio local_root. Esto permitirá que la configuración funcione con el usuario actual y con cualquier otro usuario que se agregue posteriormente:
- user_sub_token=$USER
    
    local_root=/home/$USER/ftp
    

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image66.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image66.png)

- Para garantizar que haya una cantidad considerable de conexiones disponibles, limitaremos la cantidad de puertos utilizados en el archivo de configuración:
- pasv_min_port=40000
    
    pasv_max_port=50000
    
- Ya una vez hecho estos cambios cerramos el archivo y agregamos a nuestro usuario en la lista de usuarios del servicio ftp y comprobamos que este agregado adecuadamente

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image67.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image67.png)

- Por último reiniciamos el servicio vsftpd

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image68.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image68.png)

<aside>
📖 En este módulo hemos aprendido como configurar dos servicios muy importantes para administrar un servidor como lo son HTTP y FTP, existen muchos otros que puedes investigar y poner en práctica dentro de tu máquina virtual, anímate, la práctica hace al maestro.

</aside>

### **⚡️QUIZ Configuración de servicios de red:**

- **¿Cómo se llama el archivo donde configuraremos nuestra IP de forma estática?**
    1. etc/network/interfaces
    2. /etc/netplan/00-installer-config.yaml
    3. /etc/netwokrs.conf
- **¿Cuál será el servidor DNS principal que tenemos que usar?**
    1. 1.1.1.1
    2. 8.8.8.8
    3. IP de la máquina
- **¿Cuál es el servicio que nos permitirá transferir archivos via internet?**
    1. ftp
    2. http
    3. smtp

# **Lectura 6 📕: Gestión de paquetes y software**

## **Uso de gestores de paquetes para la instalación y actualización de software**

Hemos hablado previamente sobre el uso de gestores de paquetes y cómo nos pueden ayudar a instalar aplicaciones y actualizar software, recordemos que en el entorno de los servidores Linux, los gestores de paquetes son herramientas fundamentales para la gestión eficiente del software ya que simplifican la instalación, actualización y eliminación de paquetes de software en un servidor, lo que resulta esencial para mantener el sistema actualizado y seguro.

Uno de los gestores de paquetes más populares en servidores Linux es apt-get, utilizado en distribuciones basadas en Debian y Ubuntu. Con apt-get, los administradores de sistemas pueden instalar software fácilmente utilizando comandos simples. Por ejemplo, para instalar un paquete llamado "nombre_paquete", solo necesitas ejecutar el comando "sudo apt-get install nombre_paquete". El gestor de paquetes se encargará de descargar e instalar el paquete, así como de resolver las dependencias necesarias.

Otro gestor de paquetes común en servidores Linux es yum, ya que es utilizado en distribuciones como Red Hat y CentOS. Al igual que apt-get, yum permite instalar, actualizar y eliminar paquetes de software de manera sencilla. Para instalar un paquete con yum, puedes ejecutar el comando "sudo yum install nombre_paquete". Yum también se encargará de manejar las dependencias y garantizar una instalación exitosa.

Además de apt-get y yum, existen otros gestores de paquetes populares en servidores Linux, como zypper (utilizado en openSUSE), dnf (utilizado en Fedora) y pacman (utilizado en Arch Linux). Cada gestor de paquetes tiene su propia sintaxis y comandos específicos, pero todos comparten el objetivo de simplificar la gestión del software en un servidor Linux.

Una de las ventajas clave de utilizar gestores de paquetes en servidores Linux es la capacidad de mantener el software actualizado de manera sencilla. Con un simple comando, como "sudo apt-get update" en apt-get o "sudo yum update" en yum, puedes verificar si hay actualizaciones disponibles para los paquetes instalados en el servidor. Luego, puedes ejecutar "sudo apt-get upgrade" o "sudo yum upgrade" para instalar las actualizaciones. Esto garantiza que el software esté actualizado y protegido contra vulnerabilidades conocidas.

Además, los gestores de paquetes en servidores Linux también permiten la eliminación de software de manera eficiente. Si ya no necesitas un paquete, puedes utilizar el comando correspondiente para desinstalarlo. Por ejemplo, "sudo apt-get remove nombre_paquete" en apt-get o "sudo yum remove nombre_paquete" en yum. Esto asegura una limpieza adecuada del sistema y evita la acumulación de software innecesario.

En nuestro servidor ubuntu probaremos nuestro gestor de paquete de software actualizando e instalando un software.

1. Primero usaremos el comando sudo apt update que se encargara de traer todas las aplicaciones que tengamos en el sistema.

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image69.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image69.png)

1. Una vez actualizado los paquetes, procedemos instalar las actualizaciones con el comando sudo apt upgrade.

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image70.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image70.png)

Para la instalación de software instalamos samba, que es un software que implementa el protocolo SMB y permite compartir archivos e impresoras con cualquier otro dispositivo que esté en la red.

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image71.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image71.png)

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image72.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image72.png)

<aside>
🤓 Como práctica les dejamos que investiguen como configurar el servicio samba

</aside>

## **Búsqueda y eliminación de paquetes.**

La búsqueda y eliminación de paquetes en Linux es una tarea común para los administradores de sistemas ya que a veces, es necesario encontrar un paquete específico o eliminar uno que ya no se necesita, afortunadamente, Linux cuenta con herramientas poderosas que facilitan estas tareas.

Para buscar paquetes en Linux, puedes utilizar el gestor de paquetes específico de tu distribución. Por ejemplo, en distribuciones basadas en Debian y Ubuntu, como Ubuntu puedes utilizar el comando "apt-cache search término_de_búsqueda" con el gestor de paquetes apt-get. Esto buscará en los repositorios disponibles y mostrará una lista de paquetes que coincidan con el término de búsqueda. Puedes refinar la búsqueda utilizando expresiones regulares o palabras clave más específicas.

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image73.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image73.png)

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image74.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image74.png)

En distribuciones como Red Hat y CentOS, que utilizan el gestor de paquetes yum, puedes utilizar el comando "yum search término_de_búsqueda" para buscar paquetes. Al igual que con apt-get, esto mostrará una lista de paquetes que coincidan con el término de búsqueda en los repositorios disponibles.

Además de los gestores de paquetes, también puedes utilizar herramientas adicionales para buscar paquetes en Linux. Por ejemplo, puedes utilizar el comando "dpkg -l | grep término_de_búsqueda" en distribuciones basadas en Debian para buscar paquetes instalados localmente. Esto mostrará una lista de paquetes que coincidan con el término de búsqueda.

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image75.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image75.png)

Una vez que hayas encontrado el paquete que deseas eliminar, puedes utilizar el gestor de paquetes correspondiente para eliminarlo. En distribuciones basadas en Debian y Ubuntu, puedes utilizar el comando "sudo apt-get remove nombre_paquete" con apt-get. Esto eliminará el paquete y todos sus archivos asociados del sistema.

En distribuciones como Red Hat y CentOS, puedes utilizar el comando "sudo yum remove nombre_paquete" con yum para eliminar un paquete. Al igual que con apt-get, esto eliminará el paquete y sus archivos asociados.

Si deseas eliminar completamente un paquete, incluidos los archivos de configuración, puedes utilizar el comando "sudo apt-get purge nombre_paquete" en distribuciones basadas en Debian y Ubuntu, o "sudo yum remove nombre_paquete" en distribuciones como Red Hat y CentOS.

Es importante tener en cuenta que al eliminar un paquete, es posible que se eliminen también otros paquetes que dependan de él. El gestor de paquetes te informará sobre los cambios que se realizarán antes de proceder con la eliminación.

## **Configuración de repositorios de software**

Saber cómo configurar los repositorios de software es otro de los conocimientos que deben tener los administradores de sistema ya que recordemos que los repositorios son lugares centralizados donde se almacenan los paquetes de software, y configurarlos correctamente permite acceder a una amplia variedad de software de manera fácil y segura.

En sistemas operativos como Linux, los repositorios de software son especialmente importantes, estos repositorios contienen paquetes de software precompilados y listos para ser instalados en el sistema. Al configurar los repositorios adecuados, los administradores de sistemas pueden acceder a una gran cantidad de software y mantenerlo actualizado de manera sencilla.

La configuración de repositorios varía según la distribución de Linux que estés utilizando. Por ejemplo, en distribuciones basadas en Debian y Ubuntu, la configuración de repositorios se realiza a través del archivo "/etc/apt/sources.list". Este archivo contiene las URL de los repositorios y los componentes que se deben habilitar, como "main", "universe", "restricted" y "multiverse". Al editar este archivo y agregar o modificar las URL de los repositorios, puedes configurar los repositorios de software que deseas utilizar.

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image76.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image76.png)

En distribuciones como Red Hat y CentOS, la configuración de repositorios se realiza a través de archivos ubicados en el directorio "/etc/yum.repos.d/". Estos archivos contienen información sobre los repositorios, como la URL base, los componentes habilitados y las claves de autenticación. Al crear o modificar estos archivos, puedes configurar los repositorios de software que deseas utilizar en tu sistema.

Es importante tener en cuenta que al configurar repositorios de software, es fundamental utilizar fuentes confiables y seguras. Los repositorios oficiales de las distribuciones son generalmente los más confiables, ya que son mantenidos por los desarrolladores y se someten a pruebas rigurosas. Sin embargo, también existen repositorios de terceros que pueden ofrecer software adicional. Al utilizar repositorios de terceros, es importante investigar y asegurarse de que sean confiables y estén bien mantenidos.

Una vez que hayas configurado los repositorios de software, puedes utilizar los gestores de paquetes correspondientes, como apt-get o yum, para acceder a los paquetes disponibles en los repositorios. Estos gestores de paquetes se encargará de descargar e instalar el software de manera eficiente, resolviendo automáticamente las dependencias necesarias.

### **⚡️Quiz Gestión de paquetes y software**

1. **Cual es el gestor de paquetes para las distribuciones debian y ubuntu?**
    1. **apt**
    2. **yum**
    3. **pacman**
2. **Cual es el comando usado para buscar un paquete disponible en ubuntu server?**
    1. **apt install**
    2. **apt cache search**
    3. **apt remove**
3. **Cual es la ruta que tenemos usar para configurar los repositorios**
    1. **/etc/network/interfaces**
    2. **/etc/apt/sources.list**
    3. **/etc/apt/apt.conf.d**
    

# **Lectura 7 📕: Configuración de seguridad del servidor**

## **Configuración del firewall**

Los firewall son una pieza clave en la seguridad de nuestros servidores, por lo que como administradores de sistemas es necesario que sepamos cómo configurarlo. Recordemos que un firewall actúa como una barrera entre tu servidor y posibles amenazas externas, controlando el tráfico de red y permitiendo o bloqueando conexiones según las reglas establecidas.

En Linux, uno de los firewalls más utilizados es iptables, que es una herramienta de filtrado de paquetes integrada en el kernel del sistema operativo. Sin embargo, iptables puede resultar complejo de configurar debido a su sintaxis y reglas. Por esta razón, muchas distribuciones de Linux han adoptado herramientas de administración de firewall más amigables, como UFW (Uncomplicated Firewall) en Ubuntu y CentOS, o firewalld en Fedora.

Para configurar un firewall utilizando UFW, puedes utilizar comandos sencillos que simplifican el proceso. Por ejemplo, para permitir el tráfico SSH en tu servidor, puedes ejecutar el comando "sudo ufw allow ssh". Esto abrirá el puerto 22, que es el puerto predeterminado para SSH, y permitirá las conexiones entrantes.

Además de permitir conexiones específicas, también puedes bloquear puertos no deseados utilizando UFW. Por ejemplo, para bloquear el tráfico en el puerto 80, puedes ejecutar el comando "sudo ufw deny 80". Esto evitará que cualquier conexión entrante o saliente utilice el puerto 80.

Otra herramienta comúnmente utilizada para la configuración de firewall en Linux es firewalld. Firewalld proporciona una interfaz de línea de comandos y una interfaz gráfica para administrar las reglas de firewall. Puedes utilizar comandos como "**sudo firewall-cmd --add-service=ssh**" para permitir el tráfico SSH, o "**sudo firewall-cmd --remove-service=http**" para eliminar una regla existente.

Además de permitir o bloquear puertos específicos, tanto UFW como firewalld permiten configurar reglas más avanzadas, como el filtrado por dirección IP, el enmascaramiento de direcciones o la limitación de conexiones simultáneas. Estas características adicionales te permiten personalizar aún más la configuración de tu firewall según tus necesidades específicas.

<aside>
📖 Es importante tener en cuenta que, al configurar un firewall, es fundamental comprender las implicaciones de las reglas establecidas. Configurar un firewall de manera incorrecta puede bloquear conexiones legítimas o permitir el acceso no autorizado. Por lo tanto, es recomendable tener un buen conocimiento de las reglas y realizar pruebas exhaustivas antes de implementar un firewall en un entorno de producción.

</aside>

Para esta práctica configuraremos ambos, UFW:

Instalación de UFW:

1. El primer paso será actualizar los paquetes del sistema con sudo apt update y sudo apt upgrade.

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image77.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image77.png)

1. Una vez actualizamos, procedemos a instalar nuestro firewall con el comando **sudo apt install UFW**
2. Validamos el status actual del firewall con el comando **sudo ufw status**
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image78.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image78.png)
    
3. Podemos ver que el firewall está inactivo o deshabilitado por lo que el siguiente paso será habilitarlo.
4. Habilitamos el firewall con el comando **sudo ufw enable**
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image79.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image79.png)
    

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image80.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image80.png)

1. Una vez colocado el comando, revisamos nuevamente su status con sudo ufw status

**Si queremos desactivar el firewall usamos el comando sudo ufw disable**

1. Configuramos las políticas en el firewall, por defecto, UFW tiene reglas para negar todas las conexiones entrantes y solo permite las conexiones salientes al servidor, por lo que nadie podría acceder al servidor y los servicios o aplicaciones en ejecución, estas reglas podemos conseguirlas dentro de la ruta.
2. Para editar las reglas usamos los comandos **sudo ufw default deny incoming** y **sudo ufw default allow outgoing.**
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image81.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image81.png)
    
    <aside>
    👉 Cuando instalamos un paquete a través de nuestro gestor APT, se incluye un perfil de aplicación en el directorio /etc/ufw/applications.d el cual define el servicio y mantiene la configuración de UFW activa.
    
    </aside>
    
3. Para enumerar todos los perfiles de aplicaciones usamos el comando **sudo ufw app list** 
Si queremos obtener más información sobre un perfil en específico y las reglas definidas para este, usamos el comando **sudo ufw app info “Aplicación”.**
4. El siguiente paso habilitar los servicios o puertos que queramos permitir en el firewall.
- Si queremos permitir servicios como SSH para conectarnos de forma remota usamos el comando **sudo ufw allow ssh**, en el caso que queramos usar un puerto SSH personalizado, usamos el comando **sudo ufw allow puerto** y si deseamos bloquear una conexión ssh usamos el comando **`sudo ufw deny ssh/tcp`.**
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image82.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image82.png)
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image83.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image83.png)
    
- Si queremos permitir el acceso de aplicaciones que unsam un rango de puertos, usamos el comando **`sudo ufw allow puertoInicial:puertoFinal.`**
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image84.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image84.png)
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image85.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image85.png)
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image86.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image86.png)
    
1. También tenemos la opción de permitir acceso de una sola dirección IP de sistema, para ello ejecutamos el comando **sudo ufw allow from direccionIP,** también podemos especificar que queremos recibir el tráfico de un puerto en especifico **sudo ufw allow direccionIP to any port “numeroPuerto”**
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image87.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image87.png)
    
- Si queremos eliminar las reglas del firewall lo primero que tenemos que hacer es enumerar las reglas con el comando **sudo ufw status numbered** y luego eliminamos la regla usando el comando sudo ufw delete numeroRegla, otra forma sería con el comando **sudo ufw delete reglaUFW.**
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image88.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image88.png)
    

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image89.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image89.png)

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image90.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image90.png)

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image91.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image91.png)

## **Gestión de usuarios y autenticación segura**

Hemos hablado previamente de la gestión y autenticación segura de usuarios en Linux, estas prácticas garantizan la seguridad y protección de los sistemas, evitando accesos no autorizados y protegiendo la información confidencial.

En Linux, cada usuario tiene una cuenta única que le permite acceder al sistema y realizar tareas específicas. La gestión de usuarios implica la creación, modificación y eliminación de estas cuentas de usuario.

Para crear un nuevo usuario en Linux, puedes utilizar el comando `useradd` seguido del nombre de usuario deseado. Por ejemplo, `sudo useradd nombre_usuario` creará una nueva cuenta de usuario en el sistema. Luego, puedes establecer una contraseña para el usuario utilizando el comando `passwd nombre_usuario`. Es importante utilizar contraseñas seguras que combinen letras mayúsculas y minúsculas, números y caracteres especiales.

Además de crear usuarios, también es importante asignarles los permisos adecuados. En Linux, los permisos se gestionan a través del sistema de archivos y los grupos de usuarios. Puedes utilizar comandos como "`chown`" y "`chmod`" para cambiar la propiedad y los permisos de los archivos y directorios.

La autenticación segura es otro aspecto crucial en la gestión de usuarios en servidores Linux. El uso de contraseñas seguras es solo el primer paso. También se recomienda utilizar autenticación de dos factores (2FA) para agregar una capa adicional de seguridad. Esto implica el uso de un segundo método de autenticación, como un código generado por una aplicación en el teléfono móvil, junto con la contraseña tradicional.

Además, es importante asegurarse de que los servicios de autenticación, como SSH (Secure Shell), estén configurados correctamente. Puedes modificar la configuración de SSH en el archivo "/etc/ssh/sshd_config" para permitir sólo conexiones seguras y deshabilitar el acceso de root remoto.

<aside>
👉 Otra práctica recomendada es utilizar claves de autenticación en lugar de contraseñas para acceder a los servidores. Esto implica generar un par de claves pública y privada, donde la clave privada se almacena en el cliente y la clave pública se agrega al archivo "~/.ssh/authorized_keys" en el servidor. Esto permite una autenticación sin contraseña y es más seguro que el uso de contraseñas.

</aside>

Para configurar nuestra clave pública y privada para autenticarnos dentro del servidor seguimos los siguientes pasos:

1. Creamos nuestras claves pública y privada con el comando ssh-keygen, despues nos pedira la ruta donde almacenar nuestra clave SSH, podemos aceptar la ruta que nos da por defecto, despues pedira una frase de contraseña la cual agrega una capa de seguridad adicional para evitar el inicio de sesión de usuarios no autorizados.
2. El próximo paso será copiar la clave pública al nuestro servidor, para ello usaremos la herramienta ssh-copy-id con el siguiente comando **`ssh-copy-id username@remote_host`.**
3. Procedemos a conectarnos a nuestro usuario ssh con el comando **ssh usuario@hostname** una vez introducido el comando, pedirán la frase de autenticación, la autenticación basada en claves se realizó con éxito, podemos proteger más a nuestro sistema inhabilitando la autenticación con contraseña.
4. Aunque tengamos la cuenta SSH configurada, el mecanismo de autenticación basado en contraseña sigue activo, por lo que vamos a hacer un cambio en el archivo ubicado en la ruta /etc/ssh/sshd_config con nuestro editor de código.
5. Ubicamos la directiva PasswordAuthentication y la activamos quitándole el #, nos aseguramos que el valor de la directiva sea no.
6. Reiniciamos el servicio ssh con el comando systemctl restart ssh

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image92.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image92.png)

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image93.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image93.png)

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image94.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image94.png)

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image95.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image95.png)

## **Configuración de registros de auditoría (logs) del sistema.**

La configuración de registros de auditoría, también conocidos como logs, es una práctica esencial en la administración de sistemas para monitorear y registrar eventos importantes del sistema operativo y las aplicaciones. Estos registros proporcionan información valiosa para el análisis de problemas, la detección de intrusiones y el seguimiento de actividades en el sistema.

En Linux, los registros de auditoría se encuentran en el directorio "/var/log" y contienen información detallada sobre diversos aspectos del sistema, como el inicio y apagado del sistema, errores del kernel, actividades de red, registros de aplicaciones y mucho más.

La configuración de los registros de auditoría se realiza a través del archivo de configuración del demonio de registro, que puede variar según la distribución de Linux utilizada. En distribuciones como Ubuntu y Debian, el archivo de configuración principal es "/etc/rsyslog.conf", mientras que en distribuciones como Red Hat y CentOS, se utiliza "/etc/rsyslog.d/*.conf" para configurar los registros.

En estos archivos de configuración, puedes especificar qué eventos deseas registrar y dónde deseas almacenar los registros. Puedes definir reglas para filtrar eventos específicos, establecer niveles de registro (como información, advertencia o error) y redirigir los registros a archivos específicos o enviarlos a un servidor de registro centralizado.

<aside>
⚠️ Es importante tener en cuenta que la configuración de los registros de auditoría debe equilibrar la cantidad de información registrada con la capacidad de almacenamiento disponible. Registrar demasiados eventos puede llenar rápidamente el espacio en disco y dificultar el análisis de los registros. Por otro lado, registrar muy pocos eventos puede dejar pasar información importante para la detección de problemas o actividades sospechosas.

</aside>

Además de la configuración de los registros de auditoría, es importante monitorear y analizar regularmente los registros para identificar posibles problemas o actividades maliciosas. Puedes utilizar herramientas como "grep" o "awk" para buscar eventos específicos en los registros, o utilizar herramientas de monitoreo y análisis de registros más avanzadas, como "Logstash" o "Splunk".

### **⚡️Quiz Configuración de seguridad del servidor**

1. **Estamos instalando el firewall de nuestro servidor y queremos permitir el tráfico de SSH, ¿cual comando usaremos?**
    1. **sudo ufw open ssh**
    2. **sudo ufw ssh**
    3. **sudo ufw allow ssh**
2. **¿En la configuración de nuestro usuario ssh que sustituirá nuestra clave de seguridad?**
    1. **frase de seguridad**
    2. **clave alfanumérica**
    3. **comando ssh**
3. **¿Cuál es la importancia de ver los logs del sistema?**
    1. **Poder ver información del hardware del sistema**
    2. **Poder ver información sobre eventos del sistema operativo**
    3. **Poder ver datos de nuestro servidor.**
    

# **📕 Lectura 8: Programación de tareas automatizadas**

## **Uso de cron para programar tareas**

Cron es una herramienta muy útil en sistemas operativos Linux que permite programar tareas para que se ejecuten automáticamente en momentos específicos. Con cron, puedes automatizar tareas repetitivas, como realizar copias de seguridad, actualizar bases de datos, enviar informes por correo electrónico y mucho más.

La configuración de tareas en cron se realiza a través de archivos llamados "crontabs". Cada usuario puede tener su propio crontab, que contiene las tareas programadas para ese usuario en particular. Para editar el crontab de un usuario, puedes utilizar el comando `crontab -e`.

El formato de un crontab consta de cinco campos separados por espacios: minutos, horas, día del mes, mes y día de la semana. Puedes utilizar números o asteriscos (*) para indicar todos los valores posibles en un campo. Por ejemplo, si deseas que una tarea se ejecute todos los días a las 8:00 a.m., puedes configurar el crontab de la siguiente manera: "0 8 * * * comando".

Además de los valores numéricos, también puedes utilizar expresiones especiales en los campos de tiempo. Por ejemplo, "@daily" se traduce en "0 0 * * *", lo que significa que la tarea se ejecutará todos los días a la medianoche. Otras expresiones útiles incluyen "@hourly", "@weekly" y "@monthly".

Estas expresiones se traducen de esta manera:

@reboot: Ejecuta una vez y nada más iniciarse el equipo.

1. @yearly: ejecuta sólo una vez al año: 0 0 1 1 *
2. @monthly: ejecuta una vez al mes y el primer día: 0 0 1 * *
3. @weekly: todas las semanas, el primer minuto de la primera hora de la semana: 0 0 * * 0.
4. @daily: todos los días a las 12 de la noche: 0 0 * * *
5. @midnight: Tiene el mismo efecto que el anterior.
6. @hourly: todas las horas durante su primer minuto: 0 * * * *

También podemos utilizar algunos modificadores, que son algunos caracteres especiales los cuales nos dan mucho más poder de crear nuevas reglas. Lo cual aumenta las posibilidades para poder crear procesos mucho más complejos, y como tal más precisos. Estos son:

1. : Tiene el mismo significado que asignar todos los valores.
2. ,: Nos da un listado de valores.
3. : Establece un rango de valores.
4. /: Significa «cada».
5. rango / excep: Crea excepciones en la regla.

<aside>
⚠️ Es importante tener en cuenta que las tareas programadas en cron se ejecutan en el contexto del usuario que las programó. Por lo tanto, asegúrate de que el usuario tenga los permisos adecuados para realizar las tareas programadas.

</aside>

Además, es recomendable redirigir la salida de las tareas programadas a archivos de registro para poder verificar su ejecución y detectar posibles errores. Puedes hacer esto agregando ">> ruta_del_archivo" al final de la línea de comando en el crontab.

Para listar las tareas programadas en un crontab, puedes utilizar el comando "crontab -l". Si deseas eliminar todas las tareas programadas de un crontab, puedes utilizar el comando "crontab -r".

Esto nos ayudará a programar tareas que pueden resultar repetitivas, por lo cual los administradores de sistema pueden estar pendientes de otras cosas. Estos proporcionan una forma muy eficiente de programar la ejecución de diferentes scripts, comandos y también programas. Debido al alto grado de personalización, podremos programar prácticamente lo que sea necesario y sea beneficioso para la organización y las tareas que se realizan en su entorno.

Estos sistemas ofrecen varias ventajas a nivel empresarial. La primera es la que comentamos, la capacidad de programar esas tareas más tediosas para que no sea necesaria la intervención manual. Lo cual ahorra tiempo, y reduce el riesgo de que aparezcan posibles errores relacionados con errores humanos. Algunos de los métodos más comunes son para copias de seguridad, actualizaciones de software, generar informes o la ejecución de procesos de mantenimiento. Pero a todo esto también le sumamos la flexibilidad para la programación. Todos los beneficios que hemos visto previamente de cron y crontab, los tendremos disponibles a nivel empresarial. Por lo cual las opciones para crear este tipo de automatizaciones son muy abundantes.

## **Creación y edición de archivos crontab**

La creación y edición de archivos crontab es una tarea común en sistemas Unix y Linux para programar tareas que se ejecutarán automáticamente en momentos específicos. Un archivo crontab contiene las instrucciones para el cron daemon sobre qué tareas ejecutar y cuándo hacerlo.

Para crear o editar un archivo crontab, puedes utilizar el comando "crontab -e". Esto abrirá el archivo crontab en el editor de texto predeterminado del sistema, como vi o nano. Si es la primera vez que utilizas "crontab -e", se te pedirá que elijas un editor.

El archivo crontab tiene un formato específico que consta de cinco campos separados por espacios: minutos, horas, día del mes, mes y día de la semana. Cada campo acepta valores numéricos o caracteres especiales. Por ejemplo, si deseas que una tarea se ejecute todos los días a las 8:00 a.m., puedes agregar la siguiente línea al archivo crontab:

**Copy**

`0 8 * * * comando`

En esta línea, "0" representa los minutos (en este caso, 0), "8" representa las horas (8:00 a.m.), y los asteriscos (*indican que cualquier valor es válido para los campos restantes.

Además de los valores numéricos, también puedes utilizar expresiones especiales en los campos de tiempo. Por ejemplo, "@daily" se traduce en "0 0 * * *", lo que significa que la tarea se ejecutará todos los días a la medianoche. Otras expresiones útiles incluyen "@hourly", "@weekly" y "@monthly".

Después de especificar el tiempo, debes agregar el comando que deseas ejecutar. Puede ser cualquier comando válido en el sistema, como un script, un programa o una secuencia de comandos. Asegúrate de proporcionar la ruta completa del comando si es necesario.

Es importante tener en cuenta que cada línea en el archivo crontab representa una tarea programada. Puedes agregar múltiples líneas para programar varias tareas. Cada línea debe terminar con un salto de línea.

Una vez que hayas terminado de editar el archivo crontab, guarda los cambios y cierra el editor. El cron daemon se encargará de leer y ejecutar las tareas programadas según lo especificado en el archivo crontab.

Para listar las tareas programadas en un archivo crontab, puedes utilizar el comando "crontab -l". Si deseas eliminar todas las tareas programadas de un archivo crontab, puedes utilizar el comando `crontab -r`.

Recuerda que las tareas programadas en un archivo crontab se ejecutan en el contexto del usuario que las programó. Asegúrate de que el usuario tenga los permisos adecuados para realizar las tareas programadas.

## **Monitoreo y verificación de tareas programadas**

El monitoreo y la verificación de tareas programadas son aspectos importantes en la administración de sistemas para asegurarse de que las tareas se estén ejecutando correctamente y en los momentos deseados. Esto te permite detectar y solucionar problemas potenciales, así como garantizar la eficiencia y confiabilidad del sistema.

Una forma común de monitorear las tareas programadas es revisar los registros o logs generados por el sistema. Los registros de cron, por ejemplo, proporcionan información detallada sobre la ejecución de las tareas programadas. Puedes encontrar estos registros en el directorio "/var/log" con nombres como "cron.log" o "syslog".

Para verificar si una tarea programada se ha ejecutado correctamente, puedes revisar el registro correspondiente y buscar mensajes de éxito o errores. Si encuentras algún error, es importante investigar y solucionar la causa subyacente. Puedes utilizar herramientas como "grep" o "awk" para buscar eventos específicos en los registros.

Además de los registros, también puedes recibir notificaciones por correo electrónico sobre el estado de las tareas programadas. Puedes configurar el comando o script que se ejecuta como tarea programada para enviar un correo electrónico de notificación al finalizar. Esto te permite recibir actualizaciones en tiempo real sobre el estado de las tareas y tomar medidas rápidas si es necesario.

Otra opción es utilizar herramientas de monitoreo de sistemas más avanzados, como Nagios, Zabbix o Prometheus. Estas herramientas te permiten monitorear y verificar las tareas programadas, así como otros aspectos del sistema, como el rendimiento, la disponibilidad y la utilización de recursos. Puedes configurar alertas y recibir notificaciones cuando se detecten problemas con las tareas programadas.

<aside>
⚠️ Es importante establecer una rutina de monitoreo regular para verificar el estado de las tareas programadas. Puedes programar revisiones diarias, semanales o mensuales, según la importancia y la frecuencia de las tareas. Esto te ayudará a identificar problemas de manera oportuna y garantizar que las tareas se estén ejecutando según lo planeado.

</aside>

### **⚡️Quiz Programacion de tareas automatizadas**

1. **Cómo programamos una cron job para que se ejecute cada minuto**
    1. *0 * * * ***
    2. *1 * * * ***
2. **¿Cómo programamos una cron job para que se ejecute todos los dias a la media noche?**
    1. *0 0 * * ***
    2. *12 * 1 * ***
    3. *24 * * * ***
3. **¿Cómo programamos una cron job para que se ejecute una vez a la semana**
    1. **0 0 * * 0**
    2. ** 0 0 ***
    3. **0 * 0 * 0**
    

## **Laboratorio Automatización de tareas**

Como administrador de servidores te asignaron la tarea de crear una copia de seguridad para un archivo, esta copia de seguridad se debe generar diariamente, por lo que es una tarea que puede ser algo repetitiva y tediosa.
Recuerdas que en tu formación como analista de seguridad aprendiste sobre la automatización de tareas con Cron, por lo que decides usarlo en esta oportunidad

1. El primer paso es listar las tareas cron que tienes activas en tu sistema con el comando **`crobtab -l`**

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image96.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image96.png)

<aside>
👉 En el resultado puedes ver que no hay tareas configuradas

</aside>

1. Antes de crear la tarea, nos damos cuenta que crear un script que nos cree la copia de seguridad nos facilitara mucho más el trabajo, por lo que creamos un script en python que se vera asi.

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image97.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image97.png)

1. Una vez escrito el script procedemos a crear la cronjob con el comando `crontab -e`
2. Dentro del archivo creamos la tarea asignando que se ejecute todos los dias a la media noche `0 0 * * *`  y el comando el cual seria un cambio de directorio a scripts (donde queremos guardar la copia de seguridad) y ejecutando el comando python y guardamos el archivo.
3. Revisamos los logs de la cron job ingresando el comando: **`cat /var/log/syslog | grep “auto_copiaSeg.py`**

# **📚 Lectura 9: Respaldo y recuperación de datos:**

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image98.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image98.png)

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image99.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image99.png)

## **Planificación de respaldos y políticas de retención.**

Como analistas de ciberseguridad y administradores de seguridad la planificación de respaldos y las políticas de retención son aspectos críticos en nuestro trabajo, ya que garantizan la protección y disponibilidad de los datos almacenados en ellos. Estas prácticas son fundamentales para asegurar la integridad de la información y la capacidad de recuperación ante posibles incidentes o pérdidas de datos.

Unos aspectos importantes que tenemos que tomar en consideración cuando trabajemos en nuestros respaldos son:

| Identificación de los datos críticos |  El primer paso es identificar los datos más importantes que se encuentran en el servidor Linux. Esto puede incluir archivos de configuración, bases de datos, archivos de registro y cualquier otro dato esencial para el funcionamiento de la infraestructura. Estos datos deben ser respaldados de manera prioritaria y frecuente. |
| --- | --- |
| Selección de la herramienta de respaldo | Existen varias herramientas de respaldo disponibles para servidores Linux, como rsync, tar, Bacula, entre otras. Es importante seleccionar una herramienta que se ajuste a las necesidades específicas de tu servidor y que permita realizar respaldos de manera eficiente y confiable. |
| Definición de la estrategia de respaldo | La estrategia de respaldo puede incluir respaldos completos, incrementales o diferenciales. Los respaldos completos copian todos los datos seleccionados, mientras que los incrementales y diferenciales solo respaldan los cambios realizados desde el último respaldo. Es importante evaluar cuál estrategia se ajusta mejor a tus necesidades en términos de tiempo, espacio de almacenamiento y capacidad de recuperación. |
| Programación de los respaldos | Es recomendable establecer una programación regular para los respaldos. Esto puede incluir respaldos diarios, semanales o mensuales, dependiendo de la criticidad de los datos y la frecuencia de cambios en el servidor. Además, es importante considerar el impacto en el rendimiento del servidor durante el proceso de respaldo. |
| Almacenamiento seguro | Los respaldos deben almacenarse en un lugar seguro y fuera del servidor Linux. Esto puede incluir dispositivos de almacenamiento externos, servidores de respaldo remotos o servicios en la nube. Es fundamental garantizar que los respaldos estén protegidos contra accesos no autorizados y desastres físicos. |

En cuanto a las políticas de retención, es importante establecer el tiempo durante el cual los respaldos deben ser almacenados antes de ser eliminados. Algunos aspectos a considerar son:

1. **Cumplimiento legal y normativo**: Asegúrate de cumplir con las leyes y regulaciones aplicables en cuanto a la retención de datos. Esto puede variar según la industria y la ubicación geográfica.
2. **Requisitos operativos**: Considera los requisitos operativos de tu organización, como auditorías internas o externas, acuerdos contractuales o necesidades de recuperación ante desastres. Estos requisitos pueden influir en la duración de la retención de los respaldos.
3. **Evaluación y revisión periódica**: Es recomendable revisar y actualizar regularmente las políticas de retención para asegurarse de que sigan siendo adecuadas y estén alineadas con los cambios en la organización y en el entorno legal.

## **Uso de herramientas de respaldo y recuperación**

Garantizar la protección y la disponibilidad de los datos almacenados es una labor esencial e importante dentro de nuestras funciones como administradores de servidor, para ello podemos apoyarnos en herramientas de respaldo y recuperación, estas herramientas permiten realizar copias de seguridad de los datos y facilitan su recuperación en caso de pérdida, daño o corrupción.

Algunas herramientas populares son:

| rsync | Es una herramienta de sincronización y respaldo que permite copiar y sincronizar archivos y directorios entre sistemas locales o remotos. Rsync utiliza algoritmos eficientes para transferir solo las diferencias entre los archivos, lo que reduce el tiempo y el ancho de banda requeridos para los respaldos. |
| --- | --- |
| tar | Es una herramienta de archivado que permite crear archivos comprimidos de directorios y archivos individuales. Tar se utiliza comúnmente en combinación con otras herramientas, como gzip o bzip2, para comprimir los archivos de respaldo y ahorrar espacio de almacenamiento. |
| Bacula | Es una solución de respaldo y recuperación de código abierto que ofrece una amplia gama de características y funcionalidades. Bacula permite realizar respaldos completos, incrementales y diferenciales, y ofrece opciones avanzadas como la programación de respaldos, la gestión de políticas de retención y la recuperación granular de archivos. |
| Amanda | Es otra herramienta de respaldo y recuperación de código abierto que se utiliza ampliamente en servidores Linux. Amanda permite realizar respaldos en red de manera eficiente y escalable, y ofrece características como la deduplicación de datos, la compresión y la encriptación. |
| Duplicity | Es una herramienta de respaldo basada en el protocolo rsync que ofrece respaldos incrementales y cifrados. Duplicity se integra bien con servicios en la nube, como Amazon S3 o Google Drive, lo que permite almacenar los respaldos de forma segura y fuera del servidor Linux. |

Al utilizar estas herramientas de respaldo y recuperación, es importante seguir buenas prácticas, como:

- Realizar respaldos de manera regular y programada, asegurándose de incluir los datos críticos y relevantes para la organización.
- Almacenar los respaldos en un lugar seguro y fuera del servidor Linux, preferiblemente en dispositivos de almacenamiento externos o servicios en la nube.
- Verificar la integridad de los respaldos para asegurarse de que se puedan recuperar correctamente en caso de necesidad.
- Documentar y probar los procedimientos de recuperación para garantizar una recuperación eficiente y exitosa de los datos en caso de pérdida o desastre.

## **Pruebas de verificación de los respaldos.**

Las pruebas de verificación de los respaldos son una parte fundamental de la estrategia de respaldo y recuperación de datos. Estas pruebas permiten asegurarse de que los respaldos se hayan realizado correctamente y de que los datos puedan ser recuperados de manera exitosa en caso de necesidad.

A continuación, te presento algunos puntos clave a considerar al realizar pruebas de verificación de los respaldos en servidores Linux:

1. Verificación de la integridad de los respaldos: Es importante asegurarse de que los respaldos estén completos y no hayan sufrido daños o corrupción durante el proceso de respaldo. Para ello, se pueden utilizar herramientas como md5sum o sha256sum para calcular el hash de los archivos respaldados y compararlos con los hashes originales. Si los hashes coinciden, es un indicativo de que los respaldos están íntegros.
2. Restauración de datos de prueba: Una forma efectiva de verificar los respaldos es realizar pruebas de restauración de datos en un entorno de prueba. Esto implica seleccionar algunos archivos o directorios de respaldo y restaurarlos en un servidor o máquina virtual separada. Al realizar esta prueba, se puede confirmar que los datos respaldados se pueden recuperar correctamente y que están en un estado utilizable.
3. Verificación de la consistencia de los datos: Además de verificar la integridad de los respaldos, es importante asegurarse de que los datos respaldados sean consistentes y estén en un estado utilizable. Esto implica verificar que los archivos y directorios respaldados sean accesibles y que no haya errores o inconsistencias en su contenido.
4. Pruebas de recuperación ante desastres: Las pruebas de recuperación ante desastres son esenciales para evaluar la capacidad de recuperación de los respaldos en situaciones críticas. Estas pruebas implican simular un escenario de pérdida total del servidor y realizar la recuperación de los datos utilizando los respaldos. Al realizar estas pruebas, se puede evaluar la efectividad de los respaldos y los procedimientos de recuperación.
5. Documentación y seguimiento: Es importante documentar y realizar un seguimiento de las pruebas de verificación de los respaldos. Esto incluye registrar los resultados de las pruebas, identificar cualquier problema o inconsistencia encontrada y tomar las medidas necesarias para corregirlos. Además, es recomendable establecer una programación regular para realizar pruebas de verificación de los respaldos y asegurarse de que se realicen de manera periódica.

## **Quiz: Respaldo y recuperación de datos**

1. **¿Cuál es el primer paso para la planificación de respaldo de información?**
    1. **Seleccionar la herramienta de respaldo**
    2. **Definir la estrategia de respaldo**
    3. **Identificar los datos críticos**
2. **¿Cuál herramienta nos permite crear archivos comprimidos para respaldar nuestra información?**
    1. **rsync**
    2. **tar**
    3. **amanda**
3. **Que herramienta podemos usar para calcular el hash de un archivo archivo y comprobar su autenticidad?**
    1. **sha256sum**
    2. **Duplicity**
    3. **Bacula**
    

# **📚 Lectura 10 Monitoreo y optimización del rendimiento del servidor**

## **Uso de herramientas de monitoreo del sistema**

Monitorizar y optimizar el rendimiento de nuestro servidor son aspectos fundamentales para garantizar un funcionamiento eficiente y confiable de los sistemas informáticos. Un servidor con un rendimiento óptimo puede mejorar la velocidad de respuesta, la disponibilidad de los servicios y la experiencia del usuario. Algunas prácticas clave para el monitoreo y la optimización del rendimiento del servidor Linux:

- **Monitoreo del rendimiento:** El primer paso para optimizar el rendimiento del servidor Linux es realizar un monitoreo constante de los recursos del sistema. Esto implica supervisar el uso de la CPU, la memoria, el almacenamiento y la red. Existen herramientas como Nagios, Zabbix o Munin que permiten realizar un monitoreo en tiempo real y generar alertas en caso de que algún recurso se encuentre al límite o haya un comportamiento anormal.
- I**dentificación de cuellos de botella:** Durante el monitoreo del rendimiento, es importante identificar los cuellos de botella, es decir, los componentes del sistema que limitan el rendimiento general. Pueden ser problemas de CPU, falta de memoria, cuellos de botella de red o problemas de almacenamiento. Al identificar estos cuellos de botella, se pueden tomar medidas para optimizar el rendimiento.
- **Ajuste de la configuración del sistema:** Una vez identificados los cuellos de botella, es necesario ajustar la configuración del sistema para optimizar el rendimiento. Esto puede incluir la asignación adecuada de recursos, como la configuración de la memoria virtual, la afinación del kernel o la optimización de los parámetros de red. Es importante tener en cuenta las recomendaciones específicas para el sistema operativo Linux y las aplicaciones que se ejecutan en el servidor.
- **Optimización de servicios y aplicaciones:** Además de ajustar la configuración del sistema, es importante optimizar los servicios y aplicaciones que se ejecutan en el servidor Linux. Esto implica revisar la configuración de los servicios, como el servidor web, la base de datos o el servidor de correo electrónico, y realizar ajustes para mejorar su rendimiento. También se pueden aplicar técnicas de optimización de código y utilizar herramientas de profiling para identificar y corregir cuellos de botella en las aplicaciones.
- **Monitoreo de logs y registros:** El monitoreo de los logs y registros del servidor Linux es esencial para identificar posibles problemas de rendimiento y tomar medidas correctivas. Los logs pueden proporcionar información valiosa sobre errores, advertencias, tiempos de respuesta y uso de recursos. Existen herramientas como Logwatch o Logstash que facilitan la recopilación y el análisis de los logs del servidor.
- **Actualización y parcheo del sistema:** Mantener el sistema operativo Linux actualizado con las últimas actualizaciones y parches de seguridad es crucial para garantizar un rendimiento óptimo. Las actualizaciones y parches suelen incluir mejoras de rendimiento y correcciones de errores que pueden beneficiar al servidor.
- **Escalado y balanceo de carga:** Si el servidor Linux experimenta un alto volumen de tráfico o carga, puede ser necesario implementar técnicas de escalado y balanceo de carga. Esto implica distribuir la carga de trabajo entre varios servidores o instancias para mejorar el rendimiento y la disponibilidad. Herramientas como Nginx, HAProxy o Apache Load Balancer pueden ayudar en esta tarea.

## **Identificación y solución de cuellos de botella del sistema**

La identificación y solución de cuellos de botella del sistema son procesos fundamentales para optimizar el rendimiento y garantizar un funcionamiento eficiente de un sistema informático. Un cuello de botella se refiere a un componente o recurso del sistema que limita su rendimiento general. Puede ser un problema de hardware, software o configuración que impide que el sistema funcione a su máximo potencial.

Algunas maneras que podemos usar para resolver esto es:

- **Análisis de los datos:**

 Una vez que hayas recopilado los datos de monitoreo, es importante analizarlos para identificar patrones y tendencias. Busca picos de uso de recursos, tiempos de respuesta lentos o cualquier otro indicio de un posible cuello de botella. Presta especial atención a los recursos que se encuentren constantemente al límite o que muestren un comportamiento anormal.

- **Identificación de los componentes críticos:**

En base al análisis de los datos, identifica los componentes críticos del sistema que están causando los cuellos de botella. Puede ser la CPU, la memoria, el disco, la red o incluso una configuración incorrecta de software. Prioriza los componentes que tienen un impacto significativo en el rendimiento general del sistema.

- **Optimización de recursos:**

Una vez identificados los cuellos de botella, es hora de tomar medidas para solucionarlos. Esto puede implicar optimizar el uso de los recursos existentes. Por ejemplo, puedes ajustar la configuración del sistema operativo para asignar más recursos a los procesos críticos, optimizar la configuración de la red para reducir la latencia o ajustar la configuración de la base de datos para mejorar el rendimiento de las consultas.

- **Actualización de hardware o software**:

En algunos casos, la solución de un cuello de botella puede requerir la actualización del hardware o software del sistema. Por ejemplo, si la CPU está constantemente al límite, considera actualizar a una CPU más potente. Si el disco está ralentizando el sistema, considera cambiar a una unidad de estado sólido (SSD) más rápida. Si el software está causando problemas, asegúrate de tener la última versión o considera alternativas más eficientes.

- **Pruebas y seguimiento:**

Después de implementar las soluciones, realiza pruebas exhaustivas para verificar si los cuellos de botella se han resuelto y si el rendimiento del sistema ha mejorado. Realiza un seguimiento continuo del rendimiento para asegurarte de que los cuellos de botella no vuelvan a aparecer y de que el sistema funcione de manera óptima.

## **Optimización de recursos y configuraciones del servidor**

La optimización de recursos y configuraciones del servidor en servidores Linux es esencial para garantizar un rendimiento óptimo y una eficiencia en el uso de los recursos disponibles. Al optimizar los recursos y configuraciones, puedes mejorar la velocidad de respuesta, la estabilidad y la seguridad del servidor.

Algunas prácticas clave para la optimización de recursos y configuraciones de servidores:

1. **Ajuste de la configuración del kernel:** El kernel de Linux es el núcleo del sistema operativo y controla el acceso y la gestión de los recursos del servidor. Ajustar la configuración del kernel puede ayudar a optimizar el rendimiento y la estabilidad del servidor. Puedes modificar parámetros como el tamaño del búfer de red, el número máximo de procesos o el tamaño de la memoria caché para adaptarlos a las necesidades específicas de tu servidor.
2. **Gestión de la memoria:** La gestión eficiente de la memoria es crucial para optimizar el rendimiento del servidor. Puedes ajustar la configuración de la memoria virtual (swap) para equilibrar el uso de la memoria física y virtual. Además, es recomendable utilizar herramientas como "top" o "htop" para monitorear el uso de la memoria e identificar posibles fugas de memoria o procesos que consuman demasiada memoria.
3. **Optimización del almacenamiento:** El almacenamiento es otro recurso crítico en un servidor Linux. Puedes optimizar el almacenamiento utilizando sistemas de archivos adecuados, como ext4 o XFS, y ajustando parámetros como el tamaño del bloque o la política de escritura en caché. Además, considera utilizar técnicas de particionamiento adecuadas para separar los datos del sistema operativo y los datos de las aplicaciones.
4. **Configuración de servicios y aplicaciones:** Los servicios y aplicaciones que se ejecutan en el servidor también pueden beneficiarse de una configuración adecuada. Ajusta los parámetros de configuración de los servicios, como el servidor web (Apache o Nginx), la base de datos (MySQL o PostgreSQL) o el servidor de correo electrónico (Postfix o Exim), para optimizar su rendimiento y seguridad. Además, considera deshabilitar servicios innecesarios para reducir la carga del servidor.
5. **mplementación de cachés y aceleradores**: El uso de cachés y aceleradores puede mejorar significativamente el rendimiento del servidor. Por ejemplo, puedes implementar un caché de página web como Varnish o un acelerador de bases de datos como Redis o Memcached para reducir la carga en el servidor y acelerar el acceso a los datos.
6. **Monitoreo y ajuste continu**o: La optimización de recursos y configuraciones es un proceso continuo. Es importante monitorear regularmente el rendimiento del servidor utilizando herramientas de monitoreo como Nagios, Zabbix o Prometheus. Realiza ajustes y optimizaciones adicionales según sea necesario para mantener un rendimiento óptimo a medida que cambian las necesidades y cargas de trabajo del servidor.

**Quiz Monitoreo y optimización del rendimiento del servidor**

1. **Qué herramienta podemos usar para monitorizar los logs de registros en nuestro sistema?**
    1. **apache**
    2. **Nagios**
    3. **Logstash**
2. **¿Qué podemos conseguir analizando los datos para optimizar el sistema?**
    1. **Los componentes del servidor**
    2. **picos de usos de recursos**
    3. **La configuración de los servicios y aplicaciones**
3. **¿Que herramienta podemos usar para monitorizar el sistema del servidor?**
    1. **ufw**
    2. **Nagios**
    3. **logStash**