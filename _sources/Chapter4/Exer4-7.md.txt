# Exercise 4.7

The Pauli matrices are given by

$$
X = \begin{pmatrix}
0 & 1\\ 1 &0
\end{pmatrix},Y = \begin{pmatrix}
0 & -i\\ i &0
\end{pmatrix}
$$(eqn:4.7.1)

Then we could check

$$
XYX = \begin{pmatrix}
0 & 1\\ 1 &0
\end{pmatrix}\begin{pmatrix}
0 & -i\\ i &0
\end{pmatrix}\begin{pmatrix}
0 & 1\\ 1 &0
\end{pmatrix} = \begin{pmatrix}
i & 0\\ 0 & -i
\end{pmatrix}\begin{pmatrix}
0 & 1\\ 1 &0
\end{pmatrix} = \begin{pmatrix}
0 & i\\ -i & 0
\end{pmatrix} = -Y
$$(eqn:4.7.2)

The rotation operator about the $\hat{y}$ axis is given by

$$
R_y(\theta) = \cos\frac{\theta}{2}\ I - i\sin\frac{\theta}{2}Y = \begin{pmatrix}
\cos\frac{\theta}{2} & -\sin\frac{\theta}{2} \\ \sin\frac{\theta}{2} & \cos\frac{\theta}{2}
\end{pmatrix}
$$(eqn:4.7.3)

Then we could check

$$
\begin{align}
XR_y(\theta)X &= \begin{pmatrix}
0 & 1\\ 1 &0
\end{pmatrix}\begin{pmatrix}
\cos\frac{\theta}{2} & -\sin\frac{\theta}{2} \\ \sin\frac{\theta}{2} & \cos\frac{\theta}{2}
\end{pmatrix}\begin{pmatrix}
0 & 1\\ 1 &0
\end{pmatrix} \\
&= \begin{pmatrix}
\sin\frac{\theta}{2} & \cos\frac{\theta}{2}\\ \cos\frac{\theta}{2} & -\sin\frac{\theta}{2}
\end{pmatrix}\begin{pmatrix}
0 & 1\\ 1 &0
\end{pmatrix} = \begin{pmatrix}
\cos\frac{\theta}{2} & \sin\frac{\theta}{2}\\ -\sin\frac{\theta}{2} & \cos\frac{\theta}{2}
\end{pmatrix} 
\end{align}
$$(eqn:4.7.4)

Also, for $R_y(-\theta)$ we have

$$
R_y(-\theta) = \begin{pmatrix}
\cos\frac{-\theta}{2} & -\sin\frac{-\theta}{2} \\ \sin\frac{-\theta}{2} & \cos\frac{-\theta}{2}
\end{pmatrix} = \begin{pmatrix}
\cos\frac{\theta}{2} & \sin\frac{\theta}{2} \\ -\sin\frac{\theta}{2} & \cos\frac{\theta}{2}
\end{pmatrix}
$$(eqn:4.7.5)

According to eq. {eq}`eqn:4.7.4` and eq. {eq}`eqn:4.7.5`, we have

$$
XR_y(\theta)X = R_y(-\theta)
$$(eqn:4.7.6)

---

A relative simple way to prove $XR_y(\theta)X = R_y(-\theta)$ is to use the relation $XYX=-X$​ directly. That is

$$
\begin{align}
XR_y(\theta)X &= X\left(\cos\frac{\theta}{2} I-i\sin\frac{\theta}{2} Y\right)\\
&=  \cos\frac{\theta}{2} XIX - i\sin\frac{\theta}{2} XYX \\
&= \cos\frac{\theta}{2} I + i\sin\frac{\theta}{2}Y \\
&= \cos\frac{\theta}{2} I - i\sin\left(\frac{-\theta}{2}\right)Y = R_y(-\theta)
\end{align}
$$(eqn:4.7.7)
