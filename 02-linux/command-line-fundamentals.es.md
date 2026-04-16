---
title: Fundamentos de la línea de comandos
tags:
  - linux
  - linea-de-comandos
authors:
  - blindma1den
  - lorenagubaira
description: >-
  Descubre los fundamentos de la línea de comandos en Linux. Aprende a navegar,
  manipular archivos y gestionar permisos. ¡Comienza tu viaje ahora!
---
## Introducción a la terminal y el intérprete de comandos

En IT es normal usar una terminal o intérprete de comandos para comunicarnos con nuestra computadora o laptop, estos comandos nos pueden ayudar a tener una comunicación directa con nuestra computadora, ya que estamos dictando una orden capaz de ser interpretada y procesada por el lenguaje informático, y así tener una importancia con el nivel de interacción con la PC. En otras palabras, los comandos como forma de interacción, pueden rescatarnos cuando el sistema está colapsado.

La terminal la podemos definir como un dispositivo informático que permite a un usuario interactuar con un sistema informático, normalmente para realizar tareas como ejecutar programas, entrar y salir del sistema o realizar búsquedas en la web.

La terminal de informática ha sido una herramienta clave para programadores y expertos en informática desde hace años. Esta potente herramienta nos permite interactuar con nuestros sistemas de computación, permitiendo que los usuarios realicen diversas funciones como ejecutar comandos, actualizar el software del sistema o incluso crear y modificar archivos.

Una intérprete de comandos o Shell es un programa informático que tiene la capacidad de traducir las órdenes que introducen los usuarios, mediante un conjunto de instrucciones facilitadas por el mismo, directamente al núcleo y al conjunto de herramientas que forman el sistema operativo. Las órdenes se introducen siguiendo la sintaxis incorporada por dicho intérprete, dentro del entorno proporcionado por la terminal, mediante un inductor que espera que sean introducidos los comandos o instrucciones

```bash
PROMPT>nombrecomando argumento/s /ruta/hacia/el/o/los/ficheros
```

Al ingresar la orden con la tecla 'Intro', el intérprete analiza la secuencia de caracteres ingresada y, si la sintaxis de la orden es correcta, la ejecuta, recurriendo para ello a las funciones que ofrece el sistema operativo o el programa que representa, bien sea un gestor de datos de banco, una sesión de FTP, de ssh, etc. La respuesta al usuario se representa en el monitor o en forma de segundo plano. Se trabaja de manera interactiva, es decir, usuario y máquina se comunican de forma sucesiva.

La interfaz de línea de comandos o interfaz de línea de órdenes (CLI) es un tipo de interfaz de usuario de computadora que permite a los usuarios dar instrucciones a algún programa informático o al sistema operativo por medio de una línea de texto simple

