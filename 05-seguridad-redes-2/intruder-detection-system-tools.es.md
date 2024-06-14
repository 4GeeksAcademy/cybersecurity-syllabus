---
title: "Herramientas IDS/IPS"
subtitle: "Explorando Herramientas IDS/IPS: Quickdraw, Bro y OSSEC - Protección Avanzada para Redes y Sistemas de Control"
tags: ["networks"]
authors: ["blindma1den", "lorenagubaira", "alesanchezr"]

---

Ya hablamos ampliamente de Snort y Suricata veamos algunas otras opciones.

- **Quickdraw**

Quickdraw es un conjunto de reglas para Snort realizado por la empresa Digital Bond, y sirve para aprovechar los IDS existentes mediante el desarrollo de firmas para el control del tráfico de determinados protocolos utilizados en los sistemas de control. Además, también incluye reglas para detectar dispositivos y vulnerabilidades.

Las firmas Quickdraw (reglas en el argot de Snort), identifican solicitudes no autorizadas, solicitudes y respuestas erróneas del protocolo, comandos peligrosos, y otras situaciones que son probables o posibles ataques. En este momento tienen firmas disponibles para cuatro protocolos de sistemas de control, un conjunto de firmas para identificar los ataques a las vulnerabilidades del sistema de control, y un grupo de firmas que identifican eventos de seguridad.

- **Bro**

Bro es otra herramienta que sirve de IDS/IPS, debido a sus características de análisis de red, al igual que Snort y Suricata. Se basa en un potente motor de análisis que permite un alto rendimiento en la monitorización de la red, analiza protocolos, y la información de la capa de aplicación en tiempo real

![intruder prevention system bro](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/ips1-bro.png?raw=true)

***Arquitectura de Bro***

Al igual que otras herramientas, Bro también hace uso de la librería libpcap para su funcionamiento, además es capaz de funcionar en varias redes. Además de la portabilidad adquirida mediante el uso de libpcap, Bro también puede ser una herramienta de red pasiva, lo que significa que puede actuar supervisando una red sin que sea un nodo con una dirección IP asignada. Bro está conceptualizado en dos capas:

> n Motor de eventos: Analiza y guarda el tráfico de la red para generar eventos neutros, que se basan en inicios o paradas de transmisiones, detección de puertos y protocolos.
> 
> 
> n **Política de programa**: Analiza los acontecimientos para crear políticas de acción.
> 

Bro registra los eventos, pero también puede ser configurado para tomar acciones como el envío de alertas, ejecuciones de comandos, actualizaciones y llamadas a otros programas.

- **OSSEC**

OSSEC es un IDS basado en Hosts (HIDS). Realiza análisis de logs, comprobación de la integridad, la supervisión del registro de eventos de Windows, detección de rootkits, alerta basada en tiempo y respuesta activa. Proporciona detección de intrusiones para la mayoría de sistemas operativos, incluyendo Linux, OpenBSD, FreeBSD, OS X, Solaris y Windows. OSSEC tiene una arquitectura centralizada, multiplataforma que permite a varios sistemas ser controlados y manejados fácilmente.

OSSEC se basa en nombrar a cada hosts como server o sensor, según sean sus características. Será necesario un sensor en cada zona que se quiera inspeccionar la red en busca de amenazas, y un servidor al menos para poder leer los datos que llegan de los sensores.

- **Arquitectura OSSEC**

OSSEC se compone de múltiples piezas:

n Servidor: El servidor es la pieza central del despliegue OSSEC. Almacena la integridad de los archivos de bases de datos, comprobación de los registros, eventos y entradas de auditoría del sistema. Todas las reglas, decodificadores, y las principales opciones de configuración se almacenan de forma centralizada en el administrador; por lo que es fácil de administrar incluso con un gran número de agentes.

n **Agentes/sensores:** El agente es un pequeño programa o conjunto de programas, instalado en el sistema que va a ser monitorizado. El agente recopilará información y la transmitirá al gestor para su análisis y para llevar a cabo una correlación de información. Parte de la información se recoge en tiempo real, otra será recogida periódicamente. Tiene un pequeño uso de memoria y CPU por defecto, que no afecta el uso del sistema.

