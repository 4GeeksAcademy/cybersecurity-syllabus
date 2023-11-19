# Fundamentos de la seguridad de la información

## Triada de la seguridad

Hoy en día la información se encuentra en todos lados, esta información puede correr peligro de ser intervenida o alterada por otra persona. Existen principios que son diseñados para poder proteger nuestros datos e información. Una de las principales es el triángulo de la seguridad.

También conocida como **CIA** por sus siglas en inglés (Confidencialidad, Integridad, Disponibilidad), forma la base de cualquier estrategia de ciberseguridad efectiva.

La base de la tríada de seguridad es que toda la información debe ser confidencial, íntegra, y disponible en el momento que sea requerida.

![Triada de la seguridad](../assets/triada-de-la-seguridad.png)

Profundizando en estos conceptos, es posible entender mejor las implicaciones y los métodos involucrados en su implementación. Así que veamos de que se tratan a continuanción:

- **Confidencialidad**

La confidencialidad se refiere a la protección de la información contra el acceso no autorizado. El objetivo es garantizar que solo las personas autorizadas tengan acceso a la información confidencial. 

Algunos ejemplos de medidas que garantizan la confidencialidad incluyen:

| Cifrado de datos | Utilizar algoritmos de cifrado para proteger los datos sensibles, de modo que solo puedan ser leídos por las personas que tienen la clave de descifrado adecuada. |
| --- | --- |
| Control de acceso | Implementar mecanismos como contraseñas, autenticación de dos factores y listas de control de acceso para limitar quién puede acceder a la información confidencial. |
| Políticas de seguridad | Establecer políticas y procedimientos claros sobre cómo se debe manejar y compartir la información confidencial dentro de una organización. |

- **Integridad**

La integridad se refiere a la protección de la precisión y la integridad de la información. Implica asegurarse de que los datos no sean alterados de manera no autorizada, garantizando su exactitud y confiabilidad.

Algunos ejemplos de medidas que garantizan la integridad incluyen:

| Firmas digitales | Utilizar firmas digitales para verificar la integridad de los datos y asegurar que no hayan sido modificados durante el tránsito o el almacenamiento. |
| --- | --- |
| Registros de auditoría | Mantener registros de auditoría detallados que rastreen los cambios y las actividades relacionadas con la información, lo que facilita la detección de alteraciones no autorizadas. |
| Copias de seguridad | Realizar copias de seguridad regulares de la información para garantizar que, en caso de daño o alteración, se pueda restaurar una versión válida y confiable. |

- **Disponibilidad**

La disponibilidad se refiere a asegurar que la información esté disponible y accesible cuando sea necesario. Esto implica garantizar que los sistemas y los datos estén disponibles y funcionando correctamente para los usuarios autorizados.

Algunos ejemplos de medidas que garantizan la disponibilidad incluyen:

| Planes de continuidad del negocio | Desarrollar planes y procedimientos para garantizar la disponibilidad de los sistemas y la información en caso de interrupciones, como desastres naturales o fallas del sistema. |
| --- | --- |
| Redundancia y respaldo | Establecer sistemas redundantes y realizar copias de seguridad para garantizar la disponibilidad de los datos en caso de fallas o pérdidas. |
| Mantenimiento y actualización | Realizar un mantenimiento regular de los sistemas y asegurarse de que los parches y actualizaciones de seguridad estén al día para evitar interrupciones debido a vulnerabilidades conocidas. |
| Monitoreo de la red | El monitoreo regular de la red puede ayudar a identificar y solucionar los problemas antes de que afecten a la disponibilidad de los datos. |

## Amenazas

Las amenazas son todo lo que atenta contra la seguridad de la información de las personas. Los usuarios están expuestos a las amenazas cuando navegan por internet, usan servicios, hacen compras u otras actividades por medio de internet.

### Malware

El malware es cualquier tipo de software creado para hacer daño o vulnerar la seguridad de otra pieza de **software** o **hardware**. Malware, contracción de «software malicioso», es un término colectivo utilizado para describir virus, ransomware, spyware, troyanos y cualquier otro tipo de código o software creados con intenciones maliciosas.

