# U4_S14-Tarea-Analisis-Discriminante-LDA-y-QDA-
# Comparación de LDA y QDA - Wine Dataset

Proyecto académico que implementa y compara dos modelos de clasificación estadística, el Análisis Discriminante Lineal (LDA) y el Análisis Discriminante Cuadrático (QDA), utilizando el Wine Dataset sin tratamiento previo (sin normalización ni estandarización).

## Contenido del repositorio

- `LDA_QDA_Wine.ipynb`: cuaderno de Google Colab con el análisis completo, incluyendo exploración de datos, visualizaciones, entrenamiento de LDA y QDA, matrices de confusión, métricas de evaluación, fronteras de decisión y conclusiones.
- `README.md`: este archivo, con instrucciones de ejecución y resumen de hallazgos.

## Conjunto de datos

Este proyecto utiliza el **Wine Dataset**, incluido directamente en la librería `scikit-learn`. No es necesario descargar ningún archivo externo: el dataset se carga automáticamente al ejecutar la siguiente línea dentro del notebook:

```python
from sklearn.datasets import load_wine
wine = load_wine()
```

El dataset contiene 178 observaciones, 13 variables predictoras numéricas (propiedades químicas de vinos) y una variable objetivo con 3 clases (cultivares de uva).

## Cómo ejecutar el proyecto

1. Descargar o clonar este repositorio.
2. Abrir el archivo `U4_S14: Tarea: Análisis Discriminante (LDA y QDA) - Medina Guallo Kelly.ipynb` en [Google Colab](https://colab.research.google.com/drive/12Yy1bjLwIWoHmSxhzRfeXr-GOFgGIpdS?authuser=2#scrollTo=b402d2ce) (recomendado) o en un entorno local con Jupyter Notebook.
3. Si se ejecuta en Colab, no se requiere instalación adicional: las librerías necesarias (`numpy`, `pandas`, `matplotlib`, `seaborn`, `scikit-learn`) ya están disponibles por defecto.
4. Si se ejecuta en un entorno local, instalar las dependencias con:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

5. Ejecutar todas las celdas del notebook en orden (`Entorno de ejecución > Ejecutar todas` en Colab, o `Run All` en Jupyter).

## Resumen de principales hallazgos

Tanto LDA como QDA lograron un desempeño alto sobre el Wine Dataset sin tratamiento, confirmando que las tres clases de vino son razonablemente separables a partir de sus propiedades químicas. LDA generó fronteras de decisión lineales suficientes para clasificar correctamente la mayoría de las observaciones, mientras que QDA, con fronteras cuadráticas más flexibles, obtuvo un desempeño competitivo pero con mayor sensibilidad al tamaño de muestra por clase.

El supuesto de covarianza compartida de LDA no resultó demasiado restrictivo para este dataset, lo que explica que su desempeño fuera comparable al de QDA; las métricas de accuracy, precisión, recall y F1-score fueron muy similares entre ambos modelos, mientras que QDA presentó un tiempo de entrenamiento levemente mayor.

En términos prácticos, LDA resulta preferible cuando se dispone de pocas observaciones por clase o se prioriza la interpretabilidad, mientras que QDA es más adecuado cuando las clases presentan estructuras de covarianza claramente distintas y se cuenta con suficientes datos para estimarlas de forma confiable.

## Autora

Kelly Medina Guallo — Universidad de Guayaquil, Facultad de Ciencias, Matemáticas y Físicas.
