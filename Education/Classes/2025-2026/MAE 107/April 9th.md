

The false position method,
 - Exploit graphical insight by joining $f(x_{l})$ and $f(x_{u})$ by a straight line
 - Intersection of this line w/x-axis is new estimate $(x_{r})$

$x_{l} =  x\text{-lower}, x_{u} = x\text{-upper}$

**This method includes information about function (based on shape of function)
	$\rightarrow$next guess intersection w/ x-axis
$$
\frac{f(x_{l})}{x_{r}-x_{l}} = \frac{f(x_{u})}{x_{r}-x_{u}}
<!--ID: 1780191768355-->



$$
$$
\begin{align}
f(x_{l})(x_{r}-x_{u}) = f(x_{u})(x_{r}-x_{l}) \\
x_{r} = \frac{x_{u}f(x_{l}) - x_{l} f(x_{u})}{f(x_{l})-f(x_{u})} \\
\boxed{x_{r} = x_{u} - \frac{f(x_{u})(x_{l}-x_{u})}{f(x_{l})-f(x_{u})} }
\end{align}
$$
<!--ID: 1780191768356-->



$$
\begin{align}
t= 10\mathrm{s} \\
g =9.8 \mathrm{m/s^2} \\
v = 40\mathrm{m/s} \\
m = 68.1\mathrm{kg} \\
\end{align}
$$
1. Choose upper $(x_{u})$ and lower $(x_{l})$ bounds, st function changes sign in interval
2. estimate $x_{r}$
$$
\begin{align}
v = \frac{gm}{c}(1-e^{-(4m)t}) \\
\text{find } f(c)=0 \\
\rightarrow x_{l} =12 \quad x_{u} = 16 \\
f(x_{l}) = 6.099 \\
f(x_{u}) = -2.2688 \\
 \\
\text{Plug to } x_{r} \text{ equation}  \\
x_{r} =\frac{ 16 - (-2.2688)(12-16)}{6.099 - (-2.2688)} = 14.9113 \\
f(x_{l})f(x_{u}) <0 \leftarrow \text{if coding this would be if statement} \\
x_{r} = \text{new upper bound} \\
\text{next iteration} \\
x_{u} = 14.9113 \quad f(x_{u}) = 6.0699 \\
x_{l} = 12 \quad f(x_{l}) = -0.2543 \\
\text{ plug back to } x_{r} \\
=14.7992
\end{align}
$$

## Ch.6 Open Methods


$\rightarrow$ only require a single starting value of $x$ (no bracket)

### Fixed pt iteration 
Generate new iterations by successive subst.
Write the func as $x = g(x)$
e.g. $x^2 + 2x +3 =0 \rightarrow \frac{x^2+3}{2} = x$




