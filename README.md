🚀 Challenge Telecom X: Análisis de Evasión de Clientes (Churn)
Estado del Proyecto: Finalizado ✅

Este proyecto analiza el comportamiento de los clientes de una empresa de telecomunicaciones para reducir la fuga de usuarios. Utilizando Python y técnicas de Análisis Exploratorio de Datos (EDA), identifiqué que la estabilidad contractual y los costos mensuales son los principales disparadores de evasión.

Herramientas utilizadas: Python, Pandas, Seaborn, Matplotlib, API REST.

📂 Estructura del Proyecto
Plaintext

├── data/          # Archivos de datos (CSV, JSON)
├── notebooks/     # Notebooks de Google Colab (.ipynb)
├── reports/       # Gráficos exportados e informes finales
└── README.md      # Descripción general del proyecto
📁 Origen de los Datos
Los datos fueron obtenidos de la API de Telecom X a través del repositorio de desafíos de Alura LATAM. Se utilizó la librería requests para la ingesta y pandas para la estructuración.

📊 Campos principales analizados:
Datos demográficos: Género, adultos mayores, pareja y dependientes.

Servicios contratados: Internet (DSL/Fibra), seguridad, soporte técnico.

Estado de Evasión (Churn): Variable objetivo que identifica la baja del cliente (Yes/No).

🔍 Metodología y Limpieza de Datos
1. Limpieza y Preparación
Tratamiento de Nulos: Eliminación de registros en TotalCharges con 0 meses de antigüedad para evitar sesgos.

Corrección de Tipos: Conversión de datos categóricos a numéricos (float) y corrección de columnas numéricas que venían como texto.

Integridad: Eliminación de duplicados y estandarización de categorías (eliminación de espacios en blanco).

2. Ingeniería de Datos (Feature Engineering)
Cuentas_Diarias: Creación de una métrica de costo diario proporcional (MonthlyCharges / 30).

Traducción: Renombramiento de columnas al español para mejorar la accesibilidad de los hallazgos.

Binarización: Conversión de la variable Churn a formato numérico (0/1) para análisis de correlación.

📈 Hallazgos y Resultados Visuales
Resumen Estadístico
Gasto Promedio: Los clientes tienen un cargo mensual promedio de $[Valor].

Permanencia: La mediana de permanencia es de [Valor] meses.

Tasa de Evasión: Se identificó que el [X]% de los clientes abandonaron el servicio.

Hallazgos Estratégicos (Insights)
Contratos: Los clientes con contratos Mes a Mes son los más propensos a la fuga.

Servicios: Se detectó una correlación positiva entre el uso de Fibra Óptica y la tasa de evasión.

Sensibilidad al Precio: El grupo de evasión tiene una mediana de cargos mensuales superior al grupo que permanece.

Curva de Aprendizaje: Los clientes que cancelan suelen hacerlo en los primeros 6 meses de servicio.

🏁 Recomendaciones Finales
Incentivos de Fidelización: Fomentar el paso de contratos mensuales a anuales mediante descuentos estratégicos.

Foco en el Onboarding: Reforzar el servicio al cliente durante el primer semestre de antigüedad (periodo crítico).

Revisión de Producto: Analizar la estabilidad y el precio del servicio de Fibra Óptica para mejorar la retención.
