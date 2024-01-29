
## **Configuración de una máquina virtual para pentesting**

### **Cómo Instalar Kali Linux en VirtualBox 2023**

VirtualBox es una de las mejores opciones para crear entornos virtuales gracias a su compatibilidad, funciones de seguridad, funciones de red y operación. Veamos cómo instalar Kali Linux en VirtualBox

### **Descargas**

Descargar VirtualBox: [https://www.virtualbox.org/](https://www.virtualbox.org/)

![Vistual Box](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/virtual-Box.png?raw=true)

Descarga Kali Linux: [https://www.kali.org/get-kali/](https://www.kali.org/get-kali/) Si bien hay una versión para máquinas virtuales no la vamos a usar por ser muy básica y porque la gestión de disco que hace es pésima. Seleccionaremos Installer Images.

![Kali-linux](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/kali-linux.png?raw=true)

Hay varias opciones pero recomiendo INSTALLER o EVERYTHING

- INSTALLER: Se puede descargar directamente desde la flecha de descarga
- EVERYTHING. Utilizaré esta para este tutorial. Descargamos el Torrent.

![Installer](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/installer.png?raw=true)

Si no tenes un gestor de Torrent podes usar este: [https://www.utorrent.com/intl/es/downloads/win/](https://www.utorrent.com/intl/es/downloads/win/). Descargar **µTorrent** Classic.

![µTorrent](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/%C2%B5Torrent.png?raw=true)

Al instalar µTorrent Classic eviten la basura que trae, den a SKIP ALL. Lean, no sean de los que da siguiente a todo sin leer.

![Web Advisor](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/web-advisor.png?raw=true)

No queremos que inicie con Windows.

![Configuración Torrent](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/configuracion-torrent.png?raw=true)

Abrimos nuestro archivo

![Archivo Torrent](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/archivo-torrent.png?raw=true)

Agregamos y esperamos a que termine la descarga.

![Descarga](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/descarga.png?raw=true)

Dependiendo de nuestra conexión esto puede tardar desde algunos minutos (ve por un café que a la vuelta ya va a estar descargado) hasta varias horas (Ideal para dejar descargando por la noche)

![Descarga2](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/descarga2.png?raw=true)

# **Configuración inicial en VirtualBox**

Abrimos VirtualBox y creamos una nueva máquina desde el menú Máquina - Nueva

![Virtual Box](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/virtual-box.png?raw=true)

Configuramos los parámetros de la máquina virtual, en primer lugar asignamos un nombre a la máquina virtual, definimos el tipo y versión del sistema operativo a usar y establecemos la ruta donde se guardarán todos los archivos. **Elige la unidad de almacenamiento más rápida**. Muchos usuarios tendemos a instalar y ejecutar las máquinas virtuales en una unidad de almacenamiento secundaria con mayor capacidad y que suele ser un disco duro. Si puedes, haz espacio a tu SSD y utilízala en su lugar, porque la mejora de rendimiento será brutal. Por el mismo motivo, evita emplear unidades externas que -por lo general- te van a ralentizar la ejecución de las máquinas virtuales.

![Nombre y sistema operativo](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/nombre-y-sistema-operativo.png?raw=true)

**Asigna memoria RAM**. Las máquinas virtuales son devoradoras de memoria RAM. Cada máquina virtual contiene un sistema operativo completo, por lo que tienes que repartir la memoria RAM del ordenador en varios sistemas separados. Microsoft recomienda al menos 4 GB de RAM para sistemas con Windows 10/11 y lo mismo podemos decir de las distribuciones Linux actuales. Ese es el mínimo recomendado, pero si tienes hardware suficiente deberás asignar una mayor cantidad.

![Tamño de memoria](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/tama%C3%B1o-de-memoria.png?raw=true)

Creamos un nuevo disco.

![Nuevo disco duro](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/nuevo-disco-duro.png?raw=true)

Luego definimos el tipo de disco duro a usar:

![Definición de disco](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/definicion-de-disco.png?raw=true)

**Crea discos de tamaño fijo y no dinámicos**. Al crear la máquina virtual, puedes elegir entre dos tipos diferentes de discos virtuales. Por lo general, aplicaciones como VirtualBox o VMware, utilizan discos asignados dinámicamente que crecen a medida que los vas utilizando y necesitas más espacio. Sin embargo, es preferible asignar un espacio fijo desde el principio, tendrás un mayor rendimiento y menor fragmentación. Es la mejor opción a no ser que tu espacio en disco sea crítico y no te quede más remedio que emplear almacenamiento dinámico.

![Almacenamiento en disco duro física](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/almacenamiento-en-disco-duro-fisica.png?raw=true)

Definiremos la capacidad de este: 20GB iniciales para la versión installer van a estar bien o 40GB para la que traer todas las herramientas. De todos modos más adelante podemos darle más espacio.

![Ubicación de archivo](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/ubicacion-de-archivo.png?raw=true)

Damos clic en Crear para aplicar los cambios:

![Aplicar cambios](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/aplicar-cambios.png?raw=true)

General/Avanzado: Elegimos Bidireccional.

![General/Avanzado](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/general-avanzado.png?raw=true)

**Sistema/Procesador:** Asegúrate que Intel VT-x o AMD-V esté disponible y activado. Son extensiones especiales para los procesadores que mejoran su capacidad de virtualización activando la aceleración por hardware. Casi todos los procesadores de las últimas generaciones las soportan. AMD-V está activada por defecto en modelos compatibles. Con procesadores Intel es diferente y lo habitual es que el Intel VT-x venga desactivada por defecto, provocando errores a la hora de utilizar aplicaciones de virtualización. [La solución es sencilla](https://www.muycomputer.com/2015/04/14/intel-vt-x-virtualizacion/) y pasa por entrar en la BIOS del equipo o en la configuración del firmware UEFI para activar esta característica.

**Asigna más núcleos de CPU**. En máquinas virtuales el procesador sí importa, y mucho. De hecho, hace la mayor parte del trabajo. Si tienes un procesador multinúcleo, asigna los que te puedas permitir. Como con la memoria RAM, todo dependerá del número de máquinas virtuales que arranques simultáneamente y del sistema a virtualizar. Prueba con varias opciones hasta lograr el equilibrio y que no te ralentice tu sistema principal.

![Sistema](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/sistema.png?raw=true)

**Ajusta la configuración de vídeo**. Ajustar la configuración de vídeo también puede mejorar el rendimiento de tu máquina virtual y además de gestionar resolución de pantalla como haríamos en el sistema principal, debemos asegurarnos de tener habilitadas la aceleración 2D y 3D. También podemos gestionar la cantidad de memoria de vídeo dedicada.

![Pantalla](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/pantalla.png?raw=true)

Almacenamiento: Seleccionamos la ISO que descargamos

![Almacenamiento](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/almacenamiento.png?raw=true)

Añadir

![Añadir](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/a%C3%B1adir.png?raw=true)

Seleccionamos la imagen ISO de Kali Linux:

![Kali Linux](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/kali-linux.png?raw=true)

Seleccionar:

![Selector de dísco optico](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/disco-optico.png?raw=true)

Y ya tenemos montado nuestra ISO

![Obtener ISO](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/obtener-iso.png?raw=true)

En la sección Red seleccionamos el adaptador deseado, elegiremos adaptador puente:

![Sección Red](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/seccion-red.png?raw=true)

Damos clic en Aceptar para aplicar los cambios, damos clic en "Iniciar"

![Estado actual](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/estado-actual.png?raw=true)

En la pantalla de arranque de Kali Linux elegimos "Graphical install":

![Graphical install](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/graphical-install.png?raw=true)

Seleccionamos el idioma del sistema. Yo recomiendo INGLES. Pero haremos todo en español para este tutorial:

![Seleccionarl lenguaje](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/seleccionar-lenguaje.png?raw=true)

Definimos nuestra ubicación física (varia según tu país)

![Ubicación física](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/ubicacion-fisica.png?raw=true)

Confirmamos el idioma del teclado. Si eligen Ingles luego igual pueden cambiar el teclado a español:

![Idioma Teclado](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/idioma-teclado.png?raw=true)

Después de esto se completará el proceso de configuración de la máquina:

![Componentes adicionales](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/componentes-adicionales.png?raw=true)

Asignamos un nombre al equipo:

![Nombre al equipo](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/nombre-equipo.png?raw=true)

En la siguiente ventana es opcional establecer un dominio

![Establecer dominio](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/establecer-dominio.png?raw=true)

Configuramos el nombre de usuario. Damos clic en Continuar y ratificamos el nombre de usuario:

![Nombre usuario](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/nombre-usuario.png?raw=true)

Ahora asignamos la contraseña al usuario:

![Contraseña usuario](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/contraseña-usuario.png?raw=true)

Damos clic en Continuar para seguir con el proceso de configuración. Ahora definimos el tipo de particionado a usar:

![Tipo de particionado](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/tipo-de-particionado.png?raw=true)

Usamos el método automático para que el propio sistema se encargue de configurarlo:

![Método automático](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/metodo-automatico.png?raw=true)

Después de esto podemos ver la estructura que el sistema ha asignado para el tema de particionado:

![Ficheros](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/ficheros.png?raw=true)

Damos clic en “Finalizar el particionado y escribir los cambios en el disco” y debemos aplicar los cambios:

![Cambios en el disco](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/cambios-en-el-disco.png?raw=true)

Confirmamos:

![Confirmar](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/confir.png?raw=true)

Se dará paso al proceso de instalación de Kali Linux en VirtualBox:

![Instalación de Kali Linux](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/instalacion-de-kali-linux.png?raw=true)

Elegimos lo que deseamos instalar, puede elegir otro entorno gráfico, yo voy a dejar el que trae por defecto y agregaré todas las herramientas, que para eso descargamos esta edición:

![Entorno gráfico](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/entorno-grafico.png?raw=true)

Esta réplica de red es un repositorio en cualquier ubicación del mundo disponible para acceder a las utilidades de Kali Linux. Ahora configuramos el gestor de arranque GRUB:

![GRUB](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/grub.png?raw=true)

Seleccionamos la partición donde se instalará el gestor de arranque GRUB:

![Partición GRUB](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/particion-grub.png?raw=true)
Damos clic en continuar para seguir con el proceso. Al finalizar debemos reiniciar la máquina virtual:

![Máquina virtual](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/maquina-virtual-grub.png?raw=true)

Se cargará el gestor de Kali y luego iniciamos sesión en Kali Linux:

![Gestor de Kali](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/gestor-de-kali.png?raw=true)

Al maximizar la ventana esta se ajustará a este tamaño. Accede a las utilidades de Kali Linux:

![Utilidades de Kali](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/utilidades-de-kali.png?raw=true)

## **Recomendaciones**

- **Excluye directorios en el antivirus:** La solución de seguridad de tu equipo puede estar escaneando los archivos de la máquina virtual cada vez que se acceda a ellos, reduciendo el rendimiento. El antivirus no puede ver el interior de la máquina virtual para detectar virus que se ejecuten en sistema operativo invitado, por lo que esta exploración es inútil. Para acelerar las cosas, añade el directorio de la máquina virtual a la lista de exclusiones de tu antivirus.
- **Suspender en lugar de apagar:** Cuando hayas terminado de utilizar la máquina virtual, es posible que desees guardar su estado en lugar de apagarla completamente. La próxima vez que la necesites, basta hacer un doble clic para ponerla en marcha. El sistema operativo huésped se reanudará donde lo dejó en lugar de arrancar desde cero. La función es similar a la hibernación o suspensión. La aplicación guarda el contenido de la memoria de la máquina virtual en un archivo en el disco duro, para cargarla cuando lo requiera el usuario.
- **Para máquinas virtuales, mejora tu hardware:** Todo lo dicho anteriormente es una ayuda para mejorar el rendimiento de nuestras máquinas virtuales pero, no hay milagros al utilizar este recurso tecnológico. Aquí sí vale el dicho de cuanto más mejor. Como habrás visto, para que funcionen adecuadamente tenemos que cederles recursos de nuestra máquina principal. Y no pocos. Si tu hardware no es lo suficientemente potente y las utilizas, puedes bloquear por completo tu equipo en cuanto ejecutes un sistema que requiera un cierto nivel de potencia, si bien el consumo de recursos de, por ejemplo, Windows 11 o DOS es totalmente diferente.

Con estos pasos hemos aprendido a instalar Kali Linux en VirtualBox y así tener a mano un sistema vital tanto para trabajar como para nuestro laboratorio.