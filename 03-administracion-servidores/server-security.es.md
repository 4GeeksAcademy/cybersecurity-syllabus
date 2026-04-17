---
title: Configuración de seguridad del servidor
tags:
  - servidores
authors:
  - blindma1den
  - lorenagubaira
description: >-
  Optimiza la seguridad de tu servidor Linux con nuestra guía sobre
  configuración de firewall, gestión de usuarios y registros de auditoría.
  ¡Descubre cómo proteger tu sistema!
---
## Configuración del firewall

Los firewall son una pieza clave en la seguridad de nuestros servidores, por lo que como administradores de sistemas es necesario que sepamos cómo configurarlo. Recordemos que un firewall actúa como una barrera entre tu servidor y posibles amenazas externas, controlando el tráfico de red y permitiendo o bloqueando conexiones según las reglas establecidas.

En Linux, durante años el motor de filtrado de paquetes del kernel fue `iptables`; hoy el reemplazo moderno es `nftables`, aunque muchas distribuciones siguen ofreciendo una interfaz `iptables` compatible por encima. Como configurar reglas a bajo nivel es complejo, las distribuciones suelen ofrecer frontends más amigables: **UFW** (Uncomplicated Firewall) en Debian/Ubuntu, y **firewalld** en RHEL, CentOS Stream, Rocky Linux, AlmaLinux y Fedora.

Para configurar un firewall utilizando UFW, puedes utilizar comandos sencillos que simplifican el proceso. Por ejemplo, para permitir el tráfico SSH en tu servidor, puedes ejecutar el comando `sudo ufw allow ssh`. Esto abrirá el puerto 22, que es el puerto predeterminado para SSH, y permitirá las conexiones entrantes.

Además de permitir conexiones específicas, también puedes bloquear puertos no deseados utilizando UFW. Por ejemplo, para bloquear el tráfico en el puerto 80, puedes ejecutar el comando `sudo ufw deny 80`. Esto evitará que cualquier conexión entrante o saliente utilice el puerto 80.

Otra herramienta comúnmente utilizada para la configuración de firewall en Linux es firewalld. Firewalld proporciona una interfaz de línea de comandos y una interfaz gráfica para administrar las reglas de firewall. Puedes utilizar comandos como `sudo firewall-cmd --add-service=ssh` para permitir el tráfico SSH, o `sudo firewall-cmd --remove-service=http` para eliminar una regla existente.

Además de permitir o bloquear puertos específicos, tanto UFW como firewalld permiten configurar reglas más avanzadas, como el filtrado por dirección IP, el enmascaramiento de direcciones o la limitación de conexiones simultáneas. Estas características adicionales te permiten personalizar aún más la configuración de tu firewall según tus necesidades específicas.

> 📖 Es importante tener en cuenta que, al configurar un firewall, es fundamental comprender las implicaciones de las reglas establecidas. Configurar un firewall de manera incorrecta puede bloquear conexiones legítimas o permitir el acceso no autorizado. Por lo tanto, es recomendable tener un buen conocimiento de las reglas y realizar pruebas exhaustivas antes de implementar un firewall en un entorno de producción.

Para esta práctica configuraremos ambos, UFW:

## Instalación de UFW

1. El primer paso será actualizar los paquetes del sistema con sudo apt update y sudo apt upgrade.

![Configuración del firewall - actualizar paqetes](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/server-security/server-security-image-1.jpg)

2. Una vez actualizamos, procedemos a instalar nuestro firewall con el comando `sudo apt install UFW`
    ![Configuración del firewall - instalar nuestro firewall sudo apt install UFW](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/server-security/server-security-image-2.jpg)

3. Validamos el status actual del firewall con el comando `sudo ufw status`
    
![Configuración del firewall - Verificar estado con sudo ufw status](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/server-security/server-security-image-3.jpg)
    
> 👉 Podemos ver que el firewall está inactivo o deshabilitado por lo que el siguiente paso será habilitarlo.

4. Habilitamos el firewall con el comando `sudo ufw enable`

![Configuración del firewall - comando sudo ufw enable](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/server-security/server-security-image-4.jpg)

5. Una vez colocado el comando, revisamos nuevamente su status con sudo ufw status. Si queremos desactivar el firewall usamos el comando sudo `ufw disable`.

6. Configuramos las políticas en el firewall, por defecto, UFW tiene reglas para negar todas las conexiones entrantes y solo permite las conexiones salientes al servidor, por lo que nadie podría acceder al servidor y los servicios o aplicaciones en ejecución, estas reglas podemos conseguirlas dentro de la ruta.

