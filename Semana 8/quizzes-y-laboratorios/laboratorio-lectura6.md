# 💡Laboratorio

**Instalacion de iptables**

**iptables** es una herramienta de firewall y filtrado de paquetes en sistemas Linux. Permite controlar y configurar las reglas de seguridad de red para proteger tu sistema y controlar el tráfico de red entrante y saliente.
Con iptables, se puede definir reglas que determinen qué paquetes de red se permiten o bloquean en tu sistema. Estas reglas se basan en criterios como la dirección IP de origen o destino, el puerto de origen o destino, el protocolo utilizado y otras características de los paquetes.
Las reglas de iptables se organizan en tablas, y cada tabla contiene cadenas de reglas. Las tablas más comunes son "filter", que se utiliza para filtrar paquetes, y "nat", que se utiliza para realizar traducción de direcciones de red (NAT).
Dentro de cada tabla, hay diferentes cadenas predefinidas, como "INPUT" para el tráfico entrante, "OUTPUT" para el tráfico saliente y "FORWARD" para el tráfico que se reenvía a través del sistema. Puedes agregar reglas a estas cadenas para especificar qué hacer con los paquetes que coinciden con esas reglas, como aceptarlos, rechazarlos o redirigirlos.

Para su instalacion debemos:

1. **Verificar si iptables está instalado**
Para verificar si iptables ya está instalado en tu sistema, puedes ejecutar el siguiente comando en la terminal:
    
    ```markdown
    iptables --version
    ```
    

> Si iptables está instalado, verás la versión del software. Si no está instalado, puedes pasar al siguiente paso.

2.  **Instalar iptables**
La forma de instalar iptables puede variar según la distribución de Linux que estés utilizando. Aquí te mostraré cómo hacerlo en algunas distribuciones populares:
- Ubuntu o Debian:

**sudo apt-get update**

**sudo apt-get install iptables**

- CentOS o RHEL:

**sudo yum install iptables**

3.  Configurar iptables
Una vez que iptables esté instalado, puedes comenzar a configurarlo según tus necesidades. iptables utiliza reglas para controlar el tráfico de red, por lo que deberás definir esas reglas.
Puedes crear un archivo de configuración para iptables utilizando un editor de texto, como nano o vi. Por ejemplo:

**sudo dnf install iptable**

Dentro de este archivo, puedes agregar las reglas que deseas aplicar. Por ejemplo, para permitir el tráfico SSH entrante, puedes agregar la siguiente regla:

**-A INPUT -p tcp --dport 22 -j ACCEPT**

4. Guardar y aplicar las reglas
Una vez que hayas definido tus reglas, guarda el archivo de configuración y sal del editor de texto.
Luego, puedes aplicar las reglas utilizando el siguiente comando:

**sudo iptables-restore < /etc/iptables/rules.v4**

Esto cargará las reglas desde el archivo de configuración y las aplicará en tu sistema.

5. Verificar las reglas
Puedes verificar las reglas de iptables utilizando el siguiente comando:

**sudo iptables -L** 

Y eso es todo! Ahora tienes iptables instalado y configurado en tu sistema.