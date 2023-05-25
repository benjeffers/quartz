---
title: "Gauss' Lemma"
date: "2023-05-24"
time: "17:23"
tags:
- galois-theory
---
Gauss' lemma is super important and it will help us prove [[Eisenstein's criterion]]. We will make a quick definition and state a lemma, and then prove the two main propositions.

**Definition (Content, Primitive).** Let $R$ be a UFD, and let $f(x) \in R[x]$. The *content*, $c(f)$, of $f$ is the $\gcd$ of the coefficients of $f$. If the content of $f$ is 1, then $f$ is called *primitive.* 

**Lemma.** Let $R$ be a ring and let $I$ be an ideal of $R$. Then the map $\varphi \colon R[x] \to (R/I)[x]$ given by 
$$
\varphi \left(\sum a\_ix^i \right) = \sum \left(a\_i + I \right)x^i
$$is a surjective ring homomorphism. 

Note that both of the following propositions are sometimes given the name Gauss' Lemma. 

**Proposition.** Let $R$ be a UFD, and let $f, g \in R[x]$. Then $c(fg) = c(f)c(g)$. In particular, if $f$ and $g$ are primitive, then $fg$ is primitive. 

*Proof.* Write $f(x) = c(f)f\_1(x)$ and $g(x) = c(g)g\_1(x)$ for some primitive polynomials $f\_1$ and $g\_1$. So 
$$
fg = c(f)c(g)f\_1g\_1.
$$To finish the proposition we just need to show that the product of primitive polynomials is primitive. Suppose $f$ and $g$ are primitive. If $fg$ is not primitive, then there is a prime element $\pi$ that divides all of the coefficients of $fg$. Consider the polynomial ring $R/(\pi)[x]$ over $R/(pi)$. Since $\pi$ is prime, $R/(\pi)$ is an integral domain. Let $\overline f$ and $\overline g$ be the images of $f$ and $g$ in $R/(\pi)[x]$. Since $f$ and $g$ are primitive, $\pi$ does not divide all the coefficients of $f$ or $g$, so $\overline f \neq 0$ and $\overline g \neq 0$. Therefore $\overline f \cdot \overline g = \overline{fg}$ by the lemma, and $\overline f \cdot \overline g \neq 0$ since $R/(\pi)[x]$ is an integral domain. However, if $\pi$ divides all the coefficients of $fg$, then $\overline{fg} = 0$, a contradiction. 

**Theorem (Gauss' Lemma).** Let $R$ be a UFD, let $F$ be its quotient field and let $f(x) \in R[x]$. Then $f$ is irreducible over $R$ if and only if $f$ is primitive and irreducible over $F$. 

*Proof.* Suppose $f$ is primitive and irreducible over $F$. If $f$ factors in $R[x]$ as $f = gh$ with neither $g$ nor $h$ a unit in $R[x]$, then since $f$ is irreducible over $F$, either $g$ or $h$ must be a constant. But if $g$ is a constant, then $g$ would divide all the coefficients of $gh = f$. This is impossible, since $f$ is primitive, so $f$ is irreducible over $R$. 

Conversely, suppose $f$ is irreducible over $R$. Since we can write $f = c(f)f\_1$, with $f\_1$ primitive, $c(f)$ is a unit in $R[x]$, hence $c(f)$ is a unit in $R$, so $f$ is primitive. If $f$ is not irreducible over $F$, then we can write $f = gh$ with $g, h \in F[x]$ both of degree at least 1. By using common denominators, we can write 
$$
gh = \frac{a}{b}g\_1h\_1
$$ where $g\_1, h\_1 \in R[x]$ are primitive and $a, b \in R$ are relatively prime. Then $bf = ag\_1h\_1$, but by the previous proposition, we have $b = c(bf) = a$, since $g\_1, h\_1$ are primitive. But this contradicts $\gcd(a, b) = 1$ unless $a$ and $b$ are both units in $R$. If $a$ and $b$ are units in $R$, then $f = (ag\_1)(\frac{1}{b}h\_1)$ is a nontrivial factorization of $f$ in $R[x]$, a contradiction. 