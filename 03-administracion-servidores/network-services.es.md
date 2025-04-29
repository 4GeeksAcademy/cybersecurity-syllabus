---
title: "Servicios de red"
subtitle: "Aprende a configurar servicios de red esenciales para la seguridad de su servidor. Domina la configuración de IP, DNS, HTTP y FTP con nuestra guía paso a paso."
tags: ["linux", "networking", "ciberseguridad"]
authors: ["blindma1den", "lorenagubaira"]

---

## **Configuración de la interfaz de red**

La interfaz de red y su configuración es una de las partes más importantes de un servidor y las labores de un administrador de sistemas, ya que con la interfaz de red podemos establecer la conectividad y permitir que el servidor se comunique con otros dispositivos en la red.

Para poder entablar una conexión con otros dispositivos lo primero que tenemos que hacer es asignarle una IP a nuestro servidor bien sea de una forma estática en la cual nosotros le asignamos la IP y la agregamos manualmente, ò dinámica donde dejamos que un servidor DHCP sea que asigne una dirección IP temporal.

La elección entre una dirección IP dinámica o estática para un servidor depende de varios factores y requisitos específicos. Aquí hay algunas consideraciones que pueden ayudarte a tomar una decisión informada:

- **Estabilidad y disponibilidad**: Si necesitas que tu servidor esté siempre disponible y accesible, una dirección IP estática puede ser más adecuada. Con una dirección IP estática, la dirección del servidor no cambiará, lo que facilita la conexión y el acceso constante.
- **Servicios y aplicaciones**: Si tu servidor aloja servicios o aplicaciones que requieren una dirección IP constante, como servidores web, bases de datos o servidores de correo electrónico, una dirección IP estática es recomendable. Esto garantiza que los clientes y usuarios siempre puedan acceder a tus servicios utilizando la misma dirección IP.
- **Seguridad:** Una dirección IP estática puede facilitar la implementación de medidas de seguridad, como el filtrado de direcciones IP o la configuración de reglas de firewall específicas. Esto puede ayudar a proteger tu servidor y los servicios que ofrece
- **Flexibilidad y movilidad:** Si necesitas flexibilidad para cambiar la ubicación física de tu servidor o si tu proveedor de servicios de Internet (ISP) requiere el uso de direcciones IP dinámicas, una dirección IP dinámica puede ser más conveniente. Las direcciones IP dinámicas se asignan automáticamente y pueden cambiar con el tiempo.

Después de estas consideraciones podemos indicar que la mejor configuración de IP es estática para nuestro servidor, para lograr esta configuración hacemos los siguientes pasos.

Usamos el comando `ifconfig` para conocer cuál es nuestra interfaz de red.

![Configuración de la interfaz de red - comando ifconfig para conocer cuál es nuestra interfaz](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/network-services/network-services-image-1.jpg)

lo podemos identificar como la primera interfaz que tenemos del resultado “enp0s3”

Generalmente en las distribuciones debian, las interfaces de red se configuraban a través del archivo **/etc/network/interfaces**, en el caso de ubuntu, desde la version 17.10, se cambio las configuraciones de la interfaz de red a la utilidad netplan, el cual genera un archivo YAML para facilitar la configuraciones de red. Accederemos a este archivo con un editor de código a la ruta `/etc/netplan/00-installer-config-yaml`

![Configuración de la interfaz de red - Accederemos a este archivo con un editor de código a la ruta /etc/netplan/00-installer-config-yaml](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/network-services/network-services-image-2.jpg "Accederemos a este archivo con un editor de código a la ruta /etc/netplan/00-installer-config-yaml")

![Configuración de la interfaz de red - Accederemos a este archivo con un editor de código a la ruta /etc/netplan/00-installer-config-yaml](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/network-services/network-services-image-3.jpg "Asignamos una IP 192.168.1.10 a nuestro servidor y el resto de las configuraciones")

Asignamos una `IP 192.168.1.10` a nuestro servidor y el resto de las configuraciones.

