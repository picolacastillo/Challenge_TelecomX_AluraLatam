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
