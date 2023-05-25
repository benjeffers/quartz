---
title: "Hilbert's Nullstellensatz"
date: "2023-05-24"
time: "16:29"
tags:
- algebraic-geometry
- commutative-algebra
---
In this note we state and prove Hilbert's Nullstellensatz. We will also see that it is equivalent to the [[notes/Algebraic Geometry/Weak Nullstellensatz|Weak Nullstellensatz]].

**Hilbert's Nullstellensatz.** Assume that $k$ is an algebraically closed field, and that $\mathfrak a$ is an ideal in $k[x\_1, \ldots , x\_n]$. Then one has 
$$
I(Z(\mathfrak a)) = \sqrt{\mathfrak a}. 
$$
*Proof.* First, note that polynomials in the radical $\sqrt{a}$ vanish along $Z(\mathfrak a)$ and therefore $\sqrt{\mathfrak a} \subseteq I(Z(\mathfrak a))$. To prove the other inclusion we will use the so called Rabinowitsch trick to deduce Hilbert's Nullstellensatz from the [[notes/Algebraic Geometry/Weak Nullstellensatz|Weak Nullstellensatz]]. The main point of the trick is to introduce a new variable $x\_{n+1}$ and for each $g \in I(Z(\mathfrak a))$ consider the ideal $\mathfrak b$ in the polynomial ring $k[x\_1, \ldots , x\_{n+1}]$ given by 
$$
\mathfrak b = \mathfrak a \cdot k[x\_1, \ldots , x\_{n+1}] + (1 -x\_{n+1}\cdot g). 
$$Geometrically, the zero locus $Z(\mathfrak b) \subseteq \mathbb a^{n+1}$ is the intersection of the subset $Z = Z(1 - x\_{n+1}g)$ and the inverse image $\pi^{-1}(Z(\mathfrak a))$ of $Z(\mathfrak a)$ under the projection $\pi \colon \mathbb a^{n+1} \to \mathbb A^n$ that forgets the extra coordinate $x\_{n+1}$. This intersection is empty since $g$ does not vanish along $Z$, but vanishes identically on $\pi^{-1}(Z(\mathfrak a))$. 

The  [[notes/Algebraic Geometry/Weak Nullstellensatz| First Weak Nullstellensatz]] then tells us that $1 \in \mathfrak b$, and hence there are polynomials $f\_i \in \mathfrak a$ and $h\_i$ and $h$ in $k[x\_1, \ldots , x\_{n+1}]$ satisfying a relation of the form 
$$
1 = \sum f\_i(z\_1, \ldots , x\_n)h\_i(x\_1, \ldots , x\_{n+1}) + h \cdot (1 - x\_{n+1}g).
$$Now, the last trick is to substitute $x\_{n+1} = 1/g$ and multiply through by a sufficiently high power $g^N$, for example the highest power of $x\_{n+1}$ that occurs in any of the $h\_i$'s, of $g$ to obtain 
$$
g^N = \sum f(x\_1, \ldots , x\_n)H_i(x\_1, \ldots , x\_n),
$$where $H_i(x\_1, \ldots , x\_n)= g^N\cdot h_i(x\_1, \ldots , x\_n, 1/g)$. Hence $g \in \sqrt{\mathfrak a}$. 