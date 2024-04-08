# **Planificación del SGSI**

## **Identificación y evaluación de riesgos**

Cuando trabajemos dentro de un proyecto de implementación de ISO 27001 o una auditoria con este marco, es muy importante prestar mucha atención a este paso de identificación y evaluación de riesgos, ya que este proceso nos ayudara a identificar todas las potenciales amenazas que podrían afectar la seguridad de información de la organización donde nos estemos desempeñando, desde ciberataques hasta desastres naturales e incluso errores humanos.

En la identificación de amenazas tomaremos en cuenta el contexto en el que opera la organización, tanto los factores internos como los externos que pudieran influir en la seguridad de la información de la organización y partes interesadas, así como los requisitos legales, ya una vez realizado este análisis, se realizara un inventario completo de todos los activos de información de la organización, desde los datos y sistemas hasta los procesos y personal, este paso es muy importante ya que determinaremos que activos son críticos y deben protegerse con mayor énfasis.

Ya sabiendo cuales son los activos mas importantes para la organización haremos un análisis completo y detallado para identificar las amenazas que podrían explotar vulnerabilidades en los activos de información, además de valorar todas las consecuencias que podamos tener si estos riesgos se llegaran a materializar, y valorar las posibilidades reales de que este escenario pueda ocurrir.

<aside>
💡 Este paso es muy importante ya que con esta evaluación podremos aumentar la probabilidad de identificar los potenciales riesgos y asignar recursos para poder abordar los riesgos que tengamos en las áreas con mayor prioridad. Un Ejemplo que podemos tomar de una identificación y evaluación de riesgo puede ser:

</aside>

Un posible riesgo dentro de la organización es la poca cultura de seguridad dentro del personal, esto dejaría a nuestros sistemas expuestos a un ciberataque mediante phishing o Acceso no autorizado debido a una contraseña débil o compartida a terceros.

Dentro del ISO 27001 se aborda este tema estableciendo controles y procesos estructurado en la gestión de riesgos, estos procesos incluyen la realización de evaluaciones de riesgos periódicas y la implementación de controles de seguridad adecuados para así seguir con la continua de nuestro SGSI

## **Definición y aplicación de controles de seguridad**

De acuerdo al anexo A de la ISO 27701, los controles de seguridad son practicas o acciones que debe implementar y ejecutar la organización, si en los análisis y gestión de riesgos, se ha identificado amenazas susceptibles de ser prevenidas o eliminadas usando estos controles

Los controles no son de uso obligatorio, solo requiere su implementación en caso necesario de acuerdo a los riesgos que se han identificado, se sabe su gravedad y probabilidad de ocurrencia, además en su última actualización de la norma, se solicita a la organización documentar las razones por las cuales se considera necesario uno u otro control en función de los riesgos identificados.

Dentro de la ISO 27001 existen 4 tipos de controles:

### Controles organizativos

Consta de 37 controles los cuales pueden incluir políticas y procedimientos que pueden establecer la estructura de la seguridad de información en la organización. Abarcan de desde la definición de roles y responsabilidades hasta la gestión de cambios y la concienciación del personal.

Algunos controles que podemos tener son

| Controles organizativos |  |  |
| --- | --- | --- |
| 5.1 | Políticas para la seguridad de la información | Control: Se debe definir, aprobar por la dirección, publicar y comunicar a todos los empleados y partes externas relevantes las políticas de seguridad de la información y temas específicos, así como se deben revisar los cambios significativos en intervalos de tiempo planeados, en caso de que ocurran |
| 5.4 | Responsabilidades de administración | Control: La administración debe exigir que todo el personal aplique seguridad de la información de acuerdo con lo establecido en la política de seguridad de la información, políticas de temas específicos y procedimientos de la organización |
| 5.5 | Contacto con autoridades | Control: La organización debe establecer y mantener contactos con las autoridades relevantes |


### Controles de Personas

Consta de 8 controles los cuales definen la interacción del personal con los datos y entre si, y dentro de ellos pueden tratar sobre la seguridad del personal, gestión del capital humano y la formación y sensibilización. Dentro de los controles tenemos

| Controles de personas |  |  |
| --- | --- | --- |
| 6.1 | Investigación | Control: Se deben llevar a cabo verificaciones de antecedentes a todos los candidatos al empleo de acuerdo con las leyes, regulaciones relevantes y la ética, y deben ser proporcionales a los requisitos del negocio, la clasificación de la información a la que se accede y los riesgos percibidos. |
| 6.2 | Términos y condiciones del empleo | Control: Los acuerdos contractuales con los empleados deben indicar sus responsabilidades y las de la organización para la seguridad de la información. |
| 6.7 | Trabajo Remoto | Control: Se deben implementar medidas de seguridad cuando el personal está trabajando de manera remota para proteger el acceso, proceso o almacenamiento de información fuera de las instalaciones de la organización |

### Controles físicos

Constan de 14 controles y se refieren a las medidas físicas adoptadas para proteger los activos de información, incluyendo restricciones de acceso físico, sistemas de videovigilancia y protección contra desastres naturales.

