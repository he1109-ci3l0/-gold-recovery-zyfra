# Recuperación de oro · Zyfra

Modelo de machine learning que predice el coeficiente de recuperación de oro
a partir de los parámetros del proceso de extracción y purificación.
Proyecto de ciencia de datos · dataset proporcionado por Zyfra (TripleTen).

## Objetivo
Predecir dos objetivos —`rougher.output.recovery` y `final.output.recovery`—
y evaluar con sMAPE final = 25% · rougher + 75% · final.

## Datos
Los CSV no se incluyen en el repo. Descargar y colocar en `data/`:
- `gold_recovery_train.csv`
- `gold_recovery_test.csv`
- `gold_recovery_full.csv`

## Estructura
- `data/` — datasets crudos (no versionados)
- `notebooks/` — notebook-reporte del análisis
- `src/` — código modular (carga, métrica sMAPE, modelos)
- `reports/figures/` — gráficas del EDA
- `docs/` — case study para GitHub Pages

## Entorno
conda env create -f environment.yml
conda activate gold-recovery-zyfra

## Métrica
sMAPE final = 25% · sMAPE(rougher) + 75% · sMAPE(final)