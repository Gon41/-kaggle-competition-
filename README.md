## -kaggle-competition-
______

# 1. **Objetivo**

Obtener la predicción del precio de diamantes.
Para ello tenemos el train.csv que debemos limpiar, investigar y entrenar un modelo predictivo. Para ello nos servimos del segundo archivo (predict.csv).

----
# 2. **Metodología**

## 2.1. Limpieza

No habia mucho que limpiar en el dataset, ya que no habia datos nulos ni duplicados. Revisando las columnas hay tres columnas categóricas que luego trataremos.

Estudiando la correlación y fijándonos en la columna "price", las filas "carat","x","y" y "z" tienen mucha correlación con "price".
De ellas vemos que entre "x","y" y "z" hay demasiada correlación, lo que nos indica que es probable que haya colinealidad
Cómo "x" tiene mayor correlación con "price" decido dejarla y eliminar "y" y "z".

Convierto las columnas categóricas en numéricas con el método 'dummy'.

## 2.2. Elección del modelo

He probado con los siguientes modelos:

    - LinearRegression()
    - DecisionTreeRegressor()
    - RandomForestRegressorr()

De ellos cada uno me daba menor distorsión en el precio y queda en 600-700€ de diferencia.

------


# 3. Dificultades

En clase hemos machacado mucho el tema y no ha sido complicadisimo, pero si que no llego a entender del todo cuando se aplica cada uno de los modelos o por qué se aplican.