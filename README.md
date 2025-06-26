# Diagnóstico de Enfermedades por Texto e Imágenes

Este repositorio contiene un proyecto de diagnóstico de enfermedades utilizando técnicas de Machine Learning y Deep Learning. El sistema permite realizar predicciones a partir de **datos estructurados en texto** y **análisis de imágenes médicas**:

- **Diagnóstico por texto**: Predicción de cáncer de tiroides.
- **Diagnóstico por imágenes**: Clasificación de cáncer de piel.

---

## 📄 Diagnóstico a partir de texto (Cáncer de Tiroides)

### Exploración y Preprocesamiento

Antes del modelado, se ha llevado a cabo un análisis exploratorio exhaustivo de los datos con el fin de:

- Identificar valores atípicos o inconsistencias.
- Eliminar datos faltantes o irrelevantes.
- Transformar características categóricas y numéricas para optimizar el rendimiento de los modelos.

### Modelos Utilizados

#### 1. **LightGBM (Light Gradient Boosting Machine)**

LightGBM es un algoritmo de **Gradient Boosting** desarrollado por Microsoft, optimizado para rendimiento y velocidad en grandes volúmenes de datos. Su funcionamiento se basa en:

- Construcción de árboles de decisión de forma **hoja a hoja** (leaf-wise) en lugar de nivel a nivel.
- Uso eficiente de memoria.
- Soporte para paralelización y GPU.

Ventajas clave:
- Excelente rendimiento en tareas tabulares.
- Menor tiempo de entrenamiento frente a otros métodos como XGBoost.

#### 2. **Red Neuronal Profunda con PyTorch**

Se ha implementado una red neuronal usando **PyTorch**, un framework de deep learning flexible y eficiente. Las redes neuronales utilizadas se componen de:

- Capas densas (fully connected).
- Funciones de activación no lineales como ReLU.
- Regularización mediante Dropout.
- Optimización con algoritmos como Adam.

**¿Cómo funciona una red neuronal?**

- Cada capa transforma los datos de entrada a una representación más abstracta.
- El entrenamiento ajusta los pesos internos mediante retropropagación y descenso de gradiente.
- El modelo aprende patrones complejos y relaciones no lineales entre variables.

---

## 🖼️ Diagnóstico por imagen (Cáncer de Piel)

Se ha entrenado un modelo de clasificación de imágenes médicas para identificar posibles casos de cáncer de piel a partir de fotografías dermatoscópicas.

- Las imágenes han sido preprocesadas (escalado, normalización, aumentos de datos).
- Se han utilizado arquitecturas de redes convolucionales (CNN) como base.
- El entrenamiento se realiza también en PyTorch, aprovechando sus capacidades para visión computacional.

---
