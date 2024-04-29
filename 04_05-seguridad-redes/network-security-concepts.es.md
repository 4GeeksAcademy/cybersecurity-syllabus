## Tendencias actuales en seguridad en redes

- **Permanece el riesgo asociado al teletrabajo.** El regreso a la oficina en 2022 va a ser más lento de lo inicialmente previsto. Es más, gran parte del teletrabajo generado durante la crisis sanitaria permanecerá, y se consolidarán los entornos laborales híbridos. Esto va a hacer que todo lo relacionado con la *ciberseguridad de ubicaciones remotas* continuará teniendo protagonismo. Las organizaciones están terminando de definir y fijar sus estrategias y políticas de seguridad para estos nuevos entornos híbridos, de manera que la postura de seguridad sea la misma en todos los entornos de red de la organización, independientemente de dónde se encuentren.
- **DNS sobre HTTPS (DoH) como vector de amenazas.** El creciente uso de servicios DoH está en aumento por parte de las organizaciones, y los cibercriminales van a tratar de explotar este sistema como vector de ataque, ya que proporciona un canal encriptado hacia el servidor DoH y los desarrolladores de malware son conscientes de que es un medio para eludir los controles de seguridad. Muchos proveedores de servicios y empresas están implementando DoH como una estrategia defensiva, con el objetivo de tener su propia infraestructura DNS y evitar depender de servidores DoH de terceros, pero esto puede suponer un riesgo.
- **Estrategias Zero Trust.** La proliferación de entornos de trabajo híbridos y distribuidos y de entornos de red IoT incrementará en 2022 la adopción de estrategias de seguridad *“Zero Trust”*. Una estrategia “Zero Trust” consiste en la creación de “listas blancas” de dispositivos a los que se les concede acceso a red y a los recursos de TI, una vez que han sido inventariados y securizados de acuerdo con las políticas de seguridad corporativas. Esta estrategia evitará que dispositivos IoT o dispositivos personales de teletrabajadores sean utilizados como vectores de ataque sobre DNS. En estas estrategias jugarán un papel fundamental las *soluciones de seguridad DNS* inteligentes que permitan realizar filtrado estricto de dispositivos en base a estas listas blancas. Cualquier solicitud de DNS sólo será resuelta si se hace contra un dominio reconocido y autorizado, todas las demás serán denegadas.
- **Phising y exflitración de datos.** El phising seguirá siendo, junto con el ransomware, una de las principales amenazas que hacen crecer los costes de las brechas de seguridad para las empresas. La exfiltración de datos se produce ya sea por intrusiones en red, por la pérdida de dispositivos corporativos con información sensible o mediante herramientas de malware.
    
    Según un informe de IDC un 26% de las empresas encuestadas manifestaron haber sufrido brechas de seguridad con exfiltración de datos como resultado de ataques vía DNS. En 2024, las empresas utilizarán cada vez más *DNS como primera línea de defensa*, para monitorizar el tráfico IP e identificar y prevenir el robo de datos.
    
- **Ransomware como Servicio (RaaS).** El Ransomware ha crecido durante los dos últimos años de manera exponencial, y ya en 2023 se ha experimentado un crecimiento en el denominado *Ransomware como Servicio (RaaS)*.Ambas modalidades seguirán siendo protagonistas en 2024 Como en otras áreas, los ciberdelincuentes también están utilizando los nuevos modelos de entrega de servicios de TI disponibles en el mercado. Muchas organizaciones criminales carecen de las habilidades para crear su propio ransomware y contratan este servicio en la red. La utilización de ataques RaaS con objetivos muy precisos está siendo lucrativo para los ciberdelincuentes. No son ataques masivos, sino que se utiliza ingeniería social para elaborar vectores de ataque de apariencia legítima, como correos electrónicos bien elaborados. En otros casos, los actores de amenazas pueden apuntar a vulnerabilidades específicas de un grupo de víctimas objetivo.

## **Retos y oportunidades para la seguridad en redes**

La seguridad de las redes es el área de la ciberseguridad que se centra en la protección de las redes informáticas frente a las ciberamenazas. Tiene tres objetivos principales: impedir el acceso no autorizado a los recursos de la red, detectar y neutralizar los ciberataques y las violaciones de la seguridad en curso, y garantizar que los usuarios autorizados tengan un acceso seguro a los recursos de la red que necesitan, cuando los necesitan.

