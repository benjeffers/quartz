---
title: "Rational Root Test"
date: "2023-05-24"
time: "17:07"
tags:
- galois-theory
---
We start by proving one of the most basic reducibility tests for polynomials. 

**Proposition (Rational Root Test).** Let $R$ be a UFD with quotient field $F$. Suppose that $f(x) = a\_0 + \cdots + a\_nx^n \in R[x]$ has a root $\alpha/\beta \in F$ with $\gcd(\alpha, \beta) = 1$. Then $\alpha$ divides $a\_0$ and $\beta$ divides $a\_n$. If $\deg(f) \leq 3$ then $f$ is irreducible if and only if it has no roots in $F$.

*Proof.* First, multiply the equation $f(\alpha/\beta) = 0$ by $\beta^n$ to obtain the equation 
$$
a\_n \alpha^n + a\_1 \alpha^{n-1}\beta + \cdots + a\_1 \alpha \beta^{n-1} + a\_0 \beta = 0.
$$Therefore, $a\_0 \beta = -\alpha(a\_1\beta^{n-1} + \cdots + a\_{n-1}\alpha^{n-2} \beta + a\_n \alpha^{n-1})$. Since $\alpha$ is relatively prime to $\beta$, it follows that $\alpha$ divides $a\_0$. By a similar manipulation we see that $\beta$ divides $a\_n$. 

Finally, if $f$ has degree 2 or 3, then $f$ has a linear factor if and only if it is reducible over $F$. \

**Examples.** 
- The polynomial $x^2 - p \in \mathbb Q\[x\]$  is irreducible if $p$ is prime. This can be seen from the rational root test since a factor must be of the form $\alpha/\beta$ where $\alpha$ divides $p$ and $\beta$ divides 1, so the only possibilities of roots are $\pm p$, but $p^2 - p \neq 0$ and $(-p)^2 - p \neq 0$, so the polynomial is irreducible.
- Similar to the above the polynomial $x^3 + 3x + 1$ is irreducible over $\mathbb Q\[x\]$. The only possible roots are $\pm 1$, neither of which is actually a root.
- The cubic $x^3 + 2x - 4x + 1$ could have roots $\pm 1$ and we see that $1^3 + 2 \cdot 1^2 - 4 \cdot 1 + 1 = 0$, so $x-1$ divides the polynomial and it is irreducible.
- The polynomial $x^4 - 4 = (x^2 - 2)(x^2 + 2)$ factors but has no rational roots. 