---
title: "Adquisición en Caliente vs en Frío en el Análisis Forense Digital"
subtitle: "Métodos, herramientas y decisiones críticas al recolectar evidencia digital en sistemas encendidos o apagados"
description: "Aprende cómo y cuándo realizar adquisición de evidencia digital en caliente o en frío, sus implicancias técnicas y legales, herramientas utilizadas y mejores prácticas forenses."
tags: ["ciberseguridad", "análisis forense", "adquisición de evidencia", "live acquisition", "memoria RAM", "cadena de custodia"]
authors: ["alesanchezr"]
---


En el análisis forense digital, la adquisición de evidencia es una de las fases más críticas del proceso. De su correcta ejecución depende no solo la calidad del análisis posterior, sino también la validez legal de la información recolectada.

Existen dos grandes enfoques para adquirir evidencia digital: **Adquisición en caliente y adquisición en frío**.

Ambos métodos tienen sus propias técnicas, riesgos, beneficios y herramientas. Este artículo te enseñará en profundidad cuándo elegir uno u otro, cómo hacerlo correctamente y qué errores debes evitar. Ahora, antes que nada, pongámonos de acuerdo en algo básico pero fundamental: ¿qué es exactamente la adquisición de evidencia digital?

Imagina que te llaman para investigar un crimen cibernético. Tal vez alguien accedió sin permiso a una computadora, robó información, instaló un malware o encriptó archivos con ransomware. Tu misión es clara: entender qué pasó, cómo pasó… y, sobre todo, preservar las pruebas de forma que puedan ser analizadas e incluso presentadas ante un juez si hace falta. Ahí es donde entra en juego la **adquisición de evidencia digital**.

## ¿Qué es la adquisición de evidencia digital?

La adquisición de evidencia digital es una de las tareas más delicadas y cruciales en cualquier investigación forense informática. Consiste en copiar de manera exacta y sin modificar la información contenida en un sistema informático —como discos duros, memoria RAM, registros del sistema o archivos temporales— para su posterior análisis.

El objetivo principal no es solo acceder a la información, sino hacerlo de tal forma que:

- 🛡️ Se preserve el estado original del sistema afectado.

- 🔍 Se permita un análisis detallado posterior sin contaminar la evidencia.

- ⚖️ Se garantice la trazabilidad y validez legal, mediante una correcta cadena de custodia.

> En otras palabras: obtener una copia "intocable" que refleje exactamente cómo estaban las cosas en el momento del incidente, lista para ser analizada en un laboratorio sin riesgo de modificar el original.

Ahora bien, la forma de hacer esta adquisición depende del estado del sistema al momento del hallazgo. Aquí es donde entra la gran distinción entre:

- **Adquisición en caliente (Live Acquisition):** cuando el sistema está encendido, activo y en funcionamiento.

- **Adquisición en frío (Dead Acquisition):** cuando el sistema está apagado o se apaga de manera controlada antes de recolectar los datos.

Ambos métodos son válidos y ampliamente usados en análisis forense digital, pero cada uno conlleva ventajas, desafíos y riesgos diferentes, que es esencial comprender para elegir la estrategia adecuada en cada situación.

## Adquisición en Caliente (Live Acquisition)

La adquisición en caliente, también conocida como *live acquisition*, se refiere al proceso de recolectar evidencia digital mientras el sistema objetivo está encendido y operativo.

Este tipo de adquisición permite capturar información volátil, es decir, datos que residen en la memoria temporal del sistema y que desaparecen en el momento en que se apaga o reinicia el dispositivo. Por eso, es una técnica fundamental cuando el analista llega a un escenario en el que el incidente aún está ocurriendo o el sistema aún no ha sido manipulado.

Entre los datos volátiles más importantes que se pueden capturar se encuentran:

- Memoria RAM completa: contiene procesos, claves de cifrado, contraseñas en uso, y carga de malware.
- Procesos activos: qué está corriendo en el momento exacto, incluyendo software malicioso.
- Usuarios conectados: sesiones activas, accesos remotos.
- Conexiones de red: direcciones IP con las que el sistema está comunicándose.
- Sesiones abiertas y scripts cargados.
- Llaves de cifrado temporales, que desaparecen una vez que se apaga el sistema.

> **Nota:** una vez que apagues el sistema, toda esta información se pierde para siempre. Por eso, cuando hay evidencia crítica en ejecución, se prioriza este tipo de adquisición.


### ¿Cuándo se utiliza la adquisición en caliente?

Este método se aplica cuando:

- El sistema no puede apagarse sin poner en riesgo la pérdida de evidencia volátil.
- Se está desarrollando un incidente activo, como ransomware, ataques persistentes o exfiltración de datos en tiempo real.
- Hay indicios de actividad maliciosa en curso, como procesos sospechosos o conexiones a servidores desconocidos.
- El dispositivo es un sistema embebido o de acceso complejo (routers, móviles, IoT).


#### Ejemplos de evidencia recolectada y herramientas recomendadas

| Tipo de dato           | Herramientas sugeridas                                           |
|------------------------|------------------------------------------------------------------|
| Memoria RAM            | Volatility, Belkasoft RAM Capturer, DumpIt, WinPMEM              |
| Procesos activos       | Sysinternals Process Explorer, pslist, tasklist, ps              |
| Conexiones de red      | Wireshark, TCPView, netstat, Fiddler, CurrPorts                  |
| Usuarios conectados    | who, w, query user, net session                                  |
| Actividad reciente     | last, bash_history, RecentDocs, Prefetch, registros temporales   |

---
Estas herramientas permiten capturar la información volátil del sistema sin necesidad de apagarlo, garantizando que se preserve el estado actual de los procesos y conexiones. Por otro lado la adquisición en caliente es poderosa, pero también conlleva riesgos si no se realiza con cuidado:

1. **Alteración del estado del sistema:** cualquier acción ejecutada puede modificar archivos, memoria o registros clave.
2. **Ejecución de código en el equipo comprometido:** incluso abrir una herramienta puede cambiar valores en la RAM o generar nuevos logs.
3. **Riesgo legal:** si no se documenta adecuadamente, la evidencia puede ser impugnada por posible contaminación.

Por esta razón, solo personal capacitado debería realizar live acquisition. No es un método para improvisar.


### Buenas prácticas durante la adquisición en caliente

- Documentar cada paso desde el momento de llegada al equipo.
- Calcular hashes (MD5, SHA-256) de cualquier archivo o volcado generado.
- Usar herramientas portables desde USB forense, sin instalar nada en el sistema comprometido.
- No interactuar con software sospechoso.
- No navegar por el sistema innecesariamente.
- Evitar acciones que generen cambios como conexión a internet, instalación de programas o apertura de archivos.
- Ejecutar la menor cantidad posible de comandos o scripts.
- Por ultimo, pero no menos importante si las condiciones lo permiten, realizar primero una captura de RAM (por ser la evidencia más volátil) y luego complementa con una adquisición en frío del disco. Esta combinación proporciona una visión integral del estado del sistema.

## Adquisición en Frío (Dead Acquisition)

La adquisición en frío, también llamada *dead acquisition*, es el proceso de recolección de evidencia digital **cuando el sistema está apagado**, o tras haber sido apagado de manera controlada por el analista. A diferencia de la adquisición en caliente, esta técnica se enfoca exclusivamente en datos **no volátiles**, es decir, aquellos que permanecen almacenados de forma persistente en el dispositivo, incluso después de apagarlo. Entre los principales tipos de evidencia recolectada en este escenario se incluyen:

- Imagen forense completa del disco duro.
- Archivos del sistema y de usuario.
- Logs del sistema, de red y de eventos.
- Archivos de configuración y credenciales almacenadas.
- Artefactos de programas (historial, prefetch, registros).

El objetivo es obtener una copia exacta del contenido del disco o medio de almacenamiento, sin modificar nada, que pueda ser analizada posteriormente en un entorno controlado.


### ¿Cuándo se utiliza la adquisición en frío?

Este tipo de adquisición es ideal cuando:

- El sistema ya estaba apagado al momento de iniciar la investigación (por ejemplo, en una incautación).
- Es posible apagar el sistema sin riesgo de perder información crítica.
- Se sospecha manipulación de archivos persistentes y se requiere preservar el estado exacto del disco.
- Se está trabajando bajo requerimientos legales o judiciales estrictos.


#### Ejemplos de herramientas utilizadas

| Tipo de evidencia           | Herramientas recomendadas                       |
|-----------------------------|--------------------------------------------------|
| Imagen del disco            | FTK Imager, `dd`, Guymager                      |
| Acceso sin modificación     | Dispositivos de solo lectura (Write blockers)   |
| Formato de imagen forense   | `.E01` (EnCase), `.AFF`, `.dd`                  |

Estas herramientas permiten crear una imagen bit a bit del disco duro, garantizando que no haya alteración alguna del contenido original. El uso de bloqueadores de escritura es fundamental para proteger la integridad del medio durante el proceso.



**Ventajas**

