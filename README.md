# MedicalTreatment_LogisticRegression
# 🏥 Análisis Predictivo de Supervivencia de Pacientes con PNL

Este proyecto de ciencia de datos tiene como objetivo construir y evaluar un modelo de **Regresión Logística** para predecir la probabilidad de supervivencia a un año de pacientes sometidos a tratamientos médicos. El análisis se desarrolla en dos fases principales:

1.  **Fase 1:** Creación de un modelo base utilizando únicamente datos clínicos estructurados.
2.  **Fase 2:** Mejora del modelo inicial incorporando características extraídas de comentarios de pacientes mediante técnicas de **Procesamiento de Lenguaje Natural (PNL)**.

---

## 📊 Estructura del Proyecto

El flujo de trabajo sigue el ciclo de vida estándar de un proyecto de ciencia de datos:

* **Análisis Exploratorio de Datos (EDA):** Comprensión inicial de las variables, identificación de valores atípicos y análisis de las variables de texto (distribución de sentimientos, nubes de palabras).
* **Limpieza y Preprocesamiento de Datos:** Manejo de valores nulos y atípicos para asegurar la calidad de los datos.
* **Ingeniería de Características:**
    * Codificación de variables categóricas (One-Hot, Binary Encoding).
    * Extracción de características del texto de los pacientes.
* **Modelado:** Construcción y entrenamiento de un modelo de Regresión Logística.
* **Evaluación del Modelo:** Medición del rendimiento del modelo en un conjunto de prueba utilizando métricas como la matriz de confusión, el reporte de clasificación y la curva ROC/AUC.

---

## 🤖 Fase 2: Mejora del Modelo con PNL

La segunda fase del proyecto se centra en enriquecer el modelo extrayendo insights de la columna `patient_comment`. El objetivo es capturar la percepción y experiencia del paciente como una señal predictiva adicional. Las técnicas de PNL utilizadas incluyen:

* **Preprocesamiento de Texto:**
    * **Tokenización:** División de los comentarios en palabras individuales (tokens).
    * **Lematización:** Reducción de las palabras a su forma raíz para estandarizar el vocabulario (ej. "medicamentos", "medicamento" -> "medicamento").
* **Extracción de Características de Texto:**
    * **Bag-of-Words (`CountVectorizer`):** Representación del texto basada en la frecuencia de las palabras.
    * **TF-IDF (`TfidfVectorizer`):** Ponderación de la importancia de las palabras, dando más peso a los términos que son distintivos de un comentario.
    * **N-gramas:** Captura de secuencias de palabras (ej. "efectos secundarios", "sentí mejor") para añadir contexto.

---

## 🛠️ Tecnologías Utilizadas

* **Lenguaje:** `Python 3`
* **Librerías Principales:**
    * `Pandas` y `NumPy` para la manipulación de datos.
    * `Scikit-learn` para el modelado, preprocesamiento y métricas de evaluación.
    * `Matplotlib` y `Seaborn` para la visualización de datos.
    * `NLTK` o `spaCy` para las tareas de lematización y tokenización.
    * `WordCloud` para el análisis exploratorio de texto.

---

## 🚀 Cómo Utilizar este Repositorio

1.  **Clonar el repositorio:**
    ```bash
    git clone [https://github.com/tu-usuario/nombre-del-repositorio.git](https://github.com/tu-usuario/nombre-del-repositorio.git)
    ```
2.  **Instalar las dependencias:**
    ```bash
    pip install -r requirements.txt
    ```