El riesgo de ciberataque aumenta al tiempo que crece el tamaño y la complejidad de las redes. Por ejemplo, según el informe Coste de una violación de datos de 2022 de IBM, el 83% de las organizaciones encuestadas han sufrido más de una violación de datos, es decir, una brecha de seguridad que ha dado lugar a un acceso no autorizado a información sensible o confidencial. Estos ataques son extremadamente costosos: el coste medio de una violación de datos en todo el mundo es de 4,35 millones de dólares, cifra que se duplica con creces en Estados Unidos (9,44 millones de dólares).

La seguridad de la red protege la integridad de la infraestructura, los recursos y el tráfico de la red para frustrar estos ataques y minimizar sus repercusiones financieras y operativas.

### **Tipos de tecnologías de seguridad de la red**

Los sistemas de seguridad de la red operan en el perímetro y dentro de la red.

En el perímetro, los controles de seguridad intentan impedir que las ciberamenazas entren en la red. Pero los atacantes a veces consiguen infiltrarse, razón por la cual los equipos de seguridad de redes también implantan controles en torno a los recursos dentro de la red, como ordenadores portátiles y datos. Incluso si los atacantes consiguen infiltrarse en la red, no tendrán vía libre. Esta estrategia, que consiste en colocar una serie de dispositivos de control entre los hackers y las posibles vulnerabilidades, se conoce como "defensa en profundidad".

Cada reto contrae una oportunidad de mejora y hay mucho sobre lo que trabajar ya que en este 2024 se espera, como cada año, un aumento en la actividad de los ciber criminales y mayor sofisticación tanto en técnicas como en herramientas. Puntualicemos los casos fundamentales a tener en cuenta sobre lo que más debemos prestar atención. El establecimiento de sistemas de seguridad de red implica la combinación de las siguientes herramientas:

### **Cortafuegos**

Un cortafuegos es un software o hardware que impide que el tráfico sospechoso entre o salga de una red, al tiempo que permite el paso del tráfico legítimo. Los cortafuegos pueden instalarse en el extremo de una red o utilizarse internamente para dividir redes más grandes en subredes más pequeñas. De este modo, si una parte se ve comprometida, los piratas informáticos no pueden acceder al resto de la red.

Existen diferentes tipos de cortafuegos con diferentes características. Los cortafuegos básicos utilizan el filtrado de paquetes para inspeccionar el tráfico. Los sistemas de nueva generación, más avanzados, ofrecen una protección mejorada con prevención de intrusiones, IA y aprendizaje automático, vigilancia y control de aplicaciones, además de alimentación de inteligencia sobre amenazas.

### **Control de acceso a la red (NAC)**

Las soluciones de control de acceso a la red (NAC) actúan como guardianes, autenticando y autorizando a los usuarios para determinar quién está autorizado a acceder a la red y qué puede hacer en ella. La "autenticación" consiste en comprobar que un usuario es quien dice ser. La parte de "autorización" consiste en conceder a los usuarios autenticados autorización para acceder a los recursos de la red.

Las soluciones NAC se utilizan a menudo para aplicar políticas de control de acceso basado en funciones (RBAC), que exigen que los privilegios de los usuarios reflejen sus funciones. Por ejemplo, los desarrolladores junior pueden ver y editar código, pero no ponerlo en producción. Los desarrolladores senior, en cambio, están autorizados a leer, escribir y poner código en producción. El sistema RBAC ayuda a evitar la violación de datos al mantener a los usuarios no autorizados alejados de los recursos a los que no tienen derecho de acceso.

Además de autenticar a los usuarios, algunas soluciones NAC pueden evaluar los riesgos en los terminales de los usuarios. El objetivo es impedir que los dispositivos no seguros o comprometidos accedan a la red. Si un usuario intenta acceder a la red en un dispositivo equipado con un software antimalware obsoleto o mal configurado, el sistema denegará el acceso. Algunas herramientas NAC avanzadas son incluso capaces de resolver automáticamente los problemas de no conformidad de los terminales.

### **Sistemas de detección y prevención de intrusiones (IDPS)**

Un sistema de detección y prevención de intrusiones (IDPS), a veces denominado simplemente sistema de prevención de intrusiones (IPS), puede desplegarse directamente detrás de un cortafuegos para analizar el tráfico entrante en busca de amenazas a la seguridad. Estas herramientas derivan de los sistemas de detección de intrusos (IDS), que se limitaban a señalar las actividades sospechosas para su examen. Los sistemas IDPS son ahora capaces de reaccionar automáticamente ante posibles infracciones, por ejemplo bloqueando el tráfico o restableciendo la conexión. Son especialmente eficaces para detectar y bloquear ataques de fuerza bruta, denegación de servicio (DoS) y denegación de servicio distribuida (DDoS).

