---
title: "Integration Along Curves"
date: "2023-06-27"
time: "21:36"
tags:
- complex-analysis
---
Let $\gamma$ be a parametrized curve in $\mathbb C$, i.e., there is a map $z \colon [a ,b] \to \mathbb C$, and we think of the curve, $\gamma$ as the image of this map. Then we can define 
$$
\int\_\gamma f(z)dz = \int\_a^b f(z(t))z'(t)dt. 
$$
**Definition (Primitive).** A complex-valued function $f$ has a *primitive* if $F'(z) = f(z)$. 

Note that the existence of a primitive just says that $f$ has an anti-derivative. If our function has a primitive then the above becomes 
$$
\int\_a^b f(z(t))z'(t)dt = \int\_a^b F'(z(t))z'(t)dt = F(z(b))
 - F(z(b))$$where the last equality comes from the chain rule. Now, if $a = b$, then this integral is zero. The moral of this is that if we integrate a function on a closed curve that has a primitive, then it is zero. 
 - 