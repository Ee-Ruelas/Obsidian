
# One-Dimensional Flow of a Perfect Gas

- Develop equations for perfect gas flowing in channels
- **For convenience** assume heat capacity, ${}c_{p}{}$ and ${}c_{v}{}$ are constant.
- Flow is one-dimensional, due to approximation that fluid only changes when moving in the ${}x{}$-direction: ${}v(x), \rho(x), {}$etc. 
- Diffusive effects are ignored. Thus, flow is immediately affected by a local application of wall shear stress or heat transfer.
- One-dimensional flow model nozzles, diffusers, and combustors.


# Compressibility 

Consider an ideal gas, ${}p=\rho RT{}$, in general 

$$
\delta \rho=\left( \frac{\partial \rho}{\partial T} \right)_{p}\delta T+ \left( \frac{\partial \rho }{\partial p} \right)_{T}\delta p
\tag{1}
$$
For isentropic law of an ideal gas, ${}\rho=Cp^{1/\gamma}{}$. Thus, 
$$
\left( \frac{\partial \rho}{\partial p} \right)_{T}=\frac{\rho}{p};  \quad \left( \frac{\partial \rho}{\partial p} \right)_{s}=\frac{\rho}{\gamma p}; \quad \left( \frac{\partial \rho}{\partial p} \right)_{T}=\gamma\left( \frac{\partial \rho}{\partial p} \right)_{s}=\gamma/a^{2}
$$
where ${}a{}$ is the speed of sound.

If we expand the density as a [[Taylor Series]] about some reference temperature ${}T_{\text{ref}}{}$ and some reference pressure, ${}p_{\text{ref}}{}$, 
$$
\rho=\rho_{\text{ref}}+\left[ \left( \frac{\partial \rho}{\partial T} \right)_{p} \right]_{\text{ref}} (T-T_{\text{ref}})+ \left[ \left( \frac{\partial\rho}{\partial p} \right)_{T} \right]_{\text{ref}} (p-p_{\text{ref}}) \tag{2}
$$
it follows that 

$$
\frac{\rho}{\rho_{\text{ref}}}=1+\frac{T_{\text{ref}}}{\rho_{\text{ref}}}\left[ \left( \frac{\partial \rho}{\partial T} \right)_{p} \right]_{\text{ref}} \frac{T-T_{\text{ref}}}{T_{\text{ref}}}+\frac{\gamma}{a^{2}} \frac{p-p_{\text{ref}}}{\rho_{\text{ref}}}

$$
Definitions

$$
\rho ^{\star}=\frac{\rho}{\rho_{\text{ref}}},
\quad \theta = (T-T_{\text{ref}})/T_{\text{ref}},
\quad p^{\star}=(p-p_{\text{ref}})/(\rho_{\text{ref}}U_{\infty}^{2})
$$
obtain
$$
\rho ^{\star}=1+\left( \frac{\partial \ln \rho}{\partial \ln T} \right)_{p,\text{ref}} \theta + \gamma M^{2}p^{\star} \tag{3}

$$
Here ${}M = U_{\infty}/a{}$ is the Mach number. Notice that incompressible flow ${}M\ll 1 {}$. For low-speed flow changes in density with changes in pressure can be neglected. 

# Flow of a Perfect Gas

The equation of state for a perfect gas is ${}p=\rho RT{}$, where ${}R= R^{0}/W{}$, and ${}R^{0}{}$ is the universal gas constant, and ${}W{}$ the molecular weight. 
Thus, 

$$
\begin{gather}
\ln p=\ln(\rho RT) = \ln \rho + \ln R +\ln T \\
\Rightarrow \frac{\delta \ln x}{\delta x}= \frac{1}{x} \\
\Rightarrow \delta \ln x = \frac{\delta x}{x} \\
\delta [\ln p = \ln \rho \ln R \ln T] \\
\frac{\delta p}{p}=\frac{\delta \rho}{\rho} + \frac{\delta R}{R} + \frac{\delta T}{T} \\
\Rightarrow \delta R = 0 \\
\vdots \\
\boxed{\delta p/p - \delta \rho/\rho - \delta T/T = 0 }
\end{gather}
$$

