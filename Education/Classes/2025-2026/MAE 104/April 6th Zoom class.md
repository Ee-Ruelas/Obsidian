


Momentum
$$
\frac{d}{dt} \left( \int_{CV} \rho \bar{V}dV \right) + \int_{CS} \rho \bar{V} (\bar{V}\cdot \bar{n}) dS = -\int_{CS} P\bar{n}dS + \int_{SC} \bar{\bar{\tau}}\cdot \bar{n} dS + \int_{CV} \rho gdV
$$

The gravity is negligible do to being $\bar{V} \cdot \bar{V}  = |\bar{V}|^2$ which is pretty much 0.


![[Pasted image 20260417003139.png]]
$$

$$


$$
\frac{d}{dt} \left[ \int_{CV}\rho\left( e+\frac{\bar{V^2}}{2} \right)dV \right] + \int_{CS} \rho\left( e+\frac{\bar{V^2}}{2} \right)\bar{V}\cdot \bar{n}dS = - 
$$


## Example:

![[Pasted image 20260417003235.png]]

Airfoils being stacked (infinitely) upon each other to help with calculations when solving for compressors.

The solution is transitionally invariant.

Choosing a streamline as a CV, since its tangent to the velocity field so at the top $\bar{V}\cdot \bar{n} = 0$. Normal unit vector is always pointing outward. CV can only be fluid, so you have to not include the airfoil thats why its also not included.

![[Pasted image 20260406083755.png]]



$$
\frac{d}{dt} \left( \int_{CV}\rho dV \right) + \int_{CS} \rho \bar{V}\cdot \bar{n}dS = 0
$$
Steady so $\frac{d}{dt} = 0$

$$
\int_{CS} \rho \bar{V}\cdot \bar{n}dS = 0 \Rightarrow \int_{S_{1}+S_{2}+S_{3}+S_{4}+S_{5}} \rho \bar{V}\cdot \bar{n}dS = 0 
$$

at $S_{3}, S_{4},S_{5}$ the integral is zero. 

$$
\begin{align}
\int_{S_{1} + S_{2}} \rho \bar{V} \cdot \bar{n}dS = 0 \\
-\rho_{1}u_{1}H_{1} + \rho_{2} u_{2}H_{2} = 0 \\
\boxed{\rho_{1}u_{1}=\rho_{2}u_{2}}
\end{align}
$$

$$
\int_{S_{1}+S_{2}+S_{3}+S_{4}+S_{5}} \rho \bar{V}(\bar{V}\cdot \bar{n})dS = -\int_{S_{1}+S_{2}+S_{3}+S_{4}+S_{5}} P\bar{n}dS + \int_{S_{1}+S_{2}+S_{3}+S_{4}+S_{5}} \bar{\bar{\tau}}\cdot \bar{n}dS
$$

For the first integral, $S_{3},S_{4},S_{5}$ will be zero.
For the Pressure integral, $S_{3}$ and $S_{4}$ will cancel out do symmetry assumption.
For the shear integral $S_{1}$ and $S_{2}$ will cancel do to being zero.

$$
\int_{S_{1}+S_{2}} \rho \bar{V}(\bar{V}\cdot \bar{n})dS = -\int_{S_{1}+S_{2}+S_{5}} P\bar{n}dS + \int_{S_{1}+S_{2}+S_{3}+S_{4}+S_{5}} \bar{\bar{\tau}}\cdot \bar{n}dS
$$