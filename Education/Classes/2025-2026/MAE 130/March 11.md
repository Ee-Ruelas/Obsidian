
Wednesday

# Topic 8 - IDOF: Free Vibrations


## Review 

Vibrations of discrete systems have been done throughout the entire class. So the mass is only been in one location (blocks). 

Now we can do shafts which have density and energy as a function of $x$ so $\therefore \rho(x)\quad E(x)$.

For a rod the vibration equations take the form of:
$$
\rho A \frac{ \partial y }{ \partial x }
$$


## Example 1
$$
\begin{align}
u(t) = A^{(1)} [B_{1}\cos(\omega_{1}t)+B_{2}\sin(\omega_{2}t)]+A^{(2)}[B_{1}\cos(\omega_{1})t+B_{2}\cos(\omega_{2}t)]+\dots \\  \\
a_{0} = \frac{2}{T}\int_{-\frac{T}{2}}^{ \frac{T}{2} } f(t)dt\quad a_{n} = \frac{2}{T}\int_{-\frac{T}{2}}^{ \frac{T}{2}} f(t)\cos(r\omega t)dt\quad \\
u(x,t=0) = u_{0}(x) =\sum C_{n} \sin(k_{n}x ) \\ 
\dot{u}(x,t=0) = \dot{u}_{0} (x) = \sum \omega_{n}D_{n}\sin(k_{n}x) \\
C_{n}=\frac{2}{l}\int_{0}^{l} u_{0}(x)\sin(k_{n}x)dx\quad A_{n} =\frac{2}{l\omega_{n}} \int_{0}^{l}\dot{u}_{0}(x)\sin(k_{n}x) dx
\end{align}
$$