El concepto de malware radica en una intención maliciosa. La importancia del malware se basa en el daño que es capaz de infligir en un equipo, un sistema informático, un servidor o la red. Es el cómo y el por qué que separan un tipo de malware del siguiente.

![Triada de la seguridad](../assets/malware.png)

El mundo del malware es diverso, pero muchos tipos de malware comparten señales de advertencia similares. Algunos síntomas de una infección de malware en un dispositivo son:

1. **Disminuciones repentinas del rendimiento**: el malware puede ocupar mucha potencia de procesamiento del dispositivo, dando lugar a graves ralentizaciones.
2. **Bloqueos y cierres del sistema frecuentes**: algunos tipos de malware provocarán cierres del sistema o bloqueos del equipo, mientras que otros provocarán bloqueos consumiendo demasiada RAM o elevando la temperatura de la CPU. Un uso elevado y sostenido de la CPU puede ser un signo de malware.
3. **Archivos eliminados o dañados**: el malware a menudo elimina o daña archivos como parte de su plan para causar tanto caos como sea posible.
4. **Una gran cantidad de anuncios emergentes**: la función del adware es enviarle correo basura con ventanas emergentes. Otros tipos de malware también pueden causar anuncios y alertas emergentes.
5. **Aplicaciones desconocidas**: el malware puede instalar aplicaciones adicionales en el dispositivo. Si ve nuevos programas que no instaló, podría ser el resultado de un ataque de malware.

Determinadas cepas de malware son más fáciles de detectar que otras. El **ransomware** y el **adware** son normalmente visibles de inmediato, mientras que el **spyware** permanece oculto. El único modo seguro de detectar todo el malware antes de que infecte su dispositivo es con una herramienta antivirus específica.

## Ingeniería social

La ingeniería social es la práctica ilegítima de obtener información confidencial a través de la manipulación de usuarios legítimos. Es un conjunto de técnicas que pueden usar ciertas personas para obtener información, acceso o permisos en sistemas de información que les permitan realizar daños a la persona u organismo comprometidos y es utilizado en diversas formas de estafas y suplantación de identidad. El principio que sustenta la ingeniería social es el de que, en cualquier sistema, los usuarios son el eslabón débil.

En la práctica, un ingeniero social usará comúnmente el teléfono o Internet para engañar a la gente, fingiendo ser, por ejemplo, un empleado de algún banco o alguna otra empresa, un compañero de trabajo, un técnico o un cliente. Vía Internet se usa, adicionalmente, el envío de solicitudes de renovación de permisos de acceso a páginas web o correos electrónicos falsos que solicitan respuestas e incluso las famosas cadenas, llevando así a revelar sus credenciales de acceso o información sensible, confidencial o crítica.

### Ataques de phishing

Los ataques de phishing se pueden clasificar según el objetivo contra el que se dirige el ataque, el fin, el medio que se utiliza o según el modo de operación. Un caso concreto puede pertenecer a varios tipos a la vez.  Actualmente se han contado más de 10 000 formas de phishing. Los tipos de ataques de phising más frecuentes son:

