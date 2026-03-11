# 📞 Telecom X: Análisis de Evasión de Clientes (Churn)

![Python](https://img.shields.io/badge/python-3.10+-blue.svg)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=flat&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=flat&logo=Matplotlib&logoColor=black)
![Seaborn](https://img.shields.io/badge/Seaborn-blue?style=flat&logo=python&logoColor=white)

Este proyecto realiza un análisis exploratorio de datos (EDA) detallado sobre el comportamiento de los clientes de **Telecom X**, una empresa de telecomunicaciones de LATAM. El objetivo principal es identificar los factores críticos que influyen en la deserción de clientes (*Churn*) para proponer estrategias de retención basadas en datos.

## 🎯 Propósito del Análisis

La pérdida de clientes es uno de los desafíos más costosos en la industria de telecomunicaciones. Este notebook busca responder:
* ¿Cuál es la tasa de evasión actual de la empresa?
* ¿Existen patrones de consumo (cargos mensuales/totales) asociados al Churn?
* ¿Qué servicios o métodos de pago presentan mayor riesgo de abandono?
* ¿Cómo influye el tipo de contrato en la fidelidad del cliente?

## 📂 Estructura del Proyecto

El proyecto se concentra en un único flujo de trabajo dentro del notebook `TelecomX_LATAM_v2.ipynb`, organizado de la siguiente manera:

1.  **Extracción:** Carga de datos crudos en formato JSON desde una fuente remota.
2.  **Transformación (ETL):** * Desestructuración de objetos anidados (`customer`, `phone`, `internet`, `account`).
    * Limpieza de tipos de datos (conversión de strings a numéricos).
    * Tratamiento de valores nulos mediante imputación por mediana.
3.  **Análisis y Visualización:** Creación de gráficos estadísticos para identificar tendencias.
4.  **Informe Final:** Resumen de métricas clave y correlaciones.

## 📊 Insights y Visualizaciones Clave

El análisis arrojó hallazgos fundamentales para el negocio:

### 1. Tasa de Evasión General
Aproximadamente el **26.5%** de los clientes han abandonado el servicio.

### 2. Impacto del Cargo Mensual
Se observa que los clientes que abandonan tienden a tener cargos mensuales significativamente más altos en comparación con los que permanecen.

### 3. Factores de Riesgo Críticos
* **Servicio de Internet:** Los usuarios de **Fibra Óptica** presentan una tasa de evasión considerablemente mayor que los de DSL.
* **Método de Pago:** El pago mediante **Cheque Electrónico** es el indicador más fuerte de deserción.
* **Tipo de Contrato:** Los contratos **mes a mes** tienen una tasa de fuga drásticamente superior a los contratos de 1 o 2 años.


## 🚀 Instrucciones de Uso

Para ejecutar este análisis localmente o en la nube, sigue estos pasos:

### Opción A: Google Colab (Recomendado)
1. Sube el archivo `.ipynb` a tu Google Drive.
2. Ábrelo con "Google Colaboratory".
3. Ejecuta las celdas en orden (el notebook descarga los datos automáticamente desde GitHub).

### Opción B: Entorno Local (Jupyter/VS Code)
1. Asegúrate de tener instalado Python 3.10 o superior.
2. Instala las dependencias necesarias:
   ```bash
   pip install pandas matplotlib seaborn numpy
