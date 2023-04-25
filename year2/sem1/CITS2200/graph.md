# Graphs
---
#### Definition:
A graph G consissts of a set $V(G)$ called verticies together with a collection $E(G)$ of pairs of vertices. Each pair {$x, y$} $\in E(G)$ is called an *edge* of $G$.

**Example:** if $V(G) = \{A, B, C, D\}$ and $E(G)=\{\{A, B\}, \{C, D\}, \{A, D\}, \{B, C\},  \{A, C\}\}$ then $G$ is a graph with 4 verticies and 5 edges.

#### What are they used for?

Graphs are used to model a wide range of commonly occuring situations, enabling questions about a particular problem to be reduced to certain well-studied standard graph theory questions.

**Example:** 
- In computing: a graph can be used to represent processors that are conneccted via a communication link in a parallel computor system.
- In chemistry: The verticies of a graph can be used to represent the carbon atons in a molecule, and an edge between two verticies represents the bond between the corresponding atoms.

#### Properties

**Adjacency:** If $\{x, y\} \in E(G)$, we say that $x$ and $y$ are adjacent to each other, and sometimes write $x$~$y$. The number of vertices adjacent to $v$ is called the degree or valency of $v$. The sum of the degrees of the verticies of a graph is even.

**Paths:** A path of length $n$ in a graph is a sequence of vertices $v_1$ ~ $v_2$ ~ ... ~ $v_{n+1}$ such that $(v_i, v_{i+1}) \in E(G)$ and verticies $\{ v_1, v_2, ..., v_{n+1}\}$ are distinct.

**Cycles:** A cycle of length $n$ in a graph is a sequence of vertices $v_1$ ~ $v_2$ ~ ... ~ $v_{n+1}$ such that $v_1 = v_{n+1}, (v_i, v_{i+1}) \in E(G)$ and verticies $\{ v_1, v_2, ..., v_{n+1}\}$ are distinct.

**Distance:** The distance between two vertices $x$ and $y$ in a graph is the length of the shortest path between.

#### Connectivity, forests and trees


**Connected:** A graph G is connected if there is a path between any two vertices. if the grapah is not connected then its connected components are the maximal induced subgraphs that are connected.



**Forests:** A forest is a graph that has no cycles.

**Trees:** A tree is a forest with only one connected componant it is easy to see that a tree with $n$ verticies must have exactly n-1 edges. The verticies of degree 1 in a tree are called the leaves of tree.

#### Directed and weighted graphs

**Directed Graphs:** In a directed graph, an edge is an ordered pair of vertices, and hence has a direction. In directed graphs, edges are often called arcs.

**Directed Tree:** Each vertex has at most one directed edge leading into it, and there is one vertex (the root) which has a path to every other vertex.

**Weighted graphs:** In a weighted graph, each of the edges is assigned a weight (usually a non negative integer). More formally we say tgat a weighted graph is a graph $G$ together with a weight function $w: E(G) \rightarrow R$ (then $w(e)$ represents the weight of the edge $e$).

#### Distances in weighted graphs

**Definition:** In a weighted graph $X$ a path
$$
x = x_0 \sim x_1 \sim ... \sim x_n = y
$$
has weight
$$
\sum_{i = 0}^{i = n-1} w(x_i, x_{i+1})
$$

The shortest path between two vertices $x$ and $y$ is the path of minimum weight.

