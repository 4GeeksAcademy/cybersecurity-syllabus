---
title: "File and directory management"
subtitle: "Navigating and manipulating files in Linux: Essential commands and good practices for system administrators."
tags: ["linux"]
authors: ["blindma1den", "lorenagubaira"]

---

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