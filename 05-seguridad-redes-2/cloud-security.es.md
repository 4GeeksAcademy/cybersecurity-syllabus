---
title: "Seguridad en la nube"
subtitle: "Protegiendo tus Activos Digitales: Conceptos Clave de Seguridad en la Nube para Empresas y Usuarios - Todo lo que Necesitas Saber sobre la Seguridad en la Nube"
tags: ["redes"]
authors: ["blindma1den", "lorenagubaira"]

---

Ya conocemos lo que es la seguridad en general, si nos enfocamos en la "seguridad en la nube" estamos especificando el subconjunto de tareas, politicas, controles, tecnologias y cualquier otra cosa necesaria para poder aplicar la seguridad en un entorno "nube" como Amazon Web Services, Microsoft Azure o Google Cloud.

## Localmente o en la nube

Antes de la existencia de la nube, las empresas gestionaban su infraestructura de TI de manera local. Este enfoque, conocido como computación on-premises o en sitio, requería que las empresas tuvieran todo el hardware y software necesario dentro de sus propias instalaciones. 

La nube es lo opuesto, en "la nube" los servidores y servicios no estan en las instalaciones de la empresa, sino que se acceden a través de internet. Amazon, Google y Microsoft tienen "nubes" que las empresas contratan para tener sus servidores online.

Las empresas generalmente prefieren la nube por su escalabilidad, costos reducidos, y flexibilidad. Sin embargo, algunas optan por infraestructura local por el control y seguridad que ofrece. Muchas utilizan un enfoque híbrido para combinar lo mejor de ambos mundos.

## ¿Qué tiene una nube?

Todas las nubes corporativas estan compuestas de los mismos componentes o funcionalidades:

- **Infraestructura como Servicio (IaaS)**: Proporciona recursos virtualizados como servidores, almacenamiento y redes. Ejemplos: Amazon EC2, Google Cloud Compute Engine.
- **Plataforma como Servicio (PaaS)**: Ofrece un entorno de desarrollo completo para construir, probar y desplegar aplicaciones. Ejemplos: Google App Engine, Microsoft Azure App Services.
- **Software como Servicio (SaaS)**: Ofrece aplicaciones listas para usar a través de Internet. Ejemplos: Microsoft Office 365, Google Workspace.
- **Almacenamiento**: Espacio para guardar datos en la nube, como Amazon S3 y Google Cloud Storage.
- **Redes**: Conectividad y servicios de red para vincular recursos, como redes virtuales y balanceadores de carga.
- **Seguridad**: Herramientas y servicios para proteger datos y aplicaciones, como firewalls, cifrado y gestión de identidades.
- **Bases de Datos**: Servicios para gestionar datos estructurados y no estructurados, como Amazon RDS y Google Cloud Bigtable.

## Componentes mas importantes de la seguridad en la nube

La seguridad en la nube tiene ventajas ya que los grandes proveedores de nubes como Amazon, Google y Microsoft se encargan de una parte de la misma y ya incluyen mecanismos de cifrado, protección de datos, etc. Sin embargo, una parte de la responsabilidad recae sobre nuestra implementación, y para eso debemos pensar en nuestra seguridad y como dividirla:

- Identidad: MFA, SSO, Control de Acceso Basado en Roles, etc.
- Protección de Datos: Cifrado.
- Seguridad de la Infraestructura: Segmentacion de red y monitoreo (deteccion de instrusos).
- Seguridad de Aplicaciones: Pruebas de Vulnerabilidades, actualizaciones y parches.
- Cumplimiento y Gobernanza: Politicas, regulaciones como GDPR, etc.
- Continuidad del Negocio y Recuperación ante Desastres: Respados, planes de recuperacion.

### Identidad

La gestión de identidades es fundamental para controlar quién puede acceder a los recursos en la nube y qué acciones pueden realizar. Esto se logra a través de varios mecanismos:

- **Autenticación Multifactorial (MFA):** 
  - Añade una capa extra de seguridad al requerir más de un método de verificación de identidad. Esto puede incluir contraseñas, huellas digitales, códigos enviados a dispositivos móviles, etc. MFA ayuda a prevenir accesos no autorizados incluso si las credenciales son comprometidas.

- **Single Sign-On (SSO):** 
  - Permite a los usuarios acceder a múltiples aplicaciones con una sola autenticación. Esto simplifica el proceso de inicio de sesión y mejora la experiencia del usuario al tiempo que centraliza la gestión de identidades.

- **Control de Acceso Basado en Roles (RBAC):** 
  - Asigna permisos y accesos a los usuarios en función de sus roles dentro de la organización. Esto garantiza que los empleados solo tengan acceso a los recursos necesarios para su función, minimizando el riesgo de accesos innecesarios.

### Protección de Datos

Proteger los datos almacenados y transferidos en la nube es una prioridad para garantizar la confidencialidad e integridad de la información:

- **Cifrado:**
  - **En tránsito:** Protege los datos mientras se mueven a través de las redes utilizando protocolos como SSL/TLS. Esto asegura que los datos no puedan ser interceptados y leídos por terceros.
  - **En reposo:** Cifra los datos almacenados en discos o bases de datos para que no sean accesibles sin la clave de cifrado adecuada. Esto es crucial para proteger los datos en caso de un acceso no autorizado o robo de hardware.

### Seguridad de la Infraestructura

La seguridad de la infraestructura implica proteger los componentes físicos y virtuales que componen la nube:

- **Segmentación de Red:**
  - Divide la red en segmentos más pequeños y seguros para aislar diferentes partes de la infraestructura. Esto limita el alcance de posibles ataques y facilita la implementación de medidas de seguridad específicas para cada segmento.

- **Monitoreo y Detección de Intrusos:**
  - Implementa sistemas que detectan actividades sospechosas o no autorizadas dentro de la infraestructura. Las soluciones de detección de intrusos (IDS) y prevención de intrusos (IPS) ayudan a identificar y mitigar amenazas antes de que causen daño.

### Seguridad de Aplicaciones

