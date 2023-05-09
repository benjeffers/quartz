---
title: "Cauchy-Riemann Equations"
date: "2023-05-05"
time: "14:47"
tags:
- complex-analysis
---
In this note we will make a connection between the differentiability of complex functions and the differentiability of real functions. We first consider the following example.

**Example.** Let $f(z) = \overline z$, where $\overline z = \overline{x + iy} = x-iy$ is complex conjugation. Then $f$ is not [holomorphic](notes/Complex%20Analysis/Holomorphic%20Functions.md). Indeed, we have 
$$
\frac{f(z_0 + h) - f(z_0)}{h} = \frac{\overline h}{h}.
$$If we consider $h$ real, then $\overline h = h$, and the above quotient is 1. However, if we let $h$ be purely imaginary, $h = iy$, then the above quotient is -1. Thus the limit does not exist and $f$ is not holomorphic. However, as a real function $f$ is 
$$
F \colon (x, y) \mapsto (x, -y)
$$
which is differentiable in real variables with Jacobian matrix equal to 
$$
\begin{pmatrix}1 & 0\\ 0 & -1 \end{pmatrix}. 
$$Thus if a function is differentiable as a map $\R^2 \to \R^2$ then it is not necessarily differentiable as a map $\mathbb C \to \mathbb C$. 

Now, consider the difference quotient for a complex function when $h$ is real, $h = h_1 + ih_2$ with $h_2 = 0$, i.e., 
$$
f'(z\_0) = \lim\_{h_1 \to 0} \frac{f(x\_0 + h\_1, y\_0) - f(x\_0, y\_0)}{h_1}.
$$But notice that this is exactly the partial derivative of $f$ with respect to $x$ if we write $z = x + iy$ and $f(z) = f(x, y)$. Thus 
$$
f'(z\_0) = \frac{\partial f}{\partial x}(z\_0).
$$Next, consider what happens if $h = h_1 + ih_2$ with $h_1 = 0$. Then we have 
$$
f'(z\_0) = \lim\_{h\_2 \to 0} \frac{f(x\_0, y\_0 + h\_2) - f(x\_0, y\_0)}{ih\_2} = \frac{1}{i}\frac{\partial f}{\partial y}. 
$$
This yields the following equation 
$$
\frac{\partial f}{\partial x} = \frac{1}{i}\frac{\partial f}{\partial y}
$$Writing $f = u + iv$ where $u, v \colon \R^2 \to \R$ we have 
$$
\frac{\partial f}{\partial x} = \frac{\partial u}{\partial x} + i \frac{\partial v}{\partial x}, \hspace{0.2cm}\frac{1}{i}\frac{\partial f}{\partial y} = \frac{1}{i}\frac{\partial u}{\partial y} + \frac{\partial v}{\partial y}. 
$$
Now this gives us 
$$
\frac{\partial u}{\partial x} + i \frac{\partial v}{\partial x} = \frac{1}{i}\frac{\partial u}{\partial y} + \frac{\partial v}{\partial y}
$$and separating the real and imaginary parts gives two equations 
$$
\frac{\partial u}{\partial x} = \frac{\partial v}{\partial y}, \hspace{.2cm} \frac{\partial v}{\partial x} = -\frac{\partial u}{\partial y}.
$$
These are called the *Cauchy-Riemann equations* and every holomorphic function satisfies them. And not only that, we will later show the converse, any complex function satisfying the Cauchy-Riemann equations is holomorphic. This provides a bridge between real differentiability and complex differentiability. 

Now we introduce two operators that will help us prove some nice relations between the complex derivative at a point and derivatives of real functions. Let 
$$
\frac{\partial}{\partial z} = \frac{1}{2}\left(\frac{\partial}{\partial x} + \frac{1}{i}\frac{\partial}{\partial y} \right) \text{ and } \frac{\partial}{\partial \overline{z}} = \frac{1}{2} \left(\frac{\partial}{\partial x} - \frac{1}{i} \frac{\partial}{\partial y} \right).
$$
These are defined with a $\frac{1}{2}$ to make the following proposition nicer. 


**Proposition.** If $f$ is holomorphic at $z_0$, then 
$$
\frac{\partial f}{\partial \overline z}(z_0) = 0 \text{ and } f'(z_0) = \frac{\partial f}{\partial z}(z_0) = 2 \frac{\partial u}{\partial z}(z_0).
$$Also, if we write $F(x, y) = f(z)$, then $F$ is differentiable in the sense of real variables, and 
$$
\det J_F(x_0, y_0) = \left\vert f'(z_0) \right\vert^2. 
$$

