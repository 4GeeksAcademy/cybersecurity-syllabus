---
title: "Seguridad en la red"
subtitle: "Explora los aspectos críticos de la seguridad de la red, incluida la autenticación, el control de acceso, la gestión de amenazas y la protección de datos."
tags: ["ciberseguridad"]
authors: ["blindma1den", "lorenagubaira"]

---

La seguridad en la red es un aspecto crítico de la ciberseguridad que se centra en la protección de la infraestructura de comunicaciones y la información que fluye a través de ella. Implica una serie de medidas y prácticas diseñadas para garantizar la confidencialidad, la integridad y la disponibilidad de los datos en un entorno de red. Aquí tienes información en formato de texto continuo sobre seguridad en la red:

La seguridad en la red abarca una variedad de aspectos y desafíos. Uno de los principales enfoques es la **autenticación**, que asegura que solo los usuarios autorizados tengan acceso a los recursos de la red. Esto implica la implementación de contraseñas seguras, la autenticación de dos factores (2FA) y, en algunos casos, la autenticación biométrica para verificar la identidad de los usuarios.

Otro aspecto clave de la seguridad en la red es el **control de acceso**, que determina quién tiene permiso para acceder a qué recursos de la red. El principio de "menor privilegio" dicta que los usuarios deben tener acceso solo a los recursos necesarios para realizar sus tareas laborales, lo que minimiza el riesgo de accesos no autorizados.

La **gestión de amenazas en la red** es esencial para identificar y mitigar riesgos potenciales. Esto incluye la detección y la prevención de intrusiones, así como la supervisión continua del tráfico de red en busca de actividades inusuales o maliciosas. Las herramientas como los sistemas de detección de intrusiones (IDS) y los sistemas de prevención de intrusiones (IPS) son comunes en este contexto.

La seguridad de los **datos en tránsito** es fundamental para proteger la información mientras se mueve a través de la red. Esto se logra mediante el cifrado de datos, que codifica la información de manera que solo los destinatarios autorizados puedan decodificarla. Los protocolos seguros como HTTPS y VPN se utilizan para proteger la comunicación en línea.

La seguridad en la red también implica la protección contra amenazas específicas, como malware, virus y ataques de denegación de servicio (DDoS). Esto se logra mediante el uso de software antivirus, firewalls y la implementación de políticas de seguridad que incluyen actualizaciones de software y parches regulares.

> En resumen, la seguridad en la red es un aspecto crítico de la ciberseguridad que se centra en la protección de la infraestructura de comunicaciones y la información en un entorno de red. Implica la autenticación, el control de acceso, la gestión de amenazas y la protección de datos en tránsito, entre otros aspectos, para garantizar que las redes sean seguras y confiables en un mundo cada vez más digital y conectado.

![Seguridad de la Red](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/seguridad.png?raw=true)

## **Firewall y filtrado de paquetes**

Un **firewall** y el **filtrado de paquetes** son componentes clave de la seguridad de red que se utilizan para proteger una red y sus sistemas contra amenazas cibernéticas. 

### **Firewall**

Un firewall es una barrera de seguridad que se encuentra entre una red interna y una red externa, como Internet. Su función principal es controlar el tráfico de red y decidir qué paquetes de datos se permiten o se bloquean según un conjunto de reglas predefinidas. Los firewalls pueden ser dispositivos físicos o software que se ejecuta en servidores o enrutadores.

Los firewalls se utilizan para varios propósitos, que incluyen:

1. **Control de Acceso:** Los firewalls determinan qué tráfico de red puede ingresar o salir de una red protegida. Esto se basa en reglas que definen qué direcciones IP, puertos y protocolos son permitidos o bloqueados.
2. **Protección contra Amenazas:** Ayudan a proteger una red contra amenazas cibernéticas, como intrusiones, malware y ataques de denegación de servicio (DDoS). Pueden bloquear tráfico malicioso o sospechoso.
3. **Segmentación de Red:** Los firewalls se utilizan para dividir una red en segmentos o zonas de seguridad. Esto reduce la superficie de ataque y limita la propagación de amenazas dentro de la red.
4. **Registro y Auditoría:** Los firewalls suelen tener capacidad de registro para registrar actividades de red. Esto es útil para la monitorización y la revisión de eventos de seguridad.