Asegurar las aplicaciones que se ejecutan en la nube es esencial para proteger contra vulnerabilidades y ataques:

- **Pruebas de Vulnerabilidades:**
  - Realizar evaluaciones regulares para identificar y corregir debilidades en las aplicaciones. Esto incluye escaneo de código estático, pruebas de penetración y análisis de seguridad automatizado.

- **Actualizaciones y Parches:**
  - Mantener las aplicaciones y sistemas actualizados es fundamental para protegerse contra nuevas amenazas. Los parches corrigen vulnerabilidades conocidas y mejoran la seguridad general del sistema.

### Cumplimiento y Gobernanza

La gobernanza y el cumplimiento legal garantizan que las prácticas de seguridad en la nube se alineen con las regulaciones y políticas internas:

- **Políticas de Seguridad:**
  - Definir políticas claras que establezcan las reglas y procedimientos para la protección de datos y el acceso a la nube. Estas políticas deben ser comunicadas y aplicadas de manera consistente en toda la organización.

- **Regulaciones (GDPR, HIPAA, etc.):**
  - Cumplir con las normativas legales específicas de la industria es crucial para evitar sanciones y proteger la reputación de la empresa. El GDPR, por ejemplo, establece requisitos estrictos para la protección de datos personales en la Unión Europea.

### Continuidad del Negocio y Recuperación ante Desastres

La planificación para la continuidad del negocio y la recuperación ante desastres asegura que una empresa pueda seguir operando después de un incidente:

- **Respaldos:**
  - Realizar copias de seguridad regulares de datos críticos para garantizar que puedan ser recuperados en caso de pérdida o daño. Las copias de seguridad deben almacenarse de manera segura, tanto localmente como en ubicaciones remotas.

- **Planes de Recuperación:**
  - Desarrollar y probar planes de recuperación detallados que describan los pasos a seguir para restablecer las operaciones normales después de un desastre. Esto incluye asignar roles y responsabilidades, establecer procesos de comunicación y definir métricas de tiempo de recuperación.

## **¿Qué hace que la seguridad en la nube sea diferente?**

La seguridad informática tradicional ha experimentado una inmensa evolución debido al cambio a la informática basada en la nube. Si bien los modelos de la nube permiten una mayor comodidad, la conectividad siempre activa requiere nuevas consideraciones para mantenerlas seguras. La seguridad en la nube, como una solución de ciberseguridad modernizada, se distingue de los modelos informáticos heredados en algunos aspectos.

### **Almacenamiento de datos:**

La mayor distinción es que los modelos antiguos de TI dependían en gran medida del almacenamiento de datos in situ. Las empresas han descubierto desde hace mucho tiempo que la creación de todas las plataformas informáticas internas para los controles de seguridad detallados y personalizados es costosa y rígida. Las plataformas basadas en la nube han ayudado a transferir los costes de desarrollo y mantenimiento de los sistemas, pero también a eliminar cierto control de los usuarios.

### **Velocidad de escalada:**

De manera similar, la seguridad en la nube exige una atención única al escalar los sistemas de TI de la empresa. La infraestructura y las aplicaciones centradas en la nube son muy modulares y se movilizan rápidamente. Si bien esta capacidad mantiene los sistemas uniformemente ajustados a los cambios empresariales, también plantea problemas cuando la necesidad de mejoras y comodidad de una empresa supera su capacidad para mantenerse al día en materia de seguridad.

### **Interfaz del sistema de usuarios finales:**

Tanto para las empresas como para los usuarios individuales, los sistemas de nubes también se conectan con muchos otros sistemas y servicios que se deben asegurar. Los permisos de acceso deben mantenerse desde el nivel de dispositivo de usuario final hasta el nivel de software e incluso el nivel de red. Además, tanto proveedores como usuarios deben estar atentos a las vulnerabilidades que pueden causar a través de comportamientos de configuración y acceso al sistema inseguros.

### **Proximidad a otros datos y sistemas en red:**

Dado que los sistemas en la nube son una conexión persistente entre los proveedores de la nube y todos sus usuarios, esta importante red puede comprometer incluso al propio proveedor. En los entornos de redes, un solo dispositivo o componente débil se puede explotar para infectar al resto. Los proveedores de la nube se exponen a las amenazas de muchos usuarios finales con los que interactúan, bien sea que estén proporcionando almacenamiento de datos u otros servicios. Las responsabilidades adicionales en materia de seguridad de la red recaen en los proveedores cuyos productos entregados de otro modo se basarían exclusivamente en los sistemas de los usuarios finales y no en los propios.

Resolver la mayoría de los problemas de seguridad en la nube significa que tanto los usuarios como los proveedores de la nube, tanto en entornos personales como en empresariales, deben ser proactivos en cuanto a sus propias funciones en la ciberseguridad. Este doble enfoque significa que los usuarios y los proveedores deben abordar lo siguiente:

- Configuración y mantenimiento seguros del sistema.
- Educación sobre seguridad del usuario, tanto a nivel de comportamiento como a nivel técnico.

Por último, los proveedores y los usuarios de la nube deben tener transparencia y responsabilidad para garantizar que ambas partes estén seguras.

## Amenazas y vulnerabilidades de la seguridad en la nube

Casi todas las organizaciones han adoptado la computación en la nube en distintos grados dentro de sus negocios. Sin embargo, con esta adopción de la nube surge la necesidad de garantizar que la estrategia de seguridad en la nube de la organización sea capaz de proteger contra las principales amenazas a la seguridad en la nube.

### **Mal configuración**

Las configuraciones incorrectas de los ajustes de seguridad en la nube son una de las principales causas de las filtraciones de datos en la nube. Las estrategias de gestión de la postura de seguridad en la nube de muchas organizaciones son inadecuadas para proteger su infraestructura basada en la nube.

Varios factores contribuyen a esto. La infraestructura de la nube está diseñada para ser fácilmente utilizable y permitir compartir datos fácilmente, lo que dificulta que las organizaciones garanticen que solo las partes autorizadas puedan acceder a los datos. Además, las organizaciones que utilizan una infraestructura basada en la nube tampoco tienen visibilidad y control completos sobre su infraestructura, lo que significa que deben depender de los controles de seguridad proporcionados por su proveedor de servicios en la nube (CSP) para configurar y asegurar su implementación en la nube.

