---
title: Administración basica del sistema
tags:
  - linux
authors:
  - blindma1den
  - lorenagubaira
description: >-
  Master la administración básica del sistema en Linux. Aprende a gestionar
  usuarios, grupos y optimizar la seguridad. ¡Descubre cómo mejorar tu sistema
  ahora!
---
## Gestión de grupos y usuarios

Podemos denominar a Linux como un sistema operativo multiusuario, donde existen dos tipos de usuarios: el usuario root o administrador, y el resto de los usuarios.

El usuario root tiene la posibilidad de realizar todo tipo de labores respecto a la administración del sistema. Los cambios o modificaciones realizados con este usuario pueden causar inconvenientes en la seguridad del sistema completo, por lo que debemos tener en cuenta recomendaciones como utilizar este root solo cuando sea estrictamente necesario llevar a cabo una tarea de administración, y cuando terminemos, debemos volver a trabajar con nuestro usuario normal. Además, se sugiere que para acceder al usuario administrador, primero se haya iniciado sesión a través de una cuenta de usuario normal, esta medida previene trabajar con root de manera predeterminada.

Los otros tipos de usuarios en Linux normales o no administradores, son aquellos que pueden utilizar las herramientas del sistema con normalidad, pero que no pueden ejecutar labores administrativas.

Para poder realizar el cambio de usuario normal a usuario root, se necesitarán permisos de administración, y se puede acceder ya sea proporcionando la contraseña del usuario root e iniciando sesión, o establecer una lista de usuarios que pueden tener acceso como administradores. En términos de seguridad, es recomendable optar por la segunda, opción, debido a que compartir la contraseña del usuario root con varias personas, implica el traspaso de información sensible y pone al sistema en una situación de vulnerabilidad.

Los grupos en Linux son usados principalmente para otorgar permisos sobre archivos y directorios, es decir, para gestión de usuarios linux. El sistema operativo ya trae incluido ciertos grupos predeterminados que cumplen con funciones específicas. Cada grupo creado en Linux tiene la característica de ser independiente de otros. Además, los grupos en Linux pueden tener contraseñas. Estos grupos pueden ser de tipo primario o secundario para la gestión de usuarios Linux:

- **Grupo principal**: tiene la función de determinar quién será el grupo que posea los archivos creados por el usuario. El grupo primario es el que se le asocia a la cuenta por defecto, y al que se le asignan los archivos y directorios desarrollados por el usuario. Además, el nombre del grupo suele ser el mismo nombre de usuario.
- **Grupos secundarios**: los grupos suplementarios son aquellos grupos adicionales a los que el usuario pertenezca.

Algunos comandos que podemos usar para la gestión de usuarios y grupos son

| Comando   | Descripción                    |
|-----------|-------------------------------|
| `useradd` | Agrega un usuario             |
| `userdel` | Elimina un usuario            |
| `passwd`  | Cambia la contraseña de un usuario |
| `groupadd`| Crea un grupo                 |
| `groupdel`| Elimina un grupo              |
| `whoami`  | Muestra el usuario actual     |

## Configuración de red y conexión

Una de las ventajas de la configuración de red y conexión en linux es que fácilmente se puede hacer a través desde la terminal con varios comandos, veamos cuales son:

- Para consultar la configuración de la **red TCP/IP** usamos el comando `ip addr` (o su forma abreviada `ip a`). El comando `ifconfig` está deprecado en la mayoría de distribuciones modernas y ha sido sustituido por la suite `iproute2`.

La respuesta del comando mostrará la dirección IP de la máquina (`inet`), la máscara de red en formato CIDR y la dirección de difusión (`brd`).

- Para cambiar la dirección IP de una interfaz, usamos el comando `ip`:

```bash
sudo ip addr add 192.168.1.100/24 broadcast 192.168.1.255 dev eth0
```

> **Nota:** `ifconfig` aún puede estar disponible instalando el paquete `net-tools`, pero se recomienda usar `ip` en su lugar.

