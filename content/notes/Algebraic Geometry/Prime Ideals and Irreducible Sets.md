---
title: "Prime Ideals and Irreducible Sets"
date: "2023-05-25"
time: "19:02"
tags:
- algebraic-geometry
---
Here we find another theorem that lets us pass back and forth between algebra and geometry.

**Theorem.** An algebraic set is irreducible if and only if its ideal is a prime ideal.

*Proof.* Suppose that $Y$ is an irreducible algebraic set. We will show that $I(Y)$ is prime. Indeed, if $fg \in I(Y)$, then $Y \subseteq Z(fg) = Z(f) \cup Z(g)$. Thus we can write $Y = (Y \cap Z(f)) \cup (Z \cap Z(g))$ and both of these are closed subsets of $Y$. Since $Y$ is irreducible, we either have $Y = Y \cap Z(f)$, in which case $Y \subseteq Z(f)$ or $Y \subseteq Z(g)$. Either way $f \in I(Y)$ or $g \in I(Y)$ since 
$$
I(Y) \supseteq I(Z(f)) \ni f \text{ or } I(Y) \supseteq I(Z(g)) \ni g.
$$
Conversely, let $\mathfrak p$ be a prime ideal, and suppose that $Z(\mathfrak p) = Y\_1 \cup Y\_2$. We can take our algebraic set here to be $Z(\mathfrak p)$ since if we started with an arbitrary algebraic set $X$ and assumed that $I(X) = \mathfrak p$, then $X = Z(I(X)) = Z(\mathfrak p)$ since there is a bijection between radical ideals and algebraic sets. Then, we have 
$$
Z(\mathfrak p) = Y\_1 \cup Y\_2 \implies \mathfrak p I(Z(\mathfrak p)) = I(Y\_1 \cup Y\_2) = I(Y\_1) \cap I(Y\_2)
$$so either $\mathfrak p = I(Y\_1)$ or $\mathfrak = I(Y\_2)$. Thus $Z(\mathfrak p) = Y\_1$ or $Y\_2$ and it is irreducible. 