Para editar las reglas usamos los comandos `sudo ufw default deny incoming` y `sudo ufw default allow outgoing`.
    
![Configuración del firewall - Edita las reglas con sudo ufw default](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/server-security/server-security-image-5.jpg)
    
> 👉 Cuando instalamos un paquete a través de nuestro gestor APT, se incluye un perfil de aplicación en el directorio /etc/ufw/applications.d el cual define el servicio y mantiene la configuración de UFW activa.
    
7. Para enumerar todos los perfiles de aplicaciones usamos el comando `sudo ufw app list`
    
    ![Configuración del firewall - comando sudo ufw app list](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/server-security/server-security-image-6.jpg)

Si queremos obtener más información sobre un perfil en específico y las reglas definidas para este, usamos el comando `sudo ufw app info “Aplicación”`.

8. El siguiente paso habilitar los servicios o puertos que queramos permitir en el firewall.
    
![Configuración del firewall - comando sudo ufw app info](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/server-security/server-security-image-7.jpg)

9. Si queremos permitir servicios como SSH para conectarnos de forma remota usamos el comando `sudo ufw allow ssh`, en el caso que queramos usar un puerto SSH personalizado, usamos el comando `sudo ufw allow puerto` y si deseamos bloquear una conexión ssh usamos el comando `sudo ufw deny ssh/tcp`.
    
![Configuración del firewall - comando sudo ufw deny ](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/server-security/server-security-image-8.jpg)
    
![Configuración del firewall - sudo ufw allow puertoInicial](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/server-security/server-security-image-9.jpg)

![Configuración del firewall - sudo ufw allow ssh](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/server-security/server-security-image-10.jpg)
    
10. Si queremos permitir el acceso de aplicaciones que usan un rango de puertos, usamos el comando `sudo ufw allow <start_port:end_port>`

![Configuración del firewall - sudo ufw allow range](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/server-security/server-security-image-11.jpg)
    
