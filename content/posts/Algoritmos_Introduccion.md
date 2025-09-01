---
title: "Introducción a los Algoritmos: Guía Completa"
date: 2025-09-01T11:07:14-03:00
description: "Una guía exhaustiva que cubre los fundamentos de los algoritmos, su análisis de rendimiento, los principales paradigmas de diseño, estructuras de datos esenciales y conceptos avanzados."
draft: false
tags: ["algoritmos", "estructuras de datos", "análisis de algoritmos", "notación asintótica", "programación dinámica", "teoría de grafos", "criptografía"]
---

# Introducción a los Algoritmos

## Sección 1: Fundamentos de Algoritmos y Notación Asintótica

* ¿Qué es un Algoritmo?  
* Definición: Una secuencia de pasos computacionales bien definidos para transformar una entrada en una salida, resolviendo un problema computacional.  
* Características: Precisión, finitud, determinismo (generalmente), entrada, salida.  
* Ejemplos: Algoritmos de ordenamiento (insertion sort, merge sort), búsqueda de la ruta más corta, problemas de flujo máximo, problemas NP-completos (traveling salesman).  
* El Rol de los Algoritmos como Tecnología  
* Los algoritmos son tan cruciales para el rendimiento del sistema como el hardware rápido.  
* La eficiencia algorítmica se vuelve más pronunciada con tamaños de entrada más grandes (ej., comparación entre insertion sort O(n^2) y merge sort O(n log n)).  
* Una sólida base algorítmica distingue a los programadores expertos.  
* Análisis de Algoritmos  
* Tiempo de Ejecución: Depende del tamaño de la entrada y, en algunos casos, del orden de la entrada.  
* Análisis del peor caso: Proporciona un límite superior en el tiempo de ejecución para cualquier entrada de un tamaño dado. Es el enfoque más común.  
* Análisis del caso promedio: Considera la distribución de las entradas y calcula el tiempo de ejecución esperado. Requiere supuestos sobre la distribución de las entradas o el uso de algoritmos aleatorios.  
* Modelo RAM (Random-Access Machine): Un modelo de computación donde las instrucciones se ejecutan secuencialmente, y cada instrucción básica (aritmética, movimiento de datos, control) toma un tiempo constante.  
* Notación Asintótica  
* Propósito: Describir el comportamiento limitante del tiempo de ejecución o el uso de espacio de un algoritmo a medida que el tamaño de la entrada tiende a infinito, abstrayendo los factores constantes y los términos de orden inferior.  
* O-notación (Big-O): Límite superior asintótico. f(n) \= O(g(n)) significa que existen constantes positivas c y n0 tales que 0 ≤ f(n) ≤ c g(n) para todo n ≥ n0.  
* Ω-notación (Big-Omega): Límite inferior asintótico. f(n) \= Ω(g(n)) significa que existen constantes positivas c y n0 tales que 0 ≤ c g(n) ≤ f(n) para todo n ≥ n0.  
* Θ-notación (Big-Theta): Límite asintótico estrecho (superior e inferior). f(n) \= Θ(g(n)) significa que existen constantes positivas c1, c2 y n0 tales que 0 ≤ c1 g(n) ≤ f(n) ≤ c2 g(n) para todo n ≥ n0.  
* o-notación (Small-o): Límite superior no estrecho. f(n) \= o(g(n)) significa que lim (n→∞) f(n)/g(n) \= 0\.  
* ω-notación (Small-omega): Límite inferior no estrecho. f(n) \= ω(g(n)) significa que lim (n→∞) f(n)/g(n) \= ∞.  
* Propiedades comunes: Monotonicidad, pisos y techos, factoriales, logaritmos, exponenciales.  
* Uso en ecuaciones: Cuando la notación asintótica aparece en una fórmula, representa alguna función anónima.

## Sección 2: Diseño de Algoritmos

* Paradigmas de Diseño Comunes:Divide y Vencerás: Divide un problema en subproblemas más pequeños del mismo tipo, resuelve recursivamente los subproblemas y luego combina sus soluciones para resolver el problema original (ej., merge sort, problema del subarreglo máximo).  
* Análisis con Recurrencias: T(n) \= aT(n/b) \+ D(n) \+ C(n), donde 'a' es el número de subproblemas, 'n/b' es el tamaño de cada subproblema, 'D(n)' es el tiempo de división, y 'C(n)' es el tiempo de combinación.  
* Método Maestro: Un método para resolver recurrencias de la forma T(n) \= aT(n/b) \+ f(n) en los tres casos principales.  
* Programación Dinámica: Se aplica a problemas con subestructura óptima y subproblemas superpuestos. Resuelve cada subproblema solo una vez y almacena sus soluciones en una tabla para evitar recálculos.  
* Subestructura Óptima: Una solución óptima al problema contiene soluciones óptimas a subproblemas.  
* Subproblemas Superpuestos: Un algoritmo recursivo resuelve los mismos subproblemas una y otra vez.  
* Enfoques: Top-down con memoización (almacenamiento en caché de resultados de subproblemas) o bottom-up (construyendo soluciones desde los subproblemas más pequeños).  
* Ejemplos: Problema de corte de varillas, multiplicación de cadena de matrices, subsecuencia común más larga, árboles de búsqueda binarios óptimos.  
* Algoritmos Voraces: En cada paso, hace una elección que parece ser la mejor en ese momento, con la esperanza de que conduzca a una solución globalmente óptima.  
* Propiedad de elección voraz: Una elección voraz localmente óptima conduce a una solución globalmente óptima.  
* Subestructura óptima: Similar a la programación dinámica, pero la elección voraz deja solo un subproblema por resolver.  
* Ejemplos: Problema de selección de actividades, códigos de Huffman, algoritmos de Kruskal y Prim para el árbol de expansión mínima, programación de tareas con plazos y penalizaciones.  
* Análisis Amortizado: Analiza una secuencia de operaciones, no el peor caso individual de cada operación, sino el costo total de la secuencia, promediando el costo a lo largo de las operaciones.  
* Métodos: Método de agregación (límite superior en el costo total de n operaciones), método contable (asignar costos amortizados a operaciones individuales, usando "crédito"), método potencial (uso de una función potencial para absorber o liberar costo).  
* Ejemplos: Operaciones de pila (PUSH, POP, MULTIPOP), contadores binarios, tablas dinámicas (expansión/contracción).

