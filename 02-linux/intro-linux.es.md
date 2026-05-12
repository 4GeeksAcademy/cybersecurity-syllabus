---
title: Introducción a Linux
tags:
  - linux
  - sistemas operativos
authors:
  - blindma1den
  - lorenagubaira
description: >-
  Descubre los fundamentos de Linux: seguridad, gestión de usuarios y más.
  Aprende a proteger tu sistema y aprovecha el poder del software libre.
  ¡Empieza ahora!
---
## Qué es Linux y su importancia en el mundo de la informática

A pesar de lo que generalmente se escucha sobre Linux, en realidad se trata de un **kernel** (núcleo) que actúa como intermediario entre el hardware y el software de usuario. De forma simplificada, Linux es el componente que gestiona los recursos del hardware — CPU, memoria, dispositivos — y permite que los programas se ejecuten sobre él. Fue diseñado siguiendo los principios del sistema operativo UNIX.

Este núcleo fue desarrollado por Linus Torvalds, quien en 1991 comenzó a trabajar en un núcleo de sistema operativo gratuito inspirado en UNIX. Tomó como referencia MINIX (un sistema educativo creado por Andrew S. Tanenbaum) y desarrolló un núcleo monolítico. Con la ayuda de colaboradores a través de Internet, publicó la primera versión, Linux 0.01.

Actualmente Linux es un núcleo monolítico con soporte para módulos cargables. Los controladores de dispositivos y las extensiones del núcleo normalmente se ejecutan en un espacio privilegiado conocido como anillo 0 (*ring 0*), con acceso irrestricto al hardware, aunque algunos controladores pueden ejecutarse en espacio de usuario.

En 1992, el núcleo Linux se combinó con las herramientas del proyecto GNU, iniciado por Richard Stallman en 1983. El proyecto GNU buscaba crear un sistema operativo completo de software libre, pero carecía de un núcleo funcional. La unión de ambos proyectos dio lugar a GNU/Linux, una familia de sistemas operativos tipo UNIX compuestos por software libre y de código abierto.

Entre los componentes que tenemos dentro del sistema GNU/Linux podemos conseguir:

- Un cargador de arranque el cual carga el núcleo de Linux en la memoria principal de la computadora cuando se enciende y después que se realiza la inicialización del firmware, lo podemos conseguir como GNU Grub, LILO, o SYSLINUX.
- Un programa de inicio el cual es el primer proceso lanzado por el núcleo Linux y se en él se encuentran todos los procesos que se inician a través del init como los servicios del sistema y las solicitudes de inicio de sesión.
- Las bibliotecas de software que contienen código que pueden utilizar los procesos en ejecución, también puede incluir una biblioteca estándar C la cual es necesaria para ejecutar todos los programas C en un sistema informático.
- Un sistema de gestión de paquetes, con un formato de paquetes específico. Alternativamente, los paquetes se pueden compilar a partir de archivos *tar binarios o* fuente.
- Programas de interfaz de usuario como shells de comandos/órdenes o gestores de ventanas.

## Diferencias entre Linux y otros sistemas operativos

Linux es un sistema multitarea real y multiusuario. Posee un esquema de seguridad basado en usuarios y permisos de lectura, escritura y ejecución asignados a archivos y directorios. Cada usuario es propietario de sus archivos y, por defecto, otros usuarios no pueden acceder a ellos. Este modelo de permisos reduce significativamente la propagación de malware entre cuentas de usuario, aunque no la elimina por completo.

| Característica | Windows | Linux |
| --- | --- | --- |
| Tipo de sistema operativo | Comercial (licencia de pago) | Núcleo de código abierto, distribuciones gratuitas y comerciales |
| Estabilidad | Estable en versiones recientes (Windows 10/11, Server) | Alta estabilidad, especialmente en servidores |
| Interfaz gráfica | Interfaz unificada y pulida | Variedad de entornos de escritorio (GNOME, KDE, XFCE, etc.) |
| Apto para principiantes | Sí, interfaz gráfica intuitiva | Distribuciones como Ubuntu facilitan la entrada, pero el dominio requiere línea de comandos |
| Seguridad | Modelo de permisos mejorado desde Vista/UAC; mayor superficie de ataque por cuota de mercado | Modelo de permisos robusto por defecto; menor superficie de ataque en escritorio, no invulnerable |
| Actualizaciones | Automatizadas vía Windows Update | Gestores de paquetes potentes (`apt`, `dnf`, `pacman`), actualizaciones controladas por el usuario |

### Ventajas y beneficios de utilizar Linux

El hecho de que es *software libre*, es decir, que junto con el sistema, se puede obtener el código fuente de cualquier parte del mismo y modificarlo a gusto. Ésto da varias ventajas, por ejemplo:

- La posibilidad de auditar *qué hace* un programa inspeccionando su código fuente, lo que aumenta la transparencia y la confianza en el software.
- La licencia GPL permite a cualquier desarrollador modificar y mejorar cualquier parte del sistema, lo que contribuye a una alta calidad del software incluido en GNU/Linux.
- El mantenimiento por una gran comunidad de programadores y usuarios alrededor del mundo permite una respuesta rápida ante errores y vulnerabilidades descubiertos.

Además de las ventajas anteriormente enumeradas, GNU/Linux es ideal para su utilización en un ambiente de trabajo, dos razones justifican esto:

- Al ser software libre, no existe el costo de las licencias, y una copia del sistema GNU/Linux puede instalarse en tantas computadoras como se necesite.
- Existen utilidades para el trabajo en oficina, que son compatibles con las herramientas de la serie MS-Office.
