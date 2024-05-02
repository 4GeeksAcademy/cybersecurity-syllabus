---
title: "Package and software management"
subtitle: "Discover how to manage packages and software in Linux: installation, update, uninstallation and dependency management efficiently and safely."
tags: ["linux"]
authors: ["blindma1den", "lorenagubaira"]

---

Teniendo claro que es Linux y que se constituye en dos partes, con su kernel siendo el núcleo del sistema y la otra parte como el resto de los programas que lo componen para hacer un uso más específico, estos programas se distribuyen usando paquetes, estos paquete sirven para entregar el software y su mantenimiento.

Un paquete en linux consiste en una colección de archivos que permiten la instalación de un programa y sus tareas relacionadas, como la búsqueda de dependencias, instalaciones previas, etc. Dentro de este paquete de programa tenemos todos los archivos requeridos para ser instalado y posteriormente ejecutado. Además se incluye un pequeño archivo que proporciona metadatos importantes sobre el programa.

La razón principal para distribuir software en base a paquetes es simple. Cuando hablamos de GNU/linux nos referimos a un ecosistema de distribuciones que cuenta con notables diferencias entre si. Esto no hace posible “garantizar” que un software funcione correctamente en una computadora determinada. El uso de paquetes resuelve este problema de interoperabilidad gracias al archivo de metadatos antes mencionado que actúa como un manifiesto de dependencias que deben cumplirse para que el software que está empaquetado se ejecute correctamente en un ordenador determinado.

Los gestores de paquetes nos pueden ayudar con el proceso de instalación de programas en linux, estas utilidades están presente en cada distribución, y se encargan de automatizar el proceso, también de listar paquetes disponibles en el repositorio y mostrar información sobre sus dependencias.

Los sistemas comunes de administración de paquetes incluyen:

- **DPKG**: el administrador de paquetes base para distribuciones basadas en Debian.
- **Apt-get**: una interfaz que hace más amigable y añade funciones para el sistema DPKG, que se encuentra en las distribuciones basadas en Debian.
- **Aptitude**: Aptitude es una interfaz para APT para distribuciones basadas en Debian. Muestra una lista de paquetes de software y permite al usuario elegir de modo interactivo cuáles desea instalar o eliminar
- **Synaptic**: Synaptic es instalado por defecto en Debian en la versión de escritorio, es una herramienta gráfica para la gestión de paquetes basada en GTK+ y APT.
- **RPM**: el administrador de paquetes base que se encuentra en las distribuciones basadas en Red Hat, como Red Hat Enterprise Linux, CentOS y Fedora.
- **Yum**: un front-end para el sistema RPM, que se encuentra en las distribuciones basadas en Red Hat.
- **Pacman**: el administrador de paquetes para distribuciones basadas en Arch Linux.

## Instalación y actualización de software

Hoy en dia es mucho más cómodo instalar y administrar las aplicaciones mediante el uso de ia interfaz gráfica que presentan las distribuciones basadas en Debian o Ubuntu, a pesar de eso, nos puede resultar mucho mejor hacer todas las actualizaciones e instalaciones del sistema con el gestor de paquetes ya que es mucho más potente.

Para hacer las instalaciones debemos acceder al terminal con elevación de priviliegios usando el comando sudo.

Para la explicación usaremos el gesto apt

```markdown
**sudo apt [parámetros] [nombre del programa]**
```

el caso  que queramos hacer una actualización del sistema, debemos primero hacer una actualización del índice de paquetes de nuestro sistema con cada uno de los repositorios a los que está conectado, para ello usaremos el comando:

```markdown
**sudo apt update**
```

Una vez actualizados los repositorios de sistemas procederemos a instalar las actualizaciones.

```markdown
**sudo apt upgrade**
```

La instalación de paquetes en distribuciones puede ser bastante sencilla, en el caso de apt usamos el siguiente comando:

```markdown
**sudo apt install [nombre del paquete]**
```

También podemos concatenar varios paquetes para hacer una instalación de una sola vez

```markdown
**sudo apt install -y gimp terminator**
```

Otro gestor de paquete que podemos usar para la distribuciones debian (.deb) es dpkg.

Para usar gestor usamos el siguiente comando:

```markdown
**dpkg -i nombre_paquete.deb**
```

Este proceso lo podemos simplificar en dos pasos, haciendo un desempaquetado del programa `.deb` y luego configurandolo

```markdown
**dpkg –unpack nombre_paquete.deb**
```

```markdown
**dpkg -configure nombre_paquete**
```

## Desinstalación de paquetes y gestión de dependencias

La desinstalación de paquetes y la gestión de dependencias son dos aspectos fundamentales en el sistema operativo Linux. Estas funciones permiten a los usuarios instalar y desinstalar software de manera eficiente y asegurarse de que todas las dependencias necesarias estén satisfechas.
Cuando instalamos un paquete en Linux, es posible que este dependa de otros paquetes para funcionar correctamente. Estas dependencias son componentes adicionales que el software necesita para ejecutarse sin problemas. Por ejemplo, un programa de edición de imágenes puede depender de una biblioteca gráfica específica para mostrar correctamente las imágenes.

La gestión de dependencias en Linux se encarga de resolver estas relaciones y asegurarse de que todas las dependencias estén presentes antes de instalar un paquete. Esto evita problemas de compatibilidad y garantiza que el software funcione correctamente.
Cuando deseamos desinstalar un paquete en Linux, es importante tener en cuenta las dependencias que este paquete puede tener. Si desinstalamos un paquete sin tener en cuenta sus dependencias, podríamos dejar el sistema en un estado inestable o incompleto

Afortunadamente, la mayoría de los gestores de paquetes en Linux, como apt-get en Debian y Ubuntu, o yum en Red Hat y CentOS, se encargan automáticamente de gestionar las dependencias al instalar o desinstalar paquetes. Estos gestores de paquetes resuelven las dependencias y eliminan los paquetes no utilizados de manera segura.

Para desinstalar un paquete en Linux, podemos utilizar el comando específico del gestor de paquetes correspondiente. Por ejemplo, en sistemas basados en Debian y Ubuntu, podemos usar el comando "apt-get remove" seguido del nombre del paquete que deseamos desinstalar. Esto eliminará el paquete y todas sus dependencias no utilizadas.
Es importante destacar que, en algunos casos, es posible que desinstalar un paquete pueda afectar a otros programas que dependen de él. En estos casos, el gestor de paquetes nos advertirá sobre las consecuencias antes de proceder con la desinstalación.

Si queremos desinstalar los paquetes, usamos la `flag -r`

```markdown
**dpkg -r nombre_programa**
```