![Firewall](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/firewall.png?raw=true)

### Filtrado de Paquetes

El filtrado de paquetes es una técnica que se utiliza en firewalls y routers para examinar y controlar el tráfico de red a nivel de paquete. Cada paquete de datos que atraviesa el dispositivo de filtrado de paquetes se compara con reglas específicas y se toma una decisión sobre si permitir o bloquear ese paquete.

Los criterios de filtrado de paquetes pueden incluir:

- Dirección IP de origen y destino.
- Número de puerto.
- Protocolo de transporte (por ejemplo, TCP o UDP).
- Contenido o patrones de datos específicos.

El filtrado de paquetes es una técnica eficaz para bloquear tráfico no deseado o peligroso en la red, pero se basa en reglas específicas y no tiene la inteligencia contextual de un firewall de próxima generación (NGFW). Los NGFW combinan el filtrado de paquetes con inspección profunda de paquetes y capacidades de seguridad avanzadas para una protección más completa.

> 📖 En resumen, los firewalls y el filtrado de paquetes son esenciales para la seguridad de la red al controlar y proteger el tráfico de datos que entra y sale de una red. Estas tecnologías ayudan a prevenir amenazas cibernéticas y garantizan que solo el tráfico legítimo y seguro tenga acceso a los sistemas y recursos de una red protegida.

## VPN (Virtual Private Network)

Una **VPN** (Virtual Private Network, en español Red Privada Virtual) es una tecnología que crea una conexión segura y cifrada entre dos puntos en una red, a menudo a través de Internet. La VPN se utiliza para proteger la privacidad y la seguridad de la comunicación, así como para acceder a recursos de red de manera segura, incluso cuando se utiliza una red no confiable como Internet. 

### Funcionamiento de una VPN

1. **Túnel Seguro:** Una VPN establece un túnel de comunicación cifrado entre tu dispositivo (como una computadora, un teléfono o una tableta) y un servidor VPN. Este túnel actúa como un conducto seguro a través del cual fluyen los datos.
2. **Cifrado de Datos:** Todos los datos que se envían a través de la VPN se cifran antes de salir de tu dispositivo y se descifran en el servidor VPN. Esto asegura que incluso si alguien intercepta los datos en tránsito, no pueda entenderlos sin la clave de descifrado.
3. **Dirección IP Cambiada:** Cuando te conectas a una VPN, tu dirección IP real se oculta y se reemplaza por la dirección IP del servidor VPN. Esto mejora la privacidad al hacer que tu ubicación y tu identidad sean menos rastreables.

**Beneficios de una VPN**

✅ **Seguridad en Redes Públicas:** Las VPN son ideales para proteger la comunicación en redes Wi-Fi públicas o no seguras, como las que se encuentran en cafeterías, hoteles o aeropuertos.

✅ **Acceso Remoto Seguro:** Las VPN permiten a los empleados acceder de forma segura a la red de la empresa desde ubicaciones remotas, lo que facilita el trabajo a distancia.

✅ **Privacidad en Línea:** Una VPN oculta tu dirección IP y cifra tus datos, lo que dificulta que los anunciantes y los rastreadores en línea te sigan en línea.

✅ **Acceso a Contenido Restringido:** Puedes utilizar una VPN para acceder a contenido en línea que podría estar bloqueado geográficamente en tu ubicación.

**Tipos de VPN:**

| VPN de Acceso Remoto | Permite que un usuario se conecte a la red de la empresa de forma segura desde una ubicación remota. Es útil para empleados que trabajan desde casa o en movimiento. |
| --- | --- |
| VPN de Sitio a Sitio | Conecta dos redes enteras, como las oficinas de una empresa en diferentes ubicaciones geográficas. Estas VPN son comunes en empresas multinacionales. |
| VPN de Acceso Público | Ofrece servicios de VPN a través de proveedores de servicios públicos. Los usuarios pueden suscribirse a estos servicios para proteger su privacidad en línea. |
| VPN de Capa 2 y Capa 3 | Diferentes tipos de VPN pueden operar en capas de red diferentes (como la capa 2 o la capa 3) y tener aplicaciones específicas según las necesidades de la organización. |

