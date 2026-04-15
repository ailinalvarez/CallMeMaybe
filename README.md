# 📊 Telecom Inefficient Operators Detection

---

## 🇺🇸 English Version

### 📌 Project Overview

This project analyzes telecommunications data from the virtual telephony service **CallMeMaybe** to identify **inefficient operators** based on their performance metrics.

An operator is considered inefficient if they:

* Miss a high number of incoming calls
* Have long waiting times on incoming calls
* Perform a low number of outgoing calls (when expected)

Additionally, the project evaluates the following hypothesis:

> *"The percentage of inefficient operators is the same across all tariff plans."*

---

### 🎯 Objectives

* Define thresholds for:

  * Minimum outgoing calls per day
  * Maximum acceptable waiting time
  * Maximum number of missed incoming calls
* Identify inefficient operators based on these criteria
* Compare inefficiency rates across tariff plans

---

### 📂 Datasets

1. **telecom_dataset_us.csv**

   * Call-level data (direction, duration, missed calls, etc.)

2. **telecom_clients_us.csv**

   * Client information (tariff plan, registration date)

---

### 🧹 Data Preprocessing

* Data type corrections (dates, IDs, booleans)
* Handling missing values
* Removing duplicates (~4900 records)
* Feature engineering:

  * Waiting time calculation
* Dataset merging

---

### 📊 Analysis Performed

* Exploratory Data Analysis (EDA)
* Definition of inefficiency criteria
* Aggregation of operator performance metrics
* Hypothesis testing across tariff plans

---

### 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib / Seaborn
* Jupyter Notebook

---

### 📈 Key Insights

* Identification of operator behavior patterns
* Clear segmentation between efficient and inefficient operators
* Statistical comparison across tariff plans

---

### 🚀 How to Run

1. Clone the repository
2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```
3. Open the notebook:

   ```bash
   jupyter notebook telecom-project.ipynb
   ```

---

## 🇪🇸 Versión en Español

### 📌 Descripción del Proyecto

Este proyecto analiza datos de telecomunicaciones del servicio de telefonía virtual **CallMeMaybe** para identificar **operadores ineficaces** según su rendimiento.

Un operador se considera ineficaz si:

* Pierde una gran cantidad de llamadas entrantes
* Presenta tiempos de espera prolongados
* Realiza pocas llamadas salientes (cuando se espera que lo haga)

Además, se evalúa la hipótesis:

> *"El porcentaje de operadores ineficaces es igual en los tres tipos de tarifa."*

---

### 🎯 Objetivos

* Definir umbrales para:

  * Número mínimo de llamadas salientes por día
  * Tiempo máximo de espera
  * Número máximo de llamadas entrantes perdidas
* Identificar operadores ineficaces
* Comparar la ineficiencia entre planes tarifarios

---

### 📂 Datasets

1. **telecom_dataset_us.csv**

   * Datos de llamadas

2. **telecom_clients_us.csv**

   * Información de clientes

---

### 🧹 Preprocesamiento de Datos

* Corrección de tipos de datos
* Tratamiento de valores nulos
* Eliminación de duplicados (~4900 registros)
* Ingeniería de características:

  * Cálculo del tiempo de espera
* Unión de datasets

---

### 📊 Análisis Realizado

* Análisis exploratorio (EDA)
* Definición de criterios de ineficiencia
* Agregación de métricas por operador
* Prueba de hipótesis

---

### 🛠️ Tecnologías Utilizadas

* Python
* Pandas
* NumPy
* Matplotlib / Seaborn
* Jupyter Notebook

---

### 📈 Resultados Clave

* Identificación de patrones de comportamiento
* Clasificación de operadores eficientes vs ineficaces
* Comparación estadística entre tarifas

---

### 🚀 Cómo Ejecutarlo

1. Clonar el repositorio
2. Instalar dependencias
3. Ejecutar el notebook

