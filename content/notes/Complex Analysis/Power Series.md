---
title: "Power Series"
date: "2023-05-05"
time: "23:47"
tags:
- complex-analysis
---
The goal of this note is to show that every [holomorphic](notes/Complex%20Analysis/Holomorphic%20Functions.md) function is analytic and vice versa. 

**Definition (Power Series).** A *power series* is an expression of the form $\sum_{n=0}^\infty a_nz^n$ where $a_n \in \mathbb C$. 

The first natural question to ask is when does a power series converge? Hadamard's formula will give us the answer.  

**Theorem.** Given a power series $\sum_{n=0}^\infty a_nz^n$ there exists $0 \leq R \leq \infty$ such that 
1. if $|z| < R$ the series converges absolutely. The disk $|z| < R$ is called the *disc of convergence*.
2. if $|z| > R$ the series diverges. 
We call $R$ the *radius of convergence*. Moreover, if we use the convention that $1/0 = \infty$ and $1/\infty = 0$, then $R$ is given by Hadamard's formula 
$$
\frac{1}{R} = \limsup |a_n|^{1/n}. 
$$
Note that this theorem does not say anything about the behavior at $|z| = R$. There are several different things that can happen there. 

*Proof.* Let $L = 1/R$ where $R$ is defined by the formula in the statement of the theorem, and suppose that $L \neq 0, \infty$. If $|z| < R$, choose $\epsilon > 0$ such that 
$$
(L + \epsilon)|z| = r < 1.
$$By the definition of $L$, we have that $|a_n|^{1/n} \leq L + \epsilon$ for all large $n$, therefore
$$
|a_n||z|^n \leq \left((L+ \epsilon)|z| \right)^n = r^n.
$$Comparing our series with the geometric series $\sum_{n=0}^\infty r^n$ shows that $\sum_{n=0}^\infty a_nz^n$ converges.

Now, if $|z| > R$, the we can choose $\epsilon$ such that $(L - \epsilon)|z| = r > 1$. Then $|a_n|^{1/n} \geq L - \epsilon$ for large $n$ so 
$$
|a_n||z|^n \geq \left((L - \epsilon)|z| \right)^n = r^n > 1.
$$
and since $\sum_{n=0}^\infty r^n$ diverges, so will $\sum_{n=0}^\infty a_nz^n$. 

Now we can see that a power series is holomorphic. The idea is to break up the power series into its first $N$ terms and the terms from $N$ to $\infty$. And show separately that the two pieces are holomorphic. 

**Theorem.** The power series $f(z) = \sum_{n=0}^\infty a_nz^n$ defines a holomorphic function in its disc of convergence. the derivative of $f$ is also a power series obtained by differentiating term by term the series for $f$, i.e., 
$$
f'(z) = \sum_{n=0}^\infty na_nz^{n-1}. 
$$Moreover, $f'$ has the same radius of convergence as $f$. 

*Proof.* The assertion about the radius of convergence of $f'$ follows from Hadamard's formula. Indeed, $\lim\_{n \to \infty} n^{1/n} = 1$, and therefore 
$$
\limsup |a_n|^{1/n} = \limsup |na_n|^{1/n}
$$so that $\sum a_nz^n$ and $\sum na_n z^n$ have the same radius of convergence, hence $\sum a_nz^n$ and $\sum na_nz^{n-1}$ do as well.

To prove the first assertion, we must show that the series 
$$
g(z) = \sum\_{n=0}^\infty na_nz^{n-1}
$$gives the derivative of $f$. For that, let $R$ denote the radius of convergence of $f$, and suppose $|z\_0| < r < R$. Write 
$$
f(z) = S_N(z) + E_N(z)
$$where
$$
S_N(z) = \sum\_{n=0}^N a_nz^n \text{ and } E_N(z) = \sum\_{n = N+1}^\infty a_nz^n. 
$$Then, if $h$ is chosen so that $|z_0 +h| < r$ we have 

$$
\begin{align*}
\frac{f(z\_0 + h) - f(z\_0)}{h} - g(z\_0) = \left(\frac{S\_N(z\_0 + h) - S\_N(z\_0)}{h} - S\_N\'(z\_0) \right) +& \left(S\_N\'(z\_0) - g(z\_0) \right)\\
+& \left(\frac{E\_N(z\_0 + h) - E\_N(z\_0)}{h}. \right)
\end{align*}
$$Since $a^n - b^n = (a-b)(a^{n-1} + a^{n-2}b + \cdots + ab^{n-2} + b^{n-1})$, we see that 
$$
\left\vert \frac{E\_N(z\_0 + h) = E\_N(z\_0)}{h} \right\vert \leq \sum\_{n=N+1}^\infty |a_n| \left \vert \frac{(z\_0 + h)^n - z\_0^n}{h} \right\vert \leq \sum\_{n = N+1}^\infty |a_n|nr^{n-1}.
$$where we have used the fact that $|z\_0 + h| < r$ and $|z\_0| < r$. The expression on the right is the tailend of a convergent series, since $g$ converges absolutely on $|z| < R$. Therefore, given $\epsilon > 0$ we can fine $N\_1$ o that $N > N\_1$ implies 
$$
\left \vert \frac{E\_N(z\_0 + h) - E\_N(z\_0)}{h} \right\vert < \epsilon. 
$$Also, since $\lim\_{N \to \infty} S\_N'(z\_0) = g(z\_0)$, we can find $N\_2$ so that $N > N\_2$ implies 
$$
\left \vert S\_N'(z\_0) - g(z\_0) \right\vert < \epsilon.
$$If we fix $N$ so that both $N > N\_1$ and $N > N\_2$ hold, then we can find $\delta >0$ so that $|h| < \delta$ implies 
$$
\left \vert \frac{S\_N(z\_0 + h) - S\_N(z\_0)}{h} < \epsilon \right\vert
$$because the derivative of a polynomial is obtained by differentiating term-by-term. Therefore 
$$
\left \vert \frac{f(z\_0 + h) - f(z\_0)}{h} - g(z\_0) \right\vert < 3\epsilon
$$whenever $|h| < \delta$ and thus $f$ is holomorphic with derivative $g$. 

Now that we have this result, applying it successively we get the following. 

**Corollary.** A power series is infinitely complex differentiable in its disc of convergence, and higher derivatives are also power series obtained by termwise differentiation. 

Because of this, we make the following definition.

**Definition (Analytic Function).** A function $f$ defined on an open set $\Omega$ is said to be *analytic* at a point $z\_0 \in \Omega$ if there exists a power series $\sum a_n(z - z\_0)^n$ centered at $z\_0$, with positive radius of convergence so that 
$$
f(z) = \sum\_{n=0}^\infty a\_n(z - z\_0)^n
$$for all $z$ in a neighborhood of $z\_0$. 