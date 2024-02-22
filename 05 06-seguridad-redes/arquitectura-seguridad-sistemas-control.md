# **Arquitecturas de seguridad para sistemas de control**

## **Arquitectura de seguridad con IDS**

La primera arquitectura, presentada en la Figura, describe la colocación de dispositivos de tipo IDS para monitorizar el tráfico dentro de la red de control. Para ello, todo el tráfico que pasa por los router/switches se lleva al sensor del IDS a través de puertos espejo (*mirror/SPAN*). También se añade una sonda para recibir información del cortafuegos y tener así controlado el tráfico intercambiado con la red correspondiente a la zona empresarial. Los IDS deberán de disponer de las reglas adecuadas para generar las alertas oportunas que serán mostradas al operario o administrador de seguridad correspondiente a través de la consola.

![Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image3.png](Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image3.png)

## **Arquitectura de seguridad con IPS**

La evolución de una arquitectura de seguridad con IDS pasa por bloquear tráfico. Para ello es necesario que los sensores pasen a estar en medio del tráfico, en lugar de escuchando el tráfico a través de los puertos espejo (*mirror/SPAN*), como refleja la Figura. La configuración de reglas debe ser adecuada para que no se interrumpa el flujo de tráfico de control habitual y solo se bloqueen las intrusiones y fallos de seguridad. La situación de los sensores IPS es similar a la de los sensores IDS, y el funcionamiento será exactamente el mismo, generando alerta que serán mostradas en la consola de IDS.

![Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image4.png](Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image4.png)

## **Arquitectura de seguridad con SIEM**

La Figura representa la instalación de un SIEM dentro de los sistemas de control. Hay que tener en cuenta que el SIEM se dedica a recoger y gestionar eventos de log, por lo que las fuentes de datos provendrán de todos los dispositivos. En este caso hay que tener cuidado con las comunicaciones, ya que todos los dispositivos deben poder enviar sus registro de eventos hasta el SIEM, y esto puede implicar una sobrecarga de tráfico en la red. La mejor forma de solucionar esta sobrecarga es disponer de una red exclusiva para el envío de estos mensajes.

![Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image5.png](Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image5.png)

## **Arquitectura unificada con IDS, IPS y SIEM**

La representación final (Ver Figura) muestra la puesta en conjunto de las tres tecnologías dentro de una arquitectura de red de sistemas de control. El IPS quedaría para los niveles superiores, controlando el tráfico intercambiado entre la parte de control y la parte corporativa o de negocio, los IDS gestionarían el tráfico entre la red de control y las de campo, informado de posibles anomalías en el tráfico; y el SIEM recogería la información del mayor número posible de dispositivos, incluyendo dispositivos de proceso y elementos de red, así como la información de las alertas tanto de los IDS como del IPS.

Las líneas rojas mostradas en las figuras indican los puntos donde tanto los sensores IDS como los sensores IPS se conectan para recabar el tráfico, y constituyen una conexión de red. La red de monitorización se utiliza como nexo de unión entre los sensores IDS/IPS y el núcleo central de gestión, y por este motivo no se requiere un acceso a dicha red desde ninguna otra parte de la arquitectura. Las líneas marcadas en verde que finalizan el en SIEM muestran de dónde se obtiene información y no conexiones de red reales. La información se enviará a través de las conexiones existentes, habilitando en el cortafuegos (y en su caso en el IDS/IPS) las reglas correspondientes

![Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image6.png](Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image6.png)

## **CONCLUSIONES**

Los sistemas de detección y prevención de intrusiones y los sistemas de tratamiento y gestión de eventos e incidentes aportan un nivel de seguridad a los sistemas de control siempre y cuando estén correctamente configurados y supervisados. La configuración de un sistema de prevención puede implicar muchos problemas sobre un sistema de control en producción, por lo que deben ser correctamente valoradas todas las implicaciones, así como realizar todas las posibles pruebas previamente, incluyendo las de mantener el sistema sólo en modo detección hasta estar totalmente seguros de que no se bloqueará tráfico crítico para el sistema e ir afinando progresivamente el sistema para que sólo detecte o informe de eventos importantes.

Los SIEM proporcionan información del estado del sistema a los operadores de seguridad, pero sólo son útiles si la información recogida es correctamente analizada. Centralizar todos los eventos en un único equipamiento tiene la ventaja de que todas las acciones ocurridas van a ser controladas en el mínimo tiempo y no se van a perder por tener que revisar múltiples aplicaciones. La inclusión de estas herramientas en la arquitectura de los sistemas de control puede ser compleja dependiendo del sistema que se quiera controlar, pero los beneficios van a compensar todo el esfuerzo invertido en el despliegue, ganando un control en la red y que permite asegurar el correcto funcionamiento del sistema sin intrusiones.
