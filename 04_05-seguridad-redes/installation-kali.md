## **Configuring a virtual machine for pentesting**

### **How to Install Kali Linux on VirtualBox 2023**

VirtualBox is one of the best options for creating virtual environments thanks to its compatibility, security features, networking features and operation. Let's see how to install Kali Linux on VirtualBox

### **Downloads**

Download VirtualBox: [https://www.virtualbox.org/](https://www.virtualbox.org/)

![Vistual Box](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/virtual-Box.png?raw=true)

Download Kali Linux: [https://www.kali.org/get-kali/](https://www.kali.org/get-kali/) Although there is a version for virtual machines, we are not going to use it because it is very basic and because its disk management is terrible. We will select Installer Images.

![Kali-linux](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/kali-linux.png?raw=true)

There are several options but I recommend INSTALLER or EVERYTHING.

- INSTALLER: Can be downloaded directly from the download arrow.
- EVERYTHING. I will use this one for this tutorial. We download the Torrent.

![Installer](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/installer.png?raw=true)

If you don't have a Torrent manager you can use this one: [https://www.utorrent.com/intl/es/downloads/win/](https://www.utorrent.com/intl/es/downloads/win/). Download **µTorrent** Classic.

![µTorrent](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/%C2%B5Torrent.png?raw=true)

When installing µTorrent Classic, avoid the junk that comes with it, click SKIP ALL. Read, don't be the kind of person who follows everything without reading.

![Web Advisor](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/web-advisor.png?raw=true)

We do not want it to start with Windows.

![Configuración Torrent](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/configuracion-torrent.png?raw=true)

We open our file

![Archivo Torrent](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/archivo-torrent.png?raw=true)

We add and wait for the download to finish.

![Descarga](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/descarga.png?raw=true)

Depending on our connection this can take from a few minutes (go for a coffee and it will be downloaded by the time you get back) to several hours (ideal to leave it downloading at night).

![Descarga2](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/descarga2.png?raw=true)

# **Initial configuration in VirtualBox**.

Open VirtualBox and create a new machine from the Machine - New menu.

![Virtual Box](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/virtual-box.png?raw=true)

We configure the parameters of the virtual machine, first of all we assign a name to the virtual machine, define the type and version of the operating system to use and set the path where all the files will be saved. **Choose the fastest storage drive**. Many users tend to install and run virtual machines on a secondary storage unit with greater capacity and that is usually a hard disk. If you can, make room on your SSD and use it instead, because the performance improvement will be brutal. For the same reason, avoid using external drives that will usually slow down the execution of virtual machines.

![Nombre y sistema operativo](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/nombre-y-sistema-operativo.png?raw=true)

**Allocate RAM memory**. Virtual machines are RAM memory consumers. Each virtual machine contains a complete operating system, so you have to spread the computer's RAM over several separate systems. Microsoft recommends at least 4 GB of RAM for Windows 10/11 systems and the same goes for current Linux distributions. That is the recommended minimum, but if you have enough hardware you should allocate more.

![Tamño de memoria](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/tama%C3%B1o-de-memoria.png?raw=true)

We create a new disk.

![Nuevo disco duro](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/nuevo-disco-duro.png?raw=true)

Then we define the type of hard disk to use:

![Definición de disco](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/definicion-de-disco.png?raw=true)

**Create fixed-size, non-dynamic disks**. When creating the virtual machine, you can choose between two different types of virtual disks. Generally, applications such as VirtualBox or VMware, use dynamically allocated disks that grow as you use them and need more space. However, it is preferable to allocate a fixed space from the beginning, you will have better performance and less fragmentation. This is the best option unless your disk space is critical and you have no choice but to use dynamic storage.

![Almacenamiento en disco duro física](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/almacenamiento-en-disco-duro-fisica.png?raw=true)

We will define the capacity of this one: initial 20GB for the installer version will be fine or 40GB for the one that will bring all the tools. However, we can give you more space later on.

![Ubicación de archivo](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/ubicacion-de-archivo.png?raw=true)

Click on Create to apply changes:

![Aplicar cambios](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/aplicar-cambios.png?raw=true)

General/Advanced: Choose Bidirectional.

![General/Avanzado](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/general-avanzado.png?raw=true)

**System/Processor:** Make sure Intel VT-x or AMD-V is available and enabled. These are special extensions for processors that enhance their virtualization capability by enabling hardware acceleration. Almost all processors of the latest generations support them. AMD-V is enabled by default on compatible models. With Intel processors its different and Intel VT-x is usually disabled by default, causing errors when using virtualization applications. [The solution is simple](https://www.muycomputer.com/2015/04/14/intel-vt-x-virtualizacion/) and requires entering the computer's BIOS or UEFI firmware configuration to enable this feature.

**Allocate more CPU cores**. In virtual machines the processor does matter, and a lot. In fact, it does most of the work. If you have a multi-core processor, allocate as many as you can afford. As with RAM, everything will depend on the number of virtual machines you start simultaneously and the system to virtualize. Try several options until you get the balance right and it doesn't slow down your main system.

![Sistema](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/sistema.png?raw=true)

**Adjust the video settings**. Adjusting the video settings can also improve the performance of your virtual machine and in addition to managing screen resolution as we would on the main system, we must make sure we have 2D and 3D acceleration enabled. We can also manage the amount of dedicated video memory.

![Pantalla](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/pantalla.png?raw=true)

Storage: Select the ISO that we downloaded

![Almacenamiento](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/almacenamiento.png?raw=true)

Add

![Añadir](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/a%C3%B1adir.png?raw=true)

Choose the Kali Linux ISO image:

![Kali Linux](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/kali-linux.png?raw=true)

Choose:

![Selector de dísco optico](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/disco-optico.png?raw=true)

And now we have our ISO mounted

![Obtener ISO](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/obtener-iso.png?raw=true)

In the Network section we select the desired adapter, we will choose bridge adapter:

![Sección Red](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/seccion-red.png?raw=true)
Click on OK to apply the changes, click on "Start".

![Estado actual](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/estado-actual.png?raw=true)

In the Kali Linux boot screen choose "Graphical install":

![Graphical install](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/graphical-install.png?raw=true)

Select the system language. I recommend ENGLISH. But we will do everything in Spanish for this tutorial:

![Seleccionarl lenguaje](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/seleccionar-lenguaje.png?raw=true)

We define our physical location (varies according to your country)

![Ubicación física](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/ubicacion-fisica.png?raw=true)

Confirm the keyboard language. If you choose English then you can change the keyboard to Spanish later on:

![Idioma Teclado](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/idioma-teclado.png?raw=true)

After this the machine configuration process will be completed:

![Componentes adicionales](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/componentes-adicionales.png?raw=true)

We assign a name to the machine:

![Nombre al equipo](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/nombre-equipo.png?raw=true)

In the following window it is optional to set a domain

![Establecer dominio](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/establecer-dominio.png?raw=true)

We configure the user name. Click on Continue and confirm the user name:

![Nombre usuario](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/nombre-usuario.png?raw=true)

Now we assign the password to the user:

![Contraseña usuario](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/contraseña-usuario.png?raw=true)
Click Continue to proceed with the configuration process. Now we define the type of partitioning to use:

![Tipo de particionado](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/tipo-de-particionado.png?raw=true)

We use the automatic method so that the system takes care of the configuration itself:

![Método automático](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/metodo-automatico.png?raw=true)

After this we can see the structure that the system has assigned for the partitioning issue:

![Ficheros](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/ficheros.png?raw=true)

Click on "Finish partitioning and write changes to disk" and apply the changes:

![Cambios en el disco](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/cambios-en-el-disco.png?raw=true)

Confirm:

![Confirmar](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/confirmar.png?raw=true)

This will initiate the installation process of Kali Linux on VirtualBox:

![Instalación de Kali Linux](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/instalacion-de-kali-linux.png?raw=true)

Choose what you want to install; you can select another graphical environment, but I will leave the default one and add all the tools, as we downloaded this edition for that purpose:

![Entorno gráfico](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/entorno-grafico.png?raw=true)

This network replica is a repository anywhere in the world available to access Kali Linux utilities. Now, configure the GRUB bootloader:

![GRUB](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/grub.png?raw=true)

Select the partition where the GRUB bootloader will be installed:

![Partición GRUB](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/particion-grub.png?raw=true)

Click continue to proceed with the process. Upon completion, restart the virtual machine:

![Máquina virtual](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/maquina-virtual-grub.png?raw=true)

The Kali manager will load, and then log in to Kali Linux:

![Gestor de Kali](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/gestor-de-kali.png?raw=true)

When maximizing the window, it will adjust to this size. Access Kali Linux utilities:

![Utilidades de Kali](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/utilidades-de-kali.png?raw=true)

## Recommendations

- **Exclude directories in the antivirus:** Your computer's security solution may be scanning virtual machine files every time they are accessed, reducing performance. The antivirus cannot see inside the virtual machine to detect viruses running in the guest operating system, so this scanning is useless. To speed things up, add the virtual machine directory to your antivirus exclusion list.
- **Suspend instead of shutdown:** When you're done using the virtual machine, you may want to save its state instead of shutting it down completely. The next time you need it, just double-click to start it. The guest operating system will resume where it left off instead of booting from scratch. The function is similar to hibernation or suspension. The application saves the contents of the virtual machine's memory to a file on the hard drive to load it when the user needs it.
- **For virtual machines, upgrade your hardware:** Everything mentioned above is a help to improve the performance of our virtual machines, but there are no miracles when using this technological resource. Here the saying "the more, the better" holds true. As you have seen, for them to work properly, we have to allocate resources from our main machine. And not a few. If your hardware is not powerful enough and you use them, you can completely lock your computer as soon as you run a system that requires a certain level of power, although the resource consumption of, for example, Windows 11 or DOS is completely different.

With these steps, we have learned how to install Kali Linux on VirtualBox and have a vital system at hand for both work and our laboratory.