| Controles físicos |  |  |
| --- | --- | --- |
| 7.1 | Perimetros de seguridad física | Control: Se deben definir y utilizar perímetros de seguridad para proteger las áreas que contienen información u otros activos asociados |
| 7.2 | Entrada física | Control: Se deben proteger las áreas seguras mediante controles de entrada apropiados y puntos de acceso |
| 7.4 | Monitoreo de seguridad física | Las instalaciones deben ser continuamente monitoreadas contra accesos físicos no autorizados. |


### Controles tecnológicos

Constan de 38 controles y engloban las medidas tecnológicas implementadas para proteger los sistemas y datos. Esto pueden incluir firewall, sistemas de detección de intrusos y encriptación de datos, algunos de los controles que están en la ISO 27001 son:

|           | Controles tecnológicos          |                |                |
| --------- | ------------------------------- | -------------- | -------------- |
| 8.1       | Dispositivos de punto final de usuario | Control: La información almacenada, procesada o disponible en dispositivos hardware de usuarios debe ser protegida. |
| 8.3       | Restricción de acceso a la información | Control: Se debe restringir el acceso a la información y activos asociados de acuerdo con lo establecido en la política del tema específico de control de acceso. |
| 8.7       | Protección contra malware      | Control: La protección contra malware debe ser implementada y apoyada por la consciencia apropiada del usuario. |


Si necesitamos aplicar controles de seguridad dentro de nuestra organización, debemos hacer la selección de que controles implementar de acuerdo a los resultados de la evaluación de riesgos para así abordar y mitigar esos mismos riesgos con los controles, es necesario que estos controles que sean seleccionados sean documentados detalladamente en las políticas de seguridad de información. Así garantizamos que la implementación de los controles sea para toda la organización.

## **Establecimiento de un plan de tratamiento de riesgos**

Una vez hayamos hecho la identificación y evaluación de los riesgos, debemos de establecer o contar con un plan para poder tratar dicho riesgo, este plan debe ser una estrategia detallada para poder abordar y gestionar los riesgos que hemos identificación de una manera efectiva. Dentro de estos planes debemos incluir una serie de acciones y medidas especificas diseñadas para reducir la probabilidad de ocurrencia o mitigar el impacto de los riesgos.

El primer paso para establecer un plan de tratamiento de riesgos es determinar si aceptamos que existe el riesgo y debemos de tratar dicho riesgo, la manera de tratar el riesgo quedara a criterio de organización y pueden ser

- Dejar de realizar la actividad o procesar la información que está expuesta al Riesgo
- Eliminar la fuente del riesgo
- Implementar un control de seguridad el cual nos ayude a reducir la probabilidad de un incidente de seguridad en relación a este riesgo
- Implementar un control de seguridad el cual nos disminuya el impacto si ocurre un incidente
- Transferir el riesgo a un tercero que tena una mayor capacidad de gestionar el riesgo

Si no hay un tratamiento de riesgo práctico disponible para la organización, o si se considera que el costo del tratamiento de riesgo es mayor que el costo del impacto, puede tomar la decisión de aceptar el riesgo. Esto debe ser aprobado por la gerencia.

En el tratamiento de este riesgo debemos contar siempre con planes y actividades los cuales pueden ser revisados y mejorados periódicamente, los cualquier pueden ser asignado a un segmento de nuestros activos de información de acuerdo a si cuenta con una posibilidad baja, media o alga de sufrir impacto a causa de una amenaza. De acuerdo a este mismo nivel de amenaza determinaremos la prioridad con la cual trataremos este riesgo.

El tener un plan de tratamiento de riesgos resulta beneficioso para nuestra organización a que nos puede proporcionar un enfoque proactivo para gestionar los riesgos de seguridad de información, y así mejorar la capacidad de recuperación y mejora de la organización frente a posibles amenazas, además de cumplir con los requisitos de la ISO 27001 para el establecimiento de un SGSI efectivo.

<aside>
📖 Un ejemplo practico de como es un plan de tratamiento de riesgo puede ser bajo el siguiente enunciado

</aside>

“Desde el servidor de comunicaciones de la organización existe una probabilidad media de perder la disponibilidad de nuestro servicio a causa de un ataque de malware”

Hemos aceptado que existe el riesgo, por lo que realizaremos un plan de tratamiento de riesgos el cual puede incluir

- Implementación de controles de seguridad como Instalación y actualización regular de software antivirus en todos los sistemas y concientización y formación al personal sobre buenas prácticas de seguridad
- Transferencia del riesgo como adquirir un seguro cibernético que cubra los costos asociados con la recuperación del sistema
- Reconocer y documentar que, a pesar de poder aplicar los controles, existe un riesgo residual de que se pueda materializar esta amenaza de malware.

## **Quiz 6. Planificación del SGSI:**

- **¿Cuántos tipos de controles de seguridad existen en la ISO 27001?**

    1. **2**
    2. **3**
    3. **4**

- **¿Cual es el primer plan en el tratamiento del riesgo?**

    1. **Aceptar que existe el riesgo**
    2. **Crear planes de tratamiento de riesgo**
    3. **Hacer pruebas a ver si el tratamiento del riesgo es correcto**