- **Phishing general**: Phishing tradicional, Bulk Phishing o Spray and pray. Consiste en la emisión masiva de correos electrónicos a usuarios. Estos correos suplantan a entidades de confianza (ejemplo bancos) y persiguen el engaño del usuario y la consecución de información. Por ejemplo, en el mensaje se incluyen enlaces a dominios maliciosos. Para camuflar estos enlaces es habitual que el texto del enlace sea la URL correcta, pero el enlace en sí apunte al sitio malicioso.
- **Vishing:** Es similar al phishing tradicional pero el engaño se produce a través de una llamada telefónica. El término deriva de la unión de dos palabras en inglés: ‘'voice'’ y ‘'phishing’'. Un ejemplo típico de uso de esta técnica es cuando un ciberdelincuente ha robado ya información confidencial a través de un ataque de phising, pero necesita la clave SMS o token digital para realizar y validar una operación. Es en ese momento el ciberdelincuente llama por teléfono al cliente identificándose como personal del banco y, con mensajes particularmente alarmistas, intenta de que el cliente revele el número de su clave SMS o token digital, que son los necesarios para autorizar la transacción.
- **Qrishing:** phishing a través de códigos QR el cual consiste en la manipulación de códigos QR y el posterior engaño a las víctimas mediante la suplantación de la página web o aplicación a la que se accede al escanear el código el cual dirige al usuario a un link fraudulento utilizado con la finalidad de obtener información privada de las víctimas.
- **Smishing:** Es similar al phishing tradicional pero el engaño se produce a través mensajes de texto ya sean por SMS o mensajería instantánea (como WhatsApp). Un ejemplo típico de esta técnica es cuando el cliente recibe un mensaje de texto, donde el emisor se hace pasar por el banco, y le informan que se ha realizado una compra sospechosa con su tarjeta de crédito. A su vez, el texto solicita que se comunique con la banca por teléfono de la entidad financiera y le brinda un número falso. El cliente devuelve la llamada y es ahí cuando el ciberdelincuente, haciéndose pasar por el banco, solicita información confidencial para supuestamente cancelar la compra. En una variante de esta modalidad el mensaje también podría incluir un enlace a una ‘web’ fraudulenta para solicitar información sensible.

### Ataques de fuerza bruta

Un ataque de fuerza bruta es un método de prueba y error utilizado para decodificar datos confidenciales. Las aplicaciones más comunes para los ataques de fuerza bruta son descifrar contraseñas y descifrar claves de cifrado (sigue leyendo para obtener más información sobre las claves de cifrado). Otros destinos comunes para los ataques de fuerza bruta son las claves **API** y los inicios de sesión de **SSH**. Los ataques de contraseña de fuerza bruta a menudo se llevan a cabo mediante scripts o bots que tienen como destino la página de inicio de sesión de un sitio web.

Lo que distingue los ataques de fuerza bruta de otros métodos de decodificación es que los ataques de fuerza bruta no emplean una estrategia intelectual; simplemente intentan usar diferentes combinaciones de caracteres hasta encontrar la combinación correcta. Esto se asemeja a un ladrón que intenta abrir una caja fuerte combinada al probar todas las combinaciones posibles de números hasta que se abre la caja fuerte.

Entre los tipos comunes de ataques de fuerza bruta encontramos:

- **Ataques de fuerza bruta sencillos:** En esta forma de ataque se utilizan combinaciones de contraseñas estándar o números de identificación personal. Los ataques sencillos suelen tener éxito, ya que son muchos los usuarios que no utilizan un administrador de contraseñas y siguen usando contraseñas fáciles con palabras comunes que se pueden adivinar fácilmente.
- **Ataques de diccionario:** Los atacantes comienzan con un nombre de usuario individual y prueban posibles contraseñas extraídas de diccionarios, pero modificando las palabras con caracteres especiales y números.
- **Ataques de fuerza bruta híbridos:** En este caso se utiliza lógica externa para determinar las variaciones de contraseñas y las posibles combinaciones con las que es más probable conseguir el objetivo previsto y, a continuación, se prueban todas las variaciones posibles.

## ****Seguridad de Contraseñas y Autenticación****

### **Contraseñas seguras**

Conocida también como password, una contraseña es una palabra, frase o señal que solo conoce determinada o determinadas personas y les permite reconocerse entre sí o acceder a un sitio que antes era inaccesible. Hoy en día, una contraseña sirve como método de autenticación para acceder a un recurso o sitio o grupo controlado.

Una contraseña segura es una palabra o frase caracterizada por su dificultad de adivinar o descifrar por algún programa automático. Puede contener números, mayúsculas, caracteres especiales o mejor aún, tratarse de alguna contraseña **alfanumérica**.

Las contraseñas más difíciles de vencer por los hackers y los delincuentes cibernéticos son aquellas que tienen más de doce caracteres, tienen números, letras y símbolos y no guardan relación alguna entre los datos de los usuarios que las generan.