## Sección 3: Estructuras de Datos Fundamentales

* Estructuras de Datos Elementales  
* Pilas (Stacks): LIFO (Last-In, First-Out) \- PUSH, POP. Implementación con arreglos.  
* Colas (Queues): FIFO (First-In, First-Out) \- ENQUEUE, DEQUEUE. Implementación con arreglos circulares.  
* Listas Enlazadas (Linked Lists):Sencillamente enlazadas, doblemente enlazadas (prev, next).  
* Operaciones: SEARCH, INSERT (O(1)), DELETE (O(1) si se da un puntero al nodo, O(n) si se busca por clave).  
* Implementación de punteros y objetos usando arreglos para entornos sin tipos de puntero explícitos.  
* Árboles Arraigados (Rooted Trees):Árboles binarios: Punteros a padre, hijo izquierdo, hijo derecho.  
* Árboles con ramificación ilimitada: Representación de hijo-izquierdo, hermano-derecho (O(n) espacio).  
* Tablas Hash (Hash Tables)  
* Propósito: Implementar diccionarios (INSERT, DELETE, SEARCH) con tiempo promedio O(1).  
* Direccionamiento Directo: Si el universo de claves es pequeño, usar un arreglo donde el índice es la clave.  
* Colisiones: Mapeo de múltiples claves a la misma ranura.  
* Encadenamiento (Chaining): Cada ranura de la tabla hash apunta a una lista enlazada de elementos que se han dispersado a esa ranura.  
* Direccionamiento Abierto (Open Addressing): Todas las claves se almacenan directamente en la tabla hash. Las colisiones se resuelven sondeando sistemáticamente ranuras alternativas.  
* Sondeo Lineal, Sondeo Cuadrático, Doble Hashing.  
* Funciones Hash: Una función que mapea una clave a un índice de tabla.  
* Hashing Universal: Una familia de funciones hash donde una función aleatoria de la familia tiene una baja probabilidad de colisión.  
* Análisis Probabilístico: Uso de variables aleatorias indicadoras para analizar el comportamiento promedio.  
* Árboles de Búsqueda Binarios (Binary Search Trees \- BSTs)  
* Propiedad: Para cada nodo x, todas las claves en su subárbol izquierdo son menores que x.key, y todas las claves en su subárbol derecho son mayores que x.key.  
* Operaciones: SEARCH, MINIMUM, MAXIMUM, SUCCESSOR, PREDECESSOR, INSERT, DELETE. Todas O(h) donde h es la altura del árbol.  
* Árboles aleatoriamente construidos: Altura esperada O(log n).  
* Análisis del peor caso: La altura puede ser O(n), llevando a operaciones O(n).  
* Árboles Rojo-Negros (Red-Black Trees)  
* Propósito: Mantener el equilibrio de un BST para garantizar que la altura sea O(log n) en el peor caso.  
* Propiedades:Todo nodo es rojo o negro.  
* La raíz es negra.  
* Cada hoja (NIL) es negra.  
* Si un nodo es rojo, entonces ambos hijos son negros.  
* Para cada nodo, todos los caminos simples del nodo a las hojas descendientes contienen el mismo número de nodos negros (altura-negra).  
* Operaciones: SEARCH, MINIMUM, MAXIMUM, SUCCESSOR, PREDECESSOR, INSERT, DELETE. Todas O(log n) en el peor caso.  
* Rotaciones: Operaciones para cambiar la estructura del árbol sin violar la propiedad de BST, utilizadas para mantener las propiedades rojo-negro después de inserciones y eliminaciones.  
* Aumentando Estructuras de Datos  
* Concepto: Almacenar información adicional en una estructura de datos existente y extender las operaciones para mantener y usar esta información.  
* Pasos:Elegir una estructura de datos subyacente (ej., árbol rojo-negro).  
* Determinar la información adicional que se mantendrá en cada nodo.  
* Verificar que la información adicional pueda mantenerse eficientemente con las operaciones del árbol (ej., INSERT, DELETE, ROTATIONS).  
* Desarrollar nuevas operaciones usando la información adicional.  
* Ejemplos: Árboles de estadísticas de orden (para encontrar el i-ésimo elemento más pequeño o el rango de un elemento), árboles de intervalos (para encontrar intervalos superpuestos).  
* Heapsort y Montículos (Heaps)  
* Heap (Montículo binario): Un árbol binario casi completo que satisface la propiedad de montículo (cada nodo es mayor/menor que sus hijos).  
* Max-heap: El padre es mayor o igual que sus hijos.  
* Min-heap: El padre es menor o igual que sus hijos.  
* Operaciones: MAX-HEAPIFY (O(log n)), BUILD-MAX-HEAP (O(n)), HEAPSORT (O(n log n)).  
* Colas de prioridad: Implementadas eficientemente con heaps (INSERT, EXTRACT-MIN/MAX, DECREASE/INCREASE-KEY).  
* Quicksort  
* Concepto: Algoritmo de ordenamiento por divide y vencerás que ordena en su lugar.  
* PARTITION: Un paso clave que divide el arreglo en dos subarreglos alrededor de un elemento pivote.  
* Tiempo de ejecución: O(n^2) en el peor caso, pero O(n log n) esperado.  
* Versiones aleatorizadas: Elige un pivote aleatoriamente para garantizar un buen rendimiento promedio en cualquier entrada.  
* Ordenamiento en Tiempo Lineal  
* Límites inferiores para el ordenamiento por comparación: Cualquier algoritmo de ordenamiento por comparación requiere Ω(n log n) comparaciones en el peor caso (modelo de árbol de decisión).  
* Ordenamiento por Conteo (Counting Sort): Funciona para enteros en un rango pequeño \[0, k\]. Tiempo O(n \+ k). Estable.  
* Ordenamiento por Raíces (Radix Sort): Ordena números dígito por dígito utilizando un ordenamiento estable como Counting Sort. Tiempo O(d(n \+ k)), donde d es el número de dígitos.  
* Ordenamiento por Cubetas (Bucket Sort): Funciona para entradas de una distribución uniforme. Tiempo promedio O(n).  
* Selección (Medianas y Estadísticas de Orden)  
* Problema: Encontrar el i-ésimo elemento más pequeño en un conjunto de n números.  
* Mínimo/Máximo: O(n) tiempo.  
* RANDOMIZED-SELECT: Algoritmo por divide y vencerás con O(n) tiempo esperado.  
* SELECT (tiempo lineal en el peor caso): Garantiza O(n) tiempo en el peor caso mediante una elección cuidadosa del pivote (mediana de medianas).  
* Heaps de Fibonacci (Fibonacci Heaps)  
* Propósito: Colas de prioridad fusionables con tiempos amortizados muy rápidos para ciertas operaciones (INSERT, MINIMUM, DECREASE-KEY, UNION).  
* Operaciones:MAKE-HEAP, INSERT, MINIMUM: O(1) amortizado.  
* EXTRACT-MIN, DELETE: O(log n) amortizado.  
* UNION: O(1) amortizado.  
* Cruciales para algoritmos de grafos asintóticamente rápidos.  
* Árboles van Emde Boas (van Emde Boas Trees \- vEB Trees)  
* Propósito: Una estructura de datos para diccionarios (INSERT, DELETE, SEARCH, MINIMUM, MAXIMUM, SUCCESSOR, PREDECESSOR) que opera en tiempo O(log log u) en el peor caso, donde u es el tamaño del universo de claves.  
* Restricciones: Las claves son enteros únicos en un rango restringido \[0, u-1\], donde u es una potencia exacta de 2\.  
* Estructura recursiva: Cada vEB(u) contiene un puntero summary a un vEB(sqrt(u)) y un arreglo cluster de sqrt(u) punteros a vEB(sqrt(u)) (aproximadamente).  
* Coste de espacio: O(u), lo que puede ser grande si u es muy grande.  
* Estructuras de Datos para Conjuntos Disjuntos (Disjoint Sets)  
* Propósito: Mantener una colección de conjuntos disjuntos y admitir operaciones de UNIÓN (unir dos conjuntos) y FIND-SET (determinar el conjunto que contiene un elemento).  
* Representación:Listas enlazadas: O(n) para UNION, O(1) para FIND-SET (si el representante está al principio).  
* Bosques de conjuntos disjuntos (rooted trees): Cada nodo apunta a su padre, la raíz es el representante.  
* Heurística de unión por rango (union by rank): Une el árbol de menor rango al de mayor rango para mantener la poca altura de los árboles.  
* Heurística de compresión de camino (path compression): Durante un FIND-SET, cada nodo en el camino al representante se conecta directamente al representante.  
* Rendimiento: Una secuencia de m operaciones en n elementos toma O(m α(n)) tiempo, donde α(n) es la inversa de la función de Ackermann, que crece increíblemente lento (efectivamente constante, ≤ 4).

