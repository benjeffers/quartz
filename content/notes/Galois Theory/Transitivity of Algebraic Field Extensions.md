---
title: "Transitivity of Algebraic Field Extensions"
date: "2023-05-26"
time: "19:59"
tags:
- galois-theory
---
This note proves two transitive properties of field extensions, the first is of the degree of fields, and the second is about algebraic field extensions. We need a lemma first. 

**Lemma 1.** If $K$ is a [finite extension](notes/Galois%20Theory/Basic%20Definitions%20for%20Fields.md) of $F$, then $K$ is [algebraic](notes/Galois%20Theory/Algebraic%20Field%20Extensions.md) and finitely generated over $F$.

*Proof.* Suppose that $\alpha\_1, \ldots , \alpha\_n$ is a basis for $K$ over $F$. Then every element of $K$ is of the form $\sum\_i a\_i \alpha\_i$ with $a\_i \in F$, so we have that $K = F(\alpha\_1, \ldots , \alpha\_n)$. Thus $K$ is finitely generated over $F$. If $a \in K$, then $\lbrace 1, a, \ldots , a^n \rbrace$ is linearly dependent over $F$, since $[K : F] = n$. Thus, there are $\beta\_i \in F$, not all zero, with $\sum\_i \beta\_i a^i = 0$. If 
$$
f(x) = \sum\_i \beta\_ix^i,
$$then $f(x) \in F[x]$ and $f(a) = 0$. Therefore, $a$ is algebraic over $F$, and so $K$ is algebraic over $F$. 

Now we come to a very useful result that will be used over and over again.

**Theorem 2.** Let $F \subseteq L \subseteq K$ be fields. Then,
$$
[K:F] = [K:L]\cdot [L:F]. 
$$
*Proof.* Let $\lbrace a\_i \mid i \in I \rbrace$ be a basis for $L/F$ and $\lbrace b\_j \mid j \in J \rbrace$ a basis for $K/L$. We will show that 
$$
\lbrace a\_ib\_j \mid i \in I, j \in J \rbrace
$$is a basis for $K/F$. If $x \in K$, then $x = \sum\_j \alpha\_j b\_j$ for some $\alpha\_j \in L$, with only finitely many of the $\alpha\_j \neq 0$. But $\alpha\_j = \sum\_i \beta\_{ij}a\_i$ with only finitely many of the $\beta\_{ij} \neq 0$. Thus 
$$
x = \sum\_{i, j} \beta\_{ij}a\_i b\_j
$$so the $\lbrace a\_i b\_j \rbrace$ space $K$ as an $F$-vector space. For linear independence, if $\sum\_{i,j}\beta\_{ij}a\_ib\_j = 0$ with $\beta\_{ij} \in F$, then the independence of the $b\_j$ over $L$ show that $\sum\_i \beta\_{ij}a\_i = 0$ for each $j$. However, the independence of the $a\_i$ over $F$ imply that $\beta\_{ij} = 0$ for each $i, j$. Thus the $a\_ib\_j$ are independent over $F$, giving the result. 

Note that in neither the statement nor the proof do we require the field extensions to be of finite degree. This proof works equally well for infinite extensions. 

As a quick application of this result we get the following. 

**Lemma 3.** Let $K/F$ be a field extension. Then $[K:F] = 1$ if and only if $K = F$.

*Proof.* Suppose that $K \supset F$. Then there is $\alpha \in K\backslash F$. We claim that the set $\lbrace 1, \alpha \rbrace$ is linearly independent. Indeed, suppose $0 = c\_1 + c\_2 \alpha$. If $c\_1 = 0$, then $c\_2 = 0$ as well since $\alpha \neq 0$. If $c\_1 \neq 0$, then $\alpha = -c\_1/c\_2 \in F$ which is a contradiction. Thus $1$ and $\alpha$ are linearly independent so $[K:F] \geq 2$. Conversely, suppose $K = F$. Then $\lbrace 1 \rbrace$ is a basis for $K$ over $F$ and thus $[K:F] = 1$.  

**Corollary 4.** If $K/F$ is a [finite extension](notes/Galois%20Theory/Basic%20Definitions%20for%20Fields.md) such that $[K:F]$ is prime, then there are no intermediate subfields between $K$ and $F$.

*Proof.* Suppose $F \subseteq L \subseteq K$. Then by the above theorem 
$$
[K:F] = [K:L][L:F]
$$but since $[K:F]$ is prime, either $[K:L] = 1$ and $K = L$ or $[L:F] = 1$ and $L = F$, by  Lemma 3 above. Thus there are no intermediate field extensions. 

Now we reach the main result of this note. 

**Theorem 4.** Let $F \subseteq L \subseteq K$ be fields. If $L/F$ and $K/L$ are [algebraic](notes/Galois%20Theory/Algebraic%20Field%20Extensions.md), then $K/F$ is algebraic. 

*Proof.* Let $\alpha \in K$, and let $f(x) = x^n + \cdots + a\_1 x + a\_0$ be the [minimal polynomial](notes/Galois%20Theory/Minimal%20Polynomials.md) of $\alpha$ over $L$. Since $L/F$ is algebraic, the field $L\_0 = F(a\_0, \ldots , a\_{n-1})$ is a finite extension of $F$ by Corollary 2 in [Criteria for Algebraic Extensions](notes/Galois%20Theory/Criteria%20for%20Algebraic%20Extensions.md). Now $f(x) \in L\_0[x]$, sp $\alpha$ is algebraic over $L\_0$. Thus 
$$
[L\_0(\alpha):F] = [L\_0(\alpha):L\_0] \cdot [L\_0:F]< \infty. 
$$Because $F(\alpha) \subseteq L\_0(\alpha)$, we see that $[F(\alpha):F] < \infty$, so $\alpha$ is algebraic over $F$. Since this is true for all $\alpha \in K$, we have shown that $K/F$ is algebraic. 