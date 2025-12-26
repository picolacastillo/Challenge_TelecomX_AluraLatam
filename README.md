# Challenge_TelecomX_AluraLatam
Análisis de evasión de clientes utilizando Python y técnicas de EDA.
## 📁 Origen de los Datos

Los datos fueron obtenidos de la API de **Telecom X** a través del repositorio de desafíos de Alura LATAM. Se utilizó la librería `requests` de Python para la ingesta de datos en formato JSON y `pandas` para la estructuración en un DataFrame.

### 📊 Campos principales analizados:
* **Datos demográficos:** Género, ciudadanos mayores, dependientes, etc.
* **Servicios contratados:** Tipo de internet, seguridad online, soporte técnico.
* **Estado de Evasión (Churn):** Identificación de clientes que abandonaron el servicio (Yes/No).

* ## 🔍 Análisis Exploratorio Inicial
Se realizó una inspección de la estructura del dataset identificando:
* **Variables Categóricas:** Datos demográficos y tipos de servicios (Fiber optic, DSL, etc.).
* **Variables Numéricas:** Meses de permanencia (Tenure) y cargos financieros.
* **Calidad de Datos:** Verificación de tipos mediante `df.info()` y detección de inconsistencias en columnas numéricas que venían como texto.

## 🛠️ Proceso de Limpieza
Para garantizar la fiabilidad de los resultados, se realizaron las siguientes acciones:
* **Tratamiento de Nulos:** Se identificaron valores faltantes en `TotalCharges` derivados de clientes con 0 meses de antigüedad; se optó por eliminarlos para evitar sesgos financieros.
* **Corrección de Tipos:** Conversión de variables de tipo *object* a *float* para permitir cálculos estadísticos.
* **Integridad:** Eliminación de registros duplicados y validación de consistencia en etiquetas de servicios.

## ⚙️ Ajuste y Coherencia de Datos
Tras la limpieza inicial, se aplicaron ajustes estructurales:
* **Estandarización de Categorías:** Eliminación de espacios en blanco y corrección de etiquetas inconsistentes.
* **Ingeniería de Características Simple:** Creación de una versión numérica de la variable `Churn` para facilitar el análisis de correlación.
* **Validación Final:** Verificación de que el 100% de los registros sean coherentes y estén listos para la visualización.

* ## 💡 Ingeniería de Datos (Feature Engineering)
Se incorporó una nueva variable métrica para enriquecer el análisis:
* **Cuentas_Diarias:** Cálculo del costo diario por cliente derivado de la facturación mensual (`MonthlyCharges / 30`).
* **Propósito:** Esta métrica permite comparar el impacto del gasto diario en la lealtad del cliente y facilita análisis de sensibilidad en la facturación.

* ## 🌐 Estandarización y Comunicación
* **Traducción de Variables:** Se renombraron las columnas al español para mejorar la accesibilidad de los hallazgos ante stakeholders hispanohablantes.
* **Codificación Binaria:** Transformación de la variable `Churn` a formato numérico (0/1), preparando el dataset para futuros modelos de Machine Learning y cálculos de correlación.

* ## 📊 Resumen Estadístico y Hallazgos
Tras realizar el análisis descriptivo, se identificaron los siguientes puntos:
* **Gasto Promedio:** Los clientes tienen un cargo mensual promedio de $[Valor de la media].
* **Permanencia:** La mediana de permanencia es de [Valor de la mediana] meses, lo que indica [breve interpretación].
* **Contraste de Evasión:** Los clientes que abandonan el servicio suelen tener cargos mensuales promedio más altos ($[Valor]) en comparación con los que permanecen ($[Valor]).

* ## 📈 Visualización de Resultados
### Distribución de Evasión (Churn)
Se identificó que el **[X]%** de la base de datos corresponde a clientes que abandonaron el servicio. Esta cifra representa el punto de partida para identificar los factores de riesgo en las siguientes etapas del análisis.
