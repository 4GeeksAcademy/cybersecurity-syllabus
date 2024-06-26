---
title: "Programación de tareas automatizadas"
subtitle: "Automatización eficiente: Configura cron en Linux para optimizar tareas repetitivas y asegurar la estabilidad del servidor. Aprende paso a paso."
tags: ["servidores"]
authors: ["blindma1den", "lorenagubaira"]

---

## **Uso de cron para programar tareas**

Cron es una herramienta muy útil en sistemas operativos Linux que permite programar tareas para que se ejecuten automáticamente en momentos específicos. Con cron, puedes automatizar tareas repetitivas, como realizar copias de seguridad, actualizar bases de datos, enviar informes por correo electrónico y mucho más.

La configuración de tareas en cron se realiza a través de archivos llamados "crontabs". Cada usuario puede tener su propio crontab, que contiene las tareas programadas para ese usuario en particular. Para editar el crontab de un usuario, puedes utilizar el comando `crontab -e`.

El formato de un crontab consta de cinco campos separados por espacios: minutos, horas, día del mes, mes y día de la semana. Puedes utilizar números o asteriscos (*) para indicar todos los valores posibles en un campo. Por ejemplo, si deseas que una tarea se ejecute todos los días a las 8:00 a.m., puedes configurar el crontab de la siguiente manera: "0 8 * * * comando".

Además de los valores numéricos, también puedes utilizar expresiones especiales en los campos de tiempo. Por ejemplo, "@daily" se traduce en "0 0 * * *", lo que significa que la tarea se ejecutará todos los días a la medianoche. Otras expresiones útiles incluyen "@hourly", "@weekly" y "@monthly".

Estas expresiones se traducen de esta manera:

@reboot: Ejecuta una vez y nada más iniciarse el equipo.

1. @yearly: ejecuta sólo una vez al año: 0 0 1 1 *
2. @monthly: ejecuta una vez al mes y el primer día: 0 0 1 * *
3. @weekly: todas las semanas, el primer minuto de la primera hora de la semana: 0 0 * * 0.
4. @daily: todos los días a las 12 de la noche: 0 0 * * *
5. @midnight: Tiene el mismo efecto que el anterior.
6. @hourly: todas las horas durante su primer minuto: 0 * * * *

También podemos utilizar algunos modificadores, que son algunos caracteres especiales los cuales nos dan mucho más poder de crear nuevas reglas. Lo cual aumenta las posibilidades para poder crear procesos mucho más complejos, y como tal más precisos. Estos son:

1. : Tiene el mismo significado que asignar todos los valores.
2. ,: Nos da un listado de valores.
3. : Establece un rango de valores.
4. /: Significa «cada».
5. rango / excep: Crea excepciones en la regla.

> ⚠️ Es importante tener en cuenta que las tareas programadas en cron se ejecutan en el contexto del usuario que las programó. Por lo tanto, asegúrate de que el usuario tenga los permisos adecuados para realizar las tareas programadas.

Además, es recomendable redirigir la salida de las tareas programadas a archivos de registro para poder verificar su ejecución y detectar posibles errores. Puedes hacer esto agregando ">> ruta_del_archivo" al final de la línea de comando en el crontab.

Para listar las tareas programadas en un crontab, puedes utilizar el comando "crontab -l". Si deseas eliminar todas las tareas programadas de un crontab, puedes utilizar el comando "crontab -r".

Esto nos ayudará a programar tareas que pueden resultar repetitivas, por lo cual los administradores de sistema pueden estar pendientes de otras cosas. Estos proporcionan una forma muy eficiente de programar la ejecución de diferentes scripts, comandos y también programas. Debido al alto grado de personalización, podremos programar prácticamente lo que sea necesario y sea beneficioso para la organización y las tareas que se realizan en su entorno.

Estos sistemas ofrecen varias ventajas a nivel empresarial. La primera es la que comentamos, la capacidad de programar esas tareas más tediosas para que no sea necesaria la intervención manual. Lo cual ahorra tiempo, y reduce el riesgo de que aparezcan posibles errores relacionados con errores humanos. Algunos de los métodos más comunes son para copias de seguridad, actualizaciones de software, generar informes o la ejecución de procesos de mantenimiento. Pero a todo esto también le sumamos la flexibilidad para la programación. Todos los beneficios que hemos visto previamente de cron y crontab, los tendremos disponibles a nivel empresarial. Por lo cual las opciones para crear este tipo de automatizaciones son muy abundantes.

