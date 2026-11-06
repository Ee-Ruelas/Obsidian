



LAST TIME
$$
x_{r} = \frac{x_{u}F(x_{l}) - x_{l}f(x_{u})}{F(x_{l})-f(x_{u})}
<!--ID: 1780191768370-->


$$
false position method intro
open methods

## False Position continued

write our function as $x=g(x)$ 
$f(x) = \sin x=0$
(add $x$ to both sides $\rightarrow$ for eqn. to take approp. form)
$x = \sin x +x$
$x=g(x) \Rightarrow x_{i+1} = g(x_{i}) \leftarrow$ $i$ represents iteration # (prev spatial w/T.S)

find root of $f(x) = e^{-x}-x = 0$

$x = e^{-x}$
$x_{i+1} = e^{-x_{i}}$
initial guess $x_{0}= 0$    $i=0\leftarrow$ our guess

$x_{1}-e^{-x_{0}}=1, \quad i=1$
$x_{2}=e^{-1}=0.368$
$x_{3}=e^{-0.368}=0.6922$
   $\vdots$
$x_{18} =0.5648, \quad i=10$



## Newtons Method


![[Pasted image 20260417003826.png]]

new root approx. $(x_{i+1})$
$=$ pt. where tangent line crosses the $x$ axis

geometric interpretation
slope at pt $=f'(x)=\frac{f(x_{i})-0}{x_{i}-x_{i+1}}$
rearrange 
$\boxed{x_{i+1}=x_{i}-\frac{f(x_{i})}{f'(x_{i})}}$ Newtons Raphson formula

example: find root of $f(x) = e^{-x} - x$
initial guess $x_{0} = 0$
$f'(x) = -e^{-x} -1$
$x_{i+1} = x_{i}- \frac{e^{-x_{i}}-x_{i}}{-e^{x_{i}}-1}$
$x_{1} = 0 - \frac{e^0 - 0}{-e^0  -1} = \frac{1}{2}$
$x_{2} = \frac{1}{2} - \frac{e^{-1/2}-\frac{1}{2}}{-e^{-1/2}-1} = 0.5663$

Newton Raphson can also be derived from Taylor Series 

$f(x_{i+1}) = \underset{\text{keep 1st two terms (1st order)} }{f(x_{i}) + f'(x_{i})(x_{i+1}-x_{i})} + \frac{f''(x_{i})}{2}(x_{i+1}-x_{i})^2$

at intersection  w/ 

$0 = f(x_{i}) + f'(x_{i})(x_{i+1}-x_{i})$
solving for $x_{i+1}$
$x_{i+1} = x_{i} - \frac{f(x_{i})}{f'(x_{i})}$
estimate our error: from MVT and $x_{i+1}= x_{r}$ to be true value

$0 = f(x_{i}) + f'(x_{i})(x_{r}-x_{i}) + \frac{f''(\zeta)}{2!}(x_{r}-x_{i})^2$    $(2)$
$E_{t,i+1} = x_{r } -x_{i+1}$ 
(total error at $i+1$ iteration) = exact root - $i+1$ guess
eqn$(z)$ becomes
$0 = f'(x_{i})E_{t,i+1} + \frac{f''(\zeta)}{2!}E_{t,i}^2$
rearrange
$E_{t,i+1} = -\frac{f''(x_{r})}{2f'(x_{r})}E_{t,i}^2 \leftarrow \text{"quadratic convergence"}$ # sig figs doubles w/ each iterations

Caveats
BUT no general convergence