---
title: "Introducción a Linux"
subtitle: "Descubre los fundamentos de Linux: seguridad, gestión de usuarios, contraseñas robustas y cortafuegos. Aprende cómo proteger tu sistema y más."
tags: ["linux"]
authors: ["blindma1den", "lorenagubaira"]

---

## Qué es Linux y su importancia en el mundo de la informática

A pesar de a lo que generalmente puedas escuchar sobre linux, este en realidad se trata de un núcleo o **kernel** que puede controlar a un hardware, una manera más sencilla de explicarlo es que Linux es un conjuntos de drivers necesarios para usar un dispositivo como una computadora o una laptop. Este se creó como un núcleo semejante al de un sistema operativo UNIX.

Este núcleo fue desarrollado con Linus Torvalds cuando en 1991 comenzó a trabajar con unas ideas para un núcleo de un sistema operativo gratuito similar a unix, por lo que tomó como base el sistema Minix como un clon de Unix e hizo un núcleo monolítico y así con ayuda de colaboradores, sacar la primera versión linux 0.01.

Actualmente Linux es un núcleo monolítico híbrido con controladores de dispositivos y extensiones del núcleo que normalmente se ejecutan en un espacio privilegiado conocido como anillo 0, con acceso irrestricto al hardware, aunque algunos se ejecutan en espacio de usuario.

En 1992 los desarrolladores del núcleo Linux, comenzaron a trabajar con el proyecto GNU, desarrollado por Richard Stallman en 1983 y así crear GNU/Linux, una familia de sistemas operativos tipo Unix compuesto por software libre y de código abierto buscando una solución de libre distribución de los sistemas operativos frustrado por la concesión de licencias de uso que utilizaba MINIX.

Entre los componentes que tenemos dentro del sistema GNU/Linux podemos conseguir:

- Un cargador de arranque el cual carga el núcleo de Linux en la memoria principal de la computadora cuando se enciende y después que se realiza la inicialización del firmware, lo podemos conseguir como GNU Grub, LILO, o SYSLINUX.
- Un programa de inicio el cual es el primer proceso lanzado por el núcleo Linux y se en él se encuentran todos los procesos que se inician a través del init como los servicios del sistema y las solicitudes de inicio de sesión.
- Las bibliotecas de software que contienen código que pueden utilizar los procesos en ejecución, también puede incluir una biblioteca estándar C la cual es necesaria para ejecutar todos los programas C en un sistema informático.
- Un sistema de gestión de paquetes, con un formato de paquetes específico. Alternativamente, los paquetes se pueden compilar a partir de archivos *tar binarios o* fuente.
- Programas de interfaz de usuario como shells de comandos/órdenes o gestores de ventanas.

## Diferencias entre Linux y otros sistemas operativos

Linux a diferencia de Windows, es multitarea real, y multiusuario, posee un esquema de seguridad basado en usuarios y permisos de lectura, escritura y ejecución establecidos a los archivos y directorios. Esto significa que cada usuario es propietario de sus archivos, y otro usuario no puede acceder a estos archivos. Esta propiedad no permite el contagio de virus entre archivos de diferentes usuarios.

| Característica | Windows | Linux |
| --- | --- | --- |
| Tipo de sistema operativo | Comercial (se vende y se compra) | Código abierto, descargable y modificable de forma gratuita |
| Estabilidad | Poco estable | Más estable |
| Interfaz gráfica | Alta tecnología pero poco estable | Variedad de interfaces, manejo más complejo |
| Apto para principiantes | Sí, gracias a interfaces gráficas intuitivas | Más complejo, requiere familiaridad con la línea de comandos |
| Seguridad | Frecuentes fallos de seguridad y vulnerabilidades | Raramente amenazado por fallos de seguridad |
| Actualizaciones | Sencillas y automatizadas | En ocasiones pueden ser complejas |

### Ventajas y beneficios de utilizar Linux

El hecho de que es *software libre*, es decir, que junto con el sistema, se puede obtener el código fuente de cualquier parte del mismo y modificarlo a gusto. Ésto da varias ventajas, por ejemplo:

- La seguridad de saber *qué hace* un programa tan solo viendo el código fuente, o en su defecto, tener la seguridad que al estar el código disponible,
- La libertad que provee la licencia GPL permite a cualquier programador modificar y mejorar cualquier parte del sistema, ésto da como resultado que la calidad del software incluido en GNU/Linux sea muy buena.
- El hecho de que el sistema sea mantenido por una gran comunidad de programadores y usuarios alrededor del mundo, provee una gran velocidad de respuesta ante errores de programas que se van descubriendo, que ninguna compañía comercial de software puede igualar.

Además de las ventajas anteriormente enumeradas, GNU/Linux es ideal para su utilización en un ambiente de trabajo, dos razones justifican esto:

- Al ser software libre, no existe el costo de las licencias, y una copia del sistema GNU/Linux puede instalarse en tantas computadoras como se necesite.
- Existen utilidades para el trabajo en oficina, que son compatibles con las herramientas de la serie MS-Office.
