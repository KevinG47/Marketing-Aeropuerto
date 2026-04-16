# 🛫 Predicción de Retrasos Aéreos: Estrategia de Marketing Aeroportuario

Este repositorio contiene el análisis de Machine Learning desarrollado para la Dirección de Operaciones y Marketing de nuestro Aeropuerto. 

El objetivo principal es identificar los factores clave de los retrasos aéreos y determinar qué aerolíneas son operativamente más confiables. Con esta información, el aeropuerto lanzará la campaña de marketing **"Socios de Excelencia"**, premiando la puntualidad y mejorando la experiencia de los pasajeros en nuestras salas de espera.

## 🛠️ Tecnologías Utilizadas
* **Entorno:** Docker (Contenedor aislado para evitar problemas de dependencias y memoria).
* **Procesamiento Big Data:** Apache Spark (PySpark) para procesar más de 5.3 millones de registros de vuelos.
* **Modelos de Machine Learning:** Decision Tree Classifier y Random Forest Classifier.

## 📂 Estructura del Proyecto
* `Modulo1_Exploracion.ipynb`: Análisis exploratorio de los datos (EDA) y estadísticas descriptivas.
* `Modulo2_Preparacion.ipynb`: Limpieza de datos, balanceo y Feature Engineering (Vector Assembler, StringIndexer).
* `Modulo3_Modelos.ipynb`: Entrenamiento de los algoritmos y evaluación de Feature Importance.
* `Modulo4_Evaluacion.ipynb`: Evaluación de métricas (Accuracy, F1-Score, AUC-ROC), matrices de confusión y ajuste estratégico del umbral de decisión.

## 📊 Hallazgos Principales para Negocio
1. **El Efecto Dominó (`DEP_HOUR`):** La hora programada de salida explica la mayor parte de los retrasos. Los vuelos de la tarde y noche son críticos.
2. **El Factor Aerolínea (`AIRLINE_idx`):** A través del modelo de Random Forest, comprobamos que la aerolínea tiene un **17% de impacto** en la predicción de retrasos, lo que justifica nuestra campaña para promocionar a las aerolíneas más puntuales (Southwest, American Airlines, United, JetBlue y Spirit).
3. **Ajuste Preventivo (Threshold Tuning):** Al ajustar la sensibilidad del modelo del 50% al 40%, logramos reducir los "Falsos Negativos", permitiendo al aeropuerto anticipar retrasos y salvar a más de **35,000 pasajeros** de sorpresas desagradables.

