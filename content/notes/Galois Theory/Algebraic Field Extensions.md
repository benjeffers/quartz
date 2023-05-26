---
title: "Algebraic Field Extensions"
date: "2023-05-25"
time: "20:31"
tags:
- galois-theory
---
**Definition (Algebraic Element, Transcendental Element).** If $K$ is a field extension of $F$, then an element $\alpha \in K$ is *algebraic* over $F$ if there is a nonzero polynomial $f(x) \in F[x]$ with $f(\alpha) = 0$. If $\alpha$ is not algebraic over $F$, then $\alpha$ is said to be *transcendental* over $F$.  If every element of $K$ is algebraic over $F$, then $K$ is said to be *algebraic* over $F$, and $K/F$ is called an *algebraic extension*. 

**Examples.** 
1. The complex number $i = \sqrt{-1}$ is algebraic over $\mathbb Q$, since $i^2 + 1 = 0$. 
2. If $r \in \mathbb Q$, then $a = \sqrt[n]{r}$ is algebraic over $\mathbb Q$ since $a$ is a root of $x^n- r$. 
3. If $\omega = e^{2\pi i/n} = \cos(2\pi/n) + i \sin(2\pi/n)$, then $\omega^n - 1= 0$, so $\omega$ is algebraic over $\mathbb Q$.
4. In the nineteenth century Hermite proved that $e$ is transcendental over $\mathbb Q$, and Lindemann proved that $\pi$ is transcendental over $\mathbb Q$. 
