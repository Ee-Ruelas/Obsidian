
## Concepts
A few concepts for ML
1. Notation
2. Functions of several variables
3. Convexity
4. Critical points (minima/maxima)
5. The Gradient & the Hessian 
6. The second-order derivative test


## 1 Notation

$\rightarrow$ If $A$ is a set, and $a$ is an elemetn of the set, we write $a \epsilon A$, $\epsilon$ is an element of
$\rightarrow$ If $B$ is a subset of $A$, we write: $B\subseteq A$

$\rightarrow$ we describe sets with $\{\cdot\}$ e.g.
$A  = \{1,2,3\}$
$\rightarrow$ we can use logical rules to define sets, e.g:
$A = \{n\epsilon N|n<4\} \{1,2,3\}$
set of natureal numbers(the integers), condition

## 2 Functions of several variables
$f:D\subseteq \mathbb{R}^m \rightarrow \mathbb{R}$
domain: vectors of dimension $m$  $\vec{x} = \left[\begin{matrix}x_{1}  \\  x_{2}  \\  \vdots  \\ x_{m}\end{matrix}\right]$
$f$ may also depend on a parameter
which we typically cal $\theta$
e.g: line or hyper plane

takes a vector that describes a point, returns 0 if the pt. is on the line/plane:

$$
\begin{align}
l = \{\vec{x}=(x,y)|\vec{n}^T \vec{x} + \theta=0\} \\
\vec{n}  = (n_{1},\dots,n_{m}) \\
\vec{x}  = (x_{1},\dots,x_{m}) \\
\theta\epsilon\mathbb{R} \\
\end{align}



$$

here: $m= 2; \quad \vec{n} = (1,1), \quad \theta=-1$

for $x_{1}=(1,0), \quad n^{-T}\vec{x}+\theta=\left[\begin{matrix} 1  & 1\end{matrix}\right]$ 





## 3 Convexity

Sets: A set $D$ is convex if for any $\vec{x}, \vec{y}$ in $D$, the segment $\left[\begin{matrix} \vec{x} & \vec{y} \end{matrix}\right]$ is also in $D$.

e.g. 

How can we find all the points on the segment $\left[\begin{matrix} \vec{x} & \vec{y} \end{matrix}\right]$?

$\vec{z}=\lambda \vec{x} + (1-\lambda)\vec{y},  \quad  \lambda\epsilon\left[\begin{matrix} 0 & 1 \end{matrix}\right]$

Functions: A function is convex if two conditions hold.
1) The domain, $D$, of the $f^{\underline{n}}$ is a convex set (see above)
2) $f(\vec{z})\leq \vec{\omega}$       if $f(\vec{z}) < \vec{\omega}\rightarrow \text{strictly convex}$
   where: $\vec{z} = \lambda \vec{x} + (1-\lambda)\vec{y}\rightarrow \text{points on the segment } \left[\begin{matrix} \vec{x} & \vec{y} \end{matrix}\right]$
   where: $\vec{\omega}= \lambda f(\vec{x}) + (1-\lambda)f(\vec{y})\rightarrow \text{linear interpolation b/w} f(\vec{x}) \& f(\vec{y})$
Graphically: for $m=1$


## 4 Minima & Maxima of a $f^{\underline{n}}$

A point $\vec{x}_{0}$ on a function domain is a:
1) local minimum if $f(\vec{x}_{0})\leq f(\vec{x})$ for $\vec{x}$ in the vicinity of $\vec{x}_{0}$
2) local maximum if $f(\vec{x}_{0})\geq f(\vec{x})$ for $\vec{x}$ in the vicinity of $\vec{x}_{0}$
3) global minimum if $f(\vec{x}_{0})\leq f(\vec{x})$ for all $\vec{x}$ in $D$
4) global maximum if $f(\vec{x}_{0})\geq f(\vec{x})$ for all $\vec{x}$ in $D$

Graphical Example:


If $f$ is convex if all local minimums are global minimums
$\rightarrow$ comes from the above definition of convexity 
Also note:
   $f$ is concave (strictly concave) if $-f$ is convex (strictly convex) respectfully
   $\rightarrow$ minus sign flips the graph
## 5 The Gradient & the Hassion of a differentiable function

Gradient: $f$ is differentiable if partial derivatives of $f$ exist
The gradient of $f$ is given by the vector: 

$$
\nabla f(\vec{x})= \left[\begin{matrix}
\frac{ \partial f }{ \partial x_{1} }  \\
\frac{ \partial f }{ \partial x_{2} } \\
\vdots \\
\frac{ \partial f }{ \partial x_{n} } 
\end{matrix}\right]
\epsilon
\mathbb{R}^m
$$
$\nabla f(\vec{x})$ is a vector on the plane tangent to $f$ at $\vec{x}$ that points in the direction of maximal increase of $f$

1D case




Hessian: If a function is twice differentiable, its Hassian is 

$Hf(\vec{x})=\left[\begin{matrix} \frac{ \partial f }{ \partial x }\end{matrix}\right]$