By definition ${}c_{p}=\left( \frac{\partial h}{\partial T} \right)_{p}{}$, where ${}h{}$ is the enthalpy per unit mass. For perfect gas, ${}h{}$ is only a function of ${}T{}$ hence ${}c_{p}=dh/dT{}$. Hence 
$$
\boxed{\delta h = c_{p}\delta T}
$$
From the first and second law of thermodynamics ${}T\delta s = \delta h - \delta p/\rho{}$, hence ${}\delta s / R = (c_{p} /R)\delta T /T - \delta p /(\rho RT){}$. Because ${}c_{p} - c_{v} = R{}$, and ${}\gamma = c_{p}/c_{v}{}$, ${}c_{p}/R=\gamma /(\gamma-1){}$. Hence 
$$
\begin{gather} 
T \delta s = \delta h - \frac{\delta p}{\rho} \\
\frac{1}{RT}\left[ T\delta s =  \delta h - \frac{\delta p}{\rho} \right] \\
\frac{\delta s}{R} = \frac{\delta h}{RT} - \frac{\delta p}{\rho RT} \\
\frac{\delta s}{R} = \frac{c_{p}\delta T}{RT}-\frac{\delta p}{p} \\
c_{p}-c_{v}=R \quad \text{and} \quad \gamma=c_{p} / c_{v}  \\
\frac{c_{p}}{R} = \frac{\gamma}{(\gamma-1)} \\
\frac{\delta s}{R} = \frac{\gamma}{(\gamma-1)} \frac{\delta T}{T} - \frac{\delta p}{p}
\end{gather}\\ \\ 
\boxed{\frac{\delta s}{R}=\frac{\gamma}{\gamma-1} \frac{\delta T}{T}-\frac{\delta p}{p}}

$$

# One-Dimensional Flow: Mass Conservation 

![[MAE - 113 - Compressible Flow-1793222971986.webp]]Figure: One-dimensional flow through a control volume

Consider one-dimensional differential control volume within a duct. The rates of heat and work (shaft) transfer to the control volume are ${}\dot{Q}{}$ and ${}\mathcal{P}_{s}{}$, respectively. A body force of magnitude ${}X{}$ per unit volume of fluid is presumed to act in the stream direction. The flow in the duct is presumed to be steady, and the cross-section area, ${}A(x){}$ is presumed to be a function of ${}x{}$.
The mass conservation equation is ${}\int_{cs}\rho \vec{u}\cdot \vec{n}dA=0{}$. For one-dimensional flow ${}d(\rho uA)/ dx = o.{}$Hence, the mass-flow rate, ${}\dot{m}=\rho uA= \text{constant}{}$ and 
$$
\begin{gather}
\dot{m} = \rho uA \\
\ln \dot{m} =\ln(\rho uA) \\
\ln \dot{m} = \ln \rho + \ln u + \ln A \\
\frac{\delta \dot{m}}{\dot{m}} = \frac{\delta \rho}{\rho} + \frac{\delta u}{u}+\frac{\delta A}{A} \\
\text{Since \(\dot{m}\) is a const.}\to \delta \dot{m}=0 \\
\boxed{\delta \rho / \rho + \delta u /  u + \delta A / A = 0}
\end{gather}
$$
The equation of motion is ${}\sum \vec{F}=\int_{cs}\rho \vec{u}(\vec{u}\cdot \vec{n})dA{}$, where ${}\sum \vec{F}{}$ is the sum of pressure, wall shear, and body forces. Hence
$$
\boxed{-(A\delta p + \tau_{0}c\delta x) + XA\delta x = \rho uA\delta u}
$$
where ${}\tau_{0}{}$ is the wall shear per unit area and ${}X{}$ the body force per unit volume. In the differential form
$$
-(dp / dx + \tau_{0}c / A)+X = \rho u(du / dx)

$$
neglecting the body forces
$$
\frac{\delta p}{p}+\frac{\rho u^{2}}{p} \frac{\delta u}{u} = -\frac{\tau_{0}c}{Ap}\delta x
$$
Also
$$
\frac{\rho u^{2}}{p} = \frac{\rho u^{2}}{\rho RT} = \frac{\gamma u^{2}}{\gamma RT} = \gamma M^{2}
$$
where ${}\gamma = c_{p}/cv{}$ and the Mach number ${}M = u / \sqrt{ \gamma RT }{}$. Hence the equation of motion is 
$$
\boxed{\frac{\delta p}{p}+\gamma M^{2} \frac{\delta u}{u} = - \frac{\tau_{0}c}{Ap}\delta x}
$$
The energy-conservation equation is
$$
\int_{\text{cs}}\rho(h+u^{2}/2)(\vec{u}\cdot \vec{n})dA = \int_{\text{cs}}\vec{q}\cdot \vec{n}dA_{\text{cs}} + \int_{\text{cv}}\vec{X}\cdot \vec{u} + \mathcal{P}_{s}
$$
Here, ${}h{}$ and ${}u^{2} / 2{}$ are the enthalpy and kinetic energy per unit mass, ${}\vec{q}{}$ the heat flux vector   (${}\mathrm{{W/m^{2}}}{}$), ${}A_{\text{cs}}{}$ indicates the entire control-surface are (as opposed to the area ${}A{}$ of the duct cross section), and ${}\mathcal{P}_{s}{}$ the shaft work, positive for work done on the system by the surroundings. 

