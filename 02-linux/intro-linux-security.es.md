---
title: Introducción a la seguridad de Linux
tags:
  - linux
  - ciberseguridad
authors:
  - blindma1den
  - lorenagubaira
description: >-
  Aprende los conceptos básicos y mejores prácticas de seguridad en Linux.
  Protege tu sistema con usuarios, contraseñas seguras y cortafuegos. ¡Descubre
  más!
---
La seguridad es un aspecto fundamental en cualquier sistema operativo, y a medida que más personas y organizaciones utilizan Linux, es importante comprender los conceptos básicos de seguridad para proteger nuestros sistemas y datos.

- **Usuarios y permisos**: En Linux, cada usuario tiene su propia cuenta y conjunto de permisos. Es importante crear cuentas de usuario separadas para cada persona que acceda al sistema y asignar los permisos adecuados. Los permisos determinan qué acciones pueden realizar los usuarios en archivos y directorios, como leer, escribir o ejecutar.
- **Contraseñas seguras**: Es importante utilizar contraseñas seguras que sean difíciles de adivinar. Una contraseña segura debe tener una combinación de letras mayúsculas y minúsculas, números y caracteres especiales. Además, se recomienda cambiar las contraseñas periódicamente.
- **Actualizaciones del sistema**: Mantener el sistema operativo Linux actualizado es esencial para garantizar la seguridad. Las actualizaciones del sistema incluyen parches de seguridad que corrigen vulnerabilidades conocidas. Es importante instalar regularmente las actualizaciones del sistema para protegerse contra posibles amenazas.
- **Firewall**: Un firewall es una herramienta de seguridad que controla el tráfico de red entrante y saliente. Linux cuenta con un firewall incorporado llamado iptables, que permite configurar reglas para permitir o bloquear el tráfico según nuestras necesidades. Configurar un firewall adecuado puede ayudar a proteger el sistema contra ataques externos.
- **Antivirus y software de seguridad**: Aunque Linux es menos susceptible a virus y malware en comparación con otros sistemas operativos, aún es importante utilizar software de seguridad, como antivirus y herramientas de detección de intrusiones. Estas herramientas pueden ayudar a identificar y eliminar amenazas potenciales.
- **Auditoría de seguridad**: Realizar auditorías de seguridad periódicas es una buena práctica para identificar posibles vulnerabilidades en el sistema. Las auditorías de seguridad pueden incluir la revisión de registros de actividad, análisis de vulnerabilidades y pruebas de penetración. Estas actividades nos permiten detectar y corregir posibles problemas de seguridad antes de que sean explotados.

## Gestión de cuentas de usuario y contraseñas seguras

Algunos aspectos que podemos tomar en cuenta para la gestión de cuentas de usuarios:

- **Creación de cuentas de usuario**: En Linux, se pueden crear cuentas de usuario utilizando comandos como "**useradd**" o "**adduser**". Al crear una cuenta de usuario, es importante asignar un nombre de usuario único y una contraseña segura. Además, se pueden establecer otros detalles como el directorio de inicio y el grupo primario.
- **Contraseñas seguras**: Es fundamental utilizar contraseñas seguras que sean difíciles de adivinar. Se recomienda utilizar una combinación de letras mayúsculas y minúsculas, números y caracteres especiales. Evita utilizar contraseñas obvias o información personal fácilmente accesible.
- **Políticas de contraseñas**: Establecer políticas de contraseñas es una práctica recomendada para garantizar que los usuarios utilicen contraseñas seguras. Estas políticas pueden incluir requisitos como una longitud mínima de contraseña, la necesidad de cambiar las contraseñas periódicamente y la prohibición de reutilizar contraseñas antiguas. Estas políticas se pueden configurar en el archivo "/etc/login.defs" o utilizando herramientas de gestión de contraseñas como "pam_cracklib".
- **Autenticación de dos factores**: La autenticación de dos factores (2FA) proporciona una capa adicional de seguridad al requerir un segundo método de verificación, además de la contraseña, para acceder a una cuenta. Esto ayuda a prevenir el acceso no autorizado incluso si la contraseña se ve comprometida.
- **Gestión de privilegios**: Es importante asignar los privilegios adecuados a cada cuenta de usuario en Linux. No todos los usuarios necesitan tener acceso de administrador o privilegios de superusuario. Siguiendo el principio de "menos privilegios", se deben otorgar sólo los privilegios necesarios para realizar las tareas requeridas. Esto ayuda a limitar el impacto de posibles ataques o errores humanos.

## Configuración de cortafuegos y protección de servicios

La configuración de un cortafuegos y la protección de servicios son aspectos fundamentales para garantizar la seguridad de un sistema. Estas medidas ayudan a prevenir accesos no autorizados y proteger los servicios que se ejecutan en el sistema. Aquí hay algunos conceptos clave a tener en cuenta:

