## 🔎 Laboratorio

**Descubre como ver la información de tu hardware en tu computador:**

- **Para Windows:**🤓

1. Presiona en tu teclado los botones **`win + r`** e introduce en la ventana **msinfo32** para ver información interna como el procesador, versión del software y cantidad de **RAM**.

2. Presiona en tu teclado en tus botones **`win + r`** e introduce en la ventana **cmd.**
    Abrirá la terminal de Windows e introduce el comando **systeminfo**, tendrás información desde nombre del host hasta versión de BIOS
    
3. En la misma terminal ingresa el comando ***wmic memphysical get MaxCapacity***, ***MemoryDevices.*** 
    
    > El comando te devolverá la cantidad máxima de RAM que soporta la placa base y la cantidad de slot disponibles, este es un comando muy útil si planeas mejorar la memoria RAM de tu equipo. La cantidad máxima (MaxCapacity) esta expresada en Kb por lo que tendrás que dividir por 1024 para hacer la transformación a Mb y nuevamente dividir por 1024 para tener la cantidad en Gigabytes.
