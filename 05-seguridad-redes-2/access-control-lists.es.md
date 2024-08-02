---
title: "Listas de control de acceso"
subtitle: "Explora el mundo de las Listas de Control de Acceso (ACLs) en redes: tipos, implementación y aplicación para una seguridad eficiente."
tags: ["redes"]
authors: ["blindma1den", "lorenagubaira"]

---

Las Listas de Control de Acceso (ACL) son herramientas para filtrar paquetes de red, fundamentales en el ámbito de la seguridad de redes, utilizadas para controlar el tráfico y proteger los recursos de la red.

Las Access Control Lists (ACL) son una funcionalidad que generalmente viene incluida en la mayoría de los dispositivos de red, como routers y switches, especialmente en equipos de fabricantes como Cisco, Juniper, HP, y otros.

## Definición y Propósito

Las ACL son conjuntos de reglas que permiten o deniegan el tráfico en una red. Se utilizan para implementar políticas de seguridad y controlar el acceso a recursos específicos.

> ⚠️ En la siguiente lectura nos enfocamos en dispositivos y sintaxis de cisco ya que son las mas populares en el mercado.

## Tipos de ACL 

Existen dos tipos principales de ACL: **estándar** y **extendida**. 

**Las ACL estándar** filtran el tráfico basándose únicamente en las direcciones IP de origen. Son menos flexibles que las ACL extendidas y generalmente se aplican cerca del destino del tráfico.
**Las ACL extendidas** Permiten un control más detallado al filtrar tráfico basándose en múltiples criterios, incluyendo direcciones IP de origen y destino, protocolos y números de puerto.

## Cómo Funcionan las ACL?

- Operación Básica: Las ACL examinan las cabeceras de los paquetes y aplican reglas para permitir o denegar el tráfico según los criterios especificados.
- Filtrado de Paquetes: Es cuando las ACL analizan los paquetes de datos y toman decisiones basadas en las reglas definidas.


## Aplicacion de control de acceso para ACL estandar

Para aplicar la ACL a una interfaz concreta, en el caso de los encaminadores de Cisco, se debe pasar a «modo de configuración de la interfaz» y aplicar el comando ip access-group. La sintaxis es:

```bash
$ router(config) # interface nombre-interface
$ router(config-if) # ip access-group N {in|out}
```

`nombre-interface` es la sintaxis propia de Cisco. Ej: «ethernet-0», 
`N` es el número que identifica la ACL que se quiere asociar a la interfaz. 
`IN` indica tráfico entrante y OUT saliente. 

En la figura. Se quiere dejar pasar hacia dentro todo el tráfico de las redes externas (más allá de la interfaz ethernet-1) excepto el que venga de la red 144.21.0.0. La ACL sería:

![Tabla de control de acceso](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/05-seguridad-en-redes-2/access-control-list/listas-de-control-de-acceso-image-1.jpg)

```bash
$ router(config)# access-list 1 deny 144.21.0.0 0.0.255.255
$ router(config)# access-list 1 permit any La segunda línea es obligatoria.
```

Si no se tiene en cuenta, funcionará la «por defecto» ya citada, que, aunque no se vea es:

```bash 
$ router(config)# access-list 1 deny any
```

Para aplicar la ACL a la interfaz ethernet-1, los comandos serían:

```bash
$ router(config)# interface ethernet-1
$ router(config-if)# ip access-group 1 in
```

Filtrando así, solamente, el tráfico entrante.

## Aplicacion de control de acceso para ACL extended

**Las ACLs de tipo extended,** comparten todas las demás características del **standard**, pero tienen una sintaxis más complicada, atendiendo a que permiten filtrar utilizando muchos otros criterios:

```bash
$ router(config)# access-list N {permit|deny} protocolo dir.IP-fuente [máscara-fuente] [op puerto-fuente] dir.IP-destino [máscara-destino] [op puerto-destino]
```

En este caso, N es un número entre 100 y 199, para indicar que es una lista extended, protocolo es la referencia al campo de número de protocolo de la cabecera IP y op puede ser:

- `lt`, indicando «menor que».
- `le`, indicando «menor o igual que».
- `gt`, indicando «mayor que».
- `ge`, indicando «mayor o igual que».
- `eq`, indicando «igual a».
- `ne`, indicando «distinto a».
- `range`, que permite expresar un rango de números.

Si lo que se busca es en la misma topología de la figura anterior, que se cumpla la siguiente política:

- No dejar entrar tráfico Telnet externo, salvo de la dirección `155.15.1.1`.
- Permitir el tráfico, del tipo que sea, de la dirección `133.11.1.3`.
- No dejar entrar tráfico general salvo de la red `144.21.0.0`.

La lista de acceso sería:

```bash
$ router(config)# access-list 101 permit ip host 133.11.1.3 any
$ router(config)# access-list 101 permit tcp 155.15.11.1 any eq 23
$ router(config)# access-list 101 permit ip 144.21.0.0 0.0.255.255 any
```

Igual que antes, la condición implícita por defecto, no permite entrar más tráfico.
