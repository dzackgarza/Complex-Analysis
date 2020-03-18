---
title: Complex Analysis Problem Set 3
---

# Problems From Tie

## 1

Problem
: Prove that if $f$ has two Laurent series expansions,
  $$
  \begin{aligned} f(z) = \sum c_n(z-a)^n \quad\text{and}\quad f(z) = \sum c_n'(z-a)^n\end{aligned}
  $$
  then $c_n = c_n'$.

### Solution

By taking the difference of two such expansions, it suffices to show that if $f$ is identically zero and $f(z) = \sum_{n=-\infty}^\infty c_n (z-a)^n$ about some point $a$, then $c_n = 0$ for all $n$.

Under this assumption, let $D_\eps(a)$ be a disc about $a$ and $\gamma$ be any contoured contained in its interior.
Then for each $n$, we can apply the formula

\begin{align*}
c_n
&= \frac 1 {2\pi i } \int_\gamma \frac{f(\xi)}{\qty{\xi - a}^{n+1}} ~d\xi \\
&= \frac 1 {2\pi i } \int_\gamma \frac{0}{\qty{\xi - a}^{n+1}} ~d\xi \quad\text{by assumption} \\
&= 0
,\end{align*}

which shows that $c_n = 0$ for all $n$.

$\qed$

## 2

Problem
: Find Laurent series expansions of
  $$\begin{aligned}\frac{1}{1-z^2} + \frac{1}{3-z}\end{aligned}$$
  How many such expansions are there? In what domains are each valid?

### Solution

Note that $f$ has poles at $z=-1, 1, 3$, all with multiplicity 1, and so there are 3 regions to consider:

1. $\abs{z} < 1$
2. $1 < \abs{z} < 3$
3. $3 < \abs{z}$.

\begin{center}
\begin{tikzpicture}
\pgfplotsset{every x tick label/.append style={font=\tiny, yshift=0.5ex}}
\pgfplotsset{every y tick label/.append style={font=\tiny, xshift=0.5ex}}
\begin{axis}[
    xmin=-6,
    xmax=6,
    ymin=-4,
    ymax=4,
		xtick = {-1, -3, 3, 1},
		ytick = {-1, -3, 3, 1},
    axis equal,
    axis lines=middle,
    disabledatascaling]

\fill[red] [opacity=0.5] (0,0) circle [radius=1];
\fill[orange] [opacity=0.2] (0,0) circle [radius=3];
\fill[cyan] [opacity=0.1] (0,0) circle [radius=5];

\draw[->][cyan][opacity=0.3] (axis cs:3.0, 3.0) -- (axis cs:4, 4);
\draw[->][cyan][opacity=0.3] (axis cs:-3.0, 3.0) -- (axis cs:-4, 4);
\draw[->][cyan][opacity=0.3] (axis cs:3.0, -3.0) -- (axis cs:4, -4);
\draw[->][cyan][opacity=0.3] (axis cs:-3.0, -3.0) -- (axis cs:-4, -4);

\node[font=\tiny] at (axis cs:0,1) [anchor=north west] {Region 1};
\node[font=\tiny] at (axis cs:1,2) [anchor=north west] {Region 2};
\node[font=\tiny] at (axis cs:2,3) [anchor=north west] {Region 3};

\node at (axis cs:2.5,5) [anchor=north east] {$\mathbb{C}$};
\end{axis}
\end{tikzpicture}
\end{center}


**Region 1:**
Take the following expansion:

\begin{align*}
f(z)
&= \frac{1}{1-z^2} + \frac{1}{3-z} \\
&= \sum_{n\geq 0} z^{2n} + \frac 1 3 \qty{ \frac{1}{1 - \frac 3 z}  } \\
&= \sum_{n\geq 0} z^{2n} + \frac 1 3 \sum_{n\geq 0} \qty{\frac 1 3}^n z^n \\
&= \sum_{n\geq 0} z^{2n} + \sum_{n\geq 0} \qty{\frac 1 3}^{n+1} z^n \\
.\end{align*}

