---
title: "Amenazas, vulnerabilidades y procedimientos de seguridad en redes"
subtitle: "Seguridad en Redes: Amenazas, Vulnerabilidades y Estrategias para Defensa. Aprende a Combatir Ataques DoS, DDoS, MITM y más"
technologies: ["redes", "ciberseguridad"]
authors: ["blindma1den", "lorenagubaira"]

---

En los últimos diez o quince años, hemos ido viendo cómo cambiaba el paradigma por el cual los **crackers o cibercriminales** buscaban explotar todas las vulnerabilidades posibles, dentro de cualquier organización o infraestructura nacional. Con el claro fin de contrarrestar este hecho, lo que debemos tener claro todos y cada uno de nosotros, es que debemos cambiar nuestra perspectiva hacia la forma en la que vemos la seguridad en el ámbito informático y de red, debemos conocer ciertos ataques y comprender qué podemos aprender de los mismos, para estar preparados lo mejor posible para ellos, y en ocasiones hasta poder evitarlos. En este mundo de seguridad no podemos decir que estamos preparados para evitar cualquier ataque.

## Ataque DoS o ataque de denegación de servicio

Un **ataque de denegación de servicio**, tiene como **objetivo inhabilitar el uso de un sistema**, una aplicación, un ordenador o un servidor, con el fin de bloquear el servicio para el que está destinado. Este ataque puede afectar, tanto a la fuente que ofrece la información, como puede ser una aplicación o el canal de transmisión, como a la red informática, o, en otras palabras, el cibercriminal intentará evitar que los usuarios accedan a información o a servicios.

El tipo más común es cuando **un atacante «inunda» una red** con una gran cantidad de datos, que hace que se sature la red completa. Por ejemplo, en un ataque DoS hacia una web, cuando escribimos una URL y accedemos, estaremos enviando una solicitud para que nos muestre la información, en este caso, un atacante podría realizar millones de peticiones con el objetivo de colapsar todo el sistema. Por eso, este ataque toma el nombre de «denegación de servicio», ya que no se puede acceder al sitio en cuestión.

Algunos de los problemas que nos encontraremos si nos hacen un ataque DoS, es que notaremos una enorme bajada en el rendimiento de la red y mucha lentitud (abrir archivos o acceder a sitios web). Un sitio web en particular es totalmente inaccesible y no está disponible. Seremos incapaces de entrar en cualquier sitio web al que intentemos acceder. Aumento drástico de la cantidad de spam que recibimos.

## Tipos de ataques DoS

Más allá de saber qué es, hay varios tipos de ataques DoS.

### ICMP Flood Attack

Este tipo de ataque de denegación de servicio permite agotar el ancho de banda de la víctima. Consiste en enviar una gran cantidad de información usando paquetes ICMP Echo Request, es decir, el típico ping, pero modificado para que sea más grande de lo habitual. Además, la víctima podría responderle con paquetes ICMP Echo Reply (respuesta al ping), por lo que tendremos una sobrecarga adicional, tanto en la red como en la víctima. Lo más normal es utilizar uno o varios equipos muy potentes para atacar a una misma víctima, de esta forma, la víctima no podrá gestionar correctamente el tráfico generado.

### Ping of the Dead

Este ataque es similar al anterior, consiste en enviar un paquete de más de 65536 bytes, haciendo que el sistema operativo no sepa cómo manejar este paquete tan grande, haciendo que el sistema operativo se bloquee al intentar ensamblarlo nuevamente. Hoy en día este ataque no funciona, porque el sistema operativo va a descartar los paquetes directamente. Es muy importante conocer este ataque para evitarlo en el futuro, pero ya decimos que este ataque ya no funciona porque los sistemas operativos incorporan una gran cantidad de protecciones para evitarlo.

### Tear Drop Attack

Este tipo de ataque consiste en enviar una serie de paquetes muy grandes, con el objetivo de que el destino (la víctima) no sea capaz de ensamblar esos paquetes, saturando el sistema operativo y bloqueándose. Es posible que una vez que el ataque pare, necesite que sea reiniciado para que pueda volver a funcionar correctamente. Hoy en día los kernel de los sistemas operativos incorporan protecciones frente a estos ataques.

### Jolt Dos Attack

Este tipo de ataque consiste en fragmentar un paquete ICMP, con el objetivo que la víctima no pueda volver a reensamblarlo. Esto hace que el uso de CPU en la víctima aumente, y tenga cuello de botella importante. El resultado de este ataque suele ser que el PC de la víctima se vuelve muy lenta, debido a que la CPU está muy ocupada intentando reensamblar el paquete.

### Land Attack

Este tipo de ataque consiste en enviar un paquete TCP SYN falso, donde la dirección IP del objetivo se utiliza tanto como origen y destino, con el objetivo de que cuando reciba el paquete, se confunda y no sepa dónde enviar el paquete, y bloquearse. Este tipo de ataques normalmente es reconocido por los sistemas operativos, firewalls e incluso suites de antivirus.

### Smurf Attack

