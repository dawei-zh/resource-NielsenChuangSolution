## Exercise 2.58

Suppose we can measure an observable $M$ and we prepare an eigenstate $|\psi\rangle$ of $M$ such that $M|\psi\rangle = m|\psi\rangle$. Then the average value of the measurement is obtained by
$$
\langle \psi|M|\psi\rangle = \langle \psi|m|\psi\rangle = m \tag{1}
$$
The standard deviation associated to observation of $M$ is given by
$$
\begin{align}
[\Delta (M)]^2 =& \langle M^2 \rangle - \langle M \rangle^2 \\
=& \langle \psi|M^2|\psi\rangle - \langle \psi|M|\psi\rangle^2 \\
=& \langle \psi|MM|\psi\rangle - m^2 \\
\end{align}\tag{2}\label{2}
$$
Since observable $M$ is a Hermitian operator, we could re-write eq. $\eqref{2}$ as
$$
\begin{align}
[\Delta (M)]^2 &= \langle \psi|MM|\psi\rangle - m^2 = \langle \psi|M^{\dagger}M|\psi\rangle - m^2\\
&=(\langle \psi|m)(m|\psi\rangle) - m^2=0
\end{align}\tag{3}
$$
Thus, if we prepare a quantum system in an eigenstate of observable $M$ with corresponding eigenvalue $m$​, the average observed value of $M$ is $m$, and the standard deviation is $0$. 
