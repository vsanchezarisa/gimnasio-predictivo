# 🏋️‍♂️ Sistema de Predicción de Bajas y Retención Activa (Gym Churn & GenAI)

## 📌 Descripción del Proyecto
Este proyecto implementa una solución integral de Inteligencia Artificial y Big Data para un centro deportivo. El objetivo principal es anticipar las posibles bajas de socios (Churn Prediction) a partir de datos demográficos y de comportamiento (accesos diarios) y automatizar estrategias de retención personalizadas mediante IA Generativa.

## ⚙️ Arquitectura de la Solución

El proyecto está estructurado en 4 fases principales:

1. **Pipeline de Datos (ETL):** - Integración de registros históricos de altas/bajas de 2024 y 2025.
   - Fusión y procesamiento de logs masivos de accesos diarios mediante `pandas`.
   - Feature Engineering: Creación de variables de comportamiento (frecuencia, recencia, estacionalidad) descartando perfiles anómalos (pases de 1-5 días).

2. **Machine Learning (Predictivo):**
   - Entrenamiento y validación de modelos de clasificación para predecir la probabilidad de baja.
   - Comparación de algoritmos y optimización de hiperparámetros buscando maximizar el Recall y F1-Score.

3. **Automatización y Triggers:**
   - Creación de un entorno simulado de base de datos con usuarios activos.
   - Implementación de un script automatizado que genera un informe periódico (semanal/mensual) con los usuarios en zona de riesgo.

4. **IA Generativa y Visualización (Prescriptivo):**
   - Integración de un LLM que consume el informe de riesgo y redacta correos de retención altamente personalizados basados en el perfil y comportamiento de cada socio.
   - Dashboard interactivo en Power BI para monitorizar el riesgo global de la cartera de clientes.

## 🛠️ Stack Tecnológico
* **Lenguaje:** Python
* **Procesamiento y Análisis:** Pandas, NumPy
* **Machine Learning:** Scikit-Learn / XGBoost / LightGBM
* **Base de Datos:** SQLite / SQLAlchemy (para la simulación del trigger)
* **IA Generativa:** (API del LLM seleccionado)
* **Visualización:** Power BI
* **Gestión y Control:** Jira (Scrum), Git/GitHub

## 📂 Estructura del Repositorio
```text
├── data/           # Datasets crudos y procesados (ignorados en git)
├── notebooks/      # Jupyter Notebooks (EDA, ETL, Modelado)
├── src/            # Scripts de automatización, triggers y conexión con LLM
├── dashboard/      # Archivos de Power BI
├── .gitignore
└── README.md
