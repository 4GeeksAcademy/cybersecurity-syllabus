# Lectura 5 📕: Administración basica del sistema

## Gestion de grupos y usuario

Podemos denominar a Linux como un sistema operativo multiusuario, donde existen dos tipos de usuarios, el usuario root o administrador, y el resto de los usuario

El usuario root tiene la posibilidad de realizar todo tipo de labores respecto a la administración del sistema. Los cambios o modificaciones realizados con este usuario pueden causar inconvenientes en la seguridad del sistema completo, por lo que debemos tener en cuenta recomendaciones como utilizar este root solo cuando sea estrictamente necesario llevar a cabo una tarea de administración, y cuando terminemos, debemos volver a trabajar con nuestro usuario normal. Además, se sugiere que para acceder al usuario administrador, primero se haya iniciado sesión a través de una cuenta de usuario normal, esta medida previene trabajar con root de manera predeterminada.

Los otros tipos de usuarios en Linux normales o no administradores, son aquellos que pueden utilizar las herramientas del sistema con normalidad, pero que no pueden ejecutar labores administrativas.

Para poder realizar el cambio de usuario normal a usuario root, se necesitarán permisos de administración, y se puede acceder ya sea proporcionando la contraseña del usuario root e iniciando sesión, o establecer una lista de usuarios que pueden tener acceso como administradores. En términos de seguridad, es recomendable optar por la segunda, opción, debido a que compartir la contraseña del usuario root con varias personas, implica el traspaso de información sensible y pone al sistema en una situación de vulnerabilidad.

Los grupos en Linux son usados principalmente para otorgar permisos sobre archivos y directorios, es decir, para gestión de usuarios linux. El sistema operativo ya trae incluido ciertos grupos predeterminados que cumplen con funciones específicas. Cada grupo creado en Linux tiene la característica de ser independiente de otros. Además, los grupos en Linux pueden tener contraseñas. Estos grupos pueden ser de tipo primario o secundario para la gestión de usuarios Linux:

- **Grupo principal**: tiene la función de determinar quién será el grupo que posea los archivos creados por el usuario. El grupo primario es el que se le asocia a la cuenta por defecto, y al que se le asignan los archivos y directorios desarrollados por el usuario. Además, el nombre del grupo suele ser el mismo nombre de usuario.
- **Grupos secundarios**: los grupos suplementarios son aquellos grupos adicionales a los que el usuario pertenezca.

Algunos comandos que podemos usar para la gestión de usuarios y grupos son

**`useradd`** (Agrega a un usuario)

**`userdel`** (elimina a un usuario)

**`passwd`** (cambia la contraseña de un usuario)

**`groupadd`** (crea un grupo en la gestión)

**`groupdel`** (elimina un grupo)

**`whoami`** (nos indica qué usuario somos)

## **Configuración de red y conexión**

Una de las ventajas de la configuración de red y conexión en linux es que fácilmente se puede hacer a través desde la terminal con varios comandos, veamos cuales son:

- Si queremos saber si como esta configurada la **red TCP/IP** podemos usar el comando

**`ifconfig` o con `ip add`**

La respuesta del comando nos mostrara la ip de la máquina (inet), mascara de red (netmask) y dirección de difusión (broadcast).

- Si queremos cambiar la dirección de ip, usaremos el mismo comando `ifconfig`:

```markdown
*ifconfig eth0 192.168.1.100 netmask 255.255.255.0 broadcast 192.168.1.255*
```

**`eth0`** es la interfaz de red que vamos a configurar

- El comando `ping` nos sirve de mucha utilidad para medir la latencia y la conectividad de la red. A través de este comando se mandan paquetes de datos a la dirección puesta en el comando esperando por respuesta de dicha dirección.

ejemplo:

```markdown
**ping 127.0.0.1**
```

Haciendo ping a dirección_ip con 32 bytes de datos:

Respuesta desde 127.0.0.1: bytes=32 tiempo= <10 ms TTL=128

> 💡 TTL= es el tiempo de vida del paquete enviado y su valor óptimo es 128

**Netstat** es otra herramienta que podemos utilizar a través de la línea de comandos. Nos permite monitorizar las redes y también poder solucionar determinados problemas que puedan surgir.

Cuando tratamos de luchar contra el exceso de tráfico o los software malintencionados, con Netstat estamos ante una herramienta que nos da gran ventaja con las conexiones entrantes y salientes de un equipo o servidor. Pues estas conexiones, se establecen en su correspondiente dirección de red, la cual nos indica entre otras cosas, cuál es el puerto que se ha abierto para realizar la comunicación.

Las distintas flags que podemos conseguir con este comando pueden ser:

- **`Netstat –a`**: nos permite conocer todas las redes que están activas o inactivas en un momento dado. Así lograremos detectar posibles problemas que afecten a una red.
- **`Netstat –e`**: en este caso podemos ver estadísticas sobre los paquetes de red entrantes y salientes en una tarjeta de red.
- **`Netstat –f`**: muestra el nombre de dominio completo de direcciones remotas.
- **`Netstat –n`**: este comando, a diferencia del anterior, muestra los números de puerto en lugar de los nombres.
- **`Netstat –o`**: muestra el ID de cada proceso en cada conexión.
- **`Netstat –p** X`: con este comando podemos filtrar conexiones según el protocolo (TCP, UDP, tcpv6 o tcpv4. X=TCP, UDP… el protocolo que queramos. Por ejemplo sería netstat –p TCP.
- **`Netstat –q`**: consultar los puertos de escucha y de no escucha vinculados.
- **`Netstat –s`**: muestra las estadísticas de grupo por protocolo. Así podremos clasificar las redes según los protocolos disponibles: TCP, UDP, ICMP, IPv4 o IPv6.
- **`Netstat –r`**: este comando nos muestra la tabla de enrutamiento de la red actual.
- **`Netstat –t`**: ofrece información sobre las conexiones en estado de descarga.
- **`Netstat –x`**: en este caso podemos obtener información sobre todas las conexiones NetworkDirect.

## Monitorización de recursos del sistema

En algunas ocasiones podemos tener algún problema de rendimiento dentro de nuestro sistema, y tenemos que mirar qué aplicación está consumiendo más recursos del sistema. GNU/Linux tiene disponible varias herramientas para la línea de comandos, todas estas herramientas ofrecen información de manera dinámica de lo que se está ejecutando en el sistema y ofrecen un resumen de esa información y lista de tareas que se puede ordenar por consumo de CPU, consumo de RAM, etc.

Entre las herramientas que tenemos disponibles tenemos:

- **Top**

Este programa provee una vista dinámica a tiempo real de como esta corriendo el sistema, Puede mostrar un resumen de información del sistema así como una lista de tareas que está actualmente administradas por el kernel de linux.

![Top](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/top.png)

- **ps**

Este comando realiza un seguimiento de la memoria y uso de CPU. Al ejecutar el comando, el sistema responde con el nombre de cada proceso, su número de identificación de proceso (PID), el tiempo de CPU consumido y la terminal o usuario asociados. La información que muestra el sistema es muy útil, te ofrece una visión general inicial para que puedas identificar rápidamente cualquier problema, una gran combinación es concatenar el comando ps con grep para asi examinar un proceso determinado.