![Configuración de la interfaz de red - Ya una vez asignado los valores, aplicamos el comando](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/network-services/network-services-image-4.jpg "Ya una vez asignado los valores, aplicamos el comando")

Ya una vez asignado los valores, aplicamos el comando

**`netplan apply`**

![Configuración de la interfaz de red - aplicamos el comando netplan apply](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/network-services/network-services-image-5.jpg "aplicamos el comando netplan apply")

Corroboramos que nuestra IP ya sea la que le asignamos y listo, ya tenemos la interfaz de red de nuestros servidores configurada.

![Configuración de la interfaz de red - Corroborar nuestra IP](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/network-services/network-services-image-6.jpg "Corroborar nuestra IP")

## **Configuración de la resolución de nombres (DNS)**

Otra configuración esencial para la conexión de la red es la configuración de la DNS (Domain Name System), recordemos que este protocolo es el encargado de traducir los nombres de los dominios que utilizamos en nuestro navegador como por ejemplo [www.google.com](http://www.google.com/) en las direcciones IP de los servidores web de que queremos acceder.

Este proceso se da cuando ingresamos una dirección web en nuestro navegador, éste envía una solicitud a un servicio DNS para obtener la dirección IP asociada a ese nombre del dominio, el servidor DNS busca en su base de dato devuelve la dirección IP correspondiente, permitiendo que el navegador establezca una conexión con el servidor web que aloja el sitio.

Además de su función principal de traducción de nombres de dominio, las DNS también desempeñan un papel importante en la seguridad y la optimización de la navegación. Por ejemplo, las DNS pueden implementar medidas de seguridad, como el filtrado de contenido malicioso o la detección de sitios web fraudulentos, ayudando a proteger a los usuarios de posibles amenazas en línea.

Es importante tener configurado la DNS de nuestro servidor ya que es el que nos va a permitir que los usuarios accedan a los servicios y aplicaciones alojados en el servidor mediante los nombres del dominio, aparte también se utiliza para redireccionar el tráfico a diferentes servidores en función de la carga o la disponibilidad. Esto permite distribuir la carga de trabajo entre varios servidores y garantizar un rendimiento óptimo.

La DNS también desempeña un papel importante en la seguridad de un servidor al implementar medidas de seguridad en la configuración de la DNS, como el filtrado de contenido malicioso o la detección de sitios web fraudulentos, se puede proteger al servidor y a los usuarios de posibles amenazas en línea.

Para configurar la DNS de nuestro servidor Ubuntu repetiremos el mismo proceso que hicimos al configurar nuestra IP estática ingresando a la ruta **/etc/netplan/00-installer-config.yaml** desde un editor de código.

De acuerdo a la documentación de netplan la forma de agregar nuestras DNS es a través del valor

**nameservers:**

Ya que estamos trabajando con un servidor, la DNS principal que usaremos sera la misma IP de nuestro servidor, la alternativa sera una DNS publica

![Configuración de la resolución de nombres - DNS](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/network-services/network-services-image-7.jpg)

Les dejamos una lista de DNS públicas que pueden usar para la red

| Nombre DNS | IP principal | IP alternativa |
| --- | --- | --- |
| Cloudflare | 1.1.1.1 | 1.0.0.1 |
| OpenDNS | 208.67.222.222 | 208.67.220.220 |
| Google | 8.8.8.8 | 8.8.4.4 |

Para esta configuración usaremos la DNS google

Una vez editado el archivo YAML aplicamos el comando netplan apply

Si queremos corroborar que tenemos conexion, usamos el comando ping junto a nuestro servidor alternativo

![Configuración de la resolución de nombres - comando ping](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/network-services/network-services-image-8.jpg "comando ping")

## **Configuración de servicios de red**

Cuando hablamos de los servicios de red en los referimos hablamos de las aplicaciones que se ejecutan en un segundo plano, habilitando ciertas capacidades cuando sean necesarias, estas aplicaciones son componentes fundamentales que permiten la comunicación y el intercambio de información en una red.

Uno de los servicios de red más comunes en servidores Linux es el servidor web, que permite alojar y entregar páginas web a través del protocolo HTTP. El servidor web más popular en Linux es Apache, aunque también existen otras opciones como Nginx. Estos servidores web permiten a los usuarios acceder a sitios web y aplicaciones en línea, brindando una experiencia de navegación fluida y segura

Vamos a configurar nuestro servidor HTTP con Apache aplicando los siguientes pasos:

- Instalamos Apache habiendo actualizando los paquetes locales previamente con **sudo apt update.**
    
    ![Configuración de servicios de red](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/network-services/network-services-image-9.jpg)

- Una vez actualizados los paquetes instalamos nuestro servidor apache **sudo apt install apache2.**
    
    ![Configuración de servicios de red - firewall](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/network-services/network-services-image-10.jpg)

- Antes de probar apache, es necesario modificar unos ajustes de firewall para permitir acceso externo a los puertos web predeterminados, durante la instalación, Apache se registra con UFW para proporcionar algunos perfiles de aplicaciones que pueden utilizarse para habilitar o deshabilitar el acceso a Apache a través del firewall.
    
    
- Con el comando sudo ufw app list tendremos una lista de los perfiles de aplicación.
    
    ![Configuración de servicios de red - sudo ufw](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/network-services/network-services-image-11.jpg)
    
    En el resultado tendremos tres perfiles disponibles para Apache.
    
    - **Apache**: este perfil abre solo el puerto 80 (tráfico web normal no cifrado)
    - **Apache Full**: este perfil abre el puerto 80 (tráfico web normal no cifrado) y el puerto 443 (tráfico TLS/SSL cifrado)
    - **Apache Secure**: este perfil abre solo el puerto 443 (tráfico TLS/SSL cifrado)
    - Habilitamos el perfil más restrictivo el cual sería Apache permitiendo el tráfico en el puerto 80 (puerto http)

### sudo ufw allow “Apache”

![sudo ufw allow “Apache”](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/network-services/network-services-image-12.jpg "sudo ufw allow “Apache”")

Podemos corroborar los cambios usando el comando sudo ufw status

![sudo ufw status](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/network-services/network-services-image-13.jpg "sudo ufw status")

En algunos casos podemos tener una respuesta de Status: Inactive, esto ocurre porque el firewall está inactivo, para activarlo usamos el comando sudo ufw enable, y volvemos a chequear el status

![Network Services Configuration](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/network-services/network-services-image-14.jpg)

![Configuración de servicios de red - comando sudo systemctl status apache2](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/network-services/network-services-image-15.jpg)

- Ya una vez habiendo permitido el tráfico al puerto HTTP revisamos el estatus de nuestro servidor con el comando sudo systemctl status apache2

![Configuración de servicios de red - Servidor activo](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/network-services/network-services-image-16.jpg)

Podemos ver que su estado es activo y corriendo.

- Otra forma de comprobar que nuestro servidor está activo es haciendo una solicitud de página, si no estamos seguro de la dirección IP de nuestro servidor, usamos el comando hostname -I y nos devolverá la IP la cual abriremos en un navegador web para comprobar que esté activo.

![Configuración de servicios de red - Host Name -I](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/network-services/network-services-image-17.jpg)

![Configuración de servicios de red - FTP (File Transfer Protocol)](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/network-services/network-services-image-18.jpg)

Otro de los servicios necesarios para nuestro servidor es el FTP (File Transfer Protocol) el cual lo usamos como un medio para enviar recibir archivos a través de una conexion de red usando un marco de referencia de cliente/servidor y seguridad SSL/TLS que permite a los usuarios compartir archivos y recibir desde computadoras remotas a través de una transferencia de datos segura, eficiente y confiable.

FTP funciona de la misma manera que HTTP(HypertText Transfer Protocol) o SMTP(Simple Mail Transfer Protocol). La diferencia es que el FTP se encarga de transportar archivos a través de Internet, mientras que el HTTP y el SMTP se encargan de transferir páginas web y correos electrónicos, respectivamente.

Para instalar este servicio en nuestro servidor podemos seguir los siguientes pasos:

- Antes de instalar nuestro servicio, lo recomendable es actualizar nuestro sistema operativo con sudo apt update y sudo apt upgrade.

![Configuración de servicios de red - actualizar nuestro sistema operativo con sudo apt update y sudo apt upgrade](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/network-services/network-services-image-19.jpg "actualizar nuestro sistema operativo con sudo apt update y sudo apt upgrade")

- Procederemos a instalar vsftpd (Very Secure FTP Daemon por sus siglas en inglés) el cual es un servidor FTP para los sistemas tipo unix incluido Linux, este lo haremos con el comando sudo apt install vsftpd

![Configuración de servicios de red - vsftpd (Very Secure FTP Daemon por sus siglas en inglés)](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/network-services/network-services-image-20.jpg "vsftpd (Very Secure FTP Daemon por sus siglas en inglés)")

- Una vez completada la instalación, tendremos que editar el archivo de configuración, lo recomendable en estos casos es crear una copia de seguridad del archivo original para así comenzar la configuración en blanco si cometemos algún error

![Configuración de servicios de red - crear una copia de seguridad)](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/network-services/network-services-image-21.jpg)

