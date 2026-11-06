

![[Pasted image 20260410081133.png]]

$$
\frac{d}{dt} \int_{CV} \rho dV + \int_{S_{1}+S_{2}+S_{3}+S_{4}+S_{5}}\rho \bar{v}\cdot \bar{n}dS = 0
$$
$S_{3}, S_{4}, S_{5}$ are canceled for reasons mentioned last lecture.

$$
\int_{S_{1}+S_{2}} \rho \bar{v}\cdot \bar{n}dS = -\rho_{1}u_{1}H + \rho_{2}u_{2}H = \rho_{1}u_{1}=\rho_{2}u_{2}
$$

Then we do the same with momentum equations:

$$
\int_{S_{1} + S_{2}} \rho \bar{v} (\bar{v}\cdot \bar{n})dS = -\int_{S_{1}+S_{2}}P\bar{n}dS + \int_{S_{5}} \bar{\bar{\tau}}\cdot \bar{n}dS
$$
Check last lecture to see why the bounds are this way.

$$
-\rho_{1}(u_{1},0)u_{1}H + \rho_{2}(u_{2},v_{2})u_{2}H = P_{1}(1,0)H - P_{2}(1,0)H -\int_{S_{5}}P\bar{n}dS + \int_{S_{5}}\bar{\bar{\tau}}\cdot \bar{n}dS
$$
How would you compute the $L'$ and $D'$?
![[Pasted image 20260417003749.png]]

$$
\bar{F}_{F\rightarrow A} = -\int_{S_{A}}P\bar{n}dS + \int_{S_{A}}\bar{\bar{\tau}}\cdot \bar{n}dS
$$
$$
\bar{F}_{F\rightarrow A} = (D',L')
$$
Now go back

$$
-\rho_{1}(u_{1},0)u_{1}H + \rho_{2}(u_{2},v_{2})u_{2}H = P_{1}(1,0)H - P_{2}(1,0)H -\underset{-\bar{F}_{F\rightarrow A} = -(D',L')}{\int_{S_{5}}P\bar{n}dS + \int_{S_{5}}\bar{\bar{\tau}}\cdot \bar{n}dS}
$$
$$
\boxed{D'=(P_{1}+\rho_{1}u_{1}^2)H-(P_{2}+\rho_{2}u_{2}^2)H}
$$
$$
\boxed{L'=-\rho_{2}u_{2}v_{2}H - \rho_{1}u_{1}v_{2}H}
$$
Energy Equation

$$
\frac{d}{dt} \left[ \int_{CV}\rho\left( e+\frac{\bar{v}^2}{2}dV \right) \right] + \int_{CS}\rho\left( e+\frac{\bar{v}^2}{2} \right)\bar{v}\cdot \bar{n}dS = -\int_{CS}P\bar{v}\cdot \bar{n}dS + \int_{CS}\bar{v}\cdot \bar{\bar{\tau}}\cdot \bar{n}dS + \int _{CS} K\nabla T\cdot\bar{n}dS
$$
You can replace the $\frac{d}{dt}$ to zero. and the CS, with $S_{1}+S_{2}+S_{3}+S_{4}+S_{5}$.
For the first CS, $S_{3}$-$S_{5}$ cancel
For the second CS, $S_{3}$-$S_{5}$ cancel
For the third CS, All surfaces either cancel or are zero, $\therefore$ the integral cancels out
For the fourth CS, $S_{1}$-$S_{4}$ cancel out due to uniform temperature
If we assume that airfoils are thermally insulated then
$\nabla T\cdot \bar{n}=0$ so $S_{5}$ also cancels

$$
\int_{S_{1}+S_{2}}\rho\left( e+\frac{\bar{v}^2}{2} \right)\bar{v}\cdot \bar{n}dS = -\int_{S_{1}+S_{2}}P\bar{v}\cdot \bar{n}dS
$$
remainder: $\bar{v}^2=\bar{v}\cdot \bar{v}=|\bar{v}|^2$ in other words $\bar{v}^2$ is not a vector
$$
-\rho_{1}u_{1}\left( e_{1}+\frac{u_{1}^2}{2} \right)H + \rho_{2}u_{2}\left( e_{2}+\frac{u_{2}^2+v_{2}^2}{2} \right)H=P_{1}u_{1}H-P_{2}u_{2}H
$$

$$
\rho_{1}u_{1}\left( e_{1}+\frac{v_{1}^2}{2}+\frac{P_{1}}{\rho_{1}} \right) = \rho_{2}u_{2}\left( e_{2}+\frac{u_{2}^2+v_{2}^2}{2}+ \frac{P_{2}}{\rho_{2}} \right)
$$
$$
\boxed{h_{1} + \frac{u_{1}^2}{2} = h_{2}+ \frac{u_{2}^2+v_{2}^2}{2}}
$$
$h_{1} = \frac{\gamma}{\gamma-1} \frac{P_{1}}{\rho_{1}}$
