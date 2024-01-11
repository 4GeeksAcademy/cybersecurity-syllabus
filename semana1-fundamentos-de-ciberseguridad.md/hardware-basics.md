# Lectura 2 📕: Fundamentos de hardware

To learn more about the basic components of a computer we must first know what a computer is.

A computer is a programmable digital electronic machine that executes a series of commands to process input data, obtaining information that is then sent to the output units. A computer is composed of many different integrated circuits and various support, extension and accessory elements, which together can execute various tasks very quickly and under the control of a program.

A computer is composed of two basic aspects: the **hardware** which are the parts and components of the computer and the **software** which are all the programs and systems that the computer has.

We can see the hardware as a box where a series of devices and components that process input and output information are connected, while the software is the set of instructions to execute that input and output information. Without the software instructions, the computer would be a box without utility, just as the human body would be without a brain.

## Hardware Parts 💻

Computer hardware is divided into: **Internal Hardware** and **External Hardware.** Below we will explain each of them and how they are composed.

### Internal hardware:

- **Baseboard or Motherboard**.

It is the main board of any computer system to which all other devices are connected, both directly (such as interconnected electrical circuits) and indirectly (through USB ports or other types of connectors). It has a basic software called BIOS that allows it to perform and synchronize its basic functions (such as data transmission, power management and recognition of the physical connection of other external components).

- **Processor**.

This is the Central Processing Unit (**CPU**), i.e. the brain of the computer, that controls everything that runs the computer and is responsible for performing calculations and understanding data. There are several types of CPUs that differ, among other things, in their speed for processing information. This speed is measured in a frequency unit called Hertz (Hz) and the faster the speed achieved by the processor, the faster the computer's performance. Currently, the two main CPU brands are AMD and Intel.

- Internal RAM

It is the memory that stores information, temporarily and quickly, so that the computer can use it at the moment. Its storage capacity is measured in units called *gigabytes *****(**GB**). The larger the amount of RAM, the faster the computer can run. For example, to open and use several programs at once. The contents of the RAM memory are deleted as soon as the computer is turned off because it does not store data (files, videos, programs, etc.), but retains information about the actions being performed with that data. It does not store the file or the program itself, but the information to execute it.

The ram memories can be DDR2, DDR3, DDR4 and DDR5 and will depend on the type of ram slots or ports that the motherboard has.

- Internal Memory ROM

It is the memory that stores information permanently and is called "read-only", that is, the user cannot alter the content once the information is stored, it can only be installed or uninstalled. ROM memory stores everything related to instructions or what is also called **BIOS** (basic system or boot program), which includes instructions on how to start the machine or how programs work, among others.

- Graphics processing unit (GPU)**.

Also known as **graphics card** or **video card** is an internal hardware device that connects to the motherboard and allows the computer to display images on the monitor.  There are two types of GPUs:

1. **Integrated GPU - T**also called "integrated graphics", refers to the fact that the CPU and graphics card share the same random access memory. This means that all the tasks to be executed in the system, together with those of a graphical nature, are supported by the same RAM.
2. **Dedicated graphics cards -** Also called "discrete", are those that have a separate RAM that is exclusively used by the GPU. This memory is called VRAM and the more memory the video card has, the more visual tasks it can run at the same time.

- **Sound card**.

It is an internal hardware device that connects to the motherboard and is classified according to the channels it uses. For example: stereo, quadraphonic (surround sound), MIDI (professional use connector), among others. The main function of the board is to allow the computer to reproduce sounds through speakers or headphones. It also receives sounds from the user through the connection of a microphone.

- Secondary storage device

It is the memory that stores data permanently (or until the user deletes it), such as documents, spreadsheets, images, videos, audios, backups of files, among others. These are stored data that the computer does not need immediately or quickly for its operation, but are used directly by the user. There are two types of secondary storage devices: internal (the hard disk drive) and external (external hard disk, memory card, pendrive, CD ROM, etc.).

![Internal Hardware](../assets/hardware-interno.png)

### External hardware:

- **Input devices**

They are parts that receive raw data and that the computer can process through its software. They are divided into two categories:

