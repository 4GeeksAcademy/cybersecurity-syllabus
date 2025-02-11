---
title: Máquinas Virtuales para practicar ciberseguridad
description: >-
  Descubre las mejores máquinas virtuales para practicar ciberseguridad. Aprende
  a dominar inyección SQL, XSS y más en un entorno seguro. ¡Empieza hoy!
tags:
  - ciberseguridad
---
# Máquinas Virtuales y proyectos para practicar ciberseguridad

En 4Geeks, nos gusta que nuestros estudiantes aprendan en entornos reales similares a los que encontrarán una vez que consigan un trabajo en el campo. Es por eso que preferimos usar máquinas virtuales en lugar de servicios en la nube como HackABox, TryHackMe, etc. Recomendamos usar servicios en la nube una vez que te familiarices con la instalación y el uso de configuraciones reales.

Por otro lado, se recomienda encarecidamente el uso de una máquina virtual porque estarás hackeando mucho. No querrás que tu computadora personal se vuelva vulnerable o sea hackeada; usar máquinas virtuales (VMs) es una excelente manera de aprender ciberseguridad en un entorno controlado y aislado.

Usamos una combinación de VMs internas y de dominio público diseñadas específicamente para entrenamiento en seguridad, que van desde niveles para principiantes hasta avanzados. Estas incluyen aplicaciones y sistemas vulnerables preconfigurados, que son ideales para practicar pruebas de penetración, análisis de vulnerabilidades y explotación.

## 1. Metasploitable 2 y 3

