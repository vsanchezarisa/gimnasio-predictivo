# GymChurn Predictor: Sistema Inteligente de Retención de Socios 🏋️‍♂️📊

## 📋 Descripción del Proyecto
Este proyecto de fin de curso para el ciclo de **IA y Big Data** tiene como objetivo predecir la probabilidad de baja de los socios de un gimnasio. Utilizando técnicas de **Machine Learning** y procesamiento de **Big Data**, el sistema identifica patrones de comportamiento (asistencia, perfil demográfico y tipo de cuota) para generar alertas tempranas y facilitar acciones de retención automatizadas.

## 🛠️ Stack Tecnológico
* **Lenguaje:** Python (Pandas, Scikit-learn, XGBoost/LightGBM).
* **Almacenamiento/Procesamiento:** SQL para la base de datos de usuarios y Python para ETL de archivos Excel.
* **Visualización:** Power BI para el dashboard de análisis exploratorio y resultados.
* **IA Generativa:** LLM (vía API o local) para la generación de campañas de marketing personalizadas.
* **Gestión:** Jira (Metodología Ágil) y GitHub (Control de versiones).

## 📂 Estructura de Datos
El modelo se nutre de tres fuentes principales:
1.  **Dataset de Altas:** Información demográfica y contractual de socios activos.
2.  **Dataset de Bajas (2024-2025):** Histórico de socios que abandonaron el centro.
3.  **Registros de Acceso (Lunes-Domingo):** Datos de actividad diaria durante 2024 y 2025 (crucial para medir la frecuencia de uso).

## ⚙️ Arquitectura del Sistema
El flujo de trabajo se divide en cuatro fases:
1.  **ETL & Limpieza:** Unificación de los 7 archivos de accesos y cruce con datos de socios.
2.  **Ingeniería de Variables (Feature Engineering):** Creación de métricas como "días desde la última visita", "frecuencia semanal media" y "antigüedad".
3.  **Modelado:** Entrenamiento y comparativa de modelos de clasificación (Random Forest, Gradient Boosting, etc.).
4.  **Automatización:** Trigger periódico que analiza la base de datos activa y genera un informe de riesgo.

## 🤖 Implementación de LLM
Integración de un modelo de lenguaje para transformar el **% de probabilidad de baja** en comunicaciones personalizadas (emails/notificaciones) que incentiven al socio a volver, basándose en su perfil específico.
