### **Nmap:**

> Función: Escaneo de puertos y mapeo de redes.

> Uso: Identificación de servicios en ejecución y posibles puntos de entrada.

No podemos empezar un recopilatorio con los mejores escáneres de vulnerabilidades sin hablar de uno de los más potentes, completos y veteranos que podemos encontrar en la red: [Nmap](https://nmap.org/). Este software es uno de los más usados para buscar hosts dentro de una red local, pero también permite el descubrimiento de hosts en Internet para comprobar si están conectados a la red, además, podremos realizar amplios y avanzados escaneos de puertos para comprobar si tenemos algún servicio funcionando que no esté protegido por el firewall, e incluso podremos ver si tenemos un firewall en un determinado host. Otras opciones que podremos realizar con este programa es saber qué sistema operativo utiliza un host en concreto, si escaneamos un equipo con Windows nos indicará que estamos, efectivamente, escaneando un sistema operativo Windows, y lo mismo con Linux o Unix.

Este programa es de código abierto y multiplataforma, aunque lo más normal es utilizarlo en sistemas operativos Linux para realizar la tarea de pentesting, es el primer paso para realizar una intrusión en los sistemas e intentar hackear el equipo correctamente, siempre con fines éticos para descubrir posibles vulnerabilidades. Este software tiene una gran cantidad de opciones avanzadas, y, además, dispone de una interfaz gráfica de manera opcional llamada Zenmap que podremos utilizar de manera rápida y fácil.

Es una herramienta esencial, ya que permite identificar posibles vulnerabilidades que podrían ser utilizadas como puntos de entrada por atacantes. Con una ejecución de NMAP sobre un objetivo en puntual podríamos observar aquellos dispositivos, servidores, servicios, firewalls y más, relacionados al primero. Para ello, la herramienta envía distintos tipos de paquetes (de tipo ping, echo y dirigidos a puertos) para hacer un sondeo sobre una IP o un rango de las mismas.

![Rango](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/rango.png?raw=true)

Usualmente, esta herramienta es ejecutada vía terminal (aunque existen adaptaciones con interfaz gráfica) con el formato "nmap <Flags> <Objetivo>".

Existen un sinfín de Flags que le indicarán a la ejecución configuraciones particulares. Entre las más utilizadas, encontramos:

> **-sn**, para determinar si un objetivo está disponible.

> - **sT,** para determinar qué puertos están abiertos en un objetivo usando TCP.

> - **O,** para identificar el sistema operativo y la versión del software que se ejecuta en un objetivo.

> - **A,** para el escaneo completo del objetivo.

La ejecución sin parámetros ejecuta un escaneo sencillo a los 1000 puertos más comunes, realizando anteriormente un ping para ver si el equipo está vivo (si el equipo no responde al ping, no se realizará el test de los puertos). La identificación de una vulnerabilidad en un puerto proporciona al atacante un excelente vector de ataque que, con suerte y pericia, puede hacer que la máquina sea comprometida. Es una herramienta muy flexible con multitud de opciones.

Aunque esta herramienta nació como un escáner de puertos, gracias a los **scripts NSE** que incluye por defecto (y que podemos bajar de multitud de páginas web) es posible utilizarla como una completa herramienta para buscar vulnerabilidades en redes y sistemas. Los scripts NSE utilizan la potencia del propio Nmap, pero, además, es capaz de explotar vulnerabilidades conocidas a determinados programas, por lo que es muy útil actualizarla frecuentemente con los últimos scripts. Tanto NSE como Nmap hacen un equipo realmente potente para ayudar al hacker a realizar el pentesting.

Algunas de las funciones que podremos realizar son atacar los servidores Samba probando cientos de usuarios y contraseñas, lo mismo con los servidores de FTP e incluso servidores SSH, y es que podremos atacar una gran cantidad de servicios para explotar vulnerabilidades. Cuando sale una vulnerabilidad pública, los desarrolladores incorporan este exploit en Nmap NSE para explotarla de forma fácil y rápida, con el objetivo de ayudar a los pentesters en la tarea de explotación del sistema comprometido.

## **Motivos para utilizar Nmap**

- Cuenta con capacidad para reconocer de forma rápida todos los dispositivos, incluso servidores, routers, móviles, entre otros. Y lo puede hacer tanto en redes únicas como múltiples. Por lo cual es muy buena opción para el sector empresarial donde se utilizan diferentes redes.
- Nos ayuda a realizar una identificación de los servicios que se ejecutan en el sistema. Los servidores web, DNS y otras aplicaciones serán escaneadas también. Esto hace que se puedan detectar diferentes versiones de las aplicaciones con mucha precisión. Esto ayuda a detectar vulnerabilidades existentes.
- Puede localizar información sobre los sistemas operativos que ejecutan los dispositivos. A su vez proporciona información muy detallada como las versiones de los mismos, lo cual nos ayuda mucho a realizar una planificación de diferentes enfoques durante la penetración de los paquetes.
- En las auditorías de seguridad y el escaneo de vulnerabilidades, Nmap puede atacar sistemas mediante la utilización de scripts existentes en el motor scripting de Nmap.
- Cuenta con una interfaz gráfica llamada Zenmap, que nos ayuda a llevar a cabo mapeos visuales de las redes. Esto es bueno para darle una usabilidad mayor a la herramienta y facilita que los informes se generen de una forma más detallada, intuitiva y accesible.

### **Ventajas de NMAP**

Con Nmap podemos obtener una serie de ventajas, las cuales no solo nos ayudarán a tener más funcionalidades, si no que también nos puede influir en su facilidad de uso. Algunas de ellas pueden ser:

- El sistema operativo determina cuándo Nmap puede escanear los puertos abiertos. Al menos uno de ellos tiene que estar abierto en el sistema cuando se está escaneando.
- Se pueden determinar los puertos abiertos que están a la escucha, pero es posible que a menudo este puerto no identifique al sistema operativo.
- Si se trata de identificar la generación del sistema operativo mediante un sondeo, es posible que se cree una superposición basada en la información determinada a partir de la propia sonda, y esta no se considerará autorizada. Al fin y al cabo, la identificación del sistema operativo está determinada por un algoritmo que realiza un análisis de los puertos abiertos. Muchos elementos pueden hacer que esta identificación sea errónea.

### **Desventajas de NMAP**

Pero como en todo, encontraremos algunos inconvenientes, los cuales nos puede hacer cambiar de opinión sobre si usarlo o no. Como por ejemplo:

- Nmap se puede utilizar como una herramienta para hackers. En todo caso, es posible que la seguridad de los equipos no lo permita.
- Se requiere NCAP e instalar un controlador de filtro para la red. NCAP puede interactuar con otros software, y a su vez causar problemas por excesos operacionales.
- NCAP y NMAP están pensados para ser transparentes, en cambio pueden tener interacciones con software instalado en el entorno. Esto puede ser una preocupación de cualquier administrador, por lo cual se recomienda realizar los testeos oportunos para utilizarlo.
- Los dispositivos escaneados, puede darse el caso de que respondan de forma inesperada, sobre todo si son máquinas muy diferentes a lo habitual, como un equipo médico, por ejemplo.
- Puede ser bloqueado por cortafuegos locales, tanto en el sistema que realiza el análisis como el del sistema al cual analiza. Esto puede limitar los datos disponibles considerablemente.
- Es posible bloquearlo por software como un antivirus, por ejemplo. Esto puede afectar a la profundidad y precisión de todos los datos que proporciona Nmap.
- La metodología de Nmap, trata de ser lo más eficiente posible, pero es posible que no pueda realizar escaneos en determinados puntos de la red local donde está llevando a cabo análisis.

### **Alternativas a NMAP**

NMAP no es la única herramienta que podemos encontrar. En internet hay muchas que pueden hacer la función de forma correcta, incluso algunas con nuevas características. Por ejemplo:

- **FING:** Es una opción orientada a dispositivos móviles. Nos permite realizar un análisis de forma rápida de la red donde estamos conectados. Con facilidades para detectar intrusos y realizar un control sobre la actividad que se lleva a cabo en la red.
- **Angry IP Scanner:** De nuevo nos encontramos ante un programa multiplataforma. Gratuito y con la posibilidad de realizar un análisis de varias interfaces de red. Este resulta muy rápido al escanear los puertos.
- **WinMTR:** En este caso estamos ante un ejemplo que es muy sencillo de utilizar y también gratuito. Pero solo está disponible para Windows, lo cual limita un poco. Esta puede diagnosticar problemas en las conexiones, a la vez que nos da opciones de ping y traceroute. De todos modos, resulta una de las más básicas.
- **Scapy:** Aquí no encontramos un analizador de red. Pero si nos permite manipular paquetes, y actuar como un sniffer. Esto hace que sea posible descifrar paquetes WEB, analizar VLANs y revisar redes VoIP. Resulta una de las más complejas de todo el listado.
- **Fingbox:** Es una buena opción tanto para móviles como para equipos de escritorio. Tiene una versión gratuita, pero la más completa es de pago.