For one-dimensional flow neglecting body forces, the energy equation is 
$$
\dot{m}(\delta h+u\delta u)=\delta \dot{q}+\delta \mathcal{P}_{s}

$$
Hence
$$
\boxed{\delta h+u\delta u=\delta q+\delta w_{s}}

$$
Here ${}q{}$ is the heat added of the system per unit mass and ${}w_{s}{}$ the shaft work done on the system. This equation can be written as ${}(c_{p} /R)\delta T /T + [\gamma u^{2} /(\gamma RT)]\delta u /u = (\delta q + \delta w_{s}) / (RT){}$. Hence
$$
\frac{1}{\gamma-1} \frac{\delta T}{T} + M^{2} \frac{\delta u}{u}=\frac{\delta q + \delta w_{s}}{\gamma RT} = \frac{\delta q + \delta w_{s}}{a^{2}}\
$$
where the speed of sound ${}a=\sqrt{ \gamma RT }{}$.

## Summary of Equations: One-Dimensional Flow

Equation of State
$$
\frac{\delta p}{p}-\frac{\delta \rho}{\rho}-\frac{\delta T}{T}=0 \tag{1}

$$
First and Second Law of Thermodynamics
$$
\frac{\delta s}{R}=\frac{\gamma}{\gamma-1} \frac{\delta T}{T} - \frac{\delta p}{p}\tag{2}

$$
Conservation of Mass
$$
\frac{\delta \rho}{\rho}+\frac{\delta u}{u}+\frac{\delta A}{A}=0
\tag{3}
$$
Equation of Motion
$$
\frac{\delta p}{p}+\gamma M^{2} \frac{\delta u}{u}=- \frac{\tau_{0}c}{Ap}\delta x\tag{4}
$$
Conservation of Energy
$$
\frac{1}{\gamma-1} \frac{\delta T}{T}+M^{2} \frac{\delta u}{u}= \frac{\delta q + \delta w_{s}}{a^{2}}
\tag{5}
$$

It follows from 2, 4, and 5.
$$
\frac{\delta s}{R}=\frac{\delta q + \delta w_{s}}{RT}+\frac{\tau_{0}c}{Ap}\delta x
$$
Hence entropy is increased if heat is added to the system, shaft work is done on the system and wall shear. Moreover from the definition ${}M^{2}=u^{2} /(\gamma RT){}$, it follows that 
$$
2 \frac{\delta M}{M} = 2 \frac{\delta u}{u}- \frac{\delta T}{T}

$$

# Stagnation State

The stagnation state is defined as the state that would be reached by a fluid if it were brought to rest *reversibly, adiabatically, and without work*.

The energy conservation equation is ${}\delta h+ u \delta u = 0{}$. Integration gives ${}h+u^{2} /2 = h_{0}{}$, where ${}h_{0}{}$ is the stagnation enthalpy.

Hence
$$
\frac{T_{0}}{T} = 1 + \frac{\gamma-1}{2}M^{2}

$$
For an isentropic process of a perfect gas with constant ${}c_{p}{}$, ${}p_{0} /p = (T_{0} /T)^{\gamma/(\gamma-1)}{}$, where ${}p_{0}{}$ is the stagnation pressure. Hence 
$$
\frac{p_{0}}{p} = \left[ 1 + \frac{\gamma-1}{2}M^{2} \right]^{\gamma / (\gamma-1)}; \quad \frac{\rho_{0}}{\rho} = \left[ 1+ \frac{(\gamma-1)}{2}M^{2} \right]^{1/(\gamma-1)};
$$
where ${}\rho_{0}{}$ is the density at stagnation.

![[MAE - 113 - Compressible Flow-1793332991118.webp|379]]                                   Figure: Definition of Stagnation State

For any adiabatic flow in which no work occurs, the stagnation enthalpy is constant for both reversible and irreversible flows. Hence the stagnation temperature remains the same.

The stagnation pressure reached when there is adiabatic zero-work deceleration of fluid is decreased by irreversible processes. 

The stagnation state at 1 where the temperature is ${}T_{1} {}$ and pressure is ${}p_{1}{}$, is the temperature ${}T_{01}{}$, and pressure ${}p_{01}{}$. 