Dado que muchas organizaciones no están familiarizadas con la seguridad de la infraestructura de la nube y, a menudo, tienen implementación de múltiples nubes (cada una con una gama diferente de controles de seguridad proporcionados por el proveedor), es fácil que una mala configuración o una supervisión de la seguridad dejen los recursos basados en la nube de una organización expuestos a los atacantes.

### **Acceso no autorizado**

A diferencia de la infraestructura local de una organización, su implementación basada en la nube está fuera del perímetro de la red y es directamente accesible desde la Internet pública. Si bien esto es un activo para la accesibilidad de esta infraestructura para empleados y clientes, también facilita que un atacante obtenga acceso no autorizado a los recursos basados en la nube de una organización. La seguridad configurada de manera incorrecta o las credenciales comprometidas pueden permitir que un atacante obtenga acceso directo, potencialmente sin el conocimiento de una organización.

### **Interfaces/API inseguras**

Los CSP suelen proporcionar una serie de interfaces de programación de aplicaciones (API) e interfaces para sus clientes. En general, estas interfaces están bien documentadas en un intento de hacerlas fácilmente utilizables para los clientes de un CSP. Sin embargo, esto crea problemas potenciales si un cliente no ha protegido adecuadamente las interfaces para su infraestructura basada en la nube. Un ciberdelincuente también puede utilizar la documentación diseñada para el cliente para identificar y explotar métodos potenciales para acceder y extraer datos confidenciales del entorno de nube de una organización.

Actualmente los servicios en la Nube ofrecen APIs. Las cuales son las interfaces **que son diseñadas para protegerse contra intentos accidentales y malintencionados.** Los equipos de TI utilizan interfaces y APIs para administrar e interactuar con servicios en la Nube.

Tanto la seguridad y disponibilidad de los servicios, la autenticación y control de acceso depende de la seguridad API, las interfaces y APIs débiles exponen a las organizaciones a las cuestiones de seguridad relacionadas con la confidencialidad, integridad, disponibilidad y responsabilidad.

Las APIs e interfaces tienden a ser la parte más expuesta de un sistema, ya que por lo general son accesibles desde la Internet abierta, por eso se recomienda controles adecuados y revisiones de código centrados en la seguridad y pruebas de penetración rigurosa.

### **Secuestro de cuentas**

Muchas personas tienen una seguridad de contraseñas extremadamente débil, lo que incluye la reutilización de contraseñas y el uso de contraseñas débiles. Este problema exacerba el impacto de los ataques de phishing y las filtraciones de datos, ya que permite el uso de una sola contraseña robada en varias cuentas diferentes.

El secuestro de cuentas es uno de los problemas de seguridad en la nube más graves, ya que las organizaciones dependen cada vez más de la infraestructura y las aplicaciones basadas en la nube para las funciones comerciales principales. Un atacante con las credenciales de un empleado puede acceder a datos o funcionalidades confidenciales, y las credenciales de clientes comprometidas brindan control total sobre su cuenta en línea. Además, en la nube, las organizaciones a menudo carecen de la capacidad de identificar y responder a estas amenazas con la misma eficacia que en la infraestructura local.

Por lo general, las brechas de datos y otros ataques son el resultado de contraseñas débiles o pobres. Las claves deben ser protegidas de manera adecuada, y es necesaria una infraestructura de clave pública bien asegurada, También necesitan las claves o contraseñas deben ser cambiadas periódicamente para hacer que a los atacantes les resulte más difícil utilizar las claves que han obtenido sin autorización.

Hoy en día, los fraudes y explotaciones siguen teniendo éxito, y ahora los servicios en la Nube son una nueva amenaza, ya que los atacantes pueden espiar actividades, manipular transacciones y hasta modificar los datos.

Las estrategias comunes de protección y defensa pueden contener los daños sufridos por una violación. Las organizaciones deben prohibir que se compartan las credenciales de cuenta entre los usuarios y los servicios, así como permitir los esquemas de autenticación multifactoriales donde estén disponibles. Las cuentas, incluso las cuentas de servicio, deben ser controladas de manera que cada transacción se pueda remontar a una sola persona.

### **Falta de visibilidad**

Los recursos basados en la nube de una organización están ubicados fuera de la red corporativa y se ejecutan en una infraestructura que la empresa no posee. Como resultado, muchas herramientas tradicionales para lograr visibilidad de la red no son efectivas para entornos de nube y algunas organizaciones carecen de herramientas de seguridad centradas en la nube. Esto puede limitar la capacidad de una organización para monitorear sus recursos basados en la nube y protegerlos contra ataques.

### **Intercambio externo de datos**

La nube está diseñada para facilitar el intercambio de datos. Muchas nubes ofrecen la opción de invitar explícitamente a un colaborador por correo electrónico o de compartir un enlace que permite que cualquier persona con la URL acceda al recurso compartido.

Si bien este fácil intercambio de datos es una ventaja, también puede ser un problema importante de seguridad en la nube. El uso del uso compartido basado en enlaces, una opción popular ya que es más fácil que invitar explícitamente a cada colaborador previsto, dificulta el control del acceso al recurso compartido. El enlace compartido puede ser reenviado a otra persona, robado como parte de un ataque cibernético o adivinado por un ciberdelincuente, proporcionando acceso no autorizado al recurso compartido. Además, el uso compartido basado en enlaces hace que sea imposible revocar el acceso a un solo destinatario del enlace compartido.

### **Insiders maliciosos**

Las amenazas internas son un problema de seguridad importante para cualquier organización. Un interno malintencionado ya tiene acceso autorizado a la red de una organización y a algunos de los recursos confidenciales que contiene. Los intentos de obtener este nivel de acceso son lo que revela a la mayoría de los atacantes a su objetivo, lo que dificulta que una organización no preparada detecte una información privilegiada maliciosa.

