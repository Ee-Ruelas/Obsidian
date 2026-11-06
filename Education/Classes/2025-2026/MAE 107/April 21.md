


Quiz this Thursday in class root-finding

LAST TIME
	NR formula to solve system of nonlinear equations
	 $\rightarrow$ derive from T.S; use Cramer's rule to solve (Chapm)
	 $\rightarrow$generalize through Jacobian matrix
$$
J = \begin{bmatrix}
\frac{ \partial f }{ \partial x }  & \frac{ \partial f }{ \partial x }  & \dots & \frac{ \partial f }{ \partial x }  \\
\frac{ \partial f }{ \partial x }  & \frac{ \partial f }{ \partial x }  & \dots & \frac{ \partial f }{ \partial x }  \\
\vdots \\
\frac{ \partial f_{n} }{ \partial x_{1} }  & \frac{ \partial f }{ \partial x }  & \dots & \frac{ \partial f_{n} }{ \partial x_{n} } 
\end{bmatrix}
$$
Newton Step
$$
x_{i+1} = x_{i} + \frac{f(x_{i})}{f'(x_{i})}
<!--ID: 1780191768358-->


$$
$(x_{i+1},y_{i+1})=(x_{i},y_{i})-J^{-1}f(x_{i},y_{i})$ 

## Review of linear *index notation*

$Ax =b$ (linear algebra)

$$
\begin{bmatrix}
a_{11} & a_{12}  & \dots \\
\vdots \\
a_{n1}
\end{bmatrix}
\begin{bmatrix}
x_{1} \\
x_{2} \\
\vdots \\
x_{n}
\end{bmatrix}
=\begin{bmatrix}
b_{1} \\
b_{2} \\
\vdots \\
b_{n}
\end{bmatrix}
$$
Cramers rule: each unkown in a system of linear eqns may be expressed as a function of two determinants

solving $Ax=b$
$$
x_{1} = \left|\begin{matrix}
b_{1} & a_{12} & a_{13} \\
b_{2} & a_{22} & a_{23} \\
b_{3} & a_{32} & a_{33}
\end{matrix}\right|/D \leftarrow  \det(A)
<!--ID: 1780191768359-->


$$
Ex:
$$
\begin{align}
3x_{1}+2x_{2} & =  18 \\
-x_{1}+2x_{2} & =  2 \\
\end{align}
\Rightarrow 
A=\begin{bmatrix}
3 & 2 \\
-1  & 2 
\end{bmatrix}
;B=\begin{bmatrix}
18 \\
2
\end{bmatrix}
<!--ID: 1780191768360-->


$$
$$
x_{2} = \frac{\left|\begin{matrix}
3 & 18 \\
-1 & 2
\end{matrix}\right|}{\left|\begin{matrix}
3 & 2 \\
-1 & 2
\end{matrix}\right|}
$$
<!--ID: 1780191768361-->


Determinant in index notation

$$
\det(A) = \sum_{j=1}^{N}A_{kj}C_{kj}

$$
$$
C_{ij} = (-1)^{i+j}M_{ij}
$$
sum of product of matrix elements w/associated cofactors across any column or row
<!--ID: 1780191768362-->


$M_{ij}$ is $\det$ of matrix formed by disregarding $i^{th}+j^{th}$ row + col (cofactor)

(Me: same thing we've always done)

![[Pasted image 20260421082229.png|293]]


Gaussian Elimination
Goal : solve system of equations

$$
\begin{align}
(1)\quad2u +v + 2w  & =5 \\
(2)\quad4u -6v &=-2 \\
(3)\quad-2u +7v +2w &= 9 \\
\end{align}
\Rightarrow 
\begin{bmatrix}
2 & 1 & 1 \\
4 & -6 & 0 \\
-2 & 7 & 2
\end{bmatrix}
\begin{bmatrix}
u \\
v \\
w
\end{bmatrix}
=
\begin{bmatrix}
5 \\
-2 \\
9
\end{bmatrix}
$$
Step 1: Subtract multiple of (1) from others 
(2)$-2\times(1)$
(3)$-(-1)\times(1)$

$$
\begin{align}
2u+v & +w&=5 \\
-8v &  -2w  & =-12 \\
8v &  + 3w  & =14
\end{align}
$$
Step 2: Subtract multiples of (2)
(3) $- (-1)\times(2)$
result:
$$
\begin{align}
2u +  v+ & w  & = 5 \\
  -8v - & 2w  & = -12 \\
    & 1w  & =2
\end{align}
$$
Pivots (entries on diagonal)

Solve w/ back substitution

$$
\begin{align}
w=2 \\
v=1 \\
u=1
\end{align}
$$
What can go wrong?
	$n$ pivots $\rightarrow$ one solution (what we want)
What if pivot is zero?
	row exchange 
If no full set of pivots, system is singular.

Singular example:

$$
\begin{align}
u  & + v +w & =\underline{} \\
2u & +2v+5w & =\underline{} \\ 
4u &  + 4v +8w & =\underline{}
\end{align}
$$
$$
\begin{align}
  1u + v + w  & =\underline{} \\
   0+3w & =\underline{} \\
  4w & =\underline{}
\end{align}
$$
$$
\begin{align} \\
\text{no solutions} \\
<!--ID: 1780191768363-->


3w=6 \\
4w=7 \\ 
\text{infinite solutions} \\

3w=6 \\
4w=8
\end{align}
$$

pseudo-code for Gauss Elimination

back substituion
	$x_{n} = b_{n}/a_{nn}$
 ```matlab
for i=n-1: -1:1
	sum = b(i);
	for j = i+1:n
		sum = sum-a(i,j)*x(j)
	end
	x(i)=sum/a(i,j);
end
 ```


foward elimination
```matlab
for k = 1:n-1
	for i = k+1:n
		factor=a(i,x)/a(k,k)
		for j = x+1:n
			a(i,j)=a(i,j)-factor*a(k,j)
		end
		b(i)=b(i)-factor*b(k)
	end
end
```

!dont set entries below diagonal  $=0$!

<mark style="background: #BBFABBA6;">how many operations?</mark> Count hops

additions/subtractions & multiplications/divisions about the same 
need total # operations

$\rightarrow$ first pass outer loop $k=1\rightarrow$ inner loop $i=2:n$ 
	# iterations in middle loop $\sum ^{n}_{i=1} = n-2+1=n-1$
	for each of these 
		- 1 division (for factor)
		- interior loop $2:n$
		- 1 mult. + 1 subtraction
	inner loop:
	# mult $=1+\underset{\text{inner loop}}{[n-2+1]}+1=1+n$
	total mult: $(n-1)(n+1)$
	 # subtractions
		$[n-2+1]+1=n$
	total $(n-1)(n)$


Sum all up:

| $\underset{k}{\text{outerloop}}$ | $\underset{i}{\text{middle loop}}$ | $\underset{+/- \quad \times/\div}{\text{flops}}$ |
| -------------------------------- | ---------------------------------- | ------------------------------------------------ |
|                                  |                                    |                                                  |
|                                  |                                    |                                                  |

Similar analysis  $\times/\div$ gives $\frac{n^{3}}{3}+O(n^{2})$
soln:$\boxed{\frac{2n^{3}}{3}+O(n^{2})}$ $\leftarrow$ foward elimination

back subst. $=n^{2}+O(n)$
total for G.E.:
$\frac{2n^{3}}{3}+O(n^{2})+O(n)$
$=\frac{2}{3}n^{3}+O(n^{2})$




![[April 21 2026-04-25 19.46.45.excalidraw]]