- Ya configurado el tenemos la copia creada comenzamos a permitir el trafico FTP desde el firewall usando los siguientes comandos

`sudo ufw allow 20/tcp`

`sudo ufw allow 21/tcp`

`sudo ufw allow 990/tcp`

`sudo ufw allow 40000:50000/tcp`

![Configuración de servicios de red - permitir el trafico FTP desde el firewall](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/network-services/network-services-image-22.jpg)

Estos comandos abrirán varios puertos

- **OpenSSH** es necesario si todavía quieres acceder a tu servidor a través de SSH. A veces, esta opción está activada por defecto.
- los puertos **20** y **21** para el tráfico FTP.
- los puertos **40000:50000** se reservarán para el rango de puertos pasivos que eventualmente se establecerá en el archivo de configuración.
- el puerto **990** se utilizará cuando se active el TLS.

**Ya una vez agregadas las reglas revisamos el estatus del firewall**

![Configuración de servicios de red - estatus del firewall](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/network-services/network-services-image-23.jpg)

- Abrimos el archivo **/etc/vsftpd.conf** con el editor de codigo de nuestra elección y ya dentro del archivo habilitamos la opcion
- write_enable=yes eliminando el **#,**
    
    ![Configuración de servicios de red - write_enable=yes eliminando el #](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/network-services/network-services-image-24.jpg)
    
- Agregamos unos valores nuevos al final del archivo. En primer lugar, se agregará un user_sub_token en la ruta del directorio local_root. Esto permitirá que la configuración funcione con el usuario actual y con cualquier otro usuario que se agregue posteriormente:
- user_sub_token=$USER
    
    local_root=/home/$USER/ftp
    

![Configuración de servicios de red - limitar puertos](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/network-services/network-services-image-25.jpg)

- Para garantizar que haya una cantidad considerable de conexiones disponibles, limitaremos la cantidad de puertos utilizados en el archivo de configuración:
    - pasv_min_port=40000
    - pasv_max_port=50000
    
- Ya una vez hecho estos cambios cerramos el archivo y agregamos a nuestro usuario en la lista de usuarios del servicio ftp y comprobamos que este agregado adecuadamente

![Configuración de servicios de red - cerrar y agregar usuario](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/network-services/network-services-image-26.jpg)

- Por último reiniciamos el servicio vsftpd

![Configuración de servicios de red - reiniciamos el servicio vsftpd](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/network-services/network-services-image-27.jpg)

> 📖 En este módulo hemos aprendido como configurar dos servicios muy importantes para administrar un servidor como lo son HTTP y FTP, existen muchos otros que puedes investigar y poner en práctica dentro de tu máquina virtual, anímate, la práctica hace al maestro.
