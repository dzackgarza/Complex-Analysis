---
title: Complex Analysis Problem Set 3, Part 2
---

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
