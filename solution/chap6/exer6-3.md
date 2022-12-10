## Exercise 6.3

Consider two normalized states $|\alpha\rangle$ and $|\beta\rangle$ as basis, where 
$$
\begin{align}
|\alpha\rangle &= \frac{1}{\sqrt{N-M}}\sum_{x}'' |x\rangle \\
|\beta\rangle &= \frac{1}{\sqrt{M}}\sum_{x}' |x\rangle \\
\end{align}\tag{1}
$$
The Grover iteration is given by $G = 2|\psi\rangle\langle\psi| - I$. We can write the initial state $|\psi\rangle$ with basis $|\alpha\rangle$ and $|\beta\rangle$, that is, 
$$
|\psi\rangle = \frac{1}{N^{1/2}}\sum_{x=0}^{N-1}|x\rangle  = \sqrt{\frac{N-M}{N}}|\alpha\rangle + \sqrt{\frac{M}{N}}|\beta\rangle \tag{2}
$$
Let
$$
\cos\frac{\theta}{2} =\sqrt{\frac{N-M}{N}}, \sin\frac{\theta}{2} =\sqrt{\frac{M}{N}}\tag{3}\label{3}
$$
such that 
$$
\sin\theta =2\cos\frac{\theta}{2} \sin\frac{\theta}{2} =\frac{2\sqrt{M(N-M)}}{N}\tag{4}\label{4}
$$
With the definition of $\sin(\theta/2)$ and $\cos(\theta/2)$, we could write the initial state $|\psi\rangle$ as 
$$
|\psi\rangle = \cos\frac{\theta}{2} |\alpha\rangle + \sin\frac{\theta}{2} |\beta\rangle\tag{5}
$$
From the textbook we know that, 
$$
G|\psi\rangle = \cos\frac{3\theta}{2}|\alpha \rangle + \sin\frac{3\theta}{2}|\beta\rangle \tag{6}
$$
We can use the trigonometry identities to rewrite $\cos({3\theta}/{2})$ and $\sin({3\theta}/{2})$, and $G|\psi\rangle$ becomes 
$$
\begin{align}
G|\psi\rangle =& \left(\cos\theta \cos\frac{\theta}{2} - \sin\theta\sin\frac{\theta}{2}\right)|\alpha \rangle \\
&+ \left(\sin\theta \cos\frac{\theta}{2} + \cos\theta\sin\frac{\theta}{2}\right)|\beta\rangle  \\
\end{align}\tag{7}\label{7}
$$
If we write eq. $\eqref{7}$ in the matrix form with basisi $|\alpha\rangle$ and $|\beta\rangle$, we have 
$$
G|\psi\rangle = \begin{pmatrix}
\cos\theta \cos\frac{\theta}{2} - \sin\theta\sin\frac{\theta}{2} \\
\sin\theta \cos\frac{\theta}{2} + \cos\theta\sin\frac{\theta}{2}
\end{pmatrix} = \begin{pmatrix}
\cos\theta & -\sin\theta \\
\sin\theta & \cos\theta
\end{pmatrix}\begin{pmatrix}
\cos\frac{\theta}{2} \\ \sin\frac{\theta}{2} 
\end{pmatrix}\tag{8}
$$
