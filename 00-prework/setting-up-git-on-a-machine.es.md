---
title: "Configuración de Git en una máquina"
subtitle: "Guía paso a paso para configurar y utilizar Git en tu máquina local o virtual. Aprende a verificar la instalación, configurar tus credenciales de GitHub, y trabajar con repositorios."
tags: ["ciberseguridad"]
authors: ["rosinni"]

---

# Configuración de Git en una máquina

Durante las distintas prácticas que estaremos realizando, te vamos a pedir que descargues algunos repositorios a tu máquina anfitriona o a algunas de tus máquinas virtuales. De esta forma, vamos a poder llevar a cabo algunas verificaciones para hacer que tu aprendizaje sea exitoso. A continuación, te detallamos un paso a paso de cómo hacer esa configuración por primera vez en cualquiera de tus máquinas.

## 1. Verificar la Instalación
Lo primero que haremos será verificar que Git esté correctamente instalado:

```bash
git --version
```

En caso de no ser así, deberemos hacer la descarga en la página oficial de git.

## 2. Configurar Git

Después de haber comprobado que Git está instalado, necesitas configurarlo con tu información de usuario de GitHub. Esta información se usa para identificar los commits que hagas. Configura tu nombre y correo electrónico con los siguientes comandos:

```bash
git config --global user.name "usuario de github"
git config --global user.email "email de github"
```

## 3. Ver todas las configuraciones de Git:

```bash
git config --list
```

¡Listo, ya has configurado Git!

## Clonar un Repositorio

Cuando tengas que clonar algún repositorio en tu máquina, deberás posicionarte con la línea de comando en la ruta donde quieras guardar el proyecto y especificar el siguiente comando:

```bash
git clone https://github.com/git/git.git
```

Esto creará una copia de un repositorio remoto en tu máquina local o virtual.

## ¿Cómo puedes trabajar el repositorio?
Para poder trabajar en el repositorio clonado o creado en tu máquina, deberás usar los siguientes comandos:

```bash
git add . # Agrega todos los archivos que han sido creados o modificados
git commit -m "Agregar archivo README" # Confirma los cambios
git push origin <nombre_de_rama> # Envía los cambios al repositorio remoto en GitHub
```

>   El nombre de la rama suele ser main o master

Estos pasos deberían ayudarte a configurar y usar Git en tu máquina virtual.