Noting $\abs{z^2} < 1$ implies then $\abs{z} < 1$, and that the first term converges for $\abs{z^2} < 1$ and the second for $\abs{\frac z 3} < 1 \iff \abs{z} < 3$, this expansion converges to $f$ on the region $\abs{z} < 1$.

**Region 2:**
Take the following expansion:

\begin{align*}
f(z)
&= \frac{1}{1-z^2} + \frac{1}{3-z} \\
&= -\frac{1}{z^2} \qty{\frac{1}{1 - \frac{1}{z^2}}} - \frac 1 3 \qty{ \frac{1}{1 - \frac z 3}  }  \\
&=-\frac 1 {z^2} \sum_{n\geq 0} z^{-2n} + \sum_{n\geq 0} \qty{\frac 1 3}^{n+1} z^n \\
&= -\sum_{n\geq 2}\frac{1}{z^{2n}}  + \sum_{n\geq 0} \qty{\frac 1 3}^{n+1} z^n \\
.\end{align*}

By construction, the first term converges for $\abs{ \frac{1}{z^2} } < 1 \iff \abs{z} > 1$ and the second for $\abs{z} < 3$.

**Region 3:**
Take the following expansion:

\begin{align*}
f(z)
&= \frac{1}{1-z^2} + \frac{1}{3-z} \\
&= -\frac{1}{z^2} \qty{\frac{1}{1 - \frac{1}{z^2}}} - \frac 1 z \qty{\frac 1 {1 - \frac 3 z}} \\
&= - \frac 1 {z^2} \sum_{n\geq 0} \frac{1}{z^{2n}} - \frac 1 z \sum_{n\geq 0}3^n \frac{1}{z^n} \\
&= - \sum_{n\geq 2} \frac{1}{z^{2n}} - \sum_{n\geq 1}
\qty{ \frac 1 3 }^{n-1}
\frac{1}{z^n}
.\end{align*}

> Note: in principle, terms could be collected here.

By construction, this converges on $\theset{\abs z^2 > 1} \intersect \theset{\abs z > 3} = \theset{\abs z > 3}$.

$\qed$


## 3

Problem
: Let $P, Q$ be polynomials with no common zeros. Assume $a$ is a root of
$Q$.
  Find the principal part of $P/Q$ at $z=a$ in terms of $P$ and $Q$ if $a$ is (1) a simple root, and (2) a double root.

### Solution

> todo

## 4

Problem
:   Let $f$ be non-constant, analytic in $\abs{z} > 0$, where $f(z_n) = 0$
for infinitely many points $z_n$ with $\lim_{n\to\infty} z_n = 0$.

    Show that $z=0$ is an essential singularity for $f$.

    > Example: $f(z) = \sin(1/z)$.

### Solution

It suffices to show that $z_0 = 0$ is neither a pole nor a removable singularity, i.e.

1. $\lim_{z\to z_0}f(z) \neq \infty$

2. $\abs{f(z)}$ is not bounded on any neighborhood $D_\eps(z_0)$.

The first property follows because if $f$ is analytic,

## 5

Problem
: Show that if $f$ is entire and $\lim_{z\to\infty}f(z) = \infty$, then
$f$ is a polynomial.

## 6

Problem
:
  a. Show that
  $$\begin{aligned}\int_0^{2\pi} \log\abs{1 - e^{i\theta}}~d\theta = 0\end{aligned}$$
  b. Show that this identity is equivalent to SS 3.8.9.

## 7

Problem
: Let $0<a<4$ and evaluate $$\begin{aligned}
    \int_0^\infty \frac{x^{\alpha-1}}{1+x^3} ~dx\end{aligned}$$

## 8

Problem
:   Prove the fundamental theorem of Algebra using

    a.  Rouche's Theorem.
    b. The maximum modulus principle.

## 9

Problem
:   Let $f$ be analytic in a region $D$ and $\gamma$ a rectifiable curve in
$D$ with interior in $D$.

    Prove that if $f(z)$ is real for all $z\in \gamma$, the $f$ is constant.

## 10