### **Autenticación**

Autenticación es el proceso que debe seguir un usuario para tener acceso a los recursos de un sistema o de una red de computadoras. Este proceso implica identificación (decirle al sistema quién es) y autenticación (demostrar que el usuario es quien dice ser). La autenticación por sí sola no verifica derechos de acceso del usuario; estos se confirman en el proceso de autorización.

En general, la seguridad de las redes de datos requiere para conceder acceso a los servicios de la red, tres procesos: **autenticación**, **autorización** y **registro**.

1. Autenticación: el proceso por el cual el usuario se identifica en forma inequívoca; es decir, sin duda o equivocación de que es quien dice ser.
2. Autorización: el proceso por el cual la red de datos autoriza al usuario identificado a acceder a determinados recursos de la misma.
3. Registro: el proceso mediante el cual la red registra todos y cada uno de los accesos a los recursos que realiza el usuario, autorizado o no.

Estos tres procesos se conocen por las siglas en inglés como AAA, Authentication, Authorization, and Accounting.

**Tipos de autenticación**

Se puede efectuar autenticación usando uno o varios de los siguientes métodos:

- Autenticación por conocimientos - basada en información que sólo conoce el usuario.
- Autenticación por pertenencia -  basada en algo que posee el usuario.
- Autenticación por características-  basada en alguna característica física del usuario.

La autorización es una parte del sistema operativo que protege los recursos del sistema permitiendo que sólo sean usados por aquellos consumidores a los que se les ha concedido autorización para ello. Los recursos incluyen archivos y otros objetos de datos, programas, dispositivos y funcionalidades provistas por aplicaciones. Ejemplos de consumidores son usuarios del sistema, programas y otros dispositivos.

El proceso de autorización se usa para decidir si la persona, programa o dispositivo "X" tiene permiso para acceder al dato, funcionalidad o servicio

La Autenticación de **Dos Factores** es una herramienta que ofrecen varios proveedores de servicios en línea, que cumple la función de agregar una capa de seguridad adicional al proceso de inicio de sesión de tus cuentas de Internet. La mecánica es simple: cuando el usuario inicia sesión en su cuenta personal de algún servicio online, esta herramienta le solicita que confirme la titularidad de su cuenta, proporcionando dos factores distintos. El primero de estos, es la contraseña. El segundo, puede ser varias cosas, siempre dependiendo del servicio. En el más común de los casos, suele tratarse de  un código que se envía a un teléfono móvil vía SMS o a una cuenta de email. La esencia fundamental de esta herramienta se reduce a que, si quieres loggearte a una de tus cuentas personales, debes “saber algo” y “poseer algo”. Así, por ejemplo, para acceder a la red virtual privada de una compañía, es posible que necesites de una clave y de una memoria USB.

## Control de acceso

### C**ontrol de acceso físico**

El **control de acceso físico** es un conjunto de políticas para controlar a quién se le concede acceso a un lugar físico. Hay varios ejemplos de control de acceso físico en el mundo real, como los siguientes:

- Porteros de discoteca
- Torniquetes de metro
- Agentes de aduanas en los aeropuertos
- Escáneres de tarjetas de acceso o insignias de identificación en las oficinas corporativas

En todos estos ejemplos, una persona o dispositivo sigue un conjunto de políticas para decidir quién tiene acceso a un lugar físico restringido. Por ejemplo, el escáner de la tarjeta de acceso de un hotel solo permite el acceso a los huéspedes autorizados que cuentan con una llave del hotel.

### **Control de Acceso en Sistemas**

Si hablamos de **sistemas**, el control de acceso a la información restringe el acceso a los datos y al software utilizado para manipularlos. Algunos ejemplos son los siguientes:

- Iniciar sesión en un portátil usando una contraseña
- Desbloquear un teléfono inteligente con una huella dactilar
- Acceder en remoto a la red interna de la empresa con una VPN

****Autenticación y Autorización****

