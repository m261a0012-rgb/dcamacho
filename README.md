# Implementación y análisis comparativo de paradigmas de aprendizaje automático

Actividad 1.2 · Unidad 1 · Aprendizaje Automático Avanzado · Maestría en Inteligencia Artificial, TecNM Virtual

**Autores:** Arturo Pérez y María D. Camacho · **Fecha:** octubre de 2026 · **Versión del modelo:** v1.0

## Proyecto

| Paradigma | Caso de estudio | Dataset o entorno | Modelos |
|---|---|---|---|
| Supervisado | Diagnóstico de enfermedad coronaria | Heart Disease (UCI, id 45): 303 pacientes, 13 características | SVM y red neuronal |
| No supervisado | Segmentación de clientes | Wholesale customers (UCI, id 292): 440 clientes, 6 características | PCA y K-means |
| Por refuerzo | Taxi autónomo | Entorno Taxi de Gymnasium | Q-Learning (programa base de la unidad) |

## Abrir en Google Colab

| Notebook | Abrir |
|---|---|
| 00 · Réplica de los ejemplos de la unidad | [![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/artperezg/AA_Actividad1.2_Paradigmas/blob/main/notebooks/00_replica_unidad1.ipynb) |
| 01 · Aprendizaje supervisado | [![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/artperezg/AA_Actividad1.2_Paradigmas/blob/main/notebooks/01_supervisado_SVM_y_RedNeuronal.ipynb) |
| 02 · Aprendizaje no supervisado | [![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/artperezg/AA_Actividad1.2_Paradigmas/blob/main/notebooks/02_no_supervisado_PCA_KMeans.ipynb) |
| 03 · Aprendizaje por refuerzo | [![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/artperezg/AA_Actividad1.2_Paradigmas/blob/main/notebooks/03_refuerzo_QLearning_Taxi.ipynb) |

En Colab, usar *Entorno de ejecución → Ejecutar todas*. La primera celda descarga este repositorio; no requiere Google Drive. El notebook 00 pide subir `dataset_cibersuicidio.csv` (recursos de la Unidad 1), que no se publica aquí por ser material del curso.

## Ubicación de cada punto de la actividad

| Punto de la actividad | Ubicación |
|---|---|
| Tarea 1 · Revisión y réplica de los ejemplos | Notebook 00 |
| Tarea 2 · Selección de casos de estudio y datasets | Sección 1 de los notebooks 01, 02 y 03 |
| Tarea 3 · Supervisado: preparación, entrenamiento y evaluación | Notebook 01, secciones 2, 3 y 4 |
| Tarea 4 · No supervisado: variables, PCA, K-means, agrupaciones y métricas | Notebook 02, secciones 1 a 6 |
| Tarea 5 · Refuerzo: entorno, programa base, recompensa acumulada y ajuste de α | Notebook 03, secciones 1 a 5 |
| Tarea 6 · Análisis comparativo | Reporte PDF (evidencias en el notebook 01, sección 5) |
| Tarea 7 · Organización y entrega | Este repositorio y reporte PDF |

## Versión del modelo (v1.0)

| Modelo | Configuración | Resultado |
|---|---|---|
| SVM | Kernel RBF, C = 1, γ = 0.01 | Exactitud 0.882 y F1 0.870 en prueba |
| Red neuronal | 1 capa oculta de 8 neuronas, α = 3 | Exactitud 0.855 y F1 0.849 en prueba |
| PCA + K-means | 2 componentes (70.2 % de la varianza), k = 2 | Silueta 0.296 |
| Q-Learning | α = 0.10, γ = 0.99, 15 000 episodios | 100 % de éxito en evaluación |

## Estructura

- `data/raw/`: datasets originales · `data/processed/`: datasets limpios y transformados
- `notebooks/`: código (00 a 03)
- `resultados/`: gráficas, métricas (CSV) y modelos entrenados
- `requirements.txt`: librerías utilizadas

## Referencias

Cardoso, M. (2014). *Wholesale customers* [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5030X

Janosi, A., Steinbrunn, W., Pfisterer, M., & Detrano, R. (1989). *Heart Disease* [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C52P4X

Towers, M., Kwiatkowski, A., Terry, J., Balis, J. U., De Cola, G., Deleu, T., Goulão, M., Kallinteris, A., Krimmel, M., KG, A., Perez-Vicente, R., Pierré, A., Schulhoff, S., Tai, J. J., Tan, H., & Younis, O. G. (2024). *Gymnasium: A standard interface for reinforcement learning environments* (arXiv:2407.17032). arXiv. https://doi.org/10.48550/arXiv.2407.17032
