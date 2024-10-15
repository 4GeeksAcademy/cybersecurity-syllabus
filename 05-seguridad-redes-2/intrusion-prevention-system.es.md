---
title: "Sistemas De Prevencion De Instrusos (IPS)"
description: "Los Sistemas de Prevención de Intrusos (IPS) son esenciales en la ciberseguridad, capaces de neutralizar amenazas en tiempo real. Con una reducción de falsos positivos, estos sistemas proactivos son cruciales para proteger redes en un mundo digital donde el 60% de las empresas sufren ataques cibernéticos."
technologies: ["ciberseguridad", "redes"]
keyword_es: sistemas de prevención de intrusos 0 - 10

---

En un mundo cada vez más digital, las amenazas cibernéticas son una preocupación constante para las organizaciones. Los Sistemas de Prevención de Intrusos (IPS) son una respuesta crucial a este desafío, actuando como defensores proactivos en la seguridad de la red. A diferencia de los Sistemas de Detección de Intrusos (IDS), que sólo detectan y alertan sobre posibles amenazas, los IPS están diseñados para identificar y neutralizar intrusiones en tiempo real.

## ¿Qué es un Sistemas De Prevencion De Instrusos?

Los IPS son dispositivos de hardware o software encargados de revisar el tráfico de red con el propósito de detectar y responder a posibles ataques o intrusiones. Su respuesta consiste en descartar o modificar los paquetes procedentes del ataque de tal manera que se anule su propósito. Este comportamiento los clasifica como dispositivos proactivos debido a su reacción automática a situaciones anómalas.

### Diferencias entre IPS e IDS

Mientras que un IDS se limita a detectar y notificar la intrusión al administrador del sistema, un IPS detecta y detiene la intrusión de manera predefinida. Esto se logra comprobando comportamientos de red previamente configurados como anómalos. Esta capacidad de acción inmediata distingue a los IPS como una evolución natural de los IDS, que simplemente observan y reportan.

## Funcionamiento de los Sistemas De Prevencion De Instrusos

Los IPS se asemejan al comportamiento de los cortafuegos, ya que ambos toman decisiones sobre la aceptación de paquetes en un sistema. Sin embargo, los cortafuegos basan sus decisiones principalmente en los encabezados de los paquetes (capas de red y de transporte), mientras que los IPS consideran tanto los encabezados como el contenido de los datos del paquete. Esto permite una visión más exhaustiva de las operaciones de la red, proporcionando información sobre actividades maliciosas, malas conexiones, contenido inapropiado y otras funciones, con una mínima vigilancia.

![intrusion prevention system](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/7intrucion-prevension-system.png?raw=true)

### Encabezado y contenido de paquetes dependiendo del protocolo

Las principales características de los IPS incluyen:

- **Capacidad de reacción automática ante incidentes.**
- **Aplicación de nuevos filtros conforme detecta ataques en progreso.**
- **Bloqueo automático frente a ataques efectuados en tiempo real.**
- **Disminución de falsas alarmas de ataques a la red.**
- **Protección de sistemas no parcheados.**
- **Optimización en el rendimiento del tráfico de la red.**

## Tipos de Sistemas De Prevencion De Instrusos

Los diferentes tipos de IPS se distinguen principalmente por su ubicación y enfoque:

- **IPS basados en host (HIPS):** Residen en la dirección IP específica de un solo equipo y permiten prevenir posibles ataques en el host.
- **IPS basados en red (NIPS):** Monitorizan la red en busca de tráfico sospechoso.
- **IPS basados en red inalámbrica (WIPS):** Monitorizan redes inalámbricas, al igual que los NIPS lo hacen con redes LAN.
- **IPS basados en Análisis de Comportamiento de Red (NBA):** Examina el tráfico de red para identificar amenazas que generan tráfico inusual, como ataques de DoS o malware.

## Comparación: NIPS vs. HIPS

- **HIPS**: Pueden manejar tráfico cifrado y sin cifrar, ya que analizan los datos después de que han sido descifrados en el host. Sin embargo, utilizan el procesador y la memoria del host, lo que puede impactar su rendimiento.
- **NIPS**: Pueden detectar eventos dispersos a través de la red y reaccionar fácilmente, pero no impactan el rendimiento del host, ya que operan independientemente del hardware del mismo.

