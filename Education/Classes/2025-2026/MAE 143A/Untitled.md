

## The discrete Fourier transform (DFT)

The discrete Fourier transform (DFT) of order $N_{0}$ is

$$

\begin{align}
X[k] = \sum_{n=0}^{N_{0}-1}x[n]e^{-jke_{0}n} \\
DFT^{-1} = x[n] =\frac{1}{N_{0}} \sum_{k=0}^{N_{0}-1} X[k]e^{jk\Omega_{0}n} \\
 \\

\end{align}


$$
Contains interval $X[n]$ is $N_{0}$ data points

$k=0,\dots,N_{0}-1 \quad \Omega_{0}=\frac{2\pi}{N_{0}}$

### Example 1
Problem: Compute the DFT of the signal {12,8,4}.
Solution:

$$

\begin{align} 
N_{0}=4\quad \Omega_{0} = \frac{2\pi}{4} = \frac{\pi}{2}\\
\\
X[k] = {x_{0},x_{1},x_{2},x_{3}} \\
X[k] = \sum_{n=0}^{N_{0}-1} x[n] e^{-jk\Omega_{0}n}\quad \text{DFT} \\
X[0] = 12 + 8+4+8=32 \\
X[1] = 12e^{-j\Omega_{0}0} + 8e^{-j\Omega_{0}1}+4e^{j\Omega_{0}2}+e^{j\Omega_{0}3} = 12+8e^{-j\pi/2} + \dots \\
=12+\cos\left( -\frac{\pi}{2} \right)+j\sin\left( -\frac{\pi}{2} \right) = \dots \\
\end{align}
$$
So...

$$
\begin{align}
X[0] = 32\\
X[1] = 8\\
X[2] = 0\\
X[3] = 12+j8-4j8=8
\end{align}

$$
$$
X[k] = \sum_{n=0}^{N_{0}-1} x[n] e^{-jk\Omega_{0}n}
$$
### DFT Matrix
$$
X[k] = \sum_{n=0}^{N_{0}-1} x[n]e^{-jk\Omega_{0}n},\quad  k=0,1,\dots,N_{0}-1,


$$
Matrix:
$$
\begin{bmatrix}
X[0]   &  \\
X[1] &  \\
X[2] &  \\
\vdots &  \\
X[N_{0}-1]
\end{bmatrix}
=
\begin{bmatrix}
1 &  1 &  1 &  \dots  & 1 &  \\
1  & e^{-j_{1}\Omega_{0}1} &  e^{-j_{1}\Omega_{0}2}  & \dots  & e^{-j_{1}\Omega_{0}N_{0}-1} &  \\
\vdots  & \vdots  & \vdots  & \dots  & \vdots \\
1  & e^{-j(n_{0}-1)\Omega_{0}1} & e^{-j(n_{0}-1)\Omega_{0}2}  & \dots  & e^{-j(n_{0}-1)\Omega_{0}(N_{0}-1)}
\end{bmatrix}
\begin{bmatrix} 
x[0] \\ 
x[1] \\ 
x[2] \\
\vdots \\
x[N_{0}-1]
\end{bmatrix}

$$

### Why do we need the DFT?
- DFT is the DTFS for periodic signals
- If data is non periodic, DTFT is impractical because sum -00 to 00
- DFT is practical for both infinite but periodic signals, or "discrete" (finite) signals

### Convolution Evaluation

Let us suppose $x_{1}[n]$ is of duration $N_{1}$ and singnal $x_{2}[n]$ is of duration $N_{2}$ and we are interested in computing their convolution

$$
y[n] = x_{1}[n]*x_{2}[ n]
$$
Form last week lecture: $N_{c} = N_{1}+N_{2}-1$
so...
$$
\begin{align}
x'_{1} = {x_{1}[n],0\dots ,0}\quad x_{2}' =
\end{align}
$$