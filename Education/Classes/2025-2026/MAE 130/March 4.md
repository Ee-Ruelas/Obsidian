	
# Example 1
$$
\begin{align}
\text{SDOF\quad} m =100, \quad= 20,\quad k = 2000,\quad F = 1000\text{ for } \frac{1}{100}s & \\ 
u_{0} = 0, \quad \dot{u}_{0} = 0  \\
u(t) = \frac{F\Delta t}{m\omega _{d}}e^-\zeta\omega_{0}t \sin(\omega_{d}t) \\
\omega_{0}=\sqrt{ \frac{k}{m} } = \sqrt{ 20 } \\
\frac{c}{m }= 2\zeta \omega_{0} \therefore \zeta=\frac{c}{2m\omega_{0}} = 0.022 \\
\omega_{d} - \omega_{0}\sqrt{ 1-\zeta^{2} }=4.471 \\
f\Delta=10 \\
u(t)=\frac{f\Delta t}{m\omega_{d}}e^{-\zeta \omega_{0}t} \sin(\omega_{d}t) \\
\\
<!--ID: 1773723550757-->


\end{align}
$$

# Example 2

$$
\begin{align}
\text{SDOF:} \quad m=1, \quad c = 2,\quad k = 4,\quad F = 1,\quad u_{0} = 1, \quad\dot{u}_{0} = -1 \\
m \ddot{u} + c \dot{u} + ku =  \\
\omega_{c}^{2}=\frac{k}{m}=4 \therefore \omega_{0}=2 \\
\frac{c}{m} = 2\zeta \omega_{0}\therefore\zeta=\frac{c}{2m\omega _{0}}=\frac{1}{2}\quad\text{underdamped} \\
\omega _{d}=\omega_{0}\sqrt{ 1-\zeta ^{2} }=\sqrt{ 3 } \\
u(t)=u_{h}(t)+u_{1}(t)+u_{2}(t) \\
u_{h}(t) = e^{-\zeta \omega_{0}t}[B_{1}\sin(\omega_{d}t)+B_{2}\cos(\omega_{d}t)] \\
u_{1}(t)=\frac{\hat{F}}{m \omega_{d}}e^{-\zeta \omega_{d}t}\sin(\omega_{d}t) \\
u_{2}(t)=-\frac{\hat{F}}{m\omega _{d}}e^{-\zeta \omega _{0}(t-\tau)}\sin[\omega_{d}(t-\tau)]H(t-\tau) \\


\end{align}

$$