If an adiabatic process with no work proceeds form temperature ${}T_{1}{}$ to ${}T_{2}{}$ and pressure ${}p_{1}{}$ to pressure ${}p_{2}{}$ reversibly and the stagnation temperature ${}T_{02}=T_{01}{}$, and the stagnation pressure ${}p_{02}=p_{01}{}$. 

If the adiabatic process with no work form 1 to 2 is irreversible than the stagnation temperature ${}T_{02} = T_{01}{}$, but the stagnation pressure ${}p_{02}<p_{01}{}$

Consider an adiabatic, irreversible process with no work from state 1 where the pressure is ${}p_{1},{}$ temperature, ${}T_{1}{}$, and entropy, ${}s_{1}{}$ to state 2 where the pressure is ${}p_{2}{}$, temperature, ${}T_{2}{}$, and entropy ${}s_{2}{}$.
$$
\begin{align}
 & \frac{s_{2}-s_{1}}{R} = \ln\left( \frac{T_{2}}{T_{1}} \right)^{\gamma/(\gamma-1)}-\ln\left( \frac{p_{2}}{p_{1}} \right)\\
 & =\ln\left[ \frac{T_{2}}{T_{02}} \frac{T_{01}}{T_{1}} \frac{T_{02}}{T_{01}} \right]^{\gamma/(\gamma-1)}-\ln\left( \frac{p_{2}}{p_{02}} \frac{p_{01}}{p_{1}} \frac{p_{02}}{p_{01}} \right)
\end{align}

$$
By definition ${}(T_{01} /T_{1})^{\gamma/(\gamma-1)}=p_{01}/p_{1}{}$, and ${}(T_{02} /T_{2})^{\gamma/(\gamma-1)}=p_{02} /p_{2}{}$. 
$$
\frac{s_{2}-s_{1}}{R}=\ln\left( \frac{T_{02}}{T_{01}} \right)^{\gamma/(\gamma-1)}-\ln\left( \frac{p_{02}}{p_{01}} \right)= - \ln\left( \frac{p_{02}}{p_{2}} \right),

$$
for ${}T_{02}=T_{01}{}$, because the process is adiabatic. Hence for an irreversible adiabatic process with no work, the stagnation pressure must decrease, or ${}p_{02}<p_{01}{}$ for ${}s_{2}-s_{1}>0{}$. Therefore the decrease in stagnation pressure is a measure of the irreversibility of the process. 

By definition ${}(T_{0} / T)^{\gamma/(\gamma-1)}=p_{0} /p{}$. Hence, 
$$
\frac{\gamma}{\gamma-1}\ln(T_{0})-\frac{\gamma}{\gamma-1}\ln(T)=\ln(p_{0})-\ln(p)

$$
Hence
$$
\frac{\delta s}{R}=\frac{\gamma}{\gamma-1} \frac{\delta T}{T}- \frac{\delta p}{p} = \frac{\gamma}{\gamma-1} \frac{\delta T_{0}}{T_{0}}- \frac{\delta p_{0}}{p_{0}}

$$
# Isentropic Flow in a Convergent Divergent Nozzle

Consider, one-dimensional, isentropic flow of a perfect gas in the absence of work and body forces in convergent channels ${}dA/dx<0{}$, divergent channels ${}dA /dx >0{}$ and convergent divergent channels. Here ${}A(x){}$ is the cross-sectional area of the channel. Many actual processes in nozzles and diffusers are nearly isentropic. 

For such flow the stagnation temperature, ${}T_{0}{}$, and stagnation pressure, ${}p_{0}{}$ are constant.

The mass flow rate is ${}\dot{m}=\rho uA{}$. In view of the ideal gas equation of state, ${}p=\rho RT{}$ and the definition ${}u=Ma=M\sqrt{ \gamma RT }{}$, it follows that
$$
\frac{\dot{m}}{A} = \frac{p_{0}\sqrt{ \gamma }}{\sqrt{ RT_{0} }}M\left[ \left( \frac{p}{p_{0}} \right)\left( \frac{T_{0}}{T} \right)^{1/2} \right]
$$
Because ${}T_{0} /T  = 1+M^{2}(\gamma-1) /2{}$ and ${}p_{0}/p=(T_{0} /T)^{\gamma/(\gamma-1)}{}$, it follows that 
$$
\boxed{\frac{\dot{m}}{A}=\frac{p_{0}\sqrt{ \gamma }}{\sqrt{ RT_{0} }}M\left( 1+ \frac{\gamma-1}{2}M^{2} \right)^{-(\gamma+1)/[2(\gamma-1)]}}

