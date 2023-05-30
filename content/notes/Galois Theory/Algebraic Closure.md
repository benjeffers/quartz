---
title: "Algebraic Closure"
date: "2023-05-29"
time: "21:24"
tags:
- galois-theory
---
**Definition (Algebraic Closure).** Let $K$ be a field extension of $F$. The set 
$$
\lbrace \alpha \in K \mid \alpha \text{ is algebraic over }F \rbrace
$$is called the *algebraic closure* of $F$ in $K$. 

**Proposition.** Let $K$ be a [field extension](notes/Galois%20Theory/Basic%20Definitions%20for%20Fields.md) of $F$, and let $L$ be the algebraic closure of $F$ in $K$. Then $L$ is a field, and therefore is the largest algebraic extension of $F$ contained in $K$.

*Proof.* Let $a, b \in L$. Then $F(a, b)$ is algebraic over $F$ by a [criteria for algebraic extensions](notes/Galois%20Theory/Criteria%20for%20Algebraic%20Extensions.md), so $F(a, b) \subseteq L$ and since $a \pm b, ab, a/b \in F(a, b) \subseteq L$, the set $L$ is closed under the field operations, so it is a subfield of $K$. Each element of $K$ that is algebraic over $F$ lies in $L$, which means that $L$ is the largest algebraic extension of $F$ contained in $K$. 
