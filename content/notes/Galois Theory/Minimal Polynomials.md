---
title: "Minimal Polynomials"
date: "2023-05-25"
time: "20:36"
tags:
- galois-theory
---
The minimal polynomial is an extremely useful tool to determine the degree of a field extension as well as other properties. 

**Definition (Minimal Polynomial).** If $\alpha$ is [algebraic](notes/Galois%20Theory/Algebraic%20Field%20Extensions.md) over a field $F$, then the *minimal polynomial* of $\alpha$ over $F$ is the monic polynomial $p(x)$ of least degree in $F[x]$ for which $p(\alpha) = 0$; we denote it as $\min(F, \alpha)$. Equivalently, $\min(F, \alpha)$ is the monic generator of $p(x)$ of the kernel of the evaluation homomorphism $ev_\alpha$. 

**Examples.**
1. For the complex number $i$ we have that $\min(\mathbb Q, i) = x^2 + 1 = \min(\mathbb R, i)$. However, $\min(\mathbb C, i) = x-i$, so the minimal polynomial greatly depends on the base field. 
2. Let $a= \sqrt[n]{r}$. Then $\min(\mathbb Q, a) = x^n - r$. 

**Proposition.** Let $K$ be a [field extension](notes/Galois%20Theory/Basic%20Definitions%20for%20Fields.md) of $F$ and let $\alpha \in K$ be [algebraic](notes/Galois%20Theory/Algebraic%20Field%20Extensions.md) over $F$. Then 
1. the polynomial $\min(F, \alpha)$ is irreducible over $F$;
2. if $g(x) \in F\[x\]$, then $g(\alpha) = 0$ if and only if $\min(F, \alpha)$ divides $g(x)$. 
3. If $n = \deg(\min(F, \alpha))$, then the elements $1, \alpha, \ldots , \alpha^{n-1}$ form a basis over $F$, so $[F(\alpha):F] = \deg(\min(F, \alpha)) < \infty$. Moreover, $F(\alpha) = F[\alpha]$. 

*Proof.* 
1. If $p(x) = \min(F, \alpha)$, then $F\[x\](p(x)) \cong F\[\alpha\]$ is an integral domain. Indeed, the map $ev_\alpha \colon F\[x\] \to F\[\alpha\]$ has kernel generated by $p(x)$. Thus $(p(x))$ is a prime ideal, so $p(x)$ is irreducible. 
2. If $g(x) \in F\[x\]$ with $g(\alpha) = 0$, then $g(x) \in \ker(ev_\alpha)$. But this kernel is generated by $p(x)$, so $p(x)$ divides $g(x)$. 
3. We first prove that $F\[\alpha\] = F(\alpha)$. To see this, note that $F\[\alpha\]$ is the image of the evaluation map $ev\_\alpha$. The kernel of $ev\_\alpha$ is a prime ideal since $ev\_\alpha$ maps $F\[x\]$ into an integral domain. However, $F\[x\]$ is a principal ideal domain, so every nonzero prime ideal of $F\[x\]$ is maximal. Thus, $\ker(ev\_\alpha)$ is maximal, and $F\[\alpha\] \cong F\[x\]/\ker(ev\_\alpha)$ is a field. Consequently, $F\[\alpha\] = F(\alpha)$. To finish the proof, let $n = \deg(p(x)$. If $b \in F(\alpha)$, then $b = g(\alpha)$ for some $g(x) \in F\[x\]$. By the division algorithm, $g(x) = q(x)p(x) + r(x)$, where $r(x) = 0$ or $\deg(r) < n$. Thus $b = g(\alpha) = r(\alpha)$. Since $r(\alpha)$ is an $F$-linear combination of $1, \alpha, \ldots , \alpha^{n-1}$, we see that $1, \alpha, \ldots , \alpha^{n-1}$ span $F(\alpha)$ as an $F$-vector space. If $\sum\_{i=o}^{n-1} a\_i \alpha^i = 0$, then $f(x) = \sum\_{i=o}^{n-1} a\_i x^i$ is divisible by $p(x)$, so $f(x) = 0$, or else $f$ is divisible by a polynomial of larger degree than itself. Thus, $1, \alpha, \ldots, \alpha^{n-1}$ is a basis for $F(\alpha)$ over $F$. 

**Examples.**
1. The minimal polynomial of $\sqrt[3]{2}$ over $\mathbb Q$ is $x^3 - 2$. Indeed, $x^3 - 2$ is monic and it is irreducible by [Eisenstein's Criterion](notes/Galois%20Theory/Eisenstein's%20Criterion.md) with the prime $2$. So $[\mathbb Q(\sqrt[3]{2}):\mathbb Q] = 3$. 
2. Let $p$ be a prime. Then $x^n - p$ is irreducible by [Eisenstein's Criterion](notes/Galois%20Theory/Eisenstein's%20Criterion.md) with the prime $p$, so $\sqrt[n]{p}$ has minimal polynomial $x^n -p$ and $[\mathbb Q(\sqrt[n]{p}) : \mathbb Q] = n$. 
3. The complex number $\omega = \cos(2\pi/3) + i \sin(2\pi/3) = e^{2\pi i/3}$ is a root of $x^3 -1$ over $\mathbb Q$. However, this polynomial factors as $x^3 - 1 = (x -1)(x^2 + x + 1)$. The second factor has $\omega$ as a root and is irreducible by the [Rational Root Test](notes/Galois%20Theory/Rational%20Root%20Test.md), hence it is the minimal polynomial of $\omega$ over $\mathbb Q$ and $[\mathbb Q(\omega) : \mathbb Q] = 2$. 