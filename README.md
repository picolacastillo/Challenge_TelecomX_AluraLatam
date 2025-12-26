Markdown

# 🚀 Challenge Telecom X: Análisis de Evasión de Clientes (Churn)

**Estado del Proyecto:** Finalizado ✅

Este proyecto analiza el comportamiento de los clientes de una empresa de telecomunicaciones para reducir la fuga de usuarios. Utilizando **Python** y técnicas de **Análisis Exploratorio de Datos (EDA)**, identifiqué que la estabilidad contractual y los costos mensuales son los principales disparadores de evasión.

**Herramientas utilizadas:** Python, Pandas, Seaborn, Matplotlib, API REST.

---

## 📂 Estructura del Proyecto

├── data/          # Archivos de datos (CSV, JSON)
├── notebooks/     # Notebooks de Google Colab (.ipynb)
├── reports/       # Gráficos exportados e informes finales
└── README.md      # Descripción general del proyecto

## 🛠️ Tecnologías Utilizadas
- **Lenguaje:** Python
- **Librerías principales:** pandas, requests
- **Entorno:** Google Colab
- **Formato de datos:** CSV, JSON

## 📁 Origen de los Datos
Los datos fueron obtenidos de la API de **Telecom X** a través del repositorio de desafíos de **Alura LATAM**.  
Se utilizó la librería **requests** para la ingesta y **pandas** para la estructuración.

## 📊 Campos principales analizados
- **Datos demográficos:** Género, adultos mayores, pareja y dependientes.
- **Servicios contratados:** Internet (DSL/Fibra), seguridad, soporte técnico.
- **Estado de Evasión (Churn):** Variable objetivo que identifica la baja del cliente (Yes/No).

## 🔍 Metodología y Limpieza de Datos

### 1. Limpieza y Preparación
- **Tratamiento de nulos:** Eliminación de registros en *TotalCharges* con 0 meses de antigüedad.
- **Corrección de tipos:** Conversión de datos categóricos a numéricos (*float*) y corrección de texto a número.
- **Integridad:** Eliminación de duplicados y estandarización de categorías.

### 2. Ingeniería de Datos (Feature Engineering)
- **Cuentas_Diarias:** Creación de una métrica de costo diario proporcional (*MonthlyCharges / 30*).
- **Traducción:** Renombramiento de columnas al español para mejorar la accesibilidad.
- **Binarización:** Conversión de la variable *Churn* a formato numérico (0/1).

## 📈 Hallazgos y Resultados Visuales

### Resumen Estadístico
- **Gasto promedio:** Los clientes tienen un cargo mensual promedio de $64.76.
- **Permanencia:** La mediana de la permanencia es de 29 meses.
- **Tasa de evasión:** Se identificó que el 26.5% de los clientes abandonaron el servicio.

### Hallazgos Estratégicos (Insights)
- **Contratos:** Los clientes con contratos *Mes a Mes* son los más propensos a la fuga.
- **Servicios:** Se detectó una correlación positiva entre el uso de **Fibra Óptica** y la tasa de evasión.
- **Sensibilidad al precio:** El grupo de evasión tiene una mediana de cargos mensuales superior.
  
## 🏁 Recomendaciones Finales
- **Incentivos de fidelización:** Fomentar el paso de contratos mensuales a anuales.
- **Foco en el onboarding:** Reforzar el servicio al cliente durante el primer semestre.
- **Revisión de producto:** Analizar la estabilidad y precio de la Fibra Óptica.
