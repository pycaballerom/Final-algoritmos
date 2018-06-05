# Taller 3: Camino mas corto en grafos desde una sola fuente

### 1.
* Grafo a)


|Nodo|Longitud|Peso|
|----|--------|----|
|0->1|2|5|
|0->2|1|3|
|0->3|3|6|
|0->4|4|8|

* Grafo b)


|Nodo|Longitud|Peso|
|----|--------|----|
|0->1|INF|INF|
|0->2|INF|INF|
|0->3|INF|INF|
|0->4|INF|INF|

* Grafo c)


|Nodo|Longitud|Peso|
|----|--------|----|
|0->1|1|2|
|0->2|3|1|
|0->3|2|5|
|0->4|3|7|

### 2.
En el grafo b se puede encontrar un camino a cualquier nodo excepto al nodo 0 con un costo tan bajo como se desee, ya que recoriendo el ciclo 1-3-2-1 podemos restar cuanto deseemos y acceder a todos los nodos.

### 3.
* Grafo a)


|Nodo|i=1|i=2|i=3|i=4|
|----|---|---|---|---|
|0|0-0|0-0|0-0|0-0|
|1|0-9|2-5|2-5|2-5|
|2|0-3|0-3|0-3|0-3|
|3|INF|2-9|1-6|1-6|
|4|INF|2-9|2-9|3-8|

* Grafo b)


|Nodo|i=1|i=2|i=3|i=4|
|----|---|---|---|---|
|0|0-0|0-0|0-0|--|
|1|0-9|2-5|2-5|--|
|2|0-3|0-3|0-3|--|
|3|INF|2-9|1-6|--|
|4|INF|2-9|2-9|--|

* Grafo c)


|Nodo|i=1|i=2|i=3|
|----|---|---|---|
|0|0-0|0-0|0-0|
|1|0-2|0-2|0-2|
|2|0-8|0-8|3-1|
|3|INF|1-5|1-5|
|4|INF|2-14|3-7|

### 4.
En el grafo b el ciclo de peso negativo de los nodos 1, 2, 3 hace que sus pesos durante Bellamn-Ford disminuyan de forma indefinida hasta llegar a i = 7, por lo tanto con su estructura final se retorna false.

### 5.
En cada caso la función Relax se llamo el numero de vertices -1 * número de aristas. Sí, se puede reducir el número de llamdas a la función Relax.

### 6.
Si un vertice v tiene una distancia que no ha cambiado desde la ultima vez que los nodos fuera de v fueran relajados, entonces no hay necesidad de relajar los nodos fuera de v una segunda vez.

