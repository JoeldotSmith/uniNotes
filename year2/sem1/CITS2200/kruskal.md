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


Then certainly the operation **Find** is straight foreward - we can decide whether $x, y$ are in the same cell by comparing $\pi(x)$ with $\pi(y)$

Therefore **Find** has complexity $O(1)$

#### Updating the partition

Suppose now that we wish to update the partition by merging the first two cells. 

We could update the data structure by running through the entire array and updating it as necessary.

This takes time $O(n)$ and hence the merging operation is rather slow.

#### Union by rank heuristic

There are two heuristics that can be applied to the new data structure, that speed things up enormously at the cost of maintaining a little extra data.

Let the rank of a root node of a tree be the height of that tree (the maximum distance from a leaf to the root).

The union by rank heastic tries to keep the trees balanced at all times. When a merging operation needs to be done, the root of the shorter tree is made to point to the root of the taller tree, The resulting tree therefore does not increase its height unless both tress are the same height in which case the tree height increases by 1.

#### Path compression heuristic

The path compression heuristic is based on the idea that when we perform a **Find(x)** operation we have to follow a path from $x$ to the root of the tree containing $x$.

After we have done this why do we not somply go back down through this path and make all these elements point directly to the root of the tree, rather than in a long chain through each other. 

This is reminiscent of our naive algorithm, where we made every element point directly to the leader of its cell, but it is much cheaper becasue we only alter things that we needed to look at anyway.

#### Complexity of Kruskal


In the worst case, we will perform $E$ operations on the partition data structure which has size $V$. By the complicated argument in CLRS we see that the total time for these operations if we use both hueristics is $O(Elg*V)$

Note $lg*x$ is the iterated log function, which grows extremely slowly with x.


However we must add to this time that is needed to sort the edges because we have to examine the edges in order of length. This time is $O(ElgE)$ if we use a sorting algorithm technique such as merge sort.