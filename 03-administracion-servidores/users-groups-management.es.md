---
title: Administración básica de usuarios y grupos
tags:
  - servidores
authors:
  - blindma1den
  - lorenagubaira
description: >-
  Domina los fundamentos de la gestión de usuarios y grupos en servidores
  Linux. Aprende prácticas esenciales para administrar usuarios de forma segura
  y asignar permisos. ¡Descubre más!
---
## Creación y gestión de cuentas de Usuario.

En un sistema Linux, el usuario **root** es el único con privilegios absolutos para crear y administrar usuarios, grupos y los archivos de configuración asociados. Trabajar directamente como root no es recomendable: cualquier error puede causar fallos graves en el sistema. Por eso, durante las siguientes prácticas usaremos un usuario normal y elevaremos privilegios puntualmente con `sudo`.

Como administradores de sistemas, saber como crear y gestionar las cuentas de los usuarios de nuestro sistema es algo que necesitamos conocer y dominar, ya que los usuarios son las personas o entidades que van a interactuar con el servidor y van a requerir acceso a recursos y servicios específicos. Crear una cuenta de usuario no es algo difícil en Linux, involucra también crear contraseña y asignarlo a un grupo y permisos. Aquí les dejamos un ejemplo de como crear y gestionar una cuenta de usuario, para ello abriremos la máquina virtual de nuestro servidor y seguiremos los siguientes pasos:

- Para crear un usuario en Debian/Ubuntu lo más sencillo es `sudo adduser <usuario>`, que de forma interactiva crea el directorio `/home/<usuario>`, pide la contraseña y algunos datos. Si usas `useradd` directamente (disponible en todas las distros), recuerda pasar `-m` para crear el home y establecer la contraseña después con `passwd <usuario>`: `useradd` por sí solo **no** pide contraseña.

![Creación y gestión de cuentas de usuario - crear usuario](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/users-groups-management/administracion-basica-de-usuarios-imagen-1.jpg)

- Si queremos cambiar la contraseña lo hacemos con el comando `passwd` seguido del usuario de la contraseña que queremos cambiar

![Creación y gestión de cuentas de usuario - comando password](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/users-groups-management/administracion-basica-de-usuarios-imagen-2.jpg)

- Una forma de facilitar la administración de permisos sobre archivos y directorios es a través de los grupos. Podemos crear un grupo con `groupadd <grupo>` y añadir a un usuario a un grupo secundario con `usermod -aG <grupo> <usuario>`. La combinación `-aG` es importante: `-G` indica la lista de grupos suplementarios y `-a` (*append*) evita sobrescribir los grupos a los que ya pertenece el usuario. Para ver los grupos a los que pertenece un usuario usamos `groups <usuario>`.

![Creación y gestión de cuentas de usuario - crear grupos](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/users-groups-management/administracion-basica-de-usuarios-imagen-3.jpg)

![Creación y gestión de cuentas de usuario - comando usermod](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/users-groups-management/administracion-basica-de-usuarios-imagen-4.jpg)

![Creación y gestión de cuentas de usuario - usuario adm](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/users-groups-management/administracion-basica-de-usuarios-imagen-5.jpg)

- Si queremos ver los grupos que existen en el sistema podemos conseguir en la ruta /etc/group

![Creación y gestión de cuentas de usuario - grupos existentes](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/users-groups-management/administracion-basica-de-usuarios-imagen-6.jpg)

- Cuando necesitemos eliminar un usuario del sistema lo haremos con el comando userdel seguido del nombre del usuario.

![Creación y gestión de cuentas de usuario - comando userdel](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/users-groups-management/administracion-basica-de-usuarios-imagen-7.jpg)

**Es recomendable gestionar y crear los usuarios usando los privilegios de usuario sudo y no desde el usuario root ya que a la hora de un error desde el usuario root puede ser fatal para el sistema.**

> ⚠️ Recuerda que la creación y gestión de cuentas de usuario en servidores Linux debe realizarse de manera segura y siguiendo las mejores prácticas de seguridad. Esto incluye el uso de contraseñas fuertes, la asignación adecuada de permisos y la implementación de políticas de seguridad.

## Asignación de permisos y privilegios.

