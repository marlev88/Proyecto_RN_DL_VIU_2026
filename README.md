# Proyecto_RN_DL_VIU_2026
Proyecto académico de Redes Neuronales y Deep Learning (VIU, 2026). Clasificación de imágenes mediante CNN propias, Transfer Learning y Fine-Tuning con MobileNetV2 y ResNet50. Comparación experimental de nueve modelos sobre TensorFlow Flowers.

# Clasificación de imágenes mediante Redes Neuronales Convolucionales

**Proyecto de Programación — Redes Neuronales y Deep Learning**  
**Máster Universitario en Inteligencia Artificial**  
**Universidad Internacional de Valencia (VIU), 2026**

## 1. Descripción del proyecto

Este repositorio contiene los resultados experimentales de un proyecto académico orientado a la clasificación multiclase de imágenes mediante redes neuronales convolucionales (CNN).

El objetivo principal es comparar modelos CNN desarrollados desde cero con arquitecturas preentrenadas, utilizando técnicas de regularización, aumento de datos (*Data Augmentation*), transferencia de aprendizaje (*Transfer Learning*) y ajuste fino (*Fine-Tuning*).

Se implementaron y evaluaron nueve configuraciones experimentales utilizando TensorFlow y Keras en Google Colab.

## 2. Conjunto de datos

Se utilizó **TensorFlow Flowers**, un conjunto de 3.670 imágenes clasificadas en cinco categorías:

- Daisy
- Dandelion
- Roses
- Sunflowers
- Tulips

El conjunto de datos se dividió de forma estratificada:

| Partición | Imágenes |
|---|---:|
| Entrenamiento (70 %) | 2.569 |
| Validación (15 %) | 550 |
| Prueba (15 %) | 551 |

Las imágenes fueron redimensionadas a 160 × 160 píxeles.

## 3. Experimentos realizados

| Experimento | Arquitectura o estrategia |
|---|---|
| E1 | CNN básica desarrollada desde cero |
| E2 | CNN con regularización, BatchNormalization y Dropout |
| E2b | CNN mejorada sin BatchNormalization |
| E3 | CNN con Data Augmentation |
| E3b | CNN con aumento de datos moderado |
| E4 | MobileNetV2 con Transfer Learning |
| E5 | MobileNetV2 con Fine-Tuning |
| E6 | ResNet50 con Transfer Learning |
| E7 | ResNet50 con Fine-Tuning |

Las configuraciones fueron comparadas mediante métricas de clasificación, curvas de aprendizaje y análisis del comportamiento durante el entrenamiento.

## 4. Resultados principales

Los modelos se evaluaron sobre un conjunto de prueba independiente de 551 imágenes.

| Modelo | Accuracy | F1-score macro |
|---|---:|---:|
| E7 | **91,83 %** | **0,9194** |
| E5 | 89,47 % | 0,8945 |
| E6 | 89,47 % | 0,8945 |
| E4 | 88,57 % | 0,8844 |
| E2b | 69,33 % | 0,6883 |
| E1 | 66,97 % | 0,6629 |
| E3 | 54,45 % | 0,5356 |
| E3b | 55,17 % | 0,5189 |
| E2 | 24,50 % | 0,0787 |

El mejor rendimiento se obtuvo mediante **ResNet50 con Fine-Tuning (E7)**, alcanzando un accuracy de **91,83 %** y un F1-score macro de **0,9194**.

Estos resultados muestran que, en las condiciones experimentales utilizadas, las arquitecturas preentrenadas superaron a las CNN desarrolladas desde cero.

## 5. Organización del repositorio

```text
Experimentos/
├── datos/
├── E1/
├── E2/
├── E2b/
├── E3/
├── E3b/
├── E4/
├── E5/
├── E6/
├── E7/
├── Evaluacion_Final/
├── comparacion_CNN_propias.csv
└── comparacion_CNN_propias.png
```

**Contenido de las carpetas:**

- `datos/`: particiones del conjunto de datos y visualizaciones exploratorias.
- `E1/` a `E7/`: historiales de entrenamiento y figuras correspondientes a cada configuración experimental, incluyendo E2b y E3b.
- `Evaluacion_Final/`: métricas comparativas de los nueve modelos sobre el conjunto de prueba.
- `comparacion_CNN_propias.csv` y `.png`: resultados comparativos de los modelos CNN desarrollados desde cero.

## 6. Herramientas utilizadas

- Python
- TensorFlow y Keras
- Google Colab
- NumPy y Pandas
- Scikit-learn
- Matplotlib

## 7. Alcance del repositorio

Este repositorio tiene una finalidad académica y contiene principalmente los resultados experimentales del proyecto.

El notebook completo, con el código fuente, las salidas ejecutadas, las decisiones metodológicas, los análisis y las conclusiones, se entrega directamente a través de la plataforma académica de la Universidad Internacional de Valencia.

Los archivos de los modelos entrenados (`.keras`) y el conjunto completo de imágenes no se incluyen en este repositorio.

Los archivos CSV de partición conservan las rutas utilizadas en Google Colab, por lo que pueden requerir adaptación para utilizarse en otro entorno.

## 8. Autor

**Marcos Lévano Huamaccto**  
Grupo 23  
Máster Universitario en Inteligencia Artificial  
Universidad Internacional de Valencia (VIU)  
2026

---

*Repositorio académico de resultados experimentales en clasificación de imágenes mediante Deep Learning.*