![VPN](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/VPN.png?raw=true)

> 📖 Una **VPN** es una herramienta esencial para proteger la privacidad y la seguridad en línea, así como para establecer conexiones seguras en redes públicas o para acceder a recursos de red de forma remota. Su capacidad para cifrar datos y ocultar direcciones IP la hace valiosa tanto para usuarios individuales como para empresas que buscan proteger la confidencialidad de sus comunicaciones y datos.

La diferencia clave entre una **VPN** (Virtual Private Network) y un **proxy** es cómo manejan la privacidad y la seguridad:

| VPN | Proxy |
| --- | --- |
| Una VPN crea una conexión segura y cifrada entre tu dispositivo y un servidor remoto, ocultando tu dirección IP y protegiendo tus datos. Es más adecuada para la privacidad y la seguridad, ideal para proteger la comunicación en redes públicas o acceder a la red de una empresa de forma segura. | Un proxy actúa como un intermediario entre tu dispositivo y la web. Puede ocultar tu dirección IP, pero generalmente no cifra los datos. Los proxies son útiles para el acceso a contenido bloqueado geográficamente o para ocultar tu ubicación, pero pueden ser menos seguros que una VPN. |

> 💡 Utiliza una VPN cuando necesites una conexión segura y cifrada para la privacidad y la seguridad. Emplea un proxy cuando desees cambiar tu ubicación o acceder a contenido geográficamente restringido, pero no necesites una protección de datos tan sólida.

## Seguridad en redes WiFi

La seguridad de Wi-Fi se refiere a las prácticas y medidas que se implementan para proteger una red inalámbrica (Wi-Fi) de amenazas y accesos no autorizados. Es esencial asegurarse de que tu red Wi-Fi esté protegida adecuadamente para evitar intrusiones y proteger la privacidad de los dispositivos y datos conectados.

### Principales Aspectos de la Seguridad de Wi-Fi

1. **Contraseña Fuerte:** Utiliza una contraseña segura para proteger tu red Wi-Fi. Evita contraseñas fáciles de adivinar y opta por combinaciones de letras, números y caracteres especiales.
2. **Encriptación:** Habilita la encriptación en tu router Wi-Fi. El estándar más común es WPA3 (o WPA2 si WPA3 no está disponible), que cifra la comunicación entre dispositivos y el router.
3. **Nombre de Red (SSID) Oculto:** Si es posible, oculta el SSID de tu red para que no sea visible para dispositivos cercanos. Esto añade una capa adicional de seguridad al hacer que la red sea menos visible para posibles atacantes.
4. **Filtro de Direcciones MAC:** Configura tu router para permitir solo dispositivos con direcciones MAC específicas. Si bien esto no es una medida de seguridad infalible, puede agregar una capa adicional de protección.
5. **Actualizaciones del Firmware:** Mantén el firmware de tu router actualizado. Las actualizaciones a menudo incluyen correcciones de seguridad que protegen contra vulnerabilidades conocidas.
6. **Red de Invitados:** Si tu router lo admite, crea una red de invitados separada para visitantes. Esto evita que los dispositivos de invitados tengan acceso completo a tu red principal.
7. **Cambio de Contraseñas Predeterminadas:** Cambia las contraseñas predeterminadas del router y de las cuentas de administrador. Las contraseñas predeterminadas son conocidas por los ciberdelincuentes.

**Casos de Uso y Recomendaciones:**

✅ En el hogar, asegúrate de que tu red Wi-Fi esté protegida con una contraseña fuerte y la encriptación adecuada. Limita el acceso solo a dispositivos autorizados.

✅ En entornos empresariales, utiliza autenticación de usuario y encriptación robusta. Considera implementar redes separadas para empleados y visitantes.

