---
title: "Gestión de dirección IP"
subtitle: "Mastering IP Address Management: Vital Skills for Network and Cybersecurity Pros. Learn How IP Addresses Drive Network Infrastructure and Cybersecurity."
tags: ["ip-address", "ciberseguridad"]
authors: ["blindma1den", "lorenagubaira"]

---

Es fundamental que un profesional de redes y ciberseguridad sepa gestionar direcciones IP debido a que las direcciones IP son elementos esenciales en la infraestructura de cualquier red, y desempeñan un papel crítico en la ciberseguridad.

## Dirección IP

- Una dirección IP (Protocolo de Internet) es un número único asignado a cada dispositivo conectado a una red, ya sea en una red local (LAN) o en Internet (WAN).
- Funciona de manera similar a la dirección de una casa en una calle, identificando la ubicación de un dispositivo en la red.

Imagina que tienes una red doméstica con varios dispositivos, como tu computadora, tu teléfono y tu impresora. Cada uno de estos dispositivos tiene su propia dirección IP única, como una etiqueta de dirección para que los datos puedan llegar al destino correcto.

## Subnetting: Cómo se confórman las redes

- Subnetting es el proceso de dividir una red en subredes más pequeñas. Esto se hace por varias razones, incluida la mejora de la eficiencia de la red y la seguridad.
- En ciberseguridad y pentesting, subnetting se utiliza para segmentar una red en partes más pequeñas, lo que puede ayudar a aislar y controlar el tráfico. Esto es crucial para proteger los recursos críticos y limitar la propagación de amenazas en una red.

> 💭  Imagina que tienes una red empresarial con departamentos diferentes, como ventas y contabilidad. Puedes utilizar subnetting para crear subredes separadas para cada departamento, lo que ayuda a mantener su tráfico separado y seguro. Si un atacante ingresa a una subred, su capacidad para moverse a otras partes de la red estará limitada gracias a la segmentación.

- Un profesional de ciberseguridad debe **comprender** cómo se asignan y gestionan las direcciones IP en una red para detectar y responder a amenazas. Esto incluye la identificación de dispositivos sospechosos o no autorizados que puedan intentar acceder a la red.
- El conocimiento de subnetting es esencial para diseñar y configurar medidas de seguridad efectivas, como firewalls, que pueden limitar el tráfico no autorizado entre subredes.
- En pentesting, el conocimiento de subnetting es crucial para evaluar la seguridad de una red, identificar posibles puntos de vulnerabilidad y simular ataques de manera efectiva dentro de las subredes.

Las direcciones IP son asignadas por organizaciones encargadas de administrar y distribuir recursos de direcciones IP en todo el mundo. La entidad principal que supervisa la asignación de direcciones IP en Internet es la **Internet Assigned Numbers Authority (IANA)**, que es una entidad que opera bajo la supervisión de la **Internet Corporation for Assigned Names and Numbers (ICANN)**.

La IANA es responsable de asignar bloques de direcciones IP a las **Regiones de Internet**, que son cinco regiones geográficas designadas en todo el mundo:

1. **América del Norte**
2. **Europa**
3. **Asia Pacífico**
4. **América Latina y el Caribe**
5. **África**

Cada una de estas regiones tiene su propio **Registro Regional de Internet** (RIR), que es una organización que gestiona y distribuye direcciones IP en su área geográfica correspondiente. Estos RIR son:

| ARIN (American Registry for Internet Numbers) | Responsable de América del Norte. |
| --- | --- |
| RIPE NCC (Réseaux IP Européens Network Coordination Centre) | Responsable de Europa, Oriente Medio y parte de Asia Central. |
| APNIC (Asia-Pacific Network Information Centre) | Responsable de la región de Asia Pacífico. |
| LACNIC (Latin America and Caribbean Network Information Centre) |  Encargado de América Latina y el Caribe. |
| AfriNIC (African Network Information Centre) |  Responsable de África. |

Estos RIRs, a su vez, asignan bloques más pequeños de direcciones IP a proveedores de servicios de Internet (ISP), empresas y otras organizaciones que necesitan direcciones IP para sus redes.

