---
title: "Intrusion detection systems (IDS)"
subtitle: "Guía completa de Intrusion Detection Systems (IDS): Tipos, Funcionamiento y Mejores Prácticas para Seguridad en Redes"
tags: ["networks", "ciberseguridad", "redes"]
authors: ["blindma1den", "lorenagubaira", "alesanchezr"]

---

**IDS** (*Intrusion Detection System*) el sistema de detección de intrusiones consiste en un conjunto de métodos y técnicas para revelar actividad sospechosa sobre un recurso o recursos informáticos. Es decir, eventos que sugieran un comportamiento anómalo, incorrecto o inapropiado sobre un sistema.

Un sistema de detección de intrusiones puede ser descrito como un proceso de detección y monitorización de eventos que suceden en una red. Este sistema escucha y analiza toda la información que circula por una red, permite ayudar a entender los ataques, estimar los daños causados y tratar de prevenir otros ataques. Para detectar intrusiones en un sistema, los IDS utilizan tres tipos de información: un histórico de eventos, la configuración actual del sistema y, finalmente, procesos activos del sistema o reglas.

![intrusion detection system](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/1intrusion-detection-systen.png?raw=true)

## ¿En qué consiste un IDS y cómo funciona?

Hemos de partir de la base que aunque tengamos el cortafuegos habilitado, por norma general, tendremos muchos puertos abiertos, como por ejemplo el 80 y el 443 para las aplicaciones web. Por lo que debemos tener un sistema adicional que nos ayude a controlar estas puertas abiertas. Para llevar un mayor control debemos utilizar un sistema IDS, esto es, un sistema de detección de intrusos y también de vulnerabilidades. Existen los IDS pasivos y los activos. Con los **pasivos** se generan entradas en el registro y alertas. Con los **activos**, además de realizar esas funciones, también se ejecutan acciones de respuesta, como bloquear direcciones IP o cerrar el acceso a puertos restringidos (a este tipo de IDS activo se le denomina habitualmente IPS).

Además, desde el punto de vista del software, existen diferentes tipos de herramienta: sistemas de detección de intrusos basados en host (**HIDS**, *Host-based IDS*), basados en red (**NIDS**, *Network-based IDS*), basados en firmas (*signature-based IDS*) y basados en anomalías (*anomaly-based IDS*).

![network intrusion detection](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/2network-intrusion-detection.png?raw=true)

Los sistemas IDS utilizan tres métodos para detectar el tráfico. Estos son la detección de anomalías, el análisis de protocolos y el análisis de firmas.

- Con la detección de anomalías tenemos como objetivo detectar un comportamiento anormal. Ejemplo de ello sería un volumen de tráfico ICMP (el que usa ping) inusual y muy elevado, que nos indicaría que somos el blanco o el emisor de un ataque de DDoS (Denegación de servicio)
- Respecto al análisis de protocolos se busca un tráfico de aplicación que no cumple el estándar del protocolo habitual.
- Por último, el análisis de firmas permite identificar ataques o comportamientos perjudiciales ya publicados. Suele ser la técnica más eficaz y la que no está sujeta a errores, ya que sólo se generan ataques o intrusiones que ya han tenido éxito en otro lugar, por lo que, pueden ser fácilmente identificados.

Es importante que nuestro IDS actualice la información de forma habitual, para así tener actualizadas siempre sus técnicas de análisis así como de las bases de datos de firmas.

Existen una serie de organizaciones, asociaciones y empresas que nos permiten estar al corriente de las evoluciones en materia de técnicas de intrusión y ataques. Las principales son:

- **NVD (NIST National Vulnerability Database)**: base de datos pública de vulnerabilidades con identificadores CVE y métricas CVSS ([https://nvd.nist.gov/](https://nvd.nist.gov/)).
- **MITRE CVE**: catálogo oficial de identificadores CVE ([https://cve.mitre.org/](https://cve.mitre.org/)).
- **CERT/CC** (*CERT Coordination Center*) en la Carnegie Mellon University: estudia vulnerabilidades, coordina la divulgación responsable y publica avisos de seguridad ([https://www.kb.cert.org/](https://www.kb.cert.org/)).
- **oss-security** (mailing list de openwall.com): discusión pública sobre vulnerabilidades en software de código abierto.
- **Bugtraq** fue históricamente una de las listas de referencia, pero quedó descontinuada en 2021 tras el cierre de SecurityFocus; ya no se mantiene.

### Tareas de un IDS

Un IDS realiza dos tareas fundamentales:

- Prevención: se realiza por medio de herramientas que escuchan el tráfico en la red o en un ordenador, denominados sensores, e identifican los ataques aplicando reglas, reconocimiento de patrones o técnicas inteligentes.
- Reacción: trata de detectar patrones de intrusión en las trazas de los servicios de red o en el comportamiento del sistema.

Existen indicadores estadísticos de sensibilidad, especificidad y precisión que permiten comprobar la efectividad del IDS, se basan en los siguientes conceptos:

- Verdaderos positivos (TP): existe una intrusión y el IDS la detecta correctamente.
- Falsos positivos (FP): el IDS genera una alerta sin que exista una intrusión real (falsa alarma).
- Falsos negativos (FN): existe una intrusión real pero el IDS no la detecta (alarma omitida).
- Verdaderos negativos (TN): no existe intrusión y el IDS no genera alerta (comportamiento normal correctamente clasificado).

## Tipos de IDS

Existen distintas clasificaciones de los IDS, según sea su enfoque, origen de datos, estructura y comportamiento.

![intrusion detection system clasification](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/3intrusion-detection-system-clasification.png?raw=true)

### En función del enfoque

Se presentan dos grupos: Los sistemas de detección de usos indebidos, que comparan las firmas con la información recogida; y los de detección de anomalías, que usan técnicas estadísticas para distinguir el comportamiento usual del anormal.

#### Detección de anomalías

Es necesario definir cuál es el comportamiento normal de un sistema mediante un proceso de aprendizaje de actividades, para clasificar como sospechosos los comportamientos que se desvíen de lo normal. Estos sistemas son propensos a dar falsos positivos cuando se dispara una alerta con actividad legítima, y su eficacia depende de la calidad del proceso de aprendizaje. Existen varias técnicas para realizar la detección de anomalías:

- **Sistemas basados en métodos estadísticos**: utilizan perfiles de actividad definidos por el comportamiento del usuario respecto a ficheros, programas, registros, etc., mediante métricas y modelos estadísticos.
- **Sistemas basados en aprendizaje automático**: son los más avanzados para el modelado de comportamientos normales y buscan mejorar la detección, reducir los falsos positivos y disminuir el tiempo de computación. Permiten extraer las características de un ataque y añadirlo a la base de datos como firma nueva, actualizando la base en poco tiempo.

#### Detección por uso indebido (basada en firmas/reglas)

Los sistemas basados en uso indebido monitorizan las actividades del sistema y las comparan con una base de datos de firmas de ataques. Cuando se encuentra una coincidencia, se genera una alarma. Resultan más fiables frente a ataques conocidos y son fáciles de adaptar: basta con actualizar la base de datos (escribiendo la nueva regla u obteniéndola de un tercero). Su principal limitación es la baja capacidad para detectar ataques desconocidos. Técnicas habituales:

- **Sistemas basados en conocimiento (reglas)**: violaciones de seguridad detectadas mediante el uso de reglas predefinidas.
- **Sistemas expertos**: conocimiento codificado mediante reglas de implicación (condición-acción); si se cumplen todas las condiciones, se aplica la acción. Su desventaja es que las reglas no son secuenciales, lo que dificulta aislar pasos de intrusión en el tiempo.
- **Detección de firmas**: comparación directa entre los eventos del sistema y las firmas almacenadas en la base de datos en busca de similitudes.
- **Análisis de transición de estados**: los ataques se representan como una secuencia de transiciones (máquina de estados finitos). Cuando se alcanza un estado considerado intrusión, se lanza una alarma.

#### Sistemas híbridos

Los IDS basados en firmas resultan más fiables frente a ataques conocidos, pero presentan deficiencias ante nuevos ataques. Los IDS basados en anomalías detectan ataques desconocidos, pero su rendimiento es inferior. Los sistemas híbridos combinan ambos enfoques y pueden ajustarse para operar como ambos tipos de detector, mejorando la cobertura y el rendimiento.

### En función del origen de los datos

Se encuentran tres tipos de IDS atendiendo a las fuentes de información que se utilicen:

**HIDS (*Host-based Intrusion Detection Systems*):** Los IDS basados en el host solo procesan información de las actividades de los usuarios y servicios en una máquina determinada. Permite monitorizar los datos generados por un usuario, mediante el uso de *syslog1*, e identificar amenazas e intrusiones a nivel de host. Una desventaja proviene del requerimiento de confianza en el sistema, que puede estar infectado anteriormente a la instalación, y lo hace vulnerable ante ataques directos.

**NIDS (*Network Intrusion Detection Systems*):** Los NIDS son instalados en un dispositivo en modo promiscuo, realizan una escucha pasiva sobre la red de forma que no interfieren en su uso, analizando el tráfico en tiempo real, pero por contra, resultan inútiles ante ataques locales. Los nuevos sistemas, basados en agentes inteligentes, permiten una detección de nuevos ataques usando el concepto de centinelas, que supervisan el sistema para recoger toda la información necesaria para la detección.

![network intrusion detection systems](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/4network-intrusion-detection-systems.png?raw=true)

**IDS Híbridos:** Los sistemas híbridos recogen lo mejor de ambos tipos HIDS y NIDS. Permiten una detección local de los sistemas y un sensor en cada segmento de red se encarga de la vigilancia. De esta forma se cubren las necesidades HIDS con las del NIDS, permitiendo el aprovechamiento de las ventajas de ambas arquitecturas.

### En función de su estructura

Clasificación basada en las estrategias de control:

**Sistema de Detección de Intrusión Distribuido (DIDS):** Se basa en la instalación en un sistema distribuido, ubicando sensores repartidos por varios equipos de la red. Estos sensores se comunican con un nodo central donde se recibirá toda la información y donde se cruzan los datos, lo que nos permitirá detectar los ataques con fiabilidad y obtener una visión global mejorando la detección de incidentes.

![distributed intrusion detection systems](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/5distributed-intrusion-detection-systems.png?raw=true)

**Sistema de Detección de Intrusión Centralizado:** Emplea sensores que transmiten información a un sistema central que realiza el control, permitiendo ahorrar en equipamientos.

![centralized instrusion detection system](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/6centralized-instrusion-detection-system.es.png?raw=true)

### En función de su comportamiento

Encontramos dos tipos de IDS según si realizan la prevención escuchando el tráfico o si se elabora una respuesta defensiva cuando se detecta un ataque.

**IDS Pasivo:** Sólo notifican al administrador de la red pero no actúan sobre el ataque. Únicamente procesan la información en busca de intrusiones, y una vez detectada se genera una alerta.

**IDS Activos:** Es un tipo de IDS denominado Sistema de Prevención de Intrusión (IPS). A diferencia de los IDS, esta tecnología no se limita a escuchar el tráfico de la red y a mandar alertas, sino que permite establecer reglas, como se lo hace en los cortafuegos, para detener las intrusiones.