## Sección 4: Algoritmos de Grafos

* Representaciones de Grafos  
* Listas de adyacencia: Un arreglo de |V| listas, una para cada vértice, donde cada lista contiene los vértices adyacentes. Bueno para grafos dispersos (pocas aristas). Tiempo O(|V| \+ |E|).  
* Matrices de adyacencia: Una matriz |V| x |V| donde A\[i\]\[j\] es 1 si existe una arista (i, j), 0 en caso contrario (o el peso para grafos ponderados). Bueno para grafos densos (muchas aristas) y para búsquedas de existencia de aristas en O(1). Tiempo O(|V|^2).  
* Búsqueda en Anchura (Breadth-First Search \- BFS)  
* Propósito: Explorar un grafo nivel por nivel, encontrando las distancias de caminos más cortos (en número de aristas) desde un vértice fuente.  
* Uso: Cola para gestionar los vértices a visitar. Colorea los vértices (blanco: no descubierto, gris: descubierto pero no procesado, negro: procesado).  
* Tiempo de ejecución: O(|V| \+ |E|).  
* Propiedades: Encuentra la distancia de camino más corto δ(s, v), y construye un árbol de anchura (breadth-first tree) compuesto por las aristas predecesoras.  
* Búsqueda en Profundidad (Depth-First Search \- DFS)  
* Propósito: Explorar un grafo tan profundo como sea posible a lo largo de cada rama antes de retroceder.  
* Uso: Pila (implícita en la recursión) para gestionar los vértices. Colorea los vértices (blanco, gris, negro). Registra los tiempos de descubrimiento (d\[v\]) y finalización (f\[v\]).  
* Tiempo de ejecución: O(|V| \+ |E|).  
* Propiedades: Identifica tipos de aristas (árbol, retroceso, avance, cruce), y puede usarse para la ordenación topológica y encontrar componentes fuertemente conectados.  
* Bosque de profundidad (Depth-first forest): Colección de árboles de profundidad construidos por el DFS.  
* Ordenación Topológica (Topological Sort)  
* Propósito: Producir una ordenación lineal de los vértices de un grafo dirigido acíclico (DAG) tal que para cada arista (u, v), u aparece antes que v en la ordenación.  
* Algoritmo: Realiza un DFS y, al finalizar cada vértice (cuando se vuelve negro), lo inserta al principio de una lista.  
* Tiempo de ejecución: O(|V| \+ |E|).  
* Requisito: El grafo debe ser un DAG (sin ciclos). Si hay una arista de retroceso, el grafo no es un DAG.  
* Componentes Fuertemente Conectados (Strongly Connected Components \- SCCs)  
* Definición: Para un grafo dirigido, un conjunto máximo de vértices C tal que para cada par de vértices u, v en C, existe un camino de u a v y de v a u.  
* Algoritmo de Kosaraju/Tarjan: Un algoritmo de dos pasadas de DFS (primero en G, luego en G^T en orden decreciente de tiempos de finalización).  
* Tiempo de ejecución: O(|V| \+ |E|).  
* Árboles de Expansión Mínima (Minimum Spanning Trees \- MSTs)  
* Problema: Encontrar un subgrafo de un grafo ponderado, no dirigido y conectado que es un árbol, conecta todos los vértices, y tiene el peso total mínimo de las aristas.  
* Propiedad de la arista ligera (Light-edge property): Para cualquier corte (S, V-S) que no divida las aristas de un subconjunto A de un MST, la arista de menor peso que cruza el corte es segura para A.  
* Algoritmo de Kruskal: Un algoritmo voraz que añade aristas al MST en orden creciente de peso, siempre que no formen un ciclo. Utiliza una estructura de datos de conjuntos disjuntos. Tiempo O(|E| log |E|) o O(|E| log |V|).  
* Algoritmo de Prim: Un algoritmo voraz que crece un árbol desde un vértice inicial, añadiendo en cada paso la arista de menor peso que conecta un vértice en el árbol a un vértice fuera del árbol. Utiliza una cola de prioridad. Tiempo O(|E| log |V|) con un heap binario o O(|E| \+ |V| log |V|) con un heap de Fibonacci.  
* Caminos más Cortos de Fuente Única (Single-Source Shortest Paths)  
* Problema: Encontrar los caminos de menor peso desde un vértice fuente s a todos los demás vértices en un grafo dirigido y ponderado.  
* Relajación (Relaxation): La operación central que actualiza una estimación de la distancia (d\[v\]) y el predecesor (π\[v\]) para un vértice v si se encuentra un camino más corto a través de un vértice u.  
* Algoritmo de Bellman-Ford: Resuelve para grafos con aristas de peso negativo, detecta ciclos de peso negativo. Tiempo O(|V| |E|).  
* Caminos más cortos en DAGs: Funciona ordenando topológicamente los vértices y relajando las aristas en ese orden. Tiempo O(|V| \+ |E|).  
* Algoritmo de Dijkstra: Funciona para grafos con aristas de peso no negativo. Utiliza una cola de prioridad para extraer el vértice con la estimación de distancia más pequeña. Tiempo O(|E| log |V|) con un heap binario o O(|E| \+ |V| log |V|) con un heap de Fibonacci.  
* Caminos más Cortos para Todos los Pares (All-Pairs Shortest Paths)  
* Problema: Encontrar los caminos de menor peso entre cada par de vértices en un grafo dirigido y ponderado.  
* Enfoque de multiplicación de matrices: Extiende las rutas más cortas arista por arista. Tiempo O(|V|^3 log |V|) usando exponentiación por cuadrados.  
* Algoritmo de Floyd-Warshall: Utiliza programación dinámica. Tiempo O(|V|^3). Puede manejar aristas de peso negativo pero no ciclos de peso negativo.  
* Cierre transitivo: Determinar si existe un camino entre cada par de vértices, usando una variación de Floyd-Warshall con operaciones lógicas.  
* Algoritmo de Johnson: Para grafos dispersos con aristas de peso negativo. Reweighting (reponderación) de aristas para hacerlas no negativas y luego ejecuta Dijkstra desde cada vértice. Tiempo O(|V| |E| \+ |V|^2 log |V|) con heap binario o O(|V| |E| \+ |V|^2 log |V|) con heap de Fibonacci.  
* Flujo Máximo (Maximum Flow)  
* Red de flujo: Un grafo dirigido con capacidades en las aristas, una fuente (s) y un sumidero (t).  
* Flujo: Una función que asigna un valor a cada arista, sujeto a la restricción de capacidad y la conservación del flujo.  
* Red residual: Representa la capacidad disponible en las aristas y permite reducir el flujo en una dirección para aumentar el flujo en la dirección opuesta.  
* Camino de aumento (Augmenting path): Un camino de s a t en la red residual que puede transportar flujo adicional.  
* Método de Ford-Fulkerson: Encuentra iterativamente caminos de aumento y empuja el flujo a través de ellos.  
* Teorema de Flujo Máximo-Corte Mínimo: El valor de un flujo máximo es igual a la capacidad de un corte mínimo (una partición de los vértices en S y T con s en S y t en T).  
* Algoritmos de Push-Relabel: Mantienen un preflujo (relajación de la conservación del flujo) y una función de altura. Mueven el exceso de flujo de vértices "desbordados" a "cuesta abajo" (con menor altura) y "relabelan" (aumentan la altura) de los vértices.