En la nube, la detección de un usuario interno malintencionado es aún más difícil. Con implementaciones en la nube, las empresas carecen de control sobre su infraestructura subyacente, lo que hace que muchas soluciones de seguridad tradicionales sean menos eficaces. Esto, junto con el hecho de que se puede acceder a la infraestructura basada en la nube directamente desde la internet pública y de que a menudo dicha infraestructura presenta configuraciones incorrectas de seguridad, hace que sea aún más difícil detectar a usuarios internos malintencionados.

Las actitudes maliciosas van desde el robo de datos hasta la venganza. En un escenario de Nube, un vengador interno puede destruir infraestructuras enteras o manipular los datos. Los sistemas que dependen únicamente de la empresa de servicios en la nube para la seguridad, como el cifrado, se encuentran en mayor riesgo. Se recomienda que las organizaciones controlen el proceso de cifrado y las claves, la segregación de funciones y la reducción al mínimo del acceso a los usuarios. Son también críticos el registro eficaz, la vigilancia y la auditoría de las actividades del administrador.

### **DDOS y DOS, Ataques de denegación de servicio**

La nube es esencial para la capacidad de muchas organizaciones de hacer negocios. Utilizan la nube para almacenar datos críticos para el negocio y ejecutar importantes aplicaciones internas y de cara al cliente.

Esto significa que un ataque de denegación de servicio (DoS) exitoso contra la infraestructura de la nube probablemente tendrá un impacto importante en varias empresas diferentes. Como resultado, los ataques DoS en los que el atacante exige un rescate para detener el ataque representan una amenaza importante para los recursos basados en la nube de una organización.

Estos tipos de ataques han existido durante muchos años, sin embargo, en los últimos años ha tomado más protagonismo debido a la computación en la Nube, ya frecuentemente afecta la disponibilidad. Según un estudio: “Experimentar un ataque de denegación de servicio es como estar atrapado en el tráfico en hora punta; hay una manera de llegar a su destino y no hay nada que pueda hacer al respecto, salvo sentarse y esperar”.

### **Fuga de datos**

Los entornos basados en la nube facilitan el intercambio de datos que están almacenados en ellos. Estos entornos son accesibles directamente desde la internet pública e incluyen la capacidad de compartir datos fácilmente con otras partes a través de invitaciones directas por correo electrónico o mediante un enlace público a los datos.

La facilidad para compartir datos en la nube, si bien es un activo importante y clave para la colaboración en la nube, genera serias preocupaciones con respecto a la pérdida o fuga de datos. De hecho, el 69% de las organizaciones señalan esto como su mayor preocupación en materia de seguridad en la nube. El intercambio de datos mediante enlaces públicos o la configuración de un repositorio basado en la nube como público los hace accesibles a cualquier persona con conocimiento del enlace, y existen herramientas específicas para buscar en Internet estas implementaciones en la nube no seguras.

Esto puede venir de un error humano como de un ataque dirigido, es producido por vulnerabilidades de aplicaciones o seguridad deficiente. Por otro lado, debido a la cantidad de datos almacenados en los servidores de la Nube, los proveedores se convierten en un objetivo atractivo, por eso para no incurrir en multas o enfrentar demandas por la valoración de datos, se recomienda a las organizaciones que utilicen la autenticación de factores múltiples y la encriptación para protegerse contra las violaciones de datos.

### **Vulnerabilidad del sistema explotado**

Esta amenaza, no es algo nuevo que suceda, sin embargo, se han convertido en un problema grave debido a la capacidadmultiusuario de la Nube. Las organizaciones comparten la memoria, bases de datos y otros recursos en estrecha proximidad entre sí, creando nuevas áreas de ataque.

Pero, estos ataques pueden ser minimizados gracias a prácticas que incluyen la exploración regular de la vulnerabilidad, la gestión de parches del sistema, y un rápido seguimiento de las amenazas reportadas.

### **Amenazas Persistentes Avanzadas (APT)**

Se llaman así por sus siglas en inglés, estas amenazas se filtran en los sistemas para establecer un punto de apoyo, poco a poco se van filtrando en los datos y la propiedad intelectual durante un largo tiempo, los APTs son difíciles de detectar ya que se van moviendo lateralmente a través de la red y se mezclan con el tráfico normal. Los principales proveedores de las Nubes, están utilizando técnicas avanzadas para evitar que los APTs se filtren en las infraestructuras, por lo que los clientes tienen que ser tan diligentes en la detección de los compromisos de las APTs en las cuentas de la nube como lo harían en los sistemas de correo locales.

### **Pérdida de datos Permanente.**

El objetivo principal de los hackers maliciosos es eliminar permanentemente los datos de la nube para dañar a las empresas, y los centros de datos en la nube son tan vulnerables a los desastres naturales como cualquier instalación.

Los proveedores de nube recomiendan distribuir los datos y las aplicaciones a través de múltiples zonas para una mayor protección. Las medidas adecuadas de respaldo de datos son esenciales, así como la adhesión a las mejores prácticas en la continuidad del negocio y la recuperación de desastres. La copia de seguridad diaria y el almacenamiento fuera de las instalaciones siguen siendo importantes en los entornos de nube.

### **Tecnología compartida = peligros compartidos**

Una amenaza importante para la Nube, es el intercambio de la tecnología. Por lo general, los proveedores de servicio de la Nube comparten infraestructura, plataformas y aplicaciones, y si se presenta una vulnerabilidad en cualquiera de estas capas, podría afectar a todos los que están incluidos.

Para disminuir los riesgos de forma rentable al aplicar controles de seguridad para disminuir las probabilidades de que puedan explotarse las vulnerabilidades del bien y derivar en la implementación de amenazas.

## Medidas de seguridad para la seguridad en la nube

Cloud Security abarca las tecnologías, los controles, los procesos y las políticas que se combinan para proteger sus sistemas, datos e infraestructura basados en la nube. Es un subdominio de la seguridad informática y, más ampliamente, de la seguridad de la información.

