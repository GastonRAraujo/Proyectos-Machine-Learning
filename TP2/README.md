# Trabajo Practico 2
Se encuentran ambos ejercicios por separado.
#
Ejercicio 1:

Se graficó los distintos datasets sobre la situación actual en BAHIA BLANCA.
Se encontró la prescencia de outliers y de distribuciones "anormales".

Pendiente por hacer: eliminar los outliers correspondientes

#
Ejercicio 2:

Se realizaron funciones para simplificar la comparacion al variar parametros (umbral, media de la distribucion, desvio estandar).
Se realizaron curvas ROC, y se determinarón, utilizando la curva, el valor umbral que minimiza el error.
Se comparó con la elección "a ojo" y que sucede al aumentar el solapamiento.

Se observó que este produce que el clasificador no logre predecir correctamente la etiqueta.

#
Ejercicio 3:

(codigo en construccion)

Propuestas:
1)Realizar dos curvas roc, una para cada feature, y determinar un umbral para cada feature.
2)Determinar una "distancia" umbral a la moda, a partir de la cual se determine que etiqueta se le asigna.
Si se utiliza junto con alguna transformación de los datos, daria una elipse a partir de la cual los datos pertenecen a un grupo u otro.
3)En vez de utilizar una elipse, se pueden utilizar otro tipo de funciones determinando una relacion funcional entre el umbral para cada feature:

Umbral_feature2 = f(Umbral_feature1) 
con f(x) una función continua.
dado (x1,y1):  

si y1 < f(x1) -> asigna etiqueta A

si y1 > f(x1) -> asigna etiqueta B