Este ataque consiste en enviar una gran cantidad de mensajes ICMP Echo request a la dirección IP de broadcast con la IP de origen de la víctima. De esta forma, la víctima real recibirá todas las respuestas ICMP Echo Reply de toda la red, haciendo que se sature. Antes de realizar este ataque, se debe hacer IP Spoofing para falsificar la dirección IP de origen del ICMP Echo Request, para posteriormente realizar este ataque masivo. La red dejará de funcionar con normalidad mientras se realiza el ataque, porque tendremos un alto tráfico de broadcast. Hoy en día los switches están preparados para evitar estos ataques automáticamente, en función de los PPS (Paquetes por segundo).

### SYN Flood

Este tipo de ataque es uno de los más utilizados en todo el mundo, consiste en enviar paquetes TCP con el flag SYN activado, con el objetivo de enviar cientos o miles de paquetes a un servidor y abrirle diferentes conexiones, con el objetivo de saturarle por completo. Normalmente se utiliza este ataque con una IP de origen falsa, para que todas las respuestas vayan a una IP que no existe, o a una IP víctima que también se verá saturado por todas las respuestas TCP que se envían del servidor.

> 👉 Los ataques SYN Flood se pueden evitar fácilmente con el firewall, limitando el número de paquetes TCP SYN que se pueden recibir, e incluso poniendo un proxy intermedio para añadir una verificación adicional, antes de pasarle los mensajes al servidor web o cualquier otro servicio que haga uso del protocolo TCP.

### Fraggle Dos Attack

Este ataque consiste en enviar mucho tráfico UDP a una dirección IP de broadcast, estos paquetes tienen la IP de origen de la víctima, lógicamente se ha realizado un IP Spoofing para realizar este ataque. La red entregará el tráfico de red a todos los hosts, porque estamos enviando paquetes UDP a la dirección de broadcast, y los equipos responderán. Esto ocasionará que la víctima reciba una gran cantidad de tráfico que no sea capaz de gestionar de manera adecuada, y será incapaz de trabajar con normalidad.

## Ataque denegación de servicio distribuido DDos

Este ataque de red consiste en colapsar a una víctima desde múltiples equipos de origen, por ejemplo, una botnet formada por mil ordenadores podrían atacar a un determinado objetivo. Este tipo de ataques son muy habituales, haciendo uso de las técnicas que hemos explicado anteriormente, como el SYN Flood. Aunque haya un servidor muy potente capaz de gestionar millones de solicitudes SYN Flood, si hacemos uso de una botnet con cientos o miles de ordenadores, no podrá aguantarlo y se terminará bloqueando. Este ataque de «distribuye» entre diferentes equipos, ya sean ordenadores, otros servidores infectados, dispositivos IoT hackeados y mucho más.

Algunos consejos para mitigar los ataques DDoS, son los siguientes:

- Configurar el firewall correctamente del router.
- Bloquear todo el tráfico de red, excepto lo que tengamos permitido específicamente.
- Deshabilitar cualquier servicio que no estemos usando.
- Comprobar a menudo la configuración de la red, y los registros (logs) que tengamos.
- Política de logging robusta, permitiendo correlacionar eventos (SIEM).
- Tener una buena política de contraseñas con sus correspondientes permisos.
- Limitar el ancho de banda en la red por puerto, para evitar ataques desde nuestra propia red.

### Ataque HTTP Request Smuggling

Un **ataque HTTP Request Smuggling** podemos definirlo como aquel que, aprovechando las discrepancias en el análisis, cuando uno o más dispositivos/entidades HTTP se encuentran en el flujo de datos entre el usuario y el servidor web. Nos encontramos con una técnica que interfiere con la forma en que un sitio web procesa las secuencias de solicitudes HTTP que se reciben de uno o más usuarios. Estas vulnerabilidades son a menudo de naturaleza crítica, lo que permite al ciberdelincuente eludir los controles de seguridad, obtener acceso no autorizado a datos privados e incluso comprometer directamente a otros usuarios de la aplicación. Este tráfico ilegal de solicitudes HTTP va a permitir realizar varios ataques como el envenenamiento de caché, el secuestro de sesión y además, se puede obtener la capacidad de eludir la protección del cortafuegos de las aplicaciones web.

Este ataque HTTP Request Smuggling puede afectar a diferentes equipos y servicios: el servidor web, el firewall o el servidor proxy. En cuanto al origen, se remonta al año 2005 en el que este ataque fue demostrado por un grupo de investigadores de Watchfire, entre los que están Klein, Ronen Heled, Chaim Linhart y Steve Orrin. No obstante, en los últimos años se han ido realizando una serie de mejoras que expanden la superficie de ataque y que permiten obtener el máximo acceso de privilegio a las API internas y envenenar cachés.

### Cómo se produce un HTTP Request Smuggling

Actualmente las aplicaciones web emplean con frecuencia cadenas de **servidores HTTP** entre los usuarios y la lógica de aplicación definitiva. De este modo, los usuarios mandan solicitudes a un servidor de aplicaciones para el usuario, y luego éste envía las peticiones a uno o más servidores de servicios de fondo. Hay que señalar que esta arquitectura cada vez es más frecuente y en algunos casos inevitable como en las aplicaciones basadas en la nube.

En el momento en que un servidor de aplicaciones para el usuario reenvía solicitudes HTTP a un servidor de servicios de fondo, habitualmente manda varias peticiones a través de la misma conexión de red de servicios de fondo. Esto se hace así porque es más eficiente y proporciona un mayor rendimiento. La forma de actuación es sencilla, primero las peticiones HTTP se mandan una tras otra. Luego, el servidor receptor analiza los encabezados de cada una de las solicitudes HTTP para precisar dónde acaba una petición y cuándo comienza la siguiente.

