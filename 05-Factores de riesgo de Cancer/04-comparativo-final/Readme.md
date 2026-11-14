# 04 - Regresión Logística vs Etiquetas Reales 🎯

## 💡 ¿Qué hace este programa?

Comparar los resultados de las etiquetas existentes o ya registradas históricamente
vs los resultados generados por el algoritmo de regresión logística.

Se documenta que este algoritmo obtuvo el mayor porcentaje de eficiencia frente a
otros modelos evaluados (Regresión Logística, Árboles, etc).

El análisis es informativo para validar la precisión del modelo.

> **⚠️ IMPORTANTE:** Este programa NO inventa etiquetas. Compara lo que ya estaba registrado en Kaggle vs lo que predice el modelo.

## ⚙️ ¿Cómo lo hace?

### 1. Carga la información
Carga el archivo `cancer-risk-factors.csv` que tiene los datos históricos con etiquetas registradas.

### 2. Preparación
*   **Entrada (X):** Todas las columnas menos `Patient_ID`, `Risk_Level`, `Overall_Risk_Score`
*   **Salida (y):** `Risk_Level` - La etiqueta real
*   Convierte `Cancer_Type` en columnas con `get_dummies`

### 3. Modelo
Usa un `Pipeline` con dos pasos para quitar el error rojo:

| Paso | ¿Qué hace? |
| :--- | :--- |
| **1. StandardScaler** | Escala los datos para que el modelo no se enrede |
| **2. LogisticRegression** | Modelo de regresión logística con `max_iter=5000`, `solver='lbfgs'` |

Entrena con el **80%** de los datos y evalúa con el **100%** para sacar el reporte total.

### 4. Comparativo
Crea el reporte final con 4 columnas:

| Columna | ¿Qué es? |
| :--- | :--- |
| `Patient_ID` | ID del paciente |
| `Risk_Level_Real_Kaggle` | Etiqueta real que venía en Kaggle |
| `Risk_Level_Predicho_Logistica` | Lo que predijo nuestro modelo |
| `Acierto` | **SI** si acertó, **NO** si se equivocó |

## 📊 Resultado

### Métrica Principal: % de Eficiencia / Accuracy vs etiquetas reales

| Métrica | Valor |
| :--- | :--- |
| **TOTAL DATOS** | 2000 |
| **CORRECTOS** | 1779 |
| **ERRADOS** | 221 |
| **Acierto** | **88.95%** |
| **Error** | 11.05% |

> **🏆 CONCLUSIÓN:** La Regresión Logística fue el modelo con mayor eficiencia frente a otros modelos evaluados. Con un **88.95%** de acierto, es el modelo ganador para este proyecto.

## 👔 Informe para el Jefe 

Este programa también crea un archivo especial para mostrar:

**`1_resultados_regresion_Logistica.html`**

Ese archivo tiene la tablita bonita con scroll, con título azul, igual que la de Costos Base.
Ahí se ven los 2000 pacientes, uno por uno, con su SI o NO.

## 📁 Archivos

*   `*.ipynb` - Programa principal
*   `cancer-risk-factors.csv` - Matriz de datos históricos con etiquetas
*   `1_resultados_regresion_Logistica.html` - Tabla bonita del comparativo
*   `README.md` - Este archivo
