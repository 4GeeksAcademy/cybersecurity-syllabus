### **Laboratorio 1** Escenario:

Acabas de ser contratado por la start-up D´sistemas cta para ser su administrador de sistemas, esta empresa necesita montar unos servidores para poder operar y facilitar el acceso a su información, aunque no tengas muchos conocimiento de como instalar un sistema operativo en un servidor, tu jefe decide acompañarte y explicarte en todo momento el paso a paso para la instalacion de nuestro servidor ubuntu.

1. Una vez arrancada la instalacion seleccionamos la primera opción “Try or install Ubuntu Server”

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image8.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image8.png)

1. Lo primero que configuraremos será el idioma, por lo que seleccionaremos el idioma en el que nos queramos manejar en nuestro servidor.
2. La próxima ventana nos indicará la configuración de idioma del teclado, por lo que también seleccionaremos el idioma que queramos usar en nuestro teclado.
3. En la próxima ventana nos dara a seleccionar el tipo de instalación que queremos hacer
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image9.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image9.png)
    
4. Ubuntu Server instalará una serie de paquetes que nos ayudará en el manejo de nuestro sistema operativo.
5. Ubuntu server (Minimized) es una versión más adaptable para ambientes de pruebas donde se espera algún tipo de ingreso de usuario.
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image10.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image10.png)
    
6. Seleccionaremos la primera opción.
7. El próximo paso configuramos un adaptador de red, gracias a la configuración de red de adaptador puente que hicimos previamente podemos seleccionar nuestra tarjeta de red de nuestra máquina host.
8. Luego debemos que configurar un servidor Proxy en el caso que tengamos uno disponible, de no tener podemos saltar este paso
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image11.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image11.png)
    
9. Después de la configuración de un proxy, tendremos que configurar el archivo Mirror, este es el archivo al cual nos vamos a conectar para obtener los repositorios del gestor de paquetes de archivos, ahi nos van a dar una opción por defecto la cual vamos a aceptar
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image12.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image12.png)
    
10. El próximo paso paso será configurar un disco en el que vamos a almacenar nuestro Sistema operativo, en este caso de virtualización, tendremos la opción de un disco virtual, después tendremos el resumen de las particiones del disco en el cual tendremos dos particiones, partition 1 que tendremos el grub, y la partition 2 donde tendremos nuestro Sistema operativo
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image13.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image13.png)
    
11. En la próxima ventana nos pedirá que le coloquemos los nombres a la máquina y al servidor junto a su contraseña.
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image14.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image14.png)
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image15.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image15.png)
    
12. El próximo paso nos preguntará si queremos instalar el servicio OpenSSH, recordemos que SSH es un protocolo el cual nos permitirá que podamos acceder a nuestro servidor de manera remota por lo que lo recomendable es aceptar.
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image16.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image16.png)
    
13. Seleccionaremos algunos paquetes que queramos tener en nuestro sistema operativo, estas selecciones son opcionales por lo que no aceptaremos ninguno para esta práctica.
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image17.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image17.png)
    
14. Después del último paso comienza la instalación del sistema operativo por lo que esperaremos unos minutos a que se termine una vez finalizada la instalación, seleccionamos la opción reboot now.
    
    ![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image18.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image18.png)
    

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image19.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image19.png)

#### Reflexiona

💭 Una vez terminada la instalacion tu jefe se sienta contigo y te hace ciertas preguntas saber que tanto aprendiste en este proceso.

- ¿Por que se elegio el tipo de instalacion?
- De tener un proxy para el servidor, ¿se puede agregar al momento de instalar?
- ¿Que beneficio podemos tener al instalar openssh?