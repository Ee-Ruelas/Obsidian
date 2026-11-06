
Maximal Margin Classifier
AKA Linear Support Vector Madle (SVM)
![[Pasted image 20260421153748.png|282]]
Question: of these possible linear classifiers
One Answer: $\rightarrow$ The one w/ the maximal margin
(maximum spacing from closest point(s))

Why? More robust to noisy data!

$P:$ Positive Margin Boundary in the blue $--$, 
Decision boundary: $\vec{\theta}\cdot \vec{x}+\theta_{0}=0$
N: Negative Margin Boundary red $--$
The arrows are call "support" vectors
![[Pasted image 20260421153832.png|639]]

How?
Minimize an objective function (optimization)

$$\underset{\text{Depends on }\vec{\theta},\theta,\delta_{n}}{J(\vec{\theta},\theta_{0})}=\underset{\text{quantifies unisclassifications}}{\text{Loss}}+\underset{\text{Inverse of margin size}}{\text{regularization}}$$

![[Lecture 7, Tuesday, April 21st-1776812024996.webp]]

How do we calculate the distance form a pr. to a line

$\vec{\theta}\cdot \vec{x}=0$
otherwise, projection of $\vec{x}$ on to $\vec{\theta}$ :
$d = \vec{x}\cdot \hat{\theta}=\frac{|\vec{x}\cdot \vec{\theta}|}{||\vec{\theta}||}$

$proj_{\vec{b}}\vec{a}=\frac{(\vec{a}\cdot \vec{b})}{||\vec{b}||^2}\vec{b}$  Note: If we're on the margin, $d=\frac{|\vec{\theta}\cdot \vec{x}}{||\vec{\theta}||}=\frac{1}{||\vec{\theta}||}$

What about a classifier line with an offset $\theta_{0}$?
![[Lecture 7, Tuesday, April 21st-1776812524580.webp|656]]

$$
\rightarrow  \vec{\theta}\cdot \vec{x}+\theta_{0}=0
$$
$$
\begin{align}
dist(\vec{x},L)=dist(\vec{x}-\vec{Q},L) \\
\vec{Q}=\lambda \cdot \vec{\theta} \\
\text{Since }\vec{Q} \text{ is in }L: \\
\vec{\theta}\cdot \vec{Q}+\theta_{0}=0 \\
\lambda||\vec{\theta}||^{2}+\theta_{0}=0 \\
\lambda ^{\cdot \vec{\theta}}=-\frac{\theta_{0}}{||\vec{\theta}||^{2}}\cdot \vec{\theta} \\
\vec{Q}=-\frac{\theta_{0}\vec{\theta}}{||\vec{\theta}||^{2}} \\
<!--ID: 1780191768349-->


\end{align}
$$
Finally
<!--ID: 1780191768350-->


$$
\begin{align}
\vec{x}-\vec{Q}=\vec{x}+\frac{\theta_{0}\vec{\theta}}{||\vec{\theta}||^{2}} \\
 \\
\therefore dist(\vec{x},L)=dist\left( \vec{x}+\frac{\theta_{0}\vec{\theta}}{||\vec{\theta}||^{2}},L \right) \\
 \\
\text{finding this distance as above:} \\
=\left( \vec{x} + \frac{\theta_{0}\vec{\theta}}{||\vec{\theta}||^{2}} \right)\cdot \frac{\vec{\theta}}{||\vec{\theta}||} \\
=\frac{\vec{x}\cdot \vec{\theta}}{||\vec{\theta}||}+\frac{\theta_{0}\vec{\theta}\cdot \vec{\theta}}{||\vec{\theta}||^{2}} \\
=\frac{\vec{\theta}\cdot \vec{x}+\theta_{0}}{||\vec{\theta}||}
\end{align}

$$
Thus, the signed distance for each point $i$: $\boxed{d^{i}=\frac{y^{i}(\vec{\theta}\cdot \vec{x}^{i}+\theta_{0})}{||\vec{\theta}||}}$
$\rightarrow$ equal to real distance when point is correctly classified consider a negative example on the -re boundary:

$$
d^{i}=\frac{y^{i}(\vec{\theta}\cdot \vec{x}^{i}+\theta_{0})}{||\vec{\theta}||}=\frac{1}{||\vec{\theta}||}

$$
Q: what happens when $||\vec{\theta}||$ increases? $\rightarrow$ d decreases
$\therefore$ To maximize the width of hte margins we must minimize $||\vec{\theta}||$

$$
min||\vec{\theta}||=min\sqrt{ \theta_{1}^{2}+\theta_{2}^{2}+\dots+\theta_{d}^{2} }
\leftarrow \text{dim of }\vec{\theta} \text{ not distance}

$$
but, since $\sqrt{  }$ are "hard" to compute, we'll use $\frac{1}{2}||\vec{\theta}||^{2}$ 
$\therefore$ we have our regularization term.

What about our loss term?

<mark style="background: #FF5582A6;">Hinge Loss</mark>        
Idea: Penalty should be:
$\rightarrow$ zero for properly classified pts. our side margin 
$\rightarrow$ linearly increasing for pts. inside

![[Lecture 7, Tuesday, April 21st-1776813911003.webp]]

![[Lecture 7, Tuesday, April 21st-1776814046055.webp]]

$Loss_{h}(y^{i}(\vec{\theta}\cdot \vec{x}^{i}+\theta_{0}))={\begin{cases}0,\quad if \quad z^{i}\geq_{1} \\ 1-z^{i}, \quad if\quad z^{i}<1 \end{cases}}$

What property of $Loss_{h}(z)$. Makes if good for optimization?
$\rightarrow$ its convex
To apply to a data set, we will compete the 
average hinge Loss $\rightarrow$ to be independent of $n$
$$
\frac{1}{n}\sum_{i=1}^{n}Loss_{h}(y^{i}(\vec{\theta}\cdot \vec{x}^{i}+\theta_{0}))
<!--ID: 1780191768351-->


$$
so, we have the objective function:
$$
J(\vec{\theta},\theta_{0})=\frac{1}{n}\sum_{i=1}^{n}Loss_{h}(z^{i})+\frac{||\vec{\theta}||^{2}}{2}
<!--ID: 1780191768353-->


$$
where $\lambda>0$ is a hyper parameter used to decide how to weight the two objectives (avoiding errors vs. maximizing the margin)

Effect of $\lambda$

![[Lecture 7, Tuesday, April 21st-1776814696005.webp]]

How do we knew when to stop decreasing $\lambda$?