## Sección 5: Conceptos Avanzados y Temas Seleccionados

* Algoritmos Multihilo (Multithreaded Algorithms)  
* Concepto: Describen el paralelismo lógico de una computación, indicando qué partes pueden ejecutarse en paralelo.  
* Palabras clave: spawn (ejecución concurrente potencial), sync (esperar a que los hijos spawned terminen).  
* DAG de computación: Un grafo dirigido acíclico que representa las dependencias entre hebras.  
* Medidas de rendimiento:Trabajo (Work, T1): Tiempo de ejecución en un solo procesador (versión serializada).  
* Span (T∞): La longitud de la ruta crítica más larga en el DAG de computación.  
* Paralelismo (T1/T∞): Cantidad promedio de trabajo que se puede realizar en paralelo en cada paso de la ruta crítica.  
* Speedup (T1/TP): Cuántas veces más rápido es el algoritmo en P procesadores que en 1 procesador. Limitado por P (ley del trabajo) y T1/T∞ (ley del span).  
* Planificador voraz (Greedy scheduler): Asigna dinámicamente hebras a procesadores disponibles. Garantiza TP ≤ T1/P \+ T∞.  
* Carreras de determinismo: Cuando el resultado de un programa multihilo puede variar debido al orden no determinista de las operaciones. Los algoritmos deben garantizar la independencia de las hebras paralelas.  
* Aritmética Modular y Criptosistemas  
* Conceptos básicos: Divisibilidad, números primos, compuestos, congruencia módulo n, MCD (GCD), MCD Extendido.  
* Grupos: Aditivos (Z\_n, \+\_n), multiplicativos (Z\*\_n, \*\_n).  
* Inversos modulares: Soluciones a ax ≡ 1 (mod n). Existen si y solo si gcd(a, n) \= 1\.  
* Exponenciación modular: Calcular a^b mod n eficientemente en O(log b) multiplicaciones.  
* Criptosistema de clave pública RSA:Generación de claves: Elige dos primos grandes p, q; n \= pq; φ(n) \= (p-1)(q-1); elige e tal que gcd(e, φ(n))=1; calcula d tal que ed ≡ 1 (mod φ(n)).  
* Clave pública: (e, n). Clave secreta: (d, n).  
* Cifrado: C \= M^e mod n.  
* Descifrado: M \= C^d mod n.  
* Seguridad: Depende de la dificultad de factorizar n en p y q.  
* Pruebas de primalidad (Primality testing):Pseudoprimos: Números compuestos que se comportan como primos para ciertas bases.  
* Test de primalidad de Miller-Rabin: Un algoritmo aleatorizado que prueba si un número es compuesto. Si lo es, siempre devuelve COMPOSITE. Si es primo, devuelve PRIME con alta probabilidad.

