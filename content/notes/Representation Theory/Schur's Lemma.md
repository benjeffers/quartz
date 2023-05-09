---
title: "Schur's Lemma"
date: "2023-04-09"
time: "22:49"
tags:
- representation-theory
---
Schur's lemma is one of the foundational results in representation theory and very simple to prove. It helps us classify homomorphisms of irreducible representations. 

**Theorem (Schur's Lemma).** Let $V\_1, V\_2$ be [representations](notes/Representation%20Theory/Basic%20Definitions.md) of an algebra $A$ over any field $F$, not necessarily algebraically closed. Let $\phi \colon V\_1 \to V\_2$ be a nonzero [homomorphism](notes/Representation%20Theory/Basic%20Definitions.md) of representations. Then 
1. If $V\_1$ is irreducible, $\phi$ is injective. 
2. If $V\_2$ is irreducible, $\phi$ is surjective. 
Thus if both $V_1$ and $V_2$ are irreducible, $\phi$ is an isomorphism.

This remarkable theorem tells us that any two irreducible representations of an algebra are isomorphic. 

*Proof.* 
1. Let $K$ be the kernel of $\phi$. Then $K$ is a subrepresentation of $V\_1$. Indeed, $\ker \phi = \lbrace v \in V\_1 \mid \phi(v) = 0 \rbrace$. Let $a \in A$ and $v \in \ker \phi$, then $$ \phi(\rho\_1(a)(v)) = \rho\_2(a)(\phi(v)) = \rho\_2(a)(0) = 0$$ so $\rho\_1(v)(a) \in \ker \phi$ and thus it is invariant so it is indeed a subrepresentation. But since $\phi \neq 0$ this subrepresentation cannot be $V_1$. So by irreducibility of $V\_1$ we must have $K = 0$. 
2. The Image $I$ of $\phi$ is a subrepresentation of $V\_2$. Indeed, let $I = \lbrace v \in V\_2 \mid \text{ there exists } v\_1 \in V\_1 \text{ such that } \phi(v\_1) = v\_2 \rbrace$.   Then for all $a \in A$, if $\phi(v\_1) = v\_2$ we have $$\rho\_2(a)(v_2) = \rho\_2(a)(\phi(v\_1)) = \phi(\rho\_1(a)(v\_1))\in I.$$ So $I$ is in fact a subrepresentation. Since $\phi \neq 0$, this subrepresentation cannot be 0, so by irreducibility of $V\_2$ we must have $I = V\_2$. $\blacksquare$ 

If our field is algebraically closed and our representations are finite dimensional there is a much stronger statement we can make. 

**Theorem (Schur's Lemma for Algebraically Closed Fields).** Let $V$ be a finite dimensional representation of an algebra $A$ over an algebraically closed field $k$, and let $\phi \colon V \to V$ be an intertwining operator. Then $\phi = \lambda \cdot I$ for some $\lambda \in k$. 

*Proof.* Let $\lambda$ be an eigenvalue of $\phi$. It exists since $k$ is algebraically closed. Then the operator $\phi - \lambda I$ is an intertwining operator $V \to V$ which is not an isomorphism, since its determinant is zero. Thus by the version of Schur's lemma above, this operator is zero, and $\phi = \lambda I$. 

This is very powerful, but it only works over an algebraically closed field since we must be able to find an eigenvalue. 

**Example.** Take $V = A = \mathbb C$ as an $\R$-algebra. Then consider the representation 
$$
\begin{align*}
\rho \colon \mathbb C \to &\text{End}(\mathbb C)\\
\rho(a) \mapsto & \begin{pmatrix}
0 & -1 \\ 1 & 0
\end{pmatrix}
\end{align*}
$$
This is a rotation by 90 degrees so there are no invariant subspaces. Thus it is irreducible. Now let 
$$
\begin{align*}
\rho \colon \mathbb C \to& \mathbb C\\
\begin{pmatrix}x \\ y \end{pmatrix} \mapsto & \begin{pmatrix}
0 & -1 \\ 1 & 0
\end{pmatrix} \begin{pmatrix} x \\ y \end{pmatrix}
\end{align*}
$$Then the eigenvalues of $\phi$ are the roots of $\lambda^2 + 1= 0$ which are $\pm i \notin \R$. So we cannot write $\phi = \lambda I$ for some $\lambda \in \R$. 

From this we get a nice description of the irreducible representations of commutative algebras. 

**Corollary.** Let $A$ be a commutative algebra. Then every irreducible finite dimensional representation $V$ of $A$ is 1-dimensional. 

*Proof.* Let $V$ be irreducible. For any element $a \in A$, the operator $\rho(a) \colon V \to V$ is an intertwining operator. Indeed, 
$$
\rho(a)(\rho(b)(v)) = \rho(a)\rho(b)(v) = \rho(ab)(v) = \rho(ba)(v) = \rho(b)(\rho(a)(v)).
$$Thus by Schur's lemma, $rho(a)$ is a scalar operator for any $a \in A$. Hence, every subspace of $V$ is a subrepresentation. But $V$ is irreducible, so the only subspaces are 0 and $V$. Thus $\dim V = 1$. 


It turns out that there is an infinite dimensional version of this as well.

**Theorem (Infinite Dimensional Schur's Lemma).** Let $A$ be an algebra over $\mathbb C$ and let $V$ be an irreducible representation of $A$ with at most a countable basis. Then any homomorphism of representations $\phi \colon V \to V$ is a scalar operator.

*Proof.* By the version of Schur's lemma above $D = \text{End}_A(V)$, the set of homomorphisms, is a division algebra. Indeed, since $V$ is irreducible, any  homomorphism $\phi \colon V \to V$ is an isomorphism and thus has an inverse. Now we will look at the dimension of $D$ as a vector space. Note that since $D$ is a division ring, $V$ is a free $D$-module, and thus $\dim V \geq \dim D$, so $\dim D$ is at most countable. 

Next, suppose $\phi$ is not a scalar operator and consider $\mathbb C(\phi) \subset D$. Since $\phi$ is not a scalar and $\mathbb C$ is algebraically closed, it must be transcendental. Note that the set of elements 
$$
\frac{1}{\phi - \lambda}
$$
for $\lambda \in \mathbb C$ are linearly independent, so $\mathbb C(\phi)$ has uncountable dimension. This is a contradiction since $\mathbb C(\phi) \subset D$, so $\phi$ must be a scalar. 