Un aspecto muy importante es que los **sistemas front-end y back-end** deben estar **de acuerdo sobre los límites de las solicitudes**. Esto es relevante porque, en caso contrario, un ciberdelincuente podría mandar una petición ambigua a los sistemas front-end y back-end y que lo pudieran entender de manera distinta.

Aquí, el atacante hace que parte de su solicitud de front-end sea interpretada por el servidor de back-end como el inicio de la siguiente solicitud. Lo que sucede entonces, es que se antepone a la siguiente petición, lo cual provoca una interferencia con la manera en que la aplicación procesa esa solicitud. Nos encontraríamos un ataque de HTTP Request Smuggling y puede tener resultados desastrosos para el propietario de ese servidor.

### Por qué se producen estos ataques HTTP Request Smuggling

Una gran parte de las vulnerabilidades HTTP Request Smuggling se producen porque la especificación HTTP proporciona dos formas diferentes de especificar dónde termina una solicitud. Un encabezado es simple, especifica la longitud del cuerpo del mensaje en bytes. Éste se puede utilizar para indicar que el cuerpo del mensaje usa codificación fragmentada. Esto quiere decir que el cuerpo de ese mensaje contiene uno o más fragmentos de datos. Algunos administradores de seguridad desconocen que la codificación fragmentada se puede utilizar en solicitudes HTTP y esto supone un problema.

Por si no lo sabías, HTTP proporciona dos métodos diferentes para determinar la longitud de los mensajes HTTP. También hay que señalar que es posible que un solo mensaje utilice ambos métodos a la vez, en cuyo caso entrarían en conflicto entre sí. El protocolo HTTP intenta solventar este problema indicando que si ambos encabezados Content-Length y Transfer-Encoding están presentes, entonces el encabezado Content-Length es el que no debe utilizarse. Esta fórmula puede ser suficiente para evitar la ambigüedad cuando solo tenemos un servidor activo, pero no cuando tenemos dos o más servidores encadenados.

Por lo tanto, si los servidores front-end y back-end se comportan de manera diferente en relación con **un encabezado del tipo Transfer-Encoding** que esté posiblemente ofuscado, entonces pueden estar en desacuerdo sobre los límites entre las solicitudes sucesivas. Esto nos llevaría a que se pudieran producir vulnerabilidades y un ataque HTTP Request Smuggling.

### Cómo prevenir un HTTP Request Smuggling

Los ataques HTTP Request Smuggling implican colocar tanto el encabezado Content-Length como el encabezado Transfer-Encoding en la misma petición HTTP, y después manipularlos para que los servidores front-end y back-end procesen la solicitud de manera diferente.

