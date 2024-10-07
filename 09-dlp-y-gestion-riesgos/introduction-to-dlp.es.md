# Introducción a la Prevención de Pérdida de Datos (DLP)

En 2017, la filtración de datos de Equifax expuso información personal y financiera sensible de aproximadamente 147 millones de estadounidenses. Equifax acordó un acuerdo global de hasta $425 millones para ayudar a las personas afectadas por la filtración de datos.

> La filtración de datos de Equifax fue el resultado de medidas inadecuadas de Prevención de Pérdida de Datos (DLP), entre otros fallos de seguridad.

Aunque el DLP por sí solo podría no haber evitado completamente la filtración, políticas y tecnologías de DLP robustas podrían haber mitigado significativamente el impacto o potencialmente detectado la filtración antes. He aquí por qué:

1. **Falta de Descubrimiento y Clasificación de Datos**: Un DLP efectivo comienza con saber qué datos sensibles tienes y dónde están ubicados. Equifax no logró identificar y clasificar adecuadamente todos sus datos sensibles, lo cual es un primer paso crucial en DLP.

2. **Controles de Acceso a Datos Insuficientes**: DLP implica controlar quién tiene acceso a datos sensibles. La filtración de Equifax se debió en parte a un fallo en restringir adecuadamente el acceso a sistemas y datos críticos.

3. **Monitoreo y Detección Inadecuados**: Los sistemas DLP pueden monitorear el movimiento de datos y alertar sobre actividades sospechosas. La filtración de Equifax pasó desapercibida durante meses, indicando una falta de monitoreo adecuado.

4. **Mala Encriptación de Datos**: DLP a menudo incluye la encriptación de datos sensibles. Gran parte de los datos robados de Equifax no estaban encriptados, haciéndolos fácilmente utilizables por los atacantes.

5. **Prevención Ineficaz de Exfiltración de Datos**: Las tecnologías DLP pueden prevenir que grandes cantidades de datos sean extraídas de la red. El hecho de que los atacantes pudieran exfiltrar datos durante 76 días sugiere una falta de tales controles.

Este caso subraya la importancia crítica de implementar estrategias integrales de DLP para proteger datos sensibles y detectar posibles filtraciones tempranamente.

## Definición e Importancia del DLP

La Prevención de Pérdida de Datos (DLP) es un conjunto de herramientas y procesos diseñados para detectar y prevenir el uso y transmisión no autorizados de información sensible. DLP es crucial en el panorama digital actual por varias razones:

1. **Protección de Datos Sensibles**: DLP ayuda a las organizaciones a salvaguardar su activo más valioso - la información.
2. **Cumplimiento**: Muchas industrias están sujetas a regulaciones que requieren la protección de tipos específicos de datos.
3. **Gestión de la Reputación**: Las filtraciones de datos pueden dañar severamente la reputación de una organización y la confianza del cliente.
4. **Mitigación de Amenazas Internas**: DLP puede ayudar a prevenir fugas de datos tanto accidentales como intencionales por parte de los empleados.

## Tipos de Datos Sensibles

Las organizaciones típicamente manejan varios tipos de datos sensibles, incluyendo:

1. **Información de Identificación Personal (PII)**
   - Nombres, direcciones, números de seguridad social
   - Fecha de nacimiento, números de teléfono, direcciones de correo electrónico

2. **Información Financiera**
   - Números de tarjetas de crédito, detalles de cuentas bancarias
   - Estados financieros, información fiscal

3. **Información de Salud Protegida (PHI)**
   - Registros médicos, información de prescripciones
   - Detalles de seguros, datos de pacientes

4. **Propiedad Intelectual (PI)**
   - Secretos comerciales, diseños de productos
   - Código fuente, datos de investigación

5. **Información Sensible de Negocios**
   - Planes estratégicos, detalles de fusiones y adquisiciones
   - Listas de clientes, información de precios

## Canales de Fuga de Datos

Los datos sensibles pueden filtrarse a través de varios canales:

1. **Correo Electrónico y Mensajería**
   - Enviar información sensible a destinatarios no autorizados
   - Usar cuentas de correo electrónico personales para comunicación empresarial

2. **Almacenamiento en la Nube y Compartición de Archivos**
   - Subir datos sensibles a servicios en la nube no seguros
   - Compartir archivos con permisos demasiado amplios

3. **Medios Extraíbles**
   - Copiar datos a unidades USB, discos duros externos
   - Usar dispositivos personales para almacenar datos de la empresa

4. **Impresión y Documentos Físicos**
   - Dejar documentos sensibles desatendidos
   - Eliminación inadecuada de materiales impresos

5. **Web y Redes Sociales**
   - Publicar información confidencial en sitios web públicos
   - Compartir datos sensibles en plataformas de redes sociales

6. **Tráfico de Red**
   - Transmisión de datos no encriptados
   - Ataques de hombre en el medio

7. **Dispositivos Móviles**
   - Dispositivos perdidos o robados que contienen datos sensibles
   - Uso de dispositivos personales no seguros para el trabajo
