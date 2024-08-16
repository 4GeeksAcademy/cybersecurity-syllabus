---
title: "Intrusion detection systems (IDS)"
subtitle: "Guía completa de Intrusion Detection Systems (IDS): Tipos, Funcionamiento y Mejores Prácticas para Seguridad en Redes"
tags: ["networks", "ciberseguridad", "redes"]
authors: ["blindma1den", "lorenagubaira", "alesanchezr"]

---

**IDS** (*Intrusion Detection System*) el sistema de detección de intrusiones consiste en un conjunto de métodos y técnicas para revelar actividad sospechosa sobre un recurso o recursos informáticos. Es decir, eventos que sugieran un comportamiento anómalo, incorrecto o inapropiado sobre un sistema.

Un sistema de detección de intrusiones puede ser descrito como un proceso de detección y monitorización de eventos que suceden en una red. Este sistema escucha y analiza toda la información que circula por una red, permite ayudar a entender los ataques, estimar los daños causados y tratar de prevenir otros ataques. Para detectar intrusiones en un sistema, los IDS utilizan tres tipos de información: un histórico de eventos, la configuración actual del sistema y, finalmente, procesos activos del sistema o reglas.

![intrusion detection system](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/1intrusion-detection-systen.png?raw=true)

## **¿En qué consiste un IDS y cómo funciona?**

Hemos de partir de la base que aunque tengamos el cortafuegos habilitado, por normal general, tendremos muchos puertos abiertos, como por ejemplo el 80 y el 443 para las aplicaciones web. Por lo que debemos tener un sistema adicional que nos ayude a controlar estas puertas abiertas. Por lo que para llevar un mayor control debemos de utilizar un sistema IDS, esto es, un sistema de detección de intrusos y también de vulnerabilidades. Existen los IDS activos y los pasivos. Con los primeros se genera entradas en el registro y se generan alertas. Con los segundos en cambio, además de realizar las mismas funciones que con el pasivo, también se generarían acciones, como bloquear direcciones IP o cerrar el acceso a puertos restringidos.

Además desde el punto de vista del programación (*software*) existen diferentes tipos de herramienta, los sistemas de detección de intrusos (HIDS), sistemas de detección de intrusos en red (IDPS), los sistemas de detección de intrusos basados en firmas (SIDS) y por último los sistemas de detección de intrusos basados en anomalías.

![network intrusion detection](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/2network-intrusion-detection.es.png?raw=true)

Los sistemas IDS utilizan tres métodos para detectar el tráfico. Estos son la detección de anomalías, el análisis de protocolos y el análisis de firmas.

- Con la detección de anomalías tenemos como objetivo detectar un comportamiento anormal. Ejemplo de ello sería un volumen de tráfico ICMP (el que usa ping) inusual y muy elevado, que nos indicaría que somos el blanco o el emisor de un ataque de DDoS (Denegación de servicio)
- Respecto al análisis de protocolos se busca un tráfico de aplicación que no cumple el estándar del protocolo habitual.
- Por último, el análisis de firmas permite identificar ataques o comportamientos perjudiciales ya publicados. Suele ser la técnica más eficaz y la que no está sujeta a errores, ya que sólo se generan ataques o intrusiones que ya han tenido éxito en otro lugar, por lo que, pueden ser fácilmente identificados.

Es importante que nuestro IDS actualice la información de forma habitual, para así tener actualizadas siempre sus técnicas de análisis así como de las bases de datos de firmas.

Existen una serie de organizaciones, asociaciones y empresas que nos permiten estar al corriente de las evoluciones en materia de técnicas de intrusión y ataques. Las principales son:

- Bugtraq: Es una lista de difusión dedicada a la publicación de vulnerabilidades, su uso y corrección. ( [https://www.securityfocus.com/](https://www.securityfocus.com/))
- CERT: *Computer Emergency Response Team*. Se trata de una organización que estudia las vulnerabilidades, investiga las evaluaciones en términos de redes y seguridad y ofrece servicios relacionados con la seguridad. ([Entrada de Wikipedia al respecto](https://es.wikipedia.org/wiki/Equipo_de_Respuesta_ante_Emergencias_Inform%C3%A1ticas))
- CIAC: Computer Incident Advisory Capability. Una organización de alerta e investigación gestionado por el departament de energía de Estados Unidos. ( [https://www.energy.gov/cio/about-our-services/integrated-joint-cybersecurity-coordination-center](https://www.energy.gov/cio/about-our-services/integrated-joint-cybersecurity-coordination-center))

**Tareas de un IDS**

Un IDS realiza dos tareas fundamentales:

- Prevención: se realiza por medio de herramientas que escuchan el tráfico en la red o en un ordenador, denominados sensores, e identifican los ataques aplicando reglas, reconocimiento de patrones o técnicas inteligentes.
- Reacción: trata de detectar patrones de intrusión en las trazas de los servicios de red o en el comportamiento del sistema.

Existen indicadores estadísticos de sensibilidad, especificidad y precisión que permiten comprobar la efectividad del IDS, se basan en los siguientes conceptos:

- Verdaderos positivos (TP): Intrusión existente y correctamente detectada.
- Falsos positivos (FP): Intrusión no existente e incorrectamente detectada.
- Falsos negativos (FN): Intrusión existente y no detectada.
- Verdaderos negativos (TN): Intrusión no existente y no detectada.

**Tipos de IDS**

Existen distintas clasificaciones de los IDS, según sea su enfoque, origen de datos, estructura y comportamiento

![intrusion detection system clasification](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/3intrusion-detection-system-clasification.png?raw=true)

## **En función del enfoque**

Se presentan dos grupos: Los sistemas de detección de usos indebidos, que comparan las firmas con la información recogida; y los de detección de anomalías, que usan técnicas estadísticas para distinguir el comportamiento usual del anormal.

**Detección de anomalías:** Es necesario definir cuál es el comportamiento normal de un sistema por medio de un aprendizaje de actividades, para clasificar los comportamientos que se desvíen de lo normal como sospechosos. Estos sistemas son propensos a dar falsos positivos, que son producidos cuando se dispara una alerta con actividad normal. Tienen la desventaja de que depende de la calidad del proceso de aprendizaje. Existen tres técnicas diferentes para realizar la detección de anomalías en un sistema:

- **Sistemas basados en conocimiento:** Representa el inicio en los IDS, y se basa en las violaciones de seguridad detectadas mediante el uso de reglas. Resultan más fiables y proporcionan mejores rendimientos frente a ataques conocidos, con el inconveniente de su baja capacidad para detectar nuevos ataques no incluidos en la base de datos de firmas.
- **Sistemas basados en métodos estadísticos**: Basado en perfiles de actividad que vienen definidos por el comportamiento del usuario, con respecto a ficheros, programas, registros, etc. Se realiza mediante el establecimiento de métricas y modelos estadísticos.
- **Sistemas basados en aprendizaje automático:** Son los más desarrollados para el modelado de comportamientos normales y buscan mejorar los resultados en cuanto a detección, reducción de falsos positivos y tiempo de computación. Una ventaja reside en recoger las características de un ataque y añadirlo a una base de datos como firmas nuevas, permitiendo actualizar la base de firmas en un breve lapso de tiempo.
- **Detección de usos incorrectos (detección por firma/regla):** Los sistemas de detección basados en uso indebido monitorizan las actividades que ocurren en un sistema y las compara con una base de datos de firmas de ataques. Cuando se encuentra una actividad que coincide con una de estas firmas, se genera una alarma. Presentan una facilidad de adaptación ya que basta con actualizar la base de datos, ya sea, escribiendo la nueva regla u obteniéndola de un tercero.
- **Sistemas Expertos:** Conocimiento codificado mediante reglas de implicación (condición-acción), si se cumplen todas las condiciones se aplica la acción o regla. Presenta la desventaja de que las reglas no son secuenciales, lo que dificulta aislar pasos de intrusiones en el tiempo.
- **Detección de firmas:** Realiza comparaciones entre los eventos que ocurren en el sistema y las firmas almacenadas en la base de datos en busca de similitudes.
- **Análisis de transacción de estados:** Los ataques se representan como una secuencia de transiciones (máquina de estados finitos). Cuando se alcanza un estado considerado como intrusión se lanza una alarma.
- **Híbridos:** Los IDS basados en firmas resultan más fiables y proporcionan mejores rendimientos frente a ataques conocidos, pero presentan una deficiencia ante nuevos ataques. Los IDS basados en anomalías presentan la capacidad de detectar ataques desconocidos, pero su rendimiento es inferior. Los sistemas híbridos serán una mezcla de ambos, y por lo tanto, pueden ajustarse para operar como ambos tipos de detectores, mejorando la funcionalidad, la detección de ataques y la mejora de rendimiento.

## **En función del origen de los datos**

Se encuentran tres tipos de IDS atendiendo a las fuentes de información que se utilicen:

**HIDS (*Host-based Intrusion Detection Systems*):** Los IDS basados en el host solo procesan información de las actividades de los usuarios y servicios en una máquina determinada. Permite monitorizar los datos generados por un usuario, mediante el uso de *syslog1*, e identificar amenazas e intrusiones a nivel de host. Una desventaja proviene del requerimiento de confianza en el sistema, que puede estar infectado anteriormente a la instalación, y lo hace vulnerable ante ataques directos.

**NIDS (*Network Intrusion Detection Systems*):** Los NIDS son instalados en un dispositivo en modo promiscuo, realizan una escucha pasiva sobre la red de forma que no interfieren en su uso, analizando el tráfico en tiempo real, pero por contra, resultan inútiles ante ataques locales. Los nuevos sistemas, basados en agentes inteligentes, permiten una detección de nuevos ataques usando el concepto de centinelas, que supervisan el sistema para recoger toda la información necesaria para la detección.

![network intrusion detection systems](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/4network-intrusion-detection-systems.png?raw=true)

**IDS Híbridos:** Los sistemas híbridos recogen lo mejor de ambos tipos HIDS y NIDS. Permiten una detección local de los sistemas y un sensor en cada segmento de red se encarga de la vigilancia. De esta forma se cubren las necesidades HIDS con las del NIDS, permitiendo el aprovechamiento de las ventajas de ambas arquitecturas.

## **En función de su estructura**

Clasificación basada en las estrategias de control:

**Sistema de Detección de Intrusión Distribuido (DIDS):** Se basa en la instalación en un sistema distribuido, ubicando sensores repartidos por varios equipos de la red. Estos sensores se comunican con un nodo central donde se recibirá toda la información y donde se cruzan los datos, lo que nos permitirá detectar los ataques con fiabilidad y obtener una visión global mejorando la detección de incidentes.

![distributed intrusion detection systems](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/5distributed-intrusion-detection-systems.es.png?raw=true)

**Sistema de Detección de Intrusión Centralizado:** Emplea sensores que transmiten información a un sistema central que realiza el control, permitiendo ahorrar en equipamientos.

![centralized instrusion detection system](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/6centralized-instrusion-detection-system.png?raw=true)

**En función de su comportamiento**

Encontramos dos tipos de IDS según si realizan la prevención escuchando el tráfico o si se elabora una respuesta defensiva cuando se detecta un ataque.

**IDS Pasivo:** Sólo notifican al administrador de la red pero no actúan sobre el ataque. Únicamente procesan la información en busca de intrusiones, y una vez detectada se genera una alerta.

**IDS Activos:** Es un tipo de IDS denominado Sistema de Prevención de Intrusión (IPS). A diferencia de los IDS, esta tecnología no se limita a escuchar el tráfico de la red y a mandar alertas, sino que permite establecer reglas, como se lo hace en los cortafuegos, para detener las intrusiones.
