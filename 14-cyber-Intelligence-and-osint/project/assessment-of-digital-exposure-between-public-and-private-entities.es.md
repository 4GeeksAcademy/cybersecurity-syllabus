# Evaluación de Exposición Digital entre Entidades Pública y Privada

Este proyecto tiene como objetivo aplicar técnicas de OSINT (Open Source Intelligence) para comparar la **superficie de exposición digital** de dos organizaciones reales: una del sector público y otra del sector privado. Tu objetivo será analizar, documentar y comparar los riesgos de seguridad asociados a información públicamente expuesta de ambas entidades, sin realizar acciones intrusivas, y generar un informe técnico con hallazgos, riesgos y recomendaciones.

## 📄 Instrucciones

1. **Selección de las organizaciones:** Cada grupo debe elegir una organización pública** (ej. universidad, hospital, municipio) y una organización privada (ej. empresa tecnológica, clínica privada, ecommerce). Ambas deben tener dominio web propio, presencia en buscadores y accesibilidad a fuentes abiertas.

2. **Fase de recolección OSINT:** Recolectar información de manera pasiva sobre ambas entidades utilizando herramientas OSINT. Categorías sugeridas:

    - Infraestructura visible. Subdominios (`dnsdumpster.com`, `crt.sh`, `Sublist3r`), direcciones IP y hosting.

    - Correos electrónicos y cuentas públicas: `theHarvester`, `hunter.io`

    - Servicios accesibles desde internet: `Shodan`, `Censys` para identificar puertos abiertos, banners, tecnologías

    - Filtraciones y credenciales expuestas: `Have I Been Pwned`, `DeHashed` (solo si permite)

    - Documentos y rutas indexadas: Uso de Google Dorks para localizar archivos sensibles y páginas no deseadas (`filetype:`, `intitle:`, `inurl:`)

    - Perfiles en redes sociales (opcional): Presencia en plataformas, comentarios públicos, exposición de datos.



3. **Análisis comparativo**. Completar una tabla con los hallazgos clave de cada organización:

| Elemento                      | Entidad Pública     | Entidad Privada     |
|------------------------------|----------------------|----------------------|
| Subdominios expuestos        |                      |                      |
| Correos electrónicos         |                      |                      |
| Dispositivos en Shodan       |                      |                      |
| Filtraciones encontradas     |                      |                      |
| Documentos indexados         |                      |                      |
| Riesgos identificados        |                      |                      |

Responde:

- ¿Cuál entidad muestra mayor exposición y por qué?
- ¿Qué prácticas de seguridad pasiva se evidencian?
- ¿Qué riesgos son más relevantes en cada caso?

4. **Informe final**. El informe sebe incluir:

1. Introducción
2. Metodología utilizada
3. Resultados y evidencias
4. Comparación estructurada
5. Recomendaciones de mitigación
6. Conclusión crítica


## ✅ Entregables

- Informe técnico en PDF
- Tabla comparativa (en el informe o aparte)
- Evidencias organizadas (opcional: carpeta adjunta)
- (Opcional) Presentación de resultados en clase


## Criterios de evaluación

| Criterio                                | Ponderación |
|----------------------------------------|-------------|
| Uso correcto de herramientas OSINT     | 30%         |
| Profundidad del análisis comparativo   | 25%         |
| Calidad del informe y redacción        | 20%         |
| Relevancia de hallazgos y riesgos      | 15%         |
| Propuestas de mejora y mitigación      | 10%         |



## 📝 Licencia y uso

Este proyecto es de uso exclusivamente académico y no autoriza la exposición pública de datos reales sin consentimiento. Basado en principios de ciberinteligencia ética y OSINT responsable.

