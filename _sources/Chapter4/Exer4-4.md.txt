# Exercise 4.4 (Reviewing)

The idea here is that a unitary gate $U$ can be decomposed in the following form, 

$$
U = e^{i\alpha}R_{x}(\beta)R_{z}(\gamma)R_{x}(\delta)
$$(eqn:4.4.1)

Therefore, we need to find the decomposition form of Hadmard gate with some specific rotational angle and $\varphi$. 

The Hadmard gate $H$ is defined by

$$
H = \frac{1}{\sqrt{2}}\begin{pmatrix}
1 & 1 \\ 1 & -1 
\end{pmatrix}
$$(eqn:4.4.2)

The rotational-$x$ gate is defined by

$$
R_{x}(\theta) = \begin{pmatrix}
\cos\frac{\theta}{2} & -i\sin\frac{\theta}{2} \\
-i\sin\frac{\theta}{2} & \cos\frac{\theta}{2} \\
\end{pmatrix}
$$(eqn:4.4.3)

The rotational-$z$ gate is defined by

$$
R_{z}(\theta) = \begin{pmatrix}
e^{-i\theta/2} & 0 \\
0 & e^{i\theta/2} \\
\end{pmatrix}
$$(eqn:4.4.4)

Notice that we could re-write the Hadmard gate into the sum of Pauli matrices, that is, 

$$
H = \frac{1}{\sqrt{2}}\begin{pmatrix}
1 & 1 \\ 1 & -1 
\end{pmatrix} = \frac{X + Z}{\sqrt{2}} 
$$(eqn:4.4.5)

Since Hadmard gate is a sum of Pauli matrices, we could re-write rotational gate into the sum of Pauli matrices with some special angle $\theta$, and use the combination of special rotational gates to construct the Hadmard gate. 

We could also re-write the rotational gate into sum of Pauli matrices, 

$$
R_{x}(-\pi/2) = \begin{pmatrix}
\cos\frac{\pi}{4} & i\sin\frac{\pi}{4}  \\
i\sin\frac{\pi}{4} & \cos\frac{\pi}{4}  \\
\end{pmatrix} = \frac{1}{\sqrt{2}}\begin{pmatrix}
1 & i  \\
i & 1  \\
\end{pmatrix} = \frac{I + iX}{\sqrt{2}} 
$$(eqn:4.4.6)

and also we have for rotational-$z$ gate, 

$$
\begin{align}
R_{z}(-\pi/2) &= \begin{pmatrix}
e^{i\pi/4} & 0 \\
0 & e^{-i\pi/4} \\
\end{pmatrix} \\
&= \begin{pmatrix}
\cos\frac{\pi}{4}+i\sin\frac{\pi}{4} & 0  \\
0 & \cos\frac{\pi}{4}-i\sin\frac{\pi}{4}  \\
\end{pmatrix} \\
&= \frac{1}{\sqrt{2}}\begin{pmatrix}
1+i & 0  \\
0 & 1-i\\
\end{pmatrix} = \frac{I + i Z}{\sqrt{2}}
\end{align}
$$(eqn:4.4.7)

Then we could have 

$$
\begin{align}
R_{x}(-\pi/2)R_{z}(-\pi/2)R_{x}(-\pi/2) &= \left(\frac{I + iX}{\sqrt{2}}\right)\left(\frac{I + iZ}{\sqrt{2}}\right)\left(\frac{I + iX}{\sqrt{2}}\right) \\
&= \frac{1}{2\sqrt{2}}( I+ iX + iZ + i^2ZX + iX + i^2X^2 + i^2XZ + i^3 XZX) \\
&= \frac{1}{2\sqrt{2}}( I+ iX + iZ -ZX + iX -X^2 -XZ - i XZX)  \\
&=  \frac{1}{2\sqrt{2}}( iX + iZ + iX + i Z)  \\
&= i\frac{X+Z}{\sqrt{2}} = iH\\
\end{align}
$$(eqn:4.4.8)

Note that we adopt $XZX = -Z$ and $XZ + ZX = \{X, Z\} = 0$ in the calculation. Then we could get 

$$
H = -iR_{x}(-\pi/2)R_{z}(-\pi/2)R_{x}(-\pi/2) = e^{-i\pi/2}R_{x}(-\pi/2)R_{z}(-\pi/2)R_{x}(-\pi/2)
$$(eqn:4.4.9)

In addition, we could also find that 

$$
R_{x}(\pi/2) =  \frac{I - iX}{\sqrt{2}},  R_{z}(\pi/2)= \frac{I - iZ}{\sqrt{2}}
$$(eqn:4.4.10)

Then we could have 

$$
\begin{align}
R_{x}(\pi/2)R_{z}(\pi/2)R_{x}(\pi/2) &= \left(\frac{I - iX}{\sqrt{2}}\right)\left(\frac{I - iZ}{\sqrt{2}}\right)\left(\frac{I - iX}{\sqrt{2}}\right) \\
&= \frac{1}{2\sqrt{2}}( I- iX - iZ + i^2ZX - iX + i^2X^2 + i^2XZ - i^3 XZX) \\
&= \frac{1}{2\sqrt{2}}( I- iX - iZ -ZX - iX -I -XZ - i Z) \\
&= -\frac{1}{2\sqrt{2}}( iX + iZ + iX   + i Z) =  -iH\\
\end{align}
$$(eqn:4.4.11)

Finally, we could get 

$$
H = i R_{x}(\pi/2)R_{z}(\pi/2)R_{x}(\pi/2) = e^{i\pi/2}R_{x}(\pi/2)R_{z}(\pi/2)R_{x}(\pi/2)
$$(eqn:4.4.12)
