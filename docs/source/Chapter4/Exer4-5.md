# Exercise 4.5

Consider $\hat{n} = (n_x, n_y, n_z)$ is a real unit vector in three dimension, and $\vec{\sigma} = (X, Y, Z)$. Then 

$$
\begin{align}
(\hat{n}\cdot \vec{\sigma} )^{2} =& (n_xX + n_yY + n_zZ)(n_xX + n_yY + n_zZ) \\
=& n_x^2 X^2 + n_xn_yXY + n_xn_zXZ +  n_xn_yYX \\
&+ n^2_yY^2 + n_yn_zYZ+ n_xn_zZX + n_yn_zZY + n_z^{2}Z^{2}\\
=& n_x^2 I + n_xn_yXY + n_xn_zXZ +  n_xn_yYX \\
&+ n^2_yI + n_yn_zYZ+ n_xn_zZX + n_yn_zZY + n_z^{2}I\\
\end{align}
$$(eqn:4.5.1)

Notice that for Pauli matrices, we have the anti-commutation rule as

$$
\{X, Y\}  = \{Y, Z\}  = \{X, Z\} =0
$$(eqn:4.5.2)

Then we could simplify eq. {eq}`eqn:4.5.1` as

$$
\begin{align}
(\hat{n}\cdot \vec{\sigma} )^{2} =& n_x^2 I + n^2_yI  + n_z^{2}I = I
\end{align}
$$(eqn:4.5.3)

where we have $n^2_x + n^2_y + n^2_z = 1$ for unit vector $\hat{n}$. From Exercise 4.2 we have $\exp (iAx) = \cos (x)I + i\sin(x)A$ where $A^2 = I$. Let $A = \hat{n}\cdot\vec{\sigma}$ and $x= -\theta/2$, we have 

$$
\begin{align}
\exp (-i\hat{n}\cdot\vec{\sigma}\theta/2) &= \cos \left(\frac{\theta}{2}\right)I - i\sin\left(\frac{\theta}{2}\right)(\hat{n}\cdot\vec{\sigma}) \\
&= \cos \frac{\theta}{2}I - i\sin\frac{\theta}{2}(n_xX + n_yY + n_zZ) \\
\end{align}
$$(eqn:4.5.4)
