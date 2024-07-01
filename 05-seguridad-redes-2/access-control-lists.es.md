---
title: "Listas de control de acceso"
subtitle: "Explora el mundo de las Listas de Control de Acceso (ACLs) en redes: tipos, implementación y aplicación para una seguridad eficiente."
tags: ["redes"]
authors: ["blindma1den", "lorenagubaira"]

---

# **Access Control Lists**

Muchas implementaciones de filtros de paquetes las incorporan directamente. los encaminadores Cisco incorporan dicho filtrado restrictivo por defecto en sus listas de control de acceso o ACLs (*Access Control Lists*).

> Las ACL de los encaminadores Cisco son de dos tipos: standard y extended.
> 
> 
> **Las ACLs de tipo *standard*** están compuestas de una serie de reglas ordenadas (ACE o Access control entry), cada una de las cuales solo usan, como criterio, la dirección IP origen del mensaje, y tienen una sintaxis:
> 
> router(config)# access-list N {permit|deny} dirección-IP-origen [máscara]
> 
> Recordar estas reglas para *standard y extended*:
> 
1. Al final de todas las reglas existe una más (que no pone el administrador) implícita, que deniega el resto del tráfico, que no coincide con alguna de las reglas de la ACL. Es la condición de «todo lo demás negado por defecto».
2. Hay una serie de «palabras clave» que se pueden utilizar para hacer las reglas más legibles. Por ejemplo, en lugar de 144.21.13.12 0.0.0.0, se puede escribir host 144.21.13.12, o en lugar de escribir 0.0.0.0 0.0.0.0, se puede escribir any.
3. El comando access-list solo sirve para construir la ACL, pero no la aplica a ninguna interfaz. Para ello, existe otro comando diferente.

## **Aplicacion de control de acceso**

Para aplicar la ACL a una interfaz concreta, en el caso de los encaminadores de Cisco, se debe pasar a «modo de configuración de la interfaz» y aplicar el comando ip access-group. La sintaxis es:

> router(config)# interface nombre-interface
> 
> 
> **router(config-if)#** ip access-group N {in|out}
> 

nombre-interface es la sintaxis propia de Cisco. Ej: «ethernet-0», N es el número que identifica la ACL que se quiere asociar a la interfaz. IN indica tráfico entrante y OUT saliente. En la figura. Se quiere dejar pasar hacia dentro todo el tráfico de las redes externas (más allá de la interfaz ethernet-1) excepto el que venga de la red 144.21.0.0. La ACL sería:

![Tabla de control de acceso](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/05-seguridad-en-redes-2/access-control-list/listas-de-control-de-acceso-image-1.jpg)

> router(config)# access-list 1 deny 144.21.0.0 0.0.255.255
> 
> 
> **router(config)#** access-list 1 permit any La segunda línea es obligatoria. Si no se tiene en cuenta, funcionará la «por defecto» ya citada, que, aunque no se vea es:
> 
> access-list 1 deny any
> 

Para aplicar la ACL a la interfaz ethernet-1, los comandos serían:

> router(config)# interface ethernet-1
> 
> 
> router(config-if)# ip access-group 1 in
> 

Filtrando así, solamente, el tráfico entrante.

## **Las ACLs de tipo extended**

**Las ACLs de tipo extended,** comparten todas las demás características del standa*rd*, pero tienen una sintaxis más complicada, atendiendo a que permiten filtrar utilizando muchos otros criterios:

**router(config)#** access-list N {permit|deny} protocolo dir.IP-fuente [máscara-fuente] [op puerto-fuente] dir.IP-destino [máscara-destino] [op puerto-destino]

En este caso, N es un número entre 100 y 199, para indicar que es una lista extended, protocolo es la referencia al campo de número de protocolo de la cabecera IP y op puede ser:

- lt, indicando «menor que».
- le, indicando «menor o igual que».
- gt, indicando «mayor que».
- ge, indicando «mayor o igual que».
- eq, indicando «igual a».
- ne, indicando «distinto a».
- range, que permite expresar un rango de números.

Si lo que se busca es en la misma topología de la figura anterior, que se cumpla la siguiente política:

- No dejar entrar tráfico Telnet externo, salvo de la dirección 155.15.1.1.
- Permitir el tráfico, del tipo que sea, de la dirección 133.11.1.3.
- No dejar entrar tráfico general salvo de la red 144.21.0.0.

La lista de acceso sería:

> router(config)# access-list 101 permit ip host 133.11.1.3 any
> 
> 
> **router(config)#** access-list 101 permit tcp 155.15.11.1 any eq 23
> 
> **router(config)#** access-list 101 permit ip 144.21.0.0 0.0.255.255 any
> 

igual que antes, la condición implícita por defecto, no permite entrar más tráfico.
