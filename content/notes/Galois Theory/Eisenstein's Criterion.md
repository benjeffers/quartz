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

*Proof.* By factoring out the [content](notes/Galois%20Theory/Gauss'%20Lemma.md) of $f$, we may assume that $f$ is [primitive](notes/Galois%20Theory/Gauss'%20Lemma.md). Consider the ring $R/(\pi)[x]$, and let $\overline h$ denote the image of $h \in R[x]$. The condition on the coefficients of $f$ shows that $\overline f = \overline{a\_n}x^n \neq 0$. Suppose that $f$ factors over $F$. Then by [Gauss' Lemma](notes/Galois%20Theory/Gauss'%20Lemma.md), $f$ also factors over $R$. Say $f = gh$ with $g, h \in R[x]$ both non-constant polynomials. Then $\overline f = \overline g \overline h$ in $R/(\pi)[x]$ since the map 

$$
\begin{align*}
\varphi \colon R\[x\] \to& \\; (R/(\pi))\[x\] \\
\sum a\_i x^i =&\\; \sum \left( a\_i + I \right)x^i
\end{align*}
$$
is a surjective ring homomorphism. Then, since $\overline f = \overline{a\_n}x^n$, $\overline g$ and $\overline h$ must be of the form $xc^i$. If $\deg(\overline g)$ and $\deg(\overline h)$ are both positive, then $\pi$ divides the constant term of both $g$ and $h$. But $a\_0$ is the product of these terms, which would force $\pi^2$ to divide $a\_0$, which is false. Therefore, either $\overline g$ or $\overline h$ is a constant. Since $g$ and $h$ are non-constant $\pi$ divides the leading coefficient of $g$ or $h$. But $a\_n$ is the product of these leading coefficients, so $\pi$ would divide $a\_n$ which is false. Thus $f$ must be irreducible over $F$. 

**Examples.**
1. The polynomial $x^5 - 12x^3 + 2x + 2$ is irreducible by Eisenstein's Criterion with $\pi = 2$ since $2$ divdes $2, 2$ and $12$, but not $1$, the coefficient in front of $x^5$, and $2^2 = 4$ does not divide the constant coefficient, $2$. 
2. Similarly, with $\pi = 3$, the polynomial $x^3 - 3x + 3$ is irreducible.
3. Eisenstein's criterion cannot always be used though since no prime satisfies the conditions for the polynomial $x^4 + 2x + 4$. 