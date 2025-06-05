# Cómo crear una imagen forense `.E01` desde un disco físico o virtual (en Windows)

En el análisis forense digital, una imagen `.E01` permite capturar el contenido completo de un disco duro sin alterar el original. Este archivo puede contener metadatos, fragmentarse en partes más pequeñas y verificarse automáticamente mediante hashes. A continuación, se explican dos formas de generar una imagen `.E01`: una desde un disco duro conectado físicamente al equipo, y otra desde un archivo de máquina virtual.


## Creación de imagen desde un disco duro conectado al equipo (desde Windows)

Supongamos que un disco duro fue retirado de una computadora sospechosa. El analista lo conecta a su equipo mediante un adaptador SATA-USB o una carcasa externa. El objetivo es realizar una copia bit a bit de ese disco sin modificarlo.

Para ello, se utilizará **FTK Imager**, una herramienta gratuita que permite capturar discos y generar imágenes forenses en formato `.E01`.

### Pasos:

1. Descarga e instalá [FTK Imager](https://www.exterro.com/ftk-imager).
2. Abre el programa como administrador.
3. En el menú superior, selecciona -> `File → Create Disk Image...`

![create-disk-image]()

4. Elige la opción `Physical Drive`. Aparecerá una lista de discos conectados. Selecciona el disco externo (verifica que no sea tu disco del sistema).
5. Completa los campos del caso (por ejemplo: número de caso, nombre del perito, descripción del análisis). Pueden dejarse en blanco si es una práctica.

6. En tipo de imagen, seleccioná `E01 (Expert Witness Format)`.
7. Elegí una carpeta de destino donde guardar la imagen.
8. En opciones de configuración:
   - **Compresión**: poné el valor `1` (rápido).
   - **Fragmentación**: usá `1500 MB` para dividir la imagen en partes más manejables.
   - Activá la casilla "Verify images after they are created".
9. Presioná `Start` para comenzar la adquisición.

Al finalizar, obtendrás una serie de archivos `.E01`, `.E02`, etc., junto con un archivo `.txt` que documenta los hashes generados y los detalles del caso.

---

## Creación de imagen desde una máquina virtual (archivo `.vdi` o `.vmdk`)

Cuando se trabaja con máquinas virtuales, no se dispone de un disco físico, sino de un archivo que lo representa. En VirtualBox este archivo tiene extensión `.vdi`; en VMware, `.vmdk`. El contenido de estos archivos también puede analizarse forensemente, pero primero es necesario convertirlos.

### Paso 1: Convertir el archivo de máquina virtual a `.raw`

El formato `.raw` es una copia directa del contenido del disco virtual. Para obtenerlo, se usa la herramienta `qemu-img`.

1. Descargá QEMU para Windows desde [qemu.weilnetz.de](https://qemu.weilnetz.de/w64/).
2. Extraé o instalá QEMU y ubicá el archivo `qemu-img.exe`.
3. Abrí la terminal (CMD o PowerShell) y ejecutá el comando correspondiente según tu tipo de disco:

Para VirtualBox:
```bash
qemu-img convert -f vdi -O raw "C:\ruta\al\archivo.vdi" "C:\salida\imagen.raw"
```

Para VMware:
```bash
qemu-img convert -f vmdk -O raw "C:\ruta\al\archivo.vmdk" "C:\salida\imagen.raw"
```

---

### Paso 2: Convertir `.raw` a `.E01` con FTK Imager

1. Abrí FTK Imager como administrador.
2. En el menú, seleccioná:

   `File → Create Disk Image...`

3. Seleccioná el tipo de fuente:

   `Image File`

4. Seleccioná el archivo `.raw` como fuente.
5. En el tipo de imagen de salida, seleccioná:

   `E01`

6. Completá los metadatos del caso.
7. Elegí carpeta de destino, nombre del archivo, compresión y fragmentación.
8. Presioná **Finish**, luego **Start** para comenzar la creación de la imagen.

---

## Resultado esperado

FTK Imager generará:

- Archivos segmentados: `.E01`, `.E02`, `.E03`, etc.
- Un archivo `.txt` con el hash de verificación y los metadatos del caso

Estos archivos pueden analizarse directamente con herramientas como **Autopsy** o volver a cargarse en FTK Imager para explorarlos.

Es importante conservar todos los archivos juntos en una misma carpeta y no modificar sus nombres si se desea mantener la integridad de la evidencia.