- **Nivel de Dificultad**: Principiante a Intermedio
- **Sistema Operativo**: Linux
- **Prácticas Ideales**: Seguridad de red, explotación de servicios, evaluación de vulnerabilidades
- **Algunos ejemplos de ejercicios que puedes hacer**:
  - Explotar vulnerabilidades conocidas en servicios como FTP, SSH y HTTP.
  - Practicar la seguridad en servicios y permisos mal configurados.
  - Usar herramientas como Nmap y Metasploit para realizar pruebas de penetración.
  - Enumeración de Servicios: Usar herramientas como Nmap para identificar puertos abiertos y servicios en ejecución en la VM.
  - Explotación de FTP: Explotar servicios FTP vulnerables para obtener acceso no autorizado o leer/escribir archivos.
  - Misconfiguraciones de Apache: Identificar y explotar configuraciones incorrectas comunes en el servidor Apache.
  - Explotación de Comparticiones Samba: Obtener acceso no autorizado a través de comparticiones Samba mal configuradas.
  - Explotación de Vulnerabilidades de Base de Datos: Usar [inyección SQL](https://4geeks.com/es/lesson/entendiendo-la-inyeccion-sql-la-segunda-vulnerabilidad-mas-critica-segun-owasp) en servicios MySQL vulnerables para acceder o manipular contenidos de la base de datos.

## 2. DVWA (Damn Vulnerable Web Application)

- **Nivel de Dificultad**: Principiante
- **Sistema Operativo**: Cualquier pila LAMP (Linux, Apache, MySQL, PHP)
- **Prácticas Ideales**: Seguridad de aplicaciones web, desde [inyección SQL](https://4geeks.com/es/lesson/entendiendo-la-inyeccion-sql-la-segunda-vulnerabilidad-mas-critica-segun-owasp) hasta XSS y CSRF
- **Algunos ejemplos de ejercicios que puedes hacer**:
  - Realizar inyecciones SQL para revelar contenidos de la base de datos.
  - Implementar y probar ataques de [Cross-Site Scripting (XSS)](https://4geeks.com/es/lesson/como-realizar-o-prevenir-el-ataque-xss-secuencias-de-comandos-entre-sitios).
  - Asegurar aplicaciones contra vulnerabilidades CSRF.
  - Práctica de Inyección SQL: Realizar inyecciones SQL para recuperar datos ocultos de la base de datos.
  - Cross-Site Scripting (XSS): Crear y ejecutar cargas útiles de XSS para comprender las vulnerabilidades de scripting del lado del cliente.
  - Inyección de Comandos: Explotar vulnerabilidades de inyección de comandos para ejecutar comandos no autorizados en el servidor.
  - Vulnerabilidades de Subida de Archivos: Probar y explotar funcionalidades de subida de archivos para entender los riesgos asociados con la manipulación inadecuada de archivos.
  - Ataques de Fuerza Bruta: Realizar ataques de fuerza bruta en formularios de inicio de sesión para entender la importancia de la limitación de velocidad y políticas de contraseñas fuertes.

## 3. OWASP WebGoat

- **Nivel de Dificultad**: Principiante a Intermedio
- **Sistema Operativo**: Multiplataforma (basado en Java)
- **Prácticas Ideales**: Vulnerabilidades de aplicaciones web y prácticas de codificación segura
- **Algunos ejemplos de ejercicios que puedes hacer**:
  - Trabajar a través de lecciones que explican vulnerabilidades con tareas prácticas.
  - Mitigar vulnerabilidades en escenarios simulados.
  - Desarrollar parches de código seguro para problemas identificados.
  - Fallos de Autenticación: Aprender sobre fallos en los mecanismos de autenticación y cómo explotarlos.
  - Fallos de Control de Acceso: Entender controles de acceso rotos y practicar cómo eludirlos.
  - Revisión de Código Seguro: Realizar revisiones de código para identificar fallos de seguridad en el código fuente.
  - Fallos de Inyección: Practicar la explotación de varios fallos de inyección, incluyendo SQL, XML y LDAP.
  - Fallos de Concurrencia: Explotar la concurrencia para realizar tareas como transferencias de dinero sin la sincronización adecuada.

## 4. OWASP Juice Shop

- **Nivel de Dificultad**: Intermedio
- **Sistema Operativo**: Multiplataforma (Node.js)
- **Prácticas Ideales**: Vulnerabilidades modernas de aplicaciones web, seguridad de API y mejores prácticas de seguridad
- **Algunos ejemplos de ejercicios que puedes hacer**:
  - Realizar un ataque [XSS](https://4geeks.com/es/lesson/como-realizar-o-prevenir-el-ataque-xss-secuencias-de-comandos-entre-sitios) y luego implementar políticas de seguridad de contenido para mitigarlo.
  - Realizar ejercicios de Control de Acceso Roto.
  - Explorar deserialización insegura y configuración ambiental incorrecta.
  - Autenticación Rota: Identificar y explotar problemas de autenticación para obtener acceso no autorizado.
  - Exposición de Datos Sensibles: Explorar varias maneras en que los datos sensibles podrían estar expuestos de forma incorrecta y cómo protegerlos.
  - XSS y CSRF: Experimentar con Cross-Site Scripting y Cross-Site Request Forgery para entender estas vulnerabilidades comunes en la web.
  - Deserialización Insegura: Aprender sobre y explotar vulnerabilidades de deserialización insegura.
  - Seguridad de API: Probar y asegurar APIs contra vulnerabilidades comunes como gestión inadecuada de activos y falta de limitación de recursos y tasa.

## 5. VMs de VulnHub

- **Nivel de Dificultad**: Principiante a Avanzado (varía según la VM)
- **Sistema Operativo**: Varios
- **Prácticas Ideales**: Amplia gama de prácticas de seguridad, desde escenarios amigables para principiantes hasta configuraciones complejas
- **Algunos ejemplos de ejercicios que puedes hacer**:
  - Cada VM generalmente viene con un conjunto específico de desafíos, diseñados para practicar un conjunto particular de habilidades.
  - Las tareas a menudo implican descubrir y explotar vulnerabilidades para obtener niveles de acceso más altos.
  - Escaneo de Vulnerabilidades: Usar herramientas como Nessus o OpenVAS para escanear e identificar vulnerabilidades.
  - Pruebas de Penetración: Realizar pruebas de penetración estructuradas para explotar vulnerabilidades descubiertas.
  - Ingeniería Inversa: Analizar binarios para encontrar funcionalidades ocultas o vulnerabilidades.
  - Desarrollo de Exploits: Desarrollar exploits para vulnerabilidades identificadas.
  - Post-Explotación: Entender los pasos después de obtener acceso, incluyendo mantener el acceso y borrar rastros.

## 6. Hack The Box

- **Nivel de Dificultad**: Intermedio a Avanzado
- **Sistema Operativo**: Varios
- **Prácticas Ideales**: Pruebas de penetración del mundo real, ingeniería inversa y criptoanálisis
- **Algunos ejemplos de ejercicios que puedes hacer**:
  - Completar diferentes cajas desde la enumeración hasta obtener acceso de root.
  - Usar varias herramientas de pruebas de penetración en un entorno controlado.
  - Ingeniería inversa de aplicaciones para entender fallos de seguridad.

## Otras computadoras proporcionadas a través de plataformas en línea

Los siguientes servicios gratuitos y de pago están especializados en proporcionar varias computadoras y VMs para practicar:

### 7. Proving Grounds de Offensive Security

- **Nivel de Dificultad**: Intermedio a Avanzado
- **Sistema Operativo**: Varios
- **Prácticas Ideales**: Pruebas de penetración en un entorno seguro, legal y controlado
- **Algunos ejemplos de ejercicios que puedes hacer**:
  - Seguir rutas estructuradas para aprender pruebas de penetración.
  - Practicar exploits en una variedad de sistemas operativos y configuraciones de software.

### 8. PentesterLab

- **Nivel de Dificultad**: Principiante a Intermedio
- **Sistema Operativo**: Varios
- **Prácticas Ideales**: Vulnerabilidades y exploits específicos de la web, codificación segura
- **Algunos ejemplos de ejercicios que puedes hacer**:
  - Completar ejercicios que enseñan secuestro de sesión, ataques web y el uso de encabezados de seguridad.
  - Analizar el código fuente para encontrar vulnerabilidades.

### 9. TryHackMe

- **Nivel de Dificultad**: Principiante

 a Intermedio
- **Sistema Operativo**: Varios
- **Prácticas Ideales**: Seguridad de red, scripting para seguridad, explotación de sistemas
- **Algunos ejemplos de ejercicios que puedes hacer**:
  - Participar en eventos Capture The Flag (CTF).
  - Seguir rutas guiadas para aprender sobre diferentes aspectos de la ciberseguridad.

### 10. SANS SIFT

- **Nivel de Dificultad**: Intermedio a Avanzado
- **Sistema Operativo**: Ubuntu Linux
- **Prácticas Ideales**: Análisis forense digital, respuesta a incidentes e investigación de ciberseguridad
- **Algunos ejemplos de ejercicios que puedes hacer**:
  - Realizar análisis forense de capturas de red.
  - Analizar imágenes de disco en busca de evidencia de intrusiones.

Esta categorización debería ayudar a seleccionar el entorno adecuado para las etapas de aprendizaje de los estudiantes, desde prácticas fundamentales en ciberseguridad hasta áreas más complejas y especializadas.
