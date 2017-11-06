# Ayudantía I3

### 1. Verdadero o Falso

a) En Machine Learning modelar los datos es más importante que buscar el aprendizaje. **Falso, los algoritmos buscan aprendizaje más que modelar los datos**.

b) Cuando hablamos de *clustering*, clasificación y reducción de dimensionalidad, estamos hablando de aprendizaje supervisado. **Falso, tanto *clustering* como reducción de dimensionalidad son categorías de algoritmos de aprendizaje no supervisado**.

c) El *set* de entrenamiento nos permite calibrar nuestro modelo. **Verdadero**.

d) Una fila en el set de entrenamiento, puede considerarse como una *feature*. **Falso, una fila es un vector en el espacio de características**.

f) No es posible visualizar el espacio de características de MNIST debido a que son 10 dígitos y solo podemos visualizar 2 o 3 dimensiones. **Falso, no es posible visualizar MNIST por la gran cantidad de dimensiones, pero estas son las *features***.

g) Tener un buen *set* de entrenamiento garantiza tener una buena generalización. **Falso, siempre tenemos que apuntar a generalizar para evitar *overfitting***.

h) *Overfitting* ocurre cuando el modelo comienza a memorizar los datos de entrenamiento. **Verdadero**.

i) Cada valor en la diagonal de una matriz de confusión indica la cantidad de ejemplos mal clasificados para cada clase. **Falso, indica la cantidad de ejemplos correctamente clasificados**.


### 2. Árboles de Decisión

Se desea construir un árbol de decisión para saber si Chile sería capaz de ganar un partido de fútbol. La decisión estará basada en dos atributos binarios:

* A = Llueve.
* B = El estadio está lleno.

Asuma que, históricamente, Chile gana el 70% de los partidos que juega como local (el restante lo empata o pierde). Además, Chile juega 20% de los partidos de local con lluvia y de ellos gana el 80%, mientras que cuando no llueve gana el 85%. Por otro lado, Chile juega de local 60% de sus partidos con estadio lleno y de ellos gana el 85%, mientras que cuando no hay estadio lleno gana sólo el 45% de las veces.
