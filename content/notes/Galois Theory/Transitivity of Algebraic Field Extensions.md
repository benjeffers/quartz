---
title: "Transitivity of Algebraic Field Extensions"
date: "2023-05-26"
time: "19:59"
tags:
- galois-theory
---
This note proves two transitive properties of field extensions, the first is of the degree of fields, and the second is about algebraic field extensions. We need a lemma first. 

**Lemma.** If $K$ is a [finite extension](notes/Galois%20Theory/Basic%20Definitions%20for%20Fields.md) of $F$, then $K$ is [algebraic](notes/Galois%20Theory/Algebraic%20Field%20Extensions.md) and finitely generated over $F$.

*Proof.* Suppose that $\alpha\_1, \ldots , \alpha\_n$ is a basis for $K$ over $F$. Then every element of $K$ is of the form $\sum\_i a\_i \alpha\_i$ with $a\_i \in F$, so we have that $K = F(\alpha\_1, \ldots , \alpha\_n)$. Thus $K$ is finitely generated over $F$. If $a \in K$, then $\lbrace 1, a, \ldots , a^n \rbrace$ is linearly dependent over $F$, since $[K : F] = n$. Thus, there are $\beta\_i \in F$, not all zero, with $\sum\_i \beta\_i a^i = 0$. If 
$$
f(x) = \sum\_i \beta\_ix^i,
$$then $f(x) \in F[x]$ and $f(a) = 0$. Therefore, $a$ is algebraic over $F$, and so $K$ is algebraic over $F$. 
