# Lectura 2 📕: Modelos de referencia de redes

Los modelos de referencia de redes son marcos teóricos que se utilizan para describir y entender cómo funcionan las redes de comunicación y cómo se organizan los diferentes componentes que las componen. Estos modelos establecen una estructura conceptual que ayuda a los profesionales de redes y a los diseñadores a comprender mejor los procesos de comunicación y a desarrollar estándares y protocolos de manera coherente. Dos de los modelos de referencia más conocidos son el Modelo OSI (Open Systems Interconnection) y el Modelo TCP/IP (Transmission Control Protocol/Internet Protocol):

### **Modelo OSI (Open Systems Interconnection):**

El Modelo OSI fue desarrollado por la Organización Internacional de Normalización (ISO) en la década de 1980 y consta de siete capas, cada una con un conjunto específico de funciones. Estas capas, de la más baja a la más alta, son las siguientes:

- Capa 1: Física
- Capa 2: Enlace de Datos
- Capa 3: Red
- Capa 4: Transporte
- Capa 5: Sesión
- Capa 6: Presentación
- Capa 7: Aplicación

El Modelo OSI (Open Systems Interconnection) es un marco conceptual que se utiliza para comprender cómo funcionan las redes de computadoras y cómo se comunican los dispositivos en una red. Este modelo divide la comunicación en siete capas, cada una de las cuales realiza funciones específicas. Veamos cómo funciona cada capa:

**Capa 7: Capa de Aplicación**

- Esta es la capa en la que interactúan las aplicaciones y los usuarios finales. Proporciona servicios de red a las aplicaciones, como la transferencia de archivos, el correo electrónico y la navegación web.
- Ejemplo: Un navegador web como Chrome o Firefox.

**Capa 6: Capa de Presentación**

- Esta capa se encarga de la representación y el cifrado de datos. Convierte los datos en un formato que puede ser entendido por la capa de aplicación.
- Ejemplo: La compresión de datos al enviar un archivo ZIP.

**Capa 5: Capa de Sesión**

- La capa de sesión establece, mantiene y termina conexiones de sesión entre dos dispositivos. Administra diálogos y controla la comunicación.
- Ejemplo: Iniciar una sesión de chat en línea.

**Capa 4: Capa de Transporte**

- La capa de transporte se ocupa de la transferencia de datos de extremo a extremo y asegura que los datos se entreguen de manera confiable y en orden. Controla la segmentación, el control de flujo y la recuperación de errores.
- Ejemplo: TCP (Protocolo de Control de Transmisión) que garantiza la entrega confiable de datos.

**Capa 3: Capa de Red**

- La capa de red se encarga de la dirección y el enrutamiento de datos a través de la red. Define cómo los datos se transmiten entre redes y cómo se determina la ruta más eficiente.
- Ejemplo: El protocolo IP (Protocolo de Internet) que asigna direcciones IP a dispositivos y enruta paquetes de datos a través de Internet.

**Capa 2: Capa de Enlace de Datos**

- Esta capa maneja la comunicación entre dispositivos en la misma red local (LAN) y se encarga de la detección y corrección de errores. Organiza los datos en tramas.
- Ejemplo: El estándar Ethernet que controla la comunicación en una red cableada.

**Capa 1: Capa Física**

- La capa física se refiere a la transmisión y recepción física de datos a través de medios como cables o ondas electromagnéticas. Define las especificaciones eléctricas, mecánicas y funcionales de los dispositivos de red.
- Ejemplo: Los cables Ethernet, las señales eléctricas en un cable coaxial o las señales de radio en una red inalámbrica.

> 📖 En resumen, el Modelo OSI divide el proceso de comunicación en siete capas, cada una con funciones específicas. A medida que los datos se transmiten desde la capa de aplicación en un dispositivo de origen hasta la capa física y luego se reciben en un dispositivo de destino, cada capa agrega su propio conjunto de funciones y encabezados para permitir la comunicación entre dispositivos en una red. Esta estructura facilita la comprensión y la solución de problemas en las redes de computadoras.

Cada capa se comunica con las capas adyacentes mediante interfaces bien definidas y proporciona servicios a las capas superiores. El Modelo OSI es una referencia teórica ampliamente aceptada que ayuda a comprender cómo funcionan los protocolos de red y cómo se organizan en una pila de protocolos.

