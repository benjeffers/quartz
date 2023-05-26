---
title: "Vanishing Ideal"
date: "2023-05-24"
time: "16:51"
tags:
- algebraic-geometry
- commutative-algebra
---
The [[notes/Algebraic Geometry/Algebraic Sets|zero set]] of an ideal in a polynomial ring gives us a way to get geometric information from algebraic data. The vanishing ideal allows us to go the opposite direction. These two operations will turn out to be near inverses of each other as can be seen in [[notes/Algebraic Geometry/Hilbert's Nullstellensatz]]. 

**Definition (Vanishing Ideal).** For a subset $X \subseteq \mathbb A^n$ we define the ideal $I(X)$ consisting of polynomials in $k[x\_1, \ldots, x\_n]$ that vanish along $X$; that is, 
$$
I(X) = \lbrace f \in k[x\_1, \ldots , x\_n] \mid f(x) = 0 \text{ for all } x \in X \rbrace.
$$

Note that this is inclusion-reversing. If $X \subseteq Y \subseteq \mathbb A^n$, and $f \in I(Y)$, then $f$ vanishes on all of $Y$, and hence on all of $X$, so $f \in I(X)$ and thus $I(Y) \subseteq I(X)$. This should make sense since there should be more polynomials that can vanish on a smaller set than on a bigger set. 

Another important thing to note is that $\mathfrak a \subseteq I(Z(\mathfrak a))$. To see this, take $f \in \mathfrak a$, then $f$ vanishes on a point that vanishes in $\mathfrak a$. Similarly, $X \subseteq Z(I(X))$. However in this case the inclusion might be strict. An example of this is if $X \subseteq \mathbb A^1$ is infinite, then $I(X) = 0$, so $Z(I(X)) = \mathbb A^1$. We can say something stronger here. 

**Proposition.** For $X \subseteq \mathbb A^1$, we have 
$$
Z(I(X)) = \overline X,
$$where $\overline X$ is the closure of $X$ under the [[notes/Algebraic Geometry/The Zariski Topology|Zariski Topology]]. 

*Proof.* Since $X \subseteq Z(I(X))$ and $Z(I(X))$ is a closed subset, we get the inclusion $Z(I(X)) \supseteq \overline X$. On the other hand, let $Z(\mathfrak b)$ be a closed subset that contains $X$. Then $f(x) = 0$ for all $f \in \mathfrak b$ and $x \in X$. Hence $\mathfrak b \subseteq I(X)$ and $Z(I(X)) \subseteq Z(\mathfrak b)$, since $Z(-)$ reverses inclusions. 