Klein, al que ya hemos mencionado antes, pide la normalización de las solicitudes HTTP salientes de los servidores proxy y destaca la necesidad de una solución de firewall de aplicación web robusta y de código abierto que sea capaz de manejar este tipo de ataques. Para solucionar este problema, Klein ha publicado un proyecto basado en C++ que nos va a garantizar que todas las solicitudes HTTP entrantes sean completamente válidas, compatibles y sin ambigüedades. Este trabajo está publicado en GitHub y podéis consultarlo [aquí](https://github.com/SafeBreach-Labs/RSFW).

Por otra parte, algunas otras cosas que podríamos hacer para evitar un ataque de HTTP Request Smuggling serían estas:

- Deshabilitar la reutilización de las conexiones de back-end, de modo que cada solicitud de back-end se mande a través de una conexión de red separada.
- Utilizar HTTP/2 para las conexiones de back-end, ya que este protocolo evita la ambigüedad en los límites entre las peticiones.
- Hay que usar el mismo software de servidor web exacto e idéntico para los servidores front-end y back-end. Así se garantiza que estén de acuerdo en los límites entre las solicitudes.

Tal y como habéis visto, el ataque HTTP Request Smuggling es muy importante debido a su gravedad, es bastante peligroso, sin embargo, tenemos diferentes maneras de prevenir este ataque y mitigarlo correctamente.

## Ataque Man-In-The-Middle

Los ataques Man in the Middle es un tipo de ataque que permite posteriormente realizar otros. Los ataques MITM consisten en colocarse entre la comunicación de dos o más equipos por el atacante, con el objetivo de leer, modificar al vuelo e incluso denegar el paso del tráfico desde un origen hacia un destino. Este tipo de ataques permiten conocer toda la navegación en línea y cualquier comunicación que se vaya a realizar, además, se podría dirigir toda la información hacia otro equipo existente.

Un ejemplo de ataque MITM, sería cuando un cibercriminal intercepta una comunicación entre dos personas, o entre nosotros y un servidor web, y el cibercriminal puede interceptar y capturar toda la información sensible que nosotros enviamos al sitio.

### ¿Cómo prevenir ataques Man-In-The-Middle?

Los ataques MITM no son imposibles de evitar, gracias a la tecnología de «Infraestructura de Clave Pública» podremos proteger los diferentes equipos de ataques, y es que esto nos permitiría autenticarnos frente a otros usuarios de forma segura, acreditando nuestra identidad y comprobando la identidad del destinatario con criptografía pública, además, podremos firmar digitalmente la información, garantizar la propiedad de no repudio, e incluso enviar información totalmente cifrada para conservar la confidencialidad.

En una operación criptográfica que use Infraestructura de Clave Pública, intervienen conceptualmente como mínimo las siguientes partes:

- Un usuario iniciador de la operación.
- Unos sistemas servidores que dan fe de la operación, y garantizan la validez de los certificados, la Autoridad de Certificación (CA), Autoridad de Registro y Sistema de Sellado de Tiempo.
- Un destinatario de los datos cifrados que están firmados, garantizados por parte del usuario iniciador de la operación.

Las operaciones criptográficas de clave pública, son procesos en los que se utilizan unos algoritmos de cifrado asimétrico que son conocidos y están accesibles para todos, como RSA o basados en curvas elípticas. Por este motivo, la seguridad que puede aportar la tecnología PKI, está fuertemente ligada a la privacidad de la llamada clave privada.

## Ataques de ingeniería social

Aunque los ataques de ingeniería social no son un ataque a las redes de datos, es un tipo de ataque muy popular y utilizado por los cibercriminales. Este tipo de ataques consisten en manipular a una persona para que proporcione credenciales de usuario, información privada y más. Los cibercriminales siempre buscan todas las formas posibles para hacerse con credenciales de usuario, número de tarjetas de crédito, cuentas bancarias etc, para conseguir esto, intentarán mentir a las víctimas haciéndose pasar por otras personas.

Este tipo de ataques tienen mucho éxito porque se ataca al eslabón más débil de la ciberseguridad: el ser humano. Es más fácil intentar conseguir las credenciales de usuario de una persona a través de ingeniería social, que intentar atacar un servicio como Google para extraer las contraseñas. Es fundamental en quién confiar, cuándo hacerlo y también cuándo no debemos hacerlo. No importa lo segura que sea nuestra red, si confiamos nuestra seguridad a quién no debemos, toda esa seguridad no valdrá de nada.

### ¿Cómo prevenir ataques de ingeniería social?

La primera recomendación es no tener prisa por responder a los ciberatacantes, muchos de estos ataques siempre se transmiten con cierta urgencia, por ejemplo, que es necesario urgentemente realizar una transferencia de dinero a un destinatario que nunca antes habíamos tenido. Es necesario que sospeches de cualquier mensaje extraño o no solicitado, si el correo que nos llega es de un sitio web o empresa que solemos utilizar, debemos emprender una pequeña investigación por nuestra parte, que recaiga incluso en ponernos en contacto con dicha compañía para verificar la información.

- Cuidado con las solicitudes de información bancaria
- No proporcionar nunca contraseñas de acceso, ni siquiera a entidades bancarias.
- Rechazar cualquier tipo de ayuda de terceras personas, es posible que sean cibercriminales para robar información o dinero.
- No pinchar en enlaces por email, podrían ser phishing, evitar descargar cualquier documento sospechoso.
- Establecer filtros anti spam, configurar nuestro equipo con antivirus y firewalls, revisar los filtros de email y mantener todo actualizado.

## OS Finger Printing

El término OS Finger Printing se refiere a cualquier método para determinar el sistema operativo utilizado en la víctima, con el objetivo de vulnerarlo. Normalmente este tipo de ataques se realizan en la fase de pentesting, este reconocimiento del sistema operativo se realiza al analizar indicadores de protocolos, tiempo que tarda en responder a una solicitud en concreto, y otros valores. Nmap es uno de los programas más utilizados a la hora de realizar el OS Finger Printing. ¿Para qué le servirá a un atacante saber el sistema operativo de la víctima? Para realizar ataques más dirigidos a ese sistema operativo, conocer las vulnerabilidades y explotarlas, y mucho más.

Existen dos tipos diferentes de OS Finger Printing:

- **Activo**: se consigue enviando paquetes especialmente modificados y creados para el equipo objetivo, y mirando en detalle la respuesta y analizando la información recopilada. Nmap realiza este tipo de ataques para obtener toda la información posible.
- **Pasivo**: en este caso se analiza la información recibida, sin enviar paquetes específicamente diseñados al equipo objetivo.

## Escaneo de puertos

En cualquier pentesting, el escaneo de puertos es lo primero que se realiza para intentar vulnerar a un objetivo. Es una de las técnicas de reconocimiento más utilizada por los cibercriminales para descubrir servicios expuestos con los puertos abiertos, si se está usando un firewall e incluso qué sistema operativo está usando la víctima. Todos los equipos que están conectados en la red local o en Internet, hacen uso de una gran cantidad de servicios que escuchan en determinados puertos TCP y UDP. Estos escaneos de puertos permiten saber cuáles están abiertos, e incluso qué servicio hay detrás de ellos, con el objetivo de explotar una vulnerabilidad a dicho servicio.

En los escaneos de puertos, enviaremos mensajes a cada puerto, uno por uno, dependiendo del tipo de respuesta recibida, el puerto estará abierto, filtrado o cerrado. Uno de los programas más usados para escaneo de puertos es Nmap, es la navaja suiza del escaneo de puertos porque también disponemos de Nmap NSE que permite usar scripts para explotar vulnerabilidades conocidas, o para atacar a servidores Samba, FTP, SSH etc.

Conocer los puertos que tenemos abiertos es también algo muy importante, porque un puerto identifica a un servicio que hay corriendo en el sistema. Por ejemplo, el protocolo FTP usa el puerto 21, si está abierto podría deberse a que tenemos un servidor FTP escuchando, y podríamos atacarlo. El escaneo de puertos es la primera fase de un pentesting.

### ¿Cómo prevenir el escaneo de puertos?

El escaneo de puertos no podemos evitarlo, porque no podemos evitar que un ciberdelincuente o cibercriminal intente ver qué puertos tenemos abiertos, pero lo que sí está en nuestras manos es proteger todos los puertos con un firewall bien configurado de forma restrictiva. Debemos tener en cuenta que realizar un escaneo de puertos es ilegal, según se han declarado en varios juzgados, porque es el primer paso de la intrusión o para explotar una vulnerabilidad.

Para limitar la información que vamos a proporcionar a un atacante en un escaneo de puertos, debemos hacer lo siguiente:

- Cerrar todos los puertos en el firewall, excepto los que tengan que estar abiertos para el buen funcionamiento del sistema.
- Utilizar una política del firewall restrictiva, solamente se abre lo que se vaya a utilizar.
- Cerrar servicios del sistema operativo que no sean necesarios.
- Configurar los servicios web, SSH, FTP de tal forma que no proporcionen información como el número de versión, para evitar la explotación de posibles vulnerabilidades.
- Usar TCP Wrappers, un encapsulador de TCP que darán al administrador mayor flexibilidad para permitir o denegar el acceso a determinados servicios.
- Hacer uso de programas como fail2ban para bloquear direcciones IP que realicen ataques.
- Usar IDS/IPS como Snort o Suricata, para que bloqueen las IPs de los atacantes.

## Otros ataques

Además, hay otros muchos ataques que puedes sufrir y que deberías conocer.

### ARP Spoofing

Este ataque a las redes de datos es uno de los más populares, permite atacar a equipos que estén en la misma red local, ya sea cableada o inalámbrica. Cuando se realiza un ataque ARP Spoofing, lo que estamos haciendo es que el atacante se pueda hacer pasar por el router o gateway, y que todo el tráfico de la red o desde un determinado PC (víctima) pase por él, permitiendo leer, modificar e incluso bloquear el tráfico de red.

Este ataque solamente funciona en redes IPv4, pero en redes IPv6 también existe un ataque similar, porque el protocolo ARP tan solo está disponible en redes IPv4. Este ataque es lo más fácil para poder realizar un Man in the Middle y capturar toda la información a la víctima. Para detectar estos ataques, se podría usar Reverse ARP, un protocolo que sirve para consultar las IP asociadas a una MAC, si tenemos más de una IP significa que estamos ante un ataque. Algunas suites de seguridad ya detectan este tipo de ataques, e incluso los switches gestionables permiten evitar este tipo de ataques haciendo IP-MAC Binding.

### Ataque de inundación MAC

Este es uno de los ataques más típicos en las redes de datos, consiste en inundar de direcciones MAC una red donde tengamos un switch, cada uno con diferentes direcciones MAC de origen, con el objetivo de llevar la tabla CAM de los switches y que el switch pase a funcionar como un hub. No obstante, hoy en día todos los switches disponen de protecciones frente a este ataque, haciendo que se puedan eliminar las direcciones MAC rápidamente, y que no llegue a colapsarse nunca, pero la CPU del switch estará al 100% y notaremos lentitud en la red.

En el caso de switches gestionables con VLANs, el desbordamiento solamente estaría en la VLAN afectada, no afectando al resto de VLANs de la red. Para prevenir este tipo de ataques, es recomendable configurar el Port Security en los switches, y limitar a un cierto número de direcciones MAC por puerto, de esta forma, el puerto se podría apagar automáticamente, o directamente restringir el alta de nuevas MAC hasta nueva orden.

### Envenenamiento de caché DNS

Este tipo de ataque consiste en proporcionar datos falsos vía DNS; para que una víctima obtenga esa información y visite páginas web falsas o bajo nuestro control. El equipo que haga solicitudes DNS podría recibir direcciones IP falsificadas en base a su solicitud DNS, de esta forma podremos redirigir a una víctima hacia cualquier web bajo nuestro control.

### IP Spoofing

Este ataque consiste en suplantar la dirección IP de origen de un determinado equipo, de esta forma, se podrían enviar paquetes TCP, UDP o IP con una IP de origen falsa, suplantando la dirección IP real de un dispositivo. Esto tiene varios objetivos, ocultar la identidad real del origen, o hacerse pasar por otro equipo para que todas las respuestas vayan a él directamente.

### ACK Flood

Este ataque consiste en enviar un paquete de tipo TCP ACK a un determinado objetivo, normalmente se realiza con una IP falsificada, por tanto, el IP spoofing será necesario. Es similar a ataques TCP SYN, pero si el firewall está bloqueando paquetes TCP SYN, esta es una alternativa para bloquear a la víctima.

### TCP Session Hijacking

Este ataque consiste en tomar posesión de una sesión TCP que ya existe, donde la víctima la está utilizando. Para que este ataque tenga éxito es necesario realizarse en un momento exacto, en el inicio de las conexiones TCP es donde se realiza la autenticación, es justo en ese punto cuando el cibercriminal ejecutará el ataque.

### ICMP Tunneling

Este tipo de ataques se utiliza principalmente para evadir los firewalls, porque normalmente los cortafuegos no bloquean los paquetes ICMP. También podrían usarse para establecer un canal de comunicación cifrado y difícil de rastrear. Un túnel ICMP lo que hace es establecer una conexión encubierta entre dos equipos, esto mismo también se puede usar con UDP haciendo uso de DNS.

Para prevenir los túneles ICMP, es necesario inspeccionar el tráfico ICMP en detalle, y ver qué tipo de mensajes se intercambian. Además, esto se complica si se utiliza cifrado de datos, pero podremos detectarlo porque será tráfico ICMP que no es «normal», por tanto, saltarán todas las alertas de los IDS/IPS si los configuramos correctamente.

### Ataque LOKI

Esto no es un ataque a las redes de datos, es un programa cliente/servidor que permite exfiltrar información a través de protocolos que normalmente no contienen carga útil, por ejemplo, se podría tunelizar tráfico SSH dentro del protocolo ICMP con ping e incluso con UDP para DNS. Esto se puede utilizar como puerta trasera en sistemas Linux para extraer información y enviarla remotamente sin levantar sospechas. Esto es algo que también deberíamos controlar a través de los firewalls.

Una de sus versiones, LOKI II, es uno de los primeros ejemplos de canal encubierto. Se trata de medios de comunicación que utilizan medios no convencionales para poder realizar las transferencias de información entre diferentes procesos. Pero también entre sistemas e incluso redes. De forma que eluden las políticas de seguridad más comunes. Estos suelen ser utilizados para realizar la extracción de datos de sistemas comprometidos. O para recibir comandos de un atacante, y hacer lo que él le indique.

A pesar de que este fue un sistema muy innovador, las técnicas más actuales de detección de intrusos y demás soluciones de seguridad han avanzado mucho. Por lo cual este tipo de canales encubiertos, ahora son bien conocidos y generalmente, son detectados por las soluciones de seguridad más modernas. En cambio, el concepto de LOKI y otros canales encubiertos sigue siendo muy relevante. Los atacantes buscan y utilizan métodos, que les ayuden a evadir la detección y transferir datos de una forma sigilosa.

### Ataque de secuencia TCP

Este tipo de ataque consiste en intentar predecir el número de secuencia de un tráfico TCP, con el objetivo de identificar los paquetes de una conexión TCP, y secuestrar la sesión. El típico ejemplo es un escenario donde un atacante está monitorizando el flujo de datos entre dos equipos, el atacante podría cortar la comunicación con el equipo real, y establecerse él como el equipo real, todo ello prediciendo el número de secuencia del siguiente paquete de TCP. El atacante «eliminaría» al equipo real, haciendo uso de un ataque de denegación de servicio (DoS) o similar.

Gracias a esta predicción del número de secuencia, el paquete podrá llegar a su destino antes que cualquier información del host legítimo, porque este último está bajo un ataque DoS y no permitirá la comunicación al host víctima. Este paquete del atacante se podría usar para obtener acceso al sistema, terminar una conexión por la fuerza, o directamente enviar una carga maliciosa.

> 💡 **¿Cómo prevenir el ataque de secuencia TCP?** La IETF en 2012 lanzó un nuevo estándar para establecer un algoritmo mejorado, y evitar que un atacante pueda adivinar el número de secuencia inicial en las comunicaciones TCP. Este estándar está diseñado para aumentar la robustez de las comunicaciones TCP frente al análisis predictivo y monitorización de los atacantes. Actualmente todos los sistemas operativos hacen uso de este nuevo estándar para evitar este ataque, por tanto, un atacante no podrá predecir los números de secuencia, pero los atacantes en ciertas circunstancias todavía puedan adivinarlos, aunque es mucho más difícil que antes.

### Ataques de redireccionamiento ICMP

Este ataque de red llamado ICMP Redirect, permite redirigir a un host de origen que use otra puerta de enlace diferente para que pueda estar más cerca del destino. Lógicamente, un atacante se pondrá a sí mismo como puerta de enlace, con el objetivo de que todo el tráfico pase por él para capturarlo, modificarlo o bloquearlo. Estos mensajes se envían a los diferentes hosts, pero hoy en día este tipo de ataques ICMP Redirect en sistemas Linux no están afectados, porque internamente lo tienen desactivado, pero es posible que en otros sistemas operativo sí se vean afectados.

Algunos de los ataques más conocidos, que utilizan el redireccionamiento ICMP son:

- Ataques Man-in-the-Middle
- Denegación de servicio
- Redireccionamiento de tráfico a sitios maliciosos

Algunas de las formas para poder estar un poco más protegidos frente a estos son:

- Deshabilitar el redireccionamiento ICMP
- Filtrar los mensajes ICMP
- Detección de intrusiones
- Uso de redes privadas VPN.

### Ataque de transferencia de zona DNS

Este ataque afecta a los servidores DNS, consiste en que el servidor DNS devuelve una lista de nombre de host y direcciones IP en el dominio, estas transferencias de zona normalmente se realizan entre servidores DNS autoritativos, pero este ataque podría hacer que los ciberdelincuentes consulten los servidores DNS para tener un listado de host a los que atacar. En cambio, estos ataques cuentan con riesgos asociados a los ataques de transferencia de zona. Algunos de estos riesgos son:

- Reconocimiento detallado de la estructura de la red, facilitando la planificación de otros ataques.
- Envenenamiento DNS con la información obtenida. Lo cual ya resulta más sencillo para el atacante.
- Ataques dirigidos a lugares concretos, ya que conocen los servidores y servicios específicos.

Las formas más comunes para poder mitigar y prevenir este tipo de problemas son las restricciones de acceso, y utilizar listas de control. Pero también es importante mantener la red monitorizada y en alerta, sin olvidarnos de las actualizaciones de seguridad y el uso de funciones como el DNSSEC.

## El peligro de un web Shell

Es un script malicioso que se introduce en los sistemas que son atacados. En la mayoría de los casos, los servidores web forman parte del objetivo. Una vez que dichos sistemas cuentan con el web shell, el cibercriminal puede tener control remoto del mismo. En consecuencia, tendrá acceso persistente al sistema y podrá manejarlo como quiera. Esto significa que los web shells tienen la capacidad de crear ***backdoors*** en los sistemas vulnerados para tener cierto control e incluso el control total.

Además, los web shells tienen un alcance mucho mayor. También pueden vulnerar a interfaces de gestión de dispositivos en red. Por lo que es sumamente importante tener buenas prácticas de gestión segura en redes. Sobre todo, si se trata de aquellas que cuentan con cientos y miles de dispositivos conectados a diario.

El auge del teletrabajo trae consigo riesgos de seguridad, que, si bien son ya conocidos, estos merecen especial atención, debido a que, evidentemente, no es lo mismo trabajar en un entorno de red «seguro» de una empresa, que desde casa. Sin embargo, podrías preguntarte si no es suficiente utilizar servicios de **VPN** para que podamos conectarnos con total seguridad a nuestros recursos de la organización, esa es tan sólo una parte de lo que un administrador de red debe hacer.

### Usos habituales

Una de las ventajas que tienen los ataques web shell es que son polivalentes y difíciles de detectar. Además, son peligrosos y los podrían usar para:

- El robo de datos.
- La infección de los visitantes de una web.
- El lanzamiento de ataques DDoS
- La modificación de archivos con intenciones dañinas.
- Para su utilización como un bot que forma parte de una botnet.

### Cómo funciona

Este tipo de ataques se divide en varias etapas. En primer lugar, el atacante procede a crear un mecanismo persistente en el servidor, el cual le permite generar un acceso remoto. Luego tratará de asignarse los privilegios necesarios dentro del mismo, de así poder dar uso de puertas traseras u otros métodos para realizar el ataque o utilizar los recursos disponibles, tanto del propio atacante como del servidor, para realizar actividades ilícitas. Una vez que tienen los privilegios para poder llegar a la raíz, pueden hacer muchos cambios a su antojo. Como cambiar permisos, instalar software, eliminar contenido o usuarios, robar contraseñas, etc.

Los ataques primero tienen que buscar los servidores, los cuales son vulnerables a ataques shell mediante programas de escaneo. Y una vez descubren la vulnerabilidad que les interesa, lanzan el ataque de forma inmediata, y siempre antes que el error que encontraron para su beneficio, sea parcheado.

El script le proporcionará al atacante la puerta trasera necesaria, de forma que ya podrán acceder de forma remota al servidor. Y en muchas ocasiones, es el propio hacker, quién se encarga de parchear dicha vulnerabilidad, para evitar que puedan introducir otros webshell a través de ella, y también con el fin de no ser detectados. Incluso pueden asignar factores de autenticación como contraseñas, para que solo pueda entrar un atacante específico.

### Detección de un web shell

Actualmente, detectar este tipo de ataques resulta una tarea compleja, ya que toda acción que debemos realizar, tiene que ser dentro del propio servidor donde web shell está situado. Vamos a ver algunos métodos para poder detectarlos, pero seguramente el más eficaz es prohibir algunas funciones que puedan estar afectadas y realizar una auditoría al servidor y la página web.

Este tipo de auditorías, pueden detectar **la existencia de un web shell**, de la misma forma que evitar que los atacantes puedan explotar las vulnerabilidades y suban algún otro shell.

La principal dificultad que se presenta a la hora de **detectar** **este** **tipo** **de malware** es que los atacantes pueden aplicar métodos de cifrado para cubrir su actividad maliciosa. Esto es consecuencia directa de la facilidad en que se pueden introducir los scripts. Como sabemos, para los ciberataques hay posibilidades infinitas y el escudo de protección de las redes debe reforzarse cada vez más. Algunos de los métodos de detección eficaz son los siguientes:

- Comparar una versión de la aplicación web distinta a la que se encuentra en producción. Esto último se refiere a la aplicación que está disponible para los usuarios. Esta comparación servirá para analizar las diferencias ante cualquier señal de actividad inusual.
- Buscar anomalías en el tráfico de la aplicación web mediante herramientas de monitorización.
- Aplicar detección basada en firmas, es decir, verificar todas las web shells que hayan sido modificadas. Aunque estas hayan sufrido una modificación mínima.
- Buscar flujos de tráfico en la red que tengas características inusuales.

> 👉 ¿Qué herramientas y qué procedimientos debo aplicar para el proceso de detección de estos scripts maliciosos? A continuación, compartimos recomendaciones fundamentales para protegerte eficazmente.

## Cómo proteger tus sistemas y redes

Estos web shells también se introducen directamente a los **sistemas** **y redes** que son víctimas, esto se da principalmente porque las aplicaciones web (en su mayoría) y su infraestructura vulnerable tienen permisos para realizar modificaciones de forma directa a un directorio web accesible, o bien, a piezas de código web. Sin embargo, este tipo de permisos no debería concederse.

En consecuencia, los propios sistemas abren la puerta sin inconveniente alguno a los cibercriminales para llevar a cabo los ataques. Por lo que se recomienda bloquear los permisos de modificación. Ahora bien, si es que no existe esa posibilidad, se cuenta con una alternativa.

**Los ataques shell web** pueden permitir a los actores de amenazas ejecutar comandos de forma remota en un servidor y pueden causar graves perjuicios a las organizaciones. Una cosa a tener en cuenta es que el malware basado en scripts eventualmente se canaliza en algunos puntos como *cmd.exe*, *powershell.exe* y *cscript.exe*.

En ese sentido **la prevención es fundamental** y Microsoft nos recomienda seguir una serie de pautas:

- Hay que identificar y corregir vulnerabilidades o configuraciones incorrectas en aplicaciones web y servidores web.
- Debemos implementar la segmentación adecuada de su red perimetral. El objetivo es que un servidor web comprometido de nuestra organización no ponga en riesgo al resto.
- Tenemos que habilitar la protección antivirus en los servidores web. Además, debemos **activar la protección proporcionada en la nube** para obtener las últimas defensas contra las nuevas amenazas.
- En cuanto a los usuarios sólo deben poder cargar archivos en directorios que puedan ser escaneados por un antivirus. Por otra parte también deben estar configurados para no permitir la ejecución o secuencias de comandos del lado del servidor.
- Hay que auditar y revisar los registros de los servidores web con frecuencia. Tenemos que conocer que sistemas exponemos directamente a Internet.
- Debemos utilizar el Firewall de Windows Defender, los dispositivos de prevención de intrusiones y su firewall de red para evitar la comunicación del servidor de comando y control entre los puntos finales siempre que sea factible.
- Tenemos que verificar el firewall perimetral y el proxy para restringir el acceso innecesario a los servicios.
- Necesitamos una buena política de cuentas y de credenciales. Aquí es importante limitar el uso de las cuentas de administrador local o de dominio a las estrictamente necesarias.

### Sistemas IDS/IPS y firewall de aplicaciones web

Esta alternativa consiste en poner en marcha un esquema de **monitoreo de integridad** de los archivos que están alojados en la infraestructura de las aplicaciones. De esta manera, los administradores contarán con la visibilidad necesaria ante cualquier eventualidad de cambios que puedan ocurrir en los directorios web y las piezas de código.

Por otro lado, un **firewall** especial para aplicaciones web. La misma está orientada a aquellas aplicaciones basadas en HTTP. Aplica una serie de reglas cuando se da una **conversación HTTP**. Un beneficio adicional y muy destacable es que estas reglas propias de estos firewalls también pueden proteger de otros ataques más letales como el Cross-Site Scripting y las inyecciones SQL, entre otros. De acuerdo a la organización **[OWASP](https://owasp.org/)**, este tipo de firewall está orientado a la protección a servidores. Así como los proxies protegen a los hosts (a los usuarios). De hecho, los **Firewalls de Aplicaciones Web** también se lo considera como un tipo de **proxy reverso**.

### Recursos de la NSA

Esta reconocida agencia de los EEUU ha puesto a disposición un completo repositorio en **[Github](https://github.com/nsacyber/Mitigating-Web-Shells#endpoint-detection-and-response-edr-capabilities)**. En este repositorio podemos encontrar un amplio listado de métodos y herramientas que ayudarán a que tu sistema esté protegido del malware de tipo web shell. Un punto interesante es que no será necesario realizar mayores inversiones en cuanto a soluciones de seguridad se refiere.

Ponemos como ejemplo a **PowerShell** de Microsoft. En el repositorio que hemos compartido, encontrarás soporte para realizar detección de web shells mediante un esquema de comparación «Known Good». Además, podrás realizar detección de solicitudes sospechosas en los logs de los servidores web.

Como vemos, es importante estar al tanto de las principales vulnerabilidades que se presentan no sólo a los servidores de aplicaciones web, sino también aquellos que están ligados a aplicaciones tradicionales e incluso, las propias redes de datos. En cuanto a ciberataques, hay posibilidades infinitas y el escudo de protección debe ser lo más robusto posible. Por fortuna, los recursos en línea y las herramientas sumamente accesibles nos pueden ayudar como administradores a prevenir más de una tragedia.

Sin duda, se trata de una buena forma de **bloquear amenazas de este tipo** que incluyen entre otros:

- Secuencias de comandos para la comparación de archivos conocidos buenos con WinDiff, PowerShell y Linux Diff.
- Detección de solicitudes anómalas en los registros del servidor web con consultas de Splunk para registros del servidor web, Script de PowerShell para registros de Microsoft IIS y Script de Python para registros httpd de Apache
- Reglas YARA para detectar shells web comunes
- Reglas HIPS para permitir que el sistema de seguridad basado en host de McAfee bloquee directorios web.

