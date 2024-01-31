# Lectura 10 📕: Planificación y documentación de redes

La planificación y documentación de redes es un proceso esencial para garantizar el diseño, implementación y mantenimiento efectivo de una red. Consiste en la creación de un plan estratégico que define los objetivos, requisitos y recursos necesarios para construir y gestionar una red de manera eficiente y segura esoimplica identificar las necesidades específicas de la organización, como el número de usuarios, los servicios requeridos y el volumen de tráfico esperado. También implica evaluar las tecnologías disponibles y seleccionar las más adecuadas para satisfacer las necesidades de la red.

### **Documentación de red: diagramas, inventario de equipos**

Mantener una documentación de la red es importante, ya que si una parte o toda la red queda fuera de servicio, esto puede tener un impacto negativo importante en la empresa. La documentación nos puede ayudar a tener un enfoque más sistemático para la resolución del problema con el fin de que vuelva a funcionar completamente lo antes posible.

Para que un administrador de la red pueda monitorear y resolver estos problemas de red, en necesario mantener una documentación que incluya

- Archivos de configuración incluidos los de la red y los del sistema final.
- Diagramas de topología física y lógicas

Con esta información, un administrador de red puede diagnosticar y corregir de manera eficaz los problemas de la red, según el diseño y el rendimiento esperado de la red en condiciones de operación normal.

### Archivos de configuración de red

Estos archivos contienen registros precisos y actualizados del hardware y el software usados en una red. Entre estos archivos debe existir una tabla con para cada dispositivo de red utilizado con toda la información relevante sobre ese dispositivo.

| Nombre y modelo del dispositivo | Nombre de interfaz | Dirección mac | Dirección IPV4 | Dirección IPV6 |
| --- | --- | --- | --- | --- |
| R1 Cisco 1941 152-A.M1 | G0/0 | 0071.8580.A350 | 192.168.5.1/24 | 2001:ad4:cafe:10::1/64 |
|  | G0/1 | 0071.8580.A351. | 192.168.10.1 | 2001:ad4:cafe::11::1/64 |

También podemos tener una lista de los archivos de configuración de sistema final, estos se centraron en el hardware y software usados en los dispositivos del sistema final, como servidores, consolas de administración de red y estaciones de trabajo de los usuarios

Esta lista nos ayudará ya que un sistema final mal configurado puede traernos un impacto negativo en el rendimiento general de la red. Es muy útil tener un registro de base que muestre el hardware y software usado en estos dispositivos para la resolución de problemas

| Nombre de dispositivo | Sistema operativo | Dirección MAC | Dirección IP | Gateway predeterminado | Servidor DNS | Aplicaciones de red |
| --- | --- | --- | --- | --- | --- | --- |
| PC2 | Windows 10 | 5475:DB04.9A3E | 192.168.15.5/24 | 198.168.15.1 | 192.168.15.15 | HTTP, FTP |
| SRV1 | Linux | 000C.D3691.A15B | 192.168.20.254/24 | 192.168.20.1 | 2200:DBB::ACAD:1::99 | HTTP, FTP |

### Diagramas de topología de red

Los diagramas de topología de red mantienen un registro de la ubicación, función y estado de todos los dispositivos de la red. Existen dos tipos de topologías:

- **Topología física**

Una topología física de la red muestra la distribución física de los dispositivos conectados a la red. Para resolver problemas de la capa física, es necesario conocer la forma en que los dispositivos están conectados físicamente. La información registrada en el diagrama generalmente incluye:

Tipo de dispositivo:

- Modelo y fabricante
- Versión del sistema operativo
- Tipo de cable e identificador
- Especificación del cable
- Tipo de conector
- Extremos de cables
- Topología lógica

La topología lógica de la red ilustra la forma en que los dispositivos se conectan a la red de manera lógica, es decir, cómo los dispositivos transfieren datos a través de la red al comunicarse con otros dispositivos.

Los símbolos se usan para representar los elementos de la red, como routers, servidores, hosts, concentradores VPN y dispositivos de seguridad. De manera adicional, se pueden mostrar conexiones entre varios sitios, pero no representan ubicaciones físicas reales. La información registrada en un diagrama de red lógico puede incluir lo siguiente:

- Identificadores de dispositivos
- Dirección IP y longitudes de prefijos
- Identificadores de interfaz
- Tipo de conexión
- DLCI para circuitos virtuales
- VPN de sitio a sitio
- Protocolos de routing
- Rutas estáticas
- Protocolos de enlace de datos
- Tecnologías WAN utilizadas

### **Planificacion de crecimiento de la red**

También es importante entender que una de las características más importante en el diseño de una red es que pueda ser escalable. Esto quiere decir que pueda tener una planificación para crecimiento en un futuro.

Esto nos permitirá asegurar que la calidad del servicio de la red sea óptima y pueda seguir funcionando a pesar de la gran demanda de crecimiento de usuarios, de esta forma, diseñar una red que funcione sin fallas y se adapte a las actualizaciones y cambios, resolverá problemas relacionados con la seguridad, la funcionalidad y la eficiencia.