### **Modelo TCP/IP (Transmission Control Protocol/Internet Protocol):**

El Modelo TCP/IP es un modelo de referencia práctico que se basa en el diseño de Internet y se utiliza para describir cómo se comunican los dispositivos en Internet. Aunque es menos detallado que el Modelo OSI, consta de cuatro capas principales:

- Capa de Acceso a la Red
- Capa de Internet
- Capa de Transporte
- Capa de Aplicación

> 📖 El Modelo TCP/IP se utiliza ampliamente en la configuración y administración de redes, ya que se ajusta más directamente a la arquitectura de Internet y es más sencillo de implementar y entender.

El Modelo TCP/IP (Transmission Control Protocol/Internet Protocol) es un modelo conceptual que describe cómo funcionan las redes de Internet y se divide en cuatro capas principales. Aquí te explico cada capa del Modelo TCP/IP junto con ejemplos simples:

**1. Capa de Acceso a la Red (Link Layer):**

- Esta capa se encarga de la transmisión de datos en la red física y la interconexión de dispositivos dentro de una red local (LAN).
- Ejemplo: Ethernet y Wi-Fi son protocolos comunes de la capa de acceso a la red. Cuando envías un correo electrónico desde tu computadora a otra en la misma red Wi-Fi, esta capa se encarga de la transmisión de los datos entre las dos máquinas.

**2. Capa de Internet (Internet Layer):**

- La capa de Internet se encarga de enrutar los datos entre redes diferentes y de manera global. Utiliza direcciones IP para identificar dispositivos y routers en la red.
- Ejemplo: Cuando ingresas una URL en tu navegador, como "**[www.ejemplo.com](http://www.ejemplo.com/)**", la capa de Internet resuelve la dirección IP asociada a ese nombre de dominio y dirige las solicitudes a través de la red global hasta llegar al servidor web correcto.

**3. Capa de Transporte:**

- Esta capa es responsable de la comunicación extremo a extremo, garantizando que los datos se transmitan de manera confiable y en orden.
- Ejemplo: El Protocolo de Control de Transmisión (TCP) es un protocolo de la capa de transporte que se utiliza para la transferencia de datos confiable. Cuando descargas un archivo grande desde un servidor web, TCP asegura que todos los paquetes se reciban correctamente y en el orden correcto.

**4. Capa de Aplicación:**

- La capa de aplicación es donde las aplicaciones y servicios interactúan directamente con los datos. Aquí se encuentran los protocolos y aplicaciones utilizados por los usuarios finales.
- Ejemplo: El Protocolo de Transferencia de Hipertexto (HTTP) es un protocolo de la capa de aplicación utilizado para acceder a páginas web. Cuando navegas por un sitio web, tu navegador utiliza HTTP para solicitar y recibir las páginas y los recursos del servidor web.

Es importante destacar que el Modelo TCP/IP es un modelo práctico que se adapta a la arquitectura de Internet y se centra en la funcionalidad de las capas sin dividir estrictamente en siete capas como el Modelo OSI. En la práctica, estas cuatro capas son suficientes para comprender cómo funcionan las redes de Internet y cómo se comunican los dispositivos y aplicaciones a través de ella. Cada capa desempeña un papel importante en la transferencia de datos a través de la red global.

> 💡 La importancia de estos modelos radica en que proporcionan un lenguaje común y una estructura organizativa para la comunicación de red. Ayudan a los ingenieros de redes y a los profesionales de TI a comprender mejor cómo interactúan los protocolos y los dispositivos en una red, a solucionar problemas de red y a diseñar redes eficientes y seguras.

### ⚡️QUIZ

1. Esta capa del modelo TCP/IP  es responsable de la comunicación extremo a extremo 

A. Internet

B. Física

C. Transporte ✅

2. ¿Qué ocurre en la capa física del modelo OSI?

A. Se decide la topología de red 

B. Se establece conexión a internet

C. Comienzan las comunicaciones a través de los sistemas de cableado ✅

3. Es la capa del modelo TCP/IP y OSI donde las aplicaciones y servicios interactúan directamente con los datos.

A. Aplicación ✅

B. Enlace de datos

C. Física 
