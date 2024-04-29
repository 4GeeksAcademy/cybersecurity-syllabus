# Lectura 2 📕: Principios del Marco de Ciberseguridad de NIST

El marco de Ciberseguridad ó NIST Framework es una guía desarrollada para proporcionar un enfoque estructurado para gestionar y mejorar ciberseguridad de una organización. Este framework consta de tres componentes principales: el Núcleo, los perfiles y los planes de acción.

Al hablar del núcleo del NIST Framework (también conocido como core), nos referimos a un conjunto de actividades y prácticas recomendadas para gestionar los riesgos de ciberseguridad de una organización.

El núcleo se divide en cinco funciones principales

- Identificar
- Proteger
- Detectar
- Responder
- Recuperar

![Marco de Ciberseguridad de NIST](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/marco-de-ciberseguridad-de-nist.png)

### Funciones detalladas

1. **Identificación de los sistemas críticos y activos de información.**

De acuerdo al marco de NIST, la función de identificación se encarga de desarrollar un entendimiento organizacional para administrar los riesgos de ciberseguridad en sistemas, personas, activos, datas y capacidades. Entendiendo el contexto de negocios, los recursos en que se apoyan las funciones, y los riesgos en ciberseguridad que hacen que la organización se enfoque y priorice los esfuerzos, consistente con las estrategias de administración de riesgos y necesidades de negocios.

Al identificar los sistemas críticos y activos de información, las vulnerabilidades y las amenazas existentes en el sistema, las organizaciones pueden tomar medidas proactivas para protegerse de posibles ataques cibernéticos. Una organización debe tener un inventario completo de todos sus activos de información, como sistemas, redes, datos y aplicaciones. Esto ayuda a comprender qué activos son críticos y qué medidas de seguridad se deben implementar para protegerlos adecuadamente.

También es importante evaluar las vulnerabilidades e identificar las debilidades en los sistemas y redes que pueden ser explotadas por los atacantes. Mediante la realización de evaluaciones y pruebas, las organizaciones pueden identificar los puntos débiles y tomar medidas para corregirlos antes de que sean aprovechados.

Las categorías que entran desde esta función son:

| Administración de activos | Identificar los activos físicos y de software dentro de la organización para establecer un programa de administración de activos. |
| --- | --- |
| Ambiente de Negocio | Esto se refiere a todo el ambiente de negocio que apoya a la organización, incluyendo a todo lo que se refiere a todas las partes interesadas dentro para su comprensión y su priorización. |
| Gobernanza | Identificar todas las políticas legales, regulatorias y operacionales de la organización para así definir el programa de gobernanza. |
| Evaluación de riesgos | Identificar todas las amenazas y riesgos a los recursos internos y externos de la organización. |
| Estrategia de administración de riesgos | Identificar cualquier estrategia para manejar los riesgos, estableciendo una tolerancia de riesgos |
| Gestión de riesgos | Identificar todas las estrategias de gestión de riesgos, tales como: definir prioridades, tolerancias de riesgos y asumir el riesgo de las decisiones dentro de la organización. |

2. **Protección de los sistemas de información.**

La función de proteger dentro del marco de ciberseguridad NIST se centra en la implementación de medidas de seguridad para prevenir y mitigar los riesgos de ciberseguridad en una organización. Cuando protegemos los activos y sistemas de información, reducimos la probabilidad de sufrir ataques cibernéticos y minimizar el impacto en el caso de que ocurran.

Un aspecto clave dentro de la protección de los sistemas de información es la gestión de acceso, asegurando que solo las personas autorizadas tengan acceso a los sistemas y datos sensibles. Si implementamos políticas y controles de acceso adecuados, como contraseñas seguras, autenticación de usuarios de múltiples factores y gestión de privilegios, garantizamos que solo los usuarios autorizados puedan acceder a la información confidencial.

La protección también abarca la respuesta a incidentes de seguridad, ya que las organizaciones deben tener planes y procedimientos establecidos para responder de manera efectiva a los incidentes de ciberseguridad. Esto incluye la identificación y contención de la brecha de seguridad, la recuperación de sistemas y datos, y la comunicación adecuada con las partes interesadas internas y externas.

En pocas palabras, la función de protección se apoya en la habilidad de limitar contener el impacto de un potencial evento de ciberseguridad.

Dentro de las categorías de esta función tenemos: 

- **Control de acceso y autenticación:** Proteger la administración de identidad dentro de la organización para dar un control de acceso solo a los individuos autorizados.
- **Concientización y entrenamiento:** El personal de la organización debe ser educado de acuerdo a sus particulares necesidades de ciberseguridad y la concientización debe ser creada sobre cada responsabilidad de ciberseguridad.
- **Seguridad de datos:** Establecer estrategias de seguridad para proteger la confidencialidad, integridad y disponibilidad de la información.
- **Procedimientos y procesos de protección de información:** Los sistemas y activos de información deben ser manejados y mantenidos por políticas efectivas de seguridad.
- **Mantenimiento:** Cualquier reparación o mantenimiento hecho a las instalaciones de los sistemas de seguridad debe estar en concordancia con las políticas y procedimientos de la organización.
- **Tecnología de protección:** La seguridad y la resiliencia de los sistemas de información deben ser manejadas por soluciones de tenencia de seguridad.

3. **Detección y respuesta ante incidentes de seguridad.**

La detección y respuesta de incidentes dentro del NIST Framework es una parte muy importante para la gestión de ciberseguridad, ya que esta función se centra en la implementación de sistemas y herramientas de monitoreo que permiten identificar acciones maliciosas y sospechosas dentro de los sistemas de la organización. Estos sistemas pueden incluir firewall, sistemas de detección de intrusos, sistemas de prevención de pérdidas de datos, entre otros.

