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

## Descarga e instalación de una distribución de linux en una máquina virtual

Una vez elegimos la distribución que vayamos a utilizar nos dirigimos a la página web de la distribución a instalar, tenemos dos opciones:

1. Archivo con extensión **VDI**, contiene imágenes de disco virtual con metadatos asociados y es el formato de imagen nativo de VirtualBox.

2. Archivo de imagen **ISO**, representa imágen de almacenamiento idéntica de los soportes ópticos, es decir, contiene los mismos datos que se transferirán a un cd, dvd o blu-ray.

## Instalación de software de máquina virtual

Una vez hecha la configuración inicial, iniciamos la máquina Virtual en el menú superior en la opcion iniciar

![Iniciar Máquina Virtual](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/iniciar-maquina-virtual.png)

- **Configuración inicial de sistema operativo**

En la ventana principal de instalación tenemos varias opciones, seleccionamos la opción de instalación gráfica

![Configuración del Sistema Operativo](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/configuracion-del-sistema-operativo.png)

1. Seguimos todas las instrucciones de instalación.
- Seleccionamos el idioma del sistema
- Seleccionamos ubicación para fijar la zona horaria
- Seleccionamos el teclado
- Seleccionamos el nombre de la máquina

![Kali](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/kali.png)

2. Agregamos el nombre del dominio de la máquina 

![Agregar Nombre al Dominio Kali](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/nombre-dominio-kali.png)

3. Creamos el usuario y contraseña de sistema.

![Usuario y Contraseña](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/usuario-y-contraseña.png)

![Configurar Usuario y Contraseña](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/configurar-usuario-y-contraseña.png)

4. En la opcion de particion de discos, ya que estamos usando un disco virtual, seleccionamos la opción de utilizar todo el disco  (imagen-12 IMAGEN-13)

![Particion de Discos](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/particion-de-discos.png)

5. Seleccionamos los programas que queremos instalar junto al sistema operativo

![Seleccion de Programas](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/seleccion-de-programas.png)

6. Dejar que se carguen los distintos archivos de programa en la instalación.
7. Se va a preguntar si se desea instalar el cargador de arranque grub, se acepta esa opción 

![Instalar Cargador de arranque GRUB](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/cargador-de-arranque.png)

8. Ya una vez se haya completado la instalación, procedemos a reiniciar la máquina virtual.

![Reiniciar la Maquina Virtual](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/reiniciar-la-maquina-virtual.png)

## 💡 Laboratorio: Instalacion y configuracion de sistema operativo

**Para este laboratorio instalaremos Kali Linux en una máquina virtual de VirtualBox**

1. Abrimos la interfaz de virtualBox y seleccionamos a la opción nueva

![VirtualBox](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/virtualbox.png)

2. Llenamos la información de la máquina virtual donde 
- Nombre: El nombre que llevaría nuestra máquina virtual (generalmente sería el nombre del sistema operativo que usaremos).
- Folder: La Carpeta en donde se almacenará la máquina virtual.
- Iso Image: El archivo iso para instalar nuestra máquina virtual.

![Máquina Virtual](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/maquina-virtual.png)

3. Colocamos la cantidad de memoria y procesadores que le queremos asignar a la máquina virtual, en este caso asignamos dos procesadores y 4 gb de ram

![Mmemoria y Procesadores](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/memoria-y-procesadores.png)

4. Asignamos la cantidad de memoria virtual que le queramos dar a la máquina virtual

![Mmemoria y Procesadores](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/memoria-y-procesadores.png)

5. Revisamos el resumen y vemos que todo está como lo necesitamos

![Resumen Instalación](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/resumen-instalacion.png)