Es una responsabilidad compartida entre usted y su proveedor de servicios en la nube. Usted implementa una estrategia de Cloud Security para proteger sus datos, cumplir con las normas y proteger privacidad de sus clientes. Lo que a su vez lo protege de las ramificaciones de reputación, financieras y legales de las violaciones y pérdidas de datos.

![Tabla de responsabilidad compartida del Cloud Security](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/05-seguridad-en-redes-2/cloud-security/cloud-security-image-2.jpg)

***Modelo de Responsabilidad Compartida de Cloud Security (Fuente de la imagen: Sinopsis)***

Cloud Security es un requisito crítico para todas las organizaciones. Especialmente con la última [investigación del (ISC)2](https://www.isc2.org/Resource-Center/Reports/Cloud-Security-Report) que informa que el 93% de las organizaciones están moderada o extremadamente preocupadas por Cloud Security, y una de cada cuatro organizaciones que confirman un incidente de Cloud Secutity en los últimos 12 meses.

Exploramos los riesgos de seguridad al trasladarse a la nube, comprenderá por qué es necesario Cloud Security y descubrirá las mejores prácticas de Cloud Security. También cubriremos temas como la forma de evaluar la seguridad de un proveedor de servicios en la nube e identificar las certificaciones y la formación para mejorar su Cloud Secutity.

## **¿Cómo funciona Cloud Security?**

Cloud Security es una compleja interacción de tecnologías, controles, procesos y políticas. Una práctica que está altamente personalizada a los requerimientos únicos de su organización.

Como tal, no hay una sola explicación que abarque cómo «funciona» Cloud Security

![modelo de las cargas de trabajo de las nubes](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/05-seguridad-en-redes-2/cloud-security/cloud-security-image-3.jpg)

Un modelo para asegurar las cargas de trabajo de las nubes (Fuente de la imagen: HyTrust)

Afortunadamente, hay un conjunto de estrategias y herramientas ampliamente establecidas que se pueden utilizar para lograr una sólida configuración de Cloud Security, entre ellas:

### **Gestión de la identidad y el acceso**

Todas las empresas deberían tener un [sistema de gestión de la identidad y el acceso (IAM)](https://www.csoonline.com/article/2120384/what-is-iam-identity-and-access-management-explained.html) para controlar el acceso a la información. Su proveedor de nubes se integrará directamente con su IAM u ofrecerá su propio sistema incorporado. Un IAM combina la autenticación multifactorial y las políticas de acceso de los usuarios, ayudándole a controlar quién tiene acceso a sus aplicaciones y datos, a qué pueden acceder y qué pueden hacer con sus datos.

### **Seguridad física**

[La seguridad física](https://www.ibm.com/blogs/cloud-computing/2012/02/22/cloud-physical-security-considerations/) es otro pilar de la Cloud Security. Es una combinación de medidas para prevenir el acceso directo y la interrupción del hardware alojado en el centro de datos de su proveedor de nube. La seguridad física incluye el control de acceso directo con puertas de seguridad, fuentes de alimentación ininterrumpida, CCTV, alarmas, filtración de aire y partículas, protección contra incendios y más.

### **Inteligencia, vigilancia y prevención de amenazas**

[La Inteligencia de Amenazas](https://www.forcepoint.com/cyber-edu/threat-intelligence), los Sistemas [de Detección de Intrusos (IDS)](https://www.barracuda.com/glossary/intrusion-detection-system) y los [Sistemas de Prevención de Intrusos (IPS)](https://www.forcepoint.com/cyber-edu/intrusion-prevention-system-ips) forman la columna vertebral de Cloud Security. La Inteligencia de Amenazas y las herramientas de IDS ofrecen funcionalidad para identificar a los atacantes que actualmente tienen como objetivo sus sistemas o que serán una amenaza futura. Las herramientas de IPS implementan funcionalidad para mitigar un ataque y avisarle de su ocurrencia para que usted también pueda responder.

### **Cifrado**

Usando la tecnología de la nube, usted está enviando datos hacia y desde la plataforma del proveedor de la nube, a menudo almacenándolos dentro de su infraestructura. [El cifrado](https://searchsecurity.techtarget.com/definition/encryption) es otra capa de Cloud Security para proteger sus activos de datos, codificándolos cuando están en reposo y en tránsito. Esto asegura que los datos sean casi imposibles de descifrar sin una clave de descifrado a la que sólo usted tiene acceso.

### **Pruebas de vulnerabilidad y penetración de las nubes**

Otra práctica para mantener y mejorar la Cloud Security es la [prueba de vulnerabilidad y penetración](https://www.hitachi-systems-security.com/blog/penetration-testing-vs-vulnerability-assessment/). Estas prácticas implican que usted – o su proveedor – ataque su propia infraestructura de nube para identificar cualquier debilidad o explotación potencial. A continuación, puede implementar soluciones para parchear estas vulnerabilidades y mejorar su posición de seguridad.

### **Microsegmentación**

[La microsegmentación](https://www.networkworld.com/article/3247672/what-is-microsegmentation-how-getting-granular-improves-network-security.html) es cada vez más común en la implementación de Cloud Security. Es la práctica de dividir el despliegue de la nube en distintos segmentos de seguridad, hasta el nivel de la carga de trabajo individual. Al aislar las cargas de trabajo individuales, se pueden aplicar políticas de seguridad flexibles para minimizar los daños que un atacante podría causar, en caso de que obtuviera acceso.

### **La próxima generación de cortafuegos**

[Los cortafuegos de última generación](https://digitalguardian.com/blog/what-next-generation-firewall-learn-about-differences-between-ngfw-and-traditional-firewalls) son otra pieza del rompecabezas de Cloud Security. Protegen sus cargas de trabajo usando la funcionalidad de los cortafuegos tradicionales y las nuevas características avanzadas. La protección de los cortafuegos tradicionales incluye filtrado de paquetes, inspección de estado, proxy, bloqueo de IP, bloqueo de nombres de dominio y bloqueo de puertos.

> 👉 Los cortafuegos de última generación añaden un sistema de prevención de intrusiones, inspección profunda de paquetes, control de aplicaciones y análisis del tráfico cifrado para proporcionar una detección y prevención integral de amenazas.

![Arquitectura de alojamiento](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/05-seguridad-en-redes-2/cloud-security/cloud-security-image-4.jpg)

Arquitectura de alojamiento (fuente: Kinsta)

En este ejemplo, en Kinsta aseguran todos los sitios web detrás del [Firewall de Google Cloud Platform (GCP)](https://kinsta.com/es/changelog/optimizaciones-automaticas-de-bases-de-datos-mysql-auto-recuperacion-php-firewall-gcp/#now-secured-behind-google-cloud-platform-firewall). Ofreciendo una protección de última generación y la capacidad de integrarse más estrechamente con otras soluciones de seguridad de GCP.

## **7 Riesgos de seguridad de la computación en nube**

Ya sea que esté o no operando en la nube, la seguridad es una preocupación para todos los negocios. Se enfrentará a riesgos como la denegación de servicio, el malware, la inyección SQL, las brechas de datos y la pérdida de datos. Todo ello puede tener un impacto significativo en la reputación y los resultados de su empresa.

Cuando se mueve a la nube introduce un nuevo conjunto de riesgos y cambia la naturaleza de los demás. Eso no significa que la computación en la nube no sea segura. De hecho, muchos proveedores de nubes introducen el acceso a herramientas y recursos de seguridad altamente sofisticados a los que de otra manera no podrías acceder. Simplemente significa que hay que ser consciente del cambio en los riesgos para mitigarlos. Así que, echemos un vistazo a los riesgos de seguridad únicos de la computación en nube.

**1. Pérdida de visibilidad**

La mayoría de las empresas accederán a una gama de servicios de nube a través de múltiples dispositivos, departamentos y geografías. Este tipo de complejidad en una configuración de computación en nube – sin las herramientas apropiadas en su lugar – puede causar que pierda la visibilidad del acceso a su infraestructura. Sin los procesos correctos en su lugar, puede perder de vista quién está usando sus servicios en la nube. Incluyendo qué datos están accediendo, subiendo y bajando. Si no puede verlo, no puede protegerlo. Aumentando el riesgo de violación y pérdida de datos.

**2. Violaciones del cumplimiento**

Con el aumento del control reglamentario, es probable que tenga que cumplir una serie de requisitos de cumplimiento muy estrictos. Al pasar a la nube, se introduce el riesgo de violaciones de cumplimiento si no se tiene cuidado. Muchos de estos reglamentos exigen que su empresa sepa dónde están sus datos, quién tiene acceso a ellos, cómo se procesan y cómo se protegen. Otras regulaciones requieren que su proveedor de nube tenga ciertas credenciales de cumplimiento. Una transferencia descuidada de datos a la nube, o el traslado al proveedor equivocado, puede poner a su organización en un estado de incumplimiento. Introduciendo repercusiones legales y financieras potencialmente graves.

**3. Falta de estrategia y arquitectura de Cloud Security**

Este es un riesgo de Cloud Security que puede ser fácilmente evitado, pero muchos no lo hacen. En su prisa por migrar los sistemas y datos a la nube, muchas organizaciones empiezan a funcionar mucho antes de que los sistemas y estrategias de seguridad estén en funcionamiento para proteger su infraestructura. Asegúrese de implementar una estrategia de seguridad e infraestructura diseñada para que la nube funcione en línea con sus sistemas y datos.

**4. Amenazas internas**

Sus empleados de confianza, contratistas y socios comerciales pueden ser algunos de sus mayores riesgos de seguridad. Estas amenazas internas no tienen por qué tener un propósito malicioso para causar daños a su negocio. De hecho, la mayoría de los incidentes internos se deben a la falta de formación o a la negligencia.

Mientras que actualmente se enfrenta a este problema, el traslado a la nube cambia el riesgo. Usted entrega el control de sus datos a su proveedor de servicios en la nube e introduce una nueva capa de amenaza interna de los empleados del proveedor.

**5. Incumplimientos contractuales**

Cualquier sociedad contractual que tenga incluirá restricciones sobre cómo se utilizan los datos compartidos, cómo se almacenan y quién está autorizado a acceder a ellos. Sus empleados, al trasladar involuntariamente datos restringidos a un servicio en la nube sin autorización, podrían crear un incumplimiento de contrato que podría dar lugar a acciones legales.

Asegúrese de leer los términos y condiciones de sus proveedores de nubes. Incluso si tiene autorización para mover datos a la nube, algunos proveedores de servicios incluyen el derecho de compartir cualquier dato cargado en su infraestructura. Por ignorancia, usted podría involuntariamente violar un acuerdo de no divulgación.

**6. Interfaz de usuario de aplicaciones inseguras (API)**

Cuando se operan sistemas en una infraestructura de nube, se puede utilizar una API para implementar el control. Cualquier API incorporada a sus aplicaciones web o móviles puede ofrecer acceso interno por parte del personal o externo por parte de los consumidores.

Son las API de cara al exterior las que pueden introducir un riesgo de Cloud Security Cualquier API externa insegura es una puerta de entrada que ofrece acceso no autorizado a los ciberdelincuentes que buscan robar datos y manipular servicios.

El ejemplo más destacado de una API externa insegura es el [escándalo de Facebook – Cambridge Analytica](https://www.nytimes.com/2018/04/04/us/politics/cambridge-analytica-scandal-fallout.html). La API externa insegura de Facebook le dio a Cambridge Analytica un acceso profundo a los datos de los usuarios de Facebook.

**7. Desconfiguración de los servicios de la nube**

La configuración errónea de los servicios de la nube es otro posible riesgo para Cloud Security. Con el aumento de la gama y la complejidad de los servicios, este es un problema creciente. La configuración errónea de los servicios en la nube puede hacer que los datos se expongan públicamente, se manipulen o incluso se eliminen.

Entre las causas más comunes se encuentran el mantenimiento de la seguridad predeterminada y la configuración de la gestión del acceso a datos altamente confidenciales. Otras incluyen una gestión de acceso mal ajustada que da acceso a personas no autorizadas, y el acceso a datos manipulados en los que los datos confidenciales se dejan abiertos sin necesidad de autorización.

## **¿Por qué se requiere Cloud Security?**

La adopción masiva de la tecnología de nubes combinada con un volumen y una sofisticación cada vez mayores de las amenazas cibernéticas es lo que impulsa la necesidad de Cloud Security. Reflexionando sobre los riesgos de seguridad de la adopción de la tecnología de nubes – esbozados anteriormente – el fracaso en la mitigación de los mismos puede tener implicaciones significativas.

### **Beneficios de la Cloud Security**

Más allá de la protección contra las amenazas y de evitar las consecuencias de las malas prácticas, cloud security ofrece beneficios que la convierten en un requisito para las empresas. Entre ellos se incluyen:

**1. Seguridad centralizada**

De la misma manera que la computación en la nube centraliza las aplicaciones y los datos, cloud security centraliza la protección. Ayudándole a mejorar la visibilidad, implementar controles y protegerse mejor contra los ataques. También mejora la continuidad de su negocio y la recuperación de desastres al tenerlo todo en un solo lugar.

**2. Costo reducido**

Un reputado proveedor de servicios de nube ofrecerá hardware y software incorporado dedicado a asegurar sus aplicaciones y datos las 24 horas del día. Esto elimina la necesidad de una inversión financiera significativa en su propia configuración.

**3. Administración reducida**

El paso a la nube introduce un modelo de responsabilidad compartida para la seguridad. Esto puede proporcionar una reducción significativa de la cantidad de tiempo y recursos invertidos en la administración de la seguridad. El proveedor de servicios de la nube asumirá la responsabilidad de asegurar su infraestructura – y a usted – a través del almacenamiento, la computación, las redes y la infraestructura física.

**4. Aumento de la fiabilidad**

Un proveedor líder de servicios de nube ofrecerá hardware y software de Cloud Security de última generación en el que se puede confiar. Tendrá acceso a un servicio continuo en el que sus usuarios podrán acceder de forma segura a los datos y aplicaciones desde cualquier lugar y en cualquier dispositivo.

## **Mejores prácticas para Cloud Security**

Al mover sus sistemas a la nube, muchos procesos de seguridad y mejores prácticas siguen siendo los mismos. Sin embargo, se encontrará con un nuevo conjunto de desafíos que deberá superar para mantener la seguridad de sus sistemas y datos basados en la nube.

Para ayudarle con este desafío, hemos compilado una serie de mejores prácticas de seguridad para despliegues basados en la nube.

- **Elije un proveedor de confianza**

La base de las mejores prácticas de cloud security se basa en la selección de un proveedor de servicios de confianza. Usted desea asociarse con un proveedor de nubes que ofrezca los mejores protocolos de seguridad incorporados y que se ajuste a los niveles más altos de las mejores prácticas de la industria. Un proveedor de servicios que le extiende un mercado de socios y soluciones para mejorar aún más la seguridad de su despliegue.

La marca de un proveedor de confianza se refleja en el rango de cumplimiento de la seguridad y las certificaciones que poseen. Algo que cualquier buen proveedor pondrá a disposición del público. Por ejemplo, todos los proveedores líderes como [Amazon Web Services](https://aws.amazon.com/compliance/programs/), [Alibaba Cloud](https://www.alibabacloud.com/trust-center), [Google Cloud](https://cloud.google.com/security/compliance/) (que impulsa a Kinsta) y [Azure](https://azure.microsoft.com/en-gb/overview/trusted-cloud/compliance/) ofrecen un acceso transparente en el que se puede confirmar su cumplimiento de seguridad y sus certificaciones.

- **Comprender su modelo de responsabilidad compartida**

Cuando se asocia con un proveedor de servicios en la nube y se trasladan los sistemas y datos a la nube, se entra en una asociación de responsabilidad compartida para la implementación de la seguridad. Una parte crítica de las mejores prácticas implica revisar y comprender su responsabilidad compartida. Descubrir qué tareas de seguridad permanecerán con usted y cuáles serán ahora manejadas por el proveedor. Esta es una escala móvil dependiendo de si se opta por el Software como Servicio (SaaS), Plataforma como Servicio (PaaS), Infraestructura como Servicio (IaaS), o en un centro de datos en las instalaciones.


![Modelo de responsabilidad compartida de Google Cloud Platform](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/05-seguridad-en-redes-2/cloud-security/cloud-security-image-5.jpg)

***Modelo de responsabilidad compartida de Google Cloud Platform***

Los principales proveedores de servicios en la nube como [AWS](https://aws.amazon.com/compliance/shared-responsibility-model/), [Azure](https://gallery.technet.microsoft.com/Shared-Responsibilities-81d0ff91), [Google Cloud Platform](https://cloud.google.com/blog/products/containers-kubernetes/exploring-container-security-the-shared-responsibility-model-in-gke-container-security-shared-responsibility-model-gke) y [Alibaba Cloud](https://files.alicdn.com/tpsservice/8943876c3b1dd53c97a323659e4f679f.pdf?spm=a2c63.o282931.879956.3.5bbf639dVoklbR&file=8943876c3b1dd53c97a323659e4f679f.pdf) publican lo que se conoce como un modelo de responsabilidad compartida para la seguridad. Asegurando la transparencia y la claridad. Asegúrese de revisar su modelo de responsabilidad compartida de los proveedores de servicios en la nube.

- **Revise sus contratos de proveedores de nubes y los acuerdos de nivel de servicio**

Puede que no piense en revisar sus contratos de nubes y SLA como parte de las mejores prácticas de seguridad, debería hacerlo. Los SLA y los contratos de servicio de la nube son sólo una garantía de servicio y recurso en caso de un incidente. Hay mucho más incluido en los términos y condiciones, anexos y apéndices que pueden afectar a su seguridad. Un contrato puede significar la diferencia entre que su proveedor de servicios en la nube sea responsable de sus datos y que los posea.

Según el [McAfee 2019 Cloud Adoption and Risk Report](https://www.mcafee.com/enterprise/en-us/solutions/lp/cloud-adoption-risk.html), el 62,7% de los proveedores de cloud computing no especifican que los datos de los clientes son propiedad del cliente. Esto crea una zona gris legal en la que un proveedor podría reclamar la propiedad de todos sus datos cargados. Compruebe quién es el propietario de los datos y qué pasa con ellos si termina sus servicios. Además, busque claridad sobre si el proveedor está obligado a ofrecer visibilidad de cualquier evento de seguridad y respuestas.

Si no está satisfecho con los elementos del contrato, intente negociar. Si alguno de ellos no es negociable, debe determinar si el acuerdo es un riesgo aceptable para el negocio. Si no lo es, tendrá que buscar opciones alternativas para mitigar el riesgo mediante la codificación, la supervisión o incluso un proveedor alternativo.

- **Entrene a sus usuarios**

Sus usuarios son la primera línea de defensa en la computación segura en la nube. Su conocimiento y aplicación de las prácticas de seguridad puede ser la diferencia entre proteger su sistema o abrir una puerta para los ataques cibernéticos. Como mejor práctica, asegúrese de capacitar a todos sus usuarios – personal y partes interesadas – que acceden a sus sistemas en prácticas de nube segura. Hágalos conscientes de cómo detectar el malware, identificar los correos electrónicos de phishing y los riesgos de las prácticas inseguras.

Para los usuarios más avanzados -como los administradores- que participan directamente en la aplicación de cloud security, considere la capacitación y la certificación específicas de la industria.

- **Controlar el acceso de los usuarios**

La aplicación de un control estricto del acceso de los usuarios mediante políticas es otra de las mejores prácticas de cloud security. Ayudarle a gestionar los usuarios que intentan acceder a sus servicios en la nube. Se debe empezar desde un lugar de cero confianza, sólo permitiendo a los usuarios el acceso a los sistemas y datos que requieren, nada más. Para evitar la complejidad en la aplicación de las políticas, cree grupos bien definidos con funciones asignadas para que sólo concedan acceso a los recursos elegidos. A continuación, podrá añadir usuarios directamente a los grupos, en lugar de personalizar el acceso para cada usuario individual.

- **Asegure sus puntos finales de usuario**

Otro elemento de las mejores prácticas de cloud security es asegurar los puntos finales de los usuarios. La mayoría de los usuarios accederán a sus servicios en la nube a través de los navegadores web. Por lo tanto, es fundamental introducir una seguridad avanzada en el lado del cliente para mantener los navegadores de los usuarios actualizados y protegidos contra los ataques.

También debería considerar la posibilidad de implementar una solución de seguridad de punto final para proteger sus dispositivos de usuario final. Vital con la explosión de los dispositivos móviles y el trabajo a distancia, donde los usuarios acceden cada vez más a los servicios de la nube a través de dispositivos que no son propiedad de la empresa.

Busque una solución que incluya cortafuegos, antivirus y herramientas de seguridad de Internet, seguridad de dispositivos móviles y herramientas de detección de intrusos.

- **Mantener la visibilidad de sus servicios en la nube**

El uso de los servicios de nubes puede ser diverso y fugaz. Muchas organizaciones utilizan múltiples servicios de nube en una variedad de proveedores y geografías. Las investigaciones sugieren que los recursos de la nube tienen un promedio de vida de 2 horas.

Este tipo de comportamiento crea puntos ciegos en su entorno de nubes. Si no puede verlo, no puede asegurarlo.

Asegúrese de implementar una solución de cloud security que ofrezca visibilidad de todo su ecosistema. De este modo, podrá supervisar y proteger el uso de la nube en todos sus recursos, proyectos y regiones dispares a través de un único portal. Esta visibilidad le ayudará a implementar políticas de seguridad granulares y a mitigar una amplia gama de riesgos.

- **Implementar la encriptación**

La encriptación de sus datos es una mejor práctica de seguridad independientemente de la ubicación, crítica una vez que se mueve a la nube. Al utilizar los servicios en la nube, usted expone sus datos a un mayor riesgo al almacenarlos en una plataforma de terceros y enviarlos de ida y vuelta entre su red y el servicio en la nube.

Asegúrese de implementar los más altos niveles de encriptación para los datos tanto en tránsito como en reposo. También debe considerar el uso de sus propias soluciones de encriptación antes de subir los datos a la nube, usando sus propias claves de encriptación para mantener un control total.

Un proveedor de nube puede ofrecer servicios de encriptación incorporados para proteger sus datos de terceros, pero les permite acceder a sus claves de encriptación.

- **Implementar una política de seguridad de contraseñas fuertes**

Una fuerte política de seguridad de contraseñas es la mejor práctica, independientemente del servicio al que se acceda. La aplicación de la política más estricta posible es un elemento importante para evitar el acceso no autorizado. Como requisito mínimo, todas las contraseñas deben requerir una letra mayúscula, una letra minúscula, un número, un símbolo y un mínimo de 14 caracteres. Obligar a los usuarios a actualizar su contraseña cada 90 días y configurarla de manera que el sistema recuerde las últimas 24 contraseñas.

Una política de contraseñas como ésta evitará que los usuarios creen contraseñas simples, en múltiples dispositivos, y los defenderá de la mayoría de los ataques de fuerza bruta. Como una capa adicional de mejores prácticas de seguridad y protección, también debería implementar la autenticación multifactorial. Exigir al usuario que añada dos -o más- pruebas para autentificar su identidad.

- **Usar un Cloud Access Security Broker (CASB)**

El uso de un CASB se está convirtiendo rápidamente en una herramienta central para implementar las mejores prácticas de cloud security. Es un software que se encuentra entre usted y su proveedor de servicios en la nube para extender sus controles de Cloud Security.

Un CASB le ofrece un sofisticado conjunto de herramientas de cloud security para proporcionar visibilidad de su ecosistema en la nube, hacer cumplir las políticas de seguridad de datos, implementar la identificación y protección de amenazas y mantener el cumplimiento.