Una vez detectamos un incidente, la respuesta ante este incidente es crucial para contener y mitigar los datos, de acuerdo al NIST, el ciclo de vida para la respuesta ante algún incidente se divide en 4 fases principales:

- **Preparación**: En esta etapa realizamos un plan de respuesta ante incidentes que establezca roles y responsabilidades, así como los procedimientos a seguir en caso de un incidente de seguridad.
- **Detección y análisis:** En esta etapa hacemos usos de herramientas de detección como las que mencionamos anteriormente para identificar y analizar el incidente. Además hacemos una recopilación y examinamos los registro de auditorías y realizamos los análisis forenses para así determinar la naturaleza y alcance del incidente.
- **Contención y erradicación:** Una vez sabemos la magnitud del incidente, tomamos las medidas adecuadas para contenerlo y evitar su propagación, esto puede implicar desde la desconexión de sistemas afectados, hasta la eliminación del malware y aplicación de parches de seguridad
- **Recuperación:** Después de contener y erradicar el incidente, procedemos a la recuperación de los sistemas afectados. Algunas formas de lograrlo puede ser con la restauración de datos desde copias de seguridad, reconstrucción de sistemas comprometidos o la implementación de medidas adicionales de seguridad

Entre las categorías de la detección dentro del marco de ciberseguridad tenemos:

| Anomalías y eventos | La organización debe registrar cualquier anomalía detectada y analizarlas para su completo entendimiento. |  |
| --- | --- | --- |
| Monitoreo de seguridad continuo | Los sistemas de seguridad deben ser monitoreados para así identificar cualquier evento de y así verificar la efectividad en la protección. |  |
| Procesos de detección | Son los procesos implementados y probados para anomalías y eventos. |  |

4. **Recuperación y continuidad del negocio.**

Esta función se centra en garantizar que una organización pueda recuperarse rápidamente de un incidente de seguridad y pueda mantener la continuidad de sus operaciones comerciales mediante planes y medidas de acción que permitan la minimizar el impacto a las operaciones de la organización.

Dentro del marco se recomienda un enfoque sistemático para facilitar el cumpliento de esta función.

- **Planeación de respuesta:** Asegurarse que los procesos de planeación de respuesta sean ejecutados durante y después de un incidente.
- **Comunicaciones:** Las políticas deben ser lo suficientemente flexiones para permitir la coordinación entre todas las partes interesadas tanto internas como externas
- **Análisis**: Para una respuesta efectiva y recuperación de actividades, se deben de conducir los análisis
- **Mitigación:** La organización debe manejar actividades apropiadas para detener la expansión y mitigar los efectos de los riesgos de ciberseguridad
- **Mejoras:** Las actividades de mejoras deben ser manejadas desde la experiencia obtenida de cualquier actividad de detección o respuesta actual o pasada

5. **Gestión de riesgos**

Esta función se centra en identificar, evaluar y mitigar los riesgos asociados con los activos de información de una organización.

La gestión de riesgos implica un enfoque sistemático y proactivo para identificar y abordar los riesgos de seguridad de la información. El NIST recomienda seguir un proceso de gestión de riesgos que consta de las siguientes etapas:

- **Identificación de activos:** En esta etapa, se identifican y clasifican los activos de información de una organización. Esto puede incluir datos confidenciales, sistemas críticos, infraestructuras de red y cualquier otro elemento que sea valioso para la organización.
- **Evaluación de riesgos:** Una vez que se han identificado los activos, se procede a evaluar los riesgos asociados con cada uno de ellos. Esto implica identificar las amenazas potenciales, las vulnerabilidades existentes y el impacto que un incidente de seguridad podría tener en los activos.
- **Análisis de riesgos**: En esta etapa, se realiza un análisis detallado de los riesgos identificados. Esto implica evaluar la probabilidad de que ocurra un incidente de seguridad y el impacto potencial en los activos de información. También se pueden utilizar herramientas y técnicas como el análisis cuantitativo y cualitativo de riesgos.
- **Mitigación de riesgos:** Una vez que se comprenden los riesgos, se desarrollan e implementan medidas de mitigación para reducir la probabilidad de que ocurran incidentes de seguridad y minimizar su impacto. Estas medidas pueden incluir la implementación de controles de seguridad, la actualización de software, la capacitación del personal y la mejora de los procesos internos.

> 💡 Comprender estos principios nos ayudará mucho en nuestra carrera como analistas de ciberseguridad, ya en algunas ocasiones podemos entrar a una organización donde no hay ningún sistema de seguridad, y nuestra primera labor será la implementación de la misma. En esos casos podemos usar el Marco de Ciberseguridad del NIST como una guia para así saber por dónde comenzar nuestro trabajo y cuáles pueden ser todos los pasos a seguir

## 🔎 Laboratorio
    
Felicidades, fuiste contratado como analista de ciberseguridad en la empresa Intersecurity INC, gran trabajo.
   
En tu primer día de función los directivos de la empresa te explican que no hay un sistema de seguridad y protección establecido y es urgente implementar uno, así, afortunadamente, durante tu formación educativa, estudiaste sobre el NIST Framework por lo que piensas que será una gran idea implementarlo para reforzar la seguridad dentro de la organización

Al momento de la implementación, tus jefes te hacen las siguientes preguntas:

- **¿Cuál es el primer paso para comenzar el trabajo?**

- **¿Qué medidas puedes implementar para la protección de los sistemas de información?**

- **¿Puedes explicar un poco como sería el proceso de detección y respuestas ante los incidentes de seguridad?**

- **¿Cuál es el enfoque a recuperar el sistema en caso de que se reciba un ataque a los sistemas?**

¿Cómo las responderías tú? 🤔
