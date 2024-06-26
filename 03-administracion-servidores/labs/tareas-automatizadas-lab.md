## **Laboratorio Automatización de tareas**

Como administrador de servidores te asignaron la tarea de crear una copia de seguridad para un archivo, esta copia de seguridad se debe generar diariamente, por lo que es una tarea que puede ser algo repetitiva y tediosa.
Recuerdas que en tu formación como analista de seguridad aprendiste sobre la automatización de tareas con Cron, por lo que decides usarlo en esta oportunidad

1. El primer paso es listar las tareas cron que tienes activas en tu sistema con el comando **`crobtab -l`**

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image96.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image96.png)

> 👉 En el resultado puedes ver que no hay tareas configuradas

1. Antes de crear la tarea, nos damos cuenta que crear un script que nos cree la copia de seguridad nos facilitara mucho más el trabajo, por lo que creamos un script en python que se vera asi.

![administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image97.png](administracionDeServidores-parte1%20ab5924e8fe3644549acdf70f4425a531/image97.png)

1. Una vez escrito el script procedemos a crear la cronjob con el comando `crontab -e`
2. Dentro del archivo creamos la tarea asignando que se ejecute todos los dias a la media noche `0 0 * * *`  y el comando el cual seria un cambio de directorio a scripts (donde queremos guardar la copia de seguridad) y ejecutando el comando python y guardamos el archivo.
3. Revisamos los logs de la cron job ingresando el comando: **`cat /var/log/syslog | grep “auto_copiaSeg.py`**