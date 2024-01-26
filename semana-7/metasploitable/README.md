
## **INSTALACIÓN DE METASPLOITABLE 2**

Metasploitable es un sistema operativo que ha sido diseñado con el objetivo de ser vulnerado con sencillez y gracias a esto poder llevar a cabo cientos de pruebas de penetración para mejorar la seguridad y prevenir ataques a corto, mediano o largo plazo.

## **Qué es Metasploitable**

Es un sistema de Linux que ha sido desarrollado con las más altas vulnerabilidades de seguridad en el cual podemos llevar a cabo todas las pruebas necesarias para perfeccionar las técnicas de seguridad o conocer cómo sacar el máximo provecho a aplicaciones diseñadas para este fin. Metasploitable no cuenta con entorno gráfico y se recomienda ser usado en redes privadas exclusivamente debido a su tolerancia a ataques. Es de código abierto y permite realizar pruebas de vulnerabilidades en archivos incrustados, atributos de archivo, permisos, etc. A continuación veremos cómo instalar Metasploitable en VirtualBox para realizar las diversas pruebas según sea la necesidad de cada uno.

**Requisitos previos**

Para esto será necesario contar con lo siguiente:

- [VIRTUALBOX](https://www.virtualbox.org/wiki/Downloads)
- [https://sourceforge.net/projects/metasploitable/files/Metasploitable2/](https://sourceforge.net/projects/metasploitable/files/Metasploitable2/)

Para iniciar el proceso podremos crear la máquina virtual en VirtualBox pulsando en el icono **Nueva** ubicado en el costado superior y en la ventana desplegada ingresaremos los siguientes valores:

![Ventana desplegada](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/ventana-desplegada.png?raw=true)

Pulsamos en **Next** y en la siguiente ventana podremos dejar el valor de la memoria RAM por defecto, 2048MB, o bien asignar un poco más si así lo deseamos.

![Memoria RAM](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/memoria-ram.png?raw=true)

Pulsamos en **Next** y en la siguiente ventana seleccionamos la opción **Crear un disco duro virtual ahora:**

![Crear disco duro](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/crear-disco-duro.png?raw=true)

Pulsamos en **Next** y en Terminar.

![Terminar](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/terminar.png?raw=true)

Ahora pulsaremos en el botón **Iniciar** para comenzar el proceso de instalación del sistema.

![Iniciar sistema](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/iniciar-sistema.png?raw=true)

Este proceso tarda alrededor de 5 minutos y veremos lo siguiente:

![Iniciar sistema2](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/iniciar-sistema2.png?raw=true)

Las credenciales de acceso son:

- **Usuario: msfadmin**
- **Contraseña: msfadmin**

![Credenciales de acceso](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/credenciales-de-acceso.png?raw=true)

De esta forma podremos usar Metasploitable con todas las pruebas necesarias.

## **Herramientas básicas necesarias para el pentesting**

El pentesting implica el uso de diversas herramientas para identificar y explotar vulnerabilidades en sistemas y redes. Los hackers utilizan una serie de herramientas para analizar los sistemas sobre los que están trabajando y de este modo, detectar las áreas más vulnerables y expuestas a posibles ataques de ciberdelincuentes. Una práctica esencial para mantener segura la red de una empresa y mantener los datos privados y sensibles a salvo de quien quiera hacerse con ellos.

### **Qué es un escáner de vulnerabilidades**

Un **escáner de vulnerabilidades** es un software diseñado para realizar análisis automáticos de cualquier aplicación, sistema o red en busca de cualquier posible vulnerabilidad que exista. Aunque estas aplicaciones no son capaces de detectar la vulnerabilidad con total precisión, sí son capaces de detectar ciertos elementos que podrían desencadenar en una vulnerabilidad, facilitando enormemente el trabajo a los investigadores e ingenieros. Hay **varios tipos de escáneres de vulnerabilidades**, autenticados, en los que se realizan pruebas y ataques potenciales desde la propia red, y no autenticados, en los que el investigador e intenta hacer pasar por un atacante simulando un ataque desde fuera para ver hasta dónde es capaz de llegar analizando (y explotando) posibles vulnerabilidades. En la red podemos encontrar una gran cantidad de escáneres de vulnerabilidades, la mayoría muy similares, pero con algunos aspectos que claramente les diferencian y les hacen mejores, o simplemente diferentes, que otros.

### **Qué características debe cumplir**

Estas herramientas, son ampliamente utilizadas por empresas y organizaciones. Esto es algo que utilizan para poder detectar posibles brechas de seguridad en los sistemas y redes. Pero para que estos sean efectivos, hay algunas características que deben poder cumplir. Estas son:

| Cobertura exhaustiva | Los escáneres de vulnerabilidades deben ser capaces de detectar una gran variedad de vulnerabilidades. Esto incluye los problemas de configuración, vulnerabilidades de software, de red y de aplicaciones. Por otro lado, debe poder reconocer las vulnerabilidades conocidas, como las no conocidas o nuevas. |
| --- | --- |
| Precisión | El analizador debe disponer de una alta precisión a la hora de identificar las vulnerabilidades. Esto quiere decir, que debe minimizar al máximo los falsos positivos, y falsos negativos. |
| Escaneos programados y automáticos | Una de las funciones más solicitadas, es la capacidad para realizar escaneos programados o de forma automática. Esto nos ayuda a mantener una visión al completo y de forma continua de la seguridad de los sistemas y redes. Así, se pueden detectar los problemas y ponerles solución antes de que sean explotados. |
| Análisis de informes y resultados | La herramienta debe tener la capacidad de crear informes detallados, los cuales muestran los resultados de los escaneos. Incluyen información sobre las vulnerabilidades identificadas, así como de sugerencias que nos permita ponerles solución. |
| Facilidad de uso | Un buen sistema de escaneo de vulnerabilidades, debe ser sencillo de utilizar y comprender. De forma que los resultados sean claros. Los administradores no se deben encontrar con dificultades a la hora de entender los informes o resultados. Así se pueden aplicar soluciones más efectivas. |
| Integración | Esta herramienta debe ser capaz de realizar una integración con las demás herramientas de seguridad. Sea el firewall o el antivirus. Esto ayudará a detectar intrusiones, y proporcionar una visión más completa de la seguridad de toda la red. |