Por lo tanto, la asignación de direcciones IP sigue una jerarquía, desde la IANA hasta los RIR y finalmente a los usuarios finales. Los RIRs trabajan para garantizar una distribución justa y eficiente de direcciones IP en sus regiones respectivas y también mantienen registros de las asignaciones realizadas. Esto asegura que las direcciones IP se utilicen de manera efectiva y que no se agoten rápidamente en un momento dado

## Direcciones IP

La dirección IP también conocida como la Internet protocol address, es la dirección de un dispositivo como un ordenador o un servidor web o una impresora, en una red interna o externa. Una forma de entender el concepto es la dirección de una persona para que le pueda llegar el correo, ese correo tiene que llevar la dirección exacta de la persona que recibe para que el personal de correo sepa a donde enviarla, en el caso del internet, esa dirección sería un “número de puerta” concreto para poder comunicarse con otros dispositivo y recibir paquetes de datos de ellos. La dirección IP se basa en el protocolo de internet,  y cada dirección sólo puede asignarse una vez al mismo tiempo.

Existen dos tipos de direcciones IP con aspectos muy diferentes, lo que pueden tener en común es que se componen de un identificador de red para que pueda encontrar el camino en el Enrutado ip, y de un identificador de dispositivo para así poder llegar hasta un dispositivo concreto.

Los dos tipos de dirección IP son:

### IPv4

Este tipo de IP consta en una dirección de 32 bits separado en 4 octeto (grupo de 8 bits), limitadas a  4 294 967 296 direcciones únicas, muchas de ellas LAN. Desde el punto de vista técnico, son un código binario de 32 cifras entre 0 y 1. Generalmente se suele representar como una combinación de número decimales con valores entre 0 y 255 separados por puntos. Un ejemplo de una direccion IPv4 puede ser 192.168.178.31

Actualmente esta asignación de direcciones IP pasa por una arquitectura de clases que consta de tres clases de direcciones IP que una organización puede recibir de parte de la Internet Corporation for Assigned Names and Numbers (ICANN).

- **Red clase A**

Se asigna el primer octeto para identificar la red, reservando los últimos tres octetos (24 bits) para que sean asignados a los hosts. por lo que tendría 16.777.214 hosts disponibles.

- **Red clase B**

Se asignan los dos primeros octetos para identificar la red, reservando los últimos dos octetos (16 bits) para que sean asignados a los hosts. por lo que tendrían 65.534 hosts.

- **Red clase C**

Se asignan los primeros 3 octetos para identificar la red, reservando el último octeto para que sea asignado a los hosts, por lo que la cantidad máxima de hosts sería 254 hosts

Estos cálculos podemos sacarlo elevando 2 por la cantidad de bits reservados para identificar la red menos 2 direcciones que son reservada para el broadcast y la dirección asignada de la red.

En la siguiente tabla podemos ver cómo se diferencian cada uno de las clases de redes:

| Clase | Bits | N de redes | N direcciones por red | N hosts por red | Máscara de red |
| --- | --- | --- | --- | --- | --- |
| A | 0 | 0.0.0.0 - 127.255.255.255 | 224 = 16.777.216 | 224 - 2 16.777.214 | 255.0.0.0 |
| B | 10 | 128.0.0.0 - 191.255.255.255 | 216 = 65.536 | 216  - 2 65.534 | 255.255.0.0 |
| C | 110 | 192.0.0.0 - 233.255.255.255 | 28 = 256 | 28 - 2 254 | 255.255.255.0 |
| D (Multicast) | 1110 | 224.0.0.0 - 239.255.255.255 |  |  |  |
| E (Experimental) | 1111 | 240.0.0.0 - 255.255.255.254 |  |  |  |

### Direcciones IPv6

Tienen la misma función de la dirección IPv4, esta consta de 128 bits y se expresa en notación hexadecimal de 32 dígitos, esta se creó para resolver el problema de agotamiento de direcciones IPv4, ya que este contaba con 4.294.967.296  (232) el cual es un número menor a la población mundial y dispositivos totales. A principios de 2010 quedaban menos de 10% de direcciones sin asignar, por lo que se desarrolló la IPv6 que admite 2128 o 340 sextillones de direcciones.

