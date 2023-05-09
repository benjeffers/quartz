---
title: "Hilbert Basis Theorem"
date: "2023-05-06"
time: "14:41"
tags:
- commutative-algebra
---
In this note we prove that a polynomial ring over a Noetherian ring is Noetherian. The idea of the proof is to take an ideal $I$ of $R[x]$ and create an ideal in $R$ that consists of all the leading coefficients of polynomials in $I$. Then we can use that fact that this ideal in $R$ is finitely generated to prove that $I$ is finitely generated. 

**Theorem (Hilbert Basis Theorem).** Let $R$ be a Noetherian ring. Then the polynomial ring $R[x]$ is Noetherian as well. 

*Proof.* Let $I \subseteq R[x]$ be an ideal. We need to show that $I$ is finitely generated. For $i \in \N$, set 

$$
J_i = \lbrace a_i \in R \mid \text{there exists $a_0, \ldots , a_{i-1} \in R$ such that } \sum_{j=0}^i a_jx^j \in I \rbrace.
$$Clearly $J_i \subseteq R$ is an ideal. These ideals consist of elements of $R$ that can be the leading coefficient for a polynomial in $I$. Let $a_i \in J_i$ with $f = \sum_{j=0}^i a_jx^j \in I$. Then $xf = \sum\_{j=0}^i a\_j x^{j+1} \in I$, so $a_{i} \in a_{j+1}$ as well. Thus we have an ascending chain of ideals 
$$
J_1 \subseteq J_2 \subseteq J_2 \subseteq \cdots.
$$However, since these are ideals of $R$ and $R$ is Noetherian, there exists an $n \in \N$ such that for $i \geq n$ we have $J_i = J_n$. And since each $J_i$ is finitely generated we have 
$$
J\_i = \left(a\_{i, 1}, \ldots , a\_{i, m\_i} \right)
$$for $i \leq n$, and 
$$
J_i = J_n = \left(a\_{n, 1}, \ldots , a\_{n, m\_n}\right)
$$for $i > n$. By the definition of $J_i$, there exist polynomials $f_{i, j} \in I$ of degree at most $i$ whose $i$th coefficient is $a\_{i,j}$. Set 
$$
I' = \left(f\_{i, j} \mid i =0, \ldots , n, j =1, \ldots, m\_i \right) \subset I.
$$We claim that $I = I'$. To prove this, consider a polynomial $f = \sum\_{i=0}^d b\_ix^i \in I$ with $\deg(f) = d$. We will us induction on $d$. First consider the case $d \leq n$. Since $b_d \in J_d$ we can write 
$$
b\_d = \sum\_{j=1}^{m\_d} r\_ja\_{d, j}
$$with $r\_j \in R$. Then 
$$
\widetilde f = f - \sum\_{j=1}^{m\_d}r\_jf\_{d, j} 
$$lies in $I$ and has degree less than $d$, so by induction $\widetilde f \in I'$. This implies that $f \in I'$ since each $f_{d, j} \in I'$ by definition. Now assume $d > n$. Then we can write $b\_d = \sum\_{j=1}^{m\_n} r\_j a\_{n, j}$ with $r\_j \in R$. So 
$$
\widetilde f = f - \sum\_{j=1}^{m\_n} r\_j x^{d-n}f\_{n, j}
$$lies in $I$ and has degree less than $d$, so by induction $\widetilde f \in I'$. Again we conclude that $f \in I'$. So indeed $I = I'$ is a finitely generated ideal. 