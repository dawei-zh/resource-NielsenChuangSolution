# Exercise 4.3

The rotation operator about the $\hat{z}$ axis is given by

$$
R_z(\theta) = \cos\frac{\theta}{2}\ I - i\sin\frac{\theta}{2}Z = \begin{pmatrix}
e^{-i\theta/2} & 0 \\ 0 & e^{i\theta/2}
\end{pmatrix}
$$(eqn:4.3.1)

When $\theta = \pi/4$​, we have

$$
R_z(\pi/4) = \begin{pmatrix}
e^{-i\pi/8} & 0 \\ 0 & e^{i\pi/8}
\end{pmatrix}
$$(eqn:4.3.2)

Note that the $T$ gate is defined by

$$
T = e^{i\pi/8}\begin{pmatrix}
e^{-i\pi/8} & 0 \\ 0 & e^{i\pi/8}
\end{pmatrix}
$$(eqn:4.3.3)

Compare eq. {eq}`eqn:4.3.2` and eq. {eq}`eqn:4.3.3`, we conclude that, up to a global phase $e^{i\pi/8}$, the $\pi/8$ gate $T$ satisfies $T = R_z(\pi/4)$. 