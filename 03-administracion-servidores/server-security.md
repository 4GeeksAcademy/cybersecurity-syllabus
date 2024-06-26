---
title: "Configuración de seguridad del servidor"
subtitle: "Optimiza la seguridad de tu servidor: Configuración del firewall, gestión de usuarios y registros de auditoría en Linux. Aprende paso a paso."
tags: ["servidores"]
authors: ["blindma1den", "lorenagubaira"]

---

## **Configuración del firewall**

Los firewall son una pieza clave en la seguridad de nuestros servidores, por lo que como administradores de sistemas es necesario que sepamos cómo configurarlo. Recordemos que un firewall actúa como una barrera entre tu servidor y posibles amenazas externas, controlando el tráfico de red y permitiendo o bloqueando conexiones según las reglas establecidas.

En Linux, uno de los firewalls más utilizados es iptables, que es una herramienta de filtrado de paquetes integrada en el kernel del sistema operativo. Sin embargo, iptables puede resultar complejo de configurar debido a su sintaxis y reglas. Por esta razón, muchas distribuciones de Linux han adoptado herramientas de administración de firewall más amigables, como UFW (Uncomplicated Firewall) en Ubuntu y CentOS, o firewalld en Fedora.

Para configurar un firewall utilizando UFW, puedes utilizar comandos sencillos que simplifican el proceso. Por ejemplo, para permitir el tráfico SSH en tu servidor, puedes ejecutar el comando "sudo ufw allow ssh". Esto abrirá el puerto 22, que es el puerto predeterminado para SSH, y permitirá las conexiones entrantes.

Además de permitir conexiones específicas, también puedes bloquear puertos no deseados utilizando UFW. Por ejemplo, para bloquear el tráfico en el puerto 80, puedes ejecutar el comando "sudo ufw deny 80". Esto evitará que cualquier conexión entrante o saliente utilice el puerto 80.

Otra herramienta comúnmente utilizada para la configuración de firewall en Linux es firewalld. Firewalld proporciona una interfaz de línea de comandos y una interfaz gráfica para administrar las reglas de firewall. Puedes utilizar comandos como "**sudo firewall-cmd --add-service=ssh**" para permitir el tráfico SSH, o "**sudo firewall-cmd --remove-service=http**" para eliminar una regla existente.

Además de permitir o bloquear puertos específicos, tanto UFW como firewalld permiten configurar reglas más avanzadas, como el filtrado por dirección IP, el enmascaramiento de direcciones o la limitación de conexiones simultáneas. Estas características adicionales te permiten personalizar aún más la configuración de tu firewall según tus necesidades específicas.

> 📖 Es importante tener en cuenta que, al configurar un firewall, es fundamental comprender las implicaciones de las reglas establecidas. Configurar un firewall de manera incorrecta puede bloquear conexiones legítimas o permitir el acceso no autorizado. Por lo tanto, es recomendable tener un buen conocimiento de las reglas y realizar pruebas exhaustivas antes de implementar un firewall en un entorno de producción.

Para esta práctica configuraremos ambos, UFW:

Instalación de UFW:

1. El primer paso será actualizar los paquetes del sistema con sudo apt update y sudo apt upgrade.

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image77.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image77.png)

1. Una vez actualizamos, procedemos a instalar nuestro firewall con el comando **sudo apt install UFW**
2. Validamos el status actual del firewall con el comando **sudo ufw status**
    
![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image78.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image78.png)
    
3. Podemos ver que el firewall está inactivo o deshabilitado por lo que el siguiente paso será habilitarlo.
4. Habilitamos el firewall con el comando **sudo ufw enable**
    
![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image79.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image79.png)
    

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image80.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image80.png)

1. Una vez colocado el comando, revisamos nuevamente su status con sudo ufw status

**Si queremos desactivar el firewall usamos el comando sudo ufw disable**

