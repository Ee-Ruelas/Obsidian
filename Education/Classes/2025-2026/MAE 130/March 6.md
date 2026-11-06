
## Reminder 
Do the SET's

## Review
$$
\text{Impulse: }\quad 
$$

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Education/Classes/MAE 130/Ink/Drawing/2026.3.6 - 15.09pm.drawing",
	"width": 354,
	"aspectRatio": 1.0504451038575668
}
```
$$
\begin{align}
u_{i}(t_{i}) = \frac{f(t_{i})}{m\omega_{d}}e^{-\zeta \omega_{0}(t-t_{i})}\sin[\omega_{d}(t-t_{i})]\Delta t \\
u(t)= \sum_{i=1}^{n}u_{i}(t) = \sum_{i=1}^{n}f(\tau_{i})h(t-\tau_{i})\Delta \tau=\lim_{ \Delta \tau \to 0 } \sum_{i=1}^{n}f(\tau_{i})h(t-\tau_{i})\Delta t= \\ \\
\boxed {\int_{0}^{t}f(\tau)h(t-\tau)d\tau\quad \text{Duhamel integral (convolution integral)}}
\end{align}
$$

## Example 1


```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Education/Classes/MAE 130/Ink/Drawing/2026.3.6 - 15.20pm.drawing",
	"width": 434,
	"aspectRatio": 0.8839103869653768
}
```
$$
\begin{align} \\
\text{placed instantenously}\quad m =1,\quad k=4,\quad c =1 \\
f(t) = mg = W \\ 
\omega_{0}^{2}=\frac{k}{m}=4\quad \omega_{0} = 2 \\
\zeta = \frac{c}{2\sqrt{ km }}=\frac{1}{4} \\
\omega_{d} = \omega_{0}\sqrt{ 1-\zeta^{2} }=\frac{\sqrt{ 15 }}{2} \\
u(t) = \int_{0}^{t} f(\tau)h(t-\tau)d\tau = \frac{W}{m \omega_{d}} \int_{0}^{t} e^{-\zeta \omega_{0}(t-\tau)}\sin[\omega_{d}(t-\tau)]d\tau \\
=\frac{\omega_{d}e^{-\zeta \omega_{0}t}[\omega_{d}\cos(\omega_{d}t)+\zeta \omega_{0}\sin(\omega_{d}t)]}{\omega_{d}^{2}+(\zeta \omega_{0})^{2}}
\end{align}
$$

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Education/Classes/MAE 130/Ink/Drawing/2026.3.6 - 15.29pm.drawing",
	"width": 500,
	"aspectRatio": 1
}
```

## Example 2



```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Education/Classes/MAE 130/Ink/Drawing/2026.3.6 - 15.19pm.drawing",
	"width": 500,
	"aspectRatio": 1
}
```
$$
\begin{align}
\text{Placed instantaneously on the larger mass, then removed after }t = t_{0} \\  \\
f(t) = mg(H(t)-H(t-t_{0}))  \\
\omega_{0}^{2}=\frac{k}{m}=4\quad \omega_{0} = 2 \\
\zeta = \frac{c}{2\sqrt{ km }}=\frac{1}{4} \\
\omega_{d} = \omega_{0}\sqrt{ 1-\zeta^{2} }=\frac{\sqrt{ 15 }}{2} \\
u(t) = \int_{0}^{t} f(\tau)h(t-\tau)d\tau = W\int_{0}^{t}[H(t)-H(t-t_{0})]h(t-\tau)d\tau\quad \\
 \text{or} \\
\quad \begin{cases}
t \leq t_{0} : W\int_{0}^{t}h(t-\tau)d\tau \\
t\geq t_{0}:W\left[ \int_{0}^{t_{0}}h(t-t_{0})d\tau-\int_{t_{0}}^{t}h(t-\tau)d\tau \right]
\end{cases}
\end{align}
$$

## Example 3

Harmonic Forcing 



```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Education/Classes/MAE 130/Ink/Drawing/2026.3.6 - 15.19pm.drawing",
	"width": 500,
	"aspectRatio": 1
}
```
$$
\begin{align}
f(t) = F\cos(\omega t) \\
u(t) = \int_{0}^{t}f(\tau)h(t-\tau)d\tau = \frac{F}{m\omega_{0}} \int_{0}^{t}\cos(\omega \tau)\sin(\omega_{0}(t-\tau))d\tau=\frac{F}{k-\omega^{2}m}[\cos(\omega t)-\cos(\omega_{0}t)] \\
\omega < \omega_{0} 
\end{align}
<!--ID: 1773723550756-->


$$

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Education/Classes/MAE 130/Ink/Drawing/2026.3.6 - 15.47pm.drawing",
	"width": 500,
	"aspectRatio": 1
}
```