En todos estos casos, el software se utiliza para autenticar y conceder autorización a los usuarios que necesitan acceder a la información digital. Autenticación y autorización son componentes integrales del control de acceso a la información.

La seguridad del usuario se administra mediante privilegios y permisos. Los permisos definen el nivel de acceso que los usuarios y los grupos tienen respecto de un objeto.

Aunque un usuario posea el privilegio para realizar determinadas acciones, puede que el usuario también necesite permiso para realizar la acción en un objeto concreto.

En los sistemas operativos podemos tener permisos en todos nuestros archivos para los usuarios de la red, estos permisos pueden ser para editar, ver o ejecutar los archivos.

Los permisos son un conjunto de reglas y configuraciones que determinan qué acciones pueden realizar los usuarios y grupos sobre los archivos y directorios del sistema. Estos se dividen en diferentes formatos, los cuales hacen que la seguridad de los sistemas aumente y el control sea mayor.

Los sistemas operativos son multiusuario, podemos acceder de forma simultánea con varios usuarios registrados localmente en nuestro sistema operativo, por tanto, es muy importante realizar una revisión periódica de los permisos existentes, y en  algunas ocasiones se debe evitar que otros usuarios del equipo puedan modificar los archivos.

Estos son los distintos tipos de cuentas que podemos conseguir

| Root | Se trata de la cuenta con los privilegios más altos en el sistema operativo. Puede llevar a cabo cualquier función de administración. |
| --- | --- |
| Usuarios normales | Estos tienen pocos permisos, y son sobre los que se aplican todos los que podemos crear para gestionar los accesos. |
| Usuarios de ejecución | Son usuarios que no pueden realizar un login, simplemente se dedican a lanzar procesos, entre otros. |

### Tipos de permisos****:****

- **Lectura (r)**: Es el primer permiso que podemos encontrarnos. Este nos da la opción de que un usuario pueda ver el contenido al que quiere acceder.
- **Escritura (w)**: Nos da la posibilidad de otorgar poder sobre sobre un archivo. De esta forma podrá ser modificado, al igual que un directorio.
- **Ejecución (x)**: Permite a los usuarios ejecutar diferentes parámetros dentro del equipo.
- **Sin permisos (-)**: Nos indica que el usuario no tiene ningún tipo de permiso sobre el recurso de red o contenido compartido.

**Niveles de permisos**

- **Permisos de propietario**: Se trata del usuario que crea el archivo desde su equipo. Linux asigna a este usuario el acceso a la información creada, y la posibilidad de realizar cambios sobre el mismo. Este se identifica con el parámetro «u».
- **Permisos de grupo**: Cuando un usuario pertenece a un grupo dentro del directorio de Linux, quiere decir que se le otorgan los mismos permisos que tienen los demás usuarios que pertenecen a ese mismo grupo. El sistema identifica esto con el parámetro «g».
- **Permisos del resto de usuarios**: En este caso nos referimos a los usuarios que no son los creadores del archivo, ni pertenecen al grupo que hemos indicado anteriormente. Los permisos y accesos de estos usuarios los puede establecer el propietario. El sistema los establece con el parámetro «o».

### ****Gestión de Permisos en Windows y Linux:****

**Para Windows:**

En windows podemos ver los permisos de un archivo a traves del la ventana de propiedades.

Por la consola de comando (cmd) podemos ver los propietarios del archivo con el comando dir /q 

**Para linux:**

Desde la terminal aplicamos el comando `ls -l` ; con este comando podemos ver todos los permisos de archivo por propietario, grupo y usuario.

- Si queremos cambiar permisos del archivo usaremos el comando `chmod` seguido del permiso.
- Si queremos cambiar el propietario del archivo usaremos el comando `chown` seguido del nuevo propietario.

<aside>
👉 Saber que permisos tiene el archivo le permitiria a un atacante saber si puede manipular el archivo para su conveniencia, por lo que es importante cuando se trabaja con varios usuarios mantener el metodo del menor privilegio y asi no permitir que usuarios no autorizados puedan acceder al archivo.

</aside>