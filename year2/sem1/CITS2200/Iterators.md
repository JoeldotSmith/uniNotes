# Iterators
---

Used to *traverse* a collection

In lab exercises we have seen a Stack where we can only access the top element of the stack.


#### Fail Fast Iterators

What happens if a backing collection changes during use of an iterator?

eg. multiple iterators that impement `remove()`

**One Solution:** Disallow further use of itertor (throw exception) when an unexpected change to backing collection has occured. *Fail Fast Method*

#### Inner Classes

The Inner class is able to access all of the private fields and mothods of the outer class.

This gives us a very powerful method to control access to a data structure. The code of the inner class has free range over the instance variables of the outer class, but users can only access the inner class through the prescribed interface.

Inner classes are used extensively in object oriented programming for *call backs, remote method invocation, or listener classes.*

#### Trees and Graphs

##### Binary Trees

**Definition** A binary (*indexed*) tree $T$ of $n$ nodes, $n \geqslant 0$, either:
- is empty if n = 0, or
- consists of a *root node u* and two binary trees $u(1)$ and $u(2)$ of $n_1$ and $n_2$ nodes respectivly such that $n = 1 + n_1 + n_2$.
  - $u(1)$: first or left subtree
  - $u(2)$: second or right subtree

    
    The function $u$ is called the index

**Definition**: Let $w_1, w_2$ be the roots of the subtrees $u_1, u_2$ of $u$. Then:

- $u$ is the parent of $w_1$ and $w_2$
- $w_1, w_2$ are the left and right children of $u$. $u(i)$ is also called the $i$th child
- $w_1, w_2$ are siblings

A leaf is an internal node whose left and right subtrees are both empty (external nodes)

