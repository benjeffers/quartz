---
title: "Irreducible Spaces"
date: "2023-05-24"
time: "20:21"
tags:
- algebraic-geometry
---

**Definition (Irreducible Space).** A nonempty subset $Y$ of a topological space $X$ is *irreducible* if it cannot be expressed as the union $Y = Y\_1 \cup Y\_2$ of two proper subsets, each one of which is closed in $Y$. 

**Remark.** First, we note that it is a convention to not consider the empty set to be irreducible. Second, note that in the definition $Y\_1$ and $Y\_2$ are not required to be disjoint. 

We will prove a criterion for a topological space to be irreducible which is very useful.

**Lemma.** A topological space $X$ is irreducible if and only if the intersection of any two non-empty open subsets is non-empty.

*Proof.* Assume first that $X$ is irreducible and let $U\_1$ and $U\_2$ be two open subsets. If $U\_1 \cap U\_2 =\emptyset$, then it would follow that, when taking complements, that $X = U\_1^c \cup U\_2^c$. Since $X$ is irreducible, we could infer that $U\_i^c = X$ for either $i = 1$ or $i = 2$, whence $U\_i = \emptyset$ for one of the $i$'s. To prove the other direction, assume that $X$ is expressed as a union $X = X\_1 \cup X\_2$ with the $X\_i$'s being closed. Then 
$$
\emptyset = X^c = (X\_1 \cup X\_2)^c = X\_1^c \cap X\_2^c
$$hence either $X\_1^c = \emptyset$ or $X\_2^c = \emptyset$ since they are both open. Therefore either $X\_1 = X$ or $X\_2 = X$. 

**Examples.**
1. The affine space $\mathbb A^1$ is irreducible because its only proper closed subsets are finite, yet it is infinite, as long as the base field $k$ is algebraically closed. 
2. Any non-empty open subset of an irreducible space is irreducible and dense. Indeed, let $U \subset X$ be open and non-empty. Then if $x \in X$ and $V$ is an open neighborhood of $x$, then $V \cap U \neq \emptyset$ since $X$ is irreducible. Now, $U$ is also irreducible since any two non-empty open subsets of $U$ are open in $X$, and thus their intersection is non-empty. 
3. If $Y \subseteq X$ is irreducible, then its closure $\overline Y$ is irreducible. To see this note that if $U\_1, U\_2$ are two non-empty open subsets of $\overline Y$, then $Y \cap U\_i \neq \emptyset$. Hence, $U\_1 \cap U\_2 \cap Y \neq \emptyset$ since $Y$ is irreducible, and thus $U\_1 \cap U\_2 \neq \emptyset$. 

**Lemma.** Continuous images of irreducible spaces are irreducible.

*Proof.* If $f \colon X \to Y$ is continuous and surjective and $U\_1$ and $U\_2$ are open, non-empty subsets of $Y$, it follows that each $f^{-1}(U\_i)$ is non-empty and open since $f$ is surjective. When $X$ is irreducible it holds that 
$$
f^{-1}(U\_1 \cap U\_2) = f^{-1}(U\_1) \cap f^{-1}(U\_2) \neq \emptyset
$$and so $U\_1 \cap U\_2 \neq \emptyset$. 