![intruder prevention system ossec](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/ips2-ossec.png?raw=true)

- **OSSEC en redes industriales**

A modo de resumen, e implementando este sistema en una red industrial, se puede incluir una lista blanca con la IP de cada equipo industrial, routers y switches que puedan estar conectados a la red, denegando la inyección de tráfico a cualquier otro equipo que no esté registrado en esta lista.

De esta forma, se consigue una seguridad efectiva, de forma gratuita y sencilla. Igualmente se puede crear en otros sistemas operativos, en un Linux como se ha visto, o en Windows, que se presenta a continuación. Al funcionar adecuadamente con equipos con bajo rendimiento, nos permite realizar la instalación en redes industriales donde se suelen encontrar equipos más antiguos.

La inclusión de integridad del servidor, detección de rootkits y detección activa, es un añadido a la seguridad de una red industrial, siendo un requisito indispensable para aumentar la defensa de una empresa.

## **Comparación entre varios IDS/IPS**

La Tabla 1 refleja una comparación de las características de algunos de los sistemas IDS/IPS que se han tratado en este estudio.

| Características                | Bro  | Snort | Suricata |
|--------------------------------|------|-------|----------|
| Multi Hilo                     | No   | v3.0  | Sí       |
| Soporte para IPv6              | Sí   | Sí    | Sí       |
| Reputación IP                  | Parte| No    | Sí       |
| Detección Automática de Protocolos | Sí   | v3.0  | Sí       |
| Aceleración con GPU            | No   | No    | Sí       |
| Variables globales/Flowbits    | Sí   | No    | Sí       |
| GeoIP                          | Sí   | No    | Sí       |
| Análisis Avanzado de HTTP      | Sí   | No    | Sí       |
| HTTP Access Logging            | Sí   | No    | Sí       |
| SMB Access Logging             | Sí   | No    | Sí       |
| Gratis                         | Sí   | Sí    | Sí       |


Módulo 3: Seguridad en redes inalámbricas

## **Protección de las redes inalámbricas**

Las redes inalámbricas domésticas te permiten utilizar el ordenador virtualmente desde cualquier lugar de la casa, además de conectarte con otros ordenadores de la red o acceder a Internet. No obstante, si la red inalámbrica no es segura, existen riesgos muy importantes. Por ejemplo, un hacker podría:

- Interceptar los datos que envíes o recibas
- Acceder a tus archivos compartidos

Secuestrar tu conexión a Internet y utilizar todo el ancho de banda o límite de descargas

### **Consejos de seguridad en Internet para proteger la red inalámbrica**

A continuación se incluyen varios pasos sencillos que puedes seguir para proteger tu red y routers inalámbricos:

- **Evita la utilización de la contraseña predeterminada:** Es muy fácil para un hacker descubrir cuál es la contraseña predeterminada del fabricante de tu router inalámbrico y utilizarla para acceder a la red inalámbrica. Por lo tanto, es conveniente que cambies la contraseña de administrador de tu router inalámbrico. A la hora de establecer la contraseña nueva, trata de elegir una serie compleja de números y letras, e intenta evitar la utilización de una contraseña que pueda adivinarse fácilmente.

<aside>
⚠️ **No permitas que el dispositivo inalámbrico indique su presencia - d**esactiva la difusión del identificador de red SSID (Service Set Identifier) para evitar que el dispositivo inalámbrico anuncie su presencia al mundo que te rodea.

</aside>

- **Cambia el nombre SSID del dispositivo:** Al igual que antes, es muy fácil para un hacker descubrir cuál es el nombre SSID predeterminado del fabricante del dispositivo y utilizarlo para localizar la red inalámbrica. Cambia el nombre SSID predeterminado del dispositivo e intenta evitar la utilización de un nombre que pueda adivinarse fácilmente.
- **Cifra los datos:** En la configuración de la conexión, asegúrate de que activas el cifrado. Si el dispositivo es compatible con el cifrado WPA, utilízalo; en caso contrario, utiliza el cifrado WEP.
- **Protección contra los ataques de malware e Internet:** Asegúrate de que instalas un programa antimalware eficaz en todos los ordenadores y demás dispositivos. Con el fin de mantener actualizada la protección antimalware, selecciona la opción de actualización automática en el producto.
