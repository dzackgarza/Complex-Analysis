---
title: Problem Set 1
---

# Problem 1 

Describe geometrically the sets of points z in the complex plane defined by the following relations:

a. $\abs{z-1} = 1$
b. $\abs{z-1} = 2\abs{z-2}$
c. $\frac 1 z = \bar z$
d. $\Re(z) = 3$
e. $\Im(z) = a$ with $a\in \RR$
f. $\Re(z) > a$ with $a\in \RR$
g. $\abs{z - 1} < 2\abs{z-2}$


# Problem 2

Prove that 

\begin{align*}
\abs{z_1 + z_2} \geq \abs{~\abs{z_1} - \abs{z_2}~}
\end{align*}

and explain when equality holds.

# Problem 3

Prove that the equation

\begin{align*}
z^3 + 2z + 4 = 0
\end{align*}

has its roots outside the unit circle.

> Hint: what is the maximum value of the modulus of the first two terms if $\abs{z} \leq 1$.

# Problem 4

## a

Prove that if $\abs{w_1} = c \abs{w_2}$ where $c>0$ then

\begin{align*}
\abs{w_1 - c^2 w_2} = c\abs{w_1 - w_2}
.\end{align*}

## b

Prove that if $c>0$, $c\neq 1$, then $\abs{\frac{z-z_1}{z-z_2}} = c$ defines a circle.
Find its center and radius.

> Hint: use part (a).

# Problem 5

## a

Let $z, w \in \CC$ such that $\bar z w \neq 1$. Prove that

\begin{align*}
\abs{\frac{w-z}{1-\bar w z} } < 1 \text{ if } \abs{z} < 1, \abs{w} < 1 \text{ with equality when } \abs{z} = 1 \text{ or } \abs{w} = 1
.\end{align*}

## b

Prove that for a fixed $w$ in the unit disc $\Bbb D$, the mapping

\begin{align*}
F: \CC &\to \CC \\
z &\mapsto \frac{w-z}{1-\bar w z}
\end{align*}

satisfies the following conditions:

1. $F$ is holomorphic and maps $\Bbb D$ to itself.
2. $F(0) = w$ and $F(w) = 0$.
3. If $\abs{z} = 1$ then $\abs{F(z)} = 1$.
4. $F$ is a bijection.

> Hint: compute $F^2$.

# Problem 6

Use $n$th roots of unity to show

\begin{align*}
2^{n-1} \sin\qty{\frac \pi n} \sin\qty{\frac{2\pi} n} \cdots \sin\qty{ \frac{(n-1)\pi}{n}  } = n
.\end{align*}

> Hint: $1 - \cos\qty{2\theta} = 2\sin^2(\theta)$ and $\sin(2\theta) = 2\sin(\theta)\cos(\theta)$.

# Problem 7

Prove that $f(z) = \abs{z}^2$ has derivative only at $z=0$ and nowhere else.

# Problem 8

Let $f(z)$ be analytic in its domain.
Prove that $f$ is constant if it satisfies any of the following conditions

a. $\abs{f}$ is constant
b. $\Re(f)$ is constant
c. $\arg(f)$ is constant
d. $\bar f$ is constant

How can you generalize (a) and (b)?


# Problem 9

Show that if $f$ is analytic, $\bar f$ is analytic.


# Problem 10

## a 

Show that in polar coordinates, the Cauchy-Riemann equations take the form


\begin{align*}
\frac{\partial u}{\partial r}=\frac{1}{r} \frac{\partial v}{\partial \theta} \quad \text { and } \quad \frac{\partial v}{\partial r}=-\frac{1}{r} \frac{\partial u}{\partial \theta}
.\end{align*}

## b

Use this to show that the logarithm function,

\begin{align*}
\log z=\log r+i \theta \text { where } z=r e^{i \theta} \text { with }-\pi<\theta<\pi
.\end{align*}

is holomorphic in the region $S = \theset{z = re^{i\theta} \suchthat r>0,~ -\pi < \theta < \pi}$, but is not continuous for $r> 0$.


# Problem 10

Prove that distinct complex numbers $z_1, z_2, z_3$ are the vertices of an equilateral triangle iff

\begin{align*}
z_{1}^{2}+z_{2}^{2}+z_{3}^{2}=z_{1} z_{2}+z_{2} z_{3}+z_{3} z_{1}
.\end{align*}

