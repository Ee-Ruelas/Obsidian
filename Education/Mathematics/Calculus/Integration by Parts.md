Also known as, IBP, is a method used to solve for many different integration problems, often in the form of $\int f(x)g(x)dx$.

The method uses the following equation:
$$
\int udv=uv-\int vdu
$$
*There is also a spanish saying to remember this: "Un Dia Vi Una Vaca Vestida De Uniforme"

Special problems and Examples:

1. $f(x) = \sin{(x)}$, $g(x) = x$ 
Solution
$$
\begin{align*}
\int f(x) g(x) dx =& \int \sin{(x)}xdx \Rightarrow 
\overset{\text{The one that can goe away is oftern,u} }{
\begin{matrix}
u = x\\
dv = \sin{(x)}
\end{matrix}
}\\
\begin{matrix}
du = 1\\
v = -\cos{(x)}
\end{matrix}
\Bigl\} 
= & \int udv = uv - \int vdu = -x\cos{(x)} - \int -\cos{(x)}1dx= -x\cos{(x)} + \int \cos{(x)}dx
\\
=& \boxed{-x\cos{(x)}+\sin{(x)} + C}
\end{align*}
$$
2. $f(x) = \sin{(x)}, g(x) = e^x$
$$
\begin{align*}
\int f(x) g(x) dx &= \int \sin{(x)}e^x dx\Rightarrow
\begin{matrix}
u = \sin{(x)}\\
dv = e^x
\end{matrix}
\Bigl\}
\quad
\begin{matrix}
du = \cos{(x)}\\
v = e^x
\end{matrix}\\
&= \sin{(x)}e^x  - \int e^x\cos{(x)}dx\\
&\text{Now we repeat for the new integral}\\
&=
\begin{matrix}
u = \cos{(x)}\\
dv = e^x
\end{matrix}
\Bigl\}
\begin{matrix}
du = -\sin{(x)}\\
v = e^x
\end{matrix}
\\
&= \cos{(x)}e^x + \underset{\text{Original Equation}}{\int e^x \sin{(x)}dx}\\
\int \sin{(x)}e^xdx &= \sin{(x)}e^x - \cos{(x)}e^x - \int \sin{(x)}e^xdx\\
\end{align*}
$$
This is a special integral that requires this special method to solve it, and often happens to periodic functions, and natural exponential functions.
$$
\begin{align*}
\int \sin{(x)}e^xdx = \sin{(x)}e^x - \cos{(x)}e^x - \int \sin{(x)}e^xdx\\
2\int \sin{(x)}e^xdx =\sin{(x)}e^x - \cos{(x)}e^x \\
\int \sin{(x)}e^xdx = \boxed{\frac{\sin{(x)}e^x - \cos{(x)}e^x}{2}}
\end{align*}
$$


As seen in the last example many integrals have to be integrated by parts multiple times and that can be time consuming, in that case we often use the Tabular Method.