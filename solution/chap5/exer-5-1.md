## Exercise 5.1

Consider the quantum Fourier transformation $F$, where 
$$
F \equiv \sum_{j=0}^{N-1} \left(\sum_{k=0}^{N-1}\frac{1}{\sqrt{N}}\exp(2i\pi\frac{jk}{N})|k\rangle\right)\langle j| = \sum_{j=0}^{N-1} |\tilde{j}\rangle\langle j|\tag{1}\label{1}
$$
and it will perform the following transformation, 
$$
|j\rangle \to\sum_{k=0}^{N-1}\frac{1}{\sqrt{N}}\exp(2i\pi\frac{jk}{N})|k\rangle\tag{2}
$$
To prove the transformation in eq. $\eqref{1}$ is unitary, we have
$$
\begin{align}
F^{\dagger}F &=\left[\sum_{j=0}^{N-1} |\tilde{j}\rangle\langle j|\right]^{\dagger}\left[\sum_{n=0}^{N-1} |\tilde{n}\rangle\langle n|\right] \\
&= \left[\sum_{j=0}^{N-1} |j\rangle\langle \tilde{j}|\right]^{\dagger}\left[\sum_{n=0}^{N-1} |\tilde{n}\rangle\langle n|\right] \\
&= \sum_{n,j} |j\rangle\langle \tilde{j}|\tilde{n}\rangle\langle n|
\end{align}\tag{3}
$$
where $|j\rangle$ and $|n\rangle$ is different notation for same orthonormal basis. We can calculate the inner product $\langle \tilde{j}|\tilde{i}\rangle$ as
$$
\begin{align}
\langle \tilde{j}|\tilde{n}\rangle &= \left(\sum_{k=0}^{N-1}\frac{1}{\sqrt{N}}\exp(-2i\pi\frac{jk}{N})\langle k|\right)\left(\sum_{m=0}^{N-1}\frac{1}{\sqrt{N}}\exp(2i\pi\frac{nm}{N})|m\rangle\right) \\
&= \frac{1}{N}\sum_{m,k}  \exp(-2i\pi\frac{jk}{N})\exp(2i\pi\frac{nm}{N})\langle k|m\rangle \\
&= \frac{1}{N}\sum_{k=0}^{N-1}  \exp(-2i\pi\frac{jk}{N})\exp(2i\pi\frac{nk}{N})\\
&= \frac{1}{N}\sum_{k=0}^{N-1}  \exp(2i\pi\frac{(n-j)k}{N})\\

\end{align}\tag{4}\label{4}
$$
where $|k\rangle$ and $|m\rangle$​ is different notation for same orthonormal basis. Note that 
$$
\begin{align}
\exp(2i\pi\frac{(n-j)(k+1)}{N}) &=  \exp(2i\pi\frac{(n-j)k}{N}+2i\pi\frac{(n-j)}{N}) \\
&=  \exp(2i\pi\frac{(n-j)k}{N})\exp(2i\pi\frac{(n-j)}{N})
\end{align}
$$
so we can use geometry series to simplify eq. $\eqref{4}$​ with common ratio $r=\exp[2i\pi(n-j)/N]$ as 
$$
\begin{align}
\langle \tilde{j}|\tilde{n}\rangle &= \frac{1}{N}\sum_{k=0}^{N-1}  \exp(2i\pi\frac{(n-j)k}{N})\\
&= \frac{1}{N} \frac{1-r^{N}}{1-r} \\
&= \frac{1}{N} \frac{1-\exp[2i\pi(n-j)]}{1-\exp[2i\pi(n-j)/N]} \\
\end{align}
$$
Note that for any $r\neq 1$ or $n\neq j$, 
$$
\begin{align}
\exp[2i\pi(n-j)] &= \cos(2\pi(n-j)) + i\sin(2\pi(n-j)) =1
\end{align}
$$
So we have $\langle \tilde{j}|\tilde{n}\rangle = \delta_{jn}$ and the transformation is unitary. 

