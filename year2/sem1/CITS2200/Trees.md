# General Trees
---
A general tree or multiway(indexed) tree is defined in a similar way to a binary tree except that a parent node does not need to have exactly two children.

**Definition**
A multiway(indexed) tree $T$ of $n$ nodes, $n \geqslant 0,$ either:
  - is empty, if $n = 0$ or,
  - consists of a root node $u$, an interger $d \geqslant 1$ called the degree of $u$, and $d$ multiway trees $u(1), u(2), ..., u(d)$, with sizes $n_1, n_2, ..., n_d$ respectively such that.
$$
n = 1+n_1+n_2+...+n_d
$$

A tree is a a d-ary tree if $d_u=d$ for all internal nodes $u$. We have already looked at binary (2-ary) trees.

A tree is an *(a-b)-tree* if $a \leqslant d_u \leqslant b, (a, b, \geqslant1)$, for all of $u$.