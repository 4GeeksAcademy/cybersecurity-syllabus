---
title: Criptografía Básica
tags:
  - criptografia
  - ciberseguridad
authors:
  - blindma1den
  - lorenagubaira
description: >-
  Descubre cómo la criptografía garantiza la seguridad digital. Aprende sobre
  cifrado simétrico y asimétrico, y su importancia en la ciberseguridad.
---

La **criptografía informática** es el campo que desarrolla técnicas para cifrar y descifrar información digital, con el fin de garantizar su confidencialidad, integridad y autenticidad. Gracias a la criptografía, los datos pueden transmitirse y almacenarse de manera segura, incluso si son interceptados por personas no autorizadas.

En términos simples, la criptografía transforma datos legibles (conocidos como *texto claro*) en un formato ilegible (*texto cifrado*), mediante algoritmos matemáticos y el uso de claves. Estas claves son valores secretos que permiten ejecutar los procesos de cifrado y descifrado.

## Tipos de cifrado

Existen dos enfoques principales para cifrar datos: **cifrado simétrico** y **cifrado asimétrico**, también conocido como de clave pública. Ambos son fundamentales para la seguridad digital, y suelen utilizarse en conjunto para maximizar la eficiencia y la protección.

### 1. Cifrado simétrico

Este tipo de cifrado utiliza una **única clave** para cifrar y descifrar la información. Es rápido y eficiente, por lo que se emplea en la mayoría de los sistemas donde se manejan grandes volúmenes de datos. Sin embargo, presenta un reto importante: tanto el emisor como el receptor deben compartir previamente la misma clave, lo cual puede ser riesgoso si se transmite por canales inseguros.

**Ejemplos de algoritmos simétricos:**
- **AES (Advanced Encryption Standard):** estándar actual, rápido y seguro.
- **DES (Data Encryption Standard):** ahora obsoleto, por su clave corta y vulnerabilidades conocidas.

### 2. Cifrado asimétrico (de clave pública)

Utiliza un **par de claves**: una pública, que se comparte libremente para cifrar los mensajes, y una privada, que solo el receptor posee y que se usa para descifrarlos. También permite firmar digitalmente documentos con la clave privada para verificar su autenticidad.

Este enfoque resuelve el problema de compartir claves de forma segura y se usa ampliamente en comunicaciones seguras por internet.

**Ejemplos de algoritmos asimétricos:**
- **RSA (Rivest–Shamir–Adleman):** uno de los sistemas más utilizados.
- **ECC (Elliptic Curve Cryptography):** ofrece el mismo nivel de seguridad que RSA, pero con claves más cortas y eficientes en dispositivos con pocos recursos.

## Aplicaciones de la criptografía

La criptografía tiene múltiples aplicaciones en la protección de la información en el entorno digital. A continuación, se presentan algunos de los usos más relevantes:

| **Uso** | **Descripción** |
|--------|-----------------|
| **Comunicaciones seguras** | Protege correos electrónicos, mensajes y llamadas para que solo el destinatario pueda acceder al contenido. |
| **Transacciones financieras** | Asegura los datos bancarios y tarjetas en compras y pagos en línea, previniendo el fraude. |
| **Autenticación de usuarios** | Verifica la identidad de los usuarios mediante contraseñas cifradas, certificados y firmas digitales. |
| **Almacenamiento seguro de datos** | Protege la información en discos duros o USBs en caso de pérdida o robo del dispositivo. |
| **Navegación web segura (HTTPS)** | Cifra las comunicaciones entre el navegador y los sitios web para proteger la información enviada. |
| **Protección de la privacidad** | Resguarda los datos personales en servicios de mensajería, redes sociales y plataformas en la nube. |
| **Firmas digitales** | Garantiza la integridad y autenticidad de documentos y transacciones electrónicas. |
| **Seguridad en redes y sistemas** | Protege el tráfico en VPNs, las contraseñas almacenadas y verifica archivos descargados. |
| **Protección de propiedad intelectual** | Permite controlar el acceso a contenidos digitales como libros, música o películas. |
| **Internet de las Cosas (IoT)** | Asegura la comunicación entre dispositivos conectados, previniendo manipulaciones externas. |

## Breve historia de la criptografía

La criptografía no es una disciplina moderna: ya en la antigüedad se empleaban métodos para ocultar mensajes. Uno de los más conocidos es el **Cifrado César**, usado por Julio César en sus comunicaciones militares. Consistía en reemplazar cada letra del mensaje con otra que se encontraba un número fijo de posiciones más adelante en el alfabeto.

Un hito clave en la historia moderna de la criptografía fue la **Máquina Enigma**, utilizada por los alemanes durante la Segunda Guerra Mundial para cifrar sus comunicaciones. Se consideraba indescifrable, pero un grupo de matemáticos británicos liderado por **Alan Turing** logró romper el código, lo que tuvo un impacto decisivo en el desenlace de la guerra.

![critografia](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/criptografia.png?raw=true)

A partir de los años 70, con el auge de la informática, surgieron sistemas más avanzados como la **criptografía de clave pública**, introducida por **Whitfield Diffie y Martin Hellman**, que permitió el intercambio seguro de claves sin contacto previo.

En la actualidad, la criptografía es esencial en casi todos los aspectos de la seguridad digital: protege nuestras contraseñas, datos bancarios, archivos personales, y permite una comunicación privada en un mundo cada vez más conectado.

---

**En resumen**, la criptografía no solo protege la información, sino que también genera confianza en los sistemas digitales. Comprender sus fundamentos es un paso esencial para cualquier profesional de la ciberseguridad.