### **Redes privadas virtuales (VPN)**

Una red privada virtual (o VPN del inglés "virtual private network") se utiliza para proteger la identidad de un usuario cifrando sus datos y enmascarando su dirección IP y su ubicación. Cuando alguien utiliza una VPN, ya no se conecta directamente a Internet, sino a un servidor seguro que se conecta a Internet en su nombre.

Las VPN permiten a los teletrabajadores acceder a las redes corporativas con total seguridad, incluso a través de conexiones wifi públicas no seguras, como las que se encuentran en cafeterías y aeropuertos. Las VPN cifran el tráfico de los usuarios, protegiéndolo de los hackers que quieran interceptar sus comunicaciones.

En lugar de VPN, algunas organizaciones utilizan el modelo Zero Trust Network Access (o ZTNA del inglés "acceso a red de confianza cero").En lugar de utilizar un servidor proxy, ZTNA conecta a los usuarios remotos de forma segura utilizando políticas de control de acceso zero trust. Cuando los usuarios remotos se conectan a una red a través de ZTNA, no obtienen acceso a toda la red. Solo tienen acceso a los recursos que están autorizados a utilizar, y deben ser controlados cada vez que acceden a un nuevo recurso.

### **Seguridad de aplicaciones**

La seguridad de las aplicaciones se refiere a las medidas adoptadas para proteger las aplicaciones y las interfaces de programación de aplicaciones (API) de los atacantes. En la actualidad, muchas empresas utilizan aplicaciones para llevar a cabo funciones empresariales esenciales o procesar datos confidenciales, por lo que los ciberdelincuentes suelen atacar las aplicaciones. Y como muchas aplicaciones empresariales están alojadas en nubes públicas, los piratas informáticos pueden aprovechar sus vulnerabilidades para entrar en las redes privadas de las empresas.

Las medidas de seguridad de las aplicaciones las protegen de los agentes maliciosos. Las herramientas más habituales son los cortafuegos de aplicaciones web (WAF), la autoprotección de aplicaciones en tiempo de ejecución (RASP) y las pruebas de seguridad estática y dinámica de aplicaciones (SAST y DAST).

### **Seguridad del correo electrónico**

El índice X-Force Threat Intelligence de IBM Security muestra que el phishing es el vector inicial de ciberataque más común. Las herramientas de seguridad del correo electrónico pueden ayudar a frustrar los ataques de phishing y otros intentos de poner en peligro el correo electrónico de los usuarios. La mayoría de los servicios de correo electrónico incluyen herramientas de seguridad, como filtros antispam y cifrado de mensajes. Algunas herramientas están equipadas con sandboxes, es decir, entornos aislados en los que los equipos de seguridad pueden inspeccionar los archivos adjuntos al correo electrónico en busca de malware sin exponer la red.

### **Tecnologías de seguridad asociadas**

Aunque las siguientes herramientas no son estrictamente herramientas de seguridad de red, los administradores las utilizan a menudo para proteger zonas y activos de la red.

La prevención de la pérdida de datos (DLP) se refiere a las estrategias y herramientas de seguridad de informática que impiden el robo o la filtración accidental de datos sensibles. Este enfoque aúna políticas de seguridad y tecnologías especializadas que rastrean los flujos de datos, cifran la información sensible y activan alertas si se detectan actividades sospechosa.

Las soluciones de seguridad para puntos finales protegen todos los dispositivos que se conectan a una red (portátiles, ordenadores de sobremesa, servidores, dispositivos móviles, dispositivos IoT) de los hackers que intentan utilizarlos para infiltrarse en la red. El software antivirus puede detectar y destruir troyanos, spyware y otros programas maliciosos en un dispositivo antes de que se propaguen al resto de la red. Las soluciones de detección y respuesta de puntos finales (EDR) son herramientas más avanzadas que supervisan el comportamiento de los puntos finales y reaccionan automáticamente ante los eventos que amenazan la seguridad. El software de gestión unificada de puntos finales (UEM) permite a las organizaciones supervisar, gestionar y proteger todos los dispositivos de los usuarios finales desde una única consola.

