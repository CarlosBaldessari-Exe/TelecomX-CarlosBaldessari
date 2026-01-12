📊 Telecom X BR — Análisis de Evasión (Churn)


📌 Descripción del Proyecto

Este repositorio contiene un análisis completo de evasión de clientes (churn) para la empresa Telecom X Brasil, con el objetivo de:

Identificar patrones de cancelación

Detectar los principales factores asociados al churn

Proponer acciones estratégicas de retención

Entregar un dataset limpio y listo para modelado predictivo

El análisis incluye limpieza de datos, exploración visual, análisis estadístico y recomendaciones accionables orientadas al negocio.

🎯 Objetivos

Analizar la tasa de churn y su distribución

Identificar variables clave que explican la evasión

Apoyar decisiones de negocio para reducir churn

Preparar datos finales para el equipo de Machine Learning

🗂️ Estructura del Repositorio
├── data/
│   ├── raw/
│   │   └── TelecomX_Data.json
│   └── processed/
│       └── telecomx_limpo.csv
│
├── notebooks/
│   ├── 01_extracao.ipynb
│   ├── 02_limpeza.ipynb
│   ├── 03_eda.ipynb
│   └── 04_relatorio_final.ipynb
│
├── requirements.txt
└── README.md

🔄 Pipeline de Datos
1️⃣ Extracción

Lectura del dataset vía API (TelecomX_Data.json)

Conversión a DataFrame con pd.json_normalize

2️⃣ Limpieza y Tratamiento

Flatten de estructuras anidadas

Conversión de tipos (Custo_Mensal, Custo_Total)

Tratamiento de valores inválidos y nulos

Eliminación de duplicados

Normalización de categorías textuales

3️⃣ Feature Engineering

Creación de Custo_Diario = Custo_Mensal / 30

Binning de:

Meses_Relacao

Custo_Mensal

Renombrado de columnas a portugués para claridad

El resultado final es el dataset:

📁 data/processed/telecomx_limpo.csv

📊 Análisis Exploratorio (EDA)
Distribución de Churn

Visualización de la proporción de clientes que cancelaron vs activos

Churn por Variables Clave

Género

Tipo de contrato

Método de pago

Tipo de internet

Servicios adicionales (Segurança Online, Suporte Técnico)

Facturación digital

Análisis Numérico

Comparación de:

Meses de relación

Costo mensual

Costo total

Costo diario

Estadísticas descriptivas y boxplots por churn

Correlaciones

Matriz de correlación optimizada

Selección de variables con mayor relación con churn

Creación de variable binaria temporal (Churn_bin) para análisis

🔍 Hallazgos Clave

Contrato mensual (Month-to-month) presenta la mayor tasa de churn

Clientes con baja antigüedad cancelan con mucha más frecuencia

Métodos de pago manuales tienen mayor evasión que pagos automáticos

Menor cantidad de servicios contratados se asocia fuertemente a churn

Costo mensual alto aumenta la probabilidad de cancelación

Costo total alto (clientes antiguos) reduce churn

📌 El engagement (cantidad de servicios) es un predictor más fuerte que el precio.

🧠 Recomendaciones Estratégicas
📉 Reducción de Churn

Incentivar migración de contratos mensuales a anuales

Descuentos, meses gratis o upgrades de velocidad

💳 Pagos Automáticos

Beneficios por activar débito automático

Migración desde métodos manuales

🚀 Onboarding Temprano

Contacto activo en los primeros 30 / 60 / 90 días

Soporte proactivo y tutoriales

📦 Bundles de Servicios

Paquetes con:

Seguridad Online

Soporte Técnico

Descuentos por contratar múltiples servicios

⚠️ Monitor de Riesgo

Score simple basado en:

Tenure bajo

Costo mensual alto

Contrato mensual

Pago manual

Activación temprana del equipo de retención

🧪 Tests A/B

Evaluación de ofertas y mensajes personalizados