- **Menor riesgo de alterar la evidencia**: al trabajar con el sistema apagado y utilizando herramientas especializadas, se evita la modificación involuntaria de archivos.
- **Ideal para entornos judiciales**: esta metodología es ampliamente aceptada en contextos legales, ya que ofrece garantías de integridad y reproducibilidad.
- **Permite análisis detallado y repetible**: al trabajar sobre una copia exacta del disco, los analistas pueden examinar artefactos sin temor a comprometer la evidencia original.


**Limitaciones**

- **No se capturan datos volátiles**: toda la información que estaba en memoria RAM, procesos activos o conexiones de red se pierde al apagar el sistema.
- **Se pierde contexto de ejecución**: si el equipo fue apagado abruptamente, pueden omitirse detalles importantes como sesiones activas, malware en ejecución o llaves de cifrado en memoria.

Por estas razones, cuando sea posible, se recomienda **complementar la adquisición en frío con una adquisición previa en caliente**, especialmente si el sistema estaba encendido y contenía información crítica en ejecución.

> **Nota:** La adquisición en frío es una técnica **más segura y controlada**, ideal para preservar la evidencia en investigaciones formales o análisis post-incidente. No obstante, su efectividad depende de que la evidencia relevante se encuentre en el disco y no se haya perdido información volátil clave antes del apagado.

## 🛡️ Cadena de Custodia y Validez Legal

Uno de los principios fundamentales en el análisis forense digital es garantizar que la evidencia recolectada sea **válida, íntegra y admisible legalmente**. Esto no depende solo de las herramientas utilizadas o del tipo de adquisición realizada, sino principalmente de que se haya mantenido una **cadena de custodia** rigurosa y bien documentada desde el primer momento.

La cadena de custodia es el **registro detallado del control, transferencia y manipulación de la evidencia digital**, desde que es recolectada hasta que se analiza o presenta ante una autoridad. Es esencial para demostrar que la evidencia: No fue alterada ni contaminada durante su manipulación, fue manejada exclusivamente por personal autorizado, está asociada a un procedimiento técnico confiable y es reproducible y verificable por terceros.


### Elementos clave para mantener una cadena de custodia adecuada

A continuación se detallan las acciones y precauciones que deben tomarse en cuenta, tanto en la adquisición en caliente como en frío:

1. **Registro de datos básicos del procedimiento.** Anotar de forma precisa:
   - Fecha y hora de inicio de la intervención.
   - Nombre completo y rol de las personas involucradas.
   - Ubicación física del dispositivo.
   - Estado inicial del sistema (encendido, apagado, conectado a red, etc.).

2. **Documentación exhaustiva de cada acción**. Toda acción realizada sobre el sistema o la evidencia debe quedar registrada, incluyendo:
   - Comandos ejecutados.
   - Herramientas utilizadas (versión, modo de uso).
   - Medios de almacenamiento empleados.
   - Resultados relevantes obtenidos en el momento.

3. **Uso de medios de almacenamiento seguros**  
   - Guardar los volcados de memoria, imágenes forenses y archivos recolectados en dispositivos confiables.
   - Utilizar **USBs cifrados**, discos duros externos con autenticación o almacenamiento en servidores controlados.
   - Evitar el uso de computadoras personales o medios compartidos para transportar evidencia.

4. **Cálculo y verificación de hashes**  
   Para cada imagen forense, archivo o volcado, se deben calcular:
   - Hashes criptográficos (preferentemente SHA-256, aunque también se acepta MD5).
   - Los hashes deben registrarse inmediatamente después de la adquisición y nuevamente al momento del análisis para verificar integridad.
   - Cualquier discrepancia entre los valores invalida la evidencia.

5. **Uso de formatos forenses estandarizados**  
   Siempre que sea posible, almacenar las imágenes en contenedores reconocidos y validados por la comunidad forense:
   - `.E01` (EnCase)
   - `.AFF` (Advanced Forensic Format)
   - `.dd` (raw bit-by-bit dump)

   Estos formatos permiten encapsular no solo los datos originales, sino también información adicional como metadatos, hashes y notas del proceso de adquisición.


## Comparativa: Adquisición en caliente y frío

| Característica              | Live Acquisition (en caliente)         | Dead Acquisition (en frío)                  |
|----------------------------|----------------------------------------|---------------------------------------------|
| Estado del sistema         | Encendido                              | Apagado                                     |
| Tipo de datos recolectados | Volátiles (RAM, procesos, conexiones)  | Persistentes (disco, archivos, logs)        |
| Riesgo de alteración       | Alto (requiere intervención activa)    | Bajo (con herramientas adecuadas)           |
| Valor legal                | Admisible si está bien documentado     | Más robusto para procedimientos legales     |
| Requiere experiencia       | Alta                                    | Media                                       |
| Uso típico                 | Incidentes activos, malware en memoria | Análisis post mortem, evidencia incautada   |

