---
title: "Implementación y Medidas de Seguridad del ENS"
subtitle: "🛡️ Comprendiendo los componentes clave de la implementación y las medidas de seguridad en el Esquema Nacional de Seguridad (ENS) de España"
tags: ["ENS", "ciberseguridad"]
authors: ["alesanchezr"]

---

# Implementación y Medidas de Seguridad del ENS

> Antes de comenzar, cubrimos exhaustivamente el ENS (Esquema Nacional de Seguridad) en varias lecciones. Esta lección se centra únicamente en las medidas de seguridad y la implementación.
> Lee una [Introducción al ENS](https://4geeks.com/es/lesson/introduccion-al-ens-esquema-nacional-de-seguridad) y aprende más sobre el [Marco organizativo y operativo del ENS](https://4geeks.com/es/lesson/marco-organizacional-y-operacional-del-ens).

Para implementar el Esquema Nacional de Seguridad (ENS) de España 🇪🇸, primero necesitamos nombrar un comité que será responsable de la implementación del esquema.

![Implementación del ENS](https://github.com/4GeeksAcademy/cybersecurity-syllabus/raw/main/assets/12-ens/esquema-nacional-de-seguridad.jpg?raw=true)

## Roles responsables de la implementación del ENS dentro de una organización

Desde la entrada en vigor del **Real Decreto 311/2022**, el **Esquema Nacional de Seguridad (ENS)** define de forma clara y precisa cuatro roles clave que deben estar presentes en todas las organizaciones sujetas al cumplimiento del ENS. Estos roles se especifican en el **Artículo 11** del real decreto, y **sustituyen modelos antiguos como comités o presidentes con voto de calidad**, los cuales **no figuran en la normativa oficial**.

Cada rol tiene responsabilidades bien delimitadas que aseguran la adecuada protección de los sistemas, la información y los servicios que gestiona una entidad. A continuación se describen en detalle:


### 🗂️ Responsable de la Información

Es la figura encargada de **determinar los requisitos de seguridad de la información que se trata** dentro del sistema. Esta persona, o en su caso un órgano colegiado, debe identificar la sensibilidad y criticidad de los datos, y establecer los niveles de protección necesarios conforme al **Anexo I del ENS**, que establece la categoría del sistema.

**Responsabilidades clave**:

- Clasificar la información.
- Identificar riesgos asociados al tratamiento de datos.
- Establecer requerimientos de seguridad en función de la sensibilidad.


### ⚙️ Responsable del Servicio

Tiene la responsabilidad de **definir los requisitos de seguridad de los servicios prestados por el sistema**. Esto implica evaluar el impacto que tendría una alteración, interrupción o fallo en la prestación del servicio, y colaborar con el Responsable del Sistema para identificar los riesgos y las medidas necesarias.

**Responsabilidades clave**:

- Identificar el impacto de incidentes sobre los servicios.
- Establecer los niveles de seguridad adecuados para cada servicio.
- Coordinarse con el Responsable del Sistema en la planificación de medidas.


### 🕵️‍♂️ Responsable de Seguridad (CISO)

Es el encargado de la **gestión integral de la seguridad de la información** en la organización. Debe desarrollar planes de seguridad, realizar controles periódicos, coordinar auditorías, gestionar incidentes, y servir como punto de contacto con las autoridades competentes.

**Responsabilidades clave**:

- Diseñar, aplicar y mantener políticas de seguridad.
- Coordinar la Declaración de Aplicabilidad (DoA).
- Supervisar la respuesta a incidentes y notificar a las autoridades.
- Impulsar campañas de formación y concienciación.


### 💻 Responsable del Sistema

Su función principal es **desarrollar, operar y mantener el sistema de información**, asegurando que se implementen y mantengan las medidas de seguridad adecuadas en todas las fases del ciclo de vida del sistema. También se encarga de categorizar el sistema según el ENS y realizar el análisis de riesgos.

**Responsabilidades clave**:

- Definir la arquitectura técnica y las políticas operativas.
- Aprobar configuraciones y cambios críticos de hardware/software.
- Mantener actualizado el análisis de riesgos.
- Coordinarse con otros responsables para asegurar la continuidad del servicio y la protección del sistema.

> 🔒 **Nota**: Estos cuatro roles deben estar **claramente definidos, documentados y asignados formalmente** dentro de la organización, y no pueden fusionarse de forma arbitraria. Su correcta implementación es un requisito fundamental para el cumplimiento del ENS y la obtención de la certificación correspondiente.


## Implementación del ENS: Enfoque Escalonado y Ciclo de Vida

![Implementación del ENS](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/12-ens/proceso-ens.png?raw=true)

La implementación del Esquema Nacional de Seguridad (ENS) no debe entenderse como una acción puntual, sino como un proceso continuo que abarca todo el ciclo de vida del sistema, desde su diseño inicial hasta su retirada definitiva.

Este proceso debe estar guiado por un análisis de riesgos que determine qué medidas deben aplicarse, con qué nivel de exigencia (BASE, Reforzado, Alto) y en qué momento. La correcta implementación del ENS garantiza no solo el cumplimiento normativo, sino también la protección efectiva de los servicios y la información.


### 1. Comprensión del ENS

Antes de aplicar cualquier medida, la organización debe entender su contexto y obligaciones. Este paso inicial sienta las bases para el resto del proceso:

- Clasifica tus sistemas: Determina si se trata de sistemas de nivel Bajo, Medio o Alto en función del impacto que tendría una brecha de seguridad en la confidencialidad, integridad o disponibilidad.
- Revisa los Anexos I y II del ENS:
  - Anexo I: Establece cómo categorizar los sistemas según su nivel.
  - Anexo II: Contiene las 73 medidas de seguridad obligatorias, divididas en organizativas, operacionales y de protección.
- Evalúa el cumplimiento legal vigente: Asegúrate de cumplir también con otras normativas complementarias, como el RGPD, la LOPDGDD, la Ley 40/2015 o la Ley 39/2015, entre otras.


### 2. Análisis de brechas (Gap Analysis)

Este análisis permite conocer el estado actual de la organización frente a los requisitos del ENS y detectar puntos débiles:

- Compara las medidas del ENS con la situación real de tus sistemas.
- Identifica qué controles no están implementados o lo están de forma insuficiente.
- Clasifica cada brecha según su impacto y urgencia.

Este análisis alimentará el Plan de Adecuación al ENS, que recoge los pasos concretos para alcanzar el cumplimiento.


### 3. Gobierno de Seguridad

Para cumplir con el ENS, la organización debe establecer una estructura clara de responsabilidades, sin recurrir a comités informales ni órganos sin reconocimiento normativo.

- Designa formalmente los cuatro roles definidos en el artículo 11 del RD 311/2022:
  - Responsable de la Información
  - Responsable del Servicio
  - Responsable del Sistema
  - Responsable de Seguridad (CISO)
- Define funciones, autoridad, flujos de aprobación y mecanismos de coordinación entre ellos.


### 4. Desarrollo del SGSI (Sistema de Gestión de Seguridad de la Información)

Este paso consiste en crear los fundamentos organizativos y técnicos que permitirán gestionar la seguridad de forma estructurada:

- Redacta e implementa políticas y procedimientos de seguridad.
- Establece un proceso de gestión de riesgos, acorde con metodologías reconocidas (como MAGERIT).
- Clasifica los activos de información (datos, servicios, infraestructura, personal).
- Define controles de protección según su nivel de criticidad.


### 5. Aplicación de controles técnicos

Aquí se despliegan las medidas técnicas del ENS, siempre alineadas con los resultados del análisis de riesgos. Entre ellas:

- Cifrado de la información (en reposo y en tránsito).
- Mecanismos robustos de autenticación y control de accesos.
- Sistemas de monitorización y detección de incidentes.
- Copias de seguridad, segmentación de redes, alta disponibilidad, entre otros.

La implementación técnica sin gobierno ni políticas claras puede resultar ineficaz. Ambos componentes deben ir de la mano.



### 6. Medidas administrativas

Las medidas administrativas complementan las técnicas y organizativas, asegurando que el factor humano también se gestione adecuadamente:

- Programas de formación y concienciación en seguridad para el personal.
- Protocolos de respuesta ante incidentes.
- Procedimientos para la gestión del cambio, control de configuraciones y revisiones periódicas.



### 7. Relación con terceros

La seguridad no termina en los límites de la organización. El ENS exige gestionar los riesgos derivados de proveedores externos o servicios contratados:

- Revisión de contratos y cláusulas de seguridad.
- Evaluación de riesgos de terceros.
- Supervisión del cumplimiento de medidas por parte de proveedores (auditorías, informes, etc.).


### 8. Auditoría y certificación

Una vez implementadas las medidas, es necesario verificar el cumplimiento del ENS mediante auditorías:

- Las entidades obligadas deben pasar una auditoría externa cada 2 años.
- La auditoría debe realizarla un organismo acreditado o una unidad independiente, conforme a lo establecido en la Guía CCN-STIC 820.
- Si se supera la evaluación, se emite el certificado ENS, válido por 24 meses.

La certificación no es el final, sino el inicio de un ciclo de mejora continua. Las medidas deben mantenerse y actualizarse durante todo el ciclo de vida del sistema.


# Medidas de Seguridad del ENS

Las medidas de seguridad del Esquema Nacional de Seguridad (ENS) se organizan en tres marcos:

- **Marco organizativo** (`org`)
- **Marco operacional** (`op`)
- **Medidas de protección** (`mp`)

Cada medida tiene niveles de aplicación según el perfil de seguridad del sistema:

- `=`: Requisito **BASE** (obligatorio para todos)
- `+`: Requisito para sistemas de **nivel medio**
- `++`: Requisito para sistemas de **nivel alto**

> Esta no es una lista exhaustiva. Las 73 medidas completas están disponibles en la Guía CCN-STIC 808.


## Marco Organizativo (`org`)

### Normativas y Procedimientos de Seguridad

| Medida                       | Nivel Bajo | Nivel Medio | Nivel Alto | Código |
|-----------------------------|------------|-------------|------------|--------|
| Normativas de seguridad     | =          | +           | ++         | org.2  |
| Procedimientos de seguridad | =          | +           | ++         | org.3  |

### Procesos de Autorización

| Medida                                 | Nivel Bajo | Nivel Medio | Nivel Alto | Código |
|----------------------------------------|------------|-------------|------------|--------|
| Control de instalaciones y componentes | =          | =           | =          | org.4  |


## Marco Operacional (`op`)

### Planificación

| Medida                             | Nivel Bajo | Nivel Medio | Nivel Alto | Código   |
|------------------------------------|------------|-------------|------------|----------|
| Análisis de riesgos                | =          | +           | ++         | op.pl.1  |
| Arquitectura de seguridad          | =          | +           | ++         | op.pl.2  |
| Adquisición de nuevos componentes  | =          | =           | =          | op.pl.3  |
| Gestión de capacidades             | —          | =           | =          | op.pl.4  |


## Medidas de Protección (`mp`)

### Protección de Instalaciones (`mp.if.*`)

| Medida                                           | Nivel Bajo | Nivel Medio | Nivel Alto | Código   |
|--------------------------------------------------|------------|-------------|------------|----------|
| Áreas separadas con control de acceso            | =          | =           | =          | mp.if.1  |
| Identificación de personas                       | =          | =           | =          | mp.if.2  |
| Acondicionamiento de los locales                 | =          | =           | =          | mp.if.3  |
| Energía eléctrica                                 | +          | =           | =          | mp.if.4  |
| Protección frente a incendios                     | =          | =           | =          | mp.if.5  |
| Protección frente a inundaciones                  | —          | =           | =          | mp.if.6  |
| Registro de entrada y salida de equipamiento      | =          | =           | =          | mp.if.7  |
| Instalaciones alternativas                        | —          | —           | =          | mp.if.8  |

### Protección de Personal y Activos (`mp.per.*`)

| Medida                              | Nivel Bajo | Nivel Medio | Nivel Alto | Código    |
|-------------------------------------|------------|-------------|------------|-----------|
| Caracterización del puesto          | —          | =           | =          | mp.per.1  |
| Deberes y obligaciones              | =          | =           | =          | mp.per.2  |
| Concienciación                      | =          | =           | =          | mp.per.3  |
| Formación                           | =          | =           | =          | mp.per.4  |
| Personal alternativo                | —          | —           | =          | mp.per.5  |
| Medios alternativos (equipamiento) | —          | —           | =          | mp.per.8  |

### Protección de Información (`mp.info.*`)

| Medida                     | Nivel Bajo | Nivel Medio | Nivel Alto | Código     |
|----------------------------|------------|-------------|------------|------------|
| Datos de carácter personal | =          | =           | =          | mp.info.1  |
| Calificación de la información | +      | =           | =          | mp.info.2  |
| Cifrado                    | —          | —           | =          | mp.info.3  |
| Firma electrónica          | +          | ++          | ++         | mp.info.4  |
| Sellos de tiempo           | =          | =           | =          | mp.info.5  |
| Limpieza de documentos     | =          | =           | =          | mp.info.6  |
| Copias de seguridad        | =          | =           | =          | mp.info.9  |

### Protección de Servicios (`mp.s.*`)

| Medida                                        | Nivel Bajo | Nivel Medio | Nivel Alto | Código   |
|-----------------------------------------------|------------|-------------|------------|----------|
| Protección del correo electrónico             | =          | =           | =          | mp.s.1   |
| Protección de servicios y aplicaciones web    | =          | +           | +          | mp.s.2   |
| Protección frente a la denegación de servicio | —          | =           | +          | mp.s.8   |
| Medios alternativos para servicios críticos   | —          | —           | =          | mp.s.9   |


## Leyenda de Niveles de Aplicación

- `=`: Nivel BASE, obligatorio para todos los sistemas
- `+`: Aplicable a sistemas de nivel medio
- `++`: Aplicable a sistemas de nivel alto
- `—`: No aplicable explícitamente (puede depender del análisis de riesgos)
