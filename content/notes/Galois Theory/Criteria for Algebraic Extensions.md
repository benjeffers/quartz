---
title: "Criteria for Algebraic Extensions"
date: "2023-05-29"
time: "21:03"
tags:
- galois-theory
---

**Proposition 1.** Let $K$ be a field extension of $F$. If each $\alpha\_i \in K$ is algebraic over $F$, then $F[\alpha\_1, \ldots , \alpha\_n]$ is a finite dimensional field extension of $F$ with 
$$
[F[\alpha\_1, \ldots , \alpha\_n] : F] \leq \prod\_{i=1}^n [F(\alpha\_i): F]. 
$$

*Proof.* We induct on $n$. The base case of $n = 1$ follows from a basic proposition on the [generators of fields](notes/Galois%20Theory/Generators%20of%20Fields.md). For the induction step assume that $L = F[\alpha\_1, \ldots , \alpha\_{n-1}]$ is a field and that $[L:F] \leq \prod\_{i=1}^n [F(\alpha\_1):F]$. Then 
$$
F[\alpha\_1, \ldots , \alpha\_n] = L[\alpha\_n]
$$is a field since $\alpha\_n$ is algebraic over $L$ since the [minimal polynomial](notes/Galois%20Theory/Minimal%20Polynomials.md) $\min(L, \alpha\_n)$ divides $\min(F, \alpha\_n)$. Thus we have $[F[\alpha\_1, \ldots , \alpha\_n]:L] \leq [F(\alpha\_n):F]$. Hence by the [multiplicity of degrees](notes/Galois%20Theory/Transitivity%20of%20Algebraic%20Field%20Extensions.md) and the induction hypothesis 
$$
[F[\alpha\_1, \ldots , \alpha\_n]: F] = [F[\alpha\_1, \ldots ,\alpha\_n]:L][L:F] \leq \prod\_{i=1}^n [F(\alpha\_i):F]. 
$$

**Example.** The above inequality can in fact be strict. In this case there is some interaction between the extensions. Take $a = \sqrt[4]{2}$ and $b = \sqrt[4]{18}$. Then 
$$
[\mathbb Q(a):\mathbb Q] = [\mathbb Q(b):\mathbb Q] = 4
$$since the polynomials $x^4 -2$ and $x^4 - 18$ are irreducible over $\mathbb Q$ by $[Eisenstein's Criterion](notes/Galois%20Theory/Eisenstein's%20Criterion.md) both with the prime $2$. However, $\mathbb Q(a, b) = \mathbb Q(\sqrt[4]{2}, \sqrt{3})$, which has degree 8 over $\mathbb Q$. Indeed, note that $(b/a)^4 = 9$, so $b/a = \sqrt{3}$. Thus $\sqrt{3} \in \mathbb Q(a, b)$ which shows that $\mathbb Q(\sqrt[4]{2}, \sqrt{3}) \subseteq \mathbb Q(a, b)$. For the other direction note that $\sqrt[4]{18} = \sqrt[4]{2}\cdot \sqrt{3}$. The last thing to show is that $[\mathbb Q(\sqrt[4]{2}, \sqrt{3}):\mathbb Q] = 8$. To see this note that the [minimal polynomial](notes/Galois%20Theory/Minimal%20Polynomials.md) of $\sqrt{3}$ over $\mathbb Q(\sqrt[4]{2})$ is $x^2 - 3$, since $3$ has no other square in $\mathbb Q(\sqrt[4]{2})$. Thus 
$$
[\mathbb Q(\sqrt[4]{2}, \sqrt{3}):\mathbb Q] = [\mathbb Q(\sqrt[4]{2}, \sqrt{3}): \mathbb Q(\sqrt[4]{2})] [\mathbb Q(\sqrt[4]{2}):\mathbb Q] = 2 \cdot 4 = 8.
$$So in this case the equality is strict. 

As a result of this we get a nice criteria for a field extension to be algebraic.

**Corollary 2.** If $K/F$ is a [field extension](notes/Galois%20Theory/Basic%20Definitions%20for%20Fields.md), then $\alpha \in K$ is [algebraic](notes/Galois%20Theory/Algebraic%20Field%20Extensions.md) over $F$ is and only if $[F(\alpha):F] < \infty$. Moreover, if $[K:F] < \infty$, then $K$ is [algebraic](notes/Galois%20Theory/Algebraic%20Field%20Extensions.md) over $F$. 

Note that the converse of the second statement is false. If $K/F$ is an algebraic extension that it is not necessarily true that $[K:F]<\infty$ as can be seen in the following example.

**Example.** Let $\mathbb A$ be a the [algebraic closure](notes/Galois%20Theory/Algebraic%20Closure.md) of $\mathbb Q$ in $\mathbb C$. Then by definition $\mathbb A/\mathbb Q$ is algebraic. To see that it has infinite dimension, note that $\sqrt[n]{2}$ is algebraic over $\mathbb Q$ for every $n$. Indeed, by [Eisenstein's Criterion](notes/Galois%20Theory/Eisenstein's%20Criterion.md) $x^n - 2$ is irreducible over $\mathbb Q$ for every $n \in \mathbb N$. Thus $\mathbb Q(\sqrt[n]{2}) \subseteq \mathbb A$, so 
$$
n = [\mathbb Q(\sqrt[n]{2}) :\mathbb Q] \leq [\mathbb A :\mathbb Q]
$$for all $n \in \mathbb N$, thus $[\mathbb A :\mathbb Q] = \infty$. 

Finally we reach the nice criterion for an extension to be algebraic.

**Proposition 3.** Let $K$ be a field extension of $F$, and let $X \subseteq K$ be such that each element of $X$ is algebraic over $F$. Then $F(X)$ is algebraic over $F$. If $|X| < \infty$, then $[F(X):F] < \infty$. 

*Proof.* Let $a \in F(X)$ then by Proposition 3 of [Generators of Fields](notes/Galois%20Theory/Generators%20of%20Fields.md), there exists $\alpha\_1, \ldots , \alpha\_n \in X$ with $a \in F(\alpha\_1, \ldots , \alpha\_n)$. By Proposition 1 above, $F(\alpha\_1, \ldots , \alpha\_n)$ is algebraic over $F$. Thus $a$ is algebraic over $F$ and, hence $F(X)$ is algebraic over $F$. If $|X| < \infty$, then $[F(X):F]<\infty$ by Proposition 1 above as well. 

