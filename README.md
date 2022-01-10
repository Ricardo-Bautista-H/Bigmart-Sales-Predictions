# sales-predictions

En el presente proyecto de predicción de ventas de BigMart se tuvo como problema principal uno de regresión del número de ventas en base a características como el tamaño del outlet del producto, el peso del producto, la visibilidad del producto, su contenido calórico, entre otros.

Tras realizar una limpieza de datos faltantes y realizar el análisis exploratorio se encontró que:
- la mayoría de productos vendidos son los de tipo verduras y vegetales y de snacks.
- Existe una ligera relación positiva entre las ventas y el precio máximo retail del producto
- La mayoría de ventas promedio se dan en outlets de tamaño mediano y en los de categoría 3
- La mayoría de productos vendidos son los de baja grasa

Posteriormente, para las predicciones se utilizaron los algoritmos de:
- Regresión lineal
- Regresión por Árboles de decisión
- Regresión por Knn
- Regresión por Bagged Trees
- Regresión por Random Forest

Para el caso de Knn y Árboles de decisión se utilizó GridsearchCV que utiliza validación cruzada para hallar el mejor hiperparámero.

Dentro de los resultados, se puede notar que el mayor score (R^2) se obtuvo en la regresión por Árboles de decisión con las siguientes métricas:
- Raíz del error cuadrático medio:  1165.5167537525563
- Error cuadrático medio:  1358429.303277897
- Error absoluto medio:  844.1747936107016
- R_2:  0.5611569422071387

Asimismo, visualizando y realizando un feature importance, se pudo encontrar que las variables más importantes para predecir las ventas son (en este orden):
- Item_MRP: Precio retail máxmio del producto
- El tipo de outlet
- El año de establecimiento del outlet