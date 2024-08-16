---
title: "Herramientas para la prevencion o deteccion de intrusos (IDS/IPS)"
subtitle: "Explorando Herramientas IDS/IPS: Snort, Suricata, Quickdraw, Zeek, OSSEC, y Wazuh - Protección Avanzada para Redes y Sistemas de Control"
tags: ["ciberseguridad", "networks"]
authors: ["blindma1den", "lorenagubaira", "alesanchezr"]

---

Los sistemas de detección de intrusos (IDS) y los sistemas de prevención de intrusos (IPS) son herramientas esenciales para proteger redes y sistemas de control contra accesos no autorizados y ataques cibernéticos. En este artículo, exploraremos algunas de las herramientas más destacadas en este ámbito, comenzando por Snort y Suricata.

## Snort

Snort es una de las herramientas IDS/IPS más populares y ampliamente utilizadas. Desarrollada por Sourcefire, ahora parte de Cisco, Snort se utiliza para detectar intrusiones en tiempo real al analizar el tráfico de la red y comparar los paquetes con un conjunto de reglas predefinidas. Sus características incluyen la detección de anomalías, el análisis de protocolos y la capacidad de registrar paquetes sospechosos para su posterior análisis.

Snort es conocido por su flexibilidad y robustez, permitiendo a los administradores de red personalizar y actualizar las reglas para adaptarse a las necesidades específicas de su entorno. Además, la comunidad activa de Snort proporciona una amplia base de datos de reglas y actualizaciones continuas para enfrentar nuevas amenazas.

## Suricata

Suricata es otra potente herramienta IDS/IPS que compite directamente con Snort. Desarrollada por la Open Information Security Foundation (OISF), Suricata ofrece capacidades de detección de intrusos de alto rendimiento gracias a su soporte para el procesamiento de paquetes multihilo, lo que le permite aprovechar las arquitecturas de hardware modernas.

Una de las características más destacadas de Suricata es su capacidad para realizar una inspección profunda de paquetes (DPI) y su integración con flujos de red, lo que proporciona un contexto adicional para la detección de amenazas. Suricata también ofrece una excelente compatibilidad con las reglas de Snort, lo que facilita su implementación en entornos existentes que ya utilizan Snort.

## Otras Opciones de herramientas IDS/IPS

### Quickdraw

Quickdraw es un conjunto de reglas para Snort realizado por la empresa Digital Bond. Sirve para aprovechar los IDS existentes mediante el desarrollo de firmas para el control del tráfico de determinados protocolos utilizados en los sistemas de control. Además, también incluye reglas para detectar dispositivos y vulnerabilidades.

Las firmas Quickdraw (reglas en el argot de Snort) identifican solicitudes no autorizadas, solicitudes y respuestas erróneas del protocolo, comandos peligrosos y otras situaciones que son probables o posibles ataques. En este momento, tienen firmas disponibles para cuatro protocolos de sistemas de control, un conjunto de firmas para identificar los ataques a las vulnerabilidades del sistema de control y un grupo de firmas que identifican eventos de seguridad.

### Zeek (anteriormente Bro)

Zeek es otra herramienta que sirve de IDS/IPS, debido a sus características de análisis de red, al igual que Snort y Suricata. Se basa en un potente motor de análisis que permite un alto rendimiento en la monitorización de la red, analiza protocolos y la información de la capa de aplicación en tiempo real.

![intruder prevention system Bro](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/ips1-bro.png?raw=true)

#### Arquitectura de Zeek

Al igual que otras herramientas, Zeek también hace uso de la librería libpcap para su funcionamiento y es capaz de funcionar en varias redes. Además de la portabilidad adquirida mediante el uso de libpcap, Zeek también puede ser una herramienta de red pasiva, lo que significa que puede actuar supervisando una red sin ser un nodo con una dirección IP asignada. Zeek está conceptualizado en dos capas:

- **Motor de eventos**: Analiza y guarda el tráfico de la red para generar eventos neutros, que se basan en inicios o paradas de transmisiones, detección de puertos y protocolos.
- **Política de programa**: Analiza los acontecimientos para crear políticas de acción.

Zeek registra los eventos, pero también puede ser configurado para tomar acciones como el envío de alertas, ejecuciones de comandos, actualizaciones y llamadas a otros programas.

### OSSEC

OSSEC es un IDS basado en hosts (HIDS). Realiza análisis de logs, comprobación de la integridad, supervisión del registro de eventos de Windows, detección de rootkits, alerta basada en tiempo y respuesta activa. Proporciona detección de intrusiones para la mayoría de sistemas operativos, incluyendo Linux, OpenBSD, FreeBSD, OS X, Solaris y Windows. OSSEC tiene una arquitectura centralizada y multiplataforma que permite a varios sistemas ser controlados y manejados fácilmente.