Para que una red sea escalable se deberá tener en cuenta la capacidad de adaptación, el hacer foco en aumentar la capacidad de red añadiendo mayores puntos de acceso, o bien, generar una jerarquía de redes.

La utilización de servicios de la nube, el combinar varios puertos en uno y el buscar una solución inalámbrica, también serán la clave para poder expandir y conseguir la escalabilidad en sistemas distribuidos.

Para dar soporte a una red grande, mediana o pequeña, el diseñador de la red debe elaborar una estrategia que permita que la red esté disponible y se amplíe de manera eficaz y fácil. En una estrategia básica de diseño de redes se incluyen las siguientes recomendaciones:

Utilizar equipos ampliables y modulares o dispositivos agrupados que puedan actualizarse fácilmente para aumentar las capacidades. Los módulos de dispositivos pueden añadirse al equipo existente para apoyar nuevas características y dispositivos sin necesidad de grandes actualizaciones del equipo. Algunos dispositivos pueden integrarse en un grupo para que actúen como un solo dispositivo a fin de simplificar la gestión y la configuración.

### **Mejores practicas para gestion de redes**

Diseñar una red jerárquica que incluya módulos que puedan añadirse, actualizarse y modificarse, según sea necesario, sin afectar el diseño de las demás áreas funcionales de la red. Por ejemplo, crear una capa de acceso separada que pueda ampliarse sin afectar a la distribución y las capas básicas de la red del campus.

Crear una estrategia de direcciones IPv4 e IPv6 que sea jerárquica. Una cuidadosa planificación de las direcciones elimina la necesidad de volver a direccionar la red para dar soporte a usuarios y servicios adicionales.

Elegir routers o switches multi-capas para limitar las transmisiones y filtrar otro tráfico no deseado de la red. Utilizar dispositivos de Capa 3 para filtrar y reducir el tráfico al núcleo de la red.

Podemos lograr todo esto con una buena planificación y gestión de redes.

La gestión de redes son sistemas pueden gestionar dispositivos de red como conmutadores, routers, puntos de acceso y controladores inalámbricos desde una ubicación centralizada o a distancia.

Los administradores de la red o las MSP pueden supervisar las operaciones de la red accediendo a este servidor, lo que les proporciona un gran control sin tener que acudir a las instalaciones.Una buena gestión nos puede permitir:

- **Clara visibilidad de la red**: El profesional de TI debe obtener una imagen clara de todos los dispositivos conectados en la red, observar el flujo de datos e identificar y remediar rápidamente los problemas que reducen el rendimiento de la red y pueden provocar fallos.
- **Uso más eficiente de los recursos de las TI**: podemos implementar herramientas que reducen la cantidad de trabajo manual necesario. Esto reduce los costes de mano de obra y libera a los técnicos para que puedan dedicarse a proyectos más importantes o a otras tareas.
- **Necesidades futuras de infraestructura**: Los sistemas de monitorización de red muestran cómo han funcionado los componentes de la red durante un periodo de tiempo, lo que nos permite conocer el futuro. Estos informes pueden ser analizados para ayudar a anticipar cuándo la organización puede necesitar considerar la actualización o la implementación de una nueva infraestructura de TI.
- **Mayor protección contra las amenazas a la seguridad**: La monitorización de la red establece una línea de base del rendimiento de una red. Esto facilita la detección de cambios inusuales en el comportamiento de la red, como aumentos inexplicables en los niveles de tráfico de la red. Cuando el departamento de TI puede identificar rápidamente los posibles problemas de ciberseguridad, a menudo puede intervenir antes de que la amenaza sea costosa.

<aside>
💡 **Ejercicio:**
Con los cuadros dados anteriormente elabora una lista de los equipos de configuración de red que tengas en casa o en tu oficina. Esto podría ayudarte a hacer una análisis si el rendimiento de tu red esta optimo o hay algún problema que esté afectando

</aside>

### 💡QUIZ

1. ¿Qué función principal cumple un firewall en una red de computadoras?
a) Administrar el ancho de banda de la red. ✅
b) Proteger la red al filtrar el tráfico no autorizado.
c) Proporcionar direcciones IP a los dispositivos de la red.
d) Optimizar la topología de la red.

1. ¿Cuántas capas conforman el Modelo OSI (Modelo de Interconexión de Sistemas Abiertos)?
a) 4
b) 5
c) 6
d) 7 ✅

1. ¿Cuál de los siguientes dispositivos de red opera en la capa 2 (capa de enlace de datos) del Modelo OSI y se utiliza para interconectar segmentos de red en la misma subred?
a) Enrutador (router)
b) Concentrador (hub)
c) Conmutador (switch) ✅
d) Firewall
2. ¿Cuál de las siguientes topologías de red utiliza un nodo central para conectar todos los dispositivos de la red, formando una estructura de estrella?
a) Topología de bus
b) Topología de anillo
c) Topología de malla
d) Topología de estrella ✅
3. ¿Qué representa la sigla "DMZ" en el contexto de seguridad de redes?
a) Zona de Acceso Directo
b) Zona de Mantenimiento de Datos
c) Zona Desmilitarizada ✅
d) Zona de Máxima Zonificación