El cambio más grande de IPv4 a IPv6 es la longitud de las direcciones de red, para la ipV6 fue asignada con 128 bits, el cual corresponde a 32 dígitos hexadecimales, en muchas ocasiones las direcciones IPv6 están compuestas por dos partes lógicas: un prefijo de 64 bits y otra parte de 64 bits que corresponde al identificador de interfaz, que casi siempre se genera automáticamente a partir de la dirección MAC de la interfaz a la que está asignada la dirección. Esta se escribe como 8 grupos de cuatro dígitos hexadecimales por ejemplo:

```bash
2001:0db8:85a4:0000:15e2::a8e2:1380:7545
```

Se puede comprimir un grupo de cuatro dígitos si tiene el valor de 0000.

```bash
2001:0db8:85a4::15e2::a8e2:1380:7545
```

Siguiendo esta regla, si más de dos grupos consecutivos son nulos, también pueden comprimirse como "::". Si la dirección tiene más de una serie de grupos nulos consecutivos la compresión solamente se permite en uno de ellos. Así, las siguientes son representaciones posibles de una misma dirección:

```bash
2001:0DB8:0000:0000:0000:0000:1428:57ab
2001:0DB8:0::0:1428:57ab
2001:0DB8::1428:57ab
```

### División de redes: Subnetting

Un dominio de difusión/broadcast grande es una red que conecta muchos hosts. Un problema que podemos tener con estos hosts es que pueden generar broadcast excesivas y afectar negativamente a la red. Esto da como resultado operaciones de red lentas debido a la cantidad significativa de tráfico que puede causar, y operaciones lentas del dispositivo porque un dispositivo debe aceptar y procesar cada paquete de broadcast.

La solución es reducir el tamaño de la red para crear dominios de difusión más pequeños en un proceso llamado subred. Estos espacios de red más pequeños se denominan subredes.

Esta división en subredes reduce el tráfico general de la red y mejora el rendimiento de la red. También permite que un administrador implemente políticas de seguridad como que subredes están permitidas o no para comunicarse entre sí.

El subnetting tiene como función dividir a una red grande en varias subredes más pequeñas, esto se debe realizar con mucho cuidado y planificación para no desaprovechar las direcciones IPv4.

Las redes se pueden subdividir más fácilmente en el límite de octeto /8, /16, /24. esto se puede calcular conociendo la máscara de subred de la ip que vamos a configurar.

| Longitud del prefijo | Máscara de subred | Máscara de red en binario | # hosts |
| --- | --- | --- | --- |
| /8 | 255.0.0.0 | 11111111.00000000.00000000.0000000 | 16.777.214 |
| /16 | 255.255.0.0 | 11111111.11111111.00000000.00000000 | 65534 |
| /24 | 255.255.255.0 | 11111111.11111111.11111111.00000000 | 254 |

Para verlo más claro, si contamos con una red privada 10.0.0.0/8 como red interna, con el límite de octeto sabemos que podemos conectar 16.777.214 hosts a la red de difusión. Esto sería lo ideal por lo que podemos subdividir la dirección al límite de /16 en dos redes (10.0.0.0/16 y 10.255.0.0/16) con cada sub red capaz de conectar 65.534 hosts.

Cuando queremos calcular  todas las subredes que podemos sacar al segmentar la red lo primero que debemos hacer es ubicar la clase de la dirección IP

```bash
192.168.0.0
```

Esta es una dirección clase C y según los datos de la tabla IP tendra una mascara de red **255.255.255.0**

Pasamos la cifra a binario:

```bash
11111111.11111111.11111111.00000000
```

Y en el último octeto cambiamos por 1 por la cantidad de subredes que queremos tener de forma exponencial.

Si queremos tener 4 subredes tendremos que agregar 2 1 ya que 2 elevado a la 1 es 2 y dos elevado a la 2 es 4, que cubrirá las subredes que necesitamos

```bash
11111111.11111111.11111111.11000000
```

255.255.255.192 esta seria la submascara con la que vamos a trabajar.