Problem
: For $a> 0$, evaluate
  $$\begin{aligned} \int_0^{\pi/2} \frac{d\theta}{a + \sin^2 \theta}\end{aligned}$$

## 11

Problem
: Find the number of roots of $p(z) = 4z^4 - 6z + 3$ in $\abs{z} < 1$ and
$1 < \abs{z} < 2$ respectively.

## 12

Problem
: Prove that $z^4 + 2z^3 -2z + 10$ has exactly one root in each open
quadrant.

### Solution

Let $f(z) = z^4 +2z^3 -2z + 10$, and consider the following contour:

![Image](figures/2020-03-18-11:02.png)\

Since polynomials are holomorphic on $\CC$, by the argument principle it suffices to show that $f$ does not vanish on $\Gamma$ and $\Delta_\Gamma \arg f(z) = 1$, where $\Delta_\Gamma$ denotes the total change in the argument of $f$ over $\Gamma$.

By the argument principle, we have
\begin{align*}
\Delta_\Gamma \arg f(z) = 2\pi\qty{ Z - P }
,\end{align*}

where $Z$ is the number of zeros of $f$ in the region $\Omega$ enclosed by $\Gamma$ and $P$ is the number of poles in $\Omega$.

Claim
:   \hfill
    - $\Delta_{\gamma_1}\arg f(z) = 0$
    - $\Delta_{\gamma_2}\arg f(z) = 2\pi$
    - $\Delta_{\gamma_3}\arg f(z) = 0$

Using the claim and the fact that $f$ is holomorphic on $\CC$ and thus has no poles, we obtain

\begin{align*}
\Delta_\Gamma \arg f(z) = 2\pi = 2\pi \qty{Z - 0} \implies Z = 1
.\end{align*}

Proof of Claim

$\gamma_2$:
For $R\gg 0$, we have $f(z) \sim z^$.
Along $\gamma_2$, the argument of $z$ ranges from $0$ to $\frac \pi 2$, and thus the argument of $z^4$ ranges from $0$ to $4\cdot \frac \pi 2 = 2\pi$.


## 13

Problem
: Prove that for $a> 0$, $z\tan z - a$ has only real roots.

## 14

Problem
:   Let $f$ be nonzero, analytic on a bounded region $\Omega$ and continuous
on its closure $\overline \Omega$.

    Show that if $\abs{f(z)} \equiv M$ is constant for $z\in \partial \Omega$, then $f(z) \equiv Me^{i\theta}$ for some real constant $\theta$.

# Stein and Shakarchi

## S&S 3.8.1

Problem
:   Using Euler's formula
    $$\sin(\pi z) = \frac 1 {2i}( e^{i\pi z} - e^{-i\pi z} )$$
    show that the complex zeros of $\sin(\pi z)$ are exactly the integers, each of order one.

    Calculate the residue of $\frac 1 {\sin(\pi z)}$ at $z=n\in \mathbb{Z}$.

## S&S 3.8.2

Problem
: Evaluate the integral $$\int_{\mathbb{R}} \frac{dx}{1+x^4}$$ What are
the poles of the integrand?

## S&S 3.8.4

Problem
: Show that
  $$\begin{aligned}\int_{\mathbb R} \frac{x\sin x}{x^2 + a^2} = \frac{\pi e^{-a}}{a} \quad a > 0\end{aligned}$$

## S&S 3.8.5

Problem
: Show that for $\xi \in \mathbb{R}$,
  $$
  \begin{aligned}
  \int_{\mathbb R} \frac{e^{2\pi i x \xi}}{(1+x^2)^2} = \frac \pi 2 ( 1 + 2\pi |\xi|)e^{-2\pi |\xi|}\end{aligned}
  $$

## S&S 3.8.6

