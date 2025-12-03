# DETECTOR DE SOBRECALENTAMIENTO EN TRANSFORMADORES

Sistema de análisis térmico basado en imágenes infrarrojas para detectar
sobrecalentamiento en transformadores eléctricos. El código genera un baseline
a partir de imágenes en condición normal y luego compara nuevas imágenes para
identificar anomalías térmicas y hotspots.

------------------------------------------------------------
REQUISITOS PREVIOS
------------------------------------------------------------

1. Usar Google Colab (recomendado).
2. Descargar la carpeta completa de imágenes térmicas desde:
   https://drive.google.com/drive/folders/1c09LUMkdFATJFZZKTW_yrhQwFTTb8gLE?usp=sharing
3. Guardar la carpeta en:
   Mi Drive / imagenes_termicas

La carpeta debe contener subcarpetas como:
- p1_Noload  (imágenes normales para baseline)
- p2_80
- p3_160
- p4_240
- p5_320
- p6_400
- p7_480
- p8_560
- p9_600 (imágenes con fallas)

------------------------------------------------------------
INSTRUCCIONES DE USO
------------------------------------------------------------

1. Abrir Google Colab y ejecutar el código del repositorio.
2. Montar Google Drive.
3. Cambiar la ruta al directorio:
   /content/drive/MyDrive/imagenes_termicas
4. En la primera ejecución:
   - El programa calcula el baseline con p1_Noload
   - Genera el archivo baseline_stats.pkl
5. En ejecuciones futuras:
   - Se carga automáticamente baseline_stats.pkl
6. El sistema:
   - Preprocesa las imágenes
   - Detecta bordes térmicos
   - Calcula métricas estadísticas
   - Identifica hotspots y posibles fallas
   - Genera visualizaciones PNG con el diagnóstico

------------------------------------------------------------
ESTRUCTURA ESPERADA DE CARPETAS
------------------------------------------------------------

imagenes_termicas/
├── p1_Noload
├── p2_80
├── p3_160
├── p4_240
├── p5_320
├── p6_400
├── p7_480
├── p8_560
└── p9_600

------------------------------------------------------------
NOTAS IMPORTANTES
------------------------------------------------------------

- Para analizar otra carpeta cambiar el valor:
  CARPETA_IMAGENES_PRUEBA
- Funciona con imágenes BMP, JPG y PNG.
- Las salidas se guardan como imágenes resultado_*.png


