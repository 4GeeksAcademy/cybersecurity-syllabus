---
title: "Políticas y Controles de DLP"
subtitle: "🛡️ Entendiendo los aspectos clave del diseño de políticas efectivas de DLP, la implementación de controles de DLP y la gestión de excepciones y falsos positivos"
tags: ["DLP", "ciberseguridad", "prevención de pérdida de datos"]
authors: ["alesanchezr"]
---

# Políticas y Controles de DLP

Después de definir las estrategias y tecnologías utilizadas para implementar DLP, necesitamos aplicarlas con políticas y controles. Esta lección cubrirá los aspectos clave del diseño de políticas efectivas de DLP, la implementación de controles de DLP y la gestión de excepciones y falsos positivos.

## Diseño de Políticas Efectivas

Las políticas efectivas de DLP son la base de una estrategia robusta de protección de datos. Aquí hay algunas consideraciones clave al diseñar políticas de DLP:

1. **Clasificación de Datos**: Define y categoriza claramente los tipos de datos sensibles (por ejemplo, PII, datos financieros, propiedad intelectual). Por ejemplo:

    - **PII (Información de Identificación Personal)**: Esto incluye cualquier información que pueda identificar a un individuo, como nombre, número de seguridad social, fecha de nacimiento y otros datos similares.
    - **Datos Financieros**: Esto incluye cualquier dato relacionado con transacciones financieras, como números de cuenta bancaria, información de tarjetas de crédito y detalles de pago.
    - **Propiedad Intelectual**: Esto incluye cualquier dato relacionado con la información propietaria de la empresa, como secretos comerciales, patentes y derechos de autor.

2. **Evaluación de Riesgos**: Identifica los riesgos potenciales y vulnerabilidades asociadas con cada tipo de dato. Por ejemplo:

    - **PII**: Los riesgos incluyen robo de identidad, fraude financiero y violaciones de privacidad. Las vulnerabilidades pueden incluir controles de acceso débiles, almacenamiento o transmisión sin cifrar y ataques de ingeniería social dirigidos a empleados con acceso a PII.

    - **Datos Financieros**: Los riesgos potenciales incluyen robo financiero, uso de información privilegiada y manipulación del mercado. Las vulnerabilidades podrían incluir cifrado insuficiente, segregación inadecuada de funciones en sistemas financieros y pasarelas de pago comprometidas.

    - **Propiedad Intelectual**: Los riesgos incluyen pérdida de ventaja competitiva, pérdida de ingresos y daño a la reputación de la empresa. Las vulnerabilidades podrían incluir controles de acceso inadecuados, prácticas inseguras de compartición de archivos e intentos de espionaje industrial.

3. **Cumplimiento Regulatorio**: Asegúrate de que las políticas se alineen con las regulaciones relevantes (por ejemplo, GDPR, HIPAA, PCI-DSS). Por ejemplo:

    - **GDPR**: Requiere que las organizaciones informen sobre violaciones de datos a las autoridades relevantes dentro de las 72 horas.

    - **HIPAA**: Exige el uso de identificación única de usuario para todas las personas que acceden a información de salud protegida electrónica (ePHI), como asignar un nombre de usuario o número único para identificar y rastrear la identidad del usuario.

    - **PCI-DSS**: Las organizaciones deben instalar y mantener una configuración de firewall para proteger los datos de los titulares de tarjetas. PCI-DSS también requiere que las organizaciones cifren la transmisión de datos de titulares de tarjetas a través de redes abiertas y públicas utilizando criptografía fuerte. Además, exige que las organizaciones restrinjan el acceso a los datos de los titulares de tarjetas según la necesidad de conocer y asignen un ID único a cada persona con acceso a computadoras.

4. **Concienciación del Usuario**: Desarrolla políticas que sean fáciles de entender y seguir para todos los empleados.

    - **Claridad**: La política debe estar escrita en un lenguaje claro y conciso que sea fácil de entender.
    - **Consistencia**: La política debe aplicarse de manera consistente a todos los empleados.
    - **Comunicación**: La política debe comunicarse a todos los empleados de manera clara y concisa.
    - **Capacitación**: La política debe estar respaldada por capacitación y educación para todos los empleados.
    - **Aplicación**: La política debe aplicarse de manera consistente y justa.
    - **Revisión**: La política debe revisarse y actualizarse regularmente.

5. **Escalabilidad**: Diseña políticas que puedan adaptarse al crecimiento y las necesidades cambiantes de la organización:

    - **Flexibilidad**: La política debe ser lo suficientemente flexible para adaptarse al crecimiento y las necesidades cambiantes de la organización.
    - **Modularidad**: La política debe ser lo suficientemente modular para adaptarse a las necesidades de la organización.
    - **Exhaustividad**: La política debe ser lo suficientemente exhaustiva para cubrir todos los aspectos de las operaciones de la organización.
    - **Exhaustividad**: La política debe ser lo suficientemente exhaustiva para cubrir todos los aspectos de las operaciones de la organización.

6. **Revisión Regular**: Establece un proceso para la revisión y actualización periódica de políticas. Por ejemplo, una política debe revisarse y actualizarse cada tres años.

## Gestión de Excepciones y Falsos Positivos

Incluso los sistemas de DLP bien diseñados pueden generar falsos positivos o requerir excepciones. La gestión efectiva de estos problemas es crucial:

1. **Manejo de Excepciones**: Desarrolla un proceso para revisar y aprobar excepciones a las políticas. Por ejemplo:

    - **Revisión**: La excepción debe ser revisada y aprobada por el gerente de DLP.
    - **Documentación**: La excepción debe documentarse en la política de DLP.
    - **Comunicación**: La excepción debe comunicarse a todos los empleados de manera clara y concisa.
    - **Capacitación**: La excepción debe estar respaldada por capacitación y educación para todos los empleados.
    - **Aplicación**: La excepción debe aplicarse de manera consistente y justa.
    - **Revisión**: La excepción debe revisarse y actualizarse regularmente.

2. **Reducción de Falsos Positivos**: Cada vez que se detecta un falso positivo, el sistema de DLP debe ajustarse para minimizar la probabilidad de falsos positivos similares en el futuro. Por ejemplo, si un sistema de DLP marca un correo electrónico legítimo como sospechoso, la política que activa el sistema de DLP debe ajustarse para evitar marcar correos electrónicos legítimos en el futuro.