- **Cortafuegos**: Un cortafuegos es una barrera de seguridad que controla el tráfico de red entrante y saliente. Su objetivo principal es permitir o bloquear el tráfico según las reglas establecidas. En Linux, el cortafuegos más comúnmente utilizado es iptables. Permite configurar reglas para filtrar el tráfico basado en direcciones IP, puertos y protocolos.
- **Reglas del cortafuegos**: Al configurar un cortafuegos, es importante definir reglas específicas para permitir o bloquear el tráfico. Por ejemplo, se pueden establecer reglas para permitir el acceso a servicios específicos, como SSH o HTTP, desde direcciones IP confiables. También se pueden bloquear puertos no utilizados o restringir el acceso a servicios sensibles.
- **Protección de servicios**: Los servicios que se ejecutan en un sistema, como servidores web, bases de datos o servidores de correo electrónico, pueden ser objetivos de ataques. Para proteger estos servicios, se deben tomar medidas adicionales, como:
- **Mantener los servicios actualizados**: Es importante aplicar regularmente las actualizaciones de seguridad para los servicios instalados. Esto ayuda a corregir vulnerabilidades conocidas y proteger contra ataques conocidos.
- **Configuración segura**: Asegúrate de configurar los servicios de manera segura, siguiendo las mejores prácticas recomendadas. Esto incluye deshabilitar funciones innecesarias, establecer permisos adecuados en los archivos y directorios, y utilizar contraseñas seguras para las cuentas asociadas con los servicios.
- **Monitoreo y registro**: Implementa herramientas de monitoreo y registro para supervisar la actividad de los servicios. Esto permite detectar posibles intrusiones o comportamientos anómalos y tomar medidas preventivas.
- **Limitar el acceso**: Restringe el acceso a los servicios solo a las direcciones IP o rangos de IP necesarios. Esto ayuda a reducir la superficie de ataque y limitar la exposición a posibles amenazas.
- **Herramientas de seguridad adicionales**: Además de un cortafuegos, existen otras herramientas de seguridad que se pueden utilizar para proteger los servicios en Linux. Por ejemplo, se pueden implementar sistemas de detección y prevención de intrusiones (IDS/IPS) para monitorear y bloquear actividades sospechosas. También se pueden utilizar herramientas de escaneo de vulnerabilidades para identificar posibles debilidades en los servicios.

## Instalacion de iptables

**iptables** es una herramienta de firewall y filtrado de paquetes en sistemas Linux. Permite controlar y configurar las reglas de seguridad de red para proteger tu sistema y controlar el tráfico de red entrante y saliente.
Con iptables, se puede definir reglas que determinen qué paquetes de red se permiten o bloquean en tu sistema. Estas reglas se basan en criterios como la dirección IP de origen o destino, el puerto de origen o destino, el protocolo utilizado y otras características de los paquetes.
Las reglas de iptables se organizan en tablas, y cada tabla contiene cadenas de reglas. Las tablas más comunes son "filter", que se utiliza para filtrar paquetes, y "nat", que se utiliza para realizar traducción de direcciones de red (NAT).
Dentro de cada tabla, hay diferentes cadenas predefinidas, como "INPUT" para el tráfico entrante, "OUTPUT" para el tráfico saliente y "FORWARD" para el tráfico que se reenvía a través del sistema. Puedes agregar reglas a estas cadenas para especificar qué hacer con los paquetes que coinciden con esas reglas, como aceptarlos, rechazarlos o redirigirlos.

Para su instalacion debemos:

1. **Verificar si iptables está instalado**

Para verificar si iptables ya está instalado en tu sistema, puedes ejecutar el siguiente comando en la terminal:
    
```bash
iptables --version
```

> 💡 Si iptables está instalado, verás la versión del software. Si no está instalado, puedes pasar al siguiente paso.

2.  **Instalar iptables**

La forma de instalar iptables puede variar según la distribución de Linux que estés utilizando. Aquí te mostraré cómo hacerlo en algunas distribuciones populares:
- Ubuntu o Debian:

```bash
sudo apt-get update
sudo apt-get install iptables
```

Adicionalmente haremos la instalacion de `iptables-persistent` ya que este paquete facilita la persistencia de las reglas de iptables a través de reinicios del sistema. Normalmente, las reglas configuradas en iptables se pierden cuando el sistema se reinicia. `iptables-persistent` guarda las reglas actuales y las restaura automáticamente al inicio del sistema, garantizando que las configuraciones de firewall se mantengan consistentes.

```bash
sudo apt-get install iptables-persistent
```

Durante la instalación, se te pedirá si deseas guardar las reglas actuales de iptables en los archivos rules.v4 y rules.v6.

- CentOS o RHEL:

```bash
sudo yum install iptables
```

## Agregando reglas a iptables

