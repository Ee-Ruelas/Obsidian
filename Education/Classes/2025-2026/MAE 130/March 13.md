
```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Education/Classes/2025-2026/MAE 130/Ink/Drawing/2026.3.13 - 15.06pm.drawing",
	"width": 500,
	"aspectRatio": 1
}
```
$$
\begin{align}
\frac{ \partial u^{2} }{ \partial t^{2} } -C_{0}^{2}\frac{ \partial u^{2} }{ \partial x^{2} } =0 \leftarrow u(x,t) = P(x)Q(t) \\
P(x)=A\cos(kx) + B\cos(kx)\quad Q(t) = C\cos(\omega t)+D\sin(\omega t) \\ 
P(0) = A = 0\quad P(l) = B\sin(kl) k_{n}l=n\pi\quad n = 0,1,2,3 \\
k_{n}l = \frac{\omega_{n}l}{C_{0}} = n\pi\quad \omega_{n} = \frac{nC_{0}\pi}{l} \\
u_{n}(x,t) = \sin(k_{n}x)\left[ \tilde{C}_{n}\cos\left( \frac{nc\pi t}{l} \right) + \tilde{D}_{n}\sin \left( \frac{nC_{0}\pi t}{l} \right) \right] \\
\tilde{C}_{n} = \frac{2}{l}\int_{0}^{l}u_{0}(x)\sin(k_{n}x)dx\quad \tilde{D}_{n} = \left( \frac{1}{\omega_{n}} \right)\left( \frac{2}{l} \right)\int_{0}^{l}\dot{u}_{0}(x)\sin(k_{n}x)dx \\
\tilde{C}_{n} = \frac{32h}{n^{2}\pi^{2}}\cos\left( \frac{n\pi}{4} \right)\sin\left( \frac{n\pi}{4} \right)^{3}\quad C_{n}\neq 0\quad for\quad  n=1,3,5,\dots \\
 \\
\end{align}
$$
$$
\begin{align}
n= 1,3,5:  \\
u_{n}(x,t) = \frac{8h}{\pi ^{2}}\left[ \sin\left( \frac{\pi x}{l} \right) \cos\left( \frac{C_{0}\pi t}{l} \right) -\frac{1}{9}\sin\left( \frac{3\pi x}{l} \right)\cos\left( \frac{3C_{0}\pi t}{l} \right)+\frac{1}{25}\sin\left( \frac{5\pi x}{l} \right)\cos\left( \frac{5C_{0}\pi t}{l} \right)\right]
\end{align}
$$