Como administradores de sistema, es importante saber y conocer cómo gestionar y asignar permisos y privilegios a cada usuario del sistema, ya que los permisos pueden determinar qué acciones pueden realizar los usuarios y los privilegios definen el nivel de acceso y control sobre el sistema.

Cuando manejamos un servidor una de las mejores prácticas para proteger la información es poniendo en práctica el principio del menor privilegio, el cual consiste en asignarle los permisos de accesos mínimos necesarios para que pueda desempeñar actividades en el sistema, para ello es necesario conocer sobre los permisos y cómo gestionarlos.

En Linux existen tres tipos de permisos: lectura (`r`), escritura (`w`) y ejecución (`x`). Estos permisos se asignan a tres conjuntos de usuarios: el propietario del archivo, el grupo al que pertenece el archivo y el resto de usuarios del sistema. Podemos ver los permisos de archivos y directorios con el comando `ls -l`.

![Asignación de permisos y privilegios - comando ls](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/users-groups-management/administracion-basica-de-usuarios-privilegios-imagen-1.jpg "comando ls -l nos permite visualizar permisos en los directorios o archivos")

En la siguiente imagen podemos ver como tenemos un archivo llamado `text.txt` el cual cuenta con sus permisos agrupado en tres grupos:

- Los primeros tres permisos son los permisos que tiene el propietario del archivo (“usuario"). En este caso tenemos permiso de lectura (r) y escritura (w) pero no de ejecución. rw-
- El segundo grupo de permisos son los permisos que tienen los usuarios del grupo (“departamentoIT), en este caso tenemos los mismos permisos de lectura y escritura pero no de ejecución. rw-
- El tercer grupo de de permiso son los permisos para el resto de los usuarios del sistema el cual solo podrán leer el archivo mas no podrán ni escribir o editar sobre el ni ejecutarlos

> 💡 Es normal que a todos los usuarios del sistema los separamos por grupos para que así puedan acceder únicamente a los archivos que necesitan leer, escribir o ejecutar de acuerdo al nivel de privilegios que tenga tal usuario, y así proteger información confidencial de otros departamentos de la organización, una vez que creamos un usuario, es necesario darle permisos de acuerdo a las labores que vaya a realizar en la organización.

Con el comando `chmod` podemos cambiar y otorgar permisos a los usuarios sobre un archivo.

- Si queremos dar permiso a un usuario (u), a un grupo (g) o a otros usuarios del sistema (o) colocamos la flag seguido de un + y el permiso que vayamos a asignar.
- En este caso, gestionamos permisos de lectura, escritura y ejecución solo para el propietario del archivo (u).

![Asignación de permisos y privilegios - Dar permisos a un usuario](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/users-groups-management/administracion-basica-de-usuarios-privilegios-imagen-2.jpg "Dar permisos a un usuario")

> 💡 Podemos generar permisos esenciales con los bits de ejecución setuid (suid), el bit de ejecución setgid (sgid) y el bit de ejecución sticky. El bit suid permite que un archivo se ejecute con los privilegios del propietario, mientras que el bit sgid permite que un archivo se ejecute con los privilegios del grupo. El bit sticky se utiliza principalmente en directorios para evitar que los usuarios eliminen archivos de otros usuarios

![Asignación de permisos y privilegios - bits de ejecución setuid (suid) ](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/users-groups-management/administracion-basica-de-usuarios-privilegios-imagen-3.jpg "bits de ejecución setuid (suid)")

En este caso, generamos permisos de suid de privilegio de usuario y grupo al archivo `text.txt`

Otra manera de gestionar los permisos es asignarlos con la cantidad de bits de los permisos. Tomando en cuenta que cada permiso tiene una cantidad de bits podemos sacarlos como: 

```txt
Lectura r (4)
Escritura w (2)
Ejecución x (1)
```

1. Si queremos gestionar permisos por bits esta cuenta te puede resultar útil

```txt
Lectura (r), Escritura (w), Ejecución (x)  rwx = 7
Lectura (r), Escritura (w)                 rw- = 6
Lectura (r), Ejecución (x)                 r-x = 5
Lectura (r)                                r-- = 4
Escritura (w), Ejecución (x)               -wx = 3
Escritura (w)                              -w- = 2
Ejecución (x)                              --x = 1
```

2. Colocaremos la cantidad de bits que los permisos que queramos otorgar de acuerdo a la posición de usuario, grupo y otros.

![Asignación de permisos y privilegios - Cantidad de bits de los permisos que otorgamos al usuario, al grupo u otros ](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/users-groups-management/administracion-basica-de-usuarios-privilegios-imagen-4.jpg "Cantidad de bits de los permisos que otorgamos al usuario, al grupo u otros")
    
> 💡 La asignación de permisos y privilegios en linux es esencial para así garantizar al seguridad y el control adecuado sobre los recursos del sistema
    
## Configuración de grupos y asignación de usuarios a grupos.

Saber cómo configurar y asignar un usuario a un grupo en específico es ideal cuando queremos ganar tiempo y tenemos un sistema con muchos usuarios, ya que una manera rápida de hacerlo es ir asignando a los usuarios a un grupo con los permisos de usuarios mínimos de acuerdo a su labor. Por ejemplo podemos tener un grupo de departamentoIT que pueda tener acceso ejecutar a los scripts de automatización de tareas del sistema y asi, que los usuarios de departamento de marketing no puedan tener acceso a dichos scripts.

Para ello tenemos comandos que nos pueden ayudar tales como `groupadd` para crear un grupo.

Para este ejercicio hemos creado un grupo llamado `departamentomarketing`. Una vez creado, podemos añadir al usuario al grupo con `sudo adduser <usuario> <grupo>`, seguido del nombre de usuario y del grupo al que queremos que pertenezca.

> 📝 `adduser` y `deluser` son comandos específicos de Debian/Ubuntu (son wrappers de alto nivel sobre `useradd` y `userdel`). En RHEL, CentOS Stream, Rocky y AlmaLinux no están disponibles con esta sintaxis; allí la alternativa portable para añadir a un grupo es `sudo usermod -aG <grupo> <usuario>`, y para eliminarlo, `sudo gpasswd -d <usuario> <grupo>`.

![Configuración de grupos y asignación de usuarios - comando groupadd para agregar grupos](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/users-groups-management/administracion-basica-de-usuarios-grupos-imagen-1.jpg "groupadd para agregar grupos")

![Configuración de grupos y asignación de usuarios - Adding user usuario1 to group departamentomarketing](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/users-groups-management/administracion-basica-de-usuarios-grupos-imagen-2.jpg "El usuario1 pasará a ser del grupo de departamentomarketing")

En este comando hicimos que el usuario1 pasará a ser del grupo de departamentomarketing.

Si queremos remover a un usuario del grupo lo podemos lograr con el comando deluser seguido del nombre del usuario y el grupo del cual queremos removerlo.

![Configuración de grupos y asignación de usuarios - Removing user usuario1 to group departamentomarketing](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/users-groups-management/administracion-basica-de-usuarios-grupos-imagen-3.jpg "Eliminar usuario1 del grupo de departamentomarketing")

Una forma de ver los grupos en el sistema es accediendo a la ruta /etc/group usando el comando cat. Ahí podemos ver todos los grupos que tenemos seguido de un número o identificador de grupo (gid). Por lo general, al momento de crear grupos, el sistema le asigna un gid de 1000 en adelante. Los gid menores a 100 son reservados para uso del sistema y sus grupos especiales.

![Configuración de grupos y asignación de usuarios - Comando CAT para visualizar los grupos en el sistema](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/users-groups-management/administracion-basica-de-usuarios-grupos-imagen-4.jpg "Comando CAT para visualizar los grupos en el sistema")

Si queremos modificar el gid o el nombre del grupo podemos hacerlo a través del comando groupmod seguido del nuevo gid o el nombre y el gid o nombre anterior.

![Configuración de grupos y asignación de usuarios - modificar el gid o el nombre del grupo con el comando groupmod](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/users-groups-management/administracion-basica-de-usuarios-grupos-imagen-5.jpg "modificar el gid o el nombre del grupo con el comando groupmod 'nombre nuevo o gid' + 'gid o nombre anterior' ")
