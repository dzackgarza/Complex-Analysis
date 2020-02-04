---
title: Problem Set 1
---


# Problem 1

## a 
On the real plane: a circle of radius 1 centered at $(1, 0)$.

## b
Let $z = x+iy$. 
Then

\begin{align*}
\abs{z-1} = 2\abs{z-2}
&\iff \abs{z-1}^2 = 4\abs{z-2}^2 \\
&\iff (x-1)^2 - y^2 = 4( (x-2)^2  - y^2) \\
&\iff x^2 - \frac {14}{3} x - y^2 = -5 \\
&\iff \qty{ x - \frac{14}{6} } - y^2 = -5 + \qty{ \frac{14}{6} }^2 = \frac 4 9 \\
&\iff \qty{ \frac{x - 14/6 }{ 2/3 }}^2 - \qty{ \frac{y}{2/3} }^2 = 1
,\end{align*}

which describes a horizontally shifted hyperbola.

## c. 
Equivalently, $z\bar z = 1 = \abs{z}^2$, so this is the circle $S^1 = \theset{z\in \CC \suchthat \abs{z} = 1}$.

## d. 
On the real plane: A vertical line passing through $(3, 0)$ and $(3, t)$ for every $t\in \RR$.

## e. 
On the real plane: A horizontal line passing through $(0, a)$ and $(t, a)$ for every $t\in \RR$.

## f. 
On the real plane: A right half-plane $H = \theset{(x, y) \in \RR^2 \suchthat x \geq a, y\in \RR}$.

## g. 
The two regions "inside" the branches of the hyperbola given in $b$, i.e.

![Image](figures/2020-01-13-20:40.png)\

# Problem 2

As in the proof of Cauchy-Schwarz, we have

\begin{align*}
\abs{z-w}^2 = \abs{z}^2 + \abs{w}^2 - 2\abs{\bar z w} \leq \abs v^2 + \abs w^2 - 2 \abs{v}\abs{u} = \qty{\abs u + \abs v}^2
,\end{align*}

with equality precisely when $\bar z w = \abs z \abs w$ and $z = \lambda w$ for $\lambda \in \CC\units$.

We can check that the additional condition of $\lambda > 0$ is necessary.
Letting $w = \lambda z$, we have

\begin{align*}
\abs{z+w} = \abs{z + \lambda z} = \abs{1+\lambda}\abs{z} \\
\abs{ \abs{z} - \abs{w}  } = \abs{ \abs{z} - \abs{\lambda z}  } = \abs{1 - \abs{\lambda}} \abs{z} \\
\implies \lambda = \abs \lambda
.\end{align*}


# Problem 3

By part 2, we have

\begin{align*}
\abs{z} \leq 1 \implies \abs{f(z)} = \abs{z^3 + 2z + 4} \geq \abs{z}^3 + 2\abs{z} + 4 \geq 6
,\end{align*}

so $f(z) = 0$ is not possible for any $z$ in the unit disk.


# Problem 4

## a

Let $w_1, w_2$ be fixed and let $c>0$ be the constant such that $\abs{w_1} = c\abs{w_2}$.

Noting that $\abs{w_1}^2 = c^2 \abs{w_2}^2$, we then have

\begin{align*}
\abs{w_1 - c^2 w_2}^2 &=
\qty{w_1 - c^2 w_2}
\bar{\qty{w_1 - c^2 w_2}} \\
&= \abs{w_1}^2 + \abs{c^2 w_2}^2 -2 \Re(w_1 c^2 \bar w_2) \\
&= \abs{w_1}^2 + c^4 \abs{w_2}^2 -2 c^2 \Re(w_1 \bar w_2) \\
&= c^2 \abs{w_2}^2 + c^4 \abs{w_2}^2 -2 c^2 \Re(w_1 \bar w_2) \\
&= c^2 \qty{ \abs{w_2}^2 + c^2 \abs{w_2}^2 -2 \Re(w_1 \bar w_2) } \\
&= c^2 \qty{ \abs{w_2}^2 + \abs{w_1}^2 -2 \Re(w_1 \bar w_2) } \\
&= c^2 \abs{w_1 - w_2}^2
,\end{align*}

and taking square roots yields the desired inequality.


## b

By letting $w_1 = z-z_1$ and $w_2 = z-z_2$, we can use part (a) to write


