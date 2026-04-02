# 📊 SaaS Customer Retention & Revenue Pipeline

## 🎯 1. Business Problem
Este proyecto resuelve la necesidad de una empresa de software (SaaS) de transformar sus datos crudos en decisiones estratégicas. El objetivo principal es reducir la tasa de abandono (*Churn*) y maximizar el *Lifetime Value* de los clientes.

**Preguntas clave de negocio resueltas:**
* **¿Quiénes generan más ingresos?** Identificación de cuentas *Enterprise* con planes Premium.
* **¿Qué patrones indican Churn?** Correlación entre la baja frecuencia de sesiones, el alto volumen de tickets de soporte y la inactividad prolongada.
* **¿Qué segmentos son más rentables?** Análisis comparativo de ingresos vs. costo de soporte por segmento (SMB, Enterprise, Consumer).
* **¿Cómo mejorar la retención?** Implementación de un sistema de alertas tempranas (*Risk Scoring*) para actuar antes de la cancelación.

---

## 🏗️ 2. Arquitectura de Datos (Medallion Architecture)
El proyecto sigue un flujo de ingeniería de datos profesional:

1.  **Bronze Layer (Raw):** Datos crudos en CSV con formatos de fecha inconsistentes, duplicados y valores nulos.
2.  **Silver Layer (Processed):** Pipeline de limpieza en **Python (Pandas)** que normaliza fechas, elimina duplicados, imputa montos de suscripción según el plan y filtra *outliers* de uso.
3.  **Gold Layer (Analytics):** Modelo de datos en **Power BI** con cálculos avanzados en **DAX** para medir la propensión al abandono.

---

## 🛠️ 3. Stack Tecnológico
* **Lenguaje:** Python 3.x (Pandas, OS).
* **Visualización:** Power BI Desktop.
* **Modelado:** DAX (Data Analysis Expressions).
* **Control de Versiones:** Git / GitHub.

---

## 📈 4. Insights Principales
* **Alerta de Churn:** Los clientes con más de **15 días de inactividad** y más de **3 tickets de soporte** abiertos tienen un 80% de probabilidad de cancelar en los próximos 30 días.
* **Segmento Crítico:** El segmento *Consumer* presenta la mayor volatilidad, requiriendo estrategias de automatización de soporte.
* **Oportunidad:** El 15% de los usuarios *Basic* en el segmento *SMB* tienen un uso intensivo, siendo candidatos ideales para campañas de *Upselling* a Premium.

---

## 📂 5. Estructura del Repositorio
* `/data`: Datasets originales (inconsistentes).
* `/data_output`: Datasets limpios listos para análisis.
* `/scripts`: Script de ETL en Python.
* `/dashboard`: Archivo .pbix y capturas del reporte.