*Proof.* First, using the Cauchy-Riemann equations we have 
$$
\begin{align*}
\frac{\partial f}{\partial \overline z}(z\_0) =& \frac{1}{2}\left(\frac{\partial f}{\partial x} - \frac{1}{i} \frac{\partial f}{\partial y} \right)\\
=&\; \frac{1}{2}\left(\frac{\partial u}{\partial x} + i \frac{\partial v}{\partial x} - \frac{1}{i} \frac{\partial u}{\partial y} - \frac{\partial v}{\partial y} \right)\\
=& \left(\frac{\partial v}{\partial y} + i \frac{\partial v}{\partial x} + \frac{1}{i} \frac{\partial v}{\partial x} - \frac{\partial v}{\partial y} \right) = 0. 
\end{align*}
$$Moreover, we have already showed that $f'(z_0) = \frac{\partial f}{\partial x}(z\_0) = \frac{1}{i}\frac{\partial f}{\partial y}(z\_0)$ and thus 
$$
f'(z\_0) = \frac{1}{2}\left(\frac{\partial f}{\partial x}(z\_0) + \frac{1}{i} \frac{\partial f}{\partial y}(z\_0) \right) = \frac{\partial f}{\partial z}. 
$$
Then by the Cauchy-Riemann equations we have 
$$
\begin{align*}
\frac{\partial f}{\partial z} =& \frac{1}{2}\left(\frac{\partial f}{\partial x} + \frac{1}{i} \frac{\partial f}{\partial y} \right)\\
=& \left(\left(\frac{\partial u}{\partial x} + i \frac{\partial v}{\partial x} \right) + \frac{1}{i}\left(\frac{\partial u}{\partial y} + i \frac{\partial v}{\partial y} \right) \right)\\
=& \frac{1}{2} \left(\frac{\partial u}{\partial x} - i \frac{\partial u}{\partial y} + \frac{1}{i} \frac{\partial u}{\partial y} + \frac{\partial u}{\partial x} \right)\\
=& \frac{1}{2} \left(2 \frac{\partial u}{\partial x} + \frac{2}{i} \frac{\partial u}{\partial y} \right) = 2\frac{\partial u}{\partial z}. 
\end{align*}
$$To prove that $F$ is differentiable it suffices to observe that if $H = (h\_1, h\_2)$ and $h = h\_1 + i h\_2$, then the Cauchy-Riemann equations imply 
$$
J_F(x\_0, y\_0)(H) = \left(\frac{\partial u}{\partial x} - i \frac{\partial u}{\partial y} \right)(h\_1 + ih\_2) = f'(z\_0)h.
$$
This is because we have 
$$
\begin{align*}
J_F(x\_0, y\_0)(H) =& \begin{pmatrix}
\partial u/\partial x & \partial u/\partial y\\ \partial v/\partial x & \partial v/\partial y
\end{pmatrix}\begin{pmatrix}
h\_1 \\ h\_2
\end{pmatrix}\\
=& \begin{pmatrix}
\partial u/\partial x & \partial u/\partial y\\ -\partial u/\partial y & \partial u/\partial x
\end{pmatrix}\begin{pmatrix}
h\_1 \\ h\_2
\end{pmatrix}\\
=& \left(\frac{\partial u}{\partial x} - i \frac{\partial u}{\partial y} \right)(h\_1 + i h\_2)
\end{align*}
$$by identifying matrices of the form $\begin{pmatrix} a & -b \\ b & a\end{pmatrix}$ with $\mathbb C$ and $\begin{pmatrix} h\_1 \\  h\_2 \end{pmatrix}$ with $h\_1 + i h\_2$. Then 
$$
\frac{\partial u}{\partial x} - i \frac{\partial u}{\partial y} = \frac{\partial u}{\partial x} + \frac{1}{i} \frac{\partial u}{\partial y} = 2 \frac{\partial u}{\partial z} = f'(z\_0). 
$$To get the final result we have 
$$
\det J\_F(x\_0, y\_0) = \frac{\partial u}{\partial x} \frac{\partial v}{\partial y} - \frac{\partial v}{\partial x} \frac{\partial u}{\partial y} = \left(\frac{\partial u}{\partial x}\right)\^2
 \+ \left(\frac{\partial u}{\partial y} \right)\^2 = \left \vert 2 \frac{\partial u}{\partial z} \right \vert^2 = \left \vert f'(z\_0) \right\vert$$ 
This result tells us that if a function is holomorphic then it is differentiable as a function of real variables, but as we saw in the first example, the converse is not true. 

Now we will see that any holomorphic function that satisfies the Cauchy-Riemann equations is actually holomorphic. 

**Theorem.** Suppose $f = u + iv$ is a complex-valued function defined on an open set $\Omega$. If $u$ and $v$ are continuously differentiable and satisfy the Cauchy-Riemann equations on $\Omega$, then $f$ is holomorphic on $\Omega$ and $f'(z) = \frac{\partial f}{\partial z}$. 

*Proof.* We can write 
$$
u(x + h\_1, y + h\_2) - u(x, y) = \frac{\partial u}{\partial x}h\_1 + \frac{\partial u}{\partial y}h\_2 + |h|\psi\_1(h)
$$and 
$$
v(x + h\_1, y + h\_2) - v(x, y) = \frac{\partial v}{\partial x}h\_1 + \frac{\partial v}{\partial y}h\_2 + |h|\psi\_2(h)
$$where $\psi\_j(h) \to 0$ as $|h| \to 0$ and $h = h\_1 + ih\_2$. Using the Cauchy-Riemann equations we find that 
$$
\begin{align*}
f(z + h) - f(z) =& u(x + h\_1, y + h\_2) + iv(x + h\_1, y + h\_2) - u(x, y) - v(x, y)\\
=& \frac{\partial u}{\partial x}h\_1 + \frac{\partial u}{\partial y}h\_2 + i\frac{\partial v}{\partial x} + i \frac{\partial v}{\partial y} + |h|\left(\psi\_1(h) + \psi\_2(h) \right)\\
=& \frac{\partial u}{\partial x}h\_1 + \frac{\partial u}{\partial y}h\_2 - i \frac{\partial u}{\partial y}h\_1 + i \frac{\partial u}{\partial x}h\_2 + |h|\psi(h)\\
=& \left(\frac{\partial u}{\partial x} - i \frac{\partial u}{\partial y} \right)(h\_1 + ih\_2) + |h|\psi(h)\\
=& \left(\frac{\partial u}{\partial x} + \frac{1}{i} \frac{\partial u}{\partial y} \right)(h\_1 + ih\_2) + |h|\psi(h).
\end{align*}
$$Therefore, $f$ is holomorphic and 
$$
f'(z) = 2\frac{\partial u}{\partial z} = \frac{\partial f}{\partial z}. \hspace{.2cm} 
$$
This theorem shows us that a function is holomorphic if and only if it satisfies the Cauchy-Riemann equations. 