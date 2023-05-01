# Kruskal
----
#### Implimentation
The main problem of the implementation of Kruskal is to decide whether the next edge to be added is allowable - that is, does it create a cucle or not.

Suppose that at some stafe in the algorithm the next shortest edge is {$x, y$}. Then there are two possiblilities.

**$x, y$ lie in different trees of $F$:** In this case adding the edge does not create any new cyckes, but merges together two of the trees of $F$

**$x, y$ lie in the same tree of $F$:** In this case adding the edge creates a cycle and the edge should not be added to $F$.


Therefore we need data structures that allow us to quickly find the tree to which an element belongs and quickly merge two trees.




#### Paritions or disjoint sets
The appropriate data structure for this problem is the partition (sometimes called disjoint sets). Recall that a partition of a set is a collection of disjoint subsets (called cells) that cover the entire set.

At the biginning of Kruskal's algorithm we have a partition of the verticies into the discrete partition where each cell has size 1. As each edge is added to the minimum spanning tree, the number of cells in the partition decreases one by one.

The operations that we need for kruskal's algorithm are:

**Union(cell, cell):** Creates a new partition by merging two cells.

**Find(element):** Finds the cell containing a given element.


#### Niave partitions

One simple way to represent a partition is simply to choose one element of each cell to be the leader of that cell. Then we can simply keep an array $\pi$ of length $n$ where $\pi(x)$ is the leader of the cell containing $x$.

**Example:** Consider the partition of 8 elements into 3 cells as follows.
$$
\{0, 2 | 1, 3, 5|4, 6, 7\}
$$

We could represent this as an array as follows

|  $x$ | 0  |  1 | 2  |  3 | 4  |  5 | 6  |  7 |
|---|---|---|---|---|---|---|---|---|
|  $\pi(x)$ | 0  |  1 | 0  |  1 | 4  |  1 | 4  |  4 |
