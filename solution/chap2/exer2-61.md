## Exercise 2.61

From Exercise 2.60, we could find the observable $\vec{v}\cdot\vec{\sigma}$ can be written as
$$
\begin{align}
\vec{v}\cdot\vec{\sigma} &= \frac{1}{2}(I + \vec{v}\cdot\vec{\sigma}) - \frac{1}{2}(I-\vec{v}\cdot\vec{\sigma}) \\
 &= m_{+}P_{+} + m_{-}P_{-} 
\end{align}\tag{1}
$$
where $m_+$ and $m_-$ are eigenvalues of $\vec{v}\cdot \vec{\sigma}$. If we measure $\vec{v}\cdot \vec{\sigma}$ of the state $|0\rangle$, the probability of getting result $m_+=+1$ is then obtained by
$$
\begin{align}
p(+1) &= \langle 0|P_+|0\rangle \\
&= \frac{1}{{2}}\begin{pmatrix}
1 & 0
\end{pmatrix}\begin{pmatrix}
\;v_z+1 & v_x-iv_y\;\\
\;v_x+iv_y & 1-v_z\;\\
\end{pmatrix} \begin{pmatrix}
1 \\ 0
\end{pmatrix}\\
&= \frac{1}{{2}}\begin{pmatrix}
v_z+1 & v_x-iv_y
\end{pmatrix}\begin{pmatrix}
1 \\ 0
\end{pmatrix} = \frac{v_z+1}{{2}}
\end{align}\tag{2}
$$
The post-measurement state can be obtained by
$$
\begin{align}
\frac{P_+|0\rangle}{\sqrt{p(+1)}} &= \frac{1}{\sqrt{p(+1)}}\cdot\frac{1}{2} \begin{pmatrix}
\;v_z+1 & v_x-iv_y\;\\
\;v_x+iv_y & 1-v_z\;\\
\end{pmatrix} \begin{pmatrix}
1 \\ 0
\end{pmatrix}\\
&=\frac{1}{\sqrt{2v_z+2}}\begin{pmatrix}
v_z+1 \\ v_x+iv_y
\end{pmatrix} = |w_+\rangle
\end{align}\tag{3}
$$
where $|w+\rangle$ is the eigenvector of $\vec{v}\cdot\vec\sigma$ with eigenvalue $+1$ (shown also in Exercise 2.60).

