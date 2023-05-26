---
title: "Radical Ideals and Algebraic Sets"
date: "2023-05-25"
time: "19:13"
tags:
- algebraic-geometry
---
We record here a fact that comes directly from [Hilbert's Nullstellensatz](notes/Algebraic%20Geometry/Hilbert's%20Nullstellensatz.md) and gives a way to pass from algebra to geometry. 

**Theorem.** There is a one-to-one inclusion-revering correspondence between [algebraic sets](notes/Algebraic%20Geometry/Algebraic%20Sets.md) in $\mathbb A^n$ and radical ideals in $k[x\_1, \ldots , x\_n]$. 

*Proof.* Let $\mathfrak a$ be a radical ideal in $k[x\_1, \ldots , x\_n]$. Then $I(Z(\mathfrak a)) = \sqrt{\mathfrak a} = \mathfrak a$ by [Hilbert's Nullstellensatz](notes/Algebraic%20Geometry/Hilbert's%20Nullstellensatz.md). Next, let $X$ be an [algebraic set](notes/Algebraic%20Geometry/Algebraic%20Sets.md) in $\mathbb A^n$. Then $Z(I(X)) = \overline X = X$, since $X$ is an algebraic set, so it is closed in $\mathbb A^n$. Thus we have a bijection between radical ideals and algebraic sets. 
