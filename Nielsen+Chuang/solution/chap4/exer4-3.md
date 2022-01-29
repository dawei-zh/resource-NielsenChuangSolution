## Exercise 4.3

The rotation operator about the $\hat{z}$ axis is given by
$$
R_z(\theta) = \cos\frac{\theta}{2}\ I - i\sin\frac{\theta}{2}Z = \begin{pmatrix}
e^{-i\theta/2} & 0 \\ 0 & e^{i\theta/2}
\end{pmatrix}\tag{1}
$$
When $\theta = \pi/4$​, the rotation operator is then
$$
R_z(\pi/4) = \begin{pmatrix}
e^{-i\pi/8} & 0 \\ 0 & e^{i\pi/8}
\end{pmatrix}\tag{2}\label{2}
$$
The $T$ gate is given by
$$
T = e^{i\pi/8}\begin{pmatrix}
e^{-i\pi/8} & 0 \\ 0 & e^{i\pi/8}
\end{pmatrix}\tag{3}\label{3}
$$
Compare eq. $\eqref{2}$ and eq. $\eqref{3}$, we conclude that, up to a global phase, the $\pi/8$ gate satisfies $T = R_z(\pi/4)$. 
