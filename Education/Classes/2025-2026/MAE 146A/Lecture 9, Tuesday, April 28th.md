# Linear Regression


For classifications , $s_{n}= \{\vec{x}^{i},\vec{y}^{i}|i=1,\dots,n\}$

![[Lecture 9, Tuesday, April 28th-1779811621973.webp]]
E.g. : Buting/Selling stock $y^{i}\epsilon\{+1,-1\}$
But, we could instead want to predict $y^{i}\epsilon \mathbb{R}$ (price of stock)

Regression Problems

$\vec{x}^{i}\epsilon \mathbb{R}^{d}, \quad y^{i}\epsilon \mathbb{R}$
Goal: Find a mapping of $f(\vec{x}^{i},\vec{\theta},\theta_{0})=y^{i}$

Linear Regression: Linear mapping (hyperplane)
$f(\vec{x},\vec{\theta},\theta_{0}) = y^{i}=\vec{\theta}\cdot \vec{x}+\theta_{0}$
![[Lecture 9, Tuesday, April 28th-1779811986305.webp]]
Topics to discuss:
- How to select $\vec{\theta},\theta_{0}$? What is the objective function that we will optimize?
- Learning algorithms
	- $\rightarrow$ SGD
	- $\rightarrow$ closed-form solution
- Regularization/Generalization
	- $\rightarrow$ Ridge Regression
	- $\rightarrow$ Casso Regression
Defining the objective function for Linear Regression
**Empirical Risk Function (Score Function)

Assume $\theta_{0}=0$ for now
$$
R_{n}(\vec{\theta})=\frac{1}{n}\sum_{i=1}^{n}\text{Loss}(y^{i}-\underset{f(\vec{x}^{i},\theta)}{\vec{\theta}\cdot \vec{x}^{i}})
$$

![[Lecture 9, Tuesday, April 28th-1777418300701.webp]]

Instead of Loss$_{h}$ which we used for classification we often use squared error or L2 loss, $\text{Loss}_{\text{L2}}(\vec{z})=\frac{||\vec{z}||^{2}}{2}$ which gives:

$$
R_{n}(\vec{\theta})=\frac{1}{n}\sum_{i=1}^{n} \frac{(y^{i}-\vec{\theta}\cdot \vec{x})^{2}}{2}
$$
Why do we square the errors?

$\text{Loss}(z)= z \rightarrow \text{errors of opposite signs would cancel}$
$\text{Loss}_{\text{L1}}(z)=|z| \rightarrow \text{all these regressions would look just as bad \downarrow}$

![[Lecture 9, Tuesday, April 28th-1777418808479.webp]]

As w/ classification, our real objective is to minimize the test error or score of the regression

$$
R_{w}(\vec{\theta})=\frac{1}{m}\sum ^{A+m}_{i=u+1} \frac{(y^{i}-\vec{\theta}\cdot \vec{x})^{2}}{2}
\quad
\text{on } \tau_{m} = \text{test date}

$$
Two types of mistakes/factors leading to large $R_{n}$(or $R_{a}$)
	i) structured error
$\rightarrow$ linear mapping not sufficient to predict trend of data
![[Lecture 9, Tuesday, April 28th-1777419186135.webp]]

$\rightarrow$ should use polynomial fir hete
$f(\vec{x})=\theta_{0}+\theta_{1}x_{1}+\theta_{2}x_{2}+\theta_{11}x_{1}^{2}+\theta_{22}x_{2}^{2}+\theta_{12}x_{1}x_{2}$

ii) Ene


Learning Algorithms (SGD)


| Inputs: <br>Init: | $S_{n},T$<br>$\theta_{0}=0$ |
| ----------------- | --------------------------- |
|                   |                             |
|                   |                             |
```python
for k=1,...,T
	set \eta_k =1/k (or 1/1+k)
	randomly pick i in {i,...,n}
	
```

$$
\nabla_{\theta}\left[ \frac{(y^{i}-\vec{\theta}\cdot \vec{x}^{i})^{2}}{2} \right]=\frac{2(y^{i}-\vec{\theta}\cdot \vec{x}^{i})}{2}(-\vec{x}^{i})=-(y^{i}-\vec{\theta}\cdot \vec{x}^{i})\vec{x}^{i}
$$
$\therefore$update in SGD becomes:
$$
\vec{\theta}_{k}=\vec{\theta}_{k-1}+\eta_{k}(y^{i}-\vec{\theta}_{k-1}\cdot \vec{x}^{i})\vec{x}^{i}
<!--ID: 1780191768346-->


$$
Problem: tends to overfit data $\rightarrow$ need regularization

Closed-form solution
$\hat{\theta}$ is optimal $\vec{\theta}$ that satisfies $\nabla_{\vec{\theta}}R_{n}(\vec{\theta})|_{\vec{\theta}=\hat{\theta}}$



$$
\vec{\phi}=-\frac{1}{n}\sum ^{n}_{i=1}(y^{i}-\vec{\theta}\cdot \vec{x}^{i})\vec{x}^{i}
$$
$$
\vec{\phi}=-\frac{1}{n}\sum ^{n}_{i=1}y^{i}\vec{x}^{i}+\frac{1}{n}\sum_{i=1}^{n}(\vec{\theta \cdot \vec{x}^{i}})\vec{x}^{i}
$$

$$
\vec{\phi}=-\vec{b}+\frac{1}{n}\sum_{i=1}^{n}\vec{x}^{i}\vec{x}^{i^{T}}\vec{\theta}

$$
If A is invertible: $\vec{\theta}=A^{-1}\vec{b}$
Problems: 
- $\rightarrow$ A is not necessarly inveritble (need $u\gg d$)
- $\rightarrow$ Computing