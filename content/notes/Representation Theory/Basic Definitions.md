---
title: "Basic Definitions"
date: "2023-04-09"
time: "22:15"
tags:
- representation-theory
---
$\R, \Z, \N, \Q, \Rn, \E, \C, \MaxSpec, \Gal$

**Definition (Representation).** A *representation* of an associative algebra $A$ is a vector space $V$ equipped with a homomorphism $$
\rho \colon V \to \text{End}(V).
$$
We can also think of a representation as a left $A$-module where the multiplication is given by $$
a \cdot v = \rho(a)(v).
$$
**Definition (Subrepresentation).** A *subrepresentation* of a representation $V$ is a subspace $U \subset V$ which is invariant under all operators $\rho(a) \in A$, i.e., for each $u \in U, \rho(a)(u) \in U$ for all $a \in A$. If $V\_1$ and $V\_2$ are two representations  of $A$, 
$$
\rho\_1 \colon A \to \text{End}(V\_1), \rho\_2 \colon A \to \text{End}(V\_2)
$$then $V_1 \oplus V_2$ is a representation of $A$ given by 
$$
\begin{align*}
\rho \colon \to& \text{End}(V\_1 \oplus V\_2)\\
a \mapsto & \rho\_1(a) \oplus \rho\_2(a).
\end{align*}
$$
Then, as a module, this is $\rho(a)(v\_1, v\_2) = (\rho\_1(a)(v\_1), \rho\_2(a)(v\_2))$. 

**Definition (Irreducible and Indecomposable).** A nonzero representation $V$ of $A$ is said to be *irreducible* if its only subrepresentations are $0$ and $V$. A representation is *indecomposable* if it cannot be written as a direct sum of two nonzero representations. 

**Remark.** Irreducible implies indecomposable but not vice versa. Indeed, suppose $A$ has a representation $V$ which is irreducible. Suppose that we could represent $V$ as $V\_1 \oplus V\_2$, but then both of these are subrepresentations of $V$, a contradiction. However, a representation could be indecomposable but still have a subrepresentation as in the following example. 

**Example.** Consider the group $G = (\R, +)$ and the representation 

$$
\begin{align*}
\rho \to& GL(\R^2)\\
r \mapsto & \begin{pmatrix} 1 & r\\ 0 &1 \end{pmatrix}
\end{align*}.
$$
Suppose that this representation is decomposable, i.e., there exists a $G$-invariant and linearly independent vectors $v = (v_1, v_2)$ and $w = (w_1, w_2) \in \R^2$. Then the following must be true 
$$
\begin{align*}
\rho(r)(v) =& \lambda v\\
\rho(r)(w) =& \gamma w
\end{align*}
$$
for all $r \in \R$ and some $\lambda, \gamma \in \R$. This equation implies 
$$
\begin{align*}
v\_1 + v\_2r =& \lambda v\_1\\
v\_2 =& \lambda v\_2.
\end{align*}
$$
So $\lambda = 1$ and $v\_2r = 0$ for all $r \in \R$. Then $v\_2 = 0$ and $\R v= \R e_1$. We reach the same conclusion with $w$, i.e., $\R w = \R e_1$. But this is a contradiction so $\rho$ is indecomposable. Note that $\rho$ is not irreducible because $\lbrace(r, 0) \mid r \in \R \rbrace$ is invariant under this action. Indeed, 
$$
\rho(r)(r, 0) = \begin{pmatrix}
1 & r \\ 0 & 1
\end{pmatrix} \begin{pmatrix}
r \\ 0
\end{pmatrix} = \begin{pmatrix} r \\ 0 \end{pmatrix}.
$$
So $\lbrace (r, 0) \mid r \in \R \rbrace$ is a subrepresentation. In some cases we could use the subrepresentation to create a decomposition of the representation. But in this case it would need to be of the form $\lbrace (a,b) \mid a, b \in \R, b \neq 0 \rbrace$ which cannot be $G$-invariant. Indeed, 
$$
\rho(r)(a, b) =  \begin{pmatrix}
1 & r \\ 0 & 1
\end{pmatrix} \begin{pmatrix}
a \\ b
\end{pmatrix} = \begin{pmatrix} a + rb \\ b \end{pmatrix}.
$$
For $a + rb = a$ for all $r \in \R$ we would need to require that $b = 0$ which would not work for the decomposition. 

**Examples.** 
1. $V = 0$.
2. $V = A$ and $\rho \colon A \to \text{End}(A)$ is defined as follows: $\rho(a)$ is the operator of left multiplication by $a$, so that $\rho(a)b = ab$. This is called the *regular* representation of $A$. 
3. $A = k$, a field. Then a representation of $A$ is a vector space over $\R$. 
4. $A = k\langle x\_1, \ldots , x\_n \rangle$. Then a representation of $A$ is just a vector space $V$ over $k$ with a collection of arbitrary linear operators $\rho(x\_1), \ldots , \rho(x\_n) \colon V \to V$.  A representation over $A$ is $$ \rho \colon k\langle x_1, \ldots , x_n \rangle \to V$$where $V$ is a vector space over $k$. An element of $A$ looks like $\sum_{i=1}^k a\_i x\_1^{m\_{i1}} \cdots x\_n^{m\_{in}}$ so $$ \rho\left(\sum_{i=1}^k a\_i x\_1^{m\_{i1}} \cdots x\_n^{m\_{in}} \right) = \sum_{i=1}^k a\_i \rho(x\_1)^{m\_{i1}} \cdots \rho(x\_n)^{m\_{in}}.$$

**Definition (Homomorphism).** Let $V_1, V_2$ be two representations of an algebra $A$. A *homomorphism* or *intertwining operator* $\phi \colon V\_1 \to V\_2$ is a linear operator which commutes with the action of $A$, i.e., $\phi(av) = a\phi(v)$ for any $v \in V\_1$. This really means that if we have $\rho\_1 \colon A \to V\_1$ and $\rho\_2 \colon A \to V\_2$. Then for all $a \in A$, $v \in V\_1$, 
$$
\phi(\rho\_1(a)(v)) = \rho\_2(a)(\rho(v)).
$$
A homomorphism $\phi$ is said to be an *isomorphism* if it is an isomorphism of vector spaces. The space of all homomorphisms of representations $V\_1 \to V\_2$ is denoted by $\text{Hom}(V\_1, V\_2)$. 




