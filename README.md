# Tratamiento-de-datos-2025-2026
Proyecto de Tratamiento de datos 2025/2026
# Proyecto TD: Detección de Desinformación y Análisis de Polarización

Repositorio del proyecto de la asignatura **Text Data** (Máster en Ingeniería de Telecomunicación).

## 1. Descripción del problema

El objetivo del proyecto es:

- Detectar automáticamente **contenido desinformativo** en texto (p.ej. rumores, fake news, etc.).
- Analizar su relación con la **polarización** (por ejemplo, a través de emociones, stance o lenguaje extremista).

Se trabajará con un dataset de texto etiquetado, realizando:

- Análisis exploratorio de datos (EDA).
- Distintas representaciones vectoriales del texto.
- Entrenamiento y comparación de varios modelos de clasificación (clásicos y basados en deep learning / Transformers).

## 2. Dataset

> **Nota:** Completar esta sección cuando el dataset esté decidido.

- Nombre del dataset: `TODO`
- Idioma: `TODO`
- Tareas:
  - Clasificación de desinformación / no desinformación.
  - (Opcional) Tareas relacionadas con stance / polarización.

Se incluirá una descripción detallada del dataset y sus licencias en el informe.

## 3. Metodología

### 3.1. Análisis exploratorio (EDA)

- Distribución de clases.
- Longitud de textos.
- Palabras más frecuentes por clase.
- Ejemplos de casos representativos.

### 3.2. Representación del texto

Se utilizarán al menos tres tipos de representaciones:

1. **TF-IDF** (scikit-learn).
2. **Embeddings Word2Vec** (pre-entrenados o entrenados sobre el propio corpus).
3. **Embeddings contextuales** extraídos de un modelo tipo BERT (sin fine-tuning, como features).

### 3.3. Modelos

- **Modelos clásicos (scikit-learn)**  
  - Logistic Regression  
  - Linear SVM (u otros que se consideren adecuados)
- **Red neuronal en PyTorch**  
  - Arquitectura feed-forward sobre embeddings densos.
- **Modelo Transformer fine-tuneado (Hugging Face)**  
  - Modelo base (BERT/RoBERTa/multilingüe) con capa de clasificación.

### 3.4. Evaluación

- División en **train / validation / test**.
- Métricas:
  - Accuracy
  - F1-score (macro y por clase)
  - Matriz de confusión
- Comparación de:
  - Representaciones
  - Modelos clásicos vs PyTorch vs Transformer fine-tuneado

## 4. Estructura del repositorio

```text
.
├── data/                # Dataset (o scripts para descargarlo)
├── notebooks/           # EDA y experimentos exploratorios
├── src/                 # Código fuente (preprocesado, modelos, etc.)
│   ├── preprocessing.py
│   ├── vectorizers.py
│   ├── models_sklearn.py
│   ├── model_pytorch.py
│   └── model_transformer.py
├── scripts/             # Scripts de entrenamiento / evaluación
│   ├── train_baselines.py
│   ├── train_pytorch.py
│   └── train_transformer.py
├── results/             # Resultados, tablas y métricas
├── figures/             # Figuras y gráficas del informe
├── requirements.txt
└── README.md