Problem
: Show that
  $$
  \begin{aligned}\int_{\mathbb R} \frac{dx}{(1+x^2)^{n+1}} = \frac{1\cdot 3\cdot \cdots (2n-1)\pi }{2\cdot 4\cdots (2n}\end{aligned}
  $$

## S&S 3.8.7

Problem
: Show that for $a > 1$,
  $$
  \begin{aligned}\int_0^{2\pi} \frac{d\theta}{(a+\cos \theta)^2} =
    \frac{2\pi a}{(a^2-1)^{3/2}}\end{aligned}
  $$

## S&S 3.8.8

Problem
: Show that if $a, b\in \mathbb{R}$ with $a > \abs{b}$ then
  $$
  \begin{aligned}
    \int_0^{2\pi} \frac{d\theta}{a + b\cos \theta} =
    \frac{2\pi a}{\sqrt{a^2-b^2}}\end{aligned}
  $$

## S&S 3.8.9

Problem
: Show that
  $$
  \begin{aligned}\int_0^1 \log(\sin \pi x) ~dx = -\log 2\end{aligned}$$

## S&S 3.8.10

Problem
: Show that if $a> 0$
  $$
  \begin{aligned} \int_0^{\infty} \frac{\log x}{x^2 + a^2} ~dx =\frac{\pi \log a}{2a}\end{aligned}
  $$

## S&S 3.8.14

Problem
:   Prove that if $f$ is entire and injective, then $f(z) = az + b$ with $a,b\in \mathbb{C}$ with $a\neq 0$.

    > Hint: apply the Casorati-Weierstrass theorem to $f(1/z)$.

## S&S 3.8.15

Problem
:   Use the Cauchy inequalities or the maximum modulus principle to solve
the following problems:

    ### a

    If $f$ is entire and for all $R> 0$, there are constants $A, B > 0$ such that $\sup_{\abs{z} = R} \abs{f(z)} \leq AR^k + B$, then $f$ is a polynomial of degree less than $k$.

    ### b

    Show that if $f$ is holomorphic on the unit disk, is bounded, and converges to zero uniformly in the sector $\theta \leq \arg z \leq \phi$ as $\abs{z} \to 1$, then $f \equiv 0$.

    ### c

    Let $w_1, \cdots, w_n$ be points on $S^1 \subset\mathbb{C}$.
    Show that there exists a point $z \in S^1$ such that
    $$
    \prod_{i=1}^n \abs{z-w_i} \geq 1.
    $$

    Conclude that there exists a point $w\in S^1$ such that
    $$\prod_{i=1}^n \abs{w-w_i} = 1.$$

    ### d

    Show that if $f$ is entire and $\Re(f)$ is bounded, then $f$ is constant.

## S&S 3.8.17

Problem
:   Let $f$ be non-constant, and holomorphic in an open set containing the
open unit disc.

    ### a

    Show that $\abs{z} = 1 \implies \abs{f(z)} = 1$, then the image of $f$ contains the unit disc.

    > Hint: Show that $f(z) = w_0$ has a root for every
    > $w_0 \in \mathbb{D}$, for which it suffices to show that $f(z) = 0$
    > has a root, then use the maximum modulus principle.

    ### b

    Show that if $\abs{z} \geq 1 \implies \abs{f(z)} = 1$ **and** there
    exists a point $z_0 \in \mathbb{D}$ such that $\abs{f(z_0)} < 1$, then
    the image of $f$ contains the unit disc.

## S&S 3.8.19

Problem
:   Prove the maximum modulus principle for harmonic functions; i.e.,

    ### a

    If $u$ is a non-constant real-valued harmonic function on $\Omega$, then
    $u$ can not attain its extrema on $\Omega$.

    ### b

    Suppose $\Omega$ has compact closure $\overline \Omega$, then if $u$ is
    harmonic on $\Omega$ and continuous on $\overline \Omega$, then
    $$
    \begin{aligned}
    \sup_{z\in \Omega} \abs{u(z)} \leq \sup_{z\in \overline \Omega - \Omega} \abs{u(z)}\end{aligned}
    $$

    > Hint: to prove (a), assume that $u$ attains a local maximum at $z_0$,
    > and let $f$ be holomorphic near $z_0$ with $u = \Re(f)$, then show
    > that $f$ is not open. Part (b) is a direct consequence.
