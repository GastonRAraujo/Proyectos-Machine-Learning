# Clasificación

#
Clasificador KNN 2D:
Se creó un dataset 2D mediante dos datasets gausianos. Se utilizó el clasificador por vecinos cercanos de scikitlearn. 
Luego se repitio el trabajo variando los parámetros N,K.

Observo una perdida de rendimiento al aumentar el tamaño de mi dataset pero mantener k = 1 debido a la gran sensibilidad del modelo.
Por el contrario si aumentamos k (de forma controlada para evitar overfiting debido a k>>1) vemos una mejora en el rendimiento del modelo.
#
Clasificador KNN 2D + grid search:
Se probó utilizar GridSearch que nos permite hacer crossvalidation y variar distintos parametros del modelo a utilizar sobre
lo realizado con KNeighborsClassifier de scikitlearn.

#
Recomendacion de Canciones:

Se busco determinar si una canción gustará según las características de la canción.

Se importó el dataset.csv correspondiente, y se extendió lo realizado anteriormeente para 2D pero para 14D.
Mediante StandarScaler se normalizaron los datos y se busco, mediante GridSearch, un valor óptimo para los parámetros.

Al final se repitió el codigo pero incorporando la información de banda utilizando números para determinar la misma. Para eso se utilizó "One-Hot Encoder" pero se obtuvo una perdida del accuracy y un aumento del tiempo de entrenamiento.
