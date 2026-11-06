


- Quiz 2 next Thursday $\rightarrow$ Practice Problem set #2
- 1.5 % extra credit to Final Grade.
	- 95% of lectures for majority of lecture (1hr 10min)



## Quiz 2 material cont.

To derive a two eqn NR formula, need T.S. w/ two variables.

$$
\frac{ \partial u_{i} }{ \partial x } x_{i+1} + \frac{ \partial u_{i} }{ \partial y } y_{i+1} = -u_{i} + x_{i}\frac{ \partial u_{i} }{ \partial x } + y_{i}\frac{ \partial u_{i} }{ \partial y }    
$$
$$
\frac{ \partial u_{i} }{ \partial x } x_{i+1} + \frac{ \partial u_{i} }{ \partial y } y_{i+1} = -u_{i} + x_{i}\frac{ \partial u_{i} }{ \partial x } + y_{i}\frac{ \partial u_{i} }{ \partial y }   
$$

Use Cramer's Rule:

$$
\begin{align}
x_{i+1} = x_{i}- \frac{u_{i}\frac{ \partial v_{i} }{ \partial y } -v_{i}\frac{ \partial u_{i} }{ \partial y } }{\frac{ \partial u_{i} }{ \partial x } \frac{ \partial v_{i} }{ \partial y } -\frac{ \partial u_{i} }{ \partial y } \frac{ \partial v_{i} }{ \partial x } } \\\text{determinant of jacobian}
 \\
y_{i+1} = y_{i} - \frac{u_{i}\frac{ \partial v_{i} }{ \partial x } -v_{i}\frac{ \partial u_{i} }{ \partial x } }{\frac{ \partial u_{i} }{ \partial x } \frac{ \partial v_{i} }{ \partial y } -\frac{ \partial u_{i} }{ \partial y } \frac{ \partial v_{i} }{ \partial x } } \\
\end{align}
$$
$\rightarrow$ can generalize through Jacobian matrix (not in chapter)

Jacobian matrix is a matrix of partial derivatives of a vector function $[f_{1},f_{2},f_{3},\dots,f_n]$ wrt $[x_{1},x_{2},x_{3},\dots x_{n}]$

$$
\begin{bmatrix}
\frac{ \partial f_{1} }{ \partial x_{1} }  & \frac{ \partial f_{1} }{ \partial x_{2} } &  \frac{ \partial f_{1} }{ \partial x_{3} }  & \dots & \frac{ \partial f_{1} }{ \partial x_{n} }  \\
\frac{ \partial f_{2} }{ \partial x_{1} }  & \frac{ \partial f_{2} }{ \partial x_{2} } &  \frac{ \partial f_{2} }{ \partial x_{3} }  & \dots & \frac{ \partial f_{2} }{ \partial x_{n} }  \\
\vdots \\
\frac{ \partial f_{n} }{ \partial x_{1} }  & \dots & \dots & \dots & \frac{ \partial f_{n} }{ \partial x_{n} } 
\end{bmatrix}

$$
from above (2-known T.s. deriv):

$$
(x_{i+1},y_{i+1})\begin{bmatrix}
\frac{ \partial u_{i} }{ \partial x }  & \frac{ \partial u_{i} }{ \partial y }  \\
\frac{ \partial v_{i} }{ \partial x } \frac{ \partial v_{i} }{ \partial y } 
\end{bmatrix}\rightarrow \text{pull out Jacobian matrix}

$$
recall  newton step:

$x_{i+1} = x_i -  \frac{f(x_{i})}{f'(x_{i})}$
$\rightarrow$ solve for next guess by inverting Jacobian matrix
$\rightarrow$ In Cramer's rule, divide by the det of matrix in our case matrix is Jacobian

$$
J^{-1} = \text{equivalent } \frac{1}{f'(x)}

$$
$$
\underset{\text{new guess}}{(x_{i+1},y_{i+1})}=\underset{\text{prev guess}}{(x_{i+1},y_{i+1})}-J^{-1}f(x_{i},y_{i})
$$
all vectors
   (vector of $x's$, vector of roots)
<!--ID: 1780191768364-->




End of Quiz 2 Material 

## Review of Linear Algebra

Review of basic matrix manipulations

Matrix $A = \begin{bmatrix}A_{11} &  A_{12}  & A_{13}  & \dots \\ A_{21} \\ A_{31} \\ \vdots  &   &   & A_{m,n} \end{bmatrix}$
dimension $N\cross M$
vector an ordered collection of elements

$$
c=\begin{bmatrix}
c_{1}  \\
c_{2} \\
\vdots \\
c_{n}
\end{bmatrix}
\quad
a = \begin{bmatrix}
a_{1} \\
a_{2} \\
a_{3}
\end{bmatrix}
\quad
b = \begin{bmatrix}
b_{1} \\
b_{2} \\
b_{3}
\end{bmatrix}
$$
$c=a+b = \begin{bmatrix}a_{1}+b_{1} \\ a_{2}+b_{2} \\ a_{3}+b_{3}\end{bmatrix}$

multiply by scalar

$\alpha a = \begin{bmatrix}\alpha a_{1} \\ \alpha a_{2} \\ \alpha a_{3}\end{bmatrix}$

transpose

$A = \begin{bmatrix} 1 & 2 \\ 3 & 4 \\ 5 & 6\end{bmatrix}$         $A^T = \begin{bmatrix}1 & 3 & 5 \\ 2 & 4 & 6\end{bmatrix}$

symmetric if $A=A^T$

Trace: sum of elements on diagonal
	$tr(A) = a_{11} + a_{22}+ a_{33} + \dots + a_{nn} = \sum a_{ii}$

identity matrix 

$$
\begin{bmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1
\end{bmatrix}
$$


matrix inverse

$AA^{-1}=A^{-1}A=I$

matrix multiplication 

$A_{N\cross M}B_{M\cross L}=C_{N \cross L}$

$$
C_{ij}=\sum_{k=1}^{N}A_{i,k}B_{k,j}\leftarrow \text{index notation}
$$
properties: 
- if $AB=0$ it is not necessary for either $A$ or $B$ $= 0$
- $(AB)^T = B^TA^T$

System of equations:

$$\begin{align}a_{11}x_{1}+a_{12}x_{2}+\dots+a_{n}x_{n}=b_{1} \\
a_{21}x_{1}+a_{22}x_{2}+\dots+a_{2n}x_{n}=b_{2} \\
\vdots    \\
a_{31}x_{1}+a_{32}x_{2}+\dots+a_{3n}x_{n}=b_{n}\end{align}$$

write index notation 
$$
b_{i} = \sum_{j=1}^{n} a_{ij}x_{j} \leftarrow  \text{useful for coding}
<!--ID: 1780191768366-->


$$
einstein convention leave out sum
$$
b_{i}=a_{ij}x_{j}
<!--ID: 1780191768368-->


$$


Determinants:

$det(A)$
What is it good for?
 1) test invertibility
	 1) $\det(A) =0 \text{ A is singular-inveritble}$
2) $\det(A-\lambda)$ characteristic eqn for eigenvalues
3) det gives formula for ivots


$$
\det \begin{bmatrix}
a & b \\
c & d  \\
\end{bmatrix}
=ad-bc

$$
$$
\det \begin{bmatrix}
a_{11}  & a_{12} &  a_{13} \\
a_{21}  & a_{22} &  a_{23} \\
a_{31}  & a_{32} &  a_{33}
\end{bmatrix}
=a_{11}\det \begin{bmatrix}
a_{22}  &  a_{23} \\
a_{32}  & a_{33}
\end{bmatrix}-a_{12}
\begin{bmatrix}
a_{21} & a_{23} \\
a_{31}  &  a_{33}
\end{bmatrix}+a_{13}
\begin{bmatrix}
a_{21} & a_{22} \\
a_{31}  & a_{32}
\end{bmatrix}
$$
some properties
- $\det(\alpha A) = \alpha^N \det(A)$
- $\det(A^T)=\det(A)$
- $\det(A^{-1})=\frac{1}{\det(A)}$
- $\det(AB)=\det(A)\det(B)$
- $\det(I) = 1$
<!--ID: 1780191768369-->



write in matrix form: $Ax=b$ system of eqn

$$
\begin{bmatrix}
a_{11} &  a_{12}  & \dots &  a_{1n} \\
a_{21} \\
\vdots \\
a_{n 1}  & \dots & \dots & a_{nn}
\end{bmatrix}
\begin{bmatrix}
x_{1} \\
x_{2} \\
\vdots \\
x_{n}
\end{bmatrix}=
\begin{bmatrix}
b_{1} \\
b_{2} \\
\vdots \\
b_{n}
\end{bmatrix}

$$
for small systems, we know how to solve by substitution, graphing 

Ex:

$3x_{1}+2x_{2}=10$
$-x_{1}+2x_{2}=2$
![[Pasted image 20260417003850.png]]


There can be no, infinite, singular solutions 

There is also slopes that are close,
$\rightarrow$ ill conditioning 
