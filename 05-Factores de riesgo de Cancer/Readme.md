# 05 - Factores de Riesgo de Cáncer 🎗️

## 💡 ¿Qué es este proyecto?

Este proyecto analiza los factores de riesgo de cáncer a partir de datos históricos de Kaggle.
El objetivo es entender los datos, validar cuál modelo predice mejor el riesgo, y cuánto costaría usar un modelo de IA en la nube.

Se trabajó en 4 puntos, en orden, parce. Cada punto tiene su carpeta con su programa y su informe.

## 📁 Los 4 Puntos Analizados

### 01 - Limpieza y Preparación de Datos
**Carpeta:** `01-...`
*   Se cargó el archivo `cancer-risk-factors.csv`
*   Se limpiaron nulos, duplicados y tipos de datos
*   Se dejó la matriz lista para analizar

> **Resultado:** Matriz limpia, lista para usar.

### 02 - Análisis Exploratorio
**Carpeta:** `02-...`
*   Se analizaron los factores de riesgo: edad, tabaquismo, alcohol, etc.
*   Se vieron gráficas de distribución de `Risk_Level`: Low, Medium, High
*   Se identificaron qué factores pesan más

> **Resultado:** Ya sabíamos qué estaba pasando en los datos antes de modelar.

### 03 - Costos Base por APIs
**Carpeta:** `03-costos-base`
*   Se compararon los costos de usar IA en la nube para clasificar el riesgo
*   Se consultaron las páginas oficiales de precios

| Proveedor | Para ver el precio |
| :--- | :--- |
| AWS Bedrock | [Ver en AWS](...) |
| Anthropic Claude | [Ver en Anthropic](...) |
| Google Vertex AI | [Ver en Google](...) |

> **Resultado:** Ya sabemos cuánto costaría llevar esto a producción.

### 04 - Comparativo Final - Regresión Logística vs Etiquetas Reales 🎯
**Carpeta:** `04-comparativo-final`
*   Se comparó lo que ya estaba registrado en Kaggle vs lo que predice la Regresión Logística
*   El modelo se entrenó con el 80% y se evaluó con el 100%

| Métrica | Valor |
| :--- | :--- |
| **TOTAL DATOS** | 2000 |
| **CORRECTOS** | 1779 |
| **ERRADOS** | 221 |
| **Acierto** | **88.95%** |

> **🏆 CONCLUSIÓN FINAL:** La Regresión Logística fue el modelo ganador, con **88.95%** de acierto.
> **Para ver los 2000 registros, entre a la carpeta 04 y abra el archivo `1_resultados_regresion_Logistica.csv`**

## 👔 Resumen para el Jefe

| Punto | ¿Qué hicimos? | ¿Qué entregamos? |
| :--- | :--- | :--- |
| **01** | Limpiamos los datos | Matriz limpia |
| **02** | Exploramos los datos | Gráficas y hallazgos |
| **03** | Cotizamos APIs | Tabla de costos |
| **04** | Validamos el modelo | **88.95% de acierto, 2000 registros** |
