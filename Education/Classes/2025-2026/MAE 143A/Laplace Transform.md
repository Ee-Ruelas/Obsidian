$$
F(s) =\mathcal{L}\{f\}(s) =  \int_0^\infty f(t)e^{-st}dt
$$
Example: 
$$
f(t) = 1
$$
$$
\mathcal{L}\{f(t)\} = F(s) = \int_0^\infty 1e^{-st}dt = \frac{e^{-st}}{-s}\Big|_0^\infty = (0 - \frac{1}{-s}) = \boxed{\frac{1}{s}}
$$

In signals and systems there is a use of the imaginary number or rather [[Euler's Formula]], to create: $s = \sigma + j\omega$.

Example:$$
x_1(t) = 10 \cos{(12t + 60^\circ)}u(t)
$$
$$
\begin{align}
\mathcal{L}\{f(t)\} &= F(s) = \int_0^\infty [10\cos{(12t + 60^\circ)}u(t)]e^{-st} dt  = 10\int_0^\infty \cos{(12t+60)}u(t)e^{-st}dt \\
&\rightarrow u(t) = 1 \text{ for }t\\
& = \int_0^\infty \cos{(12t+60)}e^{-st}dt \rightarrow \text{Integration by parts}\\
& \Rightarrow \text{Let's say that c is the contents inside of cosine. }
\end{align}
$$
Do [[Integration by Parts]] (IBP) to solve for the integral.

| $u$              | $dv$                 |
| ---------------- | -------------------- |
| $\cos{(cx+a)}$   | $e^{-st}$            |
| -$c\sin{(cx+a)}$ | $\frac{e^{-st}}{-s}$ |