OSSEC se basa en nombrar a cada host como servidor o sensor, según sus características. Será necesario un sensor en cada zona que se quiera inspeccionar la red en busca de amenazas y al menos un servidor para poder leer los datos que llegan de los sensores.

#### Arquitectura de OSSEC**

OSSEC se compone de múltiples piezas:

- **Servidor**: El servidor es la pieza central del despliegue OSSEC. Almacena la integridad de los archivos de bases de datos, comprobación de los registros, eventos y entradas de auditoría del sistema. Todas las reglas, decodificadores y las principales opciones de configuración se almacenan de forma centralizada en el administrador; por lo que es fácil de administrar incluso con un gran número de agentes.
- **Agentes/sensores**: El agente es un pequeño programa o conjunto de programas instalado en el sistema que va a ser monitorizado. El agente recopilará información y la transmitirá al gestor para su análisis y para llevar a cabo una correlación de información. Parte de la información se recoge en tiempo real, y otra será recogida periódicamente. Tiene un pequeño uso de memoria y CPU por defecto, que no afecta el uso del sistema.

![intruder prevention system ossec](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/cpu.es.png?raw=true)

#### OSSEC en redes industriales

Al implementar OSSEC en una red industrial, se puede incluir una lista blanca con la IP de cada equipo industrial, routers y switches que puedan estar conectados a la red, denegando la inyección de tráfico a cualquier otro equipo que no esté registrado en esta lista.

De esta forma, se consigue una seguridad efectiva, de forma gratuita y sencilla. Igualmente, se puede crear en otros sistemas operativos, en un Linux como se ha visto, o en Windows, que se presenta a continuación. Al funcionar adecuadamente con equipos con bajo rendimiento, nos permite realizar la instalación en redes industriales donde se suelen encontrar equipos más antiguos.

La inclusión de integridad del servidor, detección de rootkits y detección activa es un añadido a la seguridad de una red industrial, siendo un requisito indispensable para aumentar la defensa de una empresa.

### Wazuh

Wazuh es una plataforma de monitoreo de seguridad de código abierto que ha evolucionado a partir de OSSEC. Amplía las capacidades de OSSEC con nuevas características, como la integración con plataformas en la nube, gestión centralizada y un conjunto más amplio de reglas preconfiguradas.

#### Características Clave de Wazuh

- **Integración con el ELK Stack**: Wazuh se integra perfectamente con Elasticsearch, Logstash y Kibana, proporcionando una interfaz gráfica potente para la visualización y análisis de datos de seguridad.
- **Detección de Amenazas en la Nube**: Ofrece reglas y decodificadores específicos para entornos de nube como AWS, Azure y Google Cloud, ayudando a identificar amenazas y configuraciones incorrectas en estos entornos.
- **Gestión Centralizada**: Permite la administración de múltiples agentes y servidores desde una consola centralizada, facilitando la gestión de grandes despliegues.

## Comparación entre varios IDS/IPS

La Tabla 1 refleja una comparación de las características de algunos de los sistemas IDS/IPS que se han tratado en este estudio.

| Características                | Zeek | Snort | Suricata | OSSEC | Wazuh |
|--------------------------------|------|-------|----------|-------|-------|
| Multi Hilo                     | No   | v3.0  | Sí       | No    | No    |
| Soporte para IPv6              | Sí   | Sí    | Sí       | Sí    | Sí    |
| Reputación IP                  | Parcial| No   | Sí       | No    | Sí    |
| Detección Automática de Protocolos | Sí | v3.0  | Sí       | No    | No    |
| Aceleración con GPU            | No   | No    | Sí       | No    | No    |
| Variables globales/Flowbits    | Sí   | No    | Sí       | No    | No    |
| GeoIP                          | Sí   | No    | Sí       | No    | No    |
| Análisis Avanzado de HTTP      | Sí   | No    | Sí       | No    | No    |
| HTTP Access Logging            | Sí   | No    | Sí       | No    | No    |
| SMB Access Logging             | Sí   | No    | Sí       | No    | No    |
| Gratis                         | Sí   | Sí    | Sí       | Sí    | Sí

    |
| Integración con ELK Stack      | No   | No    | Parcial  | No    | Sí    |

---

### Conclusión

La elección de una herramienta IDS/IPS adecuada depende de las necesidades específicas de cada organización. Factores como el rendimiento, la facilidad de integración y las capacidades de análisis deben considerarse al seleccionar la solución adecuada. Las herramientas presentadas en este artículo ofrecen una amplia gama de funcionalidades que pueden adaptarse a diferentes entornos de red y necesidades de seguridad. Mantener actualizadas las reglas y configuraciones, así como integrar estas herramientas con otros sistemas de gestión de seguridad, es crucial para asegurar una protección efectiva contra amenazas cibernéticas.
