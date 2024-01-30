# Exercise 5.1

Consider a transformation $F$ defined as 

$$
F \equiv \sum_{j=0}^{N-1} \left[\sum_{k=0}^{N-1}\frac{1}{\sqrt{N}}\exp\left(2i\pi\frac{jk}{N}\right)|k\rangle\right]\langle j| = \sum_{j=0}^{N-1} |\tilde{j}\rangle\langle j|
$$(eqn:5.1.1)

where basis $\{|j\rangle\}$ and $\{|k\rangle\}$ are different orthonormal basis set. Above transformation is the quantum Fourier transformation since for any basis vector $|j\rangle$, it equivalently performs 

$$
|j\rangle \to|\tilde{j}\rangle = \sum_{k=0}^{N-1}\frac{1}{\sqrt{N}}\exp\left(2i\pi\frac{jk}{N}\right)|k\rangle
$$(eqn:5.1.2)

To prove the transformation in eq. {eq}`eqn:5.1.1` is unitary, we have

$$
\begin{align}
F^{\dagger}F &=\left[\sum_{j=0}^{N-1} |\tilde{j}\rangle\langle j|\right]^{\dagger}\left[\sum_{n=0}^{N-1} |\tilde{n}\rangle\langle n|\right] \\
&= \left[\sum_{j=0}^{N-1} |j\rangle\langle \tilde{j}|\right]^{\dagger}\left[\sum_{n=0}^{N-1} |\tilde{n}\rangle\langle n|\right] \\
&= \sum_{n,j} |j\rangle\langle \tilde{j}|\tilde{n}\rangle\langle n|
\end{align}
$$(eqn:5.1.3)

where $|j\rangle$ and $|n\rangle$ are different notation for same orthonormal basis. Then the inner product $\langle \tilde{j}|\tilde{n}\rangle$ becomes

$$
\begin{align}
\langle \tilde{j}|\tilde{n}\rangle &= \left[\sum_{k=0}^{N-1}\frac{1}{\sqrt{N}}\exp\left(-2i\pi\frac{jk}{N}\right)\langle k|\right]\left[\sum_{m=0}^{N-1}\frac{1}{\sqrt{N}}\exp\left(2i\pi\frac{nm}{N}\right)|m\rangle\right] \\
&= \frac{1}{N}\sum_{m,k}  \exp\left(-2i\pi\frac{jk}{N}\right)\exp\left(2i\pi\frac{nm}{N}\right)\langle k|m\rangle \\
&= \frac{1}{N}\sum_{k=0}^{N-1}  \exp\left(-2i\pi\frac{jk}{N}\right)\exp\left(2i\pi\frac{nk}{N}\right)\\
&= \frac{1}{N}\sum_{k=0}^{N-1}  \exp\left[2i\pi\frac{(n-j)k}{N}\right]
\end{align}
$$(eqn:5.1.4)

where $|k\rangle$ and $|m\rangle$​ are different notations for same orthonormal basis. Note that 

$$
\begin{align}
\exp\left[2i\pi\frac{(n-j)(k+1)}{N}\right] &=  \exp\left[2i\pi\frac{(n-j)k}{N}+2i\pi\frac{(n-j)}{N}\right] \\
&=  \exp\left[2i\pi\frac{(n-j)k}{N}\right]\exp\left[2i\pi\frac{(n-j)}{N}\right]
\end{align}
$$(eqn:5.1.5)

so we can use geometry series to compute the sum in eq. {eq}`eqn:5.1.4`​ with common ratio $r=\exp[2i\pi(n-j)/N]$, then

$$
\begin{align}
\langle \tilde{j}|\tilde{n}\rangle &= \frac{1}{N}\sum_{k=0}^{N-1}  \exp\left[2i\pi\frac{(n-j)k}{N}\right]\\
&= \frac{1}{N} \frac{1-r^{N}}{1-r} \\
&= \frac{1}{N} \frac{1-\exp[2i\pi(n-j)]}{1-\exp[2i\pi(n-j)/N]} \\
\end{align}
$$(eqn:5.1.6)

Then from above calculation, 

* for $r = 1$, we have $n = j$ and $\langle \tilde{j}|\tilde{n}\rangle = 1$,

* for any $r\neq 1$ we have $n\neq j$ but $n - j$ is a integer. Since

  $$
  \exp[2i\pi(n-j)] = \cos[2\pi(n-j)] + i\sin[2\pi(n-j)]
  $$(eqn:5.1.7)

  For any $n - j$ as integer, $\cos[2\pi(n-j)]$ is always $1$ and $\sin[2\pi(n-j)]$ is always $0$, so $\exp[2i\pi(n-j)] = 1$ for $\forall n, j$. Meanwhile, $(n-j)/N \neq$ so $\exp[2i\pi(n-j)/N] \neq 1$ and the denominator will not be $1$. In this case, $\langle \tilde{j}|\tilde{n}\rangle  = 0$. 

In conclusion, we have $\langle \tilde{j}|\tilde{n}\rangle = \delta_{jn}$ so $F^{\dagger}F = \sum_{n,j} \delta_{jn}|j\rangle\langle n|$ which is an identity under the matrix representation of $\{|j\rangle\}$, the basis before transformation. Then we can conclude that the Fourier transformation is unitary. 

**Question: **Is above result basis dependent?