## Sección 6: Conceptos Matemáticos Relevantes

* Series y Sumas: Fórmula para la suma de series geométricas, aritméticas.  
* Logaritmos y Exponenciales: Propiedades de logaritmos binarios, naturales.  
* Factoriales: n\! \= n \* (n-1)\!. Aproximación de Stirling.  
* Números de Fibonacci: F\_0=0, F\_1=1, F\_i \= F\_{i-1} \+ F\_{i-2}. Relación con la razón áurea.  
* Probabilidad: Eventos, espacio muestral, variables aleatorias indicadoras, valor esperado, distribución uniforme, distribución binomial.

## Cuestionario

Instrucciones: Responda cada pregunta en 2-3 oraciones.

* Explique la diferencia fundamental entre el análisis del peor caso y el análisis del caso promedio de un algoritmo.  
* ¿Por qué los algoritmos se consideran una tecnología tan importante como el hardware rápido en la computación moderna?  
* Defina la notación O-grande (O-notación) y proporcione un ejemplo de cómo se usa para describir el tiempo de ejecución.  
* ¿Cuáles son los dos ingredientes clave que debe tener un problema para que la programación dinámica sea aplicable?  
* Describa brevemente cómo funciona un algoritmo voraz y mencione una de sus propiedades clave para garantizar la optimización.  
* Explique la idea principal detrás del análisis amortizado de algoritmos, utilizando el método de agregación como ejemplo.  
* ¿Cuál es la principal ventaja de un árbol rojo-negro sobre un árbol de búsqueda binario simple?  
* En el contexto de las tablas hash, explique el problema de las colisiones y cómo el encadenamiento ayuda a resolverlo.  
* ¿Cuál es la función principal de la operación RELAX en los algoritmos de caminos más cortos de fuente única?  
* Describa brevemente cómo el criptosistema RSA utiliza la aritmética modular para permitir la comunicación segura.

## Clave de Respuestas del Cuestionario

