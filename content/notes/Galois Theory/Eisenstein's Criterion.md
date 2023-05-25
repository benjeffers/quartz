---
title: "Eisenstein's Criterion"
date: "2023-05-24"
time: "17:23"
tags:
- galois-theory
---
This seems to be the most useful irreducibility test, both in Galois theory and algebraic geometry. It is especially useful in algebraic geometry since it can be used for polynomials of multiple variables. 

**Theorem (Eisenstein's Criterion).** Let $R$ be a UFD with quotient field $F$, and let $f(x) = a\_0 + \cdots + a\_n x^n \in R[x]$. 
1. Suppose there is a prime element $\pi \in R$ such that $\pi$ divides $a\_0, \ldots , a\_{n-1}$, but not $a\_n$ and $\pi^2$ does not divide $a\_0$. Then $f$ is irreducible.
2. Suppose there is a prime element $\pi \in R$ that divides $a\_1, \ldots , a\_n$ but does not divide $a\_0$ and $\pi^2$ does not divide $a\_n$. Then $f$ is irreducible over $F$. 