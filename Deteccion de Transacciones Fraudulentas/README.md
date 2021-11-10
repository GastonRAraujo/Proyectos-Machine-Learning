# Trabajo Practico 4: Transacciones fraudulentas

# Modelos

1) KNN
2) SVM
3) RandomForest

# Preprocesado de datos
Propongo dos archivos, uno en el que se ha aplicado una reducción de la dimensionalidad y otro donde no se ha realizado.
En ambos se utilizan los tres métodos.

[Notebook con reducción de la dimensionalidad:](https://github.com/GastonRAraujo/Materia-Ap_Maq/blob/master/TP4/Transacciones_fraudulentas.ipynb)

[Notebook sin reducción de la dimensionalidad](https://github.com/GastonRAraujo/Materia-Ap_Maq/blob/master/TP4/Transacciones_fraudulentas_NO_DIM_RED.ipynb)

A su vez se comparan las métricas si utilizamos el dataset desequilibrado o si, a la hora de entrenar, se utiliza una misma cantidad de transacciones fraudulentas que no fraudulentas.

# Resultados

En cada notebook se encuentran matrices de confusion y la métricas clásicas para cada modelo entrenado.

1) Se obtuvo una mejoría al filtrar el dataset a la hora de entrenar y utilizar una muestra balanceada (igual cant de ambas etiquetas).
2) Se obtuvo una mejoría al aplicar una reducción de la dimensionalidad.

Por lo que los mejores resultados se obtuvieron para los modelos entrenados con reducción de la dimensionalidad y una muestra balanceada.
Dentro de los tres modelos utilizados, los resultados fueron muy similares en este caso (se puede observar que en los demás casos estudiados se observa mayor discrepancia).
El modelo con un mayor recall fue el KNN (K vecinos cercanos) pero posee un mayor tiempo de ejecución por lo que si hacemos una pequeña concesión en recall obtendremos un modelo rápido y preciso.
