# 🐄 Análisis y predicción de la producción de leche en Maharashtra (India)

Este proyecto analiza la **producción histórica de leche** del estado de Maharashtra (India) y desarrolla modelos de **machine learning** para predecir la producción futura a partir de la tendencia temporal.

El enfoque combina **análisis exploratorio de datos (EDA)**, **visualización**, y **modelos de regresión**, comparando un modelo lineal con un modelo de ensemble.

---

## 🌏 Contexto del problema

La producción de leche es un indicador clave para:
- planificación agropecuaria
- logística y distribución
- políticas públicas del sector lácteo

Analizar su evolución permite detectar **tendencias de largo plazo** y evaluar la capacidad de modelos predictivos simples para forecasting.

---

## 🎯 Objetivos

- Analizar la evolución anual de la producción de leche
- Identificar tendencias y patrones temporales
- Visualizar la relación entre año y producción
- Entrenar modelos de regresión para predicción
- Comparar desempeño entre modelos lineales y no lineales

---

## 📊 Dataset

**Fuente:** Indiostat  
**Cobertura:** Producción anual de leche en Maharashtra

### Variables
- `Year`
- `Milk Production` (toneladas)

Los datos son **reales y confiables**, con una estructura simple ideal para análisis temporal inicial.

---

## 🧹 Preparación de datos

- Carga del dataset desde CSV
- Verificación de tipos de datos
- Chequeo de valores nulos y duplicados
- Escalado de la variable `Year` mediante `StandardScaler`

---

## 🔍 Análisis exploratorio (EDA)

- Visualización de la producción a lo largo del tiempo (line plots)
- Gráficos de barras por año
- Diagramas de dispersión
- Histogramas y KDE
- Heatmap de correlación
- Pairplots para exploración multivariada

Estas visualizaciones permiten observar una **tendencia creciente clara** en la producción de leche.

---

## 🤖 Modelado predictivo

### 1. Regresión Lineal
- Variable explicativa: `Year`
- Escalado previo de la variable
- Evaluación mediante **R²**

### 2. Random Forest Regressor
- Búsqueda de hiperparámetros con **GridSearchCV**
- Validación cruzada (CV = 5)
- Métrica principal: **Mean Squared Error (MSE)**
- Evaluación adicional con **R²**

El Random Forest captura mejor posibles **relaciones no lineales** en la serie temporal.

---

## 📈 Resultados

- Ambos modelos muestran buen ajuste a la tendencia
- El **Random Forest** obtiene mejor desempeño predictivo que la regresión lineal
- El uso de GridSearchCV mejora la generalización del modelo
- Se observa buena concordancia entre valores reales y predichos

---

## 📊 Visualización de predicciones

- Comparación gráfica entre valores reales y predichos
- Análisis de diferencias entre predicción y realidad
- Visualización clara del ajuste del modelo

---

## 🛠️ Tecnologías utilizadas

- **Python**
- **pandas, numpy**
- **matplotlib, seaborn**
- **scikit-learn**

---

## 📂 Estructura del repositorio

├── Milk_Pro.csv
├── produccion_leche.py
├── README.md


---

## 🚀 Próximos pasos

- Validación temporal (train/test split por año)
- Comparación con modelos ARIMA / SARIMA
- Feature engineering temporal
- Predicción a futuro (forecasting explícito)
- Optimización del modelo Random Forest

---

## 👤 Autor

**Flavia Hepp**  
Data Scientist en formación  
