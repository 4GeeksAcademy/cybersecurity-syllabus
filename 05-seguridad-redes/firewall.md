Firewalls

# **Firewall**

La seguridad en cada equipo individual sigue siendo esencial pero no se puede considerar de forma aislada. Hay que considerar:

- El número de equipos en muchas organizaciones.
- Entornos heterogéneos con distintos sistemas operativos y versiones de cada sistema operativo
- usuarios con privilegios de administración pueden ser un problema a la hora de organizarlos.

Un cortafuego es una herramienta que protege una red de sistemas y dispositivos interconectados mediante el control del tráfico de red. El cortafuego debe tener tres características clave:

- Todo el tráfico de “dentro a fuera” y de “fuera a dentro” debe pasar por él.
- Solo el tráfico autorizado basado en la política de seguridad puede continuar.
- Debe ser completamente inatacable.

Aunque ningún cortafuego actual cumple estos requisitos completamente, todos intentan acercarse a ellos lo más posible.

![Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image7.png](Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image7.png)

Para proteger las redes, se puede optar por colocar uno o varios cortafuegos.

**Ventajas**:

- capacidad para ser utilizados como un punto esencial de aplicación de la política de seguridad.
- son capaces de soportar técnicas avanzadas de autenticación de manera más eficaz y económica que si se hiciera equipo por equipo.
- pueden centralizar alarmas y registros de tráfico
- Tienen menos configuración en comparación con un sistema de propósito general
- Necesitan pocos usuarios definidos para llevar a cabo su configuración y mantenimiento.

La política del tráfico en un cortafuego es **restrictiva y solo permite el tráfico que ha sido explícitamente permitido**. Esta política es segura, pero cada utilidad que necesite tráfico debe ser analizada y permitida de manera individual.

**Desventajas:**

- pueden provocar una falsa sensación de seguridad para los usuarios y administradores.
- Si son muy sofisticados, pueden requerir una configuración compleja.
- Pueden representar un cuello de botella para el tráfico de red.

T**ipos:**

- filtros de paquetes.
- *Gateways* de aplicaciones.
- *stateful inspection*. (el *Firewall-1* de *Checkpoint* o el *CiscoASA* (*Adaptative Security Appliance*), además de su tecnología particular, pueden configurarse como servidores *proxy*.)
- híbridos.

**Arquitecturas de cortafuegos**: son distintas formas de combinar cortafuegos

**Filtros de paquetes**

Los filtros de paquetes operan en **el nivel de red y transporte** y filtran paquetes IP basándose en valores de algunos campos de las cabeceras de IP, TCP o UDP. también permiten filtrar el tráfico en función del enlace de red del que provenga. El más básico consiste en un encaminador que trabaja a nivel de red, aunque en muchos casos, una máquina con software dedicado realiza esta tarea.

**Cada filtro está compuesto por reglas** que se utilizarán de distintas y orden en busca de una coincidencia. Un filtro de paquetes examina cada paquete entrante por la interfaz en la que está aplicado el filtro y:

1. Obtiene los contenidos de las cabeceras citadas del paquete.
2. Contrasta los valores contra los configurados en las reglas del filtro, ordenadamente.
3. Si cumple lo enunciado en una regla, aplica una de las dos únicas condiciones posibles: lo permite, en cuyo caso el paquete se encaminará a su destino o lo descarta.

**Campos de la cabecera**

Los **campos de las cabeceras que se usan como criterios de filtrado** son:

- Las direcciones IP origen y destino del mensaje, que viajan en la cabecera de IP.
- Los números de puerto origen y destino del mensaje, que son parte de la cabecera de TCP o de UDP.
- El tipo de protocolo o número de protocolo, parte de la cabecera de IP, que indica, el tipo de mensaje IP: si es ICMP, OSPF, TCP, UDP, etc.
- Una serie de opciones de la cabecera TCP, como los bits de sincronización, de final, de ACK, etc.

<aside>
📖 Para ser efectivo, un filtro debe permitir la especificación de puertos, ya que algunos servidores de aplicaciones IP utilizan números de puerto normalizados, mientras que los clientes utilizan números de puerto al azar por encima de 1023. Es necesario contar con operadores relacionales para implementar relaciones como “mayor que” o “igual a” y los filtros deben permitir el filtrado de paquetes según la interfaz de origen o destino. Pueden ser un software con funcionalidades avanzadas como IPTables o ser parte de un encaminador. La tecnología es simple y transparente para los usuarios.

</aside>

![Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image8.jpeg](Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image8.jpeg)

**Puntos débiles**:

- Si la configuración llega a hacerse muy grande, puede hacerse difícil el mantenimiento de los filtros.
- Si se tiene que hacer una excepción ocasional, puede ser que haya que cambiar toda la configuración, haciendo la situación bastante insegura.
- No permiten realizar ningún control a nivel de usuario ni a nivel de datos. No se puede filtrar por valores de campos de las cabeceras de aplicación.
- No es fácil filtrar protocolos con más de una conexión activa simultáneamente, como ftp, ni protocolos basados en RPC.
- No suelen guardar registro de los accesos de los usuarios.

Aplicaciones difíciles de filtrar son aquellas basadas en el entorno RPC (*Remote Procedure Call*), para las que cada servidor RPC tiene asociado un número de puerto que no es siempre el mismo. Aplicaciones como NFS (Network File System) o NIS (Network Information Services), envían mensajes al *portmapper* con el número de puerto 111 para conocer el número de puerto actual del servidor que están buscando. Estas aplicaciones están compuestas por varios servidores que se registran con el *portmapper* al iniciar, lo que las hace difíciles de filtrar. no se debe permitir el tráfico de estas aplicaciones si el cortafuego es solo un filtro de paquetes. Las **reglas de filtrado** se expresan como una tabla de condiciones y acciones que se consultan en orden hasta encontrar una regla para decidir si se permite o se bloquea un paquete.

Es importante el orden de análisis de las reglas para implementar correctamente la política de seguridad. Cuanto más complejas sean las reglas y su orden de análisis, más difícil será para el administrador gestionarlas. ¿Y si un paquete que no cumple ninguna regla especificada? Se debe añadir una regla por defecto al final de la lista que bloquee todo el tráfico que no cumpla con ninguna otra regla.

![Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image9.jpeg](Introduccio%CC%81n%20a%20la%20seguridad%20en%20redes%20b1630986b9024ea68d1f35b789d008f7/image9.jpeg)