Las soluciones de seguridad web, como las pasarelas web seguras, bloquean el tráfico de Internet malicioso e impiden que los usuarios se conecten a sitios y aplicaciones sospechosos.

La segmentación de redes es una forma de dividir grandes redes en subredes más pequeñas, ya sea físicamente o mediante software. Esta técnica limita la propagación de ransomware y otros programas maliciosos aislando una subred comprometida del resto de la red. También tiene la ventaja de mantener a los usuarios legítimos alejados de recursos a los que no deberían tener acceso.

Las soluciones de seguridad en la nube protegen los centros de datos, las aplicaciones y otros activos de la nube contra los ciberataques. En la mayoría de los casos, se trata simplemente de medidas de seguridad de red estándar (cortafuegos, NAC y VPN) aplicadas a entornos en nube. Muchos proveedores de servicios en la nube incorporan controles de seguridad en sus servicios o los ofrecen como complementos.

El análisis del comportamiento de usuarios y entidades (UEBA) utiliza el análisis del comportamiento y el aprendizaje automático para detectar actividades anómalas de usuarios y dispositivos. UEBA se utiliza para detectar amenazas internas y piratas informáticos que se han apoderado de cuentas de usuario.

### **Un enfoque zero trust para la seguridad de la red**

En el pasado, las redes corporativas estaban centralizadas, con terminales, datos y aplicaciones clave ubicados en las instalaciones de la empresa. Los sistemas de seguridad de aquella época se centraban en impedir que las amenazas atravesaran el perímetro de la red. Una vez que un usuario estaba dentro, se le consideraba de confianza y tenía un acceso prácticamente ilimitado.

Sin embargo, a medida que las organizaciones se digitalizan y adoptan entornos de nube híbrida, las redes se descentralizan cada vez más. Los recursos de red pueden encontrarse ahora en la nube (centro de datos), en dispositivos locales y remotos, así como en dispositivos móviles e IoT.

Los controles de seguridad a nivel perimetral son menos eficaces para las redes distribuidas, razón por la cual muchos equipos de seguridad informática están recurriendo al zero trust. Este tipo de seguridad coloca controles alrededor de cada recurso y no en el perímetro. La confianza depositada en los usuarios nunca es implícita. Cada vez que alguien intenta acceder a un recurso, debe ser autenticado y autorizado, aunque ya se encuentre en la red corporativa. A los usuarios autentificados sólo se les concede el acceso menos privilegiado, y sus autorizaciones se revocan en cuanto finaliza la tarea.

La seguridad de red zero trust se basa en políticas de acceso precisas, validación continua y datos recogidos de tantas fuentes como sea posible (incluidas la mayoría de las herramientas descritas anteriormente) para garantizar que sólo los usuarios adecuados puedan acceder a los recursos adecuados, por las razones adecuadas y en el momento adecuado.

## Soluciones de seguridad para redes empresariales

Aunque un enfoque de defensa en profundidad puede proteger la red de una empresa, también requiere que el equipo de seguridad informática gestione una serie de controles independientes. Las plataformas de seguridad de redes empresariales pueden ayudar a agilizar la gestión integrando herramientas dispares y permitiendo a los equipos supervisar toda la red desde una única consola. Las plataformas de seguridad de red más comunes son:

Las soluciones de gestión de eventos e información de seguridad (SIEM) recopilan información de las herramientas de seguridad internas, la cotejan en un registro central e informan de las anomalías. Las soluciones de orquestación, automatización y respuesta en materia de seguridad (SOAR) recopilan y analizan datos de seguridad, lo que permite a los equipos de especialistas definir y ejecutar medidas automatizadas en caso de ciberamenazas. Las herramientas de detección y respuesta de red (NDR) utilizan IA y aprendizaje automático para supervisar el tráfico de red y detectar actividades sospechosas.

Las soluciones de detección y respuesta extendidas (XDR) son una arquitectura de ciberseguridad abierta que integra herramientas y operaciones de seguridad para todas las capas: puntos finales, correo electrónico, aplicaciones, redes, cargas de trabajo en la nube y datos. Con XDR, las soluciones de seguridad que no están necesariamente diseñadas para trabajar juntas pueden interoperar sin problemas en la prevención, detección, investigación y respuesta ante amenazas. XDR también puede automatizar la detección de amenazas, la clasificación de incidentes y los flujos de trabajo de búsqueda de amenazas.