1. Configuramos las políticas en el firewall, por defecto, UFW tiene reglas para negar todas las conexiones entrantes y solo permite las conexiones salientes al servidor, por lo que nadie podría acceder al servidor y los servicios o aplicaciones en ejecución, estas reglas podemos conseguirlas dentro de la ruta.
2. Para editar las reglas usamos los comandos **sudo ufw default deny incoming** y **sudo ufw default allow outgoing.**
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image81.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image81.png)
    
> 👉 Cuando instalamos un paquete a través de nuestro gestor APT, se incluye un perfil de aplicación en el directorio /etc/ufw/applications.d el cual define el servicio y mantiene la configuración de UFW activa.
    
3. Para enumerar todos los perfiles de aplicaciones usamos el comando **sudo ufw app list** 
Si queremos obtener más información sobre un perfil en específico y las reglas definidas para este, usamos el comando **sudo ufw app info “Aplicación”.**
4. El siguiente paso habilitar los servicios o puertos que queramos permitir en el firewall.
- Si queremos permitir servicios como SSH para conectarnos de forma remota usamos el comando **sudo ufw allow ssh**, en el caso que queramos usar un puerto SSH personalizado, usamos el comando **sudo ufw allow puerto** y si deseamos bloquear una conexión ssh usamos el comando **`sudo ufw deny ssh/tcp`.**
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image82.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image82.png)
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image83.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image83.png)
    
- Si queremos permitir el acceso de aplicaciones que unsam un rango de puertos, usamos el comando **`sudo ufw allow puertoInicial:puertoFinal.`**
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image84.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image84.png)
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image85.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image85.png)
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image86.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image86.png)
    
1. También tenemos la opción de permitir acceso de una sola dirección IP de sistema, para ello ejecutamos el comando **sudo ufw allow from direccionIP,** también podemos especificar que queremos recibir el tráfico de un puerto en especifico **sudo ufw allow direccionIP to any port “numeroPuerto”**
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image87.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image87.png)
    
- Si queremos eliminar las reglas del firewall lo primero que tenemos que hacer es enumerar las reglas con el comando **sudo ufw status numbered** y luego eliminamos la regla usando el comando sudo ufw delete numeroRegla, otra forma sería con el comando **sudo ufw delete reglaUFW.**
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image88.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image88.png)
    

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image89.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image89.png)

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image90.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image90.png)

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image91.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image91.png)

## **Gestión de usuarios y autenticación segura**

Hemos hablado previamente de la gestión y autenticación segura de usuarios en Linux, estas prácticas garantizan la seguridad y protección de los sistemas, evitando accesos no autorizados y protegiendo la información confidencial.

En Linux, cada usuario tiene una cuenta única que le permite acceder al sistema y realizar tareas específicas. La gestión de usuarios implica la creación, modificación y eliminación de estas cuentas de usuario.

Para crear un nuevo usuario en Linux, puedes utilizar el comando `useradd` seguido del nombre de usuario deseado. Por ejemplo, `sudo useradd nombre_usuario` creará una nueva cuenta de usuario en el sistema. Luego, puedes establecer una contraseña para el usuario utilizando el comando `passwd nombre_usuario`. Es importante utilizar contraseñas seguras que combinen letras mayúsculas y minúsculas, números y caracteres especiales.

Además de crear usuarios, también es importante asignarles los permisos adecuados. En Linux, los permisos se gestionan a través del sistema de archivos y los grupos de usuarios. Puedes utilizar comandos como "`chown`" y "`chmod`" para cambiar la propiedad y los permisos de los archivos y directorios.

La autenticación segura es otro aspecto crucial en la gestión de usuarios en servidores Linux. El uso de contraseñas seguras es solo el primer paso. También se recomienda utilizar autenticación de dos factores (2FA) para agregar una capa adicional de seguridad. Esto implica el uso de un segundo método de autenticación, como un código generado por una aplicación en el teléfono móvil, junto con la contraseña tradicional.

Además, es importante asegurarse de que los servicios de autenticación, como SSH (Secure Shell), estén configurados correctamente. Puedes modificar la configuración de SSH en el archivo "/etc/ssh/sshd_config" para permitir sólo conexiones seguras y deshabilitar el acceso de root remoto.

