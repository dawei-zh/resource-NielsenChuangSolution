## Obtain Eq. 1.4

An arbitrary single-qubit state is written as $|\psi\rangle = a|0\rangle + b|1\rangle$ where complex coefficient $a$ and $b$ satisfy the normalization condition, $|a|^2 + |b|^2 = 1$. The complex number $a$ and $b$ can be written in the form of 
$$
a = |a|e^{i\gamma}, b = |b|e^{i\alpha} = |b|e^{i(\gamma+\varphi)} = |b|e^{i\gamma}e^{i\varphi} \tag{1}\label{1}
$$
where in the second identity of number $b$, we re-write the argument of $b$ into the form $\alpha = \gamma+\varphi$. With the help of eq. $\eqref{1}$, we can rewrite $|\psi\rangle$ as
$$
\begin{align}
|\psi\rangle =& |a|e^{i\gamma}|0\rangle + |b|e^{i\gamma}e^{i\varphi}|1\rangle \\
=& e^{i\gamma}(|a||0\rangle + |b|e^{i\varphi}|1\rangle)
\end{align}\tag{2}\label{2}
$$
Note that $|a|^2 + |b|^2 = 1$, then we can re-write $|a|$ and $|b|$ as
$$
|a| = \cos\frac{\theta}{2}, |b| = \sin\frac{\theta}{2}, \theta\in [0,\pi] \tag{3}\label{3}
$$
In eq. $\eqref{3}$, since we need to make sure $0<|a|<1$ and $0<|b|<1$, we need to write the sine or cosine of $\theta/2$ rather than the sine or cosine of $\theta$. Substitute eq. $\eqref{3}$ to eq. $\eqref{2}$​, we then have
$$
\begin{align}
|\psi\rangle =& e^{i\gamma}(|a||0\rangle + |b|e^{i\varphi}|1\rangle) = e^{i\gamma}\left(\cos\frac{\theta}{2}|0\rangle + e^{i\varphi}\sin\frac{\theta}{2}|1\rangle\right) 
\end{align}\tag{2}
$$