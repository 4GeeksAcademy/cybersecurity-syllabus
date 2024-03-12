# seguridad de redes 2

### 

![seguridad%20de%20redes%202%20b55173737ff04e08975955602227137c/image1.png](seguridad%20de%20redes%202%20b55173737ff04e08975955602227137c/image1.png)

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

## **Las 10 recomendaciones de la lista de seguridad para los clientes de la nube**

Cuando se migra a la nube y selecciona un proveedor de servicios, uno de los factores más importantes que se debe considerar es la seguridad. Compartirá y/o almacenará los datos de la empresa con el proveedor de servicios elegido.

Necesita estar seguro de que sus datos están seguros. Hay innumerables factores de seguridad a considerar, desde la responsabilidad compartida hasta si los estándares de seguridad del proveedor están a la altura. Esto puede ser un proceso desalentador, especialmente si no es un experto en seguridad.

### **1. Protección de los datos en tránsito y de los datos en reposo**

Cuando se pasa a un servicio en la nube, un elemento clave de la seguridad es la protección de los datos en tránsito entre usted (el usuario final) y el proveedor. Esta es una responsabilidad doble tanto para usted como para el proveedor. Necesitará protección de la red para evitar la interceptación de datos y encriptación para evitar que un atacante lea cualquier dato en caso de ser interceptado.

Busque un proveedor de servicios que le ofrezca un conjunto de herramientas para ayudarle a cifrar fácilmente sus datos en tránsito y en reposo. Esto garantizará el mismo nivel de protección para cualquier tránsito de datos interno dentro del proveedor de servicios en la nube, o el tránsito entre el proveedor de servicios en la nube y otros servicios en los que las API pueden estar expuestas.

### **2. Protección de activos**

Cuando selecciona un proveedor de servicios de nube, es necesario comprender la ubicación física de donde se almacenan, procesan y gestionan los datos. Esto es especialmente importante después de la implementación de regulaciones gubernamentales e industriales como la GDPR.

Para asegurar que sus activos estén protegidos, un buen proveedor tendrá una protección física avanzada en su centro de datos para defender sus datos de accesos no autorizados. También se asegurarán de que sus activos de datos se borren antes de que se reabastezcan o se eliminen los recursos para evitar que caigan en las manos equivocadas.

### **3. Visibilidad y control**

Un factor clave en la seguridad es la capacidad de ver y controlar sus propios datos. Un buen proveedor de servicios le ofrecerá una solución que le proporcionará una visibilidad total de sus datos y de quién está accediendo a ellos, independientemente de dónde estén y de dónde usted se encuentre.

Su proveedor debe ofrecer un monitoreo de la actividad para que pueda descubrir los cambios de configuración y seguridad en todo su ecosistema. Así como apoyar el cumplimiento de la integración de soluciones nuevas y existentes.

### **4. Mercado de seguridad de confianza y red de asociados**

Para asegurar el despliegue de la nube se necesitará más de una solución o socio. Un buen proveedor de servicios en la nube le facilitará la búsqueda y la conexión con diferentes socios y soluciones a través de un mercado.

Busque un proveedor con un mercado que ofrezca una red curada de socios de confianza con un historial de seguridad probado. El mercado también debería ofrecer soluciones de seguridad que proporcionen un despliegue con un solo clic y que sean complementarias para asegurar sus datos, ya sea que opere en un despliegue de nube público, privado o híbrido.

### **5. Gestión segura de los usuarios**

Un buen proveedor de servicios en la nube ofrecerá herramientas que permitan la gestión segura de los usuarios. Esto ayudará a impedir el acceso no autorizado a las interfaces y procedimientos de gestión para garantizar que las aplicaciones, los datos y los recursos no se vean comprometidos.

El proveedor de la nube también debe ofrecer funcionalidad para implementar protocolos de seguridad que separen a los usuarios y eviten que cualquier usuario malicioso (o comprometido) afecte a los servicios y datos de otro.

### **6. Integración de la conformidad y la seguridad**

Cuando se considera un proveedor de servicios en la nube, la seguridad y el cumplimiento van de la mano. Deben cumplir los requisitos de cumplimiento global que son validados por una organización tercera. Usted desea un proveedor de servicios en la nube que siga las mejores prácticas de la industria en materia de Cloud Security e idealmente tenga una certificación reconocida.

