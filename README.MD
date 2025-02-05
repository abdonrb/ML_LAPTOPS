# Analisis Exploratorio / Modelo MachineLearning de Laptos.
![MPG Analysis Banner](https://tecladoschulos.com/wp-content/uploads/marcas-de-ordenadores.jpg)

---

## 📋 Descripcion del proyecto

---

El **DataSet de Laptos** es un conjunto de datos obtenidos mediante técnicas de web scraping. Debido a que la información recopilada estaba desordenada y presentaba inconsistencias, procedimos a realizar una limpieza exhaustiva y un proceso de Future Engenieer, creando nuevas columnas a partir de las existentes y separando informacion. Una vez depurados los datos, transformamos las variables categóricas en numéricas utilizando OneHotEncoder y LabelEncoder, preparando el dataset para desarrollar un modelo de predicción del precio de las laptos.

**Objetrivos Principales:**
- Limpieza de datos.
- Future Engenieer.
- Analisis Univariante.
- Crear modelo predictivo para el precio de la laptop segun sus caracteristicas.

---
## 🚀 Trabajo Realizado

1. ### **Limpieza de Datos:**
 - Eliminar informacion sin importancia de las variables.
 - Ajustar los tipos de datos.

2. ### **Future Engineer:**
 - Combinar columnas.
 - Eliminar columnas irrelevantes.
 - Extraer informacion de una columna para crear otras.

3. ### **Analisis Univariante:**
 - Exploracion de la distribucion de las variables
 - Test de normalidad a cada variable numerica. (Shapiro,NormalTest,Kolmogorov-Smirnov)
 - Visualizacion de outliers.
 - Analisis de cardinalidad de las variables.

4. ### **Machine Learning:**
 - Transformacion de variables categoricas a numericas.
 - Test de colinealidad.
 - Analisis de correlacion.

## **¿Que modelo de predicción utilicé?**

Después de probar varios modelos, opte por utilizar **RandomForestRegressor** para predecir el precio. Para optimizar el rendimiento del modelo, empleé **SelectFromModel** junto a **RandomForestRegressor**, lo que permitió seleccionar únicamente las características más relevantes y descartar aquellas con poca importancia. Además con el metodo **PolynomialFeatures**, generamos columnas polinómicas para capturar relaciones no lineales entre las variables y enriquecer el conjunto de características. Posteriormente, escalé los datos con **RobustScaler**, una técnica que normaliza las variables ante valores atípicos, garantizando que todas las características se encuentren en una escala comparable y evitando que diferencias en magnitud influyan indebidamente en el modelo. Finalmente, entrené el modelo con los datos transformados y realicé la predicción sobre el conjunto de pruebas, obteniendo un error cuadrático medio (RMSE) de 3.23 🚀.

---

 ## 📂 Estructura del Proyecto  

```plaintext
├── data/                # Archivos del dataset  
├── notebooks/           # Jupyter Notebooks para el análisis exploratorio  y mdoelo de machine learning.
├── srcipts/             # Clases utilizadas para optimizar el Analisis Exploratorio.
├── README.md            # Descripción del proyecto (este archivo)  
```

---

## 🛠️ Herramientas y Librerías Utilizadas  

| Herramienta      | Uso                                                                 |
|------------------|---------------------------------------------------------------------|
| **Python** 🐍            | Lenguaje principal para manipulación y análisis de datos.         |
| **Pandas** 🐼            | Limpieza, transformación y análisis de datos tabulares.           |
| **Matplotlib** 🎨        | Creación de gráficos estáticos para visualización.                |
| **Seaborn** 📊           | Visualización avanzada de datos con gráficos estadísticos.         |
| **Scipy** 🔬             | Pruebas estadísticas e inferencia avanzada.                       |
| **Jupyter** 📓           | Entorno interactivo para escribir y ejecutar análisis paso a paso.|
|**RandomForest** 💥       | Combinación de los outputs de varios árboles de decisión para obtener un único resultado (Precio).|
|**PolynomialFeature** 🐙  |Generación de columnas polinómicas entre relaciones no lienales.|
|**RobustScaler** 💪       | Estandarizar los datos para que las variables se encunetren en un rango comparable.|

---

## 📈 **Resultados Clave**📊 
 - Logramos una gran limpieza de los datos.
 - Con la separacion de 2 CSV (Train y Test), asignamos precios a las laptos en el csv test, aplicando el modelo realizado.
 - RMSE de 3.23 🚀
 - R2 de 0.88 🚀
 - MAPE de 0.075 🚀

```