$$

Starting from the mass conservation equation and using the equation of state, first and second law of thermodynamics, obtain
$$
-\frac{\delta A}{A}=\frac{\delta \rho}{\rho}+\frac{\delta u}{u}=\frac{\delta p}{p}-\frac{\delta T}{T}+\frac{\delta u}{u}=\frac{\frac{\gamma}{\gamma-1}\delta T}{T}-\frac{\delta T}{T}+\frac{\delta u}{u}=\frac{1}{\gamma-1} \frac{\delta T}{T} + \frac{\delta u}{u}
$$
Using the energy conservation equation followed by the first and second law of thermodynamics, obtain
$$
\boxed{-\frac{\delta A}{A}=(1-M^{2}) \frac{\delta u}{u}= -\frac{1-M^{2}}{M^{2}(\gamma-1)} \frac{\delta T}{T}=- \frac{1-M^{2}}{\gamma M^{2}} \frac{\delta p}{p}}

$$
Becuase, ${}2\delta M /M = 2\delta u /u - \delta T /T{}$, it follows that 
$$
\boxed{-\frac{\delta A}{A} = \frac{2(1-M^{2})}{2+M^{2}(\gamma-1)} \frac{\delta M}{M}}
$$

## Isentropic Flow in a Convergent Nozzle, ${}\delta A /A < 0 {}$
$$
\begin{gather}
\boxed{-\frac{\delta A}{A}=(1-M^{2}) \frac{\delta u}{u} = - \frac{1-M^{2}}{M^{2}(\gamma-1)} \frac{\delta T}{T} = - \frac{1-M^{2}}{\gamma M^{2}} \frac{\delta p}{p}} \\
\boxed{\frac{\delta A}{A}=-(1-M^{2}) \frac{\delta u}{u}= \frac{1-M^{2}}{M^{2}(\gamma-1)} \frac{\delta T}{T} = \frac{1-M^{2}}{\gamma M^{2}} \frac{\delta p}{p}}
\end{gather}
$$
- With decreasing ${}A{}$
	- Subsonic flow ${}M<1{}$, ${}M{}$ and ${}u{}$ increase, ${}T{}$ and ${}p{}$ decrease.
	- Supersonic flow ${}M>1{}$, ${}M{}$ and ${}u{}$ decrease, ${}T{}$ and ${}p{}$ increase.
	 
- With increasing A
	- Subsonic flow ${}M<1{}$, ${}M{}$ and ${}u{}$ decrease, ${}T {}$ and ${}p{}$ increase.
	- Supersonic flow ${}M>1{}$, ${}M{}$ and u increase, ${}T {}$ and ${}p{}$ decrease.

## Continue...

The mass flow rate per unit are
$$
\frac{\dot{m}}{A} = \frac{p_{0}\sqrt{ \gamma }}{\sqrt{ RT_{0} }}M\left( 1+ \frac{\gamma-1}{2}M^{2} \right)^{-(\gamma+1)/[2(\gamma-1)]}

$$
For a given fluid ${}(\gamma,R){}$ and inlet state ${}(p_{0},T_{0}){}$ it can be shown that the mass flow per unit area is maximum at ${}M=1{}$. Using an asterisk to indicate those properties at ${}M=1{}$ obtain
$$
\frac{\dot{m}}{A^{*}} = \frac{p_{0}\sqrt{ \gamma }}{RT_{0}}\left( \frac{2}{\gamma+1} \right)^{(\gamma+1)/[2(\gamma-1)]}

$$
Hence
$$
\frac{A}{A^{*}} = \frac{1}{M}\left[ \left( \frac{2}{\gamma+1} \right)\left( 1+\frac{\gamma-1}{2}M^{2} \right) \right]^{(\gamma+1)/[2(\gamma-1)]}

$$
Also representing the pressure and temperature at ${}M=1 {}$ by ${}p^{*}{}$ and ${}T^{*}{}$ respectively, obtain for ${}\gamma=1.4{}$
$$
\frac{p^{*}}{p_{0}} = \left( \frac{2}{1+\gamma} \right)^{\gamma/(\gamma-1)} = 0.528,\quad
\frac{T^{*}}{T_{0}}=\frac{2}{1+\gamma}=0.833
$$
![[MAE - 113 - Compressible Flow-1793344011114.webp|298]]              Figure: One-dimensional isentropic flow of a perfect gas. (From Shapiro)


![[MAE - 113 - Compressible Flow-1793344078195.webp]]

![[MAE - 113 - Compressible Flow-1793344128149.webp|407]]
