---
title: "Fundamentos de la línea de comandos"
subtitle: "Descubre los fundamentos de la línea de comandos: cómo navegar, manipular archivos y gestionar permisos en Linux. ¡Aprende desde cero en este completo tutorial!"
tags: ["linux", "linea-de-comandos"]
authors: ["blindma1den", "lorenagubaira"]

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

Las CLI pueden emplearse interactivamente, escribiendo instrucciones en alguna especie de entrada de texto, o pueden utilizarse de una forma mucho más automatizada, leyendo órdenes desde un archivo de [Scripts](https://es.wikipedia.org/wiki/Script)scripts.

Algunas Shells CLI que frecuentemente conseguimos son:

- Bash
- Bourne Shell
- Símbolo de sistema (windows)
- Zsh

## Comandos básicos de navegación y manipulación de archivos y directorios

Estos son varios comandos basicos que lo ayudaran a navegar en la terminal. 

Las flags son una manera de pasarle opciones a los comandos y asi tener algun resultado mas especifico a lo que estamos buscando.

| Comando | Flags | Función |
| --- | --- | --- |
| pwd |  | Imprime el directorio  actual de trabajo |
| cd |  | Cambiar el directorio de trabajo |
| ls |  | Listar contenido del directorio |
|  | -R | Listara todos los archivos dentro de los subdirectorios |
|  | -a | Mostrará todos los archivos ocultos |
|  | -al | Mostrará la información detallada de los archivos y directorios |
| find |  | Buscará archivos dentro de un directorio en especifico |
|  | -iname | Buscará archivos por el nombre o extension en el directorio |
|  | -type | Buscará archivos por el tipo -f (file o archivo) -d (directorio) |
|  | -syze | Filtra los archivos por su tamaño |
|  | -user, -group | Filtra los archivos por usuario o grupo propietario del archivo |
| head |  | Permite ver hasta las primeras 10 líneas de texto de un archivo |
|  | -n o -lines | Nos imprime un numero de lineas personalizado (hasta 10) |
| tail |  | Permite ver las últimas 10 líneas de texto de un archivo |
|  | -n o -lines | Nos permite ver un numero de lineas personalizado
(hasta 10) |
| cat |  | Concatena y escribe contenido de los archivos en su salida estándar, también se puede usar para el contenido de los archivos |
| cp |  | Copia archivos o directorios y su contenido.
Se coloca el nombre del archivo a copiar y el directorio destino 
cp nombrearchivo.txt /inicio/nombredeusuario/Documentos |
| mv |  | Mueve uno o mas archivos o directorio y su contenido a otro directorio
Se coloca el nombre del archivo a mover y el directorio destino 
mv nombrearchivo.txt /inicio/nombredeusuario/Documentos. |
| rm |  | Se utiliza para eliminar un archivo o directorio del sistema |
|  | -i | Pide confirmación del sistema antes de borrar un archivo |
|  | -f | Permite al sistema eliminar sin confirmacion |
|  | -r | Borra archivos y directorios de forma recursivas |
| touch |  | Crea un archivo en blanco |
| grep |  | Permite conseguir una palabra dentro de todo el archivo en especifico |
| mkdir |  | Crea un directorio |
| chmod |  | Modifica los permisos de lectura, escritura y ejecución de un archivo o directorio. |
| chown |  | Cambia la propiedad de un archivo, directorio o enlace simbólico a un nombre de usuario específico. |
| kill |  | terminar manualmente un proceso que no responde. |
| sudo |  | Ejecutar un comando como superusuario 
Se pedirá contraseña para confirmar |

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

- r-4
- w-2
- x-1

Si sumamos los permisos daría 7. Para hacer la asignación tenemos que sumar los números de los permisos que queremos otorgar

- 7 = rwx
- 6 = rw-
- 5 = r-x
- 4 = r–
- 3 = -wx
- 2 = -w-
- 1 = –x

Todos los permisos lo podemos cambiar con el comando chmod seguido de los octetos y o permisos que queramos otorgar:

**chmod 437 file**

esto se resume a otorgar permiso de lectura al usuario propietario, premios de lectura y ejecución al resto de los usuarios del grupo y permiso de lectura, escritura al resto de los usuarios del sistema

```bash
r---wxrwx 1 user group 0 sep 17 10:53 file
```

## 💡Laboratorio: Comando básico de navegación y manipulación de archivos y directorios

Abrimos nuestro intérprete de comandos y comienza a explorar por los distintos comandos básicos que les dejamos. 

Sientete libre tambien de experimentar con la asignacion de permisos a usuario y archivos 