## Evolución y categorías de los Sistemas De Prevencion De Instrusos

La evolución de los IPS ha seguido dos generaciones históricas:

- **Primera generación**: Al detectar un ataque proveniente de una dirección IP, descartaban todos los paquetes de esa dirección, independientemente de su relación con el ataque.
- **Generación moderna**: Capaces de descartar únicamente los paquetes relacionados con el ataque identificado, permitiendo el tráfico legítimo de otros paquetes provenientes de la IP del atacante.

Existen cinco categorías de IPS según su funcionamiento, capacidades y ubicación en la arquitectura de la red:

- **IPS *inline***: Son la evolución de los NIDS basados en firmas y funcionan como un Bridge a nivel de capa dos, revisando todos los paquetes en busca de firmas. Pueden almacenar automáticamente las anomalías detectadas en un log y permitir el paso de un paquete alterando su contenido para frustrar un ataque sin alertar al atacante. Este proceso se realiza mediante *Scrubbing*, que detecta errores a través de la verificación *checksum* o por redundancia con copias de datos.

- **Switches a nivel de la capa de Aplicación (nivel 7 del modelo OSI)**: Aunque los switches trabajan habitualmente en el nivel 2 (enlace), también existen switches de nivel 7 debido a la alta demanda de ancho de banda. Su función principal es balancear la carga de las aplicaciones distribuidas entre varios servidores, tomando decisiones de enrutamiento a partir del contenido de los datos de la capa de aplicación. Aunque similares a un balanceador de carga, en su funcionamiento como IPS son capaces de bloquear ataques, posicionándose generalmente delante de los cortafuegos para proteger la red completa.

- **Cortafuegos/IDS de Aplicación**: Conocidos como HIPS, estos se instalan en cada host que se desea proteger y requieren una fase de entrenamiento para identificar patrones normales de funcionamiento en el host. A través de este entrenamiento se crea un perfil de relaciones frecuentes entre las aplicaciones y los componentes del sistema. Al apoyarse en la detección de comportamientos anómalos, son capaces de prevenir intrusiones recientes para las cuales aún no existe una definición de firmas específicas.

- **Switches Híbridos**: Combinan características de los HIPS y los switches de nivel de aplicación. Se basan en el análisis de patrones de comportamiento, ofreciendo una fortaleza particular en el conocimiento detallado del tráfico aceptable.

- **Aplicaciones engañosas**: Esta tecnología analiza todo el tráfico de red y de cada dispositivo para conocer el tráfico permitido y correcto. Al detectar tráfico no permitido, envían una respuesta marcada al atacante, lo que permite identificar y bloquear más tráfico de la misma fuente.

## Beneficios y desafíos

![ventajas intrusion prevention system](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/8ventajas-intrusion-prevesion-system.es.png?raw=true)

### Ventajas de los IPS

Los IPS ofrecen varios beneficios importantes:

- **Respuesta en tiempo real**: Actúan rápidamente para mitigar amenazas antes de que causen daño.
- **Protección proactiva**: Identifican y bloquean amenazas emergentes sin necesidad de intervención manual.
- **Reducción de falsos positivos**: Mediante ajustes y aprendizaje continuo, los IPS reducen las interrupciones innecesarias.

### Desafíos de implementación de los IPS

- **Falsos positivos y negativos**: Un IPS mal configurado puede reaccionar a amenazas inexistentes o no detectar amenazas reales.
- **Costo y complejidad**: La implementación y mantenimiento de un IPS puede ser costoso y complejo, especialmente en redes grandes.

## Tendencias emergentes

- **Inteligencia Artificial y Machine Learning**: La integración de IA y ML en los IPS está mejorando su capacidad para detectar patrones anómalos y predecir amenazas futuras.
- **IPS basados en la nube**: Ofrecen una solución escalable y flexible, permitiendo a las organizaciones protegerse sin grandes inversiones en infraestructura.

### Conclusión

Los Sistemas de Prevención de Intrusos (IPS) son una parte esencial de la ciberseguridad moderna, proporcionando una defensa proactiva contra amenazas complejas. Aunque enfrentan desafíos como la gestión de falsos positivos y el costo de implementación, su capacidad para responder rápidamente a amenazas emergentes los hace indispensables en cualquier estrategia de seguridad integral.