* Explicación: El análisis del peor caso proporciona un límite superior garantizado en el tiempo de ejecución de un algoritmo para cualquier entrada de un tamaño dado, lo que garantiza que nunca funcionará más lento de lo especificado. El análisis del caso promedio, por otro lado, calcula el tiempo de ejecución esperado promediando el rendimiento sobre una distribución supuesta de entradas, lo que puede dar una imagen más realista pero menos garantizada del rendimiento típico.  
* Explicación: Los algoritmos son cruciales porque el rendimiento total del sistema depende tanto de elegir algoritmos eficientes como de elegir hardware rápido. A medida que los problemas crecen en tamaño, las diferencias en la eficiencia algorítmica (por ejemplo, O(n log n) frente a O(n^2)) se vuelven dominantes sobre las mejoras en la velocidad bruta del hardware, lo que hace que los algoritmos sean una tecnología fundamental.  
* Definición: La notación O-grande (O(g(n))) proporciona un límite superior asintótico para una función f(n), lo que significa que f(n) crece a lo sumo tan rápido como g(n) multiplicada por una constante, para n suficientemente grande. Por ejemplo, si un algoritmo de ordenamiento tiene un tiempo de ejecución en el peor caso de O(n^2), significa que su tiempo de ejecución nunca excederá c \* n^2 para alguna constante c y n grande.  
* Ingredientes: Para que la programación dinámica sea aplicable, un problema debe exhibir subestructura óptima, lo que significa que una solución óptima al problema contiene soluciones óptimas a sus subproblemas. También debe tener subproblemas superpuestos, lo que significa que un algoritmo recursivo para el problema resuelve los mismos subproblemas una y otra vez.  
* Funcionamiento y propiedad: Un algoritmo voraz toma la decisión que parece mejor en cada paso local, esperando que esta serie de decisiones locales conduzca a una solución globalmente óptima. Una propiedad clave es la propiedad de elección voraz, que establece que una elección voraz localmente óptima es siempre parte de alguna solución globalmente óptima.  
* Idea principal: El análisis amortizado evalúa el costo total de una secuencia de operaciones en lugar del costo de cada operación individualmente. El método de agregación, por ejemplo, suma los costos reales de todas las operaciones en la secuencia y luego divide este total por el número de operaciones para obtener un costo promedio por operación, proporcionando un límite superior en el costo total.  
* Ventaja principal: La principal ventaja de un árbol rojo-negro sobre un árbol de búsqueda binario simple es que garantiza una altura O(log n) en el peor caso. Esto asegura que todas las operaciones de diccionario (búsqueda, inserción, eliminación, etc.) se ejecuten en tiempo O(log n) en el peor caso, a diferencia de los BSTs simples que pueden degenerar en una lista enlazada con operaciones O(n).  
* Colisiones y encadenamiento: Una colisión en una tabla hash ocurre cuando dos o más claves diferentes se mapean a la misma ranura de la tabla. El encadenamiento resuelve esto almacenando todos los elementos que se dispersan a la misma ranura en una lista enlazada asociada a esa ranura, permitiendo que múltiples elementos existan en la misma ubicación lógica.  
* Función principal: La operación RELAX en los algoritmos de caminos más cortos de fuente única consiste en probar si se puede mejorar el camino más corto actual hacia un vértice v y, si es así, actualizar la estimación de la distancia d\[v\] y el predecesor π\[v\] de v. Es el único mecanismo por el cual las estimaciones de caminos más cortos y los predecesores cambian.  
* Uso de aritmética modular: El criptosistema RSA genera un par de claves (pública y secreta) basadas en dos números primos grandes. Utiliza la exponenciación modular para cifrar y descifrar mensajes. Un mensaje M se cifra a C \= M^e mod n (con la clave pública e, n), y C se descifra a M \= C^d mod n (con la clave secreta d, n), donde d es el inverso modular de e con respecto al totiente de n.

## Preguntas en Formato de Ensayo

* Compare y contraste los paradigmas de diseño de algoritmos "Divide y Vencerás" y "Programación Dinámica". Incluya una discusión sobre los tipos de problemas para los que cada paradigma es más adecuado, sus propiedades subyacentes y cómo se diferencian en su enfoque para resolver subproblemas.  
* Explique cómo el Teorema de Flujo Máximo-Corte Mínimo es fundamental para la comprensión y verificación de algoritmos de flujo máximo. Describa sus implicaciones y por qué es una herramienta poderosa en la teoría de redes de flujo.  
* Analice la importancia de la notación asintótica en el estudio de algoritmos. Discuta por qué el enfoque en el comportamiento limitante es más útil que el conteo exacto de operaciones, y explique cómo la notación O, Ω y Θ proporcionan una comprensión completa de la eficiencia de un algoritmo.  
* Describa en detalle cómo el algoritmo de Dijkstra y el algoritmo de Bellman-Ford resuelven el problema de los caminos más cortos de fuente única. Explique las condiciones bajo las cuales cada algoritmo es aplicable, sus respectivos tiempos de ejecución y las razones detrás de esas diferencias de rendimiento.  
* Discuta la naturaleza de los algoritmos multihilo y sus medidas de rendimiento clave (trabajo, span, paralelismo, speedup). Explique el concepto de "carreras de determinismo" y por qué los diseñadores de algoritmos deben asegurarse de que las hebras paralelas sean independientes.

## Glosario de Términos Clave

