# 📊 Telecom Inefficient Operators Detection


### 🇺🇸 English Version

## 📌 Project Overview

CallMeMaybe, a virtual telephony provider, faced a key operational challenge: lack of visibility into operator performance.

This project transforms raw call data into a performance monitoring framework to identify inefficient operators and support data-driven decision-making.

An operator is considered inefficient if they:

* Miss a high number of incoming calls
* Have long waiting times
* Perform an abnormally low (or high) number of outgoing calls

Additionally, the project validates a business hypothesis:

   <i>"The percentage of inefficient operators is the same across all tariff plans."</i>


### 🎯 Business Objectives
* Define measurable thresholds for operator performance:
   * Minimum outgoing calls per day
   * Maximum acceptable waiting time
   * Maximum missed incoming calls
*Detect inefficient operators at scale
*Compare inefficiency rates across tariff plans (A, B, C)
*Provide actionable insights for operational improvement


### 📂 Datasets
1. telecom_dataset_us.csv
* Call-level data (direction, duration, missed calls, etc.)
2. telecom_clients_us.csv
* Client data (tariff plan, registration date)


### 🧹 Data Preprocessing
* Removed ~4,900 duplicate records
* Handled missing values (excluded ~8,000 records without operator_id)
* Corrected data types (dates, IDs, booleans)
* Feature engineering:
   * Waiting time = total_call_duration – call_duration
* Merged datasets for enriched analysis
* Filtered outliers to ensure reliable metrics


### 📊 Analytical Approach

1. Exploratory Data Analysis (EDA)

* Distribution of calls, durations, and waiting times
* Detection of anomalies and skewed data

2. Inefficiency Definition (KPIs)
Operators classified as inefficient if:
* 📉 Outgoing calls < 10 or > 50 per day
* ⏳ Waiting time ≥ 99 seconds
* ❌ Missed calls > 1 per day

3. Hypothesis Testing
* Compared inefficiency rates across tariff plans
* Statistical test: Z-test for proportions
* Applied Bonferroni correction to control Type I error


### 📈 Key Results
* 🚨 ~26% of operators identified as inefficient (281 / 1084)
* 📉 Inefficiency is not evenly distributed across plans

Plan	Inefficiency Rate
A	      35.2%
B	      23.5%
C	      20.4%

* 📊 All differences are statistically significant
* ⚠️ Plan A shows consistently worse performance


### 💡 Business Impact
* Enables data-driven operator monitoring
* Reduces missed calls and waiting times
* Highlights performance gaps across pricing plans
* Serves as a foundation for:
   * Performance dashboards
   * Alert systems for supervisors
   * Future predictive models


### 🛠️ Technologies Used
* Python
* Pandas
* NumPy
* Matplotlib / Seaborn
* SciPy
* Jupyter Notebook


#### 🚀 How to Run
- git clone <repo_url>
- cd telecom-project
- pip install -r requirements.txt
- jupyter notebook telecom-project.ipynb

### 🇪🇸 Versión en Español
## 📌 Descripción del Proyecto

CallMeMaybe, proveedor de telefonía virtual, enfrentaba un problema clave: falta de visibilidad sobre el rendimiento de sus operadores.

Este proyecto convierte datos de llamadas en un sistema de evaluación de desempeño, permitiendo identificar operadores ineficaces y mejorar la toma de decisiones.

Un operador se considera ineficaz si:

* Pierde muchas llamadas entrantes
* Tiene tiempos de espera elevados
* Realiza pocas (o demasiadas) llamadas salientes

Además, se evalúa la hipótesis:

<i>"El porcentaje de operadores ineficaces es igual en los tres tipos de tarifa."</i>

### 🎯 Objetivos de Negocio
* Definir umbrales claros de rendimiento:
   * Mínimo de llamadas salientes por día
   * Tiempo máximo de espera aceptable
   * Máximo de llamadas perdidas
* Identificar operadores ineficaces
* Comparar el rendimiento entre planes tarifarios
* Generar insights accionables


### 📂 Datasets
1. telecom_dataset_us.csv
* Datos de llamadas
2. telecom_clients_us.csv
* Información de clientes (plan, fecha de alta)


### 🧹 Preprocesamiento de Datos
* Eliminación de duplicados (~4.900 registros)
* Exclusión de registros sin operador (~8.000)
* Corrección de tipos de datos
* Ingeniería de variables:
   * Tiempo de espera = duración total – duración de llamada
* Unión de datasets
* Eliminación de valores atípicos


### 📊 Enfoque Analítico

1. Análisis Exploratorio (EDA)
* Distribuciones de llamadas, duracion y tiempo de espera
* Detección de anomalías y datos sesgados.

2. Definición de Ineficiencia (KPIs)
Un operador es ineficaz si:
* 📉 <10 o >50 llamadas salientes/día
* ⏳ ≥99 segundos de espera
* ❌ >1 llamada perdida/día

3. Prueba de Hipótesis
* Comparación entre planes (A, B, C)
* Test estadístico: Z-test de proporciones
* Corrección de Bonferroni


### 📈 Resultados Clave
* 🚨 ~26% de operadores ineficaces
* 📉 La ineficiencia no está distribuida equitativamente entre planes

Plan	% Ineficiencia
A	      35.2%
B	      23.5%
C	      20.4%

* 📊 Todas las diferencias son estadisticamente significativas
* ⚠️ El Plan A presenta el peor rendimiento


### 💡 Impacto en el Negocio
* Monitoreo automatizado de operadores
* Reducción de tiempos de espera y llamadas perdidas
* Insights estratégicos sobre planes tarifarios
* Sirve de base para:
   * Paneles de control de rendimiento
   * Sistemas de alerta para supervisores
   * Modelos predictivos futuros


### 🛠️ Tecnologías Utilizadas
* Python
* Pandas
* NumPy
* Matplotlib / Seaborn
* SciPy
* Jupyter Notebook

### 🚀 Cómo Ejecutarlo

- git clone <repo_url>
- cd telecom-project
- pip install -r requirements.txt
- jupyter notebook telecom-project.ipynb