**`eth0`** es la interfaz de red que vamos a configurar (en distribuciones modernas puede aparecer como `enp0s3`, `ens33`, etc.).

- El comando `ping` nos sirve de mucha utilidad para medir la latencia y la conectividad de la red. A través de este comando se mandan paquetes de datos a la dirección puesta en el comando esperando por respuesta de dicha dirección.

ejemplo:

```bash
ping 127.0.0.1
```

Haciendo ping a dirección_ip con 32 bytes de datos:

Respuesta desde 127.0.0.1: bytes=32 tiempo= <10 ms TTL=128

> **TTL** (*Time To Live*) indica el número máximo de saltos (routers) que un paquete puede atravesar antes de ser descartado. Su valor inicial depende del sistema operativo de origen: 64 en Linux, 128 en Windows, 255 en algunos equipos de red. No existe un valor "óptimo" universal.

**Netstat** es otra herramienta que podemos utilizar a través de la línea de comandos. Nos permite monitorizar las redes y también poder solucionar determinados problemas que puedan surgir.

Cuando tratamos de luchar contra el exceso de tráfico o los software malintencionados, con Netstat estamos ante una herramienta que nos da gran ventaja con las conexiones entrantes y salientes de un equipo o servidor. Pues estas conexiones, se establecen en su correspondiente dirección de red, la cual nos indica entre otras cosas, cuál es el puerto que se ha abierto para realizar la comunicación.

Las distintas flags que podemos conseguir con este comando pueden ser:

| Flag del Comando | Descripción                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| `Netstat –a`     | Permite conocer todas las redes que están activas o inactivas en un momento dado.            |
| `Netstat –e`     | Muestra estadísticas sobre los paquetes de red entrantes y salientes en una tarjeta de red.  |
| `Netstat –f`     | Muestra el nombre de dominio completo de las direcciones remotas.                           |
| `Netstat –n`     | Muestra los números de puerto en lugar de los nombres.                                       |
| `Netstat –o`     | Muestra el ID de cada proceso en cada conexión.                                              |
| `Netstat –p X`   | Filtra conexiones según el protocolo (TCP, UDP, tcpv6 o tcpv4).                              |
| `Netstat –q`     | Consulta los puertos de escucha y de no escucha vinculados.                                  |
| `Netstat –s`     | Muestra las estadísticas de grupo por protocolo.                                             |
| `Netstat –r`     | Muestra la tabla de enrutamiento de la red actual.                                           |
| `Netstat –t`     | Ofrece información sobre las conexiones en estado de descarga.                               |
| `Netstat –x`     | Proporciona información sobre todas las conexiones NetworkDirect.                            |

## Monitorización de recursos del sistema

En algunas ocasiones podemos tener algún problema de rendimiento dentro de nuestro sistema, y tenemos que mirar qué aplicación está consumiendo más recursos del sistema. GNU/Linux tiene disponible varias herramientas para la línea de comandos, todas estas herramientas ofrecen información de manera dinámica de lo que se está ejecutando en el sistema y ofrecen un resumen de esa información y lista de tareas que se puede ordenar por consumo de CPU, consumo de RAM, etc.

Entre las herramientas que tenemos disponibles tenemos:

- **Top**

Este programa provee una vista dinámica a tiempo real de como esta corriendo el sistema, Puede mostrar un resumen de información del sistema así como una lista de tareas que está actualmente administradas por el kernel de linux.

![Top](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/top.png)

- **ps**

Este comando realiza un seguimiento de la memoria y uso de CPU. Al ejecutar el comando, el sistema responde con el nombre de cada proceso, su número de identificación de proceso (PID), el tiempo de CPU consumido y la terminal o usuario asociados. La información que muestra el sistema es muy útil, te ofrece una visión general inicial para que puedas identificar rápidamente cualquier problema, una gran combinación es concatenar el comando ps con grep para asi examinar un proceso determinado.