## **Creación y edición de archivos crontab**

La creación y edición de archivos crontab es una tarea común en sistemas Unix y Linux para programar tareas que se ejecutarán automáticamente en momentos específicos. Un archivo crontab contiene las instrucciones para el cron daemon sobre qué tareas ejecutar y cuándo hacerlo.

Para crear o editar un archivo crontab, puedes utilizar el comando "crontab -e". Esto abrirá el archivo crontab en el editor de texto predeterminado del sistema, como vi o nano. Si es la primera vez que utilizas "crontab -e", se te pedirá que elijas un editor.

El archivo crontab tiene un formato específico que consta de cinco campos separados por espacios: minutos, horas, día del mes, mes y día de la semana. Cada campo acepta valores numéricos o caracteres especiales. Por ejemplo, si deseas que una tarea se ejecute todos los días a las 8:00 a.m., puedes agregar la siguiente línea al archivo crontab:

**Copy**

`0 8 * * * comando`

En esta línea, "0" representa los minutos (en este caso, 0), "8" representa las horas (8:00 a.m.), y los asteriscos (*indican que cualquier valor es válido para los campos restantes.

Además de los valores numéricos, también puedes utilizar expresiones especiales en los campos de tiempo. Por ejemplo, "@daily" se traduce en "0 0 * * *", lo que significa que la tarea se ejecutará todos los días a la medianoche. Otras expresiones útiles incluyen "@hourly", "@weekly" y "@monthly".

Después de especificar el tiempo, debes agregar el comando que deseas ejecutar. Puede ser cualquier comando válido en el sistema, como un script, un programa o una secuencia de comandos. Asegúrate de proporcionar la ruta completa del comando si es necesario.

Es importante tener en cuenta que cada línea en el archivo crontab representa una tarea programada. Puedes agregar múltiples líneas para programar varias tareas. Cada línea debe terminar con un salto de línea.

Una vez que hayas terminado de editar el archivo crontab, guarda los cambios y cierra el editor. El cron daemon se encargará de leer y ejecutar las tareas programadas según lo especificado en el archivo crontab.

Para listar las tareas programadas en un archivo crontab, puedes utilizar el comando "crontab -l". Si deseas eliminar todas las tareas programadas de un archivo crontab, puedes utilizar el comando `crontab -r`.

Recuerda que las tareas programadas en un archivo crontab se ejecutan en el contexto del usuario que las programó. Asegúrate de que el usuario tenga los permisos adecuados para realizar las tareas programadas.

## **Monitoreo y verificación de tareas programadas**

El monitoreo y la verificación de tareas programadas son aspectos importantes en la administración de sistemas para asegurarse de que las tareas se estén ejecutando correctamente y en los momentos deseados. Esto te permite detectar y solucionar problemas potenciales, así como garantizar la eficiencia y confiabilidad del sistema.

Una forma común de monitorear las tareas programadas es revisar los registros o logs generados por el sistema. Los registros de cron, por ejemplo, proporcionan información detallada sobre la ejecución de las tareas programadas. Puedes encontrar estos registros en el directorio "/var/log" con nombres como "cron.log" o "syslog".

Para verificar si una tarea programada se ha ejecutado correctamente, puedes revisar el registro correspondiente y buscar mensajes de éxito o errores. Si encuentras algún error, es importante investigar y solucionar la causa subyacente. Puedes utilizar herramientas como "grep" o "awk" para buscar eventos específicos en los registros.

Además de los registros, también puedes recibir notificaciones por correo electrónico sobre el estado de las tareas programadas. Puedes configurar el comando o script que se ejecuta como tarea programada para enviar un correo electrónico de notificación al finalizar. Esto te permite recibir actualizaciones en tiempo real sobre el estado de las tareas y tomar medidas rápidas si es necesario.

Otra opción es utilizar herramientas de monitoreo de sistemas más avanzados, como Nagios, Zabbix o Prometheus. Estas herramientas te permiten monitorear y verificar las tareas programadas, así como otros aspectos del sistema, como el rendimiento, la disponibilidad y la utilización de recursos. Puedes configurar alertas y recibir notificaciones cuando se detecten problemas con las tareas programadas.

> ⚠️ Es importante establecer una rutina de monitoreo regular para verificar el estado de las tareas programadas. Puedes programar revisiones diarias, semanales o mensuales, según la importancia y la frecuencia de las tareas. Esto te ayudará a identificar problemas de manera oportuna y garantizar que las tareas se estén ejecutando según lo planeado.

</aside>