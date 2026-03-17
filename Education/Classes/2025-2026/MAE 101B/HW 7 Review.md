
## H7.1

An aircraft flies at $Ma$ = 1.5 at an altitude of 3 km in standard atmosphere. Estimate the time [s] after the aircraft flies directly above a ground observer that the sound of the aircraft is heard by the observer?

### My attempt:

$$
Ma = \frac{v}{c},\quad c=\sqrt{ kRT },\quad \sin(\alpha) = \frac{c}{v} = \frac{1}{Ma}
$$
Standard atmosphere: $k = 1.4$, $R=286.9\mathrm{J/kg\cdot K},$ 

Temperature at 3km: $T= -4.49\mathrm{ \degree C} + 273.15 = 268.66\mathrm{K}$ 

$$
\begin{gather}
Ma = \frac{v}{c} = \frac{v}{\sqrt{ kRT }} \Rightarrow v = Ma\sqrt{ kRT } \\
 \\
dv =\frac{dx}{dt}\quad \therefore v = \frac{x}{t} \\
 \\
Ma\sqrt{ kRT } = \frac{x}{t} \Rightarrow t = \frac{x}{Ma\sqrt{ kRT }}  \\
x =\cos(\alpha) = \cos\left( \arcsin\left( \frac{1}{Ma} \right) \right) \\
 \\
t = \frac{\cos\left( \arcsin\left( \frac{1}{Ma} \right) \right)}{Ma\sqrt{ kRT }} \\
 \\
t = \frac{\cos\left( \arcsin\left( \frac{1}{1.5} \right) \right)}{(1.5)\sqrt{ (1.4)(286.9)(268.66) }} = 0.0015126612832645 
\end{gather}
$$