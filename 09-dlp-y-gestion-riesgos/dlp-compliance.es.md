---
title: "Cumplimiento Normativo en la Prevención de Pérdida de Datos (DLP)"
subtitle: "🛡️ Entendiendo los aspectos clave del cumplimiento normativo en DLP para GDPR, PCI-DSS e HIPA. Implementación de controles de DLP y la gestión de excepciones y falsos positivos"
tags: ["DLP", "ciberseguridad", "prevención de pérdida de datos"]
authors: ["alesanchezr"]
---

Asegurarse de que la organización cumpla con las regulaciones es la parte más importante de la DLP. Esto es cierto porque el incumplimiento puede llevar a severas sanciones financieras, dañar la reputación de la organización o incluso sacar a la organización del negocio.

Las siguientes son las regulaciones más importantes que afectan a la DLP:

1. RGPD (Reglamento General de Protección de Datos): Se aplica a organizaciones que manejan datos personales de residentes de la UE
2. PCI-DSS (Estándar de Seguridad de Datos de la Industria de Tarjetas de Pago): Se aplica a organizaciones que manejan información de tarjetas de crédito
3. HIPAA (Ley de Portabilidad y Responsabilidad del Seguro de Salud): Se aplica a organizaciones de atención médica y sus asociados comerciales en los EE. UU.

## RGPD (Reglamento General de Protección de Datos)

Uno de los casos más famosos de sanciones financieras por infringir el RGPD es la [multa de 746 millones de euros impuesta a Amazon en julio de 2021 por la autoridad de protección de datos de Luxemburgo](https://www.reuters.com/business/retail-consumer/amazon-hit-with-886-million-eu-data-privacy-fine-2021-07-30/). Esta multa récord se emitió por presuntas violaciones del RGPD relacionadas con las prácticas publicitarias de Amazon y cómo procesaba los datos personales.

### Aspectos clave del RGPD

- Requiere que las organizaciones tengan "Licitud del tratamiento". Significa que la organización debe tener una razón válida para procesar los datos, como el consentimiento del interesado o un contrato.
- Ordena el nombramiento de un Delegado de Protección de Datos (DPO) para ciertas organizaciones, responsable de asegurar que la organización cumpla con el RGPD. El DPO no es personalmente responsable del cumplimiento de la protección de datos, pero la organización sigue siendo responsable del cumplimiento y puede enfrentar sanciones por incumplimiento.
- Requiere la implementación de medidas técnicas y organizativas apropiadas para garantizar la seguridad de los datos. Esto incluye medidas como el cifrado, el control de acceso y la minimización de datos.
- Ordena la realización de Evaluaciones de Impacto sobre la Protección de Datos (EIPD) para actividades de procesamiento de alto riesgo (como el entrenamiento de una IA). Puede ser realizado internamente o por un DPO externo.
- Requiere mantener un registro de las actividades de procesamiento. Por ejemplo: Qué datos está recopilando, cómo los está utilizando, cómo los está almacenando, cómo los está asegurando, etc.
- Requiere obtener el consentimiento explícito para el procesamiento de datos personales sensibles. Esto se conoce como "Consentimiento". Significa que el interesado debe aceptar activamente el procesamiento de sus datos.
- Requiere que las organizaciones informen sobre las violaciones de datos a las autoridades supervisoras dentro de las 72 horas. Esto se conoce como "Notificación de violación".
- Ordena la inclusión de cláusulas específicas en los contratos con los procesadores de datos. Esto se conoce como "Cláusulas Contractuales Estándar".

### PCI-DSS (Estándar de Seguridad de Datos de la Industria de Tarjetas de Pago)

Uno de los casos más notables de incumplimiento de PCI-DSS es la [violación de datos de British Airways en 2018](https://en.wikipedia.org/wiki/British_Airways_data_breach), que resultó en una multa de 20 millones de libras por parte de la Oficina del Comisionado de Información del Reino Unido (ICO). La violación expuso los datos personales y financieros de aproximadamente 429,000 clientes y personal. Aunque esta multa fue principalmente bajo el RGPD, destacó graves violaciones de PCI-DSS en las prácticas de protección de datos de la empresa.

### Requisitos clave para el cumplimiento de PCI-DSS:

1. Instalar y mantener una configuración de firewall para proteger los datos del titular de la tarjeta
2. No utilizar los valores predeterminados suministrados por el proveedor para las contraseñas del sistema y otros parámetros de seguridad
3. Proteger los datos almacenados del titular de la tarjeta mediante cifrado
4. Cifrar la transmisión de los datos del titular de la tarjeta a través de redes abiertas y públicas
5. Utilizar y actualizar regularmente el software antivirus en todos los sistemas
6. Desarrollar y mantener sistemas y aplicaciones seguros
7. Restringir el acceso a los datos del titular de la tarjeta según la necesidad de conocer
8. Asignar un ID único a cada persona con acceso informático
9. Restringir el acceso físico a los datos del titular de la tarjeta
10. Rastrear y monitorear todo el acceso a los recursos de red y datos del titular de la tarjeta
11. Probar regularmente los sistemas y procesos de seguridad
12. Mantener una política que aborde la seguridad de la información

Cada uno de estos requisitos implica sub-requisitos específicos y pautas de implementación que las organizaciones deben seguir para lograr y mantener el cumplimiento de PCI-DSS.

## HIPAA (Ley de Portabilidad y Responsabilidad del Seguro de Salud)

Uno de los casos más significativos de violación de HIPAA ocurrió en 2018 cuando Anthem Inc., una de las compañías de seguros de salud más grandes de los Estados Unidos, acordó pagar $16 millones para resolver posibles violaciones de HIPAA. Este acuerdo récord siguió a una serie de ciberataques que resultaron en la mayor violación de datos de salud en la historia de EE. UU., afectando a casi 79 millones de personas.

Para garantizar el cumplimiento de HIPAA, las organizaciones de atención médica y sus asociados comerciales deben implementar las siguientes medidas específicas:

1. Realizar evaluaciones de riesgo regulares para identificar posibles vulnerabilidades en el manejo de PHI
2. Implementar controles de acceso fuertes, incluyendo ID de usuario únicos y contraseñas fuertes
3. Cifrar toda la PHI electrónica (ePHI) en reposo y en tránsito
4. Mantener registros de auditoría detallados de todo el acceso a PHI
5. Desarrollar e implementar un plan integral de respuesta a incidentes
6. Proporcionar capacitación regular sobre HIPAA a todos los empleados que manejan PHI
7. Establecer Acuerdos de Asociado de Negocios (BAA) con todos los proveedores externos que manejan PHI
8. Implementar métodos seguros de eliminación de PHI, incluyendo la destrucción adecuada de registros electrónicos y físicos
9. Utilizar canales de comunicación seguros para transmitir PHI, como correo electrónico cifrado o portales seguros
10. Actualizar y parchear regularmente todos los sistemas y software que manejan o almacenan PHI
11. Implementar salvaguardas físicas, como gabinetes cerrados con llave y acceso restringido a áreas que contienen PHI
12. Realizar auditorías internas regulares para asegurar el cumplimiento continuo de los requisitos de HIPAA