Una vez que iptables esté instalado, puedes comenzar a configurarlo según tus necesidades. Para agregar una nueva regla a iptables, puedes usar el comando `iptables` directamente. Por ejemplo, para permitir el tráfico TCP entrante al puerto 80 (HTTP), puedes ejecutar:

```bash
sudo iptables -A INPUT -p tcp --dport 80 -j ACCEPT
```

Es importante tener en cuenta que para que estas reglas ingresadas se puedan guardar explicitamente en archivos, deberemos especificarlo a través de la linea de comando.

### Guardar y aplicar las reglas

Una vez que hayas definido tus reglas aplicamos las mismas utilizando el siguiente comando:

```bash
sudo iptables-save | sudo tee /etc/iptables/rules.v4 >/dev/null
```

Esto guardará las reglas desde el kernel de nuestra computadora al archivo de configuración `rules.v4` y las aplicará en tu sistema.

### Modificación/Agregado de reglas desde el archivo `rules`

Puedes abrir el archivo de configuración para iptables utilizando un editor de texto, como nano o vim. Por ejemplo:

```bash
sudo nano /etc/iptables/rules.v4
```

Una vez abierto el archivo agrega o modifica las reglas que necesites. Acá tienes un ejemplo de lo que podria contener el archivo /etc/iptables/rules.v4:

```plaintext
# Generated by iptables-save v1.8.7 on Mon Jul 18 09:23:45 2023
*filter
:INPUT ACCEPT [0:0]
:FORWARD ACCEPT [0:0]
:OUTPUT ACCEPT [0:0]
-A INPUT -p tcp --dport 80 -j ACCEPT
COMMIT
# Completed on Mon Jul 18 09:23:45 2023
```

Después de editar el archivo de reglas, debemos  restaurarlas en iptables para que las aplique en el firewall utilizando el siguiente comando:

```sh
sudo iptables-restore < /etc/iptables/rules.v4
```

### Aceptando conexiones TCP al puerto 22

La siguiente regla de iptables permite conexiones TCP entrantes al servidor en el puerto 22, que generalmente se utiliza para el acceso SSH (Secure Shell). 

```bash
-A INPUT -p tcp --dport 22 -j ACCEPT
```

Aquí hay un desglose de la regla:

- `-A INPUT`: Esto añade la regla a la cadena `INPUT`, que maneja el tráfico de red entrante.
- `-p tcp`: Esto especifica el protocolo a coincidir, que en este caso es TCP (Protocolo de Control de Transmisión).
- `--dport 22`: Esto coincide con los paquetes que están destinados al puerto 22. La bandera `dport` significa "puerto de destino".
- `-j ACCEPT`: Esto especifica el destino de la regla, que en este caso es `ACCEPT` (aceptar) el paquete. Esto significa que el tráfico que coincide con la regla será permitido a través del firewall.

En Resumen:

- La regla se añade a la cadena `INPUT`, que trata con el tráfico entrante.
- Coincide con paquetes TCP.
- Específicamente apunta a paquetes destinados al puerto 22.
- Acepta estos paquetes, permitiendo que la conexión se establezca.

### Bloqueando los request PING

```bash
-A INPUT -p icmp --icmp-type echo-request -j DROP
```

Esta regla de iptables se utiliza para bloquear solicitudes de ping entrantes al servidor. Aquí tienes un desglose detallado de la regla:

- `-A INPUT`: Esto añade la regla a la cadena `INPUT`, que maneja el tráfico de red entrante.
- `-p icmp`: Esto especifica el protocolo a coincidir, que en este caso es ICMP (Protocolo de Mensajes de Control de Internet).
- `--icmp-type echo-request`: Esto coincide con los paquetes que son solicitudes de eco ICMP, que se utilizan para las operaciones de ping. El tipo `echo-request` es el tipo de mensaje ICMP que se envía cuando se realiza un ping.
- `-j DROP`: Esto especifica el destino de la regla, que en este caso es `DROP` (descartar) el paquete. Esto significa que el tráfico que coincida con la regla será descartado silenciosamente y no se enviará ninguna respuesta al remitente.

En Resumen:

- La regla se añade a la cadena `INPUT`, que trata con el tráfico entrante.
- Coincide con paquetes ICMP.
- Específicamente apunta a paquetes de solicitud de eco ICMP, que se utilizan para las operaciones de ping.
- Descarta estos paquetes, bloqueando efectivamente las solicitudes de ping al servidor.

Al implementar esta regla, evitas que entidades externas hagan ping a tu servidor, lo que puede ayudar a reducir el riesgo de ciertos tipos de ataques de red o actividades de reconocimiento.


## Verificar las reglas

Puedes verificar las reglas de iptables utilizando el siguiente comando:

```bash
sudo iptables -L
```


Y eso es todo! Ahora tienes iptables instalado y configurado en tu sistema.
