---
title: "Preparación del entorno de virtualización"
subtitle: "Descubre cómo preparar tu entorno de virtualización en Linux: tipos, beneficios y paso a paso para instalar y configurar máquinas virtuales."
tags: ["linux", "virtualizacion"]
authors: ["blindma1den", "lorenagubaira"]

---

En IT existe una propuesta tecnológica llamada virtualización la cual permite crear servicios con recursos que generalmente están limitados al hardware. Podemos ver esta tecnología de esta manera, imaginemos contar con tres servidores físicos, cada uno con propósitos específicos, un servidor de correo, un servidor web y un servidor ejecutando aplicaciones heredades internas. Cada servidor está usando alrededor del 30% de la capacidad de cada servidor, es decir, solo una parte de su potencial. Pero como las aplicaciones heredadas siguen siendo importantes para sus operaciones internas, tienen que conservarse junto con el tercer servidor que las aloja.

Gracias a la Virtualización, podemos dividir el servidor de correo en otros dos servidores que pueden ocuparse de tareas independientes, para poder trasladar las aplicaciones heredadas. Se utiliza el mismo hardware pero de manera más eficiente.

En la virtualización hay un software denominado hipervisor que separa los recursos físicos de los entornos virtuales que los necesitan, estos hipervisores pueden controlar un sistema operativo o instalarse directamente en el hardware. Estos toman los recursos físicos del hardware y los dividen de manera tal que los entornos virtuales puedan usarlos, estos entornos virtuales son denominados máquinas virtuales, una máquina virtual funciona como un archivo de datos único; por eso, tal como ocurre con cualquier archivo digital, es posible trasladarla de una computadora a otra, abrirla en cualquiera de ellas y tener la tranquilidad que funcionara de la misma forma.

## Tipos de virtualización que hay

### Virtualización de datos

Todos los datos distribuidos en varias ubicaciones se pueden consolidar en una sola fuente, por eso la virtualización de datos posibilita que las empresas los traten como si fueran un suministro dinámico, ya que proporciona funciones de procesamiento que permiten reunir datos de varias fuentes e incorporar nuevas facilmente segun la necesidades del usuario

### Virtualización de servidores

La virtualización de un servidor, que implica dividirlo para que sus elementos puedan utilizarse para realizar varias tareas, permite ejecutar más funciones específicas.

### Virtualización de escritorios

En esta virtualización permite que un administrador central o una herramienta de administración automatizada implementen entornos simulados de escritorio en cientos de máquinas físicas al mismo tiempo. A diferencia de los entornos de escritorio tradicionales que se instalan, configuran y actualizan físicamente en cada máquina, la virtualización de escritorios permite que los administradores realicen múltiples configuraciones, actualizaciones y controles de seguridad en todos los escritorios virtuales.

Al utilizar la virtualización, es posible interactuar con cualquier recurso de *hardware* con mayor flexibilidad. Los servidores físicos consumen electricidad, ocupan espacio de almacenamiento y necesitan mantenimiento. Con frecuencia el acceso a estos está limitado por la proximidad física y el diseño de la red. La virtualización resuelve todas estas limitaciones al abstraer la funcionalidad del *hardware* físico en el *software*. Es posible administrar, mantener y utilizar la infraestructura de *hardware* como una aplicación en la web. Esto proporciona varios beneficios a cualquier organización como:

- Utilización eficiente de los recursos de hardware
- Administración automatizada de las TI
- Recuperación de desastres más rápido.

## Elegir el sistema operativo para virtualizar

Para preparar un entorno de virtualización necesitamos un software que nos permita la virtualización y el sistema operativo

Entre los software que nos pueden permitir hacer virtualización tenemos;

- VMware
- VirtualBox
- Hyper-V (Disponible en windows)

En linux podemos conseguir los sistemas operativos como distribuciones, estas son sistemas operativos diseñados a partir del kernel de linux que admiten programas de usuarios, repositorios y bibliotecas, podemos conseguir distintas versiones de estos sistemas operativos orientado a un grupo de usuarios que lo usara.

### Distribuciones de linux mas usadas

- **Ubuntu**

Ubuntu ****es una distribución de Linux basada en Debian. Está desarrollada por Canonical y una comunidad de desarrolladores. Tiene tres ediciones oficiales: *Desktop*, *Server* y *Core*, que pueden ejecutarse tanto en ordenador como en una máquina virtual.

- **Debian**

El proyecto Debian es una comunidad de desarrolladores y usuarios que mantienen el OS GNU basado en software de código abierto. Actualmente, los sistemas Debian utilizan el kernel de Linux o el kernel de FreeBSD. Sin embargo, también están trabajando en ofrecer Debian para otros kernels.

- **Fedora**

Fedora ****es una distribución de Linux desarrollada por el proyecto Fedora. Está desarrollada y mantenida por la comunidad y es una fuente upstream de la distribución comercial RHEL. Fedora suele disponer de versiones más modernas del software, consideradas “no estable” que luego se incluyen en RHEL.

- **Arch Linux**

Arch Linux es una distribución de Linux basada en 5 principios: la simplicidad, la modernidad, el pragmatismo, el usuario en el centro y la versatilidad. Las actualizaciones siguen un modelo de *rolling release*.

**Para los usuarios destinados a la ciberseguridad y hacking:**

- **Kali Linux**

Quizás sea la distribución de seguridad por excelencia. Creada por Offensive Security y basada en Debian, es una distro que integra cientos de herramientas para hacernos las auditorías de seguridad más sencillas. Sirve tanto para test de penetración, análisis forense y auditorías de seguridad.

- **Parrot Security OS**

También es una de las favoritas para muchos, resulta una buena alternativa para Kali. Parrot Security OS o ParrotSec se basa en Debian y ha sido creada por el equipo de desarrollo FrozenBox.  En este caso han optado por un entorno de escritorio MATE y por el display manager LightDM para hacerla más ligera. Igual que Kali incluye cientos de herramientas para la seguridad (penetración, forense y auditorías en general).

- **BlackArch**

BlackArch, como su propio nombre indica, está basada en Arch Linux. Tiene un enorme repositorio con unos 1500 paquetes correspondientes a herramientas para pentesting, análisis forense y auditorías de seguridad en general. Se pueden instalar individualmente o en grupos por categorías según nuestras necesidades.
