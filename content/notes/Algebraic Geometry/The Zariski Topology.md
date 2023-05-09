---
title: "The Zariski Topology"
date: "2023-05-06"
time: "15:19"
tags:
- algebraic-geometry
---
We start by proving some properties of closed algebraic sets. 

**Proposition.** The union of two [Algebraic Sets](notes/Algebraic%20Geometry/Algebraic%20Sets.md) is algebraic, $Z(\mathfrak a) \cup Z(\mathfrak b) = Z(\mathfrak a \cap \mathfrak b)$, the intersection of any family of algebraic sets is algebraic, $\bigcap\_{i \in I} Z(\mathfrak a_i) = Z\left(\sum\_{i \in I} \mathfrak a\_i \right)$. The empty set and the whole space are also algebraic sets. 

*Proof.* If $Y\_1 = Z(\mathfrak a\_1)$ and $Y\_2 = Z(\mathfrak a\_2)$, then $Y\_1 \cup Y\_2 = Z(\mathfrak a\_1 \mathfrak a\_2)$. Indeed, if $P \in Y\_1 \cup Y\_2$, then either $P \in Y\_1$ or $P\in Y\_2$ so $P$ is a zero of every polynomial in $\mathfrak a\_1 \mathfrak a\_2 = \lbrace \sum afg \mid f \in \mathfrak a\_1, g \in \mathfrak a\_2, a \in k \rbrace$. Conversely, if $P \in Z(\mathfrak a\_1 \mathfrak a\_2)$ and $P \notin Y\_1$, say, then there is an element $f \in \mathfrak a\_1$ such that $f(P) \neq 0$. Now, for any $g \in \mathfrak a\_2$, $(fg)(P) = 0$ implies that $P \in Z(\mathfrak a\_2)$ and $Y\_1 \cup Y\_2 = Z(\mathfrak a\_1 \mathfrak a\_2)$. 

Next, recall that $\mathfrak a + \mathfrak b = \lbrace f + g \mid f \in \mathfrak a, g \in \mathfrak b \rbrace$ where $\mathfrak a, \mathfrak b$ are ideals of $k\[x\_1, \ldots , x\_n \]$. Then $Z(\mathfrak a) \cap Z(\mathfrak b) = Z(\mathfrak a + \mathfrak b)$. We can see this by first taking $P \in Z(\mathfrak a + \mathfrak b)$, then $(f + 0)(P) = f(P) = 0$ and $(0 + g)(P) = g(P) = 0$, so $P \in Z(\mathfrak a) \cap Z(\mathfrak b)$. Conversely, if $P \in Z(\mathfrak a) \cap Z(\mathfrak b)$, then if $f + g \in \mathfrak a + \mathfrak b$, $(f + g)(P) = f(P) + g(P) = 0$. So the sets are equal.

Finally, $\emptyset = Z(1)$ and $\mathbb A^n = Z(0)$. 

The above proposition tells us that we actually get a topology on $\mathbb A^n$ by taking the $Z(\mathfrak a)$ to be the closed sets.

**Definition (Zariski Topology).** We define the *Zariski topology* on $\mathbb A^n$ by taking the open subsets to be the complements of the [Algebraic Sets](notes/Algebraic%20Geometry/Algebraic%20Sets.md). This is a topology, because according to the proposition, the intersection of two open sets is open, and the union of any family of open sets is open. Furthermore, the empty set and the whole space are both open. 

