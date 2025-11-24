Este proyecto implementa un sistema de detección automática de dársenas libres u ocupadas en estacionamientos, utilizando técnicas de visión por computadora y procesamiento digital de imágenes.

El objetivo principal es analizar imágenes capturadas desde cámaras fijas y determinar el estado (ocupado/libre) de cada dársena de manera rápida, robusta y eficiente, sin emplear modelos complejos de machine learning.

El sistema incluye dos implementaciones independientes:

Implementación 1 – Análisis estadístico (Media + Desvío estándar)

Clasifica cada dársena a partir de métricas estadísticas de los niveles de gris de los píxeles pertenecientes a la región.

Se calcula media y desvío estándar.

Se aplican umbrales empíricos para decidir ocupación.

Alto desempeño (hasta 100% de precisión en varios escenarios).

Implementación 2 – Texturas con GLCM

Utiliza la Matriz de Co-ocurrencia de Niveles de Gris (GLCM) para analizar la homogeneidad de la textura dentro de cada dársena.

Se reduce resolución y niveles de gris para minimizar costos computacionales.

Clasificación basada en umbral de homogeneidad.

Desempeño correcto, aunque más sensible a sombras, manchas y elementos externos.

Flujo general del sistema

Adquisición de imágenes desde cámaras fijas.
Preprocesamiento (grises, suavizado, ecualización).
Definición manual de dársenas mediante polígonos.
Extracción de características (estadísticas o texturales).
Clasificación y visualización sobre la imagen.
Cómputo final de dársenas libres y ocupadas.

Resultados y conclusiones

El proyecto demuestra que es posible lograr una detección muy precisa con métodos simples y sin entrenar modelos de IA complejos.
La primera implementación resultó más robusta, especialmente ante variaciones de iluminación y ocupación.
