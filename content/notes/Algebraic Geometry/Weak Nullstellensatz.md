---
title: "Weak Nullstellensatz"
date: "2023-05-23"
time: "22:26"
tags:
- algebraic-geometry
- commutative-algebra
---
We will state and prove three different, but equivalent, versions of the Weak Nullstellensatz, one of the most fundamental theorems in algebraic geometry. We will start with the most general version and then use that to prove two versions that give us more geometric information.

**First Weak Nullstellensatz.** Let $k$ be a field and let $\mathfrak m$ be a maximal ideal in the polynomial ring $k[x\_1, \ldots x\_2]$. Then $k[x\_1, \ldots , x\_n]/\mathfrak m$ is a finite field extension of $k$. 

To prove this we need to first prove a lemma.

**Lemma.** If $k \subseteq K$ is a finitely generated extension of fields which is not finite, and $a\_1, \ldots , a\_r$ are elements in $k$, then $k[a\_1, \ldots , a\_r]$ is not equal to $k$.

*Proof.* We start with the case where $K$ is of transcendence degree one over $k$. Then there is a subfield $k(x) \subseteq K$ over which $K$ is finite and $x$ is transcendental over $k$. Let $\lbrace e_i \rbrace$ be a basis for $K$ over $k(x)$ with $e_0 = 1$, and let $c\_{ijk}$ be elements in $k(x)$ such that 
$$
e\_ie\_j = \sum_k c_{ijk}e_k.
$$Let $s$ be a common denominator of the $c\_{ijk}$. Then $A = \bigoplus_i k[x]_s e_i$ where $k[x]_s$ is the localization of the multiplicative set $\lbrace 1, s,s^2, \ldots  \rbrace$. Now, let $a\_1, \ldots , a\_r$ be elements in $K$ and express them in the basis $\\{e\_i \\}$; that is, write $a\_j = \sum d\_{ij} e\_i$ with $d\_{ij} \in k(x)$. Let $t$ be the common denominator of the $d\_{ij}$'s. 

Then $k[a\_1, \ldots , a\_r]$ is contained in $A_t$, and therefore cannot be equal to $K$. Indeed, if $u \in k[x]$ is an irreducible element that is not a factor of $s$ not $t$, then $u^{-1}$ will not lie in $A\_t$. 

Finally, if the transcendence degree of $K$ is more than one, we let $k' \subseteq K$ be a field containing $k$ over which $K$ has transcendence degree one. Then $K$ is never equal to $k'[a\_1, \ldots , a\_r]$, hence neither to $k[a\_1, \ldots , a\_r]$. 

Now we can prove the first version of the nullstellensatz. 

**Proof of First Nullstellensatz.** Suppose that $k[x\_1, \ldots , x\_n]/\mathfrak m$ is not a finite extension of $k$. Then by the lemma $k[a\_1, \ldots , a\_r] \neq k[x\_1, \ldots , x\_n]/\mathfrak m$ for any $a\_1, \ldots , a\_r \in k[x\_1, \ldots , x\_n]/\mathfrak m$. However, letting $\overline{x\_i}$ be the image of $x\_i$ under the natural map 
$$
k[x\_1, \ldots , x\_n] \to k[x\_1, \ldots , x\_n]/\mathfrak m
$$then $k[\overline{x\_1}, \ldots , \overline{x\_n}] = k[x\_1, \ldots , x\_n]/\mathfrak m$, a contradiction. Thus $k[x\_1, \ldots , x\_n]/\mathfrak m$ must be a finite extension of $k$. 

Now we can prove two further versions of the nullstellensatz. We will use the first version to prove the second, and then show that the second and third are equivalent. Before we do that we quickly observe that ideals of the form $(x\_1 - a\_1, \ldots , x\_n - a\_n)$ are maximal in $k[x\_1, \ldots , x\_n]$. Indeed, they are the kernel of the evaluation map 
$$
k[x\_1, \ldots , x\_n] \to k
$$at the point $(a\_1, \ldots, a\_n)$. 

**Second Weak Nullstellensatz.** Assume $k$ is algebraically closed. Then the maximal ideals in the ring $k[x\_1, \ldots , x\_n]$ are exactly those of the form $(x\_1 - a\_1, \ldots , x\_n - a\_n)$ with $(a\_1, \ldots , a\_n) \in \mathbb A^n$. 

This remarkable theorem tells us that, if the base field is algebraically closed, we can associate between points of $\mathbb A^n$ and maximal ideals of the polynomial ring in $n$ variables. This gives the first concrete connection between algebra and geometry. 

**Proof.** Let $\mathfrak m$ be a maximal ideal in $k[x\_1, \ldots , x\_n]$. Since $k$ is algebraically closed, and $k[x\_1, \ldots , x\_n]/\mathfrak m$ is a finite extension of $k$, by the first version of the Weak Nullstellensatz, they must be equal. Thus there is a $k$-algebra homomorphism 
$$
k[x\_1, \ldots , x\_n] \to k
$$which has $\mathfrak m$ as its kernel. Letting $a\_i$ be the image of $x\_i$ under this map, the ideal $(x\_1 - a\_1, \ldots, x\_n - a\_n)$ will be contained in $\mathfrak m$ and since they are both maximal they must be equal. 

And we finally arrive at our third and final version of the nullstellensatz.

**Third Weak Nullstellensatz.** Assume that $k$ is an algebraically closed field. For every proper ideal $\mathfrak a \subset k[x\_1, \ldots , x\_n]$, there is a point $x \in Z(\mathfrak a)$. 

*Proof.* We will prove that the second and third versions of the Nullstellensatz are equivalent. Assume the second statement. Then, let $\mathfrak a$ be a proper ideal. Since $\mathfrak a$ is contained in some maximal ideal $\mathfrak m = (x\_1 - a\_1, \ldots , x\_n - a\_n)$ we must have that $Z(\mathfrak m) \subseteq Z(\mathfrak a)$ and $(a\_1, \ldots , a\_n) \in Z(\mathfrak m)$, and thus $Z(\mathfrak a) \neq \emptyset$. 

Now assume the third statement. Let $\mathfrak m$ be a maximal ideal. It is proper, so there is a point $(a\_1, \ldots , a\_n) \in Z(\mathfrak m)$. Consequently it holds that 
$$
(x\_1 - a\_1 , \ldots , x\_n - a\_n) \subseteq \mathfrak m.
$$To see this, note that since $k[x\_1, \ldots , x\_n]/\mathfrak m \cong k$ (this can be seen using the evaluation map), each $x_i + \mathfrak m$ maps to some $a\_i \in k$ under this isomorphism. So each $x\_i - a\_i \in \mathfrak m$. But since $(x\_1 - a\_1, \ldots , x\_n - a\_n)$ is maximal, it must be equal to $\mathfrak m$. 

*Alternate Proof.* We can also prove the third Weak Nullstellensatz using [[Hilbert's Nullstellensatz]]. Note that $I(\emptyset) = k[x\_1, \ldots , x\_n]$. Conversely, if $\mathfrak a$ is a proper ideal, then $\sqrt{\mathfrak a}$ is not the entire polynomial ring, thus $Z(\mathfrak a) = \emptyset$ if and only if $\mathfrak a$ equal the whole polynomial ring by [[Hilbert's Nullstellensatz]]. Thus we can conclude that $Z(\mathfrak a)$ is non-empty when $\mathfrak a$ is a proper ideal. 

