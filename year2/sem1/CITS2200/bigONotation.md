# Big O Notation
---
Use Big O notation (BON) for comparing growth rates.
#### Definition
$f(n)$ is $O(g(n))$ if there is a constant $c > 0$ and an integer $n_o \geqslant 1$ such that, for all of $ n \geqslant n_o$,
$$ f(n) \leqslant cg(n). $$

#### Proof (by contradiction)
Assume that $n^3$ is $O(n^2)$. Then there exisrs *some* $c >0$ and $n_o \geqslant 1$ such that $$ n^3 \leqslant cn^2 $$ for all $n \leqslant c$ for all $n \geqslant n_o$, but that is impossible, as $n$ grows and $c$ is a constant.

From this we can see that BON focuses on *dominating terms*.

For non-polynomials identifying dominating terms may be more difficult.
Most common is CS
- polynomials - $1, n, n^2, n^3....$ *Usually low degree*
- exponentials - $2^n,....$*Corresponds to computational explosion*
- logarithmic - $\log n, .....$
- 