11. También tenemos la opción de permitir acceso de una sola dirección IP de sistema, para ello ejecutamos el comando `sudo ufw allow from <ip_address>`, también podemos especificar que queremos recibir el tráfico de un puerto en especifico `sudo ufw allow direccionIP to any port <port_number>`
    
    ![Configuración del firewall - sudo ufw allow direccionIP to any port #numeroPuerto](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/server-security/server-security-image-12.jpg)
    
- Si queremos eliminar las reglas del firewall lo primero que tenemos que hacer es enumerar las reglas con el comando `sudo ufw status numbered` y luego eliminamos la regla usando el comando `sudo ufw delete <rule_number>`, otra forma sería con el comando `sudo ufw delete <reglaUFW>`.
    
![Configuración del firewall - sudo ufw status numbered](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/server-security/server-security-image-13.jpg)

## Gestión de usuarios y autenticación segura

Hemos hablado previamente de la gestión y autenticación segura de usuarios en Linux, estas prácticas garantizan la seguridad y protección de los sistemas, evitando accesos no autorizados y protegiendo la información confidencial.

En Linux, cada usuario tiene una cuenta única que le permite acceder al sistema y realizar tareas específicas. La gestión de usuarios implica la creación, modificación y eliminación de estas cuentas de usuario.

Para crear un nuevo usuario en Linux, puedes utilizar el comando `useradd` seguido del nombre de usuario deseado. Por ejemplo, `sudo useradd <username>` creará una nueva cuenta de usuario en el sistema. Luego, puedes establecer una contraseña para el usuario utilizando el comando `passwd <username>`. Es importante utilizar contraseñas seguras que combinen letras mayúsculas y minúsculas, números y caracteres especiales.

Además de crear usuarios, también es importante asignarles los permisos adecuados. En Linux, los permisos se gestionan a través del sistema de archivos y los grupos de usuarios. Puedes utilizar comandos como `chown` y `chmod` para cambiar la propiedad y los permisos de los archivos y directorios.

La autenticación segura es otro aspecto crucial en la gestión de usuarios en servidores Linux. El uso de contraseñas seguras es solo el primer paso. También se recomienda utilizar autenticación de dos factores (2FA) para agregar una capa adicional de seguridad. Esto implica el uso de un segundo método de autenticación, como un código generado por una aplicación en el teléfono móvil, junto con la contraseña tradicional.

Además, es importante asegurarse de que los servicios de autenticación, como SSH (Secure Shell), estén configurados correctamente. Puedes modificar la configuración de SSH en el archivo `/etc/ssh/sshd_config` para permitir sólo conexiones seguras y deshabilitar el acceso de root remoto.

> 👉 Otra práctica recomendada es utilizar claves de autenticación en lugar de contraseñas para acceder a los servidores. Esto implica generar un par de claves pública y privada, donde la clave privada se almacena en el cliente y la clave pública se agrega al archivo `~/.ssh/authorized_keys` en el servidor. Esto permite una autenticación sin contraseña y es más seguro que el uso de contraseñas.

Para configurar nuestra clave pública y privada para autenticarnos dentro del servidor seguimos los siguientes pasos:

1. Creamos nuestras claves pública y privada con el comando `ssh-keygen`, despues nos pedira la ruta donde almacenar nuestra clave SSH, podemos aceptar la ruta que nos da por defecto, despues pedira una frase de contraseña la cual agrega una capa de seguridad adicional para evitar el inicio de sesión de usuarios no autorizados.

![Configuración del firewall - crear clave publica y privada con ssh](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/server-security/server-security-image-14.jpg)

2. El próximo paso será copiar la clave pública al nuestro servidor, para ello usaremos la herramienta ssh-copy-id con el siguiente comando `ssh-copy-id <username>@<remote_host>`.

3. Procedemos a conectarnos a nuestro usuario ssh con el comando `ssh <username>@<hostname>` una vez introducido el comando, pedirán la frase de autenticación, la autenticación basada en claves se realizó con éxito, podemos proteger más a nuestro sistema inhabilitando la autenticación con contraseña.

![Configuración del firewall - conectarnos con nuestro ssh](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/server-security/server-security-image-15.jpg)

![Configuración del firewall - ssh usuario](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/server-security/server-security-image-16.jpg)

4. Aunque tengamos la cuenta SSH configurada, el mecanismo de autenticación basado en contraseña sigue activo, por lo que vamos a modificar el archivo `/etc/ssh/sshd_config` con nuestro editor de código.
5. Localizamos la directiva `PasswordAuthentication`, la descomentamos (quitando el `#` del inicio de la línea) y establecemos su valor a `no`.
    
![Configuración del firewall - PasswordAuthentication](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/server-security/server-security-image-17.jpg)

6. Reiniciamos el servicio SSH con `sudo systemctl restart ssh` (el nombre del servicio es `ssh` en Debian/Ubuntu y `sshd` en RHEL/Rocky/AlmaLinux/Fedora).

## Configuración de registros de auditoría (logs) del sistema.

La configuración de registros de auditoría, también conocidos como logs, es una práctica esencial en la administración de sistemas para monitorear y registrar eventos importantes del sistema operativo y las aplicaciones. Estos registros proporcionan información valiosa para el análisis de problemas, la detección de intrusiones y el seguimiento de actividades en el sistema.

En Linux, los registros de auditoría se encuentran en el directorio `/var/log` y contienen información detallada sobre diversos aspectos del sistema, como el inicio y apagado del sistema, errores del kernel, actividades de red, registros de aplicaciones y mucho más.

La configuración de los registros de auditoría se realiza a través del archivo de configuración del demonio de registro, que puede variar según la distribución de Linux utilizada. En distribuciones como Ubuntu y Debian, el archivo de configuración principal es `/etc/rsyslog.conf`, mientras que en distribuciones como Red Hat y CentOS, se utiliza `/etc/rsyslog.d/*.conf` para configurar los registros.

En estos archivos de configuración, puedes especificar qué eventos deseas registrar y dónde deseas almacenar los registros. Puedes definir reglas para filtrar eventos específicos, establecer niveles de registro (como información, advertencia o error) y redirigir los registros a archivos específicos o enviarlos a un servidor de registro centralizado.

> ⚠️ Es importante tener en cuenta que la configuración de los registros de auditoría debe equilibrar la cantidad de información registrada con la capacidad de almacenamiento disponible. Registrar demasiados eventos puede llenar rápidamente el espacio en disco y dificultar el análisis de los registros. Por otro lado, registrar muy pocos eventos puede dejar pasar información importante para la detección de problemas o actividades sospechosas.

Además de la configuración de los registros de auditoría, es importante monitorear y analizar regularmente los registros para identificar posibles problemas o actividades maliciosas. Puedes utilizar comandos y herramientas como "grep" o "awk" para buscar eventos específicos en los registros, o utilizar herramientas de monitoreo y análisis de registros más avanzadas, como "Logstash" o "Splunk".
