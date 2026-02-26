# Telecom X — Análisis de Evasión de Clientes (Churn)

Este repositorio contiene un notebook en Python con un flujo completo de **ETL + Análisis Exploratorio (EDA)** para estudiar la **evasión de clientes (churn)** en Telecom X. El objetivo es identificar patrones y variables asociadas a la cancelación, generando **insights** y **recomendaciones** que puedan apoyar estrategias de retención y futuros modelos predictivos.

---

## 📌 Objetivo del proyecto

- Importar y preparar datos (JSON/API) aplicando conceptos de **ETL**.
- Limpiar y transformar el dataset para análisis.
- Realizar **EDA** con métricas descriptivas y visualizaciones.
- Identificar factores asociados a churn y proponer recomendaciones.

**Variable objetivo:** `Churn`  
- `0` = el cliente **no** canceló  
- `1` = el cliente **sí** canceló

---

## 🧰 Tecnologías utilizadas

- **Python 3**
- **Pandas** (carga, limpieza, transformación y análisis)
- **Matplotlib** (visualizaciones)

---

## 📂 Estructura del repositorio

- `TelecomX_LATAM_clean.ipynb` → Notebook principal con:
  - Carga y aplanamiento del JSON (flatten)
  - Tratamiento de valores faltantes y tipos de datos
  - Validaciones (duplicados / consistencia)
  - EDA (categóricas y numéricas)
  - Informe final con conclusiones y recomendaciones

> Si el nombre del notebook difiere, actualízalo aquí.

---

## ✅ Principales pasos del análisis

### 1) Extracción (Extract)
- Lectura del dataset desde fuente JSON (API/archivo).

### 2) Transformación (Transform)
- **Aplanamiento del JSON** con `json_normalize` para convertir datos anidados en columnas.
- Normalización de nombres de columnas (limpieza de espacios invisibles).
- Conversión de tipos numéricos (por ejemplo `Charges.Total` a `float`).
- Detección de faltantes “disfrazados” como strings vacíos (`''`).

### 3) Carga / Dataset final (Load)
- Dataset final listo para análisis con validaciones aplicadas.

---

## 🔎 EDA — Qué se analizó

### Distribución de churn
- Proporción de clientes con churn vs sin churn.

### Churn por variables categóricas
- Tasa de churn por:
  - Tipo de contrato
  - Servicio de internet
  - Método de pago
  - Soporte técnico (y otros servicios)

### Churn por variables numéricas
- Comparación de distribuciones por churn:
  - `tenure` (antigüedad)
  - `Charges.Monthly` (cargo mensual)
  - `Charges.Total` (total pagado)

---

## 💡 Hallazgos típicos (insights)
En el notebook se identifican patrones consistentes como:
- Contratos **Month-to-month** asociados a mayor churn que contratos de 1 o 2 años.
- Ciertos segmentos de internet (ej. **Fiber optic**) con mayor tasa de evasión.
- Método de pago **Electronic check** con churn elevado frente a pagos automáticos.
- Menor **tenure** asociado a mayor evasión (riesgo alto en primeros meses).

*(Los valores exactos están en el notebook.)*

---

## ▶️ Cómo ejecutar

1. Clona el repositorio:
   ```bash
   git clone <URL_DEL_REPO>
   cd <NOMBRE_DEL_REPO>
