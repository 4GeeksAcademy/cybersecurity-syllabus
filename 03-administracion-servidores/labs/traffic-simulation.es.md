# Simulación de tráfico al sitio wordpress

## Consigna

El estudiante debe generar tráfico artificial desde la maquina Kali hacia el sitio Wordpress. En el servidor se deben implementar herramientas de monitoreo para detectar las oleadas de peticiones y evaluar el desempeño del servidor. 

## Definir que computadora se va a usar

- Se continuará trabajando en un proyecto anterior?
- Que maquina virtual se va a usar?

## Seguir plantilla de 4geeks:

- README.md README.es.md y learn.json
- Los readme debe tener una intro, como empezar el proyecto, instrucciones paso paso y como entregar el proyecto.

## Pasos claros para realizar el project (step by step).

## Definir Entregable Exacto

- Informe de evaluación del desempeño del servidor
- Tiene que ser corrigible por el profesor o TA y en el futuro poder ser corregible de forma automatica (en la gran mayoria de los enunciados).

## Notas

- Herramienta de monitoreo Nessus (gratis) y OpenVas.
- Repo con instrucciones.
- Como simulamos el trafico? No puede venir del mismo IP.
- Determinar métricas y demás elementos relevantes que deben integrar el informe.


wpscan --url 192.168.0.109/wordpress Para revelar información del servidor y de la instalacion de wordpress
