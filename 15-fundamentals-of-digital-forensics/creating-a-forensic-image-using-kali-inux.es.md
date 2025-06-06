---
title: "Crear una Imagen Forense .E01 Usando Kali Linux"
description: "🛡️ Guía paso a paso para adquirir evidencia digital con integridad y precisión usando Kali Linux y ewfacquire."
tags: ["forense", "ciberseguridad", "kali-linux", "e01", "ewfacquire"]
author: ["alesanchezr"]
---

En el análisis forense digital, preservar la integridad de la evidencia es esencial. Por ello, la creación de una imagen forense en formato `.E01` (Expert Witness Format) es una práctica estándar para clonar discos sin alterarlos. En este artículo aprenderás paso a paso cómo crear una imagen forense desde Kali Linux usando herramientas libres y siguiendo buenas prácticas.

##  Requisitos

- Computadora con **Kali Linux**
- Disco duro de la máquina a analizar (extraído y conectado por USB o internamente)
- Acceso root o privilegios `sudo`
- Espacio libre suficiente para guardar la imagen `.E01`
- Herramienta: `libewf-tools` (incluye `ewfacquire`)

### 1. Conectar y detectar el disco

Conecta el disco sospechoso y abre una terminal y ejecuta:

```bash
sudo fdisk -l
```

### 2. Instalar la herramienta `ewfacquire`

`ewfacquire` es una herramienta de línea de comandos que forma parte del paquete `libewf-tools`. Su función es **crear una imagen forense en formato `.E01`** (Expert Witness Format), ampliamente utilizado en investigaciones digitales por su capacidad para permitir la incluisión de metadatos, calcular hashes, comprimir datos y es ampliamente aceptado en el ámbito forense.

```bash
sudo apt update
sudo apt install libewf-tools -y
```

### 3. Crear la imagen .E01

Ejecuta el siguiente comando, reemplazando `/dev/sdb` con el nombre correcto del disco:

```bash
sudo ewfacquire /dev/sdb
```

#### Datos solicitados durante la adquisición:

- Case number → `caso-001`
- Evidence number → `evidencia-01`
- Examiner name → tu nombre o ID
- Description → `Disco duro extraído de laptop sospechosa`
- Output path → `/home/kali/evidencia001.E01`

La herramienta calculará automáticamente los hashes MD5 y SHA1.

### Hashes MD5 y SHA1

Cuando realizas una copia forense, es vital asegurarte de que sea una copia exacta, bit a bit del disco original. Para verificar esto, usamos funciones hash como MD5 y SHA1. Un **hash** es como una huella digital de un archivo. Es una cadena de caracteres generada por una fórmula matemática. Si algo cambia en los datos originales (aunque sea un solo bit), el hash resultante cambia completamente.

Ejemplo, supongamos que el hash MD5 de un disco original es:

```bash
9e107d9d372bb6826bd81d3542a419d6
```

Y el hash de la imagen generada también es:

```bash
9e107d9d372bb6826bd81d3542a419d6
```

Esto significa que la copia es exacta. La imagen es válida y no ha sido alterada. Pero si los hashes no coinciden, algo falló.La imagen no es confiable como evidencia. `ewfacquire` calcula estos hashes automáticamente antes y después de copiar el disco para garantizar la integridad de la imagen.

Ahora que queda claro el tema de los hashes, continuamos con el ultimo paso.

### 4. Verificar integridad

Puedes verificar la imagen generada así:

```bash
sudo ewfverify /home/kali/evidencia001.E01
```

Si el resultado es exitoso, tu imagen está lista para ser usada en un análisis forense.

## Montar la imagen .E01

Una vez creada y verificada la imagen, es posible que desees explorar su contenido sin modificarlo. Para ello, es necesario montar la imagen. **Montar una imagen significa hacer visible su contenido en una carpeta del sistema**, como si hubieras conectado físicamente el disco original. Es decir, la imagen `.E01` se comporta como un disco real que puedes explorar.

Esto es especialmente útil en análisis forense, ya que te permite navegar entre archivos, copiar evidencia y examinar estructuras sin alterar la imagen original.

Para montar la imagen crea un directorio, montala la imagen como tal y luego navega sobre ella.
```bash
sudo mkdir /mnt/evidencia #crea un directorio
sudo ewfmount /home/kali/evidencia001.E01 /mnt/evidencia #este comando monta la imagen
cd /mnt/evidencia/ewf1 #navega en el directorio creado
ls
```

Para desmontar:

```bash
sudo umount /mnt/evidencia
```

> Recuerda que es recomendable no trabajar directamente sobre el disco original, además es importante que documentes el proceso (fechas, hashes, nombres) y que debes usar bloqueador de escritura si es posible.

Crear una imagen forense no es complicado, pero requiere atención a los detalles y hacerlo en Kali Linux que proporciona herramientas potentes y gratuitas para adquirir imágenes forenses de forma segura con herramientas como `ewfacquire`, manteniendo la integridad y confiabilidad de la evidencia digital, es un plus.
