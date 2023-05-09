---
title: "Holomorphic Functions"
date: "2023-05-05"
time: "11:10"
tags:
- complex-analysis
---
Holomorphic functions are the complex analog of differentiable real functions, but have many nicer properties.

**Definition (Holomorphic Function).** Let $\Omega$ be an open set in $\mathbb C$ and $f \colon \Omega \to \mathbb C$. The function $f$ is *holomorphic at the point* $z_0 \in \mathbb C$ if the quotient 
$$
\frac{f(z_0 + h) - f(z_0)}{h}
$$
converges to a limit when $h \to 0$. When this limit exists it is denoted $f'(z_0)$ and is called the derivative of $f$ at $z_0$: 
$$
f'(z_0) = \lim_{h \to 0} \frac{f(z_0+h) - f(z_0)}{h}.
$$We can also say that a function $f$ is holomorphic at $z_0 \in \Omega$ if and only if there exists $a \in \mathbb C$ such that 
$$
f(z_0 + h) - f(z_0) - ah = h \psi(h)
$$where $\psi$ is a function defined for small $h$ and $\lim_{h \to 0} \psi(h) = 0$. We have $a = f'(z_0)$, if it exists. 

Notice that this is very similar to the case in one variable. And we even have the following proposition which is proved in the exact same way as in one variable. 

**Proposition.** If $f$ and $g$ are holomorphic in $\Omega$ then 
1. $f + g$ is holomorphic in $\Omega$ and $(f + g)' = f' + g'$.
2. $fg$ is holomorphic in $\Omega$ and $(fg)' = f'g + fg'$.
3. If $g(z_0) \neq 0$ then $f/g$ is holomorphic at $z_0$ and $(f/g)' = \frac{f'g - fg'}{g^2}$. 
Moreover, if $f \colon \Omega \to U$ and $g \colon \Omega \to \mathbb C$ are holomorphic, then the chain rule holds:
$$
(g\circ f)' = g'(f(z))f'(z).
$$