* Algoritmo: Una secuencia de pasos computacionales bien definidos que toma un conjunto de valores como entrada y produce un conjunto de valores como salida.  
* Análisis del peor caso: Un tipo de análisis de algoritmos que determina el límite superior del tiempo de ejecución para cualquier entrada de un tamaño dado.  
* Análisis del caso promedio: Un tipo de análisis de algoritmos que calcula el tiempo de ejecución esperado de un algoritmo, promediando sobre una distribución de entradas.  
* Modelo RAM (Random-Access Machine): Un modelo computacional en el que las instrucciones se ejecutan una tras otra, y cada operación básica toma una cantidad constante de tiempo.  
* Notación Asintótica: Un conjunto de notaciones matemáticas (O, Ω, Θ, o, ω) utilizadas para describir el comportamiento limitante de las funciones, generalmente el tiempo de ejecución de los algoritmos, a medida que el tamaño de la entrada tiende a infinito.  
* Divide y Vencerás: Un paradigma de diseño de algoritmos que resuelve un problema dividiéndolo en subproblemas más pequeños del mismo tipo, resolviéndolos recursivamente y combinando sus soluciones.  
* Programación Dinámica: Un paradigma de diseño de algoritmos aplicable a problemas con subestructura óptima y subproblemas superpuestos, donde cada subproblema se resuelve solo una vez y sus resultados se almacenan.  
* Subestructura Óptima: Una propiedad de los problemas en la que una solución óptima al problema general contiene soluciones óptimas a sus subproblemas.  
* Subproblemas Superpuestos: Una propiedad de los problemas en la que un algoritmo recursivo resuelve los mismos subproblemas repetidamente.  
* Algoritmo Voraz: Un paradigma de diseño de algoritmos que en cada paso toma la decisión óptima local con la esperanza de que esto conduzca a una solución globalmente óptima.  
* Análisis Amortizado: Una técnica de análisis que examina el costo total de una secuencia de operaciones en lugar de las operaciones individuales, para obtener un límite promedio en el costo por operación.  
* Pila (Stack): Una estructura de datos LIFO (Last-In, First-Out) que admite operaciones PUSH (insertar) y POP (eliminar).  
* Cola (Queue): Una estructura de datos FIFO (First-In, First-Out) que admite operaciones ENQUEUE (insertar al final) y DEQUEUE (eliminar del principio).  
* Lista Enlazada: Una estructura de datos lineal donde los elementos no se almacenan contiguamente, sino que cada elemento apunta al siguiente (y posiblemente al anterior).  
* Tabla Hash (Hash Table): Una estructura de datos que implementa un diccionario mapeando claves a índices en un arreglo utilizando una función hash, lo que permite un tiempo de búsqueda promedio O(1).  
* Colisión (Hashing): La situación en la que dos claves diferentes se mapean a la misma ranura en una tabla hash.  
* Encadenamiento (Chaining): Un método para resolver colisiones en tablas hash, donde cada ranura de la tabla almacena una lista enlazada de los elementos que se han dispersado a ella.  
* Direccionamiento Abierto (Open Addressing): Un método para resolver colisiones en tablas hash, donde todos los elementos se almacenan directamente en la tabla, y las colisiones se resuelven sondeando ranuras alternativas.  
* Hashing Universal: Una familia de funciones hash diseñada para garantizar que una función hash aleatoria de la familia tenga una baja probabilidad de colisión.  
* Árbol de Búsqueda Binario (Binary Search Tree \- BST): Un árbol binario en el que la clave de cada nodo es mayor que todas las claves de su subárbol izquierdo y menor que todas las claves de su subárbol derecho.  
* Árbol Rojo-Negro (Red-Black Tree): Un tipo de árbol de búsqueda binario auto-equilibrado que garantiza que la altura del árbol sea logarítmica, manteniendo las operaciones eficientes.  
* Rotación (Tree Rotation): Una operación en árboles de búsqueda binarios que cambia la estructura del árbol sin violar la propiedad de ordenamiento del árbol, utilizada para reequilibrar.  
* Aumentar una Estructura de Datos: El proceso de añadir información adicional a una estructura de datos existente y modificar sus operaciones para mantener y utilizar esa información.  
* Heap (Montículo): Una estructura de datos basada en árboles binarios casi completos que satisface la propiedad de montículo (cada nodo es mayor/menor que sus hijos).  
* Heapsort: Un algoritmo de ordenamiento que utiliza la estructura de datos heap para ordenar los elementos en O(n log n) tiempo.  
* Quicksort: Un algoritmo de ordenamiento por divide y vencerás que ordena en su lugar, con un tiempo promedio esperado de O(n log n) pero un peor caso de O(n^2).  
* Ordenamiento por Conteo (Counting Sort): Un algoritmo de ordenamiento en tiempo lineal (no por comparación) para enteros en un rango pequeño.  
* Ordenamiento por Raíces (Radix Sort): Un algoritmo de ordenamiento en tiempo lineal que ordena números dígito por dígito utilizando un ordenamiento estable auxiliar.  
* Selección (Selection Problem): El problema de encontrar el i-ésimo elemento más pequeño en un conjunto de n elementos.  
* Heaps de Fibonacci (Fibonacci Heaps): Una cola de prioridad fusionable con tiempos amortizados muy rápidos para ciertas operaciones, especialmente útil en algoritmos de grafos.  
* Árbol van Emde Boas (vEB Tree): Una estructura de datos que soporta operaciones de diccionario en enteros en tiempo O(log log u) donde u es el tamaño del universo.  
* Conjuntos Disjuntos (Disjoint Sets): Una estructura de datos que mantiene una colección de conjuntos disjuntos y admite operaciones para unir conjuntos (UNION) y encontrar el representante de un conjunto (FIND-SET).  
* Compresión de Camino (Path Compression): Una heurística para la estructura de datos de conjuntos disjuntos que hace que cada nodo en el camino desde un elemento al representante apunte directamente al representante.  
* Unión por Rango (Union by Rank): Una heurística para la estructura de datos de conjuntos disjuntos que une el árbol de menor "rango" al de mayor "rango" para mantener los árboles poco profundos.  
* Listas de Adyacencia: Una representación de grafo que utiliza un arreglo de listas para almacenar los vecinos de cada vértice.  
* Matrices de Adyacencia: Una representación de grafo que utiliza una matriz para indicar la presencia o peso de las aristas entre pares de vértices.  
* Búsqueda en Anchura (Breadth-First Search \- BFS): Un algoritmo de recorrido de grafos que explora el grafo nivel por nivel, encontrando las distancias de caminos más cortos en número de aristas.  
* Búsqueda en Profundidad (Depth-First Search \- DFS): Un algoritmo de recorrido de grafos que explora el grafo tan profundo como sea posible a lo largo de cada rama antes de retroceder.  
* Ordenación Topológica (Topological Sort): Una ordenación lineal de los vértices de un DAG tal que para cada arista (u, v), u aparece antes que v en la ordenación.  
* Componentes Fuertemente Conectados (Strongly Connected Components \- SCCs): Subgrafos máximos de un grafo dirigido donde cada par de vértices en el subgrafo es mutuamente alcanzable.  
* Árbol de Expansión Mínima (Minimum Spanning Tree \- MST): Un subgrafo de un grafo ponderado, no dirigido y conectado que es un árbol, conecta todos los vértices y tiene el peso total mínimo de las aristas.  
* Algoritmo de Kruskal: Un algoritmo voraz para encontrar un MST, que añade aristas en orden creciente de peso si no forman un ciclo.  
* Algoritmo de Prim: Un algoritmo voraz para encontrar un MST, que crece un árbol desde un vértice inicial añadiendo la arista de menor peso que conecta el árbol con un vértice fuera de él.  
* Camino Más Corto de Fuente Única (Single-Source Shortest Path): El problema de encontrar los caminos de menor peso desde un vértice fuente a todos los demás vértices en un grafo ponderado.  
* Relajación (Relaxation): La operación central en los algoritmos de caminos más cortos que intenta mejorar una estimación de distancia.  
* Algoritmo de Bellman-Ford: Un algoritmo de caminos más cortos de fuente única que maneja aristas de peso negativo y detecta ciclos de peso negativo.  
* Algoritmo de Dijkstra: Un algoritmo de caminos más cortos de fuente única que funciona para grafos con aristas de peso no negativo.  
* Caminos Más Cortos para Todos los Pares (All-Pairs Shortest Paths): El problema de encontrar los caminos de menor peso entre cada par de vértices en un grafo ponderado.  
* Algoritmo de Floyd-Warshall: Un algoritmo de programación dinámica para encontrar caminos más cortos para todos los pares.  
* Algoritmo de Johnson: Un algoritmo para caminos más cortos para todos los pares en grafos dispersos con aristas de peso negativo, que utiliza reponderación y Dijkstra.  
* Red de Flujo (Flow Network): Un grafo dirigido con capacidades en las aristas, una fuente y un sumidero, utilizado para modelar el transporte de alguna cantidad.  
* Flujo Máximo (Maximum Flow): El problema de encontrar el flujo total máximo posible desde la fuente hasta el sumidero en una red de flujo.  
* Red Residual (Residual Network): Un grafo que indica la capacidad disponible para aumentar el flujo en una red de flujo.  
* Camino de Aumento (Augmenting Path): Un camino de la fuente al sumidero en la red residual que se puede usar para aumentar el flujo total.  
* Método de Ford-Fulkerson: Un algoritmo para encontrar el flujo máximo que busca repetidamente caminos de aumento.  
* Teorema de Flujo Máximo-Corte Mínimo: Un teorema fundamental que establece que el valor de un flujo máximo es igual a la capacidad de un corte mínimo en la red.  
* Algoritmos Multihilo (Multithreaded Algorithms): Algoritmos diseñados para explotar el paralelismo, dividiendo la computación en múltiples hebras que pueden ejecutarse concurrentemente.  
* Trabajo (Work, T1): El tiempo total de ejecución de un algoritmo multihilo en un solo procesador (esencialmente el tiempo de la versión serializada).  
* Span (T∞): La longitud de la ruta crítica más larga en el grafo DAG de la computación multihilo, que representa el tiempo de ejecución en un número infinito de procesadores.  
* Paralelismo: La relación entre el trabajo y el span (T1/T∞), que indica la cantidad promedio de trabajo que se puede realizar en paralelo.  
* Speedup: La relación entre el trabajo y el tiempo de ejecución en P procesadores (T1/TP), que mide la ganancia de rendimiento del paralelismo.  
* Carreras de Determinismo (Determinacy Races): Una situación en algoritmos multihilo donde el resultado de la computación puede depender del orden no determinista de las operaciones.  
* Aritmética Modular: Un sistema de aritmética para enteros donde los números "se envuelven" al alcanzar un cierto valor llamado módulo.  
* MCD (Máximo Común Divisor): El entero positivo más grande que divide dos o más enteros sin dejar resto.  
* MCD Extendido (Extended Euclidean Algorithm): Un algoritmo que calcula el MCD de dos enteros a y b, y también los coeficientes x e y tales que ax \+ by \= gcd(a, b).  
* Grupo Aditivo Modular (Z\_n, \+\_n): El conjunto de enteros {0, 1, ..., n-1} bajo la operación de adición módulo n.  
* *Grupo Multiplicativo Modular (Z\_n, \_n):* El conjunto de enteros a en {1, ..., n-1} tales que gcd(a, n) \= 1, bajo la operación de multiplicación módulo n.  
* Exponenciación Modular: La operación de calcular a^b mod n eficientemente.  
* Criptosistema RSA: Un popular criptosistema de clave pública que se basa en la dificultad de factorizar números enteros grandes.  
* Test de Primalidad de Miller-Rabin: Un algoritmo aleatorizado para probar si un número es primo. Si dice que un número es compuesto, es definitivo; si dice que es primo, es probable.

