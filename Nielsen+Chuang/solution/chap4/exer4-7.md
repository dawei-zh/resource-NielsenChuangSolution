## Exercise 4.7

The Pauli matrices are given by
$$
X = \begin{pmatrix}
0 & 1\\ 1 &0
\end{pmatrix},Y = \begin{pmatrix}
0 & -i\\ i &0
\end{pmatrix} \tag{1}\label{1}
$$
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
\end{pmatrix} = -Y\tag{2}
$$
The rotation operator about the $\hat{y}$ axis is given by
$$
R_y(\theta) = \cos\frac{\theta}{2}\ I - i\sin\frac{\theta}{2}Y = \begin{pmatrix}
\cos\frac{\theta}{2} & -\sin\frac{\theta}{2} \\ \sin\frac{\theta}{2} & \cos\frac{\theta}{2}
\end{pmatrix}\tag{3}
$$
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
\end{align}\tag{4}\label{4}
$$
Also, for $R_y(-\theta)$ we have
$$
R_y(-\theta) = \begin{pmatrix}
\cos\frac{-\theta}{2} & -\sin\frac{-\theta}{2} \\ \sin\frac{-\theta}{2} & \cos\frac{-\theta}{2}
\end{pmatrix} = \begin{pmatrix}
\cos\frac{\theta}{2} & \sin\frac{\theta}{2} \\ -\sin\frac{\theta}{2} & \cos\frac{\theta}{2}
\end{pmatrix}\tag{5}\label{5}
$$
According to eq. $\eqref{4}$ and eq. $\eqref{5}$, we have
$$
XR_y(\theta)X = R_y(-\theta)\tag{6}
$$