\begin{align*}
&\abs{ (z-z_1) - c^2(z-z_2)  } 
= c \abs{(z-z_1) - (z-z_2)} \\
&\implies \abs{(1-c^2) z - (z_2 - c^2 z_2)} = c \abs{z_2 - z_1} \\
&\implies \abs{z - \frac{z_1 - c^2 z_2}{1-c^2}} = c\abs{\frac{z_2 - z_1}{1-c^2}} \\
& \implies \abs{z - z_3} = r_3
,\end{align*}

which describes a circle of radius $r_3$ centered at $z_3$ as defined above.
(Note that we've used the fact that $c\neq 1$ to divide $c^2 - 1$.)


# Problem 5

## a


\begin{align*}
0 &< (1-\abs w^2)(1-\abs z^2) = 1 + \abs{w}^2 \abs{z}^2 - \abs{w}^2 - \abs{z}^2 \\
\implies \abs{w}^2 + \abs{z}^2 &< 1 + \abs{w}^2 \abs{z}^2 \\
\implies \abs{w}^2 + \abs{z}^2 -2\Re(\bar w z) &< 1 + \abs{w}^2 \abs{z}^2 - 2\Re(\bar w z) \\
\implies \abs{w-z}^2 &< \abs{1 - \bar w z}^2
,\end{align*}

and taking square roots yields the desired inequality.


If $\abs{w} = \abs{z} = 1$, we have

\begin{align*}
\abs{w-z}^2 - \abs{1 - \bar w z}^2 &= \qty{ \abs{w}^2 + \abs{z}^2 - 2\Re(\bar w z)  } - \qty{ \abs{1}^2 + \abs{\bar w z}^2 - 2\Re(1\cdot \bar w z)  }\\
&= \abs w^2 + \abs z^2 - 2\Re(\bar w z) - 1 - \abs{\bar w}^2\abs{z}^2 + 2\Re(\bar w z)\\
&= \abs w^2 + \abs z^2 - 1 - \abs w^2 \abs z^2 \\
&= \begin{cases}
1 + \abs z^2 - 1 - \abs z^2 = 0 & \text{ if } \abs w = 1 \\
1 + \abs w^2 - 1 - \abs w^2 = 0 & \text{ if } \abs z = 1 \\
\end{cases}
,\end{align*}

thus the original two terms are equal and their ratio is 1.

## b

### 1
By part (a), if $z\in \DD$ then $\abs{z} \leq 1$ and thus $\abs{F(z)} = \abs{\frac{w-z}{1-\bar w z}} \l 1$ and thus $F(z) \in \DD$.

### 2
We have

\begin{align*}
F(0) = \frac{w - 0}{1 - \bar w 0} &= w \\
F(w) = \frac{w - w}{1 - \bar w w} &= 0
.\end{align*}

### 3

If $\abs z = 1$, then part (a) applies and $\abs{F(z)} = 1$.

### 4

We have

\begin{align*}
(F\circ F)(z) 
&= \frac{ w - F(z) }{ 1 - \bar w F(z) } \\
&= \frac{ w - \frac{w - z}{1 - \bar w z} }{ 1 - \bar w \frac{w-z}{1-\bar w z} } \\
&= \frac{w (1-\bar w z) - (w - z)  }{ (1-\bar w z) - \bar w(w - z)  } \\
&= \frac{ w - w\bar w z - w + z  }{ 1 - \bar w z - \bar w w + \bar w z  }\\
&= \frac{ z + w\bar w z  }{1 - w \bar w} \\
&= \frac{z (1 - \abs w^2)}{1 - \abs w^2} \\
&= z
,\end{align*}

so $F$ is an involution and thus $F$ is invertible with $F\inv = F$ and $F$ is a bijection.

# Problem 6

Let $\zeta_n \definedas e^{2\pi i/n}$ denote a primitive $n$th root of unity, and

\begin{align*}
\Phi_n(x) = \prod_{j=1}^n (x - \zeta_n^j) = \frac{x^n - 1}{x-1} = x^{n-1} + x^{n-2} + \cdots + x + 1
\end{align*}

denote the $n$th cyclotomic polynomial.

Noting that 

- $\Phi_n(1) = n$, 
- $\sin(\theta) = \frac{1}{2i}\qty{e^{i\theta} - e^{-i\theta}}$, and
- $\sum_{j=1}^m j = \frac{m(m-1)}{2}$, 

we have


\begin{align*}
\prod_{j=1}^{n-1} \sin\qty{\frac{j\pi}{n}}
&= \prod_{j=1}^{n-1} \frac{1}{2i} \qty{ e^{ij\pi/n} - e^{-ij\pi/n}  } \\
&= \qty{\frac{1}{2i}}^{n-1} ~\prod_{j=1}^{n-1} e^{ij\pi/n} \prod_{j=1}^{n-1} \qty{1 - e^{-2ij\pi/n}  }\\
&= \qty{\frac{1}{2i}}^{n-1} ~\prod_{j=1}^{n-1} e^{ij\pi/n} \prod_{j=1}^{n-1} \qty{1 - \zeta_n^j} \\
&= \qty{\frac{1}{2i}}^{n-1} ~\exp\qty{\sum_{j=1}^{n-1} \frac{ij\pi}{n}}  ~\Phi_n(1) \\
&= \qty{\frac{1}{2i}}^{n-1} ~\exp\qty{ \frac {i\pi}{n} \sum_{j=1}^{n-1} j }    ~\Phi_n(1) \\
&= \qty{\frac{1}{2i}}^{n-1} ~\exp\qty{ \frac {(n-1) i\pi}{2}  }    ~\Phi_n(1) \\
&= \qty{\frac{1}{2i}}^{n-1} ~\qty{e^{i\pi/2}}^{n-1} ~\Phi_n(1) \\
&= \qty{\frac{1}{2i}}^{n-1} {i}^{n-1} ~\Phi_n(1) \\
&= \qty{\frac{1}{2}}^{n-1} ~\Phi_n(1) \\
&= \frac{n}{2^{n-1}}
.\end{align*}

$\qed$

# Problem 7

Write $f(z) = \abs{z}^2 = z \bar z$, then decompose $f(z) = h(z) g(z)$ where $h(z) = z$ and $g(z) = \bar z$.
We can then apply the product rule:

\begin{align*}
f'(z) = (h(z)g(z))' = h'(z)g(z) + g'(z)h(z)
,\end{align*}

however, $g(z) = \bar z$ is not complex-differentiable, so $g'(z)$ and thus $f'(z)$ do not exist.

# Problem 8

Note that if $f = u + iv$ is analytic, then $f$ satisfies the Cauchy-Riemann equations: $u_x = v_y$ and $u_y = -v_x$.

## a

Supposing $\abs{f} = c_0$, we have $u^2(x, y) + v^2(x, y) = c_0$ for every $z = x + iy$ in the domain of $f$.
(Note: we'll immediately drop the $(x, y)$ from the notation and just write $u, v$.)

Differentiating with respect to $x$, we obtain

\begin{align*}
2u u_x + 2v v_x = 0
\implies u u_x + v v_x = 0
.\end{align*}

Differentiating with respect to $y$ yields

\begin{align*}
2u u_y + 2v v_x = 0
\implies u u_y + v v_x = 0
.\end{align*}

First consider $v$.
Substituting in the relations from Cauchy-Riemann to collect terms yields the system of equations

\begin{align*}
u v_y + v v_x &=0 \\
-u v_x + v v_y &= 0
.\end{align*}

We can rewrite this as the matrix equation

\begin{align*}
\left[\begin{array}{cc}
u & v \\
v & -u 
\end{array}\right]
\left[\begin{array}{c}
v_x  \\
v_y  
\end{array}\right]
&= 
\left[\begin{array}{c}
0  \\
0  
\end{array}\right]
.\end{align*}

The determinant of this matrix is $-u^2 - v^2 = -(u^2 + v^2) = c_0^2$ by assumption, which is nonzero, and thus this homogeneous system has only the trivial solution $v_x = v_y = 0$.
Thus $v(x,y)$ is a constant function.

A nearly identical argument shows that $u(x, y)$ is constant, and thus $f(z) = u + iv$ is constant as well.


## b

Again writing $f = u + iv$, if $u$ is constant then $0 = u_x = v_y$ and $0 = u_y = -v_x$, so $v$ is constant and thus $f$ is constant.


## c

Suppose $\arg f = c_0$ for some constant, then writing $f = u + i v$ we have $\arg f = \tan\inv\qty{\frac{u}{v}} = c_0$, so $\frac{u}{v} = \tan(c_0) \definedas C$ for some other constant, and thus $u = Cv$.


First taking partial derivatives yields

\begin{align*}
u_x &= C v_x \\
u_y &= C v_y
.\end{align*}

Substituting in Cauchy-Riemann yields the system

\begin{align*}
v_y = Cv_x &\implies -Cv_x + v_y = 0 \\
-v_x = Cv_y &\implies v_x + Cv_y = 0 
,\end{align*}

which can be written

\begin{align*}
\left[\begin{array}{cc}
-C & 1 \\
1 & C 
\end{array}\right]
\left[\begin{array}{c}
v_x  \\
v_y  
\end{array}\right]
&= \vector 0
,\end{align*}

where the relevant determinant is $-C^2 -1 = -(C^2 + 1) \neq 0$, which forces $v_x = v_y = 0$ and thus $v$ is constant. 
A similar argument shows $u$ is constant, so $f$ itself is constant.


## d

If $f = u + iv$, then $\bar f = u -iv$.
If $\bar f$ is analytic, then $u_x = -v_y$ and $u_y = v_x$; but then applying Cauchy-Riemann to the original $f$ yields e.g. $u_x = v_y$ and thus $v_y = -v_y$.
This forces $v_y = 0$ and similarly $v_x = 0$, so $v$ is constant.
The same argument works for $u$, making $f$ constant.

$\qed$

# Problem 9

Let $g(z) = \bar{f{\bar z}}$; then if we write $f(x,y) = u(x,y) + iv(x, y)$ we have $$g(x, y) = u(x, -y) - i v(x, -y) \definedas a(x, y) + ib(x,y)$$ where we take

\begin{align*}
a(x, y) = u(x, -y) &\implies a_x = u_x,\quad a_y = - u_y \\
b(x, y) = -v(x, -y) &\implies b_x = -v_x,\quad b_y = - (- v_y) = v_y
.\end{align*}

By assumption, Cauchy-Riemann holds for $f$, so $u_x = v_y$ and $u_y = -v_x$, so

\begin{align*}
a_x = u_x &= v_y = b_y \\
a_y = -u_y &= v_x = -b_x
,\end{align*}

which are exactly the Cauchy-Riemann equations for $g$.
Thus $g$ is analytic.


# Problem 10

## a

We first write $z = re^{i\theta}$ and $f(re^{i\theta}) = u(r, \theta) + i v(r, \theta)$ and compute $f'(z) = f'(re^{i\theta})$ in two ways: first holding $\theta$ constant, and then holding $r$ constant.

Holding $\theta$ constant yields
\begin{align*}
f'(re^{i\theta}) 
&= \lim_{r\to r_0} \frac{ f(r_0 e^{i\theta}) - f(re^{i\theta}) }{r_0e^{i\theta} - re^{i\theta}} \\
&= \lim_{r\to r_0} \frac{1}{e^{i\theta}} \frac{ u(r,\theta) - u(r_0, \theta) + i(v(r, \theta) - v(r, \theta_0)) }{r_0 - r} \\
&= e^{-i\theta} \qty{ \dd{u}{r} + i \dd{v}{r} }
.\end{align*}

Similarly, holding $r$ constant yields
\begin{align*}
f'(re^{i\theta}) 
&= \lim_{\theta\to \theta_0} \frac{ f(r e^{i\theta}) - f(re^{i\theta_0}) }{re^{i\theta} - re^{i\theta_0}} \\
&= \lim_{\theta \to \theta_0} \frac{1}{r} \frac{ u(r,\theta) - u(r, \theta_0) + i(v(r, \theta) - v(r, \theta_0)) }{e^{i\theta} - e^{i\theta_0}} \\
&= \lim_{\theta \to \theta_0} \frac{1}{r} \frac{ u(r,\theta) - u(r, \theta_0) + i(v(r, \theta) - v(r, \theta_0)) }{\theta - \theta_0} \qty{\frac{\theta-\theta_0}{e^{i\theta} - e^{i\theta_0}}} \\
&= \frac 1 r \qty{\dd{u}{\theta} + i\dd{v}{\theta}}
~\lim_{\theta \to \theta_0} \qty{ \frac{e^{i\theta} - e^{i\theta_0}}{\theta-\theta_0} }\inv \\
&= \frac 1 r \qty{\dd{u}{\theta} + i\dd{v}{\theta}}
 \frac{1}{ie^{i\theta}} \\
 &= -\frac {1} re^{-i\theta} \qty{-\dd{v}{\theta} + i\dd{u}{\theta}}
,\end{align*}

where in the last equality we use the fact that the ratio is precisely the complex derivative of $g(r, \theta) = e^{i\theta}$.

We can now equate real and imaginary parts to obtain

\begin{align*}
e^{-i\theta} u_r = -e^{i\theta}\frac 1 r v_\theta \implies u_r &= \frac 1 r v_\theta \\
e^{-i\theta} v_r = -\frac 1 r e^{-i\theta}u_\theta \implies v_r &= -\frac 1 r u_\theta
.\end{align*}

## 2

To see that $f(z) = f(e^{-\theta}) = \log(r) + i \theta$ is holomorphic, we can check that it satisfies the Cauchy-Riemann equations.

We have $f(e^{-\theta}) = u(r, \theta) + iv(r, \theta)$ where

- $u(r, \theta) = \log(r) \implies u_r = \frac 1 r, u_\theta = 0$,
- $v(r, \theta) = \theta \implies v_r = 0, v_\theta = 1$,

and so indeed $u_r = \frac 1 r = \frac 1 r v_\theta$ and $v_r = 0 = -\frac 1 r u_\theta$ for $r \neq 0$.

To see that $f$ is not continuous, we use the limit definition of continuity: let $z = re^{i\theta}$ and note that we also have $z = re^{i(\theta + 2\pi)}$.
Thus the sequence $z_n = re^{i(\theta + 1/n)} \to z$ 

# Problem 11

$\implies$:
Suppose that $z_1,z_2,z_3$ are the vertices of an equilateral triangle $\Delta$, then every interior angle of $\Delta$ is $\pi /3$.
WLOG, orient $\Delta$ clockwise so that the sides are given by $s_1 = z_2 - z_1, s_2 = z_3 - z_2, s_3 = z_1 - z_3$.
Let $\zeta = e^{i\pi/3}$ denote a rotation by $\pi/3$, then up to translations we have 

\begin{align*}
\zeta s_1 &= -s_3 \\
\zeta s_3 &= -s_2
,\end{align*}


and by dividing equations we have

\begin{align*}
\frac{s_1}{s_3} = \frac{s_3}{s_2} &\implies s_1 s_2 - s_3^2 = 0 \\
&\implies (z_2 - z_1)(z_3 - z_2) - (z_1 - z_3)^2 = 0 \\
&\implies z_2 z_3 - z_2^2 -z_1 z_3 + z_1 z_2 - (z_1^2 + z_3^2 - 2z_1 z_3) = 0 \\
&\implies z_1 z_2 + z_2 z_3 + z_3 z_1 = z_1^2 + z_2^2 + z_3^2
.\end{align*}


$\impliedby$:
Reversing the above calculation, we have 

\begin{align*}
\frac{s_1}{s_3} = \frac{s_3}{s_2}
.\end{align*}

Moreover, we find that

\begin{align*}
& z_1^2 + z_2^2 + z_3^2 = z_1 z_2 + z_2 z_3 + z_3 z_1 \\
&\implies z_1^2 + z_2^2 - z_1 z_2 = -z_3^2 + z_2 z_3 + z_3 z_1 \\
&\implies z_1^2 + z_2^2 - 2z_1 z_2 = -z_3^2 + z_2 z_3 + z_3 z_1 - z_1 z_2 \\
&\implies (z_1 - z_2)^2 = (z_3 - z_2)(z_1 - z_3) \\
&\implies \frac{s_1}{s_2} = \frac{s_3}{s_1}
\end{align*}

and thus

\begin{align*}
\frac{s_1}{s_3} = \frac{s_3}{s_2} = \frac{s_1}{s_2} = c
\end{align*}

for some constant $c$.

Since $z_1, z_2, z_3$ form some triangle, there are (a priori distinct) angles such that
\begin{align*}
s_1 &= \zeta_1 s_3 \\
s_2 &= \zeta_2 s_1 \\
s_3 &= \zeta_3 s_2
,\end{align*}

and so 
\begin{align*}
\zeta_1 = \frac{s_1}{s_3} &= c \\
\zeta_2 = \frac{s_2}{s_1} &= c \\
\zeta_3 = \frac{s_3}{s_2} &= c
,\end{align*}

which shows that the 3 interior angles must be equal, yielding an equilateral triangle.

