---
title: "Introducción al ENS (Esquema Nacional de Seguridad)"
subtitle: "🛡️ Comprendiendo los fundamentos del Esquema Nacional de Seguridad, su importancia en la gestión de la seguridad de la información, y el proceso de certificación."
tags: ["ENS", "ciberseguridad"]
authors: ["alesanchezr"]

---


> 🇪🇸 Si no vas a trabajar en 🇪🇸 España, este tema te será irrelevante y puedes saltarte todo el modulo. Alternativas al ENS en otros países: NIST Cybersecurity Framework 🇺🇸, [ISO 27001](https://4geeks.com/es/lesson/introduccion-a-iso-27001) 🌎, IT-Grundschutz 🇩🇪, NERC CIP 🇺🇸, CERC 🇨🇦, NIS Directive 🇪🇺, CNSSI 1253 🇨🇳.

En algunos casos durante nuestra carrera como analistas de ciberseguridad en 🇪🇸 España, tendremos que realizar auditorías a algún sistema de un organismo público que se rige bajo el ENS, por lo que es necesario tener conocimiento sobre esto.

Entre los temas que estaremos tratando de ENS tendremos los marcos de trabajo, las medidas de protección, y los análisis de riesgos así como ciertas herramientas que nos ayudarán a la implementación del esquema, si más nada que decir entremos en el tema.

# Introducción al ENS (Esquema Nacional de Seguridad) 🛡️🇪🇸

El Esquema Nacional de Seguridad (ENS) es una normativa o conjunto de políticas y directrices cuidadosamente diseñadas para anticipar, prevenir y responder a los desafíos en el área de ciberseguridad. Este marco regulatorio fue establecido por el gobierno español para **garantizar la seguridad de los sistemas de información utilizados por las administraciones públicas**. El ENS es fundamental para proteger la información y los servicios que manejan las entidades gubernamentales. 🏛️💻

## Regulación y Finalidad del ENS

El Esquema Nacional de Seguridad (ENS) es un marco normativo establecido en el Real Decreto 311/2022, que tiene como finalidad garantizar la protección de la información en el sector público y en entidades privadas que gestionan servicios tecnológicos para administraciones públicas. El ENS es de **obligado cumplimiento** para:

- Todas las **Administraciones Públicas** españolas.
- **Empresas privadas** que presten servicios tecnológicos o gestionen sistemas públicos bajo contrato.

El cumplimiento del ENS es, por tanto, esencial tanto en entornos gubernamentales como en colaboraciones público-privadas.

## Objetivos del ENS 

Los principales objetivos del ENS son:

1. Crear las condiciones necesarias para la confianza en el uso de los medios electrónicos. 
2. Promover la gestión continuada de la seguridad. 
3. Proporcionar un lenguaje común para la interacción entre administraciones en materia de seguridad. 🗣️
4. Establecer reglas, medidas y requisitos mínimos de seguridad para las entidades públicas.

## Principios básicos 📊

El ENS se basa en los siguientes principios:

- **Seguridad integral:** La seguridad debe ser abordada desde una perspectiva global. No basta con proteger solo los sistemas tecnológicos, sino que debe abarcar: Infraestructura física, procesos internos, información en papel y digital, personas (usuarios, administradores, terceros) y servicios externos o subcontratados.

    El enfoque integral garantiza que ninguna parte del ecosistema quede desprotegida o aislada de las políticas de seguridad.

- **Gestión de riesgos:** Todas las decisiones de seguridad deben basarse en un análisis sistemático de riesgos. Esto implica: Identificar amenazas y vulnerabilidades, evaluar el impacto potencial, estimar la probabilidad de ocurrencia y aplicar medidas proporcionales para mitigarlos.

    Este principio promueve una gestión proactiva y racional, evitando inversiones innecesarias o decisiones reactivas mal fundamentadas.

- **Prevención, detección, respuesta y recuperación:** La seguridad debe contemplar todo el ciclo de vida de un incidente. Se deben implementar mecanismos para prevenir amenazas, detectar actividades anómalas, responder adecuadamente ante incidentes y recuperar la operatividad.

    Este enfoque garantiza la resiliencia de los sistemas y reduce el impacto de los ataques.

- **Reevaluación periódica:** Las medidas de seguridad deben revisarse con regularidad para asegurar su vigencia y eficacia. Esto incluye evaluar los cambios tecnológicos, organizativos y normativos que puedan afectar al sistema.

    La revisión periódica permite adaptar la protección a las nuevas circunstancias y evitar obsolescencia.

- **Función diferenciada:** Es necesario separar claramente las funciones de seguridad dentro de la organización. Se debe distinguir entre responsables de la información, del servicio, de la seguridad, y de la operación técnica.

    Esta división de responsabilidades evita conflictos de interés y facilita el control y la rendición de cuentas.

- **Mejora continua:** La seguridad no es un estado estático, sino un proceso en evolución. Las organizaciones deben aprender de sus errores, revisar procedimientos y adoptar buenas prácticas de forma constante.

    Este principio refuerza la madurez y la eficiencia del sistema de gestión de seguridad.

- **Cumplimiento normativo:** Todas las medidas deben alinearse con las leyes y regulaciones vigentes. Esto incluye normativas como el RGPD, legislación sectorial, y otras disposiciones aplicables.

    El cumplimiento normativo asegura la legalidad de las actuaciones y la protección de derechos fundamentales.

- **Responsabilidad y compromiso:** La seguridad es responsabilidad de todos los miembros de la organización, no solo del personal técnico. La alta dirección debe liderar el compromiso institucional y los usuarios deben ser conscientes de su papel en la protección de la información.

    Este principio fortalece la cultura organizacional en torno a la seguridad.


## Clasificación y niveles de medidas de seguridad

El Real Decreto 311/2022 establece **73 medidas de seguridad**, clasificadas en:

- **Marco organizativo**: 16 medidas  
- **Marco operacional**: 31 medidas  
- **Medidas de protección**: 26 medidas

Cada medida tiene tres niveles de aplicación:

- **BASE** (obligatorio)  
- **Reforzado**  
- **Alto**

Los niveles permiten adaptar la exigencia de seguridad según la categoría del sistema (baja, media o alta criticidad), de acuerdo con lo establecido en la Guía CCN-STIC 808.

## Perfil de cumplimiento

El **perfil de cumplimiento** es un concepto introducido por el Real Decreto 311/2022 como mecanismo para **adaptar las medidas de seguridad del ENS a la realidad de cada organización**, permitiendo así una aplicación **proporcional, eficaz y sostenible**. Este enfoque reconoce que no todas las entidades tienen las mismas capacidades ni enfrentan los mismos riesgos. Por ello, el perfil de cumplimiento considera los siguientes factores:

- **La criticidad de los sistemas:** Es decir, la importancia que tiene un determinado sistema o servicio para la continuidad operativa, la protección de datos sensibles o la prestación de servicios esenciales. Un sistema crítico requerirá medidas más exigentes.

- **El nivel de madurez en ciberseguridad:** Evalúa la capacidad organizativa y técnica para gestionar adecuadamente la seguridad de la información. Las entidades más maduras pueden abordar medidas avanzadas, mientras que otras podrán escalar gradualmente.

- **Los recursos disponibles:** Incluye el personal cualificado, presupuesto, infraestructura tecnológica y herramientas disponibles. El ENS reconoce la necesidad de adecuar la carga de cumplimiento a la capacidad real de cada organización.

El perfil de cumplimiento se plasma en la **declaración de aplicabilidad** y en el **plan de adecuación**, que determinan cómo, cuándo y con qué profundidad se implementarán las medidas exigidas. Este mecanismo busca evitar la aplicación rígida y homogénea de los controles, permitiendo un ENS más **realista, flexible y orientado al riesgo**, sin menoscabar la seguridad.


## Implementación y cumplimiento

Para cumplir con las obligaciones establecidas por el ENS, las organizaciones deben seguir un **proceso estructurado** que asegure la implementación eficaz y verificable de las medidas de seguridad. Este proceso consta de las siguientes fases:

1. **Análisis de riesgos:** Identificación y evaluación de los riesgos que amenazan la seguridad de la información y los servicios. Es la base para seleccionar las medidas adecuadas y definir su nivel de exigencia (BASE, Reforzado o Alto).

2. **Declaración de aplicabilidad:** Documento en el que se identifican las medidas del ENS aplicables a la organización, indicando su nivel de implementación según el perfil de cumplimiento. Debe estar debidamente justificada.

3. **Plan de adecuación:** Documento estratégico que establece las actividades, recursos y plazos necesarios para alcanzar el cumplimiento. Prioriza acciones en función del riesgo y la criticidad de los sistemas.

4. **Implementación de medidas:** Ejecución del plan de adecuación, lo cual puede incluir la adopción de políticas, configuraciones técnicas, procedimientos, formación del personal y auditoría interna.

5. **Auditorías periódicas:** Evaluaciones internas o externas que verifican el grado de cumplimiento y la eficacia de las medidas. Son obligatorias y permiten detectar desviaciones y oportunidades de mejora.

> 🕓 De acuerdo con la disposición transitoria del Real Decreto 311/2022, las entidades disponían de un **plazo de 24 meses desde abril de 2022** para adaptarse al nuevo ENS. Este periodo de transición concluyó en **abril de 2024**, por lo que **el cumplimiento es ya exigible en su totalidad**.

## Certificación del ENS

La **certificación del Esquema Nacional de Seguridad (ENS)** es un proceso formal mediante el cual una organización acredita que cumple con los requisitos de seguridad establecidos en el Real Decreto 311/2022. Esta certificación no solo verifica el cumplimiento legal, sino que también constituye una herramienta clave para **mejorar la confianza institucional, facilitar la transparencia y acreditar la madurez en ciberseguridad** ante terceros.

### ¿Quién puede certificarse?

- **Organismos de la Administración Pública** (AGE, CCAA, Entidades Locales)
- **Empresas privadas** que presten servicios tecnológicos a las AAPP
- **Proveedores tecnológicos** en procesos de licitación pública que requieran estar alineados con el ENS

> El ENS permite certificar tanto organizaciones completas como sistemas de información concretos (por ejemplo, una aplicación crítica, una infraestructura determinada, etc.).

El proceso habitual de certificación ENS comprende las siguientes etapas:

1. **Autoevaluación interna:**  
   La organización realiza una revisión interna de su grado de cumplimiento del ENS. Identifica brechas, elabora la declaración de aplicabilidad y define su perfil de cumplimiento.

2. **Auditoría por una entidad acreditada:**  
   Una empresa certificadora reconocida por ENAC (Entidad Nacional de Acreditación) evalúa el sistema de información o la organización. La auditoría verifica la implementación de las medidas según lo declarado.

3. **Informe de conformidad:**  
   Si la auditoría es satisfactoria, se emite un informe que justifica que el sistema cumple con los requisitos del ENS en el nivel correspondiente.

4. **Emisión del certificado por el CCN:**  
   El Centro Criptológico Nacional (CCN), como autoridad competente, aprueba el informe y emite el certificado de conformidad.

### Niveles de certificación

La certificación puede emitirse para uno de los siguientes niveles, según el análisis de riesgos y el impacto del sistema:

- **Nivel Básico:** Para sistemas sin información sensible y de impacto limitado.
- **Nivel Medio:** Para sistemas con impacto apreciable sobre la operativa, servicios o reputación.
- **Nivel Alto:** Para sistemas críticos que afectan a servicios esenciales, datos especialmente protegidos o funciones estratégicas del Estado.

> 🔐 La elección del nivel de certificación condiciona el número y la exigencia de las medidas que deben implementarse.


La certificación es importante porque demuestra el compromiso con la seguridad de la información, es obligatoria para ciertos sistemas de información de las administraciones públicas, puede ser un requisito para participar en licitaciones públicas y aumenta la confianza de los ciudadanos y otras organizaciones.

### Validez y renovación

La certificación ENS tiene una **validez de 2 años** desde la fecha de emisión. Una vez transcurrido ese periodo, la organización debe: someterse nuevamente a auditoría, actualizar su declaración de aplicabilidad y demostrar mejoras o mantenimiento en su sistema de seguridad

La renovación garantiza que el sistema sigue siendo **efectivo, actualizado y conforme con las exigencias regulatorias y tecnológicas** actuales.

## Comparación ENS vs ISO 27001

| Característica              | ENS                                       | ISO 27001                           |
|----------------------------|-------------------------------------------|-------------------------------------|
| Ámbito                     | Sector público en España                  | Internacional                       |
| Obligatorio                | Sí, para AAPP y empresas proveedoras      | No (voluntario)                     |
| Medidas / Controles        | 73 medidas específicas                    | 114 controles en 14 dominios        |
| Niveles de aplicación      | Bajo, Medio, Alto                         | No definidos                        |
| Certificación              | 2 años                                    | 3 años                              |
| Análisis de riesgos        | Obligatorio                               | Obligatorio                         |
| Compatibilidad             | Compatible con ISO 27001                  | Puede ser base para ENS             |

### ¿La certificación ISO 27001 es suficiente para cumplir con el ENS? 🤔

La certificación **ISO/IEC 27001** es un estándar internacional reconocido para la gestión de la seguridad de la información, y puede servir como una base sólida para cumplir con muchos de los requisitos del ENS. Sin embargo, **no es suficiente por sí sola** para garantizar la conformidad total con el Esquema Nacional de Seguridad. A continuación, se explican las diferencias clave:

1. **Requisitos adicionales específicos:**  
   El ENS establece **73 medidas de seguridad** distribuidas en tres marcos (organizativo, operacional y de protección), cada una con niveles de aplicación (BASE, Reforzado, Alto). Estos requisitos son concretos y obligatorios, y no están contemplados de forma detallada en ISO 27001.

2. **Marco legal y ámbito de aplicación:**  
   El ENS es de **cumplimiento obligatorio** en España para todas las Administraciones Públicas y para empresas proveedoras de servicios tecnológicos públicos. En cambio, ISO 27001 es una **norma voluntaria** de aplicación general.

3. **Auditoría y certificación diferenciadas:**  
   La certificación ENS se gestiona a través de entidades acreditadas por ENAC, y el proceso incluye la **validación y emisión del certificado por el Centro Criptológico Nacional (CCN)**. ISO 27001 no exige este nivel de control institucional en su proceso de certificación.

4. **Compatibilidad parcial entre controles:**  
   ISO 27001 incluye **114 controles agrupados en 14 dominios**, que no coinciden uno a uno con las medidas del ENS. Aunque hay solapamientos, muchos aspectos específicos del ENS (por ejemplo, medidas para sistemas clasificados, niveles de criticidad, perfil de cumplimiento) no están contemplados en la ISO.

### ¿Cómo puede ayudarte ISO 27001 a cumplir con el ENS?

La implementación de ISO 27001 puede facilitar el cumplimiento del ENS en varios aspectos:

- Establece una base sólida de gobernanza en seguridad.
- Fomenta una cultura de mejora continua compatible con el enfoque del ENS.
- Estandariza procedimientos como el análisis de riesgos, la documentación y la auditoría interna.

> 💡 Si tu organización ya cuenta con una certificación ISO 27001, se recomienda realizar un **análisis de brechas (gap analysis)** con respecto a las exigencias del ENS. Este análisis te permitirá **reutilizar parte del trabajo realizado** y centrarte en los **requisitos adicionales específicos** del marco español.



## Conclusión 🏁

El ENS juega un papel crucial en la ciberseguridad del sector público español, proporcionando un marco común para la protección de la información y los servicios electrónicos. Su implementación efectiva es esencial para garantizar la confianza en la administración electrónica y proteger los datos de los ciudadanos. El ENS busca aplicar un ciclo de mejora continua, siguiendo los pasos de planificación, acción, comprobación y actuación, asegurando así la constante evolución y adaptación de las medidas de seguridad frente a los cambiantes desafíos en el entorno digital. 🔐🇪🇸👥
