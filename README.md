Ecosistemas del Anime: Segmentación de Audiencias con la API de AniList

Este repositorio contiene un proyecto integral de Ciencia de Datos enfocado en la industria del anime. El objetivo principal es transformar datos estadísticos complejos extraídos de la API de AniList en decisiones estratégicas de negocio, optimizando la adquisición de licencias y reduciendo el riesgo comercial mediante técnicas avanzadas de Aprendizaje No Supervisado.
  Enlaces del Proyecto
• Sitio Web Público (Dashboard): Haz clic aquí para ver el Flexdashboard Interactivo https://guillermoanibalgv99.github.io/proyecto13-anime/
• Reporte Técnico Detallado: Disponible directamente en la barra lateral del dashboard o abriendo el archivo reporte_analisis.html en este repositorio.

 Integrantes del Equipo
  Equipo 13 - Anime
• Mendoza Díaz Citlali
• Peña Romero Gerardo
• Ramírez Pérez Gerardo Enrique
• Vásquez Rodríguez Iván
• Galindez Vergara Guillermo Anibal

  Metodología Aplicada
Para el desarrollo de esta herramienta se implementó un flujo de trabajo analítico dividido en dos fases principales:
1. Reducción de Dimensionalidad (PCA): Se identificaron variables latentes y ocultas del mercado estructuradas bajo dos grandes ejes conceptuales: Dimensión de Impacto y Audiencia (PC1) y Dimensión de Estructura y Temática (PC2).
2. Segmentación de Mercado (K-Means): Con base en las dimensiones obtenidas en el PCA, se determinó un óptimo de K = 5 clústeres para clasificar el catálogo de AniList. Esto permitió definir perfiles claros de comportamiento como el Clúster 1 (Titanes / Mayor Retención) y el Clúster 5 (Digital / Mayor Eficiencia Costo-Beneficio).
  Arquitectura del Repositorio y Reproducibilidad
Para garantizar que cualquier analista pueda replicar localmente este ecosistema sin necesidad de ejecutar los modelos matemáticos pesados desde cero, se implementó una arquitectura basada en archivos serializados de R (.rds):
• index.Rmd / index.html: Código fuente y despliegue del Flexdashboard principal (Landing Page).
• Anime.Rmd / reporte_analisis.html: Cuaderno de análisis técnico lineal que contiene el desarrollo del modelo estadístico.
• anilist_anime.csv: Conjunto de datos base extraído de la API de AniList.
• Archivos .rds (df_clusters_asignados.rds, popvscal.rds, scorefor.rds, etc.): Almacenan los objetos, gráficos procesados y clústeres asignados directamente del modelo para optimizar la velocidad de carga.
  Requisitos del Entorno (R)
Para compilar y reproducir este proyecto localmente, asegurarse de tener instaladas las siguientes librerías en el entorno de R:

tidyverse
flexdashboard
plotly
cluster
factoextra
rmarkdown

  Instrucciones para Ejecución Local
1. Clonar este repositorio en su computadora de manera local.
2. Abrir el archivo de proyecto equipo13_proyecto.Rproj utilizando RStudio.
3. Para actualizar o renderizar el reporte de análisis completo, ejecutar en la consola: rmarkdown::render("Anime.Rmd", output_file = "reporte_analisis.html")
4. Para actualizar la landing page interactiva, presione el botón Knit dentro del archivo index.Rmd.