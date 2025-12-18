# portafolios.estesi
Metodología por Etapas
El desarrollo se estructuró en tres fases:

Etapa 1: 
Objetivo: Preparar un dataset limpio y robusto.

Extracción: Uso de la API wbgapi para descargar indicadores mundiales.

Limpieza: Eliminación de variables con >15% de datos faltantes.

Imputación: Tratamiento de nulos restantes utilizando la mediana (robusta a outliers).

Target: Discretización del PIB (NY.GDP.MKTP.PP.KD) en 5 categorías: Low, Medium-Low, Medium, Medium-High, High.

Etapa 2: 
Objetivo: Mitigar la maldición de la dimensionalidad.

Estandarización: Scaling de datos (StandardScaler) para homogeneizar magnitudes.

PCA: Aplicación de Análisis de Componentes Principales.

Criterio: Selección de componentes óptimos para explicar el 90% de la varianza acumulada.

Etapa 3: 
Objetivo: Comparar el desempeño predictivo bajo dos escenarios. Se entrenaron dos tipos de algoritmos (KNN y Random Forest) bajo dos condiciones:

Variables Originales (todas las columnas numéricas).

Variables Reducidas (Componentes PCA).

Se utilizaron métricas como Accuracy, F1-Score y Matrices de Confusión para determinar qué enfoque es superior para este problema económico.