El programa de Registro de Seguridad, Confianza y Garantía de la Alianza de Cloud Security (STAR) es un buen indicador. Además, si usted está operando en una industria altamente regulada – donde HIPPA, PCI-DSS, y [GDPR](https://kinsta.com/es/blog/cumplimiento-gdpr/) podrían aplicarse – también tendrá que identificar un proveedor con certificación específica de la industria.

Para asegurar que sus esfuerzos de cumplimiento son rentables y eficientes, el proveedor de servicios en la nube debe ofrecerle la posibilidad de heredar sus controles de seguridad en sus propios programas de cumplimiento y certificación.

### **7. Identidad y autenticación**

El proveedor cloud debe asegurarse de que el acceso a cualquier interfaz de servicio se limite únicamente a las personas autorizadas y autenticadas. Cuando se trata de proveedores, se desea un servicio que ofrezca características de identidad y autenticación, incluyendo nombre de usuario y contraseña, autenticación de dos factores, certificados de cliente TLS y federación de identidad con su proveedor de identidad existente.

También quiere la posibilidad de restringir el acceso a una línea dedicada, empresa o red comunitaria. Un buen proveedor sólo entrega autenticación a través de canales seguros – como HTTPS – para evitar la interceptación. Asegúrese de evitar los servicios con prácticas de autenticación débiles. Esto expondrá sus sistemas a un acceso no autorizado que conducirá a un robo de datos, cambios en su servicio o una denegación de servicio. También evite la autenticación por correo electrónico, HTTP o teléfono.

Son extremadamente vulnerables a la ingeniería social y a la interceptación de credenciales de identidad y autenticación.

### **8. Seguridad operacional**

Al seleccionar un servicio cloud, busque un proveedor que implemente una fuerte seguridad operacional para detectar y prevenir los ataques. Esto debería cubrir cuatro elementos básicos:

- **Configuración y gestión de cambios:** Quiere un proveedor que ofrezca transparencia en los activos que componen el servicio, incluyendo cualquier configuración o dependencia. Deben informarle de cualquier cambio en el servicio que pueda afectar a la seguridad para garantizar que no se produzcan vulnerabilidades.
- **Gestión de vulnerabilidades:** Su proveedor debe contar con un proceso de gestión de la vulnerabilidad para detectar y mitigar cualquier nueva amenaza a su servicio. Se le debe mantener informado de estas amenazas, su gravedad y el calendario de mitigación de amenazas previsto, que incluye su resolución.
- **Vigilancia de protección:** Cualquier proveedor que valga la pena contará con herramientas avanzadas de monitoreo para identificar cualquier ataque, mal uso o mal funcionamiento del servicio. Tomarán medidas rápidas y decisivas para hacer frente a cualquier incidente, manteniéndole informado del resultado.
- **Gestión de incidentes:** Su proveedor ideal tendrá un proceso de gestión de incidentes planificado de antemano para los tipos comunes de ataques. Estarán listos para desplegar este proceso en respuesta a cualquier ataque.

<aside>
👉 Habrá una ruta de contacto clara para informar de cualquier incidente, con un plazo y un formato aceptables.

</aside>

### **9. Seguridad del personal**

Necesita un proveedor de servicios en la nube en cuyo personal pueda confiar, ya que tendrá acceso a sus sistemas y datos. El proveedor de servicios en la nube que elija tendrá un proceso de control de seguridad riguroso y transparente.

Deberían poder verificar la identidad de su personal, el derecho al trabajo y comprobar si hay condenas penales pendientes. Lo ideal es que se ajusten a las normas de selección establecidas localmente en sus países, como [BS 7858:2019 para el Reino Unido](https://standardsdevelopment.bsigroup.com/projects/2018-02194) o rellenar el [formulario I-9 en los EE.UU](https://www.uscis.gov/i-9).

Además de la selección, se necesita un proveedor de servicios que se asegure de que su personal comprende sus responsabilidades inherentes de seguridad y se somete a una formación regular. También deben tener una política para minimizar el número de personas que tienen acceso a sus servicios y que pueden afectarlos.

### **10. Uso seguro del servicio**

Puede elegir un proveedor de nube con una seguridad de vanguardia y aún así experimentar una brecha a través de un mal uso del servicio. Es importante entender dónde están las responsabilidades de seguridad cuando se utiliza el servicio. Su nivel de responsabilidad será influenciado por su modelo de despliegue de nubes, la forma en que utiliza cualquier servicio y las características incorporadas de cualquier servicio individual.

Por ejemplo, tiene importantes responsabilidades de seguridad con IaaS. Desplegando una instancia de computación, la responsabilidad recaería en usted para instalar un sistema operativo moderno, configurar la seguridad, y garantizar los parches y el mantenimiento en curso. Lo mismo es cierto para cualquier aplicación que se despliegue en esa instancia. Por lo tanto, asegúrese de que entiende los requisitos de seguridad del servicio elegido y las opciones de configuración de seguridad disponibles. Asegúrese también de educar a su personal en el uso seguro de sus servicios elegidos.

## Seguridad de los dispositivos móviles

La seguridad móvil se refiere a las estrategias, infraestructuras y software que se utilizan para proteger cualquier dispositivo móvil que viaja junto con los usuarios, incluyendo smartphones, tabletas y notebooks. La seguridad en los dispositivos móviles incluye la protección de datos en el dispositivo local, en los endpoints conectados al dispositivo y en los equipos de redes. Mientras estos dispositivos sigan siendo los preferidos por los usuarios, en vez de los equipos de sobremesa, seguirán siendo los principales objetivos para los hackers.

### **¿Por qué es tan importante la seguridad móvil?**

Como cada vez más usuarios viajan y trabajan desde casa, los dispositivos móviles se han integrado cada vez más en sus vidas diarias, incluyendo a los empleados de corporaciones. La actividad de navegación web solía estar limitada a los ordenadores de sobremesa y los únicos que tenían ordenadores portátiles eran los empleados que tenían que viajar por trabajo. Ahora, los teléfonos móviles, notebooks y tabletas son los más utilizados para navegar por internet y el tráfico proveniente de estos dispositivos se ha convertido en la principal forma de navegación, por delante de los PC.

Los dispositivos móviles ofrecen una superficie de ataque mucho mayor que los ordenadores de escritorio, lo que los vuelve una amenaza más grave para la seguridad corporativa. Una computadora de sobremesa no se mueve, así que la mayoría de las amenazas que soporta vienen del exterior, pero estos dispositivos son vulnerables ante ataques físicos y virtuales. Los usuarios los llevan consigo a dondequiera que van, así que los administradores deben preocuparse más por los ataques físicos (por ejemplo, robo y pérdida) y amenazas virtuales de aplicaciones externas y redes Wi-Fi (por ejemplo, ataques de intermediario). Los ordenadores de sobremesa estacionarios no se mueven de la red corporativa, lo que les facilita a los administradores controlar la seguridad tanto en la red como en los puntos de contacto. En el caso de los dispositivos móviles, los usuarios pueden hacerles rooting (obtener control privilegiado del directorio raíz), agregar cualquier aplicación o perderlos físicamente.

<aside>
💡 Por estas razones y muchas otras, las corporaciones enfrentan unos costes muy superiores a la hora de crear estrategias de seguridad informática en dispositivos móviles. Incluso con los costes adicionales, es una parte crítica de la ciberseguridad, puesto que estos aparatos constituyen amenazas significativas para la integridad de los datos.

</aside>

El futuro de la informática y la comunicación está en los dispositivos móviles, como laptops, tabletas y smartphones con capacidades de computadoras de escritorio. Su tamaño, sistemas operativos, aplicaciones y potencia de procesamiento los hacen ideales para utilizarlos desde cualquier lugar con conexión a Internet. Y con la expansión de los dispositivos reforzados, el Internet de las cosas (IoT) y los sistemas operativos, como Chrome OS, Linux y Windows, cualquier pieza de hardware que se mejore con este software y estas capacidades se convierte en un dispositivo informático móvil.

Dado que los dispositivos móviles se han vuelto más accesibles y portátiles, las organizaciones y los usuarios han preferido comprarlos y utilizarlos en lugar de las computadoras de escritorio. Y con el omnipresente acceso inalámbrico a Internet, todas las variedades de dispositivos móviles son cada vez más vulnerables a los ataques y a las violaciones de datos.

La autenticación y la autorización a través de dispositivos móviles ofrecen comodidad, pero aumentan el riesgo al eliminar las limitaciones de un perímetro empresarial seguro. Por ejemplo, las capacidades de un teléfono inteligente aumentan con las pantallas multitáctiles, los giroscopios, los acelerómetros, el GPS, los micrófonos, las cámaras de varios megapíxeles y los puertos, lo que permite acoplar más dispositivos. Estas nuevas capacidades cambian la forma de autenticar a los usuarios y de dar autorización localmente al dispositivo y a las aplicaciones y servicios de una red. Como resultado, las nuevas capacidades también están aumentando el número de puntos finales que necesitan protección frente a las amenazas de ciberseguridad.

Hoy en día, los ciberdelincuentes pueden hackear automóviles, cámaras de seguridad, monitores de bebés y dispositivos implantados de asistencia médica. Y para 2025, podría haber más de 75 000 millones de "cosas" conectadas a Internet, como cámaras, termostatos, cerraduras de puertas, televisores inteligentes, monitores de salud, dispositivos de iluminación y muchos otros dispositivos.

## Amenazas y vulnerabilidades de la seguridad de los dispositivos móviles

### **Amenazas para aplicaciones**

Los administradores pueden bloquear la instalación de aplicaciones en un ordenador de escritorio, pero un usuario puede instalar cualquier cosa en un dispositivo móvil. Las aplicaciones externas introducen diversos problemas de seguridad para estos dispositivos. Las corporaciones deben crear políticas de seguridad que ayuden a los usuarios a comprender los peligros de instalar aplicaciones externas no aprobadas.

Los usuarios no deberían ser capaces de rootear o crear un superusuario en sus teléfonos, pero algunos de ellos lo hacen, lo que inutiliza efectivamente los controles de seguridad del sistema. Las aplicaciones externas que se ejecutan en dispositivos rooteados pueden revelar datos a un hacker, si este usa determinados métodos de ataque. Las aplicaciones externas también pueden contener programas de malware y keyloggers en su código fuente. Es posible instalar programas antimalware, pero los dispositivos que han sido rooteados dejan incluso a estas aplicaciones susceptibles a la manipulación de malware.

Aunque sin duda es fundamental establecer y aplicar una política de seguridad para toda la empresa, una política por sí sola no basta para contrarrestar el volumen y la variedad de las amenazas móviles actuales. En 2019, [Verizon realizó un estudio (PDF, 77 KB, enlace externo a ibm.com)](https://www.verizon.com/business/resources/reports/ves-msi-infographic.pdf) con empresas líderes en seguridad móvil, entre ellas IBM, Lookout y Wandera, encuestando a 670 profesionales de la seguridad. El estudio reveló que 1 de cada 3 de los encuestados informó de un incidente relacionado con un dispositivo móvil. El 47% afirma que la corrección fue "difícil y costosa", y el 64% señala que que sufrieron tiempos de inactividad.

Y las empresas que adoptan políticas de traiga su propio dispositivo" (BYOD) también se abren a mayores riesgos de seguridad. Permiten que dispositivos posiblemente inseguros accedan a servidores corporativos y bases de datos sensibles, exponiéndolos a ataques. Los ciberdelincuentes y estafadores pueden explotar estas vulnerabilidades y causar daños o perjuicios al usuario y a la organización. Buscan secretos comerciales, información privilegiada y acceso no autorizado a una red segura para encontrar cualquier cosa que pueda ser rentable.

### **Phishing**

El phishing, la principal amenaza para la seguridad móvil, es un intento de estafa para robar las credenciales o los datos confidenciales de los usuarios, como los números de las tarjetas de crédito. Los estafadores envían a los usuarios correos electrónicos o mensajes SMS (mensajes de texto breves), comúnmente conocidos como mensajes de texto, diseñados para parecer que proceden de una fuente legítima, utilizando hipervínculos falsos.

### **Malware y ransomware**

El [malware](https://www.ibm.com/mx-es/topics/malware) móvil es un software no detectado, como una aplicación maliciosa o un programa espía, creado para dañar, desarticular u obtener acceso ilegítimo a un cliente, una computadora, un servidor o una red informática. El ransomware, una forma de malware, amenaza con destruir o retener los datos o archivos de una víctima a menos que se pague un rescate para desencriptar los archivos y restaurar el acceso.

### **Cryptojacking**

El criptojacking, una forma de malware, utiliza la potencia informática de una organización o de una persona sin su conocimiento para minar criptomonedas, disminuyendo la capacidad de procesamiento y la eficacia de un dispositivo.

### **Red Wi-Fi no segura**

Los puntos de acceso wifi no seguros sin una red privada virtual (VPN) hacen que los dispositivos móviles sean más vulnerables a los ciberataques. Los ciberdelincuentes pueden interceptar el tráfico y robar información privada utilizando métodos como los ataques de intermediario. Los ciberdelincuentes también pueden engañar a los usuarios para que se conecten a puntos de acceso fraudulentos, lo que facilita la extracción de datos corporativos o personales.

Los equipos de trabajo móviles, y especialmente los del tipo “traiga su propio dispositivo” (o BYOD, del inglés “*Bring Your Own Device*”), pueden crear una amenaza para la red interna. No es raro que el malware escanee la red para abrir ubicaciones de almacenamiento abiertas o recursos vulnerables para insertar ejecutables malintencionados y explotarlos. Esto puede ocurrir de manera furtiva en un dispositivo móvil que no esté adecuadamente protegido.

Los administradores pueden obligar a cualquier persona que tenga un BYOD a instalar programas antimalware, pero esto no garantiza que el software esté actualizado. Si la corporación ofrece redes Wi-Fi públicas para los clientes y empleados, esto también puede ser un punto de preocupación. Cuando los empleados se conectan a redes Wi-Fi públicas y transfieren sus datos a lugares en que otros usuarios pueden leerlos, esto deja la red vulnerable ante ataques de intermediario (MitM, por las siglas en inglés de “*Man in the Middle*”) y posible apropiación de cuenta, si el atacante roba las credenciales.

### **Sistemas operativos obsoletos**

Los sistemas operativos más antiguos suelen contener vulnerabilidades que han sido explotadas por los ciberdelincuentes, y los dispositivos con OS obsoletos siguen siendo vulnerables a los ataques. Las actualizaciones de los fabricantes suelen incluir parches de seguridad críticos para hacer frente a las vulnerabilidades que pueden ser explotadas activamente.

### **Permisos excesivos de las aplicaciones**

Las aplicaciones móviles tienen el poder de comprometer la privacidad de los datos a través de los permisos excesivos de las aplicaciones. Los permisos de las aplicaciones determinan la funcionalidad de una aplicación y su acceso al dispositivo del usuario y a sus funciones, como el micrófono y la cámara. Algunas aplicaciones son más peligrosas que otras. Algunas pueden verse comprometidas, y los datos confidenciales pueden canalizarse a través de terceros no confiables.

### **Amenazas basadas en la web y endpoints**

Las aplicaciones móviles se conectan a los datos y a las aplicaciones internas mediante endpoints o puntos finales de contacto. Estos endpoints reciben y procesan datos, y después devuelven una respuesta al dispositivo móvil. Tanto los endpoints como cualquier aplicación basada en la web, agregan nuevas amenazas para las organizaciones. Los endpoints usados por la aplicación deben codificarse correctamente con los controles de autenticación adecuados para detener a los atacantes. Unos endpoints protegidos de manera incorrecta podrían ser objetivos para un hacker dispuesto a usarlos para comprometer la aplicación y robar datos.

Como los teléfonos móviles y notebooks son cada vez más populares, algunos ataques basados en web se dirigen a estos usuarios. Los atacantes usan las páginas que lucen como las oficiales para engañar a los usuarios para que carguen datos delicados o descarguen aplicaciones malintencionadas. No es raro que un atacante le diga a un usuario que debe descargar una aplicación específica para poder ver un video u otro tipo de medios. Los usuarios descargan la aplicación sin darse cuenta de que es una app malintencionada que se usa para analizar los dispositivos en busca de vulnerabilidades y para revelar datos.

## **Medidas de seguridad para la seguridad de los dispositivos móviles**

La protección de los dispositivos móviles requiere un enfoque unificado y multicapa. Hay componentes esenciales para la seguridad de los dispositivos móviles, pero cada enfoque puede ser un poco diferente. Para optimizar la seguridad, debe encontrar el enfoque que mejor se adapte a su red.

Los requisitos básicos de seguridad siguen siendo los mismos para los dispositivos móviles que para las computadoras no móviles. En general, los requisitos son mantener y proteger la confidencialidad, la integridad, la identidad y el no repudio.

Sin embargo, las tendencias actuales en materia de seguridad móvil crean nuevos retos y oportunidades, que requieren una redefinición de la seguridad para los dispositivos informáticos personales. Por ejemplo, las capacidades y expectativas varían según el factor de forma del dispositivo (su forma y tamaño), los avances en las tecnologías de seguridad, la rápida evolución de las tácticas de amenaza y la interacción del dispositivo, como el tacto, el audio y el video.

Las organizaciones de TI y los equipos de seguridad deben reconsiderar cómo lograr los requisitos de seguridad a la luz de las capacidades de los dispositivos, el panorama de las amenazas móviles y las expectativas cambiantes de los usuarios. En otras palabras, estos profesionales necesitan asegurar múltiples vulnerabilidades dentro del entorno dinámico y de crecimiento masivo de los dispositivos móviles. Un entorno móvil seguro ofrecerá protección en al menos seis áreas principales: gestión de la movilidad empresarial, seguridad del correo electrónico, protección de los puntos finales, VPN, gateways seguros y corredor de acceso a la nube.

Las organizaciones que usan dispositivos digitales móviles tienen diversas opciones para protegerlos contra atacantes. Los componentes de la seguridad informática en dispositivos móviles se pueden usar para definir las estrategias de ciberseguridad. Además de la infraestructura agregada a la estrategia corporativa, también es importante crear políticas para estos dispositivos y BYOD que indiquen a los usuarios qué se puede instalar o no en el dispositivo.

Los siguientes componentes ayudan a cualquier organización a protegerse de ataques dirigidos a los equipos de trabajo móviles:

- **Escáneres de penetración:** es posible usar servicios de escaneo automático para hallar vulnerabilidades en los endpoints. Si bien esta no es la única medida de ciberseguridad que se puede emplear en puntos de contacto, sí es el primer paso para identificar problemas de autenticación y autorización que podrían usarse para comprometer datos.
- **VPN:** una red privada virtual o VPN, por sus siglas en inglés, es una conexión cifrada a Internet desde un dispositivo a una red. La conexión cifrada ayuda a garantizar la transmisión segura de datos confidenciales. Evita que las personas no autorizadas espíen el tráfico y permite que el usuario remoto trabaje de manera segura. Los usuarios que se conecten a una red desde una ubicación remota siempre deben usar VPN. Los servicios de VPN y las alternativas de VPN siempre activadas, instaladas en un dispositivo móvil encriptan los datos del dispositivo móvil al endpoint o desde el dispositivo móvil a la red interna. Gran cantidad de servicios externos se configuran específicamente para proteger el tráfico corporativo de un dispositivo móvil a la red interna.
- **Auditoría y control de dispositivos:** si bien los administradores no pueden controlar remotamente un teléfono móvil o una tableta, sí pueden obligar a los usuarios a instalar programas de borrado y localización remotos. Los GPS se pueden usar para localizar dispositivos robados, y el software de borrado remoto elimina todos los datos críticos si estos resultan robados.
- **Seguridad para correo electrónico:** el phishing es una de las principales amenazas para cualquier organización. Los servicios de correo electrónico suelen agregarse a un dispositivo móvil para que los usuarios puedan acceder a sus emails. Cualquier mensaje que contenga phishing puede atacar a dispositivos móviles con vínculos o archivos adjuntos malintencionados. Los filtros de correo electrónico deben bloquear a aquellos mensajes que contengan enlaces y archivos adjuntos malintencionados.
- **Seguridad de endpoint:** a medida que las organizaciones incorporan fuerza de trabajo móvil y flexible, deben implementar redes que permiten el acceso remoto. Las soluciones de seguridad de endpoint protegen a las corporaciones mediante el monitoreo de los archivos y procesos de cada dispositivo móvil que accede a la red. Al detectar constantemente la conducta maliciosa, la seguridad del endpoint puede identificar las amenazas de manera temprana. Cuando detectan conducta maliciosa, las soluciones de endpoint alertan rápidamente a los equipos de seguridad, de manera que las amenazas se eliminan antes de que puedan causar daño alguno. Con tecnologías como el móvil, el IoT y la nube, las organizaciones conectan nuevos y diferentes puntos finales a su entorno de respuesta. La seguridad de los puntos finales incluye la protección antivirus, la prevención de la pérdida de datos, el cifrado de los puntos finales y la gestión de la seguridad de los puntos finales.
- **Puerta de enlace web segura:** las puertas de enlace web seguras ofrecen seguridad en la nube potente e integral. Como el 70 por ciento de los ataques son específicos de cada organización, las empresas necesitan que la seguridad en la nube identifique los ataques ya usados antes del lanzamiento. La seguridad en la nube puede funcionar en las capas de DNS e IP para protegerlo de la suplantación de identidad (phishing), el malware y el ransomware de manera temprana. Al integrar la seguridad en la nube, puede identificar un ataque en una ubicación y prevenirlo de inmediato en otras sucursales.
- **Seguridad de correo electrónico:** el correo electrónico es la herramienta de comunicación empresarial más importante y el principal vector de ataque para cometer violaciones de seguridad. La seguridad de correo electrónico adecuada incluye capacidades avanzadas de protección contra amenazas que detectan, bloquean y resuelven las amenazas más rápidamente; evitan la pérdida de datos; y protegen la información importante en tránsito con cifrado de extremo a extremo. Para proteger los datos de las ciberamenazas basadas en el correo electrónico, como el malware, el robo de identidad y las estafas de phishing, las organizaciones deben supervisar el tráfico de correo electrónico de forma proactiva. Una protección adecuada del correo electrónico incluye servicios antivirus, antispam, de control de imágenes y de control de contenidos.
- **Agente de seguridad de acceso a la nube:** Un CASB es un punto de aplicación de políticas entre los usuarios y los proveedores de servicios en la nube (CSP). Supervisa la actividad relacionada con la nube y aplica las normas de seguridad, cumplimiento y gobernanza en torno al uso de los recursos basados en la nube. Su red debe proteger el lugar y la manera en que trabajan los empleados, incluida la nube. Necesitará un agente de seguridad de acceso a la nube (CASB), una herramienta que funciona como puerta de enlace entre la infraestructura en las instalaciones y las aplicaciones en la nube (Salesforce, Dropbox, etc.). Un CASB identifica las aplicaciones maliciosas en la nube y protege contra violaciones a la seguridad con un motor de prevención de pérdida de datos (DLP) en la nube.
- **Gestión de la movilidad empresarial:** La gestión de la movilidad empresarial (EMM) es un conjunto colectivo de herramientas y tecnologías que mantienen y gestionan cómo se utilizan los dispositivos móviles y portátiles dentro de una organización para las operaciones empresariales rutinarias.

## Seguridad web

### **Conceptos básicos de la seguridad web**

Cambiar las contraseñas con frecuencia, bloquear los dispositivos y mantener el software actualizado son prácticas de seguridad habituales. Sin embargo, la seguridad de una aplicación puede ser a menudo un elemento ignorado y vulnerable.

Las aplicaciones web tienen una alta probabilidad de enfrentarse a amenazas desencadenadas por diversos factores: fallos del sistema debidos a una codificación incorrecta, servidores mal configurados y problemas de diseño de la aplicación.

Las vulnerabilidades en el código de una aplicación o en el sistema operativo pueden ser aprovechadas por los ciberdelincuentes para acceder a bases de datos, servidores y otros datos sensibles. Aprovechando la exposición de los datos sensibles, los hackers proceden a lanzar ataques de ransomware u otras formas de fraude en línea.

Teniendo en cuenta que el **[43% de las violaciones de datos](https://securityboulevard.com/2020/05/43-of-data-breaches-connected-to-application-vulnerabilities-assessing-the-appsec-implications/)** son causadas por las vulnerabilidades de las aplicaciones, adoptar las mejores prácticas y las herramientas adecuadas es fundamental para mitigar los riesgos y reforzar la seguridad de las aplicaciones web.

En esta guía, cubriremos qué es la seguridad de las aplicaciones web, cómo funciona y qué herramientas puedes utilizar para asegurar tu aplicación web.

### **¿Qué es la seguridad en aplicaciones web?**

Como parte de la ciberseguridad, la seguridad en aplicaciones web se centra en salvaguardar los sitios web, las aplicaciones basadas en la web y los servicios en línea de una variedad de ataques maliciosos, garantizando su buen funcionamiento y rendimiento.

## **Amenazas y vulnerabilidades de la seguridad web**

Las vulnerabilidades de las aplicaciones web permiten a los delincuentes obtener un control no autorizado del código fuente, manipular información privada o interrumpir el funcionamiento normal de la aplicación.

La organización internacional sin fines de lucro dedicada a la seguridad de las aplicaciones web **[OWASP](https://owasp.org/www-project-top-ten/)** ha revelado los 10 principales riesgos de seguridad de la capa de aplicaciones web. Veamos algunos de los ataques más comunes contra las aplicaciones web.

### **Inyección SQL**

Este tipo de fallo permite a un atacante manipular las consultas a la base de datos de una aplicación inyectando código. En la mayoría de los ataques, los hackers pueden recuperar datos pertenecientes a otros usuarios o relacionados con la propia aplicación, como contraseñas, datos de tarjetas de crédito y cookies.

Cuando un ataque de inyección SQL sale mal, el atacante puede intentar un ataque de denegación de servicio o comprometer el servidor subyacente u otra infraestructura de back-end.

### **Secuencia de comandos en sitios cruzados (XSS)**

Se trata de una técnica muy utilizada para ejecutar código, normalmente JavaScript, en el sitio web o la aplicación objetivo. Una secuencia de comandos en sitios cruzados exitosa otorga a los atacantes acceso a toda la aplicación.

Un ejemplo de ataque XSS es cuando un hacker explota la vulnerabilidad de un campo de entrada y lo utiliza para inyectar código malicioso en otro sitio web.

Los hackers tienen un control total sobre lo que ocurre una vez que sus objetivos hacen clic en el enlace infectado. La razón principal por la que el XSS se considera un fallo de seguridad de alto riesgo es que permite al atacante ver los datos almacenados en LocalStorage, SessionStorage o cookies en el sistema de destino. Por lo tanto, no se debe almacenar ningún dato personal en estos sistemas.

### **Falsificación de peticiones en sitios cruzados (CSRF)**

Un ataque CSRF emplea técnicas de ingeniería social para convencer a un usuario de que modifique los datos de la aplicación, como el nombre de usuario o la contraseña. Un ataque CSRF requiere una aplicación que utilice cookies de sesión únicamente para identificar al usuario que realiza una solicitud. Estas cookies se utilizan entonces para rastrear o validar las solicitudes del usuario.

Dependiendo de la acción que el usuario es forzado a completar, el atacante puede robar dinero, cuentas o realizar otros ataques a la aplicación web.

### **Relleno de credenciales**

Los hackers utilizan nombres de usuario, correos electrónicos y contraseñas de volcados de datos disponibles públicamente en la dark web para hacerse con las cuentas de los usuarios. Los datos ilegales pueden contener millones de combinaciones de nombres de usuario y contraseñas debido a años de violaciones de datos en numerosos sitios. Esto demuestra que incluso los datos antiguos pueden ser valiosos para los atacantes.

El robo de credenciales es muy peligroso, sobre todo en las finanzas. El relleno de credenciales financieras proporciona a los ciberdelincuentes un acceso claro a toda la información de tu cuenta bancaria y de tus transacciones, lo que les permite solicitar préstamos, utilizar tus tarjetas de crédito o realizar transferencias bancarias.

### **Creación de cuentas falsas**

Normalmente, muchas empresas promueven la creación de cuentas para seguir el comportamiento de sus clientes y compartir las últimas ofertas. Esto hace que el registro rápido y sencillo sea un elemento importante, pero la seguridad puede pasarse por alto. Por lo tanto, puede ser tan fácil para los delincuentes crear cuentas falsas como cualquier otro cliente legítimo.

Los hackers pueden crear un número importante de cuentas de usuario que no están vinculadas a una persona real o que se hacen utilizando información personal robada. Estas cuentas falsas pueden utilizarse para encubrir prácticas de relleno de credenciales, aprovechar ofertas de clientes o autenticar tarjetas de crédito robadas.

Los ataques de creación de cuentas falsas son cada vez más difíciles de detectar y prevenir, ya que los hackers buscan constantemente nuevas formas de falsificar o robar identidades.

### **Desconfiguración de la seguridad**

Otra vulnerabilidad de alto riesgo de las aplicaciones web es la desconfiguración de la seguridad, que permite a los atacantes tomar fácilmente el control de los sitios web. Los atacantes malintencionados pueden aprovecharse de una amplia gama de debilidades y errores de configuración, incluyendo páginas no utilizadas, vulnerabilidades no parcheadas, archivos y directorios no seguros y configuraciones por defecto.

Elementos como los servidores web y de aplicaciones, las bases de datos o los servicios de red pueden dejarte expuesto a violaciones de datos. Los hackers pueden manipular cualquier información privada y tomar el control de las cuentas de usuario y de administrador.

### **Fallo de autorización**

Los visitantes de un sitio web o de una aplicación sólo pueden acceder a ciertas partes del mismo si tienen los permisos adecuados: esto se debe a los controles de acceso. Si, por ejemplo, gestionas un sitio web que permite a diferentes vendedores publicar sus productos, tienes que darles acceso para añadir nuevos productos y gestionar sus ventas.

Así, hay ciertas limitaciones para los clientes que no son vendedores que los hackers pueden explotar. Pueden encontrar formas de comprometer el control de acceso y liberar datos no autorizados como resultado de la modificación de los permisos de acceso de los usuarios y los archivos.

### **Inclusión de archivos locales (LFI)**

LFI es una vulnerabilidad frecuentemente descubierta en aplicaciones web mal construidas. Permite a un atacante incluir o exponer archivos en un servidor.

Si la aplicación web ejecuta el archivo, puede exponer datos sensibles o incluso ejecutar código malicioso.

## **Medidas de seguridad en la web**

### **¿Cómo funciona la seguridad en aplicaciones web?**

Además de preservar la tecnología y las características utilizadas en el desarrollo de aplicaciones, la seguridad en aplicaciones web también establece un alto nivel de protección hacia los servidores y procesos. Además, protege los servicios web, como las API, contra las amenazas en línea.

El aspecto crítico de la seguridad en las aplicaciones web es garantizar que las aplicaciones funcionen de forma segura y sin problemas en todo momento. Para lograr este objetivo, se puede empezar con un testing de seguridad en profundidad.

El testing de seguridad implica descubrir y arreglar todas las vulnerabilidades antes de que los hackers lleguen a ellas. Por ello, es muy recomendable realizar el testing en aplicaciones web durante las etapas del SDLC (ciclo de vida del desarrollo de software), y no después de que la aplicación web haya sido lanzada.

A continuación, se presentan algunas medidas de seguridad eficaces que pueden ayudar a proteger tu aplicación web.

### **Realizar una auditoría de seguridad exhaustiva**

Las auditorías de seguridad periódicas son un método excelente para garantizar que se siguen las mejores prácticas de seguridad en tu aplicación web y encontrar rápidamente cualquier fallo potencial en tus sistemas. Una auditoría de seguridad no sólo puede ayudarte a estar al tanto de las posibles vulnerabilidades, sino también a proteger tu negocio.

Para garantizar una perspectiva completa y objetiva en tu proceso de auditoría de seguridad, lo mejor es contratar a un profesional. Con su amplia experiencia y conocimientos, será un activo valioso para identificar y mitigar las vulnerabilidades que requieren la gestión de parches u otras correcciones. Tras completar una evaluación de seguridad, el siguiente paso es abordar todos los fallos descubiertos. Un buen enfoque es establecer prioridades basadas en el nivel de impacto de cada tipo de vulnerabilidad.

Asegúrate de realizar escaneos de vulnerabilidad y actualizaciones consistentes. Para hacer las cosas más eficientes, realiza tus pruebas de seguridad en aplicaciones web utilizando tus escáneres de vulnerabilidad para buscar los principales ataques de inyección como la inyección SQL, el cross-site scripting y los ataques DDoS en lugar de escanear todo tipo de vulnerabilidades. Además, no olvides asegurarte de que todos los servidores en los que se alojan tus aplicaciones web están actualizados con los últimos parches de seguridad.

### **Encriptar todos los datos**

Cuando alguien utiliza tu aplicación web, puede revelar información sensible. Esta información no debe ser accesible a ninguna parte no autorizada. Por lo tanto, es fundamental garantizar que tu aplicación web proporcione cifrado de datos durante el tránsito y en reposo. Aquí es donde el **cifrado SSL/TLS** juega un papel vital.

Cuando utilizas el cifrado SSL/TLS, utilizas una versión más segura del protocolo HTTP, HTTPS, y proteges todas las comunicaciones con tus visitantes. Sin conexiones cifradas con SSL, tanto los sitios web como las aplicaciones tienen un cifrado débil que puede poner en peligro la gestión de la sesión y el sistema de seguridad general. Consulta la comparación entre **HTTP y HTTPS** y cómo puede beneficiar a tu sitio tener un SSL. Al implementar medidas de seguridad como el protocolo HTTPS, estás construyendo una mejor presencia en línea y mejorando el rendimiento SEO.

### **Supervisar la seguridad en aplicaciones web en tiempo real**

Para asegurarte de que tu aplicación web está protegida las 24 horas del día, necesitas algo más que una auditoría de seguridad para identificar y corregir todas sus vulnerabilidades. Aquí es donde son necesarios los Firewalls de Aplicaciones Web (WAF).

Básicamente, un WAF gestiona todos los aspectos de la supervisión en tiempo real de los aspectos de seguridad de tu aplicación web, como la gestión de sesiones. Esto significa que bloquea los posibles ataques a la capa de aplicación en tiempo real, como los ataques DDoS, inyección SQL, XSS y ataques CSRF.

### **Aplicar prácticas de registro adecuadas**

Es posible que los escáneres de aplicaciones web y los firewalls no sean capaces de detectar todos los fallos de seguridad desde el principio. Por lo tanto, uno de los enfoques a tomar es la práctica de un registro adecuado. Las herramientas de registro como **[Retrace](https://stackify.com/retrace/)**, **[Logstash](https://www.elastic.co/es/logstash/)** o **[Graylog](https://www.graylog.org/)** pueden ayudar a recopilar información sobre los incidentes de error que se producen en tus aplicaciones web. Los registros ayudan a identificar el origen de una brecha y, potencialmente, al actor de la amenaza.

## **Las 10 mejores soluciones de seguridad en aplicaciones web**

Una solución de seguridad en aplicaciones web busca proteger a las empresas de todos los intentos de explotar una vulnerabilidad de código en una aplicación. Veamos las 10 mejores soluciones para asegurar las aplicaciones web y ayudar a mantener tu negocio en funcionamiento.

### **1. [Cloudflare](https://www.cloudflare.com/es-es/)**

![seguridad%20de%20redes%202%20b55173737ff04e08975955602227137c/image2.png](seguridad%20de%20redes%202%20b55173737ff04e08975955602227137c/image2.png)

Con la interfaz intuitiva de Cloudflare, los usuarios pueden identificar e investigar rápidamente los riesgos de seguridad, bloqueando cualquier amenaza cibernética potencial. Sus reglas de firewall personalizadas protegen tu sitio web y tus APIs contra el tráfico entrante malicioso, mientras que el registro de actividad te ayudará a afinar la configuración de seguridad.

Además, controla y evita el uso de credenciales robadas o expuestas que podrían dar a los atacantes acceso a tu cuenta. Los **servicios de Cloudflare** también incluyen un firewall de aplicaciones web y protección DDoS.

Aunque Cloudflare ofrece un plan **gratuito**, no incluye la capacidad WAF. Para obtener una protección automatizada contra la vulnerabilidad de las aplicaciones web, suscríbete al plan Pro de Cloudflare, que tiene un precio a partir de **20 dólares al mes**.

### **2. [Perimeter 81](https://www.perimeter81.com/)**

![seguridad%20de%20redes%202%20b55173737ff04e08975955602227137c/image3.png](seguridad%20de%20redes%202%20b55173737ff04e08975955602227137c/image3.png)

Zero Trust Application Access de Perimeter 81 proporciona un acceso totalmente auditado a los entornos en la nube, las aplicaciones y los servicios web locales, mejorando su seguridad y supervisión.

Una vez que los usuarios se registran, se listan todas las aplicaciones a las que tienen acceso. Puedes asignarles diferentes niveles de acceso en función de su rol. Además, Perimeter 81 también encripta toda la información almacenada y filtra el tráfico saliente.

Para utilizar los servicios de Perimeter 81, regístrate con tu correo electrónico del trabajo y solicita una demostración.

### **3. [NordPass](https://nordpass.com/es/)**

![seguridad%20de%20redes%202%20b55173737ff04e08975955602227137c/image4.png](seguridad%20de%20redes%202%20b55173737ff04e08975955602227137c/image4.png)

Fundada por el mismo equipo que está detrás de la popular NordVPN, NordPass es una solución de seguridad fiable para aplicaciones web. Si quieres averiguar si la información confidencial de tu empresa se ha visto comprometida, el escáner de fugas de datos de NordPass for Business te ayudará a identificar cualquier información filtrada. Además, su función de salud de las contraseñas ayuda a prevenir las amenazas a la seguridad detectando las contraseñas débiles, reutilizadas u obsoletas dentro de la empresa.

El gestor de contraseñas NordPass cuesta a partir de **3,59 dólares al mes** para la versión empresarial, mientras que hay un plan **gratuito** disponible para uso personal con una prueba premium de 30 días.

### **4. [StackHawk](https://www.stackhawk.com/)**

![seguridad%20de%20redes%202%20b55173737ff04e08975955602227137c/image5.png](seguridad%20de%20redes%202%20b55173737ff04e08975955602227137c/image5.png)

StackHawk analiza tus aplicaciones, servicios y APIs en busca de fallos de seguridad en el código o en los componentes de código abierto. Ofrece una gran eficacia a la hora de encontrar y solucionar los fallos, permitiendo a los desarrolladores de tu equipo replicar el problema que desencadenó una vulnerabilidad copiando un comando cURL.

La herramienta está construida sobre el escáner de seguridad de aplicaciones más utilizado, **[ZAP](https://www.zaproxy.org/)**, y cuenta con clientes empresariales como **Microsoft Teams**, **Slack** y **Github Actions**. Stackhawk ofrece un plan gratuito que proporciona escaneos ilimitados para una aplicación, mientras que su plan Pro comienza en **35 dólares al mes** por desarrollador. Si estás interesado en ver la plataforma StackHawk en acción, puedes solicitar una demostración en vivo.

### **5. [Forcepoint ONE](https://www.forcepoint.com/es)**

![seguridad%20de%20redes%202%20b55173737ff04e08975955602227137c/image6.png](seguridad%20de%20redes%202%20b55173737ff04e08975955602227137c/image6.png)

Si buscas una solución de ciberseguridad todo en uno, ForcePoint One es una excelente opción. Con un completo cifrado dentro de la aplicación, proporcionará el máximo nivel de seguridad tanto para las aplicaciones gestionadas como para las no gestionadas. Además, ForcePoint ONE también proporciona detección de amenazas zero-day mientras se cargan, descargan e incluso cuando los datos están en reposo. Otras características de seguridad incluyen la prevención de fuga de datos y la protección contra el malware.

Para solicitar una prueba gratuita y obtener información sobre los precios, debes ponerte en contacto con el equipo de Forcepoint.

### **6. [Barracuda](https://www.barracuda.com/)**

![seguridad%20de%20redes%202%20b55173737ff04e08975955602227137c/image7.png](seguridad%20de%20redes%202%20b55173737ff04e08975955602227137c/image7.png)

Barracuda Cloud Application Protection protege tus aplicaciones de múltiples amenazas combinando una capacidad WAF completa con servicios y soluciones de seguridad avanzados. Además de proteger las aplicaciones web, Barracuda también ofrece soluciones para proteger el correo electrónico, los datos y la red.

Al utilizar cualquiera de las soluciones WAF de Barracuda, obtienes acceso a la función Barracuda Vulnerability Manager de forma gratuita. Esta escanea tus aplicaciones web en busca de vulnerabilidades de seguridad como inyección de HTML, código malicioso, cross-site scripting y fugas de datos sensibles. Recibirás un informe completo con el análisis de seguridad de tu aplicación web, así como consejos para protegerla aún más.

### **7. [Rapid7](https://www.rapid7.com/)**

![seguridad%20de%20redes%202%20b55173737ff04e08975955602227137c/image8.png](seguridad%20de%20redes%202%20b55173737ff04e08975955602227137c/image8.png)

Las soluciones de seguridad de Rapid7 utilizan la automatización inteligente para identificar vulnerabilidades, detectar actividades maliciosas, investigar y detener ataques. Con su análisis contextual de las amenazas, Rapid7 agiliza la gestión del cumplimiento y de los riesgos para proporcionar una recopilación de datos rápida y completa en todos los usuarios, activos y redes.

Los planes de Rapid7 empiezan por **1,84 dólares al mes** para la herramienta de gestión de riesgos de vulnerabilidad y **166 dólares al mes por aplicación** para el servicio de seguridad en aplicaciones web. Todos los planes incluyen cuentas de usuario ilimitadas, un panel central de cuentas y datos compartidos en todas las herramientas. Si tienes algún problema, Rapid7 también ofrece asistencia técnica 24 horas al día, 7 días a la semana.

### **8. [WhiteHat](https://www.whitehatsec.com/)**

![seguridad%20de%20redes%202%20b55173737ff04e08975955602227137c/image9.png](seguridad%20de%20redes%202%20b55173737ff04e08975955602227137c/image9.png)

WhiteHat Security está construido sobre una arquitectura SaaS potente y escalable basada en la nube. Ofrece una protección de seguridad que incluye análisis de la composición del software y protección y supervisión automáticas de la API. Además, WhiteHat es una gran opción si buscas una solución de seguridad para aplicaciones web que agilice los flujos de trabajo y automatice la seguridad de las aplicaciones a lo largo de todo el ciclo de vida de desarrollo del software.

### **9. [Netacea](https://www.netacea.com/)**

![seguridad%20de%20redes%202%20b55173737ff04e08975955602227137c/image10.png](seguridad%20de%20redes%202%20b55173737ff04e08975955602227137c/image10.png)

Desarrolladas mediante el aprendizaje automático del comportamiento, las soluciones de detección de bots y prevención de la toma de posesión de cuentas de Netacea ayudan a identificar y detener los ataques automatizados que pueden causar graves daños a tu negocio.

El análisis de intenciones de Netacea evita que el tráfico no humano y malicioso comprometa los sitios web y las aplicaciones de forma eficaz y precisa. Antes de contratar los servicios de Netacea, puedes solicitar una demostración a medida para ver cómo funciona y cómo puede beneficiar a tu empresa.

### **10. [Mimecast](https://www.mimecast.com/)**

![seguridad%20de%20redes%202%20b55173737ff04e08975955602227137c/image11.png](seguridad%20de%20redes%202%20b55173737ff04e08975955602227137c/image11.png)

Desde los problemas de seguridad del correo electrónico hasta las vulnerabilidades de las aplicaciones, Mimecast ofrece una plataforma basada en la nube que puede encargarse de todo. Mediante sus servicios automatizados, identifica cualquier amenaza y actividad maliciosa y protege tus aplicaciones web.

Mimecast también simplifica el proceso de tratamiento de datos de acuerdo con las directrices de cumplimiento. Hay planes disponibles para empresas de más de 100 empleados y para pequeñas empresas de hasta 100 empleados. Contacta con el equipo de ventas de Minecast para recibir un presupuesto.

### **Conclusión**

Cuando se desarrolla una aplicación web, es importante garantizar su seguridad desde el principio y no después de lanzar la aplicación. Para descubrir las vulnerabilidades, los desarrolladores deben realizar constantemente pruebas de seguridad e implementar diversos tipos de controles de protección, como firewalls de aplicaciones y políticas de seguridad de contenidos. Tanto si se trata de distinguirse de la competencia, como de cumplir ciertas normas o mantener la confianza de los clientes, es esencial identificar y resolver rápidamente cualquier vulnerabilidad común en las aplicaciones web modernas.

La seguridad en las aplicaciones web es aún más importante si se trata de información confidencial y sensible. Al realizar un análisis completo de la aplicación web en busca de fallos de seguridad, vacíos y vulnerabilidades, también se reducen significativamente los riesgos asociados a una violación de datos realizada por malos actores de la ciberseguridad. Recuerda que cuanto más segura sea la aplicación web, mejor será la reputación de la marca y la experiencia del usuario.

## **Qué características de seguridad buscar en los proveedores de hosting web**

Te explicamos las principales características de seguridad que debe tener cualquier proveedor de hosting. Sin medidas de seguridad sólidas, todos los sitios web de tu cuenta de alojamiento pueden ser vulnerables. Esto puede provocar tiempos de inactividad, pérdida de ingresos y daños en tu reputación, especialmente cuando gestionas el sitio web de un cliente.

### **Seguridad del software**

Los servicios de hosting web más seguros implementan muchas funciones de seguridad de software para garantizar que tu sitio web funcione con el software más reciente y seguro. Una de las más importantes es la protección mediante firewall, que bloquea el acceso no autorizado a tu sitio web y evita ataques maliciosos. Otra función crítica es el escaneado y eliminación de malware, que ayuda a identificar y eliminar cualquier código malicioso que pueda haber infectado tu sitio web.

Además, muchas empresas de hosting ofrecen actualizaciones periódicas de software y parches para solucionar las vulnerabilidades del sistema. Las **medidas de seguridad** del software de Hostinger incluyen un analizador de tráfico anti-DDoS y software anti-malware para proteger tu cuenta de hosting de las amenazas cibernéticas.

Nuestro escáner de malware está integrado en hPanel y escanea automáticamente tus sitios web en busca de archivos dañinos. Para ver los resultados del análisis, ve a **Sitios web → Administrar.** En la barra lateral izquierda, selecciona **Seguridad → Escáner de malware**.

Si la herramienta encuentra malware, mostrará el número de archivos sospechosos detectados y limpiados. También ofrece un resumen que incluye el total de malware descubierto, las acciones realizadas, la cronología del malware en los últimos 30 días y los detalles de los archivos comprometidos y maliciosos.

### **Certificado SSL**

**Secure Sockets Layer (SSL)** es un protocolo de seguridad que cifra los datos intercambiados entre un servidor web y el navegador de un usuario. Garantiza que la información privada, como nombres de usuario, contraseñas o datos de facturación, no pueda ser interceptada por terceros. Teniendo un certificado SSL, puedes forzar HTTPS en el sitio web, lo que también mejorará tu SEO y rendimiento.

### **Copias de seguridad y restauraciones**

Los ciberataques, los desastres naturales, los fallos de hardware y los errores humanos son amenazas potenciales para la disponibilidad de un sitio web. Unos servicios fiables de copia de seguridad y restauración garantizarán que los datos de la web puedan recuperarse en caso de incidentes.

La mayoría de los proveedores de alojamiento web ofrecen copias de seguridad semanales o diarias. Además, asegúrate de que el proveedor dispone de una **función de restauración** fácil de usar para recuperar tu página web de forma rápida y cómoda. Esto puede ayudar a minimizar el tiempo de inactividad y evitar la pérdida de datos.

### **Protección DDoS**

Los ataques distribuidos de denegación de servicio (DDoS) sobrecargan un sitio web con tráfico procedente de múltiples fuentes, haciendo que no esté disponible para los usuarios legítimos. Esto puede provocar costosos tiempos de inactividad y dañar tu reputación. Al elegir un hosting seguro con una sólida protección DDoS, puedes ayudar a prevenir estos ataques y garantizar que tu sitio web siga siendo accesible y seguro.

La protección DDoS de las empresas de alojamiento web suele utilizar algoritmos que bloquean el tráfico malicioso antes de que llegue al servidor. Los servicios de hosting web seguros también disponen de técnicas de filtrado avanzadas que pueden distinguir entre tráfico legítimo e ilegítimo. Un buen servicio de alojamiento web utiliza estas medidas para asegurarse de que tu sitio web sigue siendo accesible incluso cuando llega una oleada de tráfico dañino.

### **Supervisión de redes**

La supervisión de la red consiste en escanear periódicamente la red de tu sitio web y la infraestructura del servidor web en busca de actividad inusual, como intentos de acceso no autorizados o patrones de tráfico sospechosos. De este modo, los proveedores de alojamiento web detectan y responden rápidamente a posibles incidentes de seguridad antes de que puedan causar daños importantes a tu sitio web o poner en peligro datos confidenciales.

Para saber si un **servicio de alojamiento web profesional** supervisa su red, consulta su sitio web o ponte en contacto con su servicio de atención al cliente. Elige alojamientos web que ofrezcan monitorización 24 horas al día, 7 días a la semana, utilicen herramientas avanzadas para proteger sus servidores web y tengan críticas positivas sobre la detección y solución de problemas. Comprueba también si hay garantías o acuerdos de nivel de servicio (SLA) relacionados con el tiempo de actividad y el rendimiento de la red para ver su compromiso con el mantenimiento de la red.

### **Soporte CDN**

Una red de distribución de contenidos (CDN) almacena en caché el contenido de un sitio web en servidores situados en todo el mundo. Cuando los visitantes acceden a tu sitio, la CDN recupera el contenido de la ubicación de servidor más cercana a ellos en lugar del servidor principal.

Por tanto, instalar una CDN ayuda a reducir los tiempos de carga y a mejorar el rendimiento del sitio web. Muchas CDN también ofrecen protección DDoS para evitar ataques y mantener tu página web a salvo del tráfico malicioso.

## **10 mejores prácticas de seguridad en el hosting web**

Además de contar con un proveedor de alojamiento seguro, es esencial aplicar prácticas de seguridad web por tu cuenta para proteger tus sitios web de problemas de seguridad. A continuación, exploraremos los mejores métodos para mantener la seguridad del alojamiento web.

**1. Hacer copias de seguridad periódicas**

Con las copias de seguridad, puedes restaurar rápidamente un sitio web que haya sido pirateado o haya experimentado problemas. Realiza copias de seguridad manuales de tus datos con regularidad o programa copias de seguridad automáticas. También recomendamos almacenar copias de seguridad adicionales localmente en tu equipo o disco. Esto es especialmente importante si el proveedor de alojamiento web sólo conserva las copias de seguridad durante un tiempo limitado.

**2. Utilizar el cifrado SSL**

El SSL es importante para garantizar un acceso seguro a tu sitio web y desde él, protegiendo los datos confidenciales de los clientes. Si tu proveedor de alojamiento web no te proporciona un certificado SSL gratuito, puedes comprarlo a una autoridad de certificados SSL.

Cuando tu sitio web tenga un certificado SSL, el navegador mostrará el icono de un candado junto a la URL del sitio; los visitantes pueden hacer clic en él para ver los detalles del certificado.

**3. Utilizar SFTP en lugar de FTP**

Recomendamos **utilizar SFTP** (Secure File Transfer Protocol) en lugar de FTP (File Transfer Protocol). SFTP cifra todos los datos, incluidas las credenciales de acceso y los archivos transferidos, durante la transmisión. Esto evita que los atacantes escuchen, manipulen o roben tus datos. SFTP también utiliza un puerto diferente de FTP, por lo que es más difícil para los atacantes atacar las conexiones SFTP.

<aside>
💡 **Consejo profesional:** Considera la posibilidad de transferir tus archivos utilizando clientes SFTP como **FileZilla**.

</aside>

**4. Eliminar aplicaciones no utilizadas**

Las vulnerabilidades de las aplicaciones web, como los problemas de codificación, los servidores web mal configurados, los fallos de diseño o la falta de validación de formularios, pueden dar a los delincuentes acceso a tus sitios web. Por lo tanto, es esencial supervisar regularmente tus aplicaciones y eliminar las que no se utilicen o estén en peligro. Eliminar temas y plugins obsoletos y sin usar también reforzará la **seguridad de WordPress**.

**5. Cambiar periódicamente las contraseñas**

Las contraseñas débiles pueden ser fácilmente comprometidas por atacantes, poniendo en riesgo tu sitio web y tu información sensible. Recomendamos cambiar las contraseñas al menos cada tres o seis meses. Para facilitar el proceso, utiliza un gestor de contraseñas para generar y almacenar todas las contraseñas. Esto también puede evitar la fatiga de contraseñas y la reutilización de la misma contraseña para varias cuentas.

**6. Instalar y configurar un firewall de aplicaciones web**

Los firewalls de aplicaciones web (WAF) filtran y supervisan el tráfico entre una aplicación web e Internet, bloquean las solicitudes sospechosas o maliciosas y generan alertas para su posterior investigación. Ayuda a proteger las aplicaciones web de ciberataques como el cross-site scripting (XSS) y la inyección SQL.

No todas las empresas de alojamiento web incluyen un firewall de aplicaciones web con sus servicios, por lo que es posible que tengas que adquirir uno por separado. El **[WAF de Cloudflare](https://www.cloudflare.com/es-es/waf/)** es una gran opción. Además de las ventajas de seguridad, es fácil de activar y tiene un plan gratuito disponible. Además de utilizar un firewall basado en IA para proteger tu servidor privado virtual, Hostinger es totalmente compatible con Cloudflare.

**7. Buscar malware en los archivos del sitio web**

Los programas maliciosos pueden crear o modificar archivos y robar información, como contraseñas, perjudicando así a tu sitio web y a tu reputación. Si tu proveedor de hosting no ofrece herramientas de seguridad integradas, afortunadamente existen programas de terceros que comprueban si hay virus en el sitio web y eliminan cualquier amenaza.

Uno de ellos es **[SiteGuarding](https://www.siteguarding.com/en)**, que busca varios tipos de malware, incluso virus desconocidos y nuevas amenazas. También recomendamos instalar **plugins de seguridad de WordPress** para realizar análisis regulares de malware.

**8. Actualizar constantemente el software**

Para proteger tu sitio web de posibles ataques, actualiza regularmente todo el software. Las actualizaciones de software suelen contener parches de seguridad que solucionan vulnerabilidades anteriores. Los piratas informáticos suelen aprovecharse de software obsoleto para acceder sin autorización a sitios web y robar información confidencial. También es importante mantener actualizados los plugins, temas y otros componentes del sitio web.

**¡Importante!** Haz siempre una copia de seguridad de tu sitio web antes de realizar actualizaciones para evitar la pérdida de datos o el tiempo de inactividad.

**9. Restringir el acceso al sitio web a usuarios no autorizados**

El acceso no autorizado a un sitio web puede dar lugar a filtraciones de datos u otras actividades maliciosas. Para evitar el acceso no autorizado a los datos, sigue estas prácticas:

- **Utiliza la autenticación de dos factores:** añade una capa adicional de seguridad utilizando y exigiendo una **segunda forma de identificación**.
- **Crea roles de usuario:** controla lo que pueden y no pueden hacer usuarios específicos, evitando accesos y acciones no autorizadas.
- **Utiliza un gestor de accesos:** si trabajas en una agencia o colaboras con otros autónomos, utiliza la **función de compartir cuentas de hosting** en hPanel para crear y gestionar accesos.
- **Crea una lista de IP permitidas:** crea una lista de URL bloqueadas para limitar el acceso solo a las direcciones IP autorizadas.

**10. Utilizar extensiones de seguridad adicionales**

Las extensiones de seguridad de sitios web proporcionan una capa adicional de protección contra diversas amenazas en línea, como el malware, el phishing y los intentos de pirateo.

También pueden ofrecer funciones como el bloqueo de anuncios, el bloqueo de secuencias de comandos y la gestión de cookies para mejorar el rendimiento del sitio web y la privacidad del usuario.

*A continuación se indican algunas extensiones del navegador que puedes probar:*

- **[Malwarebytes Browser Guard](https://www.malwarebytes.com/browserguard)**: mantiene tus datos online seguros bloqueando rastreadores, malware y estafas.
- **[uBlock Origin](https://ublockorigin.com/es)**: bloquea anuncios y rastreadores en sitios web. También tiene funciones avanzadas de filtrado, que permiten a los usuarios personalizar sus preferencias y bloquear elementos específicos en páginas web.

### **Conclusión**

Mejorar la seguridad del alojamiento web es esencial para proteger la reputación y los datos confidenciales de tu empresa. En este artículo, has aprendido que encontrar una empresa de alojamiento web con protocolos de seguridad como seguridad de software, certificados SSL, copias de seguridad y protección DDoS es el primer paso.

Además, es importante seguir las mejores prácticas de seguridad de hosting web, como hacer copias de seguridad de los datos del sitio web, eliminar las aplicaciones que no se utilizan, cambiar las contraseñas con regularidad, escanear en busca de malware y actualizar el software con regularidad.

## **Preguntas frecuentes sobre seguridad en el hosting web**

- **¿Qué tipo de alojamiento es el más seguro?**

Un tipo de alojamiento que proporciona recursos dedicados, como un **hosting VPS**, se considera el más seguro. Si un VPS se ve comprometido, no afectará a otros usuarios de VPS en el mismo servidor físico. Sin embargo, es importante tener en cuenta que la seguridad de los VPS depende en última instancia de tus propias medidas de seguridad.

- **¿Cómo encontrar un proveedor de alojamiento web seguro?**

Los alojamientos web seguros y fiables cuentan con varias medidas de seguridad, como certificados SSL, copias de seguridad automáticas, actualizaciones de seguridad frecuentes, asistencia 24 horas al día, 7 días a la semana, un potente firewall y protección DDoS. Cuando busques opciones, elige el **mejor hosting** que ofrezca estas características.

- **¿Puede un proveedor de hosting garantizar la seguridad de un sitio web?**

Ninguna plataforma de alojamiento puede garantizar una seguridad infalible debido a factores externos como el comportamiento de los usuarios y las integraciones de terceros. Los alojamientos web de confianza pueden minimizar los riesgos y reforzar la seguridad de los sitios web proporcionando actualizaciones de software, firewalls y copias de seguridad. Los propietarios de sitios web también deben aplicar medidas de seguridad y actualizaciones para mejorar aún más la seguridad.

- **¿Cuáles son las amenazas de seguridad más comunes a las que se enfrenta un servicio de alojamiento web?**

Las amenazas más comunes a la seguridad del alojamiento de sitios web son el malware, el phishing, el XSS, la inyección SQL y los ataques distribuidos de denegación de servicio (DDoS).

Seguridad en aplicaciones

## **Conceptos de la seguridad en aplicaciones**

La **seguridad de las aplicaciones** se refiere a las medidas de seguridad, a nivel de aplicación, cuyo propósito es impedir el robo o el secuestro de datos o códigos dentro de la aplicación. Abarca las consideraciones de seguridad que se deben tener en cuenta al desarrollar y diseñar aplicaciones, además de los sistemas y los enfoques para proteger las aplicaciones después de distribuirlas.

La seguridad de las aplicaciones puede incluir hardware, software y procedimientos que identifican o minimizan las vulnerabilidades de seguridad. Un enrutador que impide que se vea la dirección IP de un ordenador desde Internet se puede considerar una forma de seguridad de las aplicaciones mediante hardware. Pero las medidas de seguridad que se implementan a nivel de aplicación también se suelen integrar en el software. Es el caso de un cortafuegos de aplicación que defina estrictamente qué actividades están permitidas y cuáles prohibidas. Los procedimientos pueden implicar tareas como una rutina de seguridad de aplicaciones que incluya protocolos como pruebas periódicas.

La seguridad de las aplicaciones se refiere al proceso de desarrollar, añadir y probar características de seguridad dentro de las aplicaciones para evitar vulnerabilidades de seguridad contra amenazas, tales como la modificación y el acceso no autorizados.

### **¿Por qué es tan importante la seguridad de las aplicaciones?**

La seguridad de las aplicaciones es importante porque las aplicaciones actuales suelen estar disponibles a través de varias redes y conectadas a la cloud, lo que aumenta las vulnerabilidades a los peligros y las amenazas a la seguridad. Cada vez hay más presión y más alicientes para garantizar la seguridad no solo a nivel de la red, sino también dentro de las propias aplicaciones. Uno de los motivos es que los hackers están más interesados que antes en atacar aplicaciones. Al realizar pruebas de la seguridad de las aplicaciones, se pueden desvelar puntos débiles de las aplicaciones y ayudar a evitar este tipo de ataques.

La seguridad de aplicaciones no es una tecnología única, sino un conjunto de mejores prácticas, funciones y/o características añadidas al software de una empresa para ayudar a prevenir y resolver las amenazas de cibercriminales, brechas de datos y otros peligros.

Hay varios tipos de programas, servicios y dispositivos de seguridad de aplicaciones que puede utilizar una empresa. Firewalls, antivirus y cifrado de datos son sólo algunos ejemplos para evitar que usuarios no autorizados entren en un sistema. Si una empresa desea predecir conjuntos de datos específicos y confidenciales, puede establecer políticas de seguridad de aplicaciones únicas para esos recursos.

La seguridad de aplicaciones puede producirse en varias etapas, pero el establecimiento de mejores prácticas se hace con mayor frecuencia en las fases de desarrollo de aplicaciones. Sin embargo, las empresas también pueden aprovechar diferentes herramientas y servicios posteriores al desarrollo. En general, hay cientos de herramientas de seguridad a disposición de las empresas, cada una de las cuales sirve para propósitos únicos. Algunas refuerzan los cambios en el código, otras vigilan la aparición de amenazas en el código, mientras que otras establecen el cifrado de datos. Además, las empresas pueden elegir herramientas más especializadas para diferentes tipos de aplicaciones.

**Beneficios de la seguridad de aplicaciones**

Las empresas dependen de las aplicaciones para prácticamente todo lo que hacen, así que mantenerlas seguras es algo no negociable. A continuación se exponen varias razones por las que las empresas deberían invertir en la seguridad de aplicaciones:

- Reduce el riesgo que provenga tanto de fuentes internas como de terceros.
- Protege la imagen de marca, al mantener a la empresa lejos de los titulares.
- Mantiene la seguridad de los datos del cliente y aumenta su confianza.
- Protege los datos sensibles de fugas.
- Mejora la confianza de inversores y entidades de préstamo cruciales.

## **Amenazas y vulnerabilidades de la seguridad en aplicaciones**

### **¿Por qué las empresas necesitan seguridad de aplicaciones?**

Las empresas saben que la seguridad de los centros de datos en general es importante, pero pocas tienen políticas de seguridad de aplicaciones bien definidas para seguirles el ritmo a los cibercriminales e incluso ir un paso adelante. De hecho, el [informe sobre el estado de la seguridad de software de Veracode](https://www.veracode.com/state-of-software-security-report) demuestra que el 83% de todas las aplicaciones probadas (unas 85,000) presentaban al menos una falla de seguridad. En total, Veracode encontró 10 millones de fallas, lo cual indica que la mayoría de las aplicaciones presentaban una gran cantidad de brechas de seguridad.

La existencia de estas fallas de seguridad es bastante preocupante, pero lo que es todavía más preocupante es cuando las empresas no cuentan con las herramientas necesarias para evitar que estas fallas den lugar a brechas de seguridad. Para que una herramienta de seguridad de aplicaciones tenga éxito, necesita tanto identificar las vulnerabilidades como resolverlas rápidamente, antes de que se conviertan en un problema.

Pero los gerentes de TI tienen que ir mucho más allá de esas dos tareas principales. Identificar y solucionar las brechas de seguridad es el día a día del personal de seguridad de aplicaciones, pero a medida que los cibercriminales desarrollan técnicas más sofisticadas, las empresas tienen que ir varios pasos adelante con herramientas de seguridad modernas. Las amenazas son cada vez más difíciles de detectar y más perjudiciales para las empresas, que no se pueden permitir estrategias de seguridad obsoletas.

### **Entender los tipos de herramientas de seguridad de aplicaciones**

Actualmente, las empresas tienen varias opciones en cuanto a productos de seguridad de aplicaciones, la mayoría de las cuales entran en una de las dos categorías siguientes: herramientas de pruebas de seguridad (un mercado consolidado que tiene la intención de analizar el estado de la seguridad de sus aplicaciones) y herramientas de "blindaje" de seguridad, que protegen y refuerzan las aplicaciones para que las brechas sean mucho más difíciles de ejecutar.

Dentro de los productos de pruebas de seguridad, hay categorías todavía más concretas. En primer lugar, están las pruebas estáticas de seguridad de aplicaciones, que supervisan puntos específicos del código durante el proceso de desarrollo de la aplicación, lo cual ayuda a los desarrolladores a asegurarse de que no estén creando involuntariamente lagunas de seguridad durante el proceso de desarrollo.

En segundo lugar, están las pruebas dinámicas de seguridad de aplicaciones, que detectan brechas de seguridad en código en ejecución. Este método puede imitar un ataque a un sistema de producción y ayudar a los desarrolladores e ingenieros a defenderse de estrategias de ataque más sofisticadas. Tanto las pruebas estáticas y dinámicas son interesantes, así que el nacimiento de un tercer tipo no es ninguna sorpresa, las pruebas interactivas, que combinan los beneficios de ambas.

Por último, las pruebas de seguridad de aplicaciones móviles, como su nombre indica, detectan lagunas en los entornos móviles. Este método es único porque puede estudiar la forma en la que un atacante utiliza el sistema operativo móvil para provocar una brecha en el sistema y las aplicaciones que se ejecutan en él.

Pasemos al "blindaje" de aplicaciones. Como se ha mencionado, las herramientas de esta categoría están destinadas a blindar aplicaciones contra ataques. Aunque suena ideal, es una práctica menos establecida, especialmente en comparación con las herramientas de prueba. No obstante, a continuación se presentan las principales subcategorías dentro de este tipo de herramientas.

En primer lugar tenemos la autoprotección de aplicación en tiempo de ejecución (RASP), que combina estrategias de prueba y protección. Estas herramientas monitorean el comportamiento de las aplicaciones en ambientes tanto de escritorio como móviles. Los servicios RASP permiten a los desarrolladores mantenerse al día sobre el estado de la seguridad de aplicaciones mediante alertas frecuentes, e incluso puede cerrar una aplicación si el sistema entero se encuentra en peligro.

En segundo y tercer lugar, la ofuscación de código/aplicación y el software de cifrado/anti-manipulación son dos categorías que sirven esencialmente para el mismo propósito: evitar que los cibercriminales lleven a cabo una brecha en el código de una aplicación.

Por último, las herramientas de detección de amenazas se encargan de analizar el entorno en el que se ejecutan las aplicaciones. Esta categoría de herramientas puede evaluar el estado de dicho entorno, detectar posibles amenazas e incluso puede comprobar si un dispositivo móvil se ha puesto en peligro debido a "huellas digitales" únicas del dispositivo.

### **Las principales amenazas a la seguridad de las aplicaciones a las que debe prestar atención**

Las principales vulnerabilidades en aplicaciones son: inyección de código, autenticación y autorización incorrectas, exposición de datos sensibles, desbordamiento de búfer, vulnerabilidades de seguridad de configuración y problemas de criptografía. A continuación, explicamos más a detalle qué implicaciones tienen para las aplicaciones de tu empresa.

A pesar de su conveniencia, existen inconvenientes cuando se trata de confiar en aplicaciones web para empresas. Una cosa que todos los propietarios de empresas tendrán que reconocer y protegerse es la presencia de vulnerabilidades de software y amenazas a las aplicaciones web.

Si bien no hay 100% garantía de seguridad, hay algunos pasos que se pueden tomar para evitar sufrir daños. Si está utilizando CMS, entonces el informe pirateado por SUCURI muestra más de El 50% de los sitios web están infectados con una o más vulnerabilidades.

Si es nuevo en las aplicaciones web, aquí hay algunas amenazas comunes que debe tener en cuenta y evitar:

- **Inyección de código:** Esta vulnerabilidad permite a un atacante inyectar código malicioso en una aplicación, lo que le da control sobre la misma. Puede realizarse este hackeo, tanto de manera física por una persona como de manera remota, si se logra tener acceso de manera perniciosa.
- **Autenticación y gestión de sesiones:** Un atacante puede explotar debilidades en el sistema de autenticación y gestión de sesiones para acceder a cuentas de usuario o robar información confidencial. Por ejemplo, si se usa una aplicación de terceros para proteger la información de acceso de tus clientes y colaboradores o si se realiza un hackeo de sus cuentas.
- **Cross-Site Scripting (XSS):** Esta vulnerabilidad permite a un atacante inyectar código malicioso en una página web, lo que puede comprometer la seguridad de los usuarios que visitan dicha página. Este potencial ataque es bastante preocupante para aplicaciones web que requieren de una constante conexión a internet para poder funcionar. Para prevenir ataques XSS, es importante asegurarse de que se utilice codificación de caracteres en la entrada de usuario y evitar el uso de funciones de evaluación de JavaScript en la aplicación. Puede que esta manera de prevención no sea aplicable a todos los desarrollos de aplicaciones.
- **Referencias no seguras:** Si un programador no maneja adecuadamente las referencias a objetos, puede dar lugar a vulnerabilidades en el acceso a los mismos. Por lo tanto, es necesario realizar un análisis en el código fuente para prevenir la explotación de esta vulnerabilidad.
- **Malas prácticas de codificación:** El uso de malas prácticas de codificación es una de las principales vulnerabilidades en aplicaciones, como la falta de validación de entrada, puede permitir a un atacante explotar vulnerabilidades en el código. En la próxima sección veremos cómo te puedes defender contra esta, una de las principales vulnerabilidades en aplicaciones, con herramientas de análisis como SAST, DAST y SCA de Veracode.
- **Problemas en el control de acceso:** Si se implementa incorrectamente el control de acceso a ciertos recursos o funciones, un atacante puede acceder a ellos sin autorización.

## Formas de prevenir a las principales vulnerabilidades en aplicaciones

Como hemos visto, las principales vulnerabilidades en aplicaciones pueden comprometer la seguridad de tus clientes, así como impedir el crecimiento de tu empresa al carecer del marco legal normativo tanto local como internacional. A continuación, te mencionamos algunas herramientas y maneras en que puedes prevenir ataques de ciber atacantes:

- **Inyección de SQL:** Una de las principales formas de prevenir la inyección de SQL es utilizar parámetros de consulta preparados y validación de entradas de usuario para asegurarse de que no se puedan introducir comandos maliciosos en la consulta. Esta herramienta de prevención es útil y necesaria para un correcto desarrollo.
- **Ataques CSRF:** Para prevenir ataques CSRF, es necesario implementar tokens CSRF y validar siempre los tokens al procesar solicitudes.

## **Medidas de seguridad para la seguridad en aplicaciones**

Hay diferentes tipos de características de seguridad de las aplicaciones, como la autenticación, la autorización, el cifrado, el registro y las pruebas de seguridad de las aplicaciones. Los desarrolladores también pueden codificar las aplicaciones para reducir las vulnerabilidades de seguridad.

Los desarrolladores de software pueden integrar procedimientos de autenticación y autorización en las aplicaciones para asegurarse de que solo accedan los usuarios autorizados. Los procedimientos de autenticación garantizan la identidad de los usuarios. Se consigue obligando a los usuarios a proporcionar un nombre de usuario y una contraseña para iniciar la sesión en una aplicación. La autenticación multifactor requiere más de una forma de autenticación. Por ejemplo, algo que el usuario sabe (una contraseña), algo que tiene (un dispositivo móvil) y algo que le caracteriza (una huella dactilar o el reconocimiento facial).

Una vez autenticado, puede autorizarse al usuario para acceder a la aplicación y a utilizarla. El sistema puede validar que el usuario tenga permiso para acceder a la aplicación comparando su identidad con una lista de usuarios autorizados. La autenticación se debe efectuar antes que la autorización para que la aplicación solo contraste las credenciales de usuario validadas con la lista de usuarios autorizados.

Cuando el usuario esté autenticado y esté usando la aplicación, se pueden proteger los datos confidenciales con otras medidas de seguridad para que los ciberdelincuentes no los vean ni los usen. En las aplicaciones basadas en la cloud, en las que el tráfico que contiene datos confidenciales circula entre el usuario final y la cloud, ese tráfico se puede cifrar para proteger los datos.

Por último, si se vulnera la seguridad de una aplicación, el registro puede ayudar a identificar quién ha accedido a los datos y cómo. Los archivos de registro de la aplicación ofrecen un control con marcas de tiempo de los aspectos de la aplicación a los que se ha accedido y de la persona implicada. Es necesario probar la seguridad de las aplicaciones para asegurarse de que todos estos controles de seguridad funcionen correctamente.

### **Seguridad de las aplicaciones en la cloud**

La seguridad de las aplicaciones en la cloud plantea desafíos adicionales. Dado que los entornos de cloud ofrecen recursos compartidos, se debe comprobar con especial atención que los usuarios solo tengan acceso a los datos que están autorizados a consultar en las aplicaciones basadas en la cloud. Los datos confidenciales también son más vulnerables en las aplicaciones basadas en la cloud, puesto que los datos se transmiten por Internet del usuario a la aplicación y viceversa.

### **Seguridad de las aplicaciones móviles**

Los dispositivos móviles también transmiten y reciben información por Internet, no por una red privada, de modo que son vulnerables a ataques. Las empresas pueden utilizar redes privadas virtuales (VPN) para añadir una capa de seguridad a las aplicaciones móviles que proteja a los empleados que inicien sesión en las aplicaciones de forma remota. Los departamentos de TI también pueden optar por revisar las aplicaciones móviles y asegurarse de que cumplan las políticas de seguridad de la empresa antes de permitir que los empleados las usen en los dispositivos móviles que se conecten con la red empresarial.

### **Seguridad de las aplicaciones web**

Aplicaciones o servicios a los que los usuarios acceden a través de una interfaz de navegador por Internet. Como las aplicaciones web no se encuentran en las máquinas de los usuarios, sino en servidores remotos, la información de entrada y de salida se tiene que transmitir por Internet. La seguridad de las aplicaciones web preocupa en especial a las empresas que alojan aplicaciones web o proporcionan servicios web. Dichas empresas suelen optar por proteger su red contra intrusiones con un cortafuegos para aplicaciones web. Un cortafuegos para aplicaciones web inspecciona los paquetes de datos que considera perjudiciales y, si es necesario, los bloquea.

## **¿Qué son los controles de seguridad de las aplicaciones?**

Los controles de seguridad de las aplicaciones son técnicas que mejoran la seguridad de una aplicación a nivel de codificación para que sea menos vulnerable a las amenazas. Muchos de estos controles afectan a cómo responde la aplicación a entradas inesperadas que un ciberdelincuente podría utilizar para aprovecharse de una debilidad. Un programador puede escribir código para una aplicación que le otorgue más control sobre el resultado de estas entradas inesperadas. El «fuzzing» es un tipo de prueba de seguridad de las aplicaciones en la que los desarrolladores examinan los resultados de valores o entradas inesperados para determinar cuáles hacen que la aplicación funcione de una forma imprevista que podría suponer una deficiencia de seguridad.

### **¿Qué son las pruebas de seguridad de las aplicaciones?**

Los desarrolladores de aplicaciones realizan pruebas de seguridad de las aplicaciones dentro del proceso de desarrollo de software para asegurarse de que no haya vulnerabilidades de seguridad en una versión nueva o actualizada de una aplicación de software. Las auditorías de seguridad pueden garantizar que la aplicación cumpla una serie específica de criterios de seguridad. Una vez que una aplicación supera la auditoría, los desarrolladores deben asegurarse de que solo puedan acceder a ellas los usuarios autorizados. En las pruebas de intrusión, los desarrolladores piensan como un ciberdelincuente y buscan formas de irrumpir en la aplicación. Las pruebas de intrusión pueden incluir ingeniería social o intentos de engañar a los usuarios para que permitan el acceso no autorizado. Por lo general, los verificadores llevan a cabo análisis de seguridad tanto sin autenticar como autenticados (como usuarios con la sesión iniciada) para detectar vulnerabilidades de seguridad que quizás no se den en ambos estados.

### **Cómo activar la seguridad de aplicaciones**

Sin duda, la seguridad de aplicaciones más sólida y efectiva empieza en el código. Este enfoque, conocido como seguridad por diseño, es crucial para hacer las cosas bien. En muchos casos, las vulnerabilidades de las aplicaciones empiezan con una arquitectura vulnerable plagada de defectos de diseño. Esto significa que la seguridad de la aplicación debe fundarse en el proceso de desarrollo, es decir, en el código.

Un enfoque de seguridad por diseño significa que sus aplicaciones empiezan con una base limpia y bien protegida. Pero más allá de este método, hay otras mejores prácticas de seguridad de aplicaciones que las empresas deben tener en cuenta a la hora de perfeccionar su estrategia.

1. Trate su arquitectura de nube, ya sea pública u on-premise, como insegura. Con esta mentalidad como punto de partida, se elimina la complacencia de asumir que la nube es lo suficientemente segura.
2. Aplique medidas de seguridad a cada componente de su aplicación y durante cada fase del proceso de desarrollo. Asegúrese de incluir las medidas apropiadas para cada componente en concreto.
3. Una estrategia crucial, pero que requiere mucho tiempo, es automatizar los procesos de instalación y configuración. Aunque ya haya completado estos procesos anteriormente, tendrá que rehacerlos para sus aplicaciones de próxima generación.
4. No basta con establecer medidas de seguridad. Asegúrese de realizar pruebas frecuentes una y otra vez para asegurarse de que funcionen correctamente. En el caso de una brecha, estará agradecido de haber detectado y resuelto cualquier falla.
5. Aproveche las capacidades del SaaS para dedicar menos tiempo a laboriosas tareas de seguridad y reenfocar su atención en proyectos que generen mayor valor. El SaaS es relativamente accesible y no requiere un equipo de TI dedicado a configurar productos.

Algunas de las principales vulnerabilidades en aplicaciones sólo pueden identificarse a través del análisis del código fuente.

- **Análisis estático de código fuente (SAST):** La prueba de seguridad de aplicaciones estáticas (SAST) se utiliza para identificar vulnerabilidades de seguridad durante el ciclo de vida de desarrollo de software (SDLC). Funciona principalmente en el código fuente y los binarios. Las herramientas SAST funcionan de la mano con el desarrollo de aplicaciones y alertan sobre cualquier problema a medida que se descubren en vivo. La idea detrás del análisis SAST es realizar una evaluación "de adentro hacia afuera" y asegurar la aplicación antes del lanzamiento público. Hay muchas herramientas SAST que puede consultar aquí en [OWASP](https://owasp.org/www-community/Source_Code_Analysis_Tools).
- **Análisis dinámico de aplicaciones (DAST):** Si bien las herramientas SAST se implementan durante el ciclo de desarrollo, las pruebas dinámicas de seguridad de aplicaciones (DAST) se utilizan al final del mismo. Esto presenta un enfoque de "afuera hacia adentro", similar al de un pirata informático, y no se necesita código fuente ni archivos binarios para ejecutar el análisis DAST. Esto se realiza en una aplicación en ejecución a diferencia de SAST, que se realiza en código estático.
- **Análisis de composición de software (SCA):** El análisis de composición de software (SCA) se trata de proteger los frentes de código abierto de su aplicación, si tiene alguno.

> Si bien SAST puede encubrir esto hasta cierto punto, una herramienta SCA independiente es mejor para un análisis en profundidad de todos los componentes de código abierto para el cumplimiento, las vulnerabilidades, etc.
 
- **Pentesting:** En un alto nivel, Penetration Testing funciona de manera similar a DAST al atacar una aplicación desde el exterior para descubrir lagunas de seguridad. Pero si bien DAST es mayoritariamente automática y económica, las pruebas de penetración se realizan manualmente por expertos (hackers éticos) y es un asunto costoso. Aún así, hay Pentest para realizar una inspección automática, pero los resultados pueden carecer de profundidad en comparación con las pruebas manuales.
- **RASP**: Aplicación en tiempo de ejecución Self-Protección (RASP), como lo demuestra su nombre, ayuda a Detectar problemas de seguridad en tiempo real. Los protocolos RASP están integrados en la aplicación para evitar vulnerabilidades que puedan falsificar otras medidas de seguridad.

## Seguridad de los datos

### Conceptos básicos de la seguridad de los datos

En líneas generales, **seguridad de datos se refiere a medidas de protección de la privacidad digital que se aplican para evitar el acceso no autorizado a los datos**, los cuales pueden encontrarse en ordenadores, bases de datos, sitios web, etc. La **seguridad de datos** también protege los datos de una posible corrupción.

### **¿Qué es seguridad de datos?**

La seguridad de datos, también conocida como seguridad de la información o seguridad informática, es un aspecto esencial de TI en organizaciones de cualquier tamaño y tipo. **Se trata de un aspecto que tiene que ver con la protección de datos contra accesos no autorizados y para protegerlos de una posible corrupción durante todo su ciclo de vida**.

**Seguridad de datos incluye conceptos como encriptación de datos, tokenización y prácticas de gestión de claves que ayudan a proteger los datos en todas las aplicaciones y plataformas de una organización**.

Hoy en día, organizaciones de todo el mundo invierten fuertemente en la tecnología de información relacionada con la ciberdefensa con el fin de proteger sus activos críticos: su marca, capital intelectual y la información de sus clientes.

En todos los temas de seguridad de datos **existen elementos comunes que todas las organizaciones deben tener en cuenta a la hora de aplicar sus medidas: las personas, los procesos y la tecnología**.

### **Seguridad de la Información**

En un mundo digital interconectado, la Seguridad de la Información se erige como el baluarte que resguarda los secretos, la privacidad y la integridad de nuestros datos. Este artículo explora los fundamentos esenciales de la seguridad de la información, desentrañando las estrategias y mejores prácticas necesarias para enfrentar los desafíos del ciberespacio. Acompáñanos en este viaje hacia un entendimiento profundo de cómo proteger la información en la era digital.

### **Protegiendo tu Data Personal**

Los datos personales son cualquier información que se puede utilizar para identificarlo y puede existir tanto **fuera** de línea como **en línea**. Muchas personas piensan que si no tienen ninguna cuenta en redes sociales o en línea, entonces no tienen una identidad en línea. Este no es el caso. Si usa la web, tiene una identidad en línea. Al elegir un nombre de usuario, es importante no revelar ninguna información personal.

- No utilices tu nombre completo ni partes de tu dirección o número de teléfono.
- No utilices tu nombre de usuario de correo electrónico.
- No utilices la misma combinación de nombre de usuario y contraseña, especialmente en las cuentas financieras.
- No elijas un nombre de usuario muy extraño y luego lo reutilices una y otra vez, ya que hace que sea más fácil rastrearlo.
- No elijas un nombre de usuario que dé pistas sobre tus contraseñas, como una serie de números o letras, la primera parte de una frase de dos partes o el departamento en el que trabajas, como TI.
- Elija un nombre de usuario que sea apropiado para el tipo de cuenta, es decir, empresarial, social o personal.

### **Tus Datos**

Los datos personales describen cualquier información tuya, incluido tu nombre, número de seguro social, número de licencia de conducir, fecha y lugar de nacimiento e incluso fotos o mensajes que intercambia con familiares y amigos. Los ciberdelincuentes pueden utilizar esta información confidencial para identificarte y hacerse pasar por vos, lo que infringe tu privacidad y puede causar graves daños a tu reputación.

- **Registros médicos**: Cada vez que visita al médico, la información personal sobre tu salud física y mental y tu bienestar se agrega a sus registros médicos electrónicos (EHR). Dado que la mayoría de estos registros se guardan en línea, debe conocer la información médica que comparte. Y estos registros van más allá de los límites del consultorio del médico. Por ejemplo, muchos monitores de actividad física recopilan grandes cantidades de datos clínicos, como la frecuencia cardíaca, la presión arterial y los niveles de azúcar en la sangre, que se transfieren, almacenan y muestran a través de la nube. Por lo tanto, debe considerar que estos datos forman parte de tu historia clínica.
- **Registros educativos:** contienen información sobre sus calificaciones y logros académicos. Sin embargo, estos registros también pueden incluir tu información de contacto, registros de asistencia, informes disciplinarios, registros de salud y vacunas, así como cualquier registro de educación especial, incluidos los programas de educación individualizada.
- **Registros de empleo y financieros:** Los datos de empleo pueden ser valiosos para los hackers si pueden recopilar información sobre tu empleo anterior o incluso sus evaluaciones de desempeño actuales. Tu historial financiero puede incluir información sobre sus ingresos y gastos. Tus registros de impuestos pueden incluir cheques de pago, extractos de tarjetas de crédito, tu calificación crediticia y los detalles de tu cuenta bancaria. Todos estos datos, si no se protegen adecuadamente, pueden comprometer tu privacidad y permitir que los ciberdelincuentes utilicen tu información para tu propio beneficio.

### **Datos personales vs. Datos empresariales**

Todo lo que viaja por la red es vulnerable. Por lo tanto, la seguridad informática empresarial es muy importante, ya que los atacantes tratarán de acceder a la información que se encuentra bajo nuestro poder.

Los **Datos Personales** son información que solo te interesa a ti: fotos, redes sociales, cuentas bancarias, facturas, información familiar, entre otras. Asegúrate de que las personas que tienen acceso a estos datos solo sean las que quieres que accedan a ellos.

Los **Datos Empresariales** son los datos a los que accediste desde que formas parte de la empresa: clientes, gastos, información financiera y tributaria, métricas, estadísticas, resultados, entre otras. Las empresas se aseguran de que no compartas estos datos con otras personas pidiéndote que firmes un *NDA* (acuerdo de no divulgación).

![seguridad%20de%20redes%202%20b55173737ff04e08975955602227137c/image12.png](seguridad%20de%20redes%202%20b55173737ff04e08975955602227137c/image12.png)

### **¿Dónde están sus datos?**

Ayer compartiste un par de fotos de tu primer día de trabajo con algunos de tus amigos cercanos. Tomaste algunas fotos en el trabajo con tu teléfono. Los compartiste con cinco amigos cercanos, que viven en varios lugares del mundo. Todos tus amigos descargaron las fotos y ahora tienen copias de tus fotos en sus dispositivos. Uno de tus amigos estaba tan orgulloso que decidieron publicar y compartir tus fotos en línea.

Las fotos ya no están solo en tu dispositivo. De hecho, han terminado en servidores ubicados en diferentes partes del mundo y personas que ni siquiera conoces ahora tienen acceso a tus fotos. Este es solo un ejemplo que nos recuerda que cada vez que recopilamos o compartimos datos personales, debemos considerar nuestra seguridad.

Existen distintas leyes que protegen la privacidad y los datos en tu país. Pero, ¿sabes dónde están tus datos? Después de una consulta, el médico actualizará tu historia clínica. Para fines de facturación, esta información se puede compartir con la empresa de seguros. En tales casos, tu registro médico, o parte de él, ahora está disponible en la compañía de seguros. Las tarjetas de fidelidad de la tienda pueden ser una manera conveniente de ahorrar dinero en tus compras. Sin embargo, la tienda está usando esta tarjeta para crear un perfil de tu comportamiento de compra, que luego puede usar para dirigirse a usted con ofertas especiales de sus socios de marketing.

### **Dispositivos inteligentes**

A menos que haya elegido recibir estados de cuenta impresos (DINOSAURIO), probablemente acceda a copias digitales de los estados de cuenta bancaria a través del sitio web de tu banco. Y al pagar una factura, es muy probable que haya transferido los fondos requeridos a través de una aplicación de banca móvil. Pero además de permitirle acceder a tu información, los dispositivos informáticos ahora también pueden generar información sobre usted.

Las tecnologías portátiles, como los relojes inteligentes y los rastreadores de actividad, recopilan tus datos para la investigación clínica, el monitoreo de la salud del paciente y el seguimiento del estado físico y el bienestar. A medida que crece el mercado mundial de rastreadores de fitness, también lo hace el riesgo para tus datos personales. Puede parecer que la información disponible en línea es gratuita. las empresas de redes sociales generan la mayoría de sus ingresos vendiendo publicidad basada en los datos de los clientes que se han extraído mediante algoritmos o fórmulas. Por supuesto, estas empresas argumentarán que no están \”vendiendo\” datos de clientes con sus socios de marketing.

## **Triangulo CIA: Confidencialidad, Integridad y Disponibilidad**

**Una cadena es tan fuerte como su eslabón más débil.** Entre más crece nuestra responsabilidad, más aumenta la confidencialidad de nuestros datos y el impacto que puede generar que los atacantes u otras personas accedan a ellos.

Asegúrate de que vos mismo, tus compañeros y tus empleados, no sean el eslabón más débil de la cadena, emplea estrategias dentro de tu organización y dentro de tu vida diaria que te ayuden a proteger la información, protégela tú, no esperes que los demás lo hagan por ti, como el área de IT, el área de tecnología, tú mismo puedes protegerla. Asegúrate de todos tus dispositivos, tenlos siempre a la vista, tenlos siempre bloqueados o encriptados.

Ten cuidado con las fotos, las fotos tienen mucha información que puede necesitar el próximo atacante. Asegúrate de no ser tú que expongas información que hay que cuidar.

![seguridad%20de%20redes%202%20b55173737ff04e08975955602227137c/image13.jpg](seguridad%20de%20redes%202%20b55173737ff04e08975955602227137c/image13.jpg)

El **Triangulo CIA** está conformado por los siguientes elementos:

- **Confidencialidad:**

nos asegura que la información que tenemos la compartimos con otras empresas con otras organizaciones, en redes sociales, o cuando hacemos una compra en línea o que dejamos en la nube cuando subimos nuestras fotos, es información que esta disponible y que es confidencial solo mía y que no va a ser accedida o no va a ser vista por sistemas o por personas que no están autorizadas.

Ejemplo: una compra en línea, en la cual estas dejando el numero de tu tarjeta, tu nombre, dirección, datos personales y entre otros, este sitio donde estas haciendo la compra tiene que asegurarte que la información que tu estas dejando para hacer la compra es confidencial y que nadie va a tener acceso a esa información y mucho menos que estén en textos planos claramente legibles.

- **Integridad:**

esta propiedad nos asegura que la información que nosotros estamos almacenando se va a mantener así durante todo su tiempo de vida dentro del sistema y no va a ser modificada sin mi autorización, incluso si yo pido que lo cambien, ya que el sistema tiene registros de que es lo que se ha cambiado, esta integridad debe asegurarnos que la información se va a mantener intacta y se mantendrá integrada en el sistema del que se maneje y se almacene.

- **Disponibilidad:**

esta propiedad nos asegura que la información se encuentra disponible siempre para todos los usuarios. (importante: esta información solo debe estar disponible para los usuarios autorizados).

Por eso algunos sitios te preguntan en una ventana emergente si les das permiso de usar tus datos personales o no autorizas.

Cada cosa que realizamos en la organización o con la información de nuestra organización, si tu cargo es de manejar información confidencial, el impacto que va a tener una pérdida de esa información o que un atacante capture esa información es mucho más alto.

## **Datos de la organización**

> Datos Tradicionales: suelen ser generados y mantenidos por todas las organizaciones, grandes y pequeñas. Incluye lo siguiente:
> 
- **Datos transaccionales,** como detalles relacionados con la compra y venta, actividades de producción y operaciones organizativas básicas, como cualquier información utilizada para tomar decisiones de empleo.
- **La propiedad intelectual,** como patentes, marcas registradas y planes de nuevos productos, permite a una empresa obtener una ventaja económica sobre sus competidores. Esta información a menudo se considera un secreto comercial y perderla puede resultar desastroso para el futuro de una empresa.
- **Los datos financieros,** como las declaraciones de ingresos, los balances y las declaraciones de flujo de caja brindan información sobre el estado de la empresa.

Internet de las cosas (IoT) y Big Data: IoT es una gran red de objetos físicos, como sensores, software y otros equipos. Todas estas «cosas» están conectadas a Internet, con la capacidad de recopilar y compartir datos. Y dado que las opciones de almacenamiento se están expandiendo a través de la nube y la virtualización, no sorprende que la aparición de IoT haya llevado a un crecimiento exponencial de los datos, creando una nueva área de interés en tecnología y negocios llamada «Big Data».

## **El cubo**

Ampliemos el concepto del **Triangulo CIA.** El McCumber Cube es un marco modelo creado por John McCumber para ayudar a las organizaciones a establecer y evaluar iniciativas de seguridad de la información al considerar todos los factores relacionados que las afectan. Este modelo de seguridad tiene tres dimensiones:

### **Los principios fundamentales para proteger los sistemas de información.**

![seguridad%20de%20redes%202%20b55173737ff04e08975955602227137c/image14.png](seguridad%20de%20redes%202%20b55173737ff04e08975955602227137c/image14.png)

**Como ya vimos nos referimos a:**

- **La confidencialidad** es un conjunto de reglas que evita que la información sensible sea revelada a personas no autorizadas, espacio de recursos y procesos. Los métodos utilizados para garantizar la confidencialidad incluyen **el cifrado** de datos, **la autenticación** y **el control de** acceso.
- **La integridad** garantiza que la información o los procesos del sistema estén protegidos contra modificaciones intencionales o accidentales. Una forma de garantizar la integridad es utilizar una función **hash** o **suma** de comprobación.
- **La disponibilidad** significa que los usuarios autorizados pueden acceder a los sistemas y datos cuando y donde sea necesario y aquellos que no cumplen con las condiciones establecidas, no lo son. Esto se puede lograr manteniendo el equipo, **realizando reparaciones de** hardware, **manteniendo los sistemas operativos y el software actualizados, y creando copias** de seguridad .

### **La protección de la información en cada uno de sus estados posibles.**

![seguridad%20de%20redes%202%20b55173737ff04e08975955602227137c/image15.png](seguridad%20de%20redes%202%20b55173737ff04e08975955602227137c/image15.png)

### **Las medidas de seguridad utilizadas para proteger los datos.**

![seguridad%20de%20redes%202%20b55173737ff04e08975955602227137c/image16.png](seguridad%20de%20redes%202%20b55173737ff04e08975955602227137c/image16.png)

- **La concientización**, la capacitación y la educación son las medidas implementadas por una organización para garantizar que los usuarios estén informados sobre las posibles amenazas a la seguridad y las acciones que pueden tomar para proteger los sistemas de información.
- **La tecnología** se refiere a las soluciones basadas en software (y hardware) diseñadas para proteger los sistemas de información como los firewalls, que monitorean continuamente tu red en busca de posibles incidentes maliciosos.
- **La política y el procedimiento** se refieren a los controles administrativos que proporcionan una base para la forma en que una organización implementa el aseguramiento de la información, como los planes de respuesta a incidentes y las pautas de mejores prácticas.

## Amenazas y vulnerabilidades de la seguridad de los datos

### **¿Quién más quiere mis datos?**

Tu proveedor de Internet (ISP) Tu ISP hace un seguimiento de tu actividad en línea y, en algunos países, puede vender estos datos a los anunciantes con fines de lucro. En ciertas circunstancias, es posible que los ISP tengan la obligación legal de compartir tu información con las agencias o autoridades de vigilancia del gobierno.

- **Anunciantes:** La publicidad dirigida forma parte de la experiencia de Internet. Los anunciantes monitorean y rastrean tus actividades en línea, como los hábitos de compra y las preferencias personales, y envían anuncios dirigidos a tu manera.
- **Motores de búsqueda y plataformas de redes sociales:** Estas plataformas recopilan información sobre tu género, geolocalización, número de teléfono e ideologías políticas y religiosas en función de tus historiales de búsqueda y tu identidad en línea. Luego, esta información se vende a los anunciantes con fines de lucro.
- **Sitios web que visita:** Los sitios web utilizan cookies para rastrear sus actividades con el fin de brindar una experiencia más personalizada. Pero esto deja un rastro de datos que está vinculado a tu identidad en línea que a menudo puede terminar en manos de los anunciantes.

Es obvio que los ciberdelincuentes son cada vez más sofisticados en tu búsqueda de datos personales valiosos. Pero también representan una enorme amenaza para los datos de la organización.

Veamos diferentes tipos de ataque que peuden poner en riesgo las disponibilidad, la integridad y la confidencialidad.

Es extensa la lista de los **tipos de ciberataques** porque existen miles de variantes. No obstante, te daremos a conocer los más comunes a los que diversas industrias se enfrentan día a día.

### **Ransomware o “secuestro de datos”**

Dentro de los tipos de ciberataques, el *ramsomware* es un malware encriptado para rechazar el acceso a los recursos, tales como los archivos de usuario con el fin de obligar al propietario del sistema infectado a pagar una especie de “rescate” con el fin de recuperar el acceso a los recursos cifrados.

Este ejemplo de ciberataque es uno de los más comunes; además de la encriptación de los datos, también se utilizan técnicas de extorsión, ya que si no se paga el monto establecido los piratas informáticos amenazan con exponer información confidencial.

### **Malware o “software malicioso”**

Como lo vimos antes, el *ramsomware* sólo es una parte de esta gran familia de código malicioso utilizado en los ciberataques. Este puede ser usado para diversos propósitos:

- Robo de información
- Alteración de contenido
- Daño de un sistema informático de forma permanente

**Entre los tipos de malware más comunes podemos encontrar los siguientes:**

- ***Botnet malware:*** Se utilizan para actividades delictivas y funcionan a través de una *botnet* en donde se instalan sistemas infectados.
- ***Cryptominers:*** Adquisición de criptomonedas desde la computadora de la víctima.
- ***Troyanos bancarios:*** Extraen información y credenciales de instituciones financieras, o de los usuarios, con el objetivo de robar o transferir recursos de manera electrónica.
- ***Mobile*** ***malware:*** Mediante aplicaciones móviles, se instala código malicioso.
- ***Rootkits***: Se instala en los dispositivos con el objetivo de dar control total al atacante.
- ***Adware***: Presentación de anuncios para obtener información o instalar algún software malicioso.

## **Phishing**

Los correos electrónicos de phishing pueden ser difíciles de detectar. Por ejemplo, a menudo se dirigirán a vos por tu nombre para parecer legítimos, pero los ciberdelincuentes pueden encontrar fácilmente esta información en Internet. Por lo tanto, es importante mantenerse alerta y pensar antes de hacer clic. El phishing es muy común y, a menudo, funciona. Por ejemplo, en agosto de 2020, la marca de juegos de élite Razer sufrió una violación de datos que expuso la información personal de aproximadamente 100 000 clientes.

Un consultor de seguridad descubrió que un clúster en la nube (un grupo de servidores vinculados que proporcionan almacenamiento de datos, bases de datos, redes y software a través de Internet) estaba mal configurado y expuso un segmento de la infraestructura de Razer a la Internet pública, lo que provocó una fuga de datos. Razer tardó más de tres semanas en proteger la instancia en la nube del acceso público, tiempo durante el cual los ciberdelincuentes tuvieron acceso a la información de los clientes que podría haberse utilizado en ataques de ingeniería social y fraude, como la que acaba de descubrir.

Los correos electrónicos de phishing pueden ser difíciles de detectar. Por ejemplo, a menudo se dirigirán por tu nombre para parecer legítimos, pero los ciberdelincuentes pueden encontrar fácilmente esta información en Internet. Por lo tanto, es importante mantenerse alerta y pensar antes de hacer clic. El phishing es muy común y, a menudo, funciona. Por ejemplo, en agosto de 2020, la marca de juegos de élite Razer sufrió una violación de datos que expuso la información personal de aproximadamente 100 000 clientes.

Un consultor de seguridad descubrió que un clúster en la nube (un grupo de servidores vinculados que proporcionan almacenamiento de datos, bases de datos, redes y software a través de Internet) estaba mal configurado y expuso un segmento de la infraestructura de Razer a la Internet pública, lo que provocó una fuga de datos.

Razer tardó más de tres semanas en proteger la instancia en la nube del acceso público, tiempo durante el cual los ciberdelincuentes tuvieron acceso a la información de los clientes que podría haberse utilizado en ataques de ingeniería social y fraude, como la que acaba de descubrir. Por lo tanto, las organizaciones deben adoptar un enfoque proactivo de la seguridad en la nube para garantizar que los datos confidenciales estén protegidos.

## **Denegación de servicio**

![seguridad%20de%20redes%203%20c295661c6a5741b1a91532efe7ca8c9e/image1.jpg](seguridad%20de%20redes%203%20c295661c6a5741b1a91532efe7ca8c9e/image1.jpg)

### **Los ataques de denegación de servicio (DoS)**

son un tipo de ataque de red que es relativamente sencillo de llevar a cabo, incluso por parte de un atacante no cualificado. Un ataque DoS da como resultado cierto tipo de interrupción del servicio de red a los usuarios, los dispositivos o las aplicaciones.

- **Cantidad abrumadora de tráfico:** Esto es cuando se envía una gran cantidad de datos a una red, a un host o a una aplicación a una velocidad que no pueden procesar. Esto ocasiona una disminución de la velocidad de transmisión o respuesta o una falla en un dispositivo o servicio.
- **Paquetes malicioso formateados:** Un paquete es una colección de datos que fluye entre una computadora o aplicación de origen y una receptora a través de una red, como Internet. Cuando se envía un paquete con formato malicioso, el receptor no puede manejarlo. Por ejemplo, si un atacante reenvía paquetes que contienen errores o paquetes formateados incorrectamente que no pueden ser identificados por una aplicación, esto hará que el dispositivo receptor funcione muy lentamente o se bloquee. Los ataques de DoS se consideran un riesgo importante porque pueden interrumpir fácilmente la comunicación y causar una pérdida significativa de tiempo y dinero.
- **DoS distribuido:** Un ataque DoS distribuido (DDoS) es similar a un ataque DoS pero proviene de múltiples fuentes coordinadas. Por ejemplo:
    - Un atacante crea una red (botnet) de hosts infectados llamados zombies, que son controlados por sistemas de manejo.
    - Las computadoras zombis constantemente analizan e infectan más hosts, creando más y más zombis.
    - Cuando está listo, el hacker proporciona instrucciones a los sistemas manipuladores para que los botnet de zombies lleven a cabo un ataque de DDoS.

## **Ingeniería social:**

Es la manipulación a las personas para que realicen acciones o divulguen información confidencial. Los ingenieros sociales con frecuencia dependen de la disposición de las personas para ayudar, pero también se aprovechan de sus vulnerabilidades. Por ejemplo, un atacante llamará a un empleado autorizado con un problema urgente que requiere acceso inmediato a la red y apelará a la vanidad o la codicia del empleado o invocará la autoridad mediante el uso de técnicas de eliminación de nombres para obtener este acceso.

**¿Cómo funciona la ingeniería social?**

![seguridad%20de%20redes%203%20c295661c6a5741b1a91532efe7ca8c9e/image2.jpg](seguridad%20de%20redes%203%20c295661c6a5741b1a91532efe7ca8c9e/image2.jpg)

**Tipos de Ingeniería Social**

![seguridad%20de%20redes%203%20c295661c6a5741b1a91532efe7ca8c9e/image3.jpg](seguridad%20de%20redes%203%20c295661c6a5741b1a91532efe7ca8c9e/image3.jpg)

Ataques en 2 niveles:

![seguridad%20de%20redes%203%20c295661c6a5741b1a91532efe7ca8c9e/image4.jpg](seguridad%20de%20redes%203%20c295661c6a5741b1a91532efe7ca8c9e/image4.jpg)

**¿Cómo protegernos?**

- Concientizar a las personas y educar sobre seguridad
- Fomentar la adopción de medidas preventivas;
- Nunca divulgar información sensible con desconocidos o en lugares públicos;
- Implementar políticas de seguridad en la organización
- Efectuar controles de seguridad fisica para reducir el peligro inherente a las personas;
- Realizar auditorías y hacer ingeniería social para detectar huecos de seguridad de esta naturaleza.

## Medidas de seguridad para la seguridad de los datos

### **Ingeniería de la seguridad de datos**

**Pensar en seguridad de datos y construir defensas desde el primer momento es de vital importancia**. Los ingenieros de seguridad tienen como objetivo proteger la red de las amenazas desde su inicio hasta que son confiables y seguras. **Los ingenieros de seguridad diseñan sistemas que protegen las cosas correctas de la manera correcta. Si el objetivo de un ingeniero de software es asegurar que las cosas sucedan, el objetivo del ingeniero de seguridad es asegurar que las cosas (malas) no sucedan** diseñando, implementando y probando sistemas completos y seguros.

La ingeniería de seguridad cubre mucho terreno e incluye muchas medidas, **desde pruebas de seguridad y revisiones de código regulares hasta la creación de arquitecturas de seguridad y modelos de amenazas** para mantener una red bloqueada y segura desde un punto de vista holístico.

### **Encriptación**

Si la ingeniería de seguridad de datos protege la red y otros activos físicos como servidores, computadoras y bases de datos, **la encriptación protege los datos y archivos reales almacenados en ellos o que viajan entre ellos a través de Internet**. Las estrategias de encriptación son cruciales para cualquier empresa que utilice la nube y son una excelente manera de proteger los discos duros, los datos y los archivos que se encuentran en tránsito a través de correo electrónico, en navegadores o en camino hacia la nube.

En el caso de que los datos sean interceptados, la encriptación dificulta que los hackers hagan algo con ellos. Esto se debe a que **los datos encriptados son ilegibles para usuarios no autorizados sin la clave de encriptación**. La encriptación no se debe dejar para el final, y debe ser cuidadosamente integrada en la red y el flujo de trabajo existente para que sea más exitosa.

### **Detección de intrusión y respuesta ante una brecha de seguridad**

Si en la red ocurren acciones de aspecto sospechoso, como alguien o algo que intenta entrar, la detección de intrusos se activará. **Los sistemas de detección de intrusos de red (NIDS) supervisan de forma continua y pasiva el tráfico de la red en busca de un comportamiento que parezca ilícito o anómalo y lo marcan para su revisión**. Los NIDS no sólo bloquean ese tráfico, sino que **también recopilan información sobre él y alertan a los administradores de red**.

Pero a pesar de todo esto, las brechas de seguridad siguen ocurriendo. Es por eso que **es importante tener un plan de respuesta a una violación de datos**. Hay que estar preparado para entrar en acción con un sistema eficaz. Ese sistema se puede actualizar con la frecuencia que se necesite, por ejemplo si hay cambios en los componentes de la red o surgen nuevas amenazas que deban abordarse. **Un sistema sólido contra una violación garantizará que tienes los recursos preparados y que es fácil seguir un conjunto de instrucciones para sellar la violación y todo lo que conlleva**, ya sea que necesites recibir asistencia legal, tener pólizas de seguro, planes de recuperación de datos o notificar a cualquier socio de la cuestión.

### **Firewall**

¿Cómo mantener a visitantes no deseados y software malicioso fuera de la red? Cuando estás conectado a Internet, una buena manera de asegurarse de que sólo las personas y archivos adecuados están recibiendo nuestros datos es mediante **firewalls: software o hardware diseñado con un conjunto de reglas para bloquear el acceso a la red de usuarios no autorizados**. Son excelentes líneas de defensa para evitar la interceptación de datos y bloquear el malware que intenta entrar en la red, y también evitan que la información importante salga, como contraseñas o datos confidenciales.

### **Análisis de vulnerabilidades**

Los hackers suelen analizar las redes de forma activa o pasiva en busca de agujeros y vulnerabilidades. Los analistas de seguridad de datos y **los profesionales de la evaluación de vulnerabilidades son elementos clave en la identificación de posibles agujeros y en cerrarlos**. **El software de análisis de seguridad se utiliza para aprovechar cualquier vulnerabilidad de un ordenador, red o infraestructura de comunicaciones, priorizando y abordando cada uno de ellos con planes de seguridad de datos que protegen, detectan y reaccionan**.

### **Pruebas de intrusión**

El análisis de vulnerabilidad (que identifica amenazas potenciales) también puede incluir deliberadamente investigar una red o un sistema para detectar fallos o hacer **pruebas de intrusión. Es una excelente manera de identificar las vulnerabilidades antes de tiempo y diseñar un plan para solucionarlas**. Si hay fallos en los sistemas operativos, problemas con incumplimientos, el código de ciertas aplicaciones u otros problemas similares, un administrador de red experto en pruebas de intrusión puede ayudarte a localizar estos problemas y aplicar parches para que tengas menos probabilidades de tener un ataque.

**Las pruebas de intrusión implican la ejecución de procesos manuales o automatizados que interrumpen los servidores, las aplicaciones, las redes e incluso los dispositivos de los usuarios finales para ver si la intrusión es posible y dónde se produjo esa ruptura. A partir de esto, pueden generar un informe para los auditores como prueba de cumplimiento.**

Una prueba de intrusión completa **puede ahorrarte tiempo y dinero** al prevenir ataques costosos en áreas débiles que no conoces. El tiempo de inactividad del sistema puede ser otro efecto secundario molesto de ataques maliciosos, por lo que hacer pruebas de intrusión con regularidad es una excelente manera de evitar problemas antes de que surjan.

### **Información de seguridad y gestión de eventos**

Hay una línea aún más holística de defensa que se puede emplear para mantener los ojos en cada punto de contacto. Es lo que se conoce como **Información de Seguridad y Gestión de Eventos (SIEM)**. SIEM es un enfoque integral que **monitoriza y reúne cualquier detalle sobre la actividad relacionada con la seguridad de TI que pueda ocurrir en cualquier lugar de la red, ya sea en servidores, dispositivos de usuario o software de seguridad como NIDS y firewalls**. Los sistemas SIEM luego compilan y hacen que esa información esté centralizada y disponible para que se pueda administrar y analizar los registros en tiempo real, e identificar de esta forma los patrones que destacan.

Estos sistemas pueden ser bastante complejos de configurar y mantener, por lo que es importante contratar a un experto administrador SIEM.

### **Ciberseguridad: HTTPS, SSL y TLS**

Internet en sí mismo se considera una red insegura, lo cual es algo que puede asustar cuando nos damos cuenta que actualmente es la espina dorsal de muchas de las transacciones de información entre organizaciones. Para protegernos de que, sin darnos cuenta, compartamos nuestra información privada en todo Internet, existen diferentes estándares y protocolos de cómo se envía la información a través de esta red. **Las conexiones cifradas y las páginas seguras con protocolos HTTPS pueden ocultar y proteger los datos enviados y recibidos en los navegadores. Para crear canales de comunicación seguros, los profesionales de seguridad de Internet pueden implementar protocolos TCP/IP (con medidas de criptografía entretejidas) y métodos de encriptación como Secure Sockets Layer (SSL) o TLS (Transport Layer Security)**.

El software anti-malware y anti-spyware también es importante. Está diseñado para supervisar el tráfico de Internet entrante o el malware como spyware, adware o virus troyanos.

### **Detección de amenazas en punto final**

Se pueden prevenir ataques de ransomware siguiendo buenas prácticas de seguridad, como tener software antivirus, el último sistema operativo y copias de seguridad de datos en la nube y en un dispositivo local. Sin embargo, esto es diferente para organizaciones que tienen múltiple personal, sistemas e instalaciones que son susceptibles a ataques.

**Los usuarios reales, junto con los dispositivos que usan para acceder a la red (por ejemplo, teléfonos móviles, ordenadores portátiles o sistemas TPV móviles), suelen ser el eslabón más débil de la cadena de seguridad. Se deben implementar varios niveles de protección, como tecnología de autorización que otorga acceso a un dispositivo a la red.**

### **Prevención de pérdida de datos (DLP)**

Dentro de la seguridad de punto final hay otra estrategia de seguridad de datos importante: la **prevención de pérdida de datos (DLP)**. Esencialmente, esto abarca las medidas que se toman para asegurar que no se envían datos confidenciales desde la red, ya sea a propósito, o por accidente. **Puede implementarse software DLP para supervisar la red y asegurarse de que los usuarios finales autorizados no estén copiando o compartiendo información privada o datos que no deberían**.

<aside>
💡 **LIMITAR EL ACCESO A LA INFORMACIÓN**
Es importante que **se proteja la información limitando su disponibilidad**. Algunas de las acciones más comunes es **cifrar la información** para que todo aquel que pretenda acceder a **datos privados** no pueda hacerlo sin conocer la **clave** de descifrado.

En el caso de las empresas para la continuidad del negocio, se deberá **delimitar el acceso** a datos sensibles de la empresa a los trabajadores.

</aside>

### **Contraseñas seguras y dinámicas**

Aunque pueda parecer una obviedad, aún existen usuarios, en la era de la transformación digital, que utilizan contraseñas basándose en secuencias básicas como puede ser 1234 o ABCD. Para que una contraseña se considere segura debe contar con **un mínimo de 8 caracteres y contener al menos una mayúscula, números y caracteres especiales.**

Otra de las recomendaciones a tener en cuenta es que las contraseñas deben ser **aleatorias**, **evitando utilizar información personal**. Además, éstas deben ser diferentes para cada dispositivo o cuenta y deben **cambiarse periódicamente**.

Aunque pueda parecer una tarea complicada, existen **herramientas que permiten generar contraseñas seguras**. Una de las opciones más comunes para aquellos que no logren recordar nunca las claves consiste en crear un **fichero con todas las contraseñas**. Este documento debe estar protegido por un antivirus.

Estas contraseñas deben **aplicarse también en las redes de casa** como puede ser el router de ADSL y Wi-fi.

### Proteger correo electrónico

El **correo electrónico**, junto con las redes sociales, se ha convertido en una **fuente de información sensible** que debe ser protegida. Hay que ser consciente de todos los datos que se pueden concentrar en el correo, así como de las múltiples trampas que existen como el ***pishing***, con la que pueden extraer hasta datos sobre nuestra **tarjeta de crédito**.

Una de las medidas de seguridad que se recomienda es la de **usar filtros antispam**, así como **sistemas de encriptación de mensajes**. Con estas acciones **se asegurará la** **protección y privacidad de la información almacenada** en el correo electrónico. El ataque a correos electrónicos es una de las **amenazas y fraudes en los sistemas de información** más recurrentes.

### Realizar backups y borrados seguros

**Realizar periódicamente *backups* o copias de seguridad** es otra de las acciones que hay que hacer si queremos proteger nuestra **base de datos.**

Para no perder datos que interfieran en la actividad de cualquier empresa, así como fotografías o contenido personal es fundamental realizar copias de seguridad cada cierto tiempo. Aunque, igual de importante es **restablecer esa información, como eliminar la que ya no resulta útil** de forma segura.

### Acceder a páginas web y compras seguras

Otro de los errores más comunes de los usuarios es acceder a páginas web que no cuentan con el protocolo **https en su URL**. Si dispone de la **ese final** eso significa que la página web o *site* **cumple con los estándares de seguridad**.

Además de vigilar la URL, también es importante **ver los métodos de pago electrónico que ofrece la página web.** Cada vez son más los *e-commerce* que dentro de su pasarela de pago incluyen varios procesos de verificación para que la transacción sea lo más segura posible.

### Almacenamiento en la nube, en red y local

Posiblemente, este consejo puede ir más vinculado al uso empresarial, aunque como particulares también es una opción a considerar. La **nube** es un espacio de almacenamiento virtual que permite almacenar todo tipo de información. Ahora bien, al estar en la red es vital que esté bien protegido ante cualquier **ataque dirigido**. Otro de los sistemas de almacenamiento de datos a los que se puede recurrir son el **almacenamiento local**, mediante **dispositivos físicos**, y el **almacenamiento Red**, el cual almacena la información en una **red interna** a la que se puede acceder mediante unos permisos.

### Contratar servicios de seguridad integral y actualizaciones al día

Aunque parezca increíble, aún existen usuarios que no tienen un antivirus instalado en sus terminales informáticas. Ya seas una empresa o un particular **debes tener instalados softwares integrales de seguridad** como son el **antivirus**, el **anti espías** o un **firewall**. Con esta acción lograrás proteger la información ante cualquier posible ataque.

Además de contar con servicios de seguridad integral es importante que todos los programas y sistemas operativos instalados en el pc estén actualizados. Siempre hay que intentar tener la última versión.

### Vigilar las conexiones a internet wi-fi y navegaciones

Los expertos aconsejan **activar los modos privados en los navegadores y controlar y borrar las cookies** para no dejar rastro de nuestra actividad en los sitios web visitados.

Otra de las acciones que se tienen que hacer para preservar esa seguridad en el acceso a internet es la de **no conectarse a redes Wi-fi públicas**. Aunque, a priori, pueda ser un servicio muy útil, es un arma de doble filo. Todas las líneas Wi-fi abiertas o compartidas **pueden llevar a la identificación personal**. Siempre y cuando no exista un mecanismo de cifrado ni redes privadas virtuales (VPN), hay que evitar su uso.

### Proteger el teléfono móvil

Los teléfonos móviles se han convertido con el paso de los años en una extensión más de nosotros. Es tal su evolución que en la actualidad ya se puede tener la cuenta bancaria vinculada, sesiones iniciadas para comprar en e-commerce, etc.

Igual que sucede con el PC debemos **proteger todos los accesos posibles del móvil mediante patrones o contraseñas**. Además de datos bancarios, también se encuentra el correo electrónico, imágenes y vídeos personales, conversaciones privadas en aplicaciones de mensajería instantánea…

Además de proteger el teléfono móvil mediante patrones, también se debe **realizar, periódicamente, copias de seguridad** para minimizar el riesgo de pérdida de datos.

### Cierre de sesiones y apagón de internet

Por último, otras de las medidas de seguridad que debes tomar durante tu actividad en la red es la de **cerrar la sesión y apagar internet si ya no lo vas a usar más.** Al desconectarlo reducirás la posibilidad de sufrir un **ataque informático**. También puedes utilizar el **modo avión**, si lo deseas.

En el caso de un acceso en espacios públicos, deberás tener muy presente durante el registro la **casilla de recordar contraseña**. **Nunca la aceptes**, puesto que esta opción se encarga de guardar la clave y cualquiera podría entrar, aún desconociéndola.

Estos han sido algunos de los consejos sobre ciberseguridad más extendidos hasta el momento, tanto para empresas como para particulares. Si te parece interesante cómo combatir las **amenazas y fraudes en los sistemas de información** el **[Máster en Seguridad Informática y Gestión del Riesgo Tecnológico](https://www.euncet.es/es/master-online-ciberseguridad)** es para ti. ¡Descubre cómo ser un **experto en informática** y seguridad!

## **Las 9 medidas que aseguran la información de tu empresa**

Cumpliendo estas **9 medidas de seguridad informática básicas,** nuestra empresa podrá garantizar que sus datos se encuentran protegidos.

**1. Controles de acceso a los datos más estrictos**

**¿Cómo proteger la información de una empresa?** Una de las principales medidas de [seguridad](https://www.datos101.com/empresa-ciberseguridad-madrid/) es limitar el acceso a la información. Cuantas menos personas accedan a una información, menor será el riesgo de comprometerla. Por lo tanto, es necesario implantar en nuestra empresa un sistema que impida dar acceso a datos innecesarios, a un usuario, cliente, etc.

**2. Realizar copias de seguridad**

Poseer un sistema de [copias de seguridad](https://www.datos101.com/copias-de-seguridad-en-la-nube-para-empresas/) periódico permite que la empresa garantice que puede recuperar los datos ante una incidencia de carácter catastrófico, impidiendo la pérdida de los mismos y permitiendo la recuperación de la normalidad en el trabajo en apenas unos minutos.

**3. Utilizar contraseñas seguras**

El acceso a las distintas plataformas que utiliza la empresa (correo electrónico, servidor de copias de [seguridad NAS](https://www.datos101.com/nas-backup-almacenamiento/), etc.) debe realizarse utilizando claves de seguridad (contraseñas) seguras, que impidan que puedan ser fácilmente descubiertas por piratas informáticos. El uso de contraseñas seguras es una de las medidas de seguridad informática más importantes en una empresa.

**4. Proteger el correo electrónico**

Hoy en día, la mayoría de comunicaciones de nuestra empresa la realizamos utilizando el [correo electrónico](https://www.datos101.com/backup-office-365/). Por lo tanto, otra medida de seguridad es utilizar filtros antispam y sistemas de encriptado de mensajes, para asegurar la protección y privacidad de toda esa información.

**5. Contratar un software integral de seguridad**

**¿Cómo proteger la información en internet?** La mejor forma es contratando un paquete de seguridad integral que contenga [antivirus,](https://www.datos101.com/bitdefender-antivirus/) antiespías, antimalware, firewall, etc., y que permita proteger la información ante posibles ataques externos a través de internet.

**6. Utilizar software DLP**

Existen programas de prevención de pérdidas de datos (DLP) que pueden ser implementados como medida de seguridad en nuestra empresa para supervisar que ningún usuario esté copiando o compartiendo información o datos que no deberían.

**7. Trabajar en la nube**

Trabajar en la nube permite, entre otras ventajas, contar con los sistemas de seguridad de la información que posee el proveedor de servicios. Además, este proveedor será responsable de esa seguridad.

**8. Involucrar a toda la empresa en la seguridad**

Para que las **medidas de seguridad informática** de una empresa funcione, debemos involucrar en su participación a todos los estamentos que participan en la misma, incluyendo a los agentes externos como puedan ser clientes, proveedores, etc. Muchas veces, nuestra empresa tiene implantados los sistemas correctos de seguridad, y la brecha en la misma, se produce al relacionarnos con un tercero que carece de estas medidas de seguridad.

**9. Monitorización continua y respuesta inmediata**

Debemos implantar en nuestra empresa un sistema que permita monitorizar la gestión de los datos y detectar aquellos posibles fallos o actuaciones incorrectas. Este sistema de control permitirá actuar rápidamente para solventar cualquier incidencia y minimizar su repercusión.

## **Elaborar una política de seguridad de la información**

Dar importancia a la seguridad de la Empresa es fundamental. Por ello es necesario fijar quién será el responsable de gestionar la ciberseguridad en la pequeña y mediana empresa y **elaborar una Política de Seguridad que determine los riesgos** que se van a aceptar. Además, es crucial que todos los empleados o colaboradores entiendan la importancia de la seguridad. debe contemplar lo siguiente:

- Debe garantizar la integridad de la información, los equipos que la contienen y los procesos a la que es sometida.
- Debe proteger la confidencialidad de la información.
- Debe regular la disponibilidad de la información de manera que esté siempre a disposición de la persona autorizada para su uso, en cualquier momento y circunstancia.

![seguridad%20de%20redes%203%20c295661c6a5741b1a91532efe7ca8c9e/image5.jpg](seguridad%20de%20redes%203%20c295661c6a5741b1a91532efe7ca8c9e/image5.jpg)

requiere de innumerables tareas, muchas de ellas técnicas. Pero otras relacionadas con la administración general de la organización, que van desde contar con el presupuesto adecuado para la implementación hasta vencer los reparos que por distintos modelos mentales existan sobre su uso.

deben asegurar que la política de seguridad de la información a establecer sea la más conveniente para la organización dentro de los recursos con que se cuente y no resulte solamente un “maquillaje”.

En general se adopten los criterios de la **Norma ISO 27002**, que establece los principios generales para el inicio, la implementación, el mantenimiento y la mejora continua de la gestión de la seguridad de la información en una organización.

## **Monitorizar de redes y servicios**

![seguridad%20de%20redes%203%20c295661c6a5741b1a91532efe7ca8c9e/image6.jpg](seguridad%20de%20redes%203%20c295661c6a5741b1a91532efe7ca8c9e/image6.jpg)

Es necesario que la red de la PYME esté protegida tanto de ataques externos como internos. Conviene comprobar si el proveedor de internet **incluye un cortafuegos que controle las conexiones de red** de acceso a internet y que todas ellas estén vigiladas.

Detectar fallos de hardware o una actividad anormal es más fácil con **herramientas que incluso son gratuitas**. Es recomendable utilizarlas y si hablamos de una mediana empresa conviene elegir otras opciones que incluyen análisis de tráfico, uso de IP, etc. Los **Mecanismos detectivos** se desarrollan para detectar cambios en el sistema con el objetivo de alertar sobre algún intento de intrusión. Se usan herramientas que monitorean y avisan de cambios realizados, asegurando la integridad de la información que se encuentra en los sistemas de almacenamiento.

Estos sistemas están continuamente supervisando los componentes de red y las personas o intrusos que están intentando entrar ilegalmente en ella, describiendo las actividades o procesos que realizan los individuos o sistemas no autorizados sobre los elementos de la red. Operan cuando ya se produjo el ataque y se genera un registro y una alerta.

En la práctica, encontraremos estos sistemas cuando una empresa tiene computadores en red e intercambian información de valor. Los más utilizados en la actualidad son los IDS **s*oftware* de seguridad** que se encarga de monitorear la red y/o dispositivos conectados a esta, para detectar intentos de acceso no autorizados y generar una alerta para notificar al administrador del sistema, que será quien determine el tipo de respuesta o acción a tomar con base en la información recibida.

Un IDS **pasivo** que detecte actividad maliciosa, generará alertas o entradas de registro, pero no tomará medidas. **Un IDS activo,** (IDPS) también podrá configurarse para tomar medidas, como bloquear direcciones IP o cerrar el acceso a recursos restringidos.

## **Controlar los usuarios y dispositivos extraíbles**

Es importante **controlar quiénes son los usuarios y donde entran en una red de una empresa**. El administrador debe controlar a los usuarios y se recomienda solo dar acceso a los espacios que los empleados necesiten dentro de la plataforma. Los datos o información personal deben estar separados y vigilados.

Los dispositivos extraíbles como memorias USB, Tarjetas SD, etc. pueden en un momento determinado ser fuente de origen de malware. Por ello **se recomienda que sean controladas y proporcionadas por el administrador** de sistema y se escanee su contenido antes de su uso.

## **Contratar un profesional o empresa en seguridad informática**

Es crucial **invertir en su contratación para estar protegido** tanto por ataques propios como por daños que se puedan hacer a terceros.

## **Puntos importantes de seguridad a tomar en cuenta:**

- No usar la misma contraseña para todas las cuentas
- No creer en anuncios fraudulentos
- Tener siempre cuidado a los enlaces de ciertos ads
- Tener cuidado con las paginas que te piden el uso de las cookies.
- Tener cuidado de no mostrar información confidencial en algún archivo que vaya a ser mostrado en publico o a personas ajenas a la empresa.
- Tener cuidado de quien esta observando tu pantalla
- Evitar entrar a redes abiertas en los comercios o lugares públicos.
- Si es necesario entrar a una red abierta usar un VPN.

**Celular:**

- Contraseña, patrón, pin, etc.
- Mostrar las notificaciones de información importante (Estando bloqueado el celular).

**Computadora:**

- Acceso a múltiples perfiles o sesiones.
- Protección con contraseña, huella digial, etc
- No dejar la computadora desbloqueada cuando la dejemos de usar.
- Verificar que al navegar por internet el navegador contenga la “s” (https)

**Libretas:**

- No dejar información confidencial o importante anotada en libretas
- Tener bajo cuidado estas libretas

**Inicio de sesiones:**

- Usar gestores de contraseñas.
- No dejar contraseñas en postic o papelitos escondidos.
- No mandar contraseñas en mensajes
- No guardar contraseñas en notas

## **Decálogo de ciberseguridad:**

![seguridad%20de%20redes%203%20c295661c6a5741b1a91532efe7ca8c9e/image7.jpg](seguridad%20de%20redes%203%20c295661c6a5741b1a91532efe7ca8c9e/image7.jpg)

- Debemos proteger nuestro **puesto de trabajo** y mantener limpio de papeles que contengan información sensible.
- Es recomendable establecer en tu **dispositivo móvil** una clave de acceso y la opción de bloqueo automático
- No hagas uso de **equipos no corporativos**. Si es necesario, no manejes información corporativa en este tipo de equipos.
- Evita las **fugas de información**. No mantengamos conversaciones confidenciales en lugares donde puedan ser oídas por terceros.
- **Las contraseñas** deben ser secretas y únicas, no debemos anotarlas, compartirlas o reutilizarlas.
- Se debe realizar una **navegación segura** y evitar acceder a páginas no confiables.
- Utilizar el **correo electrónico** de forma segura y elimina o informa a tu departamento de informática todo correo sospechoso que recibas.
- Protege **la información** y realiza copias de seguridad de la información sensible que sólo esté en nuestro equipo.
- Cuando **viajes**, no envíes información sensible a través de redes WiFi no confiables.
- **Todos somos seguridad** Debemos avisar al departamento de seguridad si detectamos cualquier actividad sospechosa.
- Desactiva las notificaciones con pantalla bloqueada del celular
- Bloquea el PC de escritorio cuando no lo estes usando
- Usa un gestor de cuentas, no uses la misma contraseña
- No escribas tu contraseña en un post it o en un block de notas, tampoco la mandes por la web
- Asegurate de usar https (cifrado)
- No hagas click en ventanas emergentes de origen desconocido
- No muestres informacion confifencial en grandes pantallas o muy visibles
- Cuidado con quien observa tu pantalla
- Usa VPN cuando te conectes a redes publicas

## **Un Tip Relevante, el Uso de 3 Emails Diferentes:**

- Email Publico: Subscripciones, newsletters, RRSS. Es el correo que compartes para crear cuentas que no sean importante o para dar a un servicio que quieras probar.
- **Email Personal:** Para la familia, amigos, datos personales, registro civil. Bancos. Cosas serias y personales.
- **Email Corporativo:** Solo usado para ámbito laborar.

Con tus correos distribuidos en estas 3 cuentas, puedes tener mejor control de los correos que llegan, contener correos basura o spam, levantar alarmas en caso de la llegada de un correo fue de lugar. También podrás tener seguridad de que si el correo Email Publico, es comprometido, no alcanzarán tus datos personales.

![seguridad%20de%20redes%203%20c295661c6a5741b1a91532efe7ca8c9e/image8.jpg](seguridad%20de%20redes%203%20c295661c6a5741b1a91532efe7ca8c9e/image8.jpg)

## **Tecnología que más usamos:**

- **Celular:** recomendación, tener algún patrón o bloqueo, es importante que configures tu móvil para que no muestre las notificaciones en pantalla, así el teléfono este bloqueado, ya que puede ser información confidencial y puede ser leída por terceras personas.
- **Computadoras:** por ningún motivo dejes sin contraseña tu equipo de trabajo o personal, y por ningún motivo te levantes y lo dejes sin bloquear.
- **Bloc de notas:** en nuestro puntero, no solo escribimos lista de pendientes, también tenemos información personal y confidencial como clientes importantes, contraseñas que escribimos para no olvidar, cartas confidenciales, entre otros, lo mas importante es asegurarnos de no tener este tipo de información anotadas en libretas y estas libretas no deben estar al alcance de todos.

<aside>
⚠️ **Ten cuidado con quien observa tu pantalla**, ya que puedes tener chat abiertos con información confidencial o puedes tener tu banca en línea y no faltan las personas mal intencionadas que se pueden para detrás de nosotros y obtener esta información fácilmente que personal, privada y tuya o de la organización. Ten cuidado con esto, ya que es un ataque de ingeniería social bastante aplicada.

</aside>

**En caso de que manejes un celular empresario**, con información confidencial, ten cuidado de NO conectarte a redes abiertas o públicas, como la de las cafeterías o restaurantes, puedes ser víctima de un ataque llamado MAN IN THE MIDDLE, en el que las personas se infiltran y se aprovechan de la inseguridad de la red para meterse y obtener información que es confidencial y que esa persona no está autorizada para tener. Si lo vas a hacer usa una herramienta conocida como BPN para asegurarte de que la información va a viajar segura.

![seguridad%20de%20redes%203%20c295661c6a5741b1a91532efe7ca8c9e/image9.jpg](seguridad%20de%20redes%203%20c295661c6a5741b1a91532efe7ca8c9e/image9.jpg)

## **Seguridad al navegar**

En Internet asegúrate que en la barra de búsqueda veas la S después del http. (htpps:) Esto nos indica que la información está viajando cifrada al servidor. Si a la hora de navegar, te encuentras con un aviso como este

Que te hacen sentir especial, no hagas caso a este tipo de publicidad, ya que es engañosa y puede ser muy dañino para tu computador descargar este tipo de virus. En algunos casos, estas ventanas emergentes no son necesariamente malware o virus que se va a instalar en nuestros computadores, muchas veces son app que Google nos muestra y que son inocentes o tal vez te interesen, es importante fijarnos donde se encuentra ubicado el enlace de esa ventana emergente.

Otro tipo de ventana emergente es el siguiente: En el que te está avisando que van a capturar las cookies. En algunas empresas tiene pantallas gigantes donde muestran información, es importante que no tengan métricas ni información confidencial de la organización, porque muchas veces hay visitas de personas que no pertenecen a la organización y que quieren y pueden obtener acceso a esos datos y que no están autorizados a tener.

### **Contraseñas**

Para ingresar a tu equipo**,** ya se a tu correo, Instagram, Facebook, entre otros, asegúrate de tener un gestor de contraseñas, ya sea que tengas uno o que Google Chrome te ofrezca uno gestor de contraseñas. Nunca dejes la contraseña escrita en un post donde todos pueden verla y menos envíes la contraseña por mensajes de texto, no almacenes tu contraseña en un blog de nota dentro de tu computador porque se puede encontrar muy fácilmente y sobre todo, no uses la misma contraseña para todo.

Conceptos básicos de la gestión de incidentes de seguridad

Este grupo está enfocado principalmente en atender los incidentes de seguridad de la información que se presentan sobre los activos soportados por la plataforma tecnológica de la entidad.

![seguridad%20de%20redes%203%20c295661c6a5741b1a91532efe7ca8c9e/image10.png](seguridad%20de%20redes%203%20c295661c6a5741b1a91532efe7ca8c9e/image10.png)

### **Preparación**

Esta etapa dentro del ciclo de vida de respuesta a incidentes suele hacerse pensando no sólo en crear un modelo que permita a la entidad estar en capacidad de responder ante estos, sino también en la forma como pueden ser detectados, evaluados y gestionar las vulnerabilidades para prevenirse, asegurando que los sistemas, redes, y aplicaciones son lo suficientemente seguros . Aunque el equipo de respuesta a incidentes no es normalmente responsable de la prevención de incidentes, es muy importante que se considere como un componente fundamental de los programas de respuesta. El equipo de respuesta a incidentes debe actuar como una herramienta de experiencia en el establecimiento de recomendaciones para el aseguramiento de los sistemas de información y la plataforma que los soporta.

En esta etapa el grupo de gestión de incidentes o quien se designe para esta labor debe velar por la disposición de los recursos de atención de incidentes y las herramientas necesarias para cubrir las demás etapas del ciclo de vida del mismo, creando (si no existen) y validando (si existen) los procedimientos necesarios y programas de capacitación.

La etapa de preparación debe ser apoyada por la dirección de tecnologías de la información o quien haga sus veces, incluyendo las mejores prácticas para el aseguramiento de redes, sistemas, y aplicaciones por ejemplo:

· **Gestión de Parches de Seguridad:** las entidades dependiendo de su estratificación deben contar con un programa de gestión de vulnerabilidades (Sistemas Operativos, Bases de Datos, Aplicaciones, Otro Software Instalado), este programa ayudara a los administradores en la identificación, adquisición, prueba e instalación de los parches.

· **Aseguramiento de plataforma:** las entidades dependiendo de si estratificación deben ser aseguradas correctamente. Se debe configurar la menor cantidad de servicios (principio de menor privilegio) con el fin de proveer únicamente aquellos servicios necesarios tanto a usuarios como a otros equipos. Se deben revisar configuraciones por default (usuarios, contraseñas y archivos compartidos). Cada recurso que pueda ser accedido por externos e incluso por usuarios internos debe desplegar alguna advertencia. Los servidores deben tener habilitados sus sistemas de auditoría para permitir el login de eventos.

· **Seguridad en redes:** Debe existir una gestión constante sobre los elementos de seguridad. Las reglas configuradas en equipos de seguridad como firewalls deben ser revisadas continuamente. Las firmas y actualizaciones de dispositivos como IDS o IPS deben encontrarse al día. Todos los elementos de seguridad y de red deben encontrarse sincronizados y sus logs deben ser enviados a un equipo centralizado de recolección de logs para su respectivo análisis.

· **Prevención de código malicioso:** Todos los equipos de la infraestructura (servidores como equipos de usuario) deben tener activo su antivirus, antimalware con las firmas de actualización al día.

· **Sensibilización y entrenamiento de usuarios:** Usuarios en la entidad incluidos los administradores de TI deben ser sensibilizados de acuerdo a las políticas y procedimientos existentes relacionados con el uso apropiado de redes, sistemas y aplicaciones en concordancia con los estándares de seguridad de la entidad. Los encargados de los sistemas de información deben establecer las necesidades de capacitación de las personas encargadas de la protección de los datos.

Las actividades descritas anteriormente buscan prevenir la ocurrencia de incidentes de seguridad de la información que esta soportada por TI, y adicionalmente es necesario realizar una evaluación mensual.

### **Recursos de comunicación**

En este numeral se pretende enunciar los elementos necesarios para la comunicación del equipo de atención de incidentes dentro de la entidad.

- **Información de Contacto:** Se debe tener una lista de información de contacto de cada una de las personas que conforman el grupo de gestión de incidentes o quienes realicen sus funciones.
- **Información de Escalamiento:** Se debe contar con información de contacto para el escalamiento de incidentes según la estructura de la entidad.

**Política de Comunicación:** La entidad debe tener una política de comunicación de los incidentes de seguridad para definir que incidente puede ser comunicado a los medios y cual no.

<aside>
📖 - Información de los administradores de la plataforma tecnológica (Servicios, Servidores)
- Contacto con el área de recursos humanos o quien realice sus funciones (por si se realizan acciones disciplinarias).
- Contacto con áreas interesadas o grupos de interés (CCP - Policía Nacional, Fiscalía, entre otras)

</aside>

**Hardware y Software**

Para una correcta y eficiente gestión de incidentes la entidad debería tener en cuenta los siguientes elementos:

· Portátiles Forenses:

· Analizadores de protocolos.

· Software de adquisición.

· Software para recolección de evidencia.

· Kit de respuesta a incidentes.

· Software de análisis forense.

· Medios de almacenamiento

## **Recursos para el análisis de incidentes**

- Tener un listado de los puertos conocidos y de los puertos utilizados para realizar un ataque.
- Tener un diagrama de red para tener la ubicación rápida de los recursos existentes
- Una Línea – Base de Información de: Servidores (Nombre, IP, Aplicaciones, Parches, Usuarios Configurados, responsable de cambios). Esta información siempre debe estar actualizada para poder conocer el funcionamiento normal del mismo y realizar una identificación más acertada de un incidente.
- Se debe tener un análisis del comportamiento de red estándar en este es recomendable incluir: puertos utilizados por los protocolos de red, horarios de utilización, direcciones IP con que generan un mayor tráfico, direcciones IP que reciben mayor número de peticiones.

## Recursos para la mitigación y remediación

En este punto se consideran los elementos básicos para la contención de un posible incidente, Backup de Información, imágenes de servidores, y cualquier información base que pueda recuperar el funcionamiento normal del sistema.

### **Detección, evaluación y análisis**

**Detección Identificación y Gestión de Elementos Indicadores de un Incidente**

Los indicadores son los eventos que nos señalan que posiblemente un incidente ha ocurrido generalmente algunos de estos elementos son:

> · Alertas en sistemas de seguridad
> 
> 
> · Caídas de servidores
> 
> · Reportes de usuarios
> 
> · Software antivirus dando informes
> 
> · Otros funcionamientos fuera de lo normal del sistema
> 

La identificación y gestión de elementos que alertan sobre un incidente nos proveen información que puede alertarnos sobre la futura ocurrencia del mismo y preparar procedimientos para minimizar su impacto. Algunos de estos elementos pueden ser:

> · Logs de servidores
> 
> 
> · Logs de aplicaciones
> 
> · Logs de herramientas de seguridad
> 
> · Cualquier otra herramienta que permita la identificación de un incidente de seguridad
> 

En la entidad debe existir un listado de fuentes generadoras de eventos que permitan la identificación de un incidente de seguridad de la información.

### **Análisis**

Las actividades de análisis del incidente involucran otra serie de componentes, es recomendable tener en cuenta los siguientes:

> · Tener conocimientos de las características normales a nivel de red y de los sistemas.
> 
> 
> · Los administradores de TI deben tener conocimiento total sobre los comportamientos de la Infraestructura que están Administrando.
> 
> · Toda información que permita realizar análisis al incidente debe estar centralizada (Logs de servidores, redes, aplicaciones).
> 
> · Es importante efectuar correlación de eventos, ya que por medio de este proceso se pueden descubrir patrones de comportamiento anormal y poder identificar de manera más fácil la causa del incidente.
> 
> · Para un correcto análisis de un incidente debe existir una única fuente de tiempo (Sincronización de Relojes) ya que esto facilita la correlación de eventos y el análisis de información.
> 
> · Se debe mantener y usar una base de conocimiento con información relacionada sobre nuevas vulnerabilidades, información de los servicios habilitados, y experiencias con incidentes anteriores.
> 
> · Crear matrices de diagnóstico e información para los administradores menos experimentados.
> 

### **Evaluación**

Para realizar la evaluación de un incidente de seguridad se debe tener en cuenta los niveles de impacto con base en los insumos entregados por el análisis de riesgos y la clasificación de activos de información de la entidad. La severidad del incidente puede ser:

> · **Alto Impacto:** El incidente de seguridad afecta a activos de información considerados de impacto catastrófico y mayor que influyen directamente a los objetivos misionales del Instituto. Se incluyen en esta categoría aquellos incidentes que afecten la reputación y el buen nombre o involucren aspectos legales. Estos incidentes deben tener respuesta inmediata.
> 
> 
> · **Medio Impacto:** El incidente de seguridad afecta a activos de información considerados de impacto moderado que influyen directamente a los objetivos de un proceso determinado.
> 
> · **Bajo Impacto:** El incidente de seguridad afecta a activos de información considerados de impacto menor e insignificante, que no influyen en ningún objetivo. Estos incidentes deben ser monitoreados con el fin de evitar un cambio en el impacto.
> 

## **Clasificación De Incidentes De Seguridad De La Información**

Algunos ejemplos de clasificación de incidentes podrían ser (esta clasificación está sujeta a cada entidad dependiendo de su infraestructura, de sus riesgos y criticidad de los activos. La clasificación dada es solo un ejemplo):

- Acceso no autorizado: Es un incidente que involucra a una persona, sistema o código malicioso que obtiene acceso lógico o físico sin autorización adecuada del dueño a un sistema, aplicación, información o un activo de información.
- Modificación de recursos no autorizado: Un incidente que involucra a una persona, sistema o código malicioso que afecta la integridad de la información o de un sistema de procesamiento.
- Uso inapropiado de recursos: Un incidente que involucra a una persona que viola alguna política de uso de recursos.
- No disponibilidad de los recursos: Un incidente que involucra a una persona, sistema o código malicioso que impide el uso autorizado de un activo de información.
- Multicomponente: Un incidente que involucra más de una categoría anteriormente mencionada.
- Otros: Un incidente que no puede clasificarse en alguna de las categorías anteriores. Este tipo de incidentes debe monitorearse con el fin de identificar la necesidad de crear nuevas categorías.

## **Priorización De Los Incidentes Y Tiempos De Respuesta**

Con el fin de permitir una atención adecuada a los incidentes (análisis, contención y erradicación) se debe determinar el nivel de prioridad del mismo, y de esta manera atenderlos adecuadamente según la necesidad.

A manera de ejemplo se definen una serie de variables que podrán ser utilizadas para realzar la evaluación de los incidentes

> · Prioridad
> 
> 
> · Criticidad de impacto
> 
> · Impacto Actual
> 
> · Impacto Futuro
> 

**Nivel de Prioridad:** Depende del valor o importancia dentro de la entidad y del proceso que soporta el o los sistemas afectados.

| Nivel Criticidad | Valor | Definición |
| --- | --- | --- |
| Inferior | 0,10 | Sistemas no críticos, como estaciones de trabajo de usuarios con funciones no críticas. |
| Bajo | 0,25 | Sistemas que apoyan a una sola dependencia o proceso de una entidad. |
| Medio | 0,50 | Sistemas que apoyan más de una dependencias o proceso de la entidad. |
| Alto | 0,75 | Sistemas pertenecientes al área de Tecnología y estaciones de trabajo de usuarios con funciones críticas. |
| Superior | 1,00 | Sistemas Críticos. |

*Tabla 1: Niveles de Criticidad de Impacto*

- **Impacto Actual:** Depende de la cantidad de daño que ha provocado el incidente en el momento de ser detectado.
- **Impacto Futuro:** Depende de la cantidad de daño que pueda causar el incidente si no es contenido, ni erradicado.

| Nivel Impacto | Valor | Definición |
| --- | --- | --- |
| Inferior | 0,10 | Impacto leve en uno de los componentes de cualquier sistema de información o estación de trabajo. |
| Bajo | 0,25 | Impacto moderado en uno de los componentes de cualquier sistema de información o estación de trabajo. |
| Medio | 0,50 | Impacto alto en uno de los componentes de cualquier sistema de información o estación de trabajo. |

| Alto | 0,75 | Impacto moderado en uno o más componentes de más de un sistema de información. |
| --- | --- | --- |
| Superior | 1,00 | Impacto alto en uno o más componentes de más de un sistema de información. |

*Tabal 2: Niveles de Impacto Actual y Futuro*

Luego de tener definidas las variables se obtiene la *prioridad* mediante la siguiente formula:

***Nivel Prioridad = (Impacto actual * 2,5) + (Impacto futuro * 2,5) + (Criticidad del Sistema * 5)***

Y los resultados obtenidos se deben compara con la siguiente tabla para determinar la prioridad de atención:

| Nivel Prioridad | Valor |
| --- | --- |
| Inferior | 00,00 – 02,49 |
| Bajo | 02,50 – 03,74 |
| Medio | 03,75 – 04,99 |
| Alto | 05,00 – 07,49 |
| Superior | 07,50 – 10,00 |

*Tabla 3: Niveles de Prioridad del Incidente*

## **Tiempos de Respuesta**

Para el caso de la atención de incidentes de seguridad se ha establecido unos tiempos máximos de atención de los mismos, con el fin de atender adecuadamente los incidentes de acuerdo a su criticidad e impacto. Los tiempos expresados en la siguiente Tabla son un acercamiento al tiempo máximo en que el incidente debe ser atendido, y no al tiempo en el cual el incidente debe ser solucionado. Esto se debe a que la solución de los incidentes puede variar dependiendo del caso.

| Nivel Prioridad | Tiempo de Respuesta |
| --- | --- |
| Inferior | 3 horas |
| Bajo | 1 hora |
| Medio | 30 min |
| Alto | 15 min |
| Superior | 5 min |

*Tabla 4: Tiempos Máximos de Atención de Incidentes*

Cabe resaltar que cada entidad está en la libertad de definir tiempos de atención a incidentes como crean conveniente y dependiendo de la criticidad de los activos impactados.

## **Declaración y Notificación de Incidentes**

Un incidente de seguridad de la información se define como un acceso, intento de acceso, uso, divulgación, modificación o destrucción no autorizada de información; un impedimento en la operación normal de las redes, sistemas o recursos informáticos; o una violación a una Política de Seguridad de la Información de la entidad. La notificación de los incidentes permite responder a los mismos en forma sistemática, minimizar su ocurrencia, facilitar una recuperación rápida y eficiente de las actividades minimizando la pérdida de información y la interrupción de los servicios, y el proceso de tratamiento de incidentes, y manejar correctamente los aspectos legales que pudieran surgir durante este proceso.

A continuación se describe un proceso de notificación de incidentes de seguridad que podría ser adoptado por la entidad:

- Un usuario, tercero o contratista que sospeche sobre la materialización de un incidente de seguridad deberá notificarlo al primer punto de contacto definido por la entidad (Ej: Soporte de primer nivel). El incidente puede ser notificado a través de cualquier canal de comunicación (Telefónico, Correo, Aplicativo) es importante resaltar que debe existir un formato el cual el usuario que reporta el incidente debe diligenciar con la mayor cantidad posible de información relacionada con el incidente.
- El primer punto de contacto identificará el tipo de incidente (de acuerdo a la tabla de clasificación de incidentes que realiza la entidad). Analizará si el incidente reportado corresponde a un incidente de seguridad de la información o está relacionado con requerimientos propios de la infraestructura de TI. En caso de ser catalogado como un incidente de seguridad se notificarán a la persona encargada de la atención de incidentes o a quien haga sus veces para que tome las decisiones correspondientes. El primer punto de contacto será el encargado de realizar el seguimiento del Incidente hasta su cierre definitivo.
- Si el incidente de seguridad es identificado por otra línea diferente a un usuario de la entidad, a través de los elementos de detección o administradores de TI, este es notificado directamente a la persona encargada de atención de incidentes quien tomará las acciones necesarias de atención. Se notificará al primer punto de contacto sobre la presentación de un incidente de seguridad para que realice la documentación respectiva y esté atento al seguimiento y desarrollo del mismo.
- El punto de contacto clave dentro de la gestión de incidentes es la persona encargada de la atención de los mismos, el cual se encarga de coordinar y asignar las actividades con las partes interesadas. Estos últimos se encargan de solicitar el apoyo a las personas involucradas con el proceso con el fin de la correcta ejecución de actividades que den solución al incidente.
- La persona encargada de la atención de incidentes tendrá la potestad para decidir sobre las acciones que se deban ejecutar ante la presencia de un incidente de seguridad y es la persona que notificará a las altas directivas de la entidad.

## Conteción, erradicación y recupereación

Es importante para la entidad implementar una estrategia que permita tomar decisiones oportunamente para evitar la propagación del incidente y así disminuir los daños a los recursos de TI y la pérdida de la confidencialidad, integridad y disponibilidad de la información.

Esta fase se descompone claramente en tres componentes.

**Contención:** esta actividad busca la detección del incidente con el fin de que no se propague y pueda generar más daños a la información o a la arquitectura de TI, para facilitar esta tarea la entidad debe poseer una estrategia de contención previamente definida para poder tomar decisiones por ejemplo: apagar sistema, desconectar red, deshabilitar servicios.

*Ejemplos de estrategias de contención a incidentes*

| Incidente | Ejemplo | Estrategia de contención |
| --- | --- | --- |
| Acceso no autorizado | Sucesivos intentos fallidos de login | Bloqueo de cuenta |
| Código Malicioso | Infección con virus | Desconexión de la red del equipo afectado |
| Acceso no autorizado | Compromiso del Root | Apagado del sistema |
| Reconocimiento | Scanning de puertos | Incorporación de reglas de filtrado en el firewall |

La estrategia de contención varía según el tipo de incidente y los criterios deben estar bien documentados para facilitar la rápida y eficaz toma de decisiones. Algunos criterios que pueden ser tomados como base son:

> · Criterios Forenses
> 
> 
> · Daño potencial y hurto de activos
> 
> · Necesidades para la preservación de evidencia
> 
> · Disponibilidad del servicio
> 
> · Tiempo y recursos para implementar la estrategia
> 
> · Efectividad de la estrategia para contener el incidente (parcial o total)
> 
> · Duración de la solución
> 

**Erradicación y Recuperación:** Después de que el incidente ha sido contenido se debe realizar una erradicación y eliminación de cualquier rastro dejado por el incidente como código malicioso y posteriormente se procede a la recuperación a través de la restauración de los sistemas y/o servicios afectados para lo cual el administrador de TI o quien haga sus veces deben restablecer la funcionalidad de los sistemas afectados, y realizar un endurecimiento del sistema que permita prevenir incidentes similares en el futuro.

*Ejemplos de estrategias de erradicación de incidentes*

| Incidente | Ejemplo | Estrategia de erradicación |
| --- | --- | --- |
| DoS (denegación de servicio) | SYN Flood | Restitución del servicio caído |
| Virus | Gusano en la red | Corrección de efectos producidos. Restauración de backups |
| Vandalismo | Defacement a un sitio web | Reparar el sitio web |
| Intrusión | Instalación de un rootkit | Reinstalación del equipo y recuperación de datos |

*Ejemplos de estrategias de recuperación de incidentes*

| Incidente | Ejemplo | Estrategia de recuperación |
| --- | --- | --- |
| DoS (denegación de servicio) | SYN Flood | Restitución del servicio caído |
| Virus | Gusano en la red | Corrección de efectos producidos. Restauración de Backups |
| Vandalismo | Defacement a un sitio web | Reparar el sitio web |

| Intrusión | Instalación de un Rootkit | Reinstalación del equipo y recuperación de datos |
| --- | --- | --- |

En algunas ocasiones durante el proceso de Atención de Incidentes de Seguridad Informática específicamente en la fase de “Contención, Erradicación y Recuperación” se puede hacer necesario activar el BCP (Plan de Continuidad del Negocio) o el DRP (Plan de Recuperación de Desastres) en el caso que un incidente afecte gravemente a un determinado sistema.

![seguridad%20de%20redes%203%20c295661c6a5741b1a91532efe7ca8c9e/image11.png](seguridad%20de%20redes%203%20c295661c6a5741b1a91532efe7ca8c9e/image11.png)

*Integración del Proceso de Atención de Incidentes de Seguridad con el Proceso de Contingencia y Disaster Recovery.*

## **Actividades post-incidentes**

Las actividades Post-Incidente básicamente se componen del reporte apropiado del Incidente, de la generación de lecciones aprendidas, del establecimiento de medidas tecnológicas, disciplinarias y penales de ser necesarias así como el registro en la base de conocimiento para alimentar los indicadores.

**Lecciones Aprendidas:**

Una de las partes más importantes de un plan de respuesta a incidentes de TI es la de aprender y mejorar. Cada equipo de respuesta a incidentes debe evolucionar para reflejar las nuevas amenazas, la mejora de la tecnología, y las lecciones aprendidas. Mantener un proceso de "lecciones aprendidas" después de un incidente grave, y periódicamente después de los incidentes menores, es sumamente útil en la mejora de las medidas de seguridad y el proceso de gestión de incidentes

Mantener un adecuado registro de lecciones aprendidas permite conocer:

> · Exactamente lo que sucedió, en qué momento y cómo el personal gestionó el incidente.
> 
> 
> · Los procedimientos documentados.
> 
> · Si se tomaron las medidas o acciones que podrían haber impedido la recuperación.
> 
> · Cuál sería la gestión de personal y que debería hacerse la próxima vez que ocurra un incidente similar.
> 
> · Acciones correctivas pueden prevenir incidentes similares en el futuro.
> 
> · Cuales herramientas o recursos adicionales son necesarios para detectar, analizar y mitigar los incidentes en el futuro.
> 

El proceso de lecciones aprendidas puede poner de manifiesto la falta de un paso o una inexactitud en un procedimiento y son un punto de partida para el cambio, y es precisamente debido a la naturaleza cambiante de la tecnología de la información y los cambios en el personal, que el equipo de respuesta a incidentes debe revisar toda la documentación y los procedimientos para el manejo de incidentes en determinados intervalos.

## Roles y perfiles necesarios para la atención de incidentes

A continuación presentaremos una descripción de los actores que intervienen y conforman el proceso de atención de Incidentes, para cada actor se presentará una breve descripción sobre su perfil y la función dentro del proceso de respuesta a Incidentes de Seguridad de la información.

- **Usuario Sensibilizado:** Es un empleado, empleados de firmas contratista o terceros con acceso a la infraestructura de la entidad, quien debe estar educado y concientizado sobre las guías implementadas sobre la seguridad de la información y en particular la guía de atención de incidentes, estos usuarios serán muchas veces quienes reporten los problemas y deberán tener en cuenta lo siguiente:
- **Agente Primer Punto de Contacto**: Es el encargado de recibir las solicitudes por parte de los usuarios sobre posibles incidentes también debe registrarlos en la base de conocimiento y debe ser el encargado de escalarlos a la persona encargada de la atención de incidentes. Este Agente debe contar adicionalmente con capacitación en Seguridad de la Información (con un componente tecnológico fuerte) y debe conocer perfectamente la clasificación de Incidentes y los procesos de escalamiento de Incidentes. Adicionalmente debe contar con una capacitación básica en técnicas forenses, específicamente en recolección y manejo de evidencia, lo cual involucra fundamentalmente dos aspectos.

> · Admisibilidad de la evidencia: si la evidencia se puede utilizar o no en una corte
> 
> 
> · Peso de la evidencia: la calidad y cabalidad de la evidencia.
> 

Este no es un actor que realiza la centralización de los incidentes reportados por los usuarios, da un tratamiento inicial y escala el incidente para que sea tratado.

- **Administrador del Sistema:** se define como la persona encargada para configurar y mantener un activo informático. También debe ser notificado por el agente de primer punto de contacto sobre un incidente de seguridad con el fin de analizar, identificar, contener y erradicar un incidente de seguridad. Este debe documentar y notificar al agente de primer punto de contacto sobre el incidente la solución del mismo. Se recomienda que los administradores cuenten con capacitación en Seguridad de la Información (con un componente tecnológico fuerte no solo en su plataforma si no en Redes y erradicación de vulnerabilidades) y debe conocer perfectamente la clasificación de Incidentes y los procesos de escalamiento de Incidentes. Adicionalmente debe contar con una capacitación en técnicas forenses, específicamente en recolección y manejo de evidencia.
- **Administrador de los sistemas de Seguridad:** Personas encargadas de configurar y mantener un activo informático relacionado con la seguridad de la plataforma ej. Firewall, Sistemas de Prevención de Intrusos, Routers, Sistemas de Gestión y Monitoreo. También debe ser notificado por el agente de primero contacto sobre un incidente de seguridad con el fin de analizar, identificar, contener y erradicar un incidente de seguridad. Este debe documentar y notificar al agente de primer contacto sobre el incidente y la solución del mismo. Se recomienda que los administradores de esta tecnología sean expertos en Seguridad de la Información (con un componente tecnológico fuerte en Redes y erradicación de vulnerabilidades, Ethical Hacking y técnicas forenses) y debe conocer perfectamente la clasificación de Incidentes de la entidad.
- **Analista Forense:** Es un experto en el tema forense, quien debe estar disponible en caso de que un incidente de impacto alto (o uno que amerite acciones disciplinarias o legales o investigación profunda) requiera una investigación completa para solucionarlo y determinar los siguientes Ítems
    
    > · Que sucedió.
    > 
    > 
    > · Donde sucedió.
    > 
    > · Cuando Sucedió.
    > 
    > · Quien fue el Responsable.
    > 
    > · Como sucedió.
    > 

Este actor debe ser un apoyo para los demás actores en caso de dudas sobre los procedimientos y debe ejercer un liderazgo técnico en el proceso de atención de Incidentes de seguridad de la información.

- **Líder del Grupo de Atención de Incidentes:** Responde a las consultas sobre los incidentes de seguridad que impacten de forma inmediata, y es el encargado de revisar y evaluar los indicadores de gestión correspondientes a la atención de incidentes de seguridad para poder ser presentados a los directivos. El Líder Grupo de Atención de Incidentes estará en la capacidad de convocar la participación de otros funcionarios de la organización cuando el incidente lo amerita (Prensa y Comunicaciones, Gestión de Talento Humano, Gestión Jurídica, Tecnología, Representante de las Directivas para el SGSI).
    
    También debe estar al tanto del cumplimiento de los perfiles mencionados y de revisar el cumplimiento de los procedimientos y mejores prácticas, así como también de los indicadores de gestión, y en capacidad de disparar si lo amerita planes de contingencia y/o continuidad.
    
    <aside>
    📖 Finalmente el Líder del Grupo de Atención de Incidentes será el responsable del modelo de Gestión de incidentes y debe estar en la capacidad de revisar todos los incidentes de seguridad y los aspectos contractuales que manejan el outsourcing del servicio help desk.
    
    </aside>
    

## **Proceso y técnicas de gestión de incidentes de seguridad**

Los incidentes en la seguridad de la información parecen inevitables hoy en día por lo que no tenemos más remedio que plantearlos como vamos a gestionar dichos incidentes de la manera más ágil y eficiente para la organización

Es por ello que la norma **[ISO 27001](https://normaiso27001.es/)** dedica un capítulo a establecer controles para gestionar los incidentes en la seguridad de la información e inclusive se ha dedicado un documento específico con los principios para gestionar incidentes en la seguridad de la información

### Objetivo 1: Gestión de incidentes y mejoras de seguridad de la información

Garantizar un enfoque consistente y eficaz para la gestión de incidentes de seguridad de la información, incluyendo la comunicación de eventos de seguridad y debilidades.

Como hemos mencionado, un análisis de riesgos no puede concluir con la eliminación total de las vulnerabilidades pues esto aún ni siquiera seria práctico o viable por lo que las vulnerabilidades residuales siempre existen por lo que tendremos de seguro incidentes en la seguridad de la información además de que puedan surgir amenazas o y vulnerabilidades no identificadas hasta ahora.

Es por ello que debemos implementar una herramienta para la gestión de los incidentes de la seguridad de la información con los siguientes objetivos generales

- **Detectar**, informar y evaluar incidentes de la Seguridad de la información
- **Responder** a incidentes
- **Reportar** vulnerabilidades
- **Aprender** de los incidentes de la Seguridad de la información

## Los pasos para la resolución de incidentes

La gestión de incidentes de seguridad se basa en diferentes pasos, que incluyen:

![seguridad%20de%20redes%203%20c295661c6a5741b1a91532efe7ca8c9e/image12.jpg](seguridad%20de%20redes%203%20c295661c6a5741b1a91532efe7ca8c9e/image12.jpg)

*NOTA: Estos pasos podrían ser estados diferentes que un incidente por lo que también es importante informar al usuario sobre cualquier cambio en el estado del incidente.*

- **1. Notificación del incidente:** una persona detecta un evento que puede dañar el funcionamiento de la organización, por lo que necesita comunicar el incidente de acuerdo con los procedimientos de comunicación de la organización (generalmente un correo electrónico, una llamada telefónica, una herramienta de software, etc.)
- **2. Clasificación del incidente:** una persona recibe la notificación del incidente y, según los diversos parámetros, se clasifica. La persona que detecta el incidente también puede hacer una clasificación, pero es un experto técnico que lo clasifica de la manera adecuada.
- **3. Tratamiento del incidente:** una vez que se clasifica el incidente y se conoce la gravedad y el tiempo acordado para su resolución, un experto técnico debe decidir sobre las medidas necesarias para resolverlo.
- **4. Cierre el incidente:** una vez que se resuelve el incidente, se registra toda la información generada durante el tratamiento y, finalmente, se notifica a la persona que envió primero la notificación del incidente que se cerró.
- **5. Base de conocimiento:** toda la información generada durante el tratamiento del incidente es crítica para posibles incidentes similares en el futuro, así como para recopilar evidencia. Imagine que un usuario actualiza un sistema y luego de esto, el sistema se cierra (involuntariamente). Luego, el usuario abre un incidente y el incidente se resuelve y se cierra. La información generada para resolver el incidente se registra, por lo que si el problema vuelve a ocurrir en el futuro, simplemente pueden referirse a la base de conocimiento; Tendrán la solución perfecta sin perder tiempo.

<aside>
👉 En este sentido la norma establece una serie de controles empezando por la organización que debemos llevar a cabo para acometer esta tarea

</aside>

## **Controles para la gestión de incidetes de la seguridad de la información**

### Responsables y procedimientos

En primer lugar deberemos tener implantado y documentado los procedimientos que nos dirijan en el proceso de gestión de incidentes de la seguridad de la información.

Estos procesos deben tener en cuenta:

- **Las responsabilidades**
    - Defina un responsable o responsables para la gestión de incidentes quien deberá garantizar que se desarrollan los procedimientos adecuados para que se realicen todas las tareas o procesos necesarios para gestionar los incidentes
    - Defina las responsabilidades de cada empleado tanto en la colaboración para la respuesta, como en la necesidad de comunicación de los incidentes de seguridad de la información
- **Los procesos o procedimientos**
    - Que existan procedimientos para la detección, análisis y elaboración de informes de incidentes de la seguridad de la información
    - Elabore procedimientos para que se comuniquen los incidente
    - Que dichos procedimientos sean conocidos (Que cada empleado conozca los procedimientos de comunicación de incidentes y sus responsabilidades)
    - Que existan vías de comunicación adecuadas (asegúrese de que se definen los puntos de recogida de información para los incidentes y eventos de la seguridad de la información)
- **Capacitación**
    - Asegúrese de la competencia del personal de atención y resolución de incidentes. Mantenga un plan de capacitación de las personas que se ocupan de los incidentes de la seguridad de la información

## Reportes de eventos de seguridad de la información

Este control nos pide que establezcamos los canales de comunicación para todos los eventos o incidentes. Estos canales, naturalmente deben estar establecidos con los responsables de la gestión de los incidentes.

Es importante que todos los usuarios estén informados y familiarizados con los mecanismos de notificación. Con usuarios nos referimos a usuarios tanto internos como externos

Antes que nada vamos a distinguir entre dos conceptos más o menos similares pero que debemos separar para un correcto análisis de los incidentes en la Seguridad de la Información

### Evento de la seguridad de la información

Cualquier ocurrencia identificada en un sistema de información, servicio o estado de la red que indica una posible infracción en la seguridad de la información, en la política o fallo en los controles, o una situación previamente desconocida que puede ser relevante para la seguridad

### Incidente de la seguridad de la información

Cuando el evento se puede clasificar como no deseado o inesperado dentro de los eventos de seguridad de la información y además tienen una probabilidad significativa de comprometer las operaciones comerciales y suponen una seria amenaza para la seguridad de la información

Un evento en la seguridad de la información no significa necesariamente una implicación en la confidencialidad, integridad o disponibilidad a veces incluso lo deseamos, podemos aprender de ello y endurecer la seguridad

- El incidente siempre es indeseado

### Aclarando conceptos: amenaza, vulnerabilidad, evento e incidente

![seguridad%20de%20redes%203%20c295661c6a5741b1a91532efe7ca8c9e/image13.jpg](seguridad%20de%20redes%203%20c295661c6a5741b1a91532efe7ca8c9e/image13.jpg)

## **Amenaza para la Seguridad de la información**

> *Una amenaza se refiere a cualquier cosa que tenga el potencial de causar daños graves a un sistema o activo de información. Una amenaza es algo que puede suceder o no, pero tiene el potencial de causar un daño grave.*
> 

*Las amenazas pueden provocar ataques a sistemas informáticos, redes y más.*

### **Vulnerabilidad en la Seguridad de la información**

*Se refiere a una debilidad o defecto en un sistema o activo de información que puede dejarlo expuesto a una amenaza o ataque. Una vulnerabilidad también puede referirse a cualquier tipo de debilidad en un sistema de información en sí mismo, en un conjunto de procedimientos o en cualquier cosa que deje la seguridad de la información expuesta a una amenaza.*

### **Evento en la Seguridad de la información**

*Un evento de seguridad de la información es un cambio en las operaciones diarias de una red o servicio de tecnología de la información que indica que una política de seguridad puede haber sido violada o una protección de seguridad puede haber fallado.*

### **Incidente en la Seguridad de la información**

*Una sola o una serie de eventos de seguridad de la información no deseados o inesperados que tienen una probabilidad significativa de comprometer las operaciones comerciales y amenazar seguridad de información. Por ejemplo un comportamiento anómalo en un sistema es un evento, sin embargo, si se encuentra evidencia del virus en el sistema, se puede considerar un incidente de seguridad.*

### Reporte de debilidades de seguridad de la información

El reporte de incidentes debe acompañarse con un reporte de posibles debilidades del sistema que se detecten en cualquier momento. Esto debe estar soportado por:

- La comunicación a los usuarios de la exigencia de observar y reportar cualquier debilidad de seguridad de la información vista o sospechada en sistemas o servicios

<aside>
💡 Se aconseja advertir que los usuarios que probar la fortaleza o debilidad de los sistemas a ver si encuentran una vulnerabilidad serán considerados por la compañía como un mal uso del sistema

</aside>

### Evaluación y decisión sobre los eventos de seguridd de información

Como ya hemos visto en los puntos anteriores, los eventos de la seguridad de la información pueden clasificarse en simples eventos o pueden pasar a ser Indecentes de la seguridad de la información

Para ello establece:

- Un criterio de priorización de incidentes dependiendo del sistema o servicio afectado, del usuario etc.
- La evaluación de incidentes debe ser realizada tanto por el usuario como por el equipo de gestión que debe revisar la prioridad.
- Lleve un registro de la evaluación de los incidentes para poder analizar los parámetros de calidad tanto en su resolución como de su clasificación.

Hay muchas formas de clasificar incidentes, pero lo habitual es considerar dos parámetros:

- **Impacto:** Daño causado al negocio (en términos económicos, imagen, etc.)
- **Urgencia:** La rapidez con la cual la organización necesita corregir el incidente

La combinación de estos parámetros nos permitirá determinar la prioridad de cada incidente, por lo que de esta manera puede establecer, por ejemplo, la siguiente tabla de valores:

![seguridad%20de%20redes%203%20c295661c6a5741b1a91532efe7ca8c9e/image14.jpg](seguridad%20de%20redes%203%20c295661c6a5741b1a91532efe7ca8c9e/image14.jpg)

Así podríamos clasificar las incidencias en:

- **NIVEL CRÍTICO (5 a 6)**__
- **NIVEL GRAVE (4)**__
- **NIVEL LEVE (1 a 2)**__

### Respuesta a incidentes de seguridad

Se trata de controlar el proceso de resolución de incidentes en la seguridad de la información.

Los controles a establecer serian.

- Evalue si la organización tiene la capacidad para resolver el incidente por si misma o necesita ayuda de terceros.
- Mantenga un registro con las evidencias de las incidencias
- Establezca el sistema de comunicaciones necesarias entre usuarios y el equipo de gestión de incidencias o quien deba estar informado de las actuaciones y situación del proceso de resolución de las incidencias
- Registre las acciones llevadas a cabo y los resultados de las mismas
- Cierre la incidencia formalmente cuando se haya resuelto
- Realice un análisis para determinar las causas de cada incidente

### Aprendiendo de los incidentes de seguridad de la información

Como ya hemos adelantado los incidentes no solo son un problema a solucionar sino una fuente de información para la resolución de futuros incidentes o para la mejora de la seguridad de la información

Los controles de la norma para mantener una base de conocimientos sobre los incidentes en la seguridad de la información son:

- Creación de un registro que considere
- Volumen de incidentes producidos
- Tipología de incidentes producidos
- Coste de la resolución de la incidencia
- Impacto de la incidencia
- Solución aplicada

La información sobre los incidentes nos puede ayudar a:

- Identificar los incidentes más recurrentes y de alto impacto
- Mejorar nuestro sistema de gestión con nuevos controles y criterios para la evaluación de riesgos
- Realizar entrenamientos a los usuarios para evitar incidentes y a los gestores de incidentes para mejorar la resolución de los mismos

<aside>
👉 Para este último punto se recomienda utilizar datos No reales para los entrenamientos.

</aside>

### Recolección de evidencia

Los incidentes sobre la seguridad de la información pueden requerir acciones posteriores como sanciones o acciones legales. Recuperar las evidencias para utilizarlas posteriormente puede volverse un dolor de cabeza si no hemos previsto algún mecanismo para guardarlas.

En este capítulo la norma nos pone como control el que conservemos la información sobre las incidencias de forma que podamos recuperar:

- Los inicios y cierres de sesión
- Las identificaciones
- El estado de los dispositivos y de las redes
- Las evidencias de reuniones informativas, documentación sobre responsabilidades y funciones de seguridad del personal

***No debe pasar por alto…***

*En ocasiones puede ser necesaria una investigación forense de las evidencias informáticas. Conviene tener en cuenta mantener a salvo los derechos de acceso a la información para poder realizar una investigación forense.*

*Para ello hay que tener en cuenta los distintos requisitos de las jurisdicciones pertinentes y estar preparados mediante la comunicación previa al personal o la firma de cláusulas contractuales*

- **Otro tema es la preservación de las evidencias…**

*Los incidentes no sabemos normalmente en que van a terminar y si requerirán posteriores acciones legales o disciplinarias Determinadas incidencias pueden conllevar el borrado de las evidencias con el objeto de ocultar al responsable de las mismas, es por ello que se recomienda establecer sistemas de copiado y preservación de registros con tal de que ciertas evidencias no se puedan eliminar tan fácilmente.*

- **Seguridad de las evidencias…**

*Finalmente si es posible o se identifica como necesario se pueden certificar los sistemas de recogida de evidencias o mantener medios de vigilancia y control independientes (homologados y legales) para fortalecer las evidencias de cara a acciones legales*

## **Herramientas de gestión de incidentes de seguridad**

Nos gustaría destacar que la gestión de incidencias no se hace sólo con una herramienta, sino con la selección correcta de herramientas, las mejores prácticas y el equipo de DevOps. Vamos a hablar de nuestras herramientas de gestión de incidencias favoritas que creemos que marcan la diferencia en el proceso de gestión de incidencias:

- [BigPanda](https://www.bigpanda.io/)
- [OnPage](https://www.onpage.com/)
- [NinjaRMM](https://www.ninjarmm.com/)
- [Rundeck](https://www.rundeck.com/open-source)
- [ServiceNow](https://www.servicenow.com/)
- [Issuetrak](https://www.issuetrak.com/)
- [AlertOps](https://alertops.com/)
- [Atlassian](https://www.atlassian.com/software/jira/service-management/features/service-desk)

Hay otras herramientas estupendas que ayudan a realizar el seguimiento de los incidentes, que cada incidente puede ser rastreado y documentado para poder identificar tendencias y hacer comparaciones a lo largo del tiempo. Hay algunas salas de chat que permiten la comunicación de texto en tiempo real para diagnosticar y resolver el incidente como un equipo y proporcionar un rico conjunto de datos para el análisis de la respuesta más tarde. Además, el chat de vídeo complementa el chat de texto para muchos incidentes, el chat de vídeo en equipo puede ayudar a discutir los hallazgos y trazar una estrategia de respuesta. El sistema de alertas, que es extremadamente importante, se integra con su sistema de supervisión y gestiona las rotaciones de guardia y las escaladas. Las herramientas de documentación, como Confluence, pueden capturar los documentos del estado de los incidentes y los postmortem.

## Tendencias actuales en seguridad en redes

- **Permanece el riesgo asociado al teletrabajo.** El regreso a la oficina en 2022 va a ser más lento de lo inicialmente previsto. Es más, gran parte del teletrabajo generado durante la crisis sanitaria permanecerá, y se consolidarán los entornos laborales híbridos. Esto va a hacer que todo lo relacionado con la *ciberseguridad de ubicaciones remotas* continuará teniendo protagonismo. Las organizaciones están terminando de definir y fijar sus estrategias y políticas de seguridad para estos nuevos entornos híbridos, de manera que la postura de seguridad sea la misma en todos los entornos de red de la organización, independientemente de dónde se encuentren.
- **DNS sobre HTTPS (DoH) como vector de amenazas.** El creciente uso de servicios DoH está en aumento por parte de las organizaciones, y los cibercriminales van a tratar de explotar este sistema como vector de ataque, ya que proporciona un canal encriptado hacia el servidor DoH y los desarrolladores de malware son conscientes de que es un medio para eludir los controles de seguridad. Muchos proveedores de servicios y empresas están implementando DoH como una estrategia defensiva, con el objetivo de tener su propia infraestructura DNS y evitar depender de servidores DoH de terceros, pero esto puede suponer un riesgo.
- **Estrategias Zero Trust.** La proliferación de entornos de trabajo híbridos y distribuidos y de entornos de red IoT incrementará en 2022 la adopción de estrategias de seguridad *“Zero Trust”*. Una estrategia “Zero Trust” consiste en la creación de “listas blancas” de dispositivos a los que se les concede acceso a red y a los recursos de TI, una vez que han sido inventariados y securizados de acuerdo con las políticas de seguridad corporativas. Esta estrategia evitará que dispositivos IoT o dispositivos personales de teletrabajadores sean utilizados como vectores de ataque sobre DNS. En estas estrategias jugarán un papel fundamental las *soluciones de seguridad DNS* inteligentes que permitan realizar filtrado estricto de dispositivos en base a estas listas blancas. Cualquier solicitud de DNS sólo será resuelta si se hace contra un dominio reconocido y autorizado, todas las demás serán denegadas.
- **Phising y exflitración de datos.** El phising seguirá siendo, junto con el ransomware, una de las principales amenazas que hacen crecer los costes de las brechas de seguridad para las empresas. La exfiltración de datos se produce ya sea por intrusiones en red, por la pérdida de dispositivos corporativos con información sensible o mediante herramientas de malware.
    
    Según un informe de IDC un 26% de las empresas encuestadas manifestaron haber sufrido brechas de seguridad con exfiltración de datos como resultado de ataques vía DNS. En 2024, las empresas utilizarán cada vez más *DNS como primera línea de defensa*, para monitorizar el tráfico IP e identificar y prevenir el robo de datos.
    
- **Ransomware como Servicio (RaaS).** El Ransomware ha crecido durante los dos últimos años de manera exponencial, y ya en 2023 se ha experimentado un crecimiento en el denominado *Ransomware como Servicio (RaaS)*.Ambas modalidades seguirán siendo protagonistas en 2024 Como en otras áreas, los ciberdelincuentes también están utilizando los nuevos modelos de entrega de servicios de TI disponibles en el mercado. Muchas organizaciones criminales carecen de las habilidades para crear su propio ransomware y contratan este servicio en la red. La utilización de ataques RaaS con objetivos muy precisos está siendo lucrativo para los ciberdelincuentes. No son ataques masivos, sino que se utiliza ingeniería social para elaborar vectores de ataque de apariencia legítima, como correos electrónicos bien elaborados. En otros casos, los actores de amenazas pueden apuntar a vulnerabilidades específicas de un grupo de víctimas objetivo.

## **Retos y oportunidades para la seguridad en redes**

La seguridad de las redes es el área de la ciberseguridad que se centra en la protección de las redes informáticas frente a las ciberamenazas. Tiene tres objetivos principales: impedir el acceso no autorizado a los recursos de la red, detectar y neutralizar los ciberataques y las violaciones de la seguridad en curso, y garantizar que los usuarios autorizados tengan un acceso seguro a los recursos de la red que necesitan, cuando los necesitan.

El riesgo de ciberataque aumenta al tiempo que crece el tamaño y la complejidad de las redes. Por ejemplo, según el informe Coste de una violación de datos de 2022 de IBM, el 83% de las organizaciones encuestadas han sufrido más de una violación de datos, es decir, una brecha de seguridad que ha dado lugar a un acceso no autorizado a información sensible o confidencial. Estos ataques son extremadamente costosos: el coste medio de una violación de datos en todo el mundo es de 4,35 millones de dólares, cifra que se duplica con creces en Estados Unidos (9,44 millones de dólares).

La seguridad de la red protege la integridad de la infraestructura, los recursos y el tráfico de la red para frustrar estos ataques y minimizar sus repercusiones financieras y operativas.

### **Tipos de tecnologías de seguridad de la red**

Los sistemas de seguridad de la red operan en el perímetro y dentro de la red.

En el perímetro, los controles de seguridad intentan impedir que las ciberamenazas entren en la red. Pero los atacantes a veces consiguen infiltrarse, razón por la cual los equipos de seguridad de redes también implantan controles en torno a los recursos dentro de la red, como ordenadores portátiles y datos. Incluso si los atacantes consiguen infiltrarse en la red, no tendrán vía libre. Esta estrategia, que consiste en colocar una serie de dispositivos de control entre los hackers y las posibles vulnerabilidades, se conoce como "defensa en profundidad".

Cada reto contrae una oportunidad de mejora y hay mucho sobre lo que trabajar ya que en este 2024 se espera, como cada año, un aumento en la actividad de los ciber criminales y mayor sofisticación tanto en técnicas como en herramientas. Puntualicemos los casos fundamentales a tener en cuenta sobre lo que más debemos prestar atención. El establecimiento de sistemas de seguridad de red implica la combinación de las siguientes herramientas:

### **Cortafuegos**

Un cortafuegos es un software o hardware que impide que el tráfico sospechoso entre o salga de una red, al tiempo que permite el paso del tráfico legítimo. Los cortafuegos pueden instalarse en el extremo de una red o utilizarse internamente para dividir redes más grandes en subredes más pequeñas. De este modo, si una parte se ve comprometida, los piratas informáticos no pueden acceder al resto de la red.

Existen diferentes tipos de cortafuegos con diferentes características. Los cortafuegos básicos utilizan el filtrado de paquetes para inspeccionar el tráfico. Los sistemas de nueva generación, más avanzados, ofrecen una protección mejorada con prevención de intrusiones, IA y aprendizaje automático, vigilancia y control de aplicaciones, además de alimentación de inteligencia sobre amenazas.

### **Control de acceso a la red (NAC)**

Las soluciones de control de acceso a la red (NAC) actúan como guardianes, autenticando y autorizando a los usuarios para determinar quién está autorizado a acceder a la red y qué puede hacer en ella. La "autenticación" consiste en comprobar que un usuario es quien dice ser. La parte de "autorización" consiste en conceder a los usuarios autenticados autorización para acceder a los recursos de la red.

Las soluciones NAC se utilizan a menudo para aplicar políticas de control de acceso basado en funciones (RBAC), que exigen que los privilegios de los usuarios reflejen sus funciones. Por ejemplo, los desarrolladores junior pueden ver y editar código, pero no ponerlo en producción. Los desarrolladores senior, en cambio, están autorizados a leer, escribir y poner código en producción. El sistema RBAC ayuda a evitar la violación de datos al mantener a los usuarios no autorizados alejados de los recursos a los que no tienen derecho de acceso.

Además de autenticar a los usuarios, algunas soluciones NAC pueden evaluar los riesgos en los terminales de los usuarios. El objetivo es impedir que los dispositivos no seguros o comprometidos accedan a la red. Si un usuario intenta acceder a la red en un dispositivo equipado con un software antimalware obsoleto o mal configurado, el sistema denegará el acceso. Algunas herramientas NAC avanzadas son incluso capaces de resolver automáticamente los problemas de no conformidad de los terminales.

### **Sistemas de detección y prevención de intrusiones (IDPS)**

Un sistema de detección y prevención de intrusiones (IDPS), a veces denominado simplemente sistema de prevención de intrusiones (IPS), puede desplegarse directamente detrás de un cortafuegos para analizar el tráfico entrante en busca de amenazas a la seguridad. Estas herramientas derivan de los sistemas de detección de intrusos (IDS), que se limitaban a señalar las actividades sospechosas para su examen. Los sistemas IDPS son ahora capaces de reaccionar automáticamente ante posibles infracciones, por ejemplo bloqueando el tráfico o restableciendo la conexión. Son especialmente eficaces para detectar y bloquear ataques de fuerza bruta, denegación de servicio (DoS) y denegación de servicio distribuida (DDoS).

### **Redes privadas virtuales (VPN)**

Una red privada virtual (o VPN del inglés "virtual private network") se utiliza para proteger la identidad de un usuario cifrando sus datos y enmascarando su dirección IP y su ubicación. Cuando alguien utiliza una VPN, ya no se conecta directamente a Internet, sino a un servidor seguro que se conecta a Internet en su nombre.

Las VPN permiten a los teletrabajadores acceder a las redes corporativas con total seguridad, incluso a través de conexiones wifi públicas no seguras, como las que se encuentran en cafeterías y aeropuertos. Las VPN cifran el tráfico de los usuarios, protegiéndolo de los hackers que quieran interceptar sus comunicaciones.

En lugar de VPN, algunas organizaciones utilizan el modelo Zero Trust Network Access (o ZTNA del inglés "acceso a red de confianza cero").En lugar de utilizar un servidor proxy, ZTNA conecta a los usuarios remotos de forma segura utilizando políticas de control de acceso zero trust. Cuando los usuarios remotos se conectan a una red a través de ZTNA, no obtienen acceso a toda la red. Solo tienen acceso a los recursos que están autorizados a utilizar, y deben ser controlados cada vez que acceden a un nuevo recurso.

### **Seguridad de aplicaciones**

La seguridad de las aplicaciones se refiere a las medidas adoptadas para proteger las aplicaciones y las interfaces de programación de aplicaciones (API) de los atacantes. En la actualidad, muchas empresas utilizan aplicaciones para llevar a cabo funciones empresariales esenciales o procesar datos confidenciales, por lo que los ciberdelincuentes suelen atacar las aplicaciones. Y como muchas aplicaciones empresariales están alojadas en nubes públicas, los piratas informáticos pueden aprovechar sus vulnerabilidades para entrar en las redes privadas de las empresas.

Las medidas de seguridad de las aplicaciones las protegen de los agentes maliciosos. Las herramientas más habituales son los cortafuegos de aplicaciones web (WAF), la autoprotección de aplicaciones en tiempo de ejecución (RASP) y las pruebas de seguridad estática y dinámica de aplicaciones (SAST y DAST).

### **Seguridad del correo electrónico**

El índice X-Force Threat Intelligence de IBM Security muestra que el phishing es el vector inicial de ciberataque más común. Las herramientas de seguridad del correo electrónico pueden ayudar a frustrar los ataques de phishing y otros intentos de poner en peligro el correo electrónico de los usuarios. La mayoría de los servicios de correo electrónico incluyen herramientas de seguridad, como filtros antispam y cifrado de mensajes. Algunas herramientas están equipadas con sandboxes, es decir, entornos aislados en los que los equipos de seguridad pueden inspeccionar los archivos adjuntos al correo electrónico en busca de malware sin exponer la red.

### **Tecnologías de seguridad asociadas**

Aunque las siguientes herramientas no son estrictamente herramientas de seguridad de red, los administradores las utilizan a menudo para proteger zonas y activos de la red.

La prevención de la pérdida de datos (DLP) se refiere a las estrategias y herramientas de seguridad de informática que impiden el robo o la filtración accidental de datos sensibles. Este enfoque aúna políticas de seguridad y tecnologías especializadas que rastrean los flujos de datos, cifran la información sensible y activan alertas si se detectan actividades sospechosa.

Las soluciones de seguridad para puntos finales protegen todos los dispositivos que se conectan a una red (portátiles, ordenadores de sobremesa, servidores, dispositivos móviles, dispositivos IoT) de los hackers que intentan utilizarlos para infiltrarse en la red. El software antivirus puede detectar y destruir troyanos, spyware y otros programas maliciosos en un dispositivo antes de que se propaguen al resto de la red. Las soluciones de detección y respuesta de puntos finales (EDR) son herramientas más avanzadas que supervisan el comportamiento de los puntos finales y reaccionan automáticamente ante los eventos que amenazan la seguridad. El software de gestión unificada de puntos finales (UEM) permite a las organizaciones supervisar, gestionar y proteger todos los dispositivos de los usuarios finales desde una única consola.

Las soluciones de seguridad web, como las pasarelas web seguras, bloquean el tráfico de Internet malicioso e impiden que los usuarios se conecten a sitios y aplicaciones sospechosos.

La segmentación de redes es una forma de dividir grandes redes en subredes más pequeñas, ya sea físicamente o mediante software. Esta técnica limita la propagación de ransomware y otros programas maliciosos aislando una subred comprometida del resto de la red. También tiene la ventaja de mantener a los usuarios legítimos alejados de recursos a los que no deberían tener acceso.

Las soluciones de seguridad en la nube protegen los centros de datos, las aplicaciones y otros activos de la nube contra los ciberataques. En la mayoría de los casos, se trata simplemente de medidas de seguridad de red estándar (cortafuegos, NAC y VPN) aplicadas a entornos en nube. Muchos proveedores de servicios en la nube incorporan controles de seguridad en sus servicios o los ofrecen como complementos.

El análisis del comportamiento de usuarios y entidades (UEBA) utiliza el análisis del comportamiento y el aprendizaje automático para detectar actividades anómalas de usuarios y dispositivos. UEBA se utiliza para detectar amenazas internas y piratas informáticos que se han apoderado de cuentas de usuario.

### **Un enfoque zero trust para la seguridad de la red**

En el pasado, las redes corporativas estaban centralizadas, con terminales, datos y aplicaciones clave ubicados en las instalaciones de la empresa. Los sistemas de seguridad de aquella época se centraban en impedir que las amenazas atravesaran el perímetro de la red. Una vez que un usuario estaba dentro, se le consideraba de confianza y tenía un acceso prácticamente ilimitado.

Sin embargo, a medida que las organizaciones se digitalizan y adoptan entornos de nube híbrida, las redes se descentralizan cada vez más. Los recursos de red pueden encontrarse ahora en la nube (centro de datos), en dispositivos locales y remotos, así como en dispositivos móviles e IoT.

Los controles de seguridad a nivel perimetral son menos eficaces para las redes distribuidas, razón por la cual muchos equipos de seguridad informática están recurriendo al zero trust. Este tipo de seguridad coloca controles alrededor de cada recurso y no en el perímetro. La confianza depositada en los usuarios nunca es implícita. Cada vez que alguien intenta acceder a un recurso, debe ser autenticado y autorizado, aunque ya se encuentre en la red corporativa. A los usuarios autentificados sólo se les concede el acceso menos privilegiado, y sus autorizaciones se revocan en cuanto finaliza la tarea.

La seguridad de red zero trust se basa en políticas de acceso precisas, validación continua y datos recogidos de tantas fuentes como sea posible (incluidas la mayoría de las herramientas descritas anteriormente) para garantizar que sólo los usuarios adecuados puedan acceder a los recursos adecuados, por las razones adecuadas y en el momento adecuado.

## Soluciones de seguridad para redes empresariales

Aunque un enfoque de defensa en profundidad puede proteger la red de una empresa, también requiere que el equipo de seguridad informática gestione una serie de controles independientes. Las plataformas de seguridad de redes empresariales pueden ayudar a agilizar la gestión integrando herramientas dispares y permitiendo a los equipos supervisar toda la red desde una única consola. Las plataformas de seguridad de red más comunes son:

Las soluciones de gestión de eventos e información de seguridad (SIEM) recopilan información de las herramientas de seguridad internas, la cotejan en un registro central e informan de las anomalías. Las soluciones de orquestación, automatización y respuesta en materia de seguridad (SOAR) recopilan y analizan datos de seguridad, lo que permite a los equipos de especialistas definir y ejecutar medidas automatizadas en caso de ciberamenazas. Las herramientas de detección y respuesta de red (NDR) utilizan IA y aprendizaje automático para supervisar el tráfico de red y detectar actividades sospechosas.

Las soluciones de detección y respuesta extendidas (XDR) son una arquitectura de ciberseguridad abierta que integra herramientas y operaciones de seguridad para todas las capas: puntos finales, correo electrónico, aplicaciones, redes, cargas de trabajo en la nube y datos. Con XDR, las soluciones de seguridad que no están necesariamente diseñadas para trabajar juntas pueden interoperar sin problemas en la prevención, detección, investigación y respuesta ante amenazas. XDR también puede automatizar la detección de amenazas, la clasificación de incidentes y los flujos de trabajo de búsqueda de amenazas.