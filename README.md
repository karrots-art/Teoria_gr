# Introducción a Teoría de Gráficas

La teoría de gráficas es una rama de las matemáticas que estudia las propiedades de los grafos, aplicándolas en distintas áreas, incluyendo la computación. Estos también son conocidos como **grafos**.

### Conceptos básicos

Para comprender más a fondo este tema, es fundamental conocer los siguientes conceptos:

- **Gráficas**: Conjunto de vértices y aristas que conectan algunos o todos los vértices, representando relaciones entre objetos.
- **Vértices (nodos)**: Representan los puntos de interés en el sistema modelado.
- **Aristas**: Son las conexiones entre los vértices.

###Tipos de gráficas

Dependiendo de sus características, las gráficas se pueden clasificar en:

- **Digráfica**: Las aristas tienen una única dirección.
- **Multigráfico**: Permite la conexión de varias aristas entre dos vértices.
- **Seudográfico**: Incluye bucles, es decir, aristas que conectan un vértice consigo mismo.

Al ser representaciones visuales, las gráficas siguen estructuras específicas, se rigen por teoremas, y permiten analizar recorridos y seguir trayectorias. Además, existen diferentes tipos de gráficas dependiendo de su uso y propósito.

##2. Representación Algebraica


La representación algebraica de grafos se refiere a las diversas formas en las que un grafo puede ser descrito utilizando conceptos matemáticos y estructuras algebraicas. Estas representaciones facilitan el análisis y la manipulación de grafos mediante herramientas algebraicas y matrices. Las formas más comunes de representación algebraica son:

1. **Matriz de Adyacencia**
   Es una matriz cuadrada en la que cada elemento A[i][j] indica si existe una arista entre los vértices i y j. Si el grafo es dirigido, la matriz es asimétrica, y si es no dirigido, será simétrica. Los valores en la matriz pueden ser:
   * 0 si no hay arista entre los vértices i y j.
   * 1 (o el peso de la arista) si hay una arista entre los vértices i y j.

2. **Matriz de Incidencia**
   Es una matriz que describe la relación entre vértices y aristas. Para un grafo con n vértices y m aristas, la matriz de incidencia es una matriz de tamaño n×m, donde cada fila representa un vértice y cada columna representa una arista.
   * +1 si el vértice es el origen de una arista dirigida.
   * -1 si el vértice es el destino de una arista dirigida.
   * 0 si el vértice no está involucrado en esa arista.

3. **Lista de Adyacencia**
   En lugar de usar una matriz, se utiliza una lista donde a cada vértice le corresponde una lista de los vértices a los que está directamente conectado.

4. **Vector de Grados**
   Este es un vector que describe el grado de cada vértice del grafo.

5. **Polinomio Característico**
   El polinomio característico de un grafo se obtiene de la matriz de adyacencia del grafo.

**Matriz de Trayectorias**
La matriz de trayectorias de un grafo es una representación algebraica utilizada para modelar las conexiones indirectas entre los vértices del grafo.

**Definición**
Dado un grafo G=(V,E), donde V es el conjunto de vértices y E el conjunto de aristas, la matriz de adyacencia A es una matriz cuadrada cuyo elemento A[i][j] indica si existe una arista entre el vértice v_i y el vértice v_j.

**Propiedades de la matriz de trayectorias**
* **Matriz A^1 (Matriz de adyacencia):** La matriz de trayectorias de longitud 1 es simplemente la matriz de adyacencia del grafo A, donde cada elemento A[i][j] indica si existe una arista directa entre v_i y v_j.


##3. Conectividad y Caminos

## Caminos
Los caminos se definen como la longitud desde un vértice de origen **Y** hasta un vértice de destino **X**, siguiendo una secuencia de recorrido.

### ¿Qué es un grafo conexo?
Un grafo es conexo **si y sólo si** existe un camino entre cualquier par de vértices del grafo. Es decir, para cualquier par de vértices **(a, b)**, hay un camino posible de **a** a **b**.

La conexión en un grafo conexo se describe como una relación de equivalencia con las siguientes propiedades:

- **Simetría**: Si **(a, b)** pertenece a los vértices de un grafo, entonces **a** y **b** están conectados. Es decir, si existe **(a, b)**, también debe existir **(b, a)**.
- **Reflexividad**: Un vértice siempre está conectado consigo mismo.
- **Transitividad**: Si **a** está conectado con **b** y **b** está conectado con **c**, entonces **a** y **c** también están conectados. Es decir, si existen **(a, b)** y **(b, c)**, debe existir **(a, c)**.

### Conectividad
La conectividad en un grafo se refiere a determinar cuántas aristas o vértices se pueden eliminar sin que el grafo deje de ser conexo. Sea **G** un grafo conexo:

### Aristo-conectividad
Es el **mínimo número de aristas** cuya eliminación desconecta dos vértices **a** y **b**, haciendo que el grafo deje de ser conexo. Esta se denota como **λ(G)**.

