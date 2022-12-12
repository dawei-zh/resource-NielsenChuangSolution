## Exercise 2.60

To calculate eigenvalue of operator $\vec{v}\cdot\vec{\sigma}$, we can expand the operator as
$$
\begin{align}
\vec{v}\cdot\vec{\sigma} &= v_{x}\sigma_x + v_y\sigma_y + v_z\sigma_z \\
&= \begin{pmatrix}
0 & v_x\\ v_x &0
\end{pmatrix} + i\begin{pmatrix}
0 & -v_y\\ v_y &0
\end{pmatrix}+ \begin{pmatrix}
v_z & 0\\ 0 &-v_z
\end{pmatrix} \\
&= \begin{pmatrix}
v_z & v_x-iv_y\\ v_x+iv_y &-v_z
\end{pmatrix}
\end{align} \tag{1}\label{1}
$$
Then we could solve the following equation for eigenvalue $\lambda$, 
$$
\begin{align}
|\vec{v}\cdot\vec{\sigma} - \lambda I| &= \begin{vmatrix}
v_z-\lambda & v_x-iv_y\\ v_x+iv_y &-v_z-\lambda
\end{vmatrix} \\
&= -v_z^2+\lambda^2 - v_x^2 - v_y^2  \\
&= \lambda^2 - 1 = 0 \iff \lambda = \pm 1
\end{align}\tag{2}
$$
where we use $v^2_x+v^2_y+v^2_z = 1$ since $\vec{v}$​ is a unit vector. The corresponding normalized eigenvectors can be obtained by
$$
\begin{align}
\vec{v}\cdot\vec{\sigma}|w_+\rangle &= \begin{pmatrix}
v_z & v_x-iv_y\\ v_x+iv_y &-v_z
\end{pmatrix}\begin{pmatrix}
a \\ b
\end{pmatrix} = \begin{pmatrix}
a \\ b
\end{pmatrix} \iff |w_+\rangle = \frac{1}{\sqrt{2+2v_z}}\begin{pmatrix}
v_z+1 \\ v_x+iv_y
\end{pmatrix} \tag{3a}\\

\vec{v}\cdot\vec{\sigma}|w_-\rangle &= \begin{pmatrix}
v_z & v_x-iv_y\\ v_x+iv_y &-v_z
\end{pmatrix}\begin{pmatrix}
c \\ d
\end{pmatrix} = -\begin{pmatrix}
c \\ d
\end{pmatrix} \iff |w_-\rangle = \frac{1}{\sqrt{2+2v_z}}\begin{pmatrix}
-v_x+iv_y \\ v_z+1
\end{pmatrix}\tag{3b}
\end{align}
$$
Note that the normalized coefficient is obtained by
$$
\begin{align}
&\text{For }|w_+\rangle: \|v_z+1\|^2 + \|v_x+iv_y\|^2 = v_z^2 +2v_z +1+v_x^2+v_y^2 = 2+2v_z \\
&\text{For }|w_-\rangle: \|-v_x+iv_y\|^2+\|v_z+1\|^2  = v_x^2+v_y^2+v_z^2 +2v_z +1 = 2+2v_z
\end{align}\tag{4}
$$
Then the projector $P_{+}$ can be obtained by
$$
\begin{align}
P_+ = |w_+\rangle\langle w_+| &= \frac{1}{{2+2v_z}}\begin{pmatrix}
v_z+1 \\ v_x+iv_y
\end{pmatrix} \begin{pmatrix}
v_z+1 & v_x-iv_y
\end{pmatrix} \\
&= \frac{1}{{2(1+v_z)}}\begin{pmatrix}
\;(v_z+1)^2 & (v_z+1)(v_x-iv_y)\;\\
\;(v_z+1)(v_x+iv_y) & (v_x+iv_y)(v_x-iv_y)\;\\
\end{pmatrix} \\
&= \frac{1}{{2}}\begin{pmatrix}
\;v_z+1 & v_x-iv_y\;\\
\;v_x+iv_y & (v^2_x+v^2_y)/(v_z+1)\;\\
\end{pmatrix} \\
&= \frac{1}{{2}}\begin{pmatrix}
\;v_z+1 & v_x-iv_y\;\\
\;v_x+iv_y & (1-v^2_z)/(v_z+1)\;\\
\end{pmatrix} \\
&= \frac{1}{{2}}\begin{pmatrix}
\;v_z+1 & v_x-iv_y\;\\
\;v_x+iv_y & 1-v_z\;\\
\end{pmatrix} 
\end{align}\tag{5}\label{5}
$$
Compare eq. $\eqref{1}$ and eq. $\eqref{5}$, we could conclude that $P_{+} = (I + \vec{v}\cdot\vec{\sigma})/2$. Similarly, we have for $P_{-}$, 
$$
\begin{align}
P_- = |w_-\rangle\langle w_-| &= \frac{1}{{2+2v_z}}\begin{pmatrix}
-v_x+iv_y \\ v_z+1
\end{pmatrix} \begin{pmatrix}
-v_x-iv_y & v_z+1
\end{pmatrix} \\
&= \frac{1}{{2(1+v_z)}}\begin{pmatrix}
\;(v_x+iv_y)(v_x-iv_y) & -(v_z+1)(v_x-iv_y)\;\\
\;-(v_z+1)(v_x+iv_y) & (v_z+1)^2\;\\
\end{pmatrix} \\
&= \frac{1}{{2}}\begin{pmatrix}
\;(v_x^2+v^2_y)/(v_z+1) & -(v_x-iv_y)\;\\
\;-(v_x+iv_y) & v_z+1\;\\
\end{pmatrix} \\
&= \frac{1}{{2}}\begin{pmatrix}
\;(1-v^2_z)/(v_z+1) & -(v_x-iv_y)\;\\
\;-(v_x+iv_y) & v_z+1\;\\
\end{pmatrix} \\
&= \frac{1}{{2}}\begin{pmatrix}
\;1-v_z & -(v_x-iv_y)\;\\
\;-(v_x+iv_y) & 1-(-v_z)\;\\
\end{pmatrix} = \frac{1}{2}(I - \vec{v}\cdot\vec{\sigma})
\end{align}\tag{6}\label{6}
$$
