# Lectura 6 📕: Criptografía Básica

La criptografía en informática es el campo que se ocupa de desarrollar técnicas y métodos para cifrar y descifrar información con el objetivo de asegurar su confidencialidad, integridad y autenticidad en el entorno digital. La criptografía permite que los datos se transmitan y almacenen de manera segura, incluso si son interceptados por personas no autorizadas.

En términos simples, la criptografía en informática utiliza algoritmos matemáticos para convertir datos legibles en un formato ilegible y luego volver a convertirlos al formato original cuando sea necesario. Los datos originales se llaman "**texto claro**" y los datos cifrados se denominan "**texto cifrado**". Para llevar a cabo el proceso de cifrado y descifrado, se utilizan claves, que son valores secretos utilizados por los algoritmos.

Hay dos tipos principales de criptografía utilizados en informática:

1. **Criptografía de Clave Simétrica:** En este enfoque, una única clave se utiliza tanto para cifrar como para descifrar los datos. Tanto el remitente como el receptor deben conocer y mantener en secreto esta clave. Si un tercero intercepta la clave, podría descifrar los datos. Los algoritmos de cifrado simétrico comunes incluyen DES (Estándar de Cifrado de Datos) y AES (Estándar de Encriptación Avanzada).
2. **Criptografía de Clave Pública:** También conocida como criptografía asimétrica, este enfoque utiliza un par de claves: una clave pública y una clave privada. La clave pública se comparte libremente y se utiliza para cifrar los datos, mientras que la clave privada, que debe mantenerse en secreto, se utiliza para descifrarlos. Además, la clave privada se utiliza para firmar digitalmente documentos para autenticar su origen. Un algoritmo popular en este campo es RSA.

La criptografía en informática es fundamental para asegurar la privacidad y la seguridad de las comunicaciones en línea, las transacciones electrónicas, la autenticación de usuarios y la protección de datos confidenciales. Además, juega un papel crucial en la confianza que los usuarios tienen en la seguridad de sus interacciones digitales diarias, como compras en línea, acceso a cuentas bancarias y el intercambio de información personal.

### Tipos de cifrados

Hay varios tipos de cifrado que se utilizan en el campo de la criptografía para proteger la confidencialidad de la información. Estos tipos de cifrado se pueden clasificar en dos categorías principales: cifrado simétrico y cifrado asimétrico (o de clave pública). Aquí tienes una explicación de ambos:

**1. Cifrado Simétrico:**
En el cifrado simétrico, una sola clave se utiliza tanto para cifrar como para descifrar los datos. Esto significa que tanto el remitente como el receptor deben conocer y mantener en secreto la misma clave. La principal ventaja del cifrado simétrico es que es rápido y eficiente para el cifrado y el descifrado. Sin embargo, el desafío radica en la gestión segura de la clave compartida, ya que cualquier exposición o compromiso de la clave puede poner en riesgo la seguridad de los datos.

Ejemplos de algoritmos de cifrado simétrico:

- **AES (Advanced Encryption Standard):** Un algoritmo ampliamente utilizado y considerado seguro para cifrar datos.
- **DES (Data Encryption Standard):** Un algoritmo anteriormente común, pero ahora considerado inseguro debido a su longitud de clave corta.

**2. Cifrado Asimétrico (Cifrado de Clave Pública):**
El cifrado asimétrico utiliza un par de claves: una **clave pública** y una **clave privada**. La clave pública se comparte libremente y se utiliza para cifrar los datos antes de enviarlos. Sin embargo, solo la clave privada correspondiente al destinatario puede descifrar los datos. Esto resuelve el problema de la gestión de claves compartidas en el cifrado simétrico. Además, las claves privadas también se utilizan para firmar digitalmente documentos para autenticar su origen.

Ejemplos de algoritmos de cifrado asimétrico:

- **RSA (Rivest-Shamir-Adleman):** Un algoritmo ampliamente utilizado para cifrado y firmas digitales en aplicaciones de seguridad.
- **ECC (Elliptic Curve Cryptography):** Un algoritmo de cifrado de clave pública que ofrece una seguridad comparable a RSA pero con claves más cortas, lo que lo hace eficiente en términos de recursos.

En general, tanto el cifrado simétrico como el cifrado asimétrico desempeñan roles importantes en la protección de la información en línea y en la seguridad de las comunicaciones digitales. A menudo, se utilizan en combinación para aprovechar las ventajas de ambos enfoques y garantizar una mayor seguridad en diversos contextos y aplicaciones.