### Vértice-conectividad
Es el **mínimo número de vértices** cuya eliminación desconecta dos vértices **a** y **b**, haciendo que el grafo deje de ser conexo. Esta se denota como **K(G)**.
#4. Gráficas Especiales  

## Gráfica Euleriana
Una gráfica es **Euleriana** si es posible recorrer todas sus aristas en un solo trazo, comenzando y terminando en el mismo vértice.

### Teoremas:
1. Una gráfica conectada es Euleriana **si y sólo si** todos los vértices tienen grado par.
2. En una gráfica Euleriana, el conjunto de aristas puede ser particionado en circuitos de aristas disjuntas.
.

## Gráfica Unicursal  
Una gráfica es **Unicursal** si se pueden recorrer todas sus aristas en un solo trazo, comenzando en un vértice y terminando en otro.  

### Nota:
En una gráfica Unicursal, los vértices pueden repetirse en el paseo abierto.  

### Teorema:
Una gráfica conectada es Unicursal **si y sólo si** todos los vértices son de grado par, excepto dos: el inicial y el final.


## Gráfica Hamiltoniana
Un **Circuito Hamiltoniano** es un circuito que pasa por todos los vértices de una gráfica. Una gráfica que contiene un Circuito Hamiltoniano es una **Gráfica Hamiltoniana**.

### Teorema:
Una condición suficiente, pero no necesaria, para que una gráfica simple sea Hamiltoniana es que el grado de todos los vértices sea al menos \(n/2\), donde \(n\) es el número total de vértices y contienen un circuito que pasa por todos los vértices.

## Gráficas Trazadas Arbitrariamente
Una gráfica es **Trazada Arbitrariamente** desde un vértice **V** si el conjunto de aristas puede particionarse en circuitos de aristas disjuntas, y todos ellos contienen al vértice **V**, es decir, todos los circuitos contienen un vértice común.

#5. Gráficas Lineales

El gráfico lineal es una transformación de las líneas de un grafo en puntos, mostrando cómo están conectadas entre sí dependiendo de los nodos que comparten. Este tipo de gráfica es útil para analizar relaciones entre conexiones, en lugar de centrarse únicamente en los nodos originales.

### Aplicaciones
- **Análisis de redes de transporte y comunicación**: Modela redes donde los nodos representan rutas (carreteras, vuelos, etc.) y las conexiones indican intersecciones o puntos en común.

### Ejemplo
En una red de aerolíneas:
- **Vértices**: Representan vuelos.
- **Aristas**: Indican aeropuertos comunes entre esos vuelos.

---

# 6. Gráficos Planares

Un **grafo planar** es aquel que puede dibujarse en un plano sin que sus aristas se crucen. Este concepto tiene aplicaciones importantes gracias a sus propiedades únicas y restricciones geométricas.

### Aplicaciones
- **Representación de mapas geográficos**: Los gráficos planares se utilizan en cartografía para modelar regiones adyacentes.

### Contexto
En cartografía, un mapa se representa mediante un grafo planar:
- **Nodos**: Representan regiones (países, estados, etc.).
- **Aristas**: Representan fronteras entre regiones adyacentes.

### Ventaja
Los gráficos planares garantizan que las aristas no se crucen, respetando la disposición física de las regiones en un plano.
# Conclusión
La teoría de grafos es una rama fundamental de las matemáticas y la informática que estudia estructuras formadas por nodos y aristas. A lo largo de esta introducción, se han cubierto los conceptos básicos para poder comprender gráficas .

El estudio de gráficas permite resolver problemas  esenciales para tareas como la búsqueda de caminos y la detección de ciclos. En resumen, la teoría de gráficas es crucial para abordar problemas prácticos y teóricos en diversas disciplinas.
#Material utilizado
https://www.youtube.com/watch?v=IU-ahHmUQRA
https://www.youtube.com/watch?v=2ufAXhByz7I&amp;t=5s
https://www.youtube.com/watch?v=n73Vzh16dlk&amp;t=4s
https://libroweb.alfaomega.com.mx/book/685/free/ovas_statics/cap7/Introduccion%20a%20la%20teoria%20de%20grafos.%20Chacon,%20Jose%20Luis..pdf
https://fcaenlinea1.unam.mx/anexos/1566/1566_u4_anexo3.pdf
 https://www.youtube.com/watch?v=Pd36ywgCO_8&t=1596s
https://medium.com/@matematicasdiscretaslibro/cap%C3%ADtulo-11-teoria-de-grafos-3b00228dd81c
https://www.youtube.com/watch?v=tBB9d8ESX28
https://www.nature.com/articles/srep03495
https://ijrti.org/papers/IJRTI2101001.pdf
https://mathworld.wolfram.com/PlanarGraph.html
https://mathworld.wolfram.com/LineGraph.html
