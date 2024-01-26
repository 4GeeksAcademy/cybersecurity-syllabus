### **bWAPP**

Este completo tutorial te enseñará a realizar pentesting y comprobar las principales vulnerabilidades Web a través de la herramienta bWAPP. Creado por Malik Messelem , **[bWAPP](http://www.itsecgames.com/)** (abreviatura en ingles de "aplicación web con fallos") es posiblemente, dentro de los Hacker Simulator, una de las aplicaciones gratuitas y de código abierto más conocida, esta creada de forma deliberada con vulnerabilidades. Es de los mejores, si no el mejor, con fallos deliberados para practicar y mejorar nuestras habilidades de hacking ético. Ya sea para un entusiasta de la ciberseguridad, un apasionado, un estudiante, un desarrollador o un profesional que sencillamente busca divertirse, este entorno, nos va a ayudar a efectuar y mejorar nuestras habilidades de hacking ético y pruebas de penetración en un entorno excelente. Lo que hace que bWAPP sea único, es que **ofrece más de cien vulnerabilidades** y fallos de aplicaciones web derivados del ya conocidísimos [Proyecto Top diez de OWASP](https://owasp.org/www-project-top-ten/).

![bwapp](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/bwapp.png?raw=true)

Algunas de las vulnerabilidades son:

- Cross-site scripting (XSS), rastreo entre sitios (XST) y falsificación de peticiones entre sitios (CSRF).
- Ataques de Man in the Midle.
- Falsificación de petición del lado del servidor (SSRF).
- Ataques DoS.
- Inyecciones de SQL, HTML, iFrame, SSI, OS Command, PHP, XML, XPath, LDAP, Host Header y SMTP y mucho más…

bWAPP está construido en PHP y emplea una base de datos MySQL. Se puede alojar tanto en el sistema operativo Windows como en Linux: en Windows, puede alojarse en el servidor xampp y wamp, en Linux, Apache, e igualmente es genial para utilizar en **Kali Linux**.

- Puedes [descargarte bWAPP](http://www.itsecgames.com/download.htm) desde su web .
- Web del proyecto: [http://sourceforge.net/projects/bwapp/](http://sourceforge.net/projects/bwapp/)

![Archivos bwapp](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/archivos-bwapp.png?raw=true)

Puede ser alojado en Linux o Windows sobre Apache o IIS y MySQL. Se admite en WAMP o XAMPP. Otra posibilidad es la utilizar una máquina virtual que sirve para VMware o para VirtualBox. bWAPP es libre y abierto, se puede descargar en dos versiones una para utilizar en forma local y otra para instalar en una máquina virtual. El sitio web está desarrollado en PHP y MySQL por lo que es multiplataforma. Descargamos instalar [bWAPP](https://sourceforge.net/projects/bwapp/files/latest/download?source=files) en local,en este caso lo haremos en kali linux.

Luego ir a la ubicación que hemos descargado BWAPP, abrimos el explorador como administrador y copiamos el archivo a /var/www/html y descomprimimos o por línea de comandos:

> unzip bWAPPv2.2.zip -d /var/www/html

Después de haber descomprimido vamos a darle permisos.

> chmod -R 777 /var/www/html/bWAPPv2.2

Ejecutamos apache y msql

> service apache2 start

> service mysql start

![Apache y msql](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/apache-y-msql.png?raw=true)
Listo ahora pueden ir a su navegador o colocar la IP de su máquina o sino colocar localhost

[http://127.0.0.1/bWAPPv2.2/bWAPP/install.php](http://127.0.0.1/bWAPPv2.2/bWAPP/install.php)

Le damos here!

![aqui](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/aqui.png?raw=true)

En Windows deben instalar wampServer [Download wampserver3.3.0_x64.exe (WampServer) (sourceforge.net)](https://sourceforge.net/projects/wampserver/files/WampServer%203/WampServer%203.0.0/wampserver3.3.0_x64.exe/download)

![wampServer](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/wampserver.png?raw=true)

Instalamos e iniciamos, si todo va bien vamos a ver un icono nuevo en la barra

![Icono Nuevo](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/icono-nuevo.png?raw=true)

![Archivo bwapp](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/archivo-bwapp.png?raw=true)

![Instalación bwapp](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/instalacion-bwapp.png?raw=true)

[http://127.0.0.1/bWAPP/login.php](http://127.0.0.1/bWAPP/login.php)

![Login bwapp](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/login-bwapp.png?raw=true)

Ahora si… happy hacking

## **Bee-Box**

si deseamos instalar en una máquina virtual el proyecto es [Bee-Box](https://sourceforge.net/projects/bwapp/files/bee-box/bee-box_v1.6.7z/download). **Bee-box es una máquina virtual Linux con todo preinstalado**. Así solo deberemos explorar todas las vulnerabilidades bWAPP sin correr el riesgo de desfigurar el sitio web bWAPP. Además con la máquina virtual podremos intentar conseguir acceso root. I**nstalaremos la versión Bee-Box de bWAPP**, para ello descomprimimos el archivo que descargamos y los creara una carpeta con muchos archivos vmdk a nuestro servidor local. A continuación crearemos la máquina virtual asignando una versión Linux Ubuntu de 32 bit.

![Bee-box1](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/bee-box1.png?raw=true)

![Bee-box2](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/bee-box2.png?raw=true)

A continuación deberemos seleccionar el archivo descargado denominado **bee-box.vdmk**

![Archivo Bee-box](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/archivo-bee-box.png?raw=true)

![Resumen](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/resumen.png?raw=true)

Antes de iniciar la máquina virtual, recordemos que deberemos configurar la red esto la hacemos desde **Configuración** para poder tener una dirección IP y poder acceder a la máquina virtual desde otro ordenador.

![IP](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/ip.png?raw=true)

Hacemos clic en crear y luego en Iniciar, para que la máquina virtual comience a funcionar, una vez cargada veremos el escritorio.

![Desktop](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/desktop.png?raw=true)