> 👉 Otra práctica recomendada es utilizar claves de autenticación en lugar de contraseñas para acceder a los servidores. Esto implica generar un par de claves pública y privada, donde la clave privada se almacena en el cliente y la clave pública se agrega al archivo "~/.ssh/authorized_keys" en el servidor. Esto permite una autenticación sin contraseña y es más seguro que el uso de contraseñas.

Para configurar nuestra clave pública y privada para autenticarnos dentro del servidor seguimos los siguientes pasos:

1. Creamos nuestras claves pública y privada con el comando ssh-keygen, despues nos pedira la ruta donde almacenar nuestra clave SSH, podemos aceptar la ruta que nos da por defecto, despues pedira una frase de contraseña la cual agrega una capa de seguridad adicional para evitar el inicio de sesión de usuarios no autorizados.
2. El próximo paso será copiar la clave pública al nuestro servidor, para ello usaremos la herramienta ssh-copy-id con el siguiente comando **`ssh-copy-id username@remote_host`.**
3. Procedemos a conectarnos a nuestro usuario ssh con el comando **ssh usuario@hostname** una vez introducido el comando, pedirán la frase de autenticación, la autenticación basada en claves se realizó con éxito, podemos proteger más a nuestro sistema inhabilitando la autenticación con contraseña.
4. Aunque tengamos la cuenta SSH configurada, el mecanismo de autenticación basado en contraseña sigue activo, por lo que vamos a hacer un cambio en el archivo ubicado en la ruta /etc/ssh/sshd_config con nuestro editor de código.
5. Ubicamos la directiva PasswordAuthentication y la activamos quitándole el #, nos aseguramos que el valor de la directiva sea no.
6. Reiniciamos el servicio ssh con el comando systemctl restart ssh

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image92.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image92.png)

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image93.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image93.png)

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image94.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image94.png)

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image95.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image95.png)

## **Configuración de registros de auditoría (logs) del sistema.**

La configuración de registros de auditoría, también conocidos como logs, es una práctica esencial en la administración de sistemas para monitorear y registrar eventos importantes del sistema operativo y las aplicaciones. Estos registros proporcionan información valiosa para el análisis de problemas, la detección de intrusiones y el seguimiento de actividades en el sistema.

En Linux, los registros de auditoría se encuentran en el directorio "/var/log" y contienen información detallada sobre diversos aspectos del sistema, como el inicio y apagado del sistema, errores del kernel, actividades de red, registros de aplicaciones y mucho más.

La configuración de los registros de auditoría se realiza a través del archivo de configuración del demonio de registro, que puede variar según la distribución de Linux utilizada. En distribuciones como Ubuntu y Debian, el archivo de configuración principal es "/etc/rsyslog.conf", mientras que en distribuciones como Red Hat y CentOS, se utiliza "/etc/rsyslog.d/*.conf" para configurar los registros.

En estos archivos de configuración, puedes especificar qué eventos deseas registrar y dónde deseas almacenar los registros. Puedes definir reglas para filtrar eventos específicos, establecer niveles de registro (como información, advertencia o error) y redirigir los registros a archivos específicos o enviarlos a un servidor de registro centralizado.

> ⚠️ Es importante tener en cuenta que la configuración de los registros de auditoría debe equilibrar la cantidad de información registrada con la capacidad de almacenamiento disponible. Registrar demasiados eventos puede llenar rápidamente el espacio en disco y dificultar el análisis de los registros. Por otro lado, registrar muy pocos eventos puede dejar pasar información importante para la detección de problemas o actividades sospechosas.

Además de la configuración de los registros de auditoría, es importante monitorear y analizar regularmente los registros para identificar posibles problemas o actividades maliciosas. Puedes utilizar herramientas como "grep" o "awk" para buscar eventos específicos en los registros, o utilizar herramientas de monitoreo y análisis de registros más avanzadas, como "Logstash" o "Splunk".