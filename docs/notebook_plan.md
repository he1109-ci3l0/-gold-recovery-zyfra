# Plan del notebook — Recuperación de oro

## Reglas (no se rompen)
1. Una celda a la vez, con confirmación entre cada una. Nunca el notebook entero.
2. Imports todos juntos en una sola celda al inicio.
3. Numeración del curso (1.1, 1.2, 2.1...), no la del pipeline.
4. Paleta del proyecto en todas las gráficas: blush #F3E4DD, durazno #EABCA5, malva #C9A7BF, vino #733445, pizarra #334142, vino oscuro #381D26.
5. Markdown del notebook = voz de analista (profesional). La explicación de "cómo se hace" va en el chat, no en el notebook.
6. Código sin comentarios inline. Funciones reutilizables, sin duplicar.
7. RANDOM_STATE = 12345.

## Estructura (orden fijo de celdas)

### Apertura
- MD · Título + objetivo + método
- MD · Resumen ejecutivo (abre con el resultado; se llena al final)
- MD · Contexto, condiciones y supuestos (proceso, 2 objetivos, sMAPE 25/75, test sin objetivos → solo features del test)
- CODE · Imports + RANDOM_STATE + paleta (dict) + estilo

### 1. Preparación de los datos
- MD · Encabezado
- CODE · 1.1 cargar 3 archivos + dimensiones
- CODE · 1.2 verificar recovery (EAM)
- CODE · 1.3 columnas ausentes en test
- CODE · 1.4 preprocesamiento (fecha, orden, ffill)
- MD · Hallazgos sección 1

### 2. Análisis de los datos
- MD · Encabezado
- CODE · 2.1 metales por etapa
- CODE · 2.2 tamaño de partícula train vs test
- CODE · 2.3 concentraciones totales + eliminación de anomalías
- MD · Hallazgos sección 2

### 3. Modelo
- MD · Encabezado
- CODE · 3.1 función sMAPE + scorer
- CODE · 3.2 features (intersección con test) + 2 objetivos
- CODE · 3.2 entrenar modelos + validación cruzada → tabla comparativa
- CODE · 3.3 mejor modelo en test (verdad desde full por fecha)
- MD · Hallazgos / resultados

### Cierre
- MD · Parámetros no rentables — lectura de negocio
- CODE · importancia de características del mejor modelo
- MD · Conclusión de negocio
- MD · Links y recursos