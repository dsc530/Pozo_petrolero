# OilyGiant: Recomendación de Nuevos Pozos Petrolíferos

La compañía de extracción de petróleo **OilyGiant** necesita determinar los mejores lugares donde abrir **200 pozos nuevos** de petróleo, optimizando reservas y beneficios.

## 📋 Descripción del Proyecto
A partir de parámetros recolectados en pozos petrolíferos de distintas regiones (calidad de crudo y volumen de reservas), se construye un modelo de machine learning que:
1. Predice el volumen de reservas en pozos nuevos.  
2. Selecciona los 200 puntos (pozos) con estimaciones más altas.  
3. Calcula el beneficio total por región y el riesgo de pérdidas.  
4. Identifica la región óptima con beneficio promedio máximo y riesgo inferior al 2.5 %.

## 🎯 Objetivos
- **Análisis de Parámetros:** Usar calidad de crudo y volumen de reservas como variables base.  
- **Modelado Predictivo:** Entrenar regresión lineal para estimar volumen de reservas.  
- **Selección de Pozos:** Escoger los 200 puntos con mayor reserva estimada (estudio de 500 puntos iniciales).  
- **Cálculo de Beneficio:**  
  - Presupuesto total: 100 M USD para 200 pozos.  
  - Ingreso por barril de crudo: 4.5 USD → 1 unidad (1 000 barriles) = 4 500 USD.  
- **Control de Riesgo:** Mantener regiones con probabilidad de pérdida < 2.5 %; elegir la de mayor beneficio promedio.

## 🗂️ Estructura del Proyecto
1. **Importación de Datos**  
   - Lectura de CSV con `pandas`.  
2. **Exploración de Datos (ETL)**  
   - Detección y tratamiento de nulos, duplicados y tipos de datos.  
   - Estadísticas descriptivas de variables numéricas.  
3. **Separación y Entrenamiento**  
   - División en conjuntos de entrenamiento y prueba.  
   - Ajuste de un modelo de **regresión lineal** por región.  
   - Comparación de RMSE para identificar la región con mejor ajuste.  
4. **Estimación de Ganancias**  
   - Cálculo de ingreso total según las 200 mejores reservas proyectadas.  
5. **Ganancias y Riesgos**  
   - Construcción de intervalos de confianza para beneficio.  
   - Cálculo de probabilidad de pérdidas por región.  
   - Selección final de la región que cumple objetivos de beneficio y riesgo.

## 📦 Requisitos del Entorno
1. Python 3.8 o superior
2. Pandas
3. numpy
4. scikit-learn
5. Scipy

## 🚀 Cómo Clonar el Repositorio
```bash
git clone https://github.com/dsc530/Pozo_petrolero.git
cd oilygiant-well-recommendation