Sabemos que necesitamos 4 subredes y que irán desde la dirección 192.168.0.0 hasta la 192.168.0.255 que tendrá 256 hosts disponibles, por lo que si las dividimos entre las 4 subredes nos daría 64 hosts por subred.

De los 64 hosts tendremos 62 para asignar ya que necesitamos el host de red y el host de broadcast.

La dirección de red será la primera dirección de la subred y la dirección broadcast sera la ultima direccion.

| Subred                     | Dirección de Red | Broadcast          |
|----------------------------|------------------|-------------------|
| 192.168.0.1 - 192.168.0.62 | 192.168.0.0      | 192.168.0.63      |
| 192.168.0.65 - 192.168.0.126| 192.168.0.64    | 192.168.0.127     |
| 192.168.0.129 - 192.168.0.190| 192.168.0.128  | 192.168.0.191     |
| 192.168.0.193 - 192.168.0.254| 192.168.0.192  | 192.168.0.255     |

## Configuración manual y automática de direcciones IP

Teniendo claro que la dirección IP es la forma de identificar a un dispositivo dentro de una red. La dirección IP de un dispositivo, se puede configurar de forma dinámica/automática a través del protocolo DHCP y manual.

El protocolo de configuración dinámica de Host (DHCP) es un protocolo cliente-servidor el cual proporciona automáticamente un hosts con su dirección IP, y otra información de configuración relacionada, como la máscara de subred y la puerta de enlace predeterminada.

Este protocolo nos genera ciertas ventajas ya que este proceso esta automatizado y se administra de forma centralizada. El servidor DHCP mantiene un grupo de direcciones IP y entrega una dirección a cualquier cliente habilitado para DHCP cuando se inicia en la red. Dado que las direcciones IP son dinámicas, en lugar de estáticas (asignadas permanentemente), las direcciones que ya no estén en uso, se devuelven automáticamente al grupo para la reasignación

### Cómo activar el protocolo DHCP

#### Activar el protocolo DHCP en Windows

1. Haz clic en Inicio > Configuración > Red e Internet.
2. Haz clic en Ethernet o Wi-Fi. Selecciona Administrar y haz clic en Editar junto a Asignación de IP.
3. En editar configuración IP de red, selecciona Automática (DHCP.)
4. Haz clic en `Guardar` para activar la nueva configuración.

#### Activar el protocolo DHCP en Linux

1. Buscamos la opción editar las conexiones.
2. Nos dirigimos a la opción Ajustes de IPv4.
3. En método seleccionamos la opción DHCP.

> 💡 El método manual consta que nosotros nos encargamos de asignar la dirección IP que nos interese. Esto nos traerá ventajas ya que sabremos qué dirección tiene un dispositivo en concreto, por lo que nos evitará muchos problemas a la hora de conectarnos a él. También nos permite establecer una especie de clasificación de forma que siempre que encontremos un dispositivo en nuestra red, sepamos de qué tipo de dispositivo se trata

### Cómo configurar la IP manualmente

#### Cómo configurar la IP manualmente en Windows

1. Haz clic en Inicio > Configuración > Red e Internet.
2. Haz clic en Ethernet o Wi-Fi. Selecciona Administrar y haz clic en `Editar` junto a Asignación de IP.
3. En `Editar` configuración IP de red, selecciona `Manual`.
4. Ingresa la dirección IP de la cual se quiera usar y la demás información.
5. Haz clic en Guardar para activar la nueva configuración.

#### Cómo configurar la IP manualmente en Linux

1. Buscamos la opción editar las conexiones.
2. Nos dirigimos a la opción Ajustes de IPv4.
3. En método seleccionamos la opción `Manual`.
4. Se coloca la IP que se quiera usar y resto de los datos.
5. Selecciona `Guardar`.

>💡**Tema de discusión**
>
>¿Cual es el motivo principal por el cual la ICAAN decidió sacar el protocolo de ipV6?
>
>¿Que ventaja podemos tener al hacer una división de redes en una organización?
>
>¿Cual es la importancia de conocer la mascara de red en un proceso de división de redes?
>