Las CLI pueden emplearse interactivamente, escribiendo instrucciones en alguna especie de entrada de texto, o pueden utilizarse de una forma mucho más automatizada, leyendo órdenes desde un archivo de [scripts](https://es.wikipedia.org/wiki/Script).

Algunas Shells CLI que frecuentemente conseguimos son:

- Bash
- Bourne Shell
- Símbolo de sistema (windows)
- Zsh

## Comandos básicos de navegación y manipulación de archivos y directorios

En la lección de [Archivos y directorios](./files-directories.es.md) vimos los comandos fundamentales para navegar y manipular el sistema de archivos: `pwd`, `cd`, `ls`, `cat`, `head`, `tail`, `cp`, `mv`, `rm`, `touch` y `mkdir`. Aquí ampliamos con comandos adicionales que complementan el trabajo en la terminal.

Las *flags* son opciones que se pasan a los comandos para obtener un resultado más específico.

| Comando | Flags | Función |
| --- | --- | --- |
| `find` | | Busca archivos dentro de un directorio según diferentes criterios |
| | `-iname` | Busca archivos por nombre (insensible a mayúsculas/minúsculas) |
| | `-type` | Filtra por tipo: `-type f` (archivo) o `-type d` (directorio) |
| | `-size` | Filtra los archivos por su tamaño |
| | `-user`, `-group` | Filtra los archivos por usuario o grupo propietario |
| `grep` | | Busca un patrón de texto dentro de uno o varios archivos |
| `chmod` | | Modifica los permisos de lectura, escritura y ejecución de un archivo o directorio |
| `chown` | | Cambia el propietario de un archivo, directorio o enlace simbólico |
| `kill` | | Envía una señal a un proceso (por defecto SIGTERM para terminarlo) |
| `sudo` | | Ejecuta un comando con privilegios de superusuario (pedirá contraseña) |

## Gestión de permisos de archivos y directorios

En una distribución de linux, los archivos y directorios se pueden ejecutar dependiendo del los permisos de usuario que tenga. Podemos ver los permisos que puede tener un directorio con el comando **ls -l**

| drwxr-xr-x 1 user user  1046 sep 14 16:24  Descargas |
| --- |
| drwxr-xr-x 1 user user  610 sep 16 19:03  Desktop |
| drwxr-xr-x 1 user user  94 sep 15 08:59  Documentos |
| drwxr-xr-x 1 user user 42 ago 27 11:38  Imágenes |
| drwxr-xr-x 1 user user 0 ago 18 19:20  Música |

Hablemos un poco mas de esto…

La primera letra indicará si es un directorio o un archivo, en el caso de ser un directorio tendrá la letra d, si no tendría un (-).

Los permisos pueden ser:

- r - lectura
- w - escritura
- x - ejecución

**Los permisos se dividen en 3 partes:**

1. Los permisos del dueño del archivo siendo las primeras 3 letras
2. Los permisos de usuario de los miembros del grupo siendo las segundas 3 letras
3. los permisos de usuario para los demás miembros del grupo siendo las últimas 3 letras

```bash
rw-r--r-- 1 user group	0 sep 17 10:53 file
```

Esta descripción indica que es un archivo al tener un (-) en el inicio

Para el usuario propietario sólo tendrá permiso de lectura y escritura y para el resto de los usuarios del grupo y del sistema sólo tendrá permiso de lectura, no podrán ni escribir ni ejecutar el archivo.

```bash
drwxr-xr-x 1 user user   24 sep 15 09:04 network
```

El archivo es un directorio, donde el usuario propietario tendrá permisos de escritura, lectura y ejecución, los usuarios del grupo tendrán permisos de lectura y ejecución al igual que los usuarios del sistema.

Otra forma de hacer la gestión de permisos de usuario en linux es por sus octetos

Cada permiso tiene una cantidad:

- `r` = 4
- `w` = 2
- `x` = 1

Para asignar permisos, se suman los valores de los permisos deseados para cada grupo (propietario, grupo, otros):

- 7 = `rwx` (4+2+1)
- 6 = `rw-` (4+2)
- 5 = `r-x` (4+1)
- 4 = `r--` (4)
- 3 = `-wx` (2+1)
- 2 = `-w-` (2)
- 1 = `--x` (1)
- 0 = `---` (sin permisos)

Todos los permisos se pueden cambiar con el comando `chmod` seguido de los tres dígitos octales:

```bash
chmod 755 script.sh
```

Esto asigna al propietario permisos de lectura, escritura y ejecución (`rwx` = 7), y al grupo y a otros usuarios permisos de lectura y ejecución (`r-x` = 5):

```bash
-rwxr-xr-x 1 user group 0 sep 17 10:53 script.sh
```

Otro ejemplo habitual es `chmod 644`, que se usa comúnmente para archivos regulares: lectura y escritura para el propietario, solo lectura para grupo y otros.

## Laboratorio: Comandos básicos de navegación y manipulación de archivos y directorios

Abre tu intérprete de comandos y experimenta con los distintos comandos básicos que hemos visto.

Practica también con la asignación de permisos a usuarios y archivos.
