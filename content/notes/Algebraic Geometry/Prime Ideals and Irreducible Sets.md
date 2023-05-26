---
title: "Prime Ideals and Irreducible Sets"
date: "2023-05-25"
time: "19:02"
tags:
- algebraic-geometry
---
Here we find another theorem that lets us pass back and forth between algebra and geometry.

**Theorem.** An [algebraic set](notes/Algebraic%20Geometry/Algebraic%20Sets.md) is [irreducible](notes/Algebraic%20Geometry/Irreducible%20Spaces.md) if and only if its [vanishing ideal](notes/Algebraic%20Geometry/Vanishing%20Ideal.md) is a prime ideal.

*Proof.* Suppose that $Y$ is an irreducible algebraic set. We will show that $I(Y)$ is prime. Indeed, if $fg \in I(Y)$, then $Y \subseteq Z(fg) = Z(f) \cup Z(g)$. Thus we can write $Y = (Y \cap Z(f)) \cup (Z \cap Z(g))$ and both of these are closed subsets of $Y$. Since $Y$ is irreducible, we either have $Y = Y \cap Z(f)$, in which case $Y \subseteq Z(f)$ or $Y \subseteq Z(g)$. Either way $f \in I(Y)$ or $g \in I(Y)$ since 
$$
I(Y) \supseteq I(Z(f)) \ni f \text{ or } I(Y) \supseteq I(Z(g)) \ni g.
$$
Conversely, let $\mathfrak p$ be a prime ideal, and suppose that $Z(\mathfrak p) = Y\_1 \cup Y\_2$. We can take our algebraic set here to be $Z(\mathfrak p)$ since if we started with an arbitrary algebraic set $X$ and assumed that $I(X) = \mathfrak p$, then $X = Z(I(X)) = Z(\mathfrak p)$ since there is a bijection between radical ideals and algebraic sets. Then, we have 
$$
Z(\mathfrak p) = Y\_1 \cup Y\_2 \implies \mathfrak p I(Z(\mathfrak p)) = I(Y\_1 \cup Y\_2) = I(Y\_1) \cap I(Y\_2)
$$so either $\mathfrak p = I(Y\_1)$ or $\mathfrak = I(Y\_2)$. Thus $Z(\mathfrak p) = Y\_1$ or $Y\_2$ and it is irreducible. 


This theorem gives us a simpler tool to determine which algebraic sets are irreducible.

**Examples.**
1. The affine space $\mathbb A^n$ is irreducible since $I(\mathbb A^n) = (0)$ which is prime in $k[x\_1, \ldots , x\_n]$ since it is an integral domain.
2. Let $f$ be an irreducible polynomial in $A = k[x, y]$. Then $(f)$ is a prime ideal since it is irreducible and $A$ is a UFD. And thus the zero set $Y = Z(f)$ is irreducible. It is called the *affine curve* defined by the equation $f(x, y) = 0$. If $f$ has degree $d$, we say that $Y$ is a curve of *degree $d$*. 
3. If $f$ is an irreducible polynomial in $k[x\_1, \ldots , x\_n]$, we obtain an [affine variety](notes/Algebraic%20Geometry/Affine%20Variety.md) $Y = Z(f)$, which is called a *surface* if $n = 3$, or a *hypersurface* if $n > 3$. 