La criptografía se utiliza en una amplia variedad de aplicaciones para proteger la confidencialidad, integridad y autenticidad de la información en el mundo digital. Aquí tienes algunos de los usos más comunes de la criptografía:

| Comunicaciones Seguras | La criptografía se utiliza para cifrar las comunicaciones en línea, como correos electrónicos, mensajes de texto y llamadas telefónicas. Esto garantiza que solo el destinatario autorizado pueda acceder y comprender el contenido del mensaje. |
| --- | --- |
| Transacciones Financieras: | La criptografía se emplea en las transacciones en línea y las operaciones bancarias para proteger la información financiera, como los números de tarjetas de crédito y las contraseñas. Esto evita el robo de datos y el fraude. |
| Autenticación de Usuarios | En la autenticación, la criptografía se utiliza para generar y verificar firmas digitales, contraseñas y certificados digitales. Ayuda a confirmar que los usuarios son quienes dicen ser antes de permitirles acceder a sistemas y datos sensibles. |
| Almacenamiento de Datos Seguro | La información almacenada en dispositivos, como discos duros y unidades USB, puede cifrarse para protegerla en caso de pérdida o robo. Incluso si un dispositivo se pierde, los datos permanecen inaccesibles sin la clave adecuada. |
| Navegación Web Segura | La criptografía se utiliza para habilitar conexiones seguras a través del protocolo HTTPS en sitios web. Esto asegura que los datos transmitidos entre el navegador del usuario y el servidor web estén cifrados y protegidos. |
| Protección de la Privacidad | En aplicaciones que tratan con datos personales, la criptografía ayuda a proteger la privacidad de los usuarios. Esto incluye aplicaciones de mensajería, redes sociales y servicios de almacenamiento en la nube. |
| Firmas Digitales | La criptografía permite la creación de firmas digitales para documentos y transacciones electrónicas. Esto garantiza la autenticidad y la integridad de los documentos, ya que cualquier modificación sería detectable. |
| Seguridad en Redes y Sistemas | La criptografía se utiliza en redes privadas virtuales (VPNs) para crear canales seguros entre dispositivos y encriptar el tráfico. También se emplea para proteger las contraseñas almacenadas en sistemas y para verificar la integridad de los archivos descargados. |
| Protección de Propiedad Intelectual | Los creadores de contenido pueden utilizar la criptografía para proteger sus creaciones digitales, como música, películas y libros electrónicos, y evitar la piratería. |
| Internet de las Cosas (IoT) | La criptografía asegura la comunicación entre dispositivos conectados en IoT, protegiendo los datos y evitando la manipulación no autorizada de dispositivos. |

En resumen, la criptografía es esencial para salvaguardar la seguridad y la privacidad en el mundo digital. A través de una variedad de aplicaciones y usos, la criptografía desempeña un papel fundamental en la protección de información sensible y en el establecimiento de confianza en las comunicaciones y las transacciones en línea.

Hace siglos, en tiempos de la antigua Grecia y Roma, la criptografía ya estaba en uso para proteger mensajes secretos en tiempos de guerra y diplomacia. Uno de los métodos más conocidos es el "Cifrado César", utilizado por Julio César para ocultar mensajes militares. En este método, cada letra del mensaje se reemplazaba por otra que se encontraba un número fijo de posiciones hacia adelante en el alfabeto.

Sin embargo, uno de los momentos más destacados en la historia de la criptografía ocurrió durante la Segunda Guerra Mundial. Los alemanes utilizaron una máquina de cifrado llamada "Enigma" para codificar sus comunicaciones militares, creyendo que eran indescifrables. Pero un equipo de matemáticos y criptógrafos liderado por Alan Turing en Bletchley Park, Reino Unido, logró descifrar la Enigma, un logro crucial que ayudó a los Aliados a obtener información clave y cambiar el curso de la guerra.

![critografia](../assets/criptografia.png)

Después de la guerra, la criptografía continuó evolucionando con el advenimiento de la informática. La criptografía de clave pública, desarrollada en la década de 1970 por Whitfield Diffie y Martin Hellman, permitió el intercambio seguro de claves sin necesidad de compartir secretos previos. Esto allanó el camino para la seguridad en línea, incluida la navegación segura por internet y las transacciones electrónicas.

En los tiempos modernos, la criptografía es esencial para la seguridad en línea, protegiendo datos confidenciales y facilitando la autenticación segura. Desde la encriptación de mensajes hasta la protección de contraseñas y la firma digital, la criptografía sigue siendo una herramienta crucial en la protección de la privacidad y la seguridad en el mundo digital.