✅ Si necesitas acceso remoto a tu red, utiliza una VPN para una conexión segura desde fuera de tu red local.

✅ Realiza auditorías de seguridad de tu red Wi-Fi de forma regular para identificar posibles vulnerabilidades y mejorar la protección.

### Buenas prácticas

1. **Encriptación WPA3/WPA2:** Utiliza encriptación WPA3 o WPA2 en tu red Wi-Fi. Estos protocolos de seguridad cifran la comunicación entre dispositivos y el router. Evita el uso de WEP, que es menos seguro.
2. **Contraseñas Fuertes:** Configura contraseñas fuertes tanto para el acceso a la red Wi-Fi como para el panel de administración del router. Evita contraseñas predefinidas o débiles.
3. **Actualizaciones de Firmware:** Mantén el firmware del router actualizado. Las actualizaciones a menudo incluyen correcciones de seguridad que protegen contra vulnerabilidades conocidas.
4. **Red de Invitados:** Si es posible, configura una red de invitados separada con acceso a Internet pero sin acceso a la red principal. Esto limita la exposición de la red principal a dispositivos no confiables.
5. **Monitoreo y Auditoría:** Implementa herramientas de monitoreo y realiza auditorías regulares de seguridad en la red Wi-Fi. Esto te ayudará a detectar y mitigar posibles amenazas y vulnerabilidades.

> 📖 La seguridad en el enrutador y el switch es esencial para proteger una red empresarial o doméstica contra amenazas cibernéticas y garantizar un funcionamiento seguro y confiable. Recuerda que los dispositivos de red también son actores en el escenario de ciberseguridad:

### Seguridad en el Enrutador

1. **Contraseñas Fuertes:** Cambia las contraseñas predeterminadas del enrutador y establece contraseñas fuertes para el acceso al panel de administración. Evita utilizar información fácilmente adivinable, como nombres o fechas de nacimiento.
2. **Actualizaciones de Firmware:** Mantén el firmware del enrutador actualizado. Los fabricantes suelen lanzar actualizaciones de seguridad que corrigen vulnerabilidades conocidas.
3. **Cortafuegos (Firewall):** Habilita el cortafuegos integrado en el enrutador para filtrar el tráfico no deseado y bloquear posibles amenazas. Configura las reglas del cortafuegos según tus necesidades.
4. **Desactiva Servicios Innecesarios:** Desactiva cualquier servicio o puerto que no necesites. Cuantos menos servicios estén habilitados, menos posibilidades hay de que se exploten vulnerabilidades.
5. **Acceso Remoto Seguro:** Si habilitas el acceso remoto al enrutador, hazlo de manera segura utilizando una VPN u otras medidas de autenticación fuertes. Limita el acceso solo a direcciones IP autorizadas.

### Seguridad en el Switch

1. **VLAN (Virtual LAN):** Utiliza VLAN para segmentar la red en grupos lógicos. Esto mejora la seguridad al limitar la comunicación entre dispositivos y restringir el acceso a áreas críticas de la red.
2. **Control de Acceso basado en Puertos (Port-Based Access Control):** Configura el switch para limitar el acceso a puertos específicos. Esto evita que dispositivos no autorizados se conecten a la red.
3. **Monitoreo de Tráfico:** Implementa herramientas de monitoreo de tráfico para detectar actividades inusuales o no autorizadas en la red. Esto facilita la detección de posibles amenazas.
4. **Actualizaciones de Firmware:** Al igual que con los enrutadores, mantén el firmware del switch actualizado para beneficiarte de las correcciones de seguridad.
5. **Autenticación 802.1X:** Utiliza autenticación basada en estándar 802.1X para controlar el acceso a la red. Requiere que los dispositivos se autentiquen antes de permitirles conectarse.

> 📖 En conjunto, estas prácticas ayudan a fortalecer la seguridad en el enrutador y el switch, formando una sólida defensa contra amenazas cibernéticas y proporcionando un entorno de red más seguro y confiable.
