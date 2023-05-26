---
title: "Basic Definitions for Fields"
date: "2023-05-25"
time: "18:01"
tags:
- galois-theory
---
We collect here some basic definitions and examples of field extensions.

Recall that a field is a commutative ring with identity such that the nonzero elements form a group under multiplication.

**Definition (Field Extension, Base Field).** If $F \subseteq K$ are fields, then $K$ is called a *field extension* of $F$ and we refer to $F$ as the *base field*. A field extension is denoted as $K/F$. 

So a field extension is as simple as one field containing another. The most familiar examples would be $\mathbb R/\mathbb Q$ or $\mathbb C /\mathbb R$. 

Given a field extension $K/F$ one of the most powerful ideas in Galois theory is that we can view $K$ as an $F$-vector space. Indeed, for any scalar $\alpha \in F$ and vector $v \in K$ we have $\alpha \cdot v = \alpha v$ which is well-defined in $K$ since it is a field and $\alpha \in F \subseteq K$. 

**Definition (Degree, Finite Extension, Infinite Extension).** Let $K/F$ be a field extension. We denote the dimension of $K$ as a $F$-vector space as $[K:F]$, and call it the *degree* of the field extension. If $[K:F] < \infty$ then $K$ is a *finite extension* of $F$, and otherwise we call $K$ an *infinite extension* of $F$. 

**Examples.**
1. Some of the familiar examples of fields are $\mathbb Q, \mathbb R$, and $\mathbb C$. Additionally, $\mathbb Z/p\mathbb Z$ is a field, usually denoted as $\mathbb F_p$. 
2. Let $k$ be a field and let $x$ be a variable. The rational function field $k(x)$ is the quotient field of the polynomial ring $k\[x\]$. It can be written explicitly as $$ k(x) = \left\\{\frac{f(x)}{g(x)} \mid g(x) \neq 0 \right\\}. $$ Similarly, given $n$ variables $x\_1, x\_2, \ldots , x\_n$ we can form the field $k(x\_1, \ldots, x\_n)$.
3. Let $k$ be a field and let $k((x))$ be the set of formal generalized power series in $x$ with coefficients in $k$. We define addition and multiplication as $$\sum\_n^\infty a\_nx^n + \sum\_n^\infty b\_nx^n = \sum\_n^\infty (a\_n + b\_n)x^n$$ and $$ sum\_n^\infty a\_nx^n \cdot \sum\_n^\infty b\_nx^n = \sum\_{n=n\_0 + n\_1}^\infty \left(\sum\_{k = n\_0}^{n- n\_1} a\_nb\_{n-k} \right)x^n.$$  To see that this is a field, let $f = \sum\_{n = n\_0}^\infty a\_nx^n$ be a nonzero element of $k((x))$. We will show that $f$ has an inverse in $k((x))$. Suppose that we have written the series so that $a\_{n\_0}$ is the first nonzero coefficient. By multiplying by $a\_{n\_0}^{-1}x^{-n\_0}$, to find an inverse for $f$ is suffices to assume that $n\_0 = 0$ and $a\_{n\_0} = 1$. We can find the coefficients $b\_n$ of the inverse by recursion.  To have $$\sum\_{n=0}^\infty a\_nx^n \cdot \sum\_{n=0}^\infty b\_nx^n = 1,$$ we need $b\_0 = 1$ since $a\_0 = 1$. For $n > 0$, the coefficient of $x^n$ is $$b\_na\_0 + b\_{n-1}a\_1 + \cdots + b\_0a\_n = 0,$$ so if we have determined $b\_0, \ldots , b\_{n-1}$, then we determine $b\_n$ from the equation $$b\_n = - \sum\_{k=1}^n b\_{n-k}a\_k.$$ This yields our inverse. 

We record here some examples of field extensions.

**Examples.**
1. If $a \in \mathbb C$, let $$\mathbb Q(a) = \left\\{ \frac{\sum\_i \alpha\_i a^i}{\sum\_i \beta\_i a^i} \mid \alpha\_i, \beta\_i \in \mathbb Q, \sum\_i \beta\_ia^i \neq 0 \right\\}.$$ Then $\mathbb Q(a)$ is a field extension of $\mathbb Q$. Depending on what $a$ is, the extension could be finite or infinite. 
2. If $k$ is a field, let $K = k(t)$ be the field of rational functions in $t$ over $k$. If $f$ is a nonzero element of $K$, then we can mimic the construction of $\mathbb Q(a)$ in the previous example. Let $F = k(f)$ be the set of all rational functions in $f$, i.e., $$F = \left\\{\frac{\sum\_{i=0}^n a\_i f^i}{\sum\_{j=0}^m b\_j f^j} \mid a\_i, b\_j \in k, \sum\_{j=0}^m b\_j f^j \neq 0 \right\\}.$$ For example, if $f(t) = t^2$, then $K/F$ is an extension of degre 2 and $\lbrace 1, t \rbrace$ is a basis for $K$ over $F$. 
3. Let $p(t) = t^3 - 2 \in \mathbb Q[t]$. Then $p(t)$ is irreducible over $\mathbb Q$ by the [Rational Root Test](notes/Galois%20Theory/Rational%20Root%20Test.md). The ideal $(p(t))$ in $\mathbb Q[t]$ is maximal, since $p$ is irreducible, and so $K = \mathbb Q\[t\]/(p(t))$ is a field. The set of cosets $\lbrace a + (p(t)) \mid a \in \mathbb Q \rbrace$ can be seen to be a field isomorphic to $\mathbb Q$ under the map $a \mapsto a + (p(t))$. Using this we can view $\mathbb Q\[t\]/(p(t))$ as a field extension of $\mathbb Q$ by identifying $\mathbb Q$ with this set of cosets. If $f(t) \in \mathbb Q\[t\]$, then by the division algorithm $f(t) = q(t)p(t) + r(t)$ with $r(t) = 0$ or $\deg(r) < \deg(p) = 3$. Moreover, $f(t)$ and $r(t)$ generate the same coset in $\mathbb Q\[t\]/(p(t))$. What this means is that any element of $K$ has a uniqu representation in the form $a + bt + ct^2 + (p(t))$ for some $a, b, c \in \mathbb Q$. Therefore, the cosets $1 + p(t), t + (p(t)), t^2 + (p(t))$ form a basis for $K$ over $\mathbb Q$ and thus $[K: \mathbb Q] = 3$. 