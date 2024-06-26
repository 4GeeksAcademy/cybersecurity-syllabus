---
title: "Gestión de paquetes y software"
subtitle: "Domina gestión de paquetes en Linux: instala, actualiza y elimina software con facilidad. Aprende a configurar repositorios y mantén tu sistema seguro."
tags: ["linux"]
authors: ["blindma1den", "lorenagubaira"]

---

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

> 🤓 Como práctica les dejamos que investiguen como configurar el servicio samba

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