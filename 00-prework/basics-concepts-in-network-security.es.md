---
title: Seguridad de red Básica
tags:
  - ciberseguridad
authors:
  - blindma1den
  - lorenagubaira
description: >-
  Aprende a mejorar la seguridad de tu red con reglas de filtrado de paquetes en
  un firewall. ¡Descubre cómo proteger tu información hoy!
---
En el mundo actual, más del 90% de las brechas de datos comienzan con vulnerabilidades en la red. En esta lección, aprenderás a mejorar la seguridad de tu red configurando reglas de filtrado de paquetes en un firewall. Cubriremos los conceptos básicos de los firewalls, el filtrado de paquetes y tecnologías avanzadas como VPN y WPA/WPA2. Al final, podrás configurar reglas de firewall para proteger tu red y asegurar una comunicación segura. ¡Empecemos!

## Firewall y filtrado de paquetes

Un firewall es un dispositivo o software que se utiliza para proteger una red de amenazas externas. Funciona monitoreando y filtrando el tráfico de red que entra y sale de la red, permitiendo solo el tráfico seguro.

El **filtrado de paquetes** es una de las funciones principales de los firewalls. Este proceso implica inspeccionar cada paquete de datos que entra o sale de la red y compararlo con un conjunto de reglas de seguridad configuradas previamente. Si un paquete no cumple con las reglas, se bloquea y no se permite su transmisión.

El filtrado de paquetes puede basarse en diversos criterios, como la dirección IP, el puerto, la dirección MAC, el protocolo, el contenido de los paquetes, etc.

Además de proteger la red de ataques externos, los firewalls también pueden utilizarse para controlar el acceso de los usuarios a Internet y para limitar el tráfico de red interno, por ejemplo, para bloquear el acceso a sitios web no deseados.

La configuración de reglas de filtrado de paquetes en un firewall implica especificar las condiciones que se deben cumplir para que un paquete de datos sea permitido o bloqueado. Estas reglas se basan en criterios como la dirección IP de origen y destino, el puerto, el protocolo, etc.

### Pasos para configurar reglas de filtrado en un firewall:

1. **Acceder al firewall**: Para acceder al firewall y configurar las reglas de filtrado de paquetes, se requiere acceso a una consola de administración o a una interfaz web de gestión.
2. **Definir las reglas de filtrado**: Una vez dentro de la consola de administración, se pueden definir las reglas de filtrado de paquetes especificando los criterios para cada regla.
3. **Aplicar las reglas**: Una vez definidas las reglas, es necesario aplicarlas para que el firewall las utilice para filtrar el tráfico de red.
4. **Verificar el funcionamiento**: Finalmente, es importante verificar que las reglas de filtrado de paquetes se están aplicando correctamente y que no hay errores o conflictos.

>🔥 **Ejercicio** - Investiga sobre las reglas de firewall y crea 5 reglas y explique que tipo de trafico filtraria


### Tecnologías de Seguridad para Redes y Comunicaciones

**Virtual private network (VPN)**

Una **VPN** o **red privada** virtual crea una conexión de red privada entre dispositivos a través de Internet. Las VPN se utilizan para transmitir datos de forma segura y anónima a través de redes públicas. Su funcionamiento consiste en ocultar las direcciones IP de los usuarios y cifrar los datos para que nadie que no esté autorizado a recibirlos pueda leerlos.

Una conexión VPN redirige los paquetes de datos de una maquina a otro servidor remoto antes de enviarlos a terceros a traves de internet

Las principales características de la tecnología VPN son las siguientes:

- **Protocolo de túnel**

Una red privada virtual crea un túnel de datos seguro entre su máquina local y otro servidor VPN situado a miles de kilómetros. Cuando se conecta, este servidor VPN se convierte en el origen de todos sus datos. El proveedor de servicios de Internet (ISP) y otros terceros ya no pueden ver el contenido de su tráfico de Internet.

- **Cifrado**

Los protocolos VPN como IPSec codifican sus datos antes de enviarlos a través del túnel de datos. IPsec es un conjunto de protocolos para proteger las comunicaciones por protocolo de Internet (IP) mediante la autenticación y el cifrado de todos los paquetes IP de una secuencia de datos. El servicio de VPN actúa como un filtro, lo que hace que sus datos sean ilegibles en un extremo y solo los descodifica en el otro, lo que evita el uso indebido de datos personales, incluso si su conexión de red se viera comprometida. El tráfico de red ya no es vulnerable a los ataques, y su conexión a Internet es segura.

- **Acceso wifi protegido (WPA)**

El WPA (acceso Wi-Fi protegido) es un protocolo de seguridad inalámbrica lanzado en 2003 para solucionar las crecientes vulnerabilidades de su predecesor, WEP. El protocolo Wi-Fi WPA es más seguro que el WEP, porque usa una clave de 256 bits para el cifrado, lo que supone una gran mejora respecto a las claves de 64 y 128 bits que usa el sistema WEP.

El WPA también usa el Protocolo de integridad de clave temporal (TKIP), que genera de forma dinámica una nueva clave para cada paquete o unidad de datos. El TKIP es mucho más seguro que el sistema de clave fija que usa WEP.

Aun así, el WPA no está exento de defectos. El TKIP, el componente principal de WPA, se diseñó para implementarse en los sistemas con WEP a través de actualizaciones de firmware. Esto hizo que el WPA siguiera basándose en elementos fácilmente explotables.

- **Acceso WiFi protegido 2 (WPA2)**

El WPA2 (acceso Wi-Fi protegido 2) es la segunda generación del protocolo de seguridad inalámbrica de acceso Wi-Fi protegido. Al igual que su predecesor, el WPA2 se diseñó para asegurar y proteger las redes Wi-Fi. El WPA2 garantiza que los datos enviados o recibidos a través de la red inalámbrica estén cifrados y que solo tengan acceso a ellos las personas que tengan la contraseña de la red.

Una de las ventajas del sistema WPA2 fue que introdujo el sistema de cifrado avanzado (AES) para sustituir al sistema TKIP, más vulnerable, usado en el protocolo WPA original. El AES proporciona un cifrado potente y lo utiliza el gobierno de Estados Unidos para proteger los datos clasificados.
