DETECTOR DE SOBRECALENTAMIENTO EN TRANSFORMADORES

Este proyecto implementa un sistema de análisis térmico para identificar posibles sobrecalentamientos en transformadores mediante imágenes infrarrojas. Utiliza procesamiento de imágenes, análisis estadístico y detección de hotspots para determinar si un transformador opera dentro de condiciones normales.

REQUISITOS PREVIOS

Usar Google Colab (recomendado).

Tener la carpeta de imágenes térmicas disponible en este enlace:
https://drive.google.com/drive/folders/1c09LUMkdFATJFZZKTW_yrhQwFTTb8gLE?usp=sharing

La carpeta descargada debe ubicarse en la siguiente ruta dentro de Google Drive:
Mi Drive / imagenes_termicas

Dentro de esta carpeta deben existir subcarpetas como:

p1_Noload (imágenes normales para construir el baseline)

p2_80

p3_160

…

p9_600 (imágenes con posibles fallas)

INSTRUCCIONES DE USO

Montar Google Drive en Colab.

Cambiar el directorio hacia la carpeta llamada imagenes_termicas dentro de Mi Drive.

Ejecutar el código completo del repositorio.

El programa realizará automáticamente lo siguiente:

Cargar imágenes normales y calcular el baseline.

Guardar un archivo llamado baseline_stats.pkl.

Analizar las imágenes de prueba.

Detectar bordes, calcular métricas térmicas y determinar si existe sobrecalentamiento.

Generar imágenes de salida con hotspots y mapas térmicos.

El archivo baseline_stats.pkl solo se genera la primera vez. Si ya existe, el programa lo cargará automáticamente.

ESTRUCTURA ESPERADA DE CARPETAS

imagenes_termicas
│
├── p1_Noload
├── p2_80
├── p3_160
├── p4_240
├── p5_320
├── p6_400
├── p7_480
├── p8_560
└── p9_600

NOTAS IMPORTANTES

Puedes cambiar la carpeta a analizar modificando el valor de CARPETA_IMAGENES_PRUEBA dentro del código.

El análisis genera archivos PNG con la visualización completa del diagnóstico.

El sistema funciona con imágenes BMP, JPG o PNG.
