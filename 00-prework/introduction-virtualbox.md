---
title: "Introduction to VirtualBox"
subtitle: "Conoce como funciona esta poderosa herramienta, y aprende a crear una maquina virtual."
tags: ["cybersecurity"]
authors: ["arnaldoperez"]

---

## What is VirtualBox?

VirtualBox es un programa gratuito que te permite instalar diferentes sistemas operativos dentro de tu computadora actual, como si fueran programas independientes. Es como tener varias computadoras en una sola.

VirtualBox es relativamente fácil de usar, incluso para personas sin experiencia en computación.

## ¿Qué necesitas para usar VirtualBox?

- Una computadora con un procesador relativamente potente (al menos 2 núcleos) y suficiente memoria RAM (al menos 4 GB).
- Espacio libre en tu disco duro para instalar los sistemas operativos que deseas probar.
- Un sistema operativo principal compatible con VirtualBox (Windows, Linux).

## ¿Qué es una maquina virtual(MV)?

### Imagina que tu computadora es como una casa

El sistema operativo anfitrión (también llamado host) es como el dueño de la casa. Controla todo y te permite usar programas, navegar por internet, etc.
Una máquina virtual (también llamado huésped) es como una habitación dentro de la casa. En ella, puedes instalar un sistema operativo diferente, como si fuera un inquilino independiente.
En otras palabras, una máquina virtual es un programa que te permite ejecutar otro sistema operativo dentro de tu sistema operativo actual. Es como tener dos computadoras en una.

### ¿Para qué sirve una máquina virtual?

- Probar nuevos sistemas operativos sin riesgo: Puedes instalar un sistema operativo diferente en una "habitación" virtual y probarlo sin afectar tu sistema operativo principal. Si no te gusta, puedes eliminarlo fácilmente.
- Aprender sobre diferentes sistemas operativos: Puedes usar una máquina virtual para practicar con diferentes sistemas operativos y aprender cómo funcionan.
- Ejecutar programas que solo funcionan en un sistema operativo específico: Si necesitas usar un programa que solo funciona en Windows, por ejemplo, puedes instalarlo en una maquina virtual de Windows dentro de tu Mac o Linux.
- Aislar software inseguro: Puedes instalar software que no es de confianza en una maquina virtual para evitar que afecte a tu sistema operativo principal.

## Manejo de recursos de una MV

En VirtualBox, la administración de recursos para las máquinas virtuales se basa en la configuración de los siguientes elementos. Estos se puede asignar al momento de crear una nueva máquina y pueden modificarse posteriormente de ser necesario.

### Memoria RAM

Determina cómo se asigna la memoria a la máquina virtual. El valor asignado será el que tenga disponible para utilizar la maquina huésped para funcionar. 

Puede determinarse al momento de crear la maquina:

![Memoria de maquina virtual VirtualBox](/assets/vb-memoria.png)

O puede modificarse después de haber sido creada la maquina, pero solo se puede cambiar mientras el huésped este apagado.
![Memoria de maquina virtual VirtualBox](/assets/vb-maquina-config-memoria.png)

### CPU

En este apartado se asignan la cantidad de procesadores que puede usar la maquina virtual. La cantidad de procesadores disponibles para asignar corresponde a los procesadores lógicos que tenga el anfitrión, por ejemplo: Con un procesador de 4 núcleos y 8 hilos, aparecen disponibles 8 procesadores.
![Procesadores de maquina virtual VirtualBox](/assets/vb-maquina-creacion-cpu.png)

Una vez creada la máquina tambien se pueden modificar los procesadores del huesped, e incluso se puede limitar el porcentaje del procesador anfitrion que tendrán permitido utilizar.
![Procesadores de maquina virtual VirtualBox](/assets/vb-maquina-config-memoria-cpu.png)

### Almacenamiento y medios virtuales

El sistema operativo huesped se aloja en un disco duro virtual, es un archivo que simula un disco duro físico para la máquina virtual, y que ademas es portable (se puede mover facilmente a otra maquina) y tambien comprime los datos para ahorrar espacio de almacenamiento en el anfitrion.

Al momento de crear la maquina se determina el nombre del archivo y la capacidad máxima del disco duro virtual. El archivo ira creciendo a medida que el huesped tenga mas y mas datos, hasta llegar a su capacidad máxima. De la misma forma, se pueden agregar discos preexistentes a una maquina virtual.
![Disco duro de maquina virtual VirtualBox](/assets/vb-maquina-creacion-dd.png)

Una vez creada la maquina con su respectivo disco, podremos ver y modificar las unidades virtuales en el "Administrador de medios virtuales". Esta herramienta nos muestra todos los discos duros virtuales, las Unidades de disco virtuales. En cada una de sus pestañas tendremos opciones de importar nuevas medios virtuales o importar alguno que ya exista, de esta manera podemos configurar maquinas virtuales con cualquier tipo de medios conectados para lograr simular el entorno que sea necesario.
![Menú de medios virtuales VirtualBox](/assets/vb-menu-virtual-media.png)
![Discos duros virtuales VirtualBox](/assets/vb-virtual-media-drives.png)

En cuanto a los medios ópticos, estos son compuestos por archivos ISO que pueden ser descargados desde distintas partes y agregados a las maquinas virtuales. Estos archivos son el estándar mas utilizado para instaladores de sistemas operativos, tanto Windows como sistemas GNU/Linux; ambos disponibles desde sus respectivas web oficiales. Con la opcion "Añadir" de la pestaña de "Discos opticos"
![Discos ópticos virtuales VirtualBox](/assets/vb-virtual-media-optical.png)
![Discos ópticos virtuales VirtualBox](/assets/vb-maquina-config-optical-es.png)

### Red

Tipo de adaptador de red: Determina cómo la máquina virtual se conecta a la red.
Modo de red: Determina cómo la máquina virtual interactúa con la red del host.

### Otros recursos

Dispositivos USB: Puedes conectar dispositivos USB a la máquina virtual.
Sonido: Puedes configurar la salida de sonido de la máquina virtual.
Carpetas compartidas: Puedes compartir carpetas entre la máquina virtual y el sistema operativo host.

Para administrar los recursos de una máquina virtual en VirtualBox:

Abre VirtualBox y selecciona la máquina virtual que deseas configurar.
Haz clic en "Configuración".
Selecciona la pestaña de recursos que deseas configurar (memoria, CPU, almacenamiento, red, etc.).
Modifica los valores de configuración según tus necesidades.
Haz clic en "Aceptar" para guardar los cambios.

## Consejos para administrar los recursos de una máquina virtual:

- Asigna la cantidad de memoria RAM y CPU que necesita la máquina virtual para un funcionamiento optimo sin comprometer el desempeño del anfitrion. Si asignas demasiada memoria RAM o CPU, el sistema operativo host podría ralentizarse.
- Utiliza un disco duro virtual de tamaño adecuado. Si el disco duro virtual es demasiado pequeño, la máquina virtual podría quedarse sin espacio en disco.
- Configura el tipo de adaptador de red adecuado para la máquina virtual y al entorno que intentas simular, puede que necesites tener varias conexiones de red.
- Comparte carpetas entre la máquina virtual y el sistema operativo host solo si es necesario.

Es importante tener en cuenta que la cantidad de recursos que puedes asignar a una máquina virtual está limitada por los recursos disponibles en el sistema operativo host.
