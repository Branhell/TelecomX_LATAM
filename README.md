# 📊 Informe Final – Análisis de Evasión de Clientes (Churn) en Telecom X

## 🔹 Introducción
El objetivo de este análisis es comprender el problema de **evasión de clientes (Churn)** en la empresa Telecom X.  
La evasión ocurre cuando los clientes deciden cancelar el servicio, lo que impacta directamente en los ingresos y sostenibilidad del negocio.  
Mediante el análisis de datos demográficos, tipo de contrato, métodos de pago y comportamiento de consumo, buscamos identificar patrones que expliquen por qué algunos clientes permanecen y otros se retiran.

---

## 🔹 Limpieza y Tratamiento de Datos
1. **Importación de datos**: Se cargó el archivo JSON desde la API de Telecom X.  
2. **Normalización**: Se expandieron las columnas anidadas (`customer`, `phone`, `internet`, `account`) para obtener un DataFrame plano.  
3. **Corrección de inconsistencias**:  
   - Eliminación de duplicados.  
   - Conversión de columnas numéricas (`Charges.Monthly`, `Charges.Total`) a valores numéricos.  
4. **Estandarización y transformación**:  
   - Conversión de variables binarias (`Yes/No`) a valores 1 y 0.  
   - Renombrado de columnas para mayor claridad (`MonthlyCharges`, `TotalCharges`).  
5. **Creación de columna adicional**: Se generó `daily_accounts` para calcular el gasto diario a partir de la facturación mensual.

---

## 🔹 Análisis Exploratorio de Datos
- **Distribución general de Churn**: Aproximadamente un cuarto de los clientes cancelaron el servicio.  
- **Análisis descriptivo**:  
  - Clientes con menor tiempo de contrato (`tenure`) presentan mayor evasión.  
  - Cargos mensuales altos (`MonthlyCharges`) se asocian con mayor probabilidad de cancelación.  
  - Clientes con acumulados bajos (`TotalCharges`) tienden a cancelar más, reflejando que son clientes nuevos.  
- **Variables categóricas**:  
  - El género no mostró diferencias significativas en evasión.  
  - Los contratos mensuales tienen mayor tasa de cancelación que los contratos de largo plazo.  
  - Los métodos de pago electrónicos presentan mayor evasión que pagos automáticos o transferencias.  
- **Variables numéricas**:  
  - Histogramas mostraron que clientes con `tenure` bajo y `MonthlyCharges` altos concentran la mayor evasión.  

---

## 🔹 Conclusiones e Insights
- La **evasión está fuertemente asociada con clientes nuevos** (tenure bajo).  
- Los **cargos mensuales altos** incrementan la probabilidad de cancelación.  
- Los **contratos mensuales y métodos de pago electrónicos** son los perfiles con mayor riesgo de churn.  
- El género no influye significativamente en la decisión de cancelar.  

---

## 🔹 Recomendaciones
1. **Fidelización temprana**: Implementar estrategias de retención en los primeros meses de contrato.  
2. **Planes más atractivos**: Ofrecer contratos a largo plazo con beneficios claros.  
3. **Optimización de precios**: Revisar la estructura de cargos mensuales para clientes con alto riesgo.  
4. **Incentivos en métodos de pago**: Promover pagos automáticos con beneficios adicionales.  
5. **Monitoreo continuo**: Crear dashboards para identificar clientes en riesgo y actuar de manera preventiva.  

---

## 🚀 Conclusión
Este informe resume el proceso completo de análisis de evasión de clientes en Telecom X, desde la importación y limpieza de datos hasta la obtención de insights y recomendaciones estratégicas.  
La información obtenida permitirá diseñar acciones concretas para **reducir la tasa de churn y mejorar la fidelización de clientes**.
