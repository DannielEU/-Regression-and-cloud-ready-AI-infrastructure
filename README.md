# Modelado de Luminosidad Estelar mediante Regresión

Este proyecto implementa modelos de regresión para predecir la luminosidad de estrellas basándose en características físicas como la masa y la temperatura efectiva.

## Descripción General

El trabajo contiene dos notebooks que van desde un modelo lineal simple hasta modelos polinómicos multivariables:

1. **Part 1 - Regresión Lineal Simple**: Modela la relación entre masa estelar y luminosidad
2. **Part 2 - Regresión Polinómica**: Extiende el modelo para capturar efectos no lineales e interacciones entre masa y temperatura

## Notebooks

###  01_part1_linreg_1feature.ipynb
**Regresión lineal simple para luminosidad estelar**

- Implementa regresión lineal desde primeros principios: $\hat{L} = w \cdot M + b$
- Modela la luminosidad estelar (L) como función de la masa estelar (M)
- Utiliza error cuadrático medio (MSE) como función de costo
- Analiza la superficie de costo J(w,b)
- Implementa optimización con descenso de gradiente
- Calcula métricas de rendimiento (MSE, RMSE, R²)
- Presenta limitaciones del modelo lineal en datos no lineales

###  02_part2_polyreg.ipynb
**Regresión polinómica multivariable para luminosidad estelar**

- Extiende el modelo a características múltiples: masa (M) y temperatura efectiva (T)
- Feature engineering con polinomios e interacciones:
  - Modelo M1: [M, T]
  - Modelo M2: [M, T, M²]
  - Modelo M3: [M, T, M², M·T]
- Implementa normalización de features para estabilidad numérica
- Compara rendimiento de modelos con complejidad creciente
- Evalúa el trade-off entre underfitting y overfitting
- Analiza el impacto de variables adicionales en la predicción

## Datos

Dataset de estrellas reales con 10 muestras:
- **Masa estelar (M)**: 0.6 - 2.4 unidades solares
- **Temperatura efectiva (T)**: 3800 - 9200 K
- **Luminosidad (L)**: 0.15 - 35.0 unidades solares (variable objetivo)

## Requisitos

```
numpy
matplotlib
```

## Ejecución

1. Abrir los notebooks en Jupyter Notebook o VS Code con extensión de Jupyter
2. Ejecutar las celdas en orden secuencial
3. Los resultados incluyen visualizaciones y métricas de rendimiento

## Resultados Esperados

- Gráficos de datos originales y predicciones del modelo
- Superficies de costo para visualizar la optimización
- Comparación de modelos (MSE, RMSE, R²)
- Análisis del ajuste del modelo a los datos

## AWS SageMaker

Este proyecto fue ejecutado en AWS SageMaker. Las evidencias de ejecución se encuentran en las imágenes adjuntas:

![Ejecución Notebook 1](image.png)
![Ejecución Notebook 1 (cont)](image-1.png)
![Ejecución Notebook 2](image-2.png)

## Autor

Trabajo de Ciencia de Datos - Regresión Lineal y Polinómica
Febrero 2026