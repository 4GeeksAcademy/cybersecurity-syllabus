---
title: "Redes en VirtualBox"
subtitle: "Conoce las posibilidades de conexión entre maquinas virtuales en VirtualBox y descubre opciones para experimentar en distintos escenarios"
tags: ["redes", "ciberseguridad"]
authors: ["arnaldoperez"]

---

## Interfaces Virtuales

En VirtualBox es una poderosa herramienta que nos permite ejecutar sistemas operativos por completo, desde la comodidad de una ventana en nuestra computadora, como si se tratase de una aplicación más. Si bien esto es muy util a la hora de explorar sistemas operativos desconocidos o experimentar con las opciones que ya conocemos, también resulta muy util a la hora de estudiar como pueden interactuar estos sistemas operativos entre si o con el resto de computadoras en nuestra red.

Ahi es donde las maquinas virtuales en VirtualBox ofrecen una variedad de interfaces que pueden agregarse a las máquinas para que interactúen de maneras particulares, dependiendo del escenario que queramos simular. Podrás crear una red interna entre tus maquinas virtuales, con o sin acceso al resto de la red, entre otras cosas.

## NAT (Network Address Translation)

NAT es un servicio, que como indican sus siglas en inglés, traduce las direcciones IP privadas en una pública que puede conectarse a internet. Esto es lo que le permite a la red de una casa u oficina, tener conexión a internet para muchos equipos con direcciones privadas, utilizando una sola dirección publica para todos. Si bien esto permite ahorrar direcciones IP, esto viene con la limitante de no poder recibir directamente conexiones espontaneas desde fuera de la red hacia uno de los dispositivos internos. Para lograr esto se debe recurrir a otras tecnologías (como los proxys) si quieren atender estas peticiones, y es por ello que las direcciones públicas son un bien muy cotizado en el ámbito de la tecnología y las redes.

Imagina que tu edificio es una red y cada apartamento en ella es como un dispositivo. NAT es como el portero del edificio. Los amigos de afuera (Internet) no pueden entrar directamente a tu departamento, pero pueden hablar con el portero. De la misma forma, cuando un habitante necesita salir, el portero le abre la puerta al exterior y lo identifica a su regreso para dejarlo entrar.

### ¿Para qué sirve NAT?

- Ahorrar direcciones IP: Hay muchas menos direcciones IP públicas que dispositivos en el mundo. NAT permite que varios dispositivos compartan una sola dirección IP pública.
- Seguridad: NAT ayuda a proteger tu red de intrusos bloqueando por defecto e acceso espontaneo a los equipos dentro de la red.
- Privacidad: NAT oculta las direcciones IP privadas de tus dispositivos a Internet.

## Conexiones en VirtualBox

Desde las ventana de configuración de una máquina virtual en VirtualBox, podemos activar hasta 4 interfaces de red. Cada una de estas interfaces puede emular un adaptador especifico y conectarse a una de las opciones disponibles.

![Interfaces de red de maquinas virtuales VirtualBox](../assets/vbox-network-interfaces.png)

### Conexión NAT

Esta interfaz usa una IP privada en tu máquina virtual, con traducción a la red del equipo anfitrión. Esto permite acceder a internet desde la computadora en VirtualBox utilizando la red del equipo anfitrión, pero sin exponer la maquina virtual a conexiones externas. Es ideal si solo quieres acceder a internet desde la maquina huésped sin mayor complicación. Es el modo por defecto de conexión.

## Redes NAT

Si ademas de conectarte a internet, también quieres comunicación entre diferentes máquinas virtuales, puedes utilizar una red NAT. Incluso puedes crear varias redes para utilizarla en distintas máquinas según sea conveniente.

Para crear redes NAT debes ir al menú `Archivo > Herramientas > Administrador de red`

![Menú administrador de red en VirtualBox](../assets/vb-menu-virtual-media.png)

Una vez ahi podrás ir a la pestaña de `Redes NAT` y crear tantas redes como necesites. Para cada una de ellas puedes configurar las direcciones IP que se utilizarán, asi como también reenvío de puertos desde la computadora del anfitrión a un invitado.

![Administrador de redes en VirtualBox](../assets/vbox-network-manager.png)

## Interfaz Puente (Bridged)

Esta conexión utilizar una de las interfaces del sistema anfitrión directamente para conectarse a la red. En este caso la maquina virtual sobrepasa las restricciones del sistema anfitrión y figura en la red como un dispositivo mas. Es una opción util si se desea prestar un servicio desde un servidor virtual hacia el resto de la red.

## Red Interna

Esta es una red virtual que permite conectar de forma privada a un grupo de máquinas virtuales. Esta red oculta a las maquines huéspedes de toda la red y las aplicaciones del sistema anfitrión.

## Red Solo Anfitrión (Host Only)

Es parecido a una red interna en lo que respecta a que se trata de una conexion privada entre maquinas virtuales, pero con la excepcion de que el sistema anfitrón tiene acceso a la red. En el caso de anfitrión se instala una interfaz virtual que se conectará junto a las demás maquinas virtuales en ésta red. Por defecto esta red esta aislada de la red externa, asi que de necesitarse este tipo de conexiones se deben recurrir a técnicas adicionales como conexciones puente o NAT.

Las redes "solo-anfitrión" también deben crearse en la ventana del administrador de redes de VirtualBox y se encuentran en la pestaña junto a las "Redes Nat". En las interfaces de tu ordenador podrás ver la interfaz que se conecta a red como un adaptador más en tu sistema.

![Adaptador solo-anfitrion de VirtualBox](../assets/vbox-host-only-network-adapter.png)

## Versatilidad en VirtualBox

Con estas opciones podemos simular distintos escenarios en VirtualBox, desde un data center con varios servidores virtuales que reciben conexiones externas, hasta una simple arquitectura cliente-servidor con una máquina para cada rol. La limitante mas relevante es la capacidad de tu computador para ejecutar varias máquinas virtuales, fuera de esto es mas que suficiente para tener un buen laboratorio virtual en tu computador.