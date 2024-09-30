---
title: "Solución de problemas de red"
subtitle: "Domina la resolución de problemas de la red: herramientas de diagnóstico, identificación de problemas, resolución y monitoreo de eventos para un rendimiento óptimo."
tags: ["redes"]
authors: ["blindma1den", "lorenagubaira"]

---

A veces podemos tener problemas de rendimiento en nuestra red y es necesario saber la razón para así poder tomar los correctivos. Para ello tenemos herramientas que pueden realizar un diagnóstico de red.

Un diagnóstico de red es el procedimiento que realizamos para determinar e inspeccionar todo lo que está sucediendo dentro de nuestra red.

Para ello se aplican diferentes herramientas que nos permitirán detectar posibles fallos o errores en los registros, asimismo eliminarlos y corregir las desviaciones.

Gracias a un diagnóstico de red podemos lograr aumentar la velocidad de conexión a Internet, podemos verificar cuántas direcciones IP se conectan a nuestra red, podemos controlar también porque algún nodo no se puede conectar con facilidad y por sobre todas las cosas con un diagnóstico de red podemos saber qué nivel de seguridad tiene la misma.

Para realizar un análisis de red lo que necesitamos es conocer la estructura, el diseño y el grado de implementación que tiene la misma. Para ello tenemos que recabar datos y conceptos que existen en la red, cuando es una red pequeña este paso lo podemos realizar rápidamente pero cuando nos encontramos con redes de una buena cantidad de nodos es recomendable realizarlo con mucha cautela a este punto.

Lo primero que haremos es conocer a los usuarios y demás personas intervinientes en la red. Posteriormente nos dedicaremos a la estructura física con su diagrama de hardware teórico y real.

Nos enfocaremos en la capa 1, 2 y 3 del modelo de las 7 capas de redes.

Para poder conseguir un buen resultado en esta etapa realizaremos un inventario de todo el cableado, conectores, disponibilidad de electricidad cercana, determinaremos también la cantidad de fibra óptica o ADSL, y analizaremos el tendido que tienen los demás cables que trabajan para la conexión de Internet.

Conociendo los puntos de entrada y los cables, nos dirigiremos al tráfico de la información, estudiando los diferentes protocolos que existen en la red y así poder definir la calidad del servicio que están brindando.

Ya teniendo todos estos datos, tendremos que confirmar e identificar la seguridad que tiene la red con respecto a la navegación por Internet a través de firewall y de otros dispositivos de seguridad tanto en hardware como en software.

## **Identificación de y resolución de problemas comunes**

Cuando sabemos que algo funciona mal en nuestra red lo primero que tendremos que hacer es enfocarnos directamente en nuestro dispositivo.

Para ello es recomendable apagarlo o reiniciarlo y comprobar si sigue existiendo el problema.

Si esto no se soluciona tendremos que verificar la parte del hardware de nuestra red, analizaremos las conexiones de cables entre nuestro router y los dispositivos, si es que tenemos una red LAN, verificaremos el estado de los conectores como así también el estado en general de todos los componentes externos.

En el caso de Windows, cuenta con su propia herramienta de diagnóstico de red la cual podemos conseguir en “red e internet” y buscamos la opción “Solucionador de problemas de red”. También podemos conseguir herramientas como Uptrends Uptime Monitor y Wifi Explorer

Entre los problemas más comunes que podemos conseguir en nuestra red podemos conseguir:

- **Red Lenta**

Puede haber muchas razones por las que una red que proporcionaba un rendimiento adecuado en el pasado ahora frustra a los usuarios. Un puerto de conmutación o un enlace que falla puede hacer que el tráfico se dirija alrededor del fallo y sobrecargue otro enlace.

Otro problema de velocidad de la red podría surgir si los empleados deciden descargar videos de alta definición mientras están en el trabajo porque la descarga en la oficina es más rápida que si utilizan su conexión a internet en casa

> 💡 Esto lo podríamos resolver con una herramienta de monitorización de la red.

- **Problemas de conectividad física**

Una conexión de red puede interrumpirse repentinamente por problemas de conectividad física, este problema es común cuando un cable de red se daña o se suelta. Es posible que en el momento que se añadan o se quiten cables en un conmutador uno de los otros cables se desconecten accidentalmente.

- **Búsqueda DNS lentas**

El DNS hace coincidir el nombre común utilizado para emparejar los nombres de servidores o servicios con la dirección de internet que enruta una solicitud de red. En el caso de los nombres más utilizados, es probable que la coincidencia ya esté almacenada en la caché DNS del sistema, y la búsqueda es rápida. En el caso de los nombres menos utilizados, la coincidencia puede estar almacenada en una caché más lejana, como el servidor raíz del nombre de primer nivel, como .com, .org

Cada servidor DNS a lo largo de la ruta comprueba su caché antes de hacer una petición al siguiente servidor a lo largo de la ruta. El siguiente servidor comprueba entonces su caché, repitiendo el proceso. Si la búsqueda es lenta, puede haber un enlace lento en la ruta o un servidor lento o sobrecargado. Para solucionar este problema, el administrador de la red local puede reconfigurar los routers locales para desplazar las peticiones a una cadena de servidores más rápida.

- **Direcciones IP duplicadas y estáticas**

En una red, no hay dos sistemas que puedan compartir la misma dirección de internet. Si hay direcciones de internet duplicadas, ninguno de los dos sistemas puede acceder a la red de forma fiable. Las direcciones de la mayoría de los dispositivos de red se asignan cuando el Protocolo de Configuración Dinámica de Host (DHCP) arranca los sistemas de la red local. DHCP mantiene un conjunto de direcciones asignadas a la red local, asignando una dirección diferente del conjunto a cada sistema.

A las estaciones de trabajo no se les asignan direcciones permanentes, sino que reciben una por un tiempo limitado de DHCP. Los sistemas vuelven a solicitarla antes de que se agote el tiempo y suelen recibir la misma dirección. Si el sistema se apaga sin volver a solicitarla y el tiempo se agota, pierde esta dirección y puede recibir una diferente al arrancar.

## **Monitoreo de red y registro de eventos**

Otra herramienta que nos ayudará a corregir las fallas en nuestra red es el monitoreo de eventos, Solemos llamar a las actividades de los usuarios en la red eventos, y este nos genera información sobre eventos individuales o hacer un seguimiento de las tendencias de los eventos para identificar rápidamente un comportamiento anormal, una de las funciones de realizar este monitoreo es garantizar la seguridad y proteger los datos de la compañía.

Entre los datos que podemos hacerle seguimiento tenemos:

- Inicios de sesión.
- Cierres de sesión.
- Cargas de páginas web.
- Llamadas de la interfaz de programación de aplicaciones (API).

Todos estos eventos se pueden almacenar en un archivo de registro de eventos, y está disponible para su visualización y descarga después de 24 horas.

**Otros usos que le podemos dar al monitoreo de eventos:**

- Monitorear la pérdida de datos: En algunos casos como que un ex empleado se vaya con la competencia, si no hemos eliminado su usuario del sistema podría acceder a su cuenta y obtener información de la empresa, por lo que con el monitoreo de eventos se podría descubrir esas actividades
- Optimizar el desempeño: En ocasiones es difícil determinar la causa del bajo rendimiento de la red y el monitoreo de evento puede determinar si la causa está relacionado con un problema de la red o con alguna otra razón.

>💪 **Desafío:**
>
>Realiza  prueba en tu computadora del monitoreo de eventos y revisa todos los eventos que han ocurrido en tu sesión. A continuación, describe los eventos que te parecen más importantes a nivel corporativo.