1. manual input devices that must be operated by the user (keyboard, mouse, touch screen, touch screen, microphone, etc.) and 2.
2. Automatic input devices, which trigger the input of information on their own, independent of the user (magnetic stripe reader, PIN and chip reader, bar code reader, etc.).

- Output devices

These are parts that send out the data processed by the computer. There are two types: **temporary output** such as the monitor, which constantly updates the output image on the screen, and **permanent output** such as a printer, which reproduces information on a piece of paper that lasts as a hard copy.

- Storage devices

These are devices that allow the recording of information that is generally found in RAM, and that both the user and the operating system have at their disposal for their daily work and operation. We can consider this type of storage as non-volatile, that is, both programs and data do not disappear, even when the computer is turned off. This means that the user can save his programs and information with the certainty that they will not be deleted even when the computer is not turned on.

Currently there are several devices used for computer data storage, entre ellos tenemos:

1. **Disco Duro:**

Un **disco duro** o **disco rígido** es un dispositivo de almacenamiento de datos no volátil que emplea un sistema de grabación magnética para almacenar datos digitales de forma rápida y segura. Es decir, para almacenar datos se utilizan únicamente dos valores representados por 0 y 1 como código binario . Un *bit* es la unidad mínima y elemental utilizada para almacenar información en los discos duros. Como es una unidad muy pequeña se suele utilizar el byte que equivale a 8 bits.

Físicamente un disco duro se compone de uno o más discos (también conocidos como platos) rígidos generalmente de aluminio y recubiertos de una capa de material magnetizable, unidos por un mismo eje que gira a gran velocidad dentro de una caja metálica sellada. Sobre cada plato, y en cada una de sus caras, se sitúa un cabezal de lectura/escritura que flota sobre una delgada lámina de aire generada por la rotación de los discos. En un disco duro magnético la información se guarda en sectores de disco en formato binario organizado por bloques. Por lo tanto, se usa como unidad básica de almacenamiento de información los bytes junto a un prefijo de cantidad. Se ha establecido como acuerdo general la utilización de una **b** para indicar bits, y una **B** para indicar bytes.

Entre los discos duros podemos conseguir:

**1.1** Disco duro Rigido (Hard drive disk o HDD) modelo de 3.5” , con formato de conexión sata y una velocidad de transmisión cercana de datos a 80 MB/s en operaciones de lectura y a 60 MB/s en escritura.

**1.2** Discos duro Solido (Solid State drive o SSD) modelo de 2.5”, con formato de conexión sata y una velocidad de transmisión de datos cercana a 250 MB/s en lectura y a 230 MB/s en escritura de datos.

**1.3** Disco duro Solido M2, modelos de tamaño reducido de 22mm, con un formato de conexión con el bus PCIe 4.0, con una velocidad de transmisión de hasta 10gbps

2. **Memoria Flash:**

El almacenamiento flash es una tecnología de almacenamiento de datos basada en una memoria de alta velocidad que se programa eléctricamente. La velocidad del almacenamiento flash es lo que le dio el nombre: escribe datos y realiza operaciones de entradas y salidas aleatorias a la velocidad del flash.

El almacenamiento flash utiliza un tipo de memoria no volátil que se denomina “**memoria flash**”. La memoria no volátil no requiere alimentación para mantener la integridad de los datos almacenados con lo que, si se interrumpe el suministro, no se pierde nada. Dicho de otro modo, la memoria no volátil no olvida los datos que ha almacenado cuando el disco se desconecta.

Generalmente conseguimos los dispositivos de almacenamiento flash en memorias USB (Universal Serial bus), hoy en contamos con distintos formatos de usb:

- USB 2.0 entre 240 mb/s a 480 mb/s, y los reconocemos por ser de color negro.

- USB 3.0 preparado para recibir 640 mb/s y lo reconocemos por ser de color azul.

- **Dispositivos periféricos**

Es un dispositivo independiente, conectado externa o internamente a la tarjeta madre, que permite al sistema informático realizar una función extra. Como tal, no forma parte del proceso central de una computadora, sino que sirve a nivel de complemento para aumentar sus capacidades funcionales.

![Hardware Externo](../assets/hardware-externo.png)

Existen 5 tipos de periféricos de computadora:

| Periféricos de entrada | Aquellos que permiten el ingreso de datos desde el exterior. Ejemplos: mouse, teclado, micrófono y escáner. |
| --- | --- |
| Periféricos de salida | Proyectan la información desde el interior de un sistema informático hacia el exterior. La información proyectada es, por lo general, en formato auditivo, visual o impreso. Ejemplos: pantalla, impresora, altavoces y tarjeta gráfica. |
| Periféricos de entrada/salida (E/S) | Son los dispositivos que pueden tanto recibir como emitir información. Es decir, a diferencia de un periférico de entrada o salida, los dispositivos de E/S pueden cumplir con ambas funciones (recepción y emisión), no limitándose únicamente a una. Ejemplos: pantalla táctil, impresora multifuncional, casco de realidad virtual y módem. |
| Periféricos de comunicación | Elementos físicos que permiten la conexión entre dos o más dispositivos. Ejemplos: tarjeta de red, hub USB, módem, fax y conmutador de red. |

## Arquitectura de computadoras

La arquitectura de la computadora se refiere a una serie de ideas similares dentro de los campos de la informática y la tecnología. A nivel de **software**, se refiere a los sistemas de lenguaje ensamblador que conectan las diversas partes del hardware de la computadora en un solo sistema en funcionamiento. Cuando se trata de **hardware**, se aplica igualmente a los métodos de creación y utilización de hardware y al proceso de construcción de componentes informáticos. Cada una de estas definiciones describe un proceso similar, la idea de comenzar con un sistema informático que no funciona y hacerlo funcional, pero todas miran el proceso desde un punto de vista diferente. En otras palabras, el concepto de arquitectura de computadora se refiere a la integración de su estructura física con su estructura lógica.

La arquitectura de los ordenadores es importante en el sentido de que determina cómo funcionará un ordenador y para qué se puede utilizar. Determina el rendimiento, el consumo de energía, el tamaño y el coste del ordenador.

Una arquitectura de ordenador puede ser una combinación entre hardware y software, o sólo una de las dos. Una arquitectura de hardware es la implementación de la lógica de un ordenador, mientras que la arquitectura de software es la implementación de la funcionalidad de un ordenador. Sin embargo, la arquitectura de software depende en gran medida de la arquitectura de hardware.

### Arquitectura de ordenadores y arquitectura de software

Los términos arquitectura de computadoras y arquitectura de software no son lo mismo y tienen significados totalmente diferentes. Mientras que la arquitectura de los ordenadores es la lógica que dirige un dispositivo físico, la arquitectura del software es la lógica que dirige la funcionalidad de un dispositivo.

Entre los componentes principales de la arquitectura tenemos

1. CPU o procesador.
2. Bus.
3. Memoria principal (Memoria Ram).
4. Sistema de entrada y salida.

> 👉 Existen distintos tipos de arquitectura de datos, entre los cuales contamos con:

| Arquitectura de flujo de datos | Es una arquitectura paralela en la que los datos pasan por las diferentes etapas del cálculo. En esta arquitectura, el resultado de un cálculo se utiliza como entrada para otro cálculo. |
| --- | --- |
| Arquitectura von Neumann | La arquitectura von Neumann es una arquitectura secuencial en la que el cálculo se ejecuta secuencialmente. El cálculo se realiza en un orden secuencial. Esta arquitectura tiene una unidad central de procesamiento (CPU), una memoria y dispositivos de entrada-salida. |
| Arquitectura Harvard | Esta arquitectura es una versión modificada de la arquitectura von Neumann. Tiene dos memorias separadas: una para las instrucciones del programa y otra para los datos. |
| Arquitectura Harvard modificada | Es una combinación de la arquitectura de flujo de datos y la arquitectura Harvard. En esta arquitectura, hay una memoria de programa y una memoria de datos. |

### 💪 **Ejercicio**

Haz una lista con las caracteristicas de la PC que te gustaria armar o no todas las tarjetas madres son compatibles con todos los procesadores, asi que investiga cual es la tarjeta madre ideal para el procesador que te gustaria tener, la cantidad de RAM, el tipo de disco de almacenamiento y si en su arqutectura tambien incluye una tarjeta de video.
