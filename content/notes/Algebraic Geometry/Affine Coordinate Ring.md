---
title: "Affine Coordinate Ring"
date: "2023-05-25"
time: "19:30"
tags:
- algebraic-geometry
---
We can view elements of $k[x\_1, \ldots , x\_n]$ as functions on $\mathbb A^n$ by evaluating them at points of $k^n$. We can extend this idea to [affine varieties](notes/Algebraic%20Geometry/Affine%20Variety.md) by defining the coordinate ring. 

**Definition.** Let $Y \subseteq \mathbb A^n$ be an affine algebraic set. We define the *affine coordinate ring* $A(Y)$ of $Y$ to be $k[x\_1, \ldots , x\_n]/I(Y)$. 

Now, two functions $f, g$ of $k[x\_1, \ldots , x\_n]$ restrict to the same function on $Y \subseteq \mathbb A^n$ when $f-g \in I(Y)$. The coordinate ring of $Y$ consists of all polynomial functions on $Y$, and factors out the ones that vanish on $Y$, i.e., $I(Y)$. 