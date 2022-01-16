## Exercise 4.2

Suppose $A$ is a matrix such that $A^2 = I$ and $x$ is a real number. We can use Taylor expansion to calculate $\exp (iAx)$. The Taylor expansion of $e^{x}$ is given by
$$
e^{x} = \sum_{n=0}^{\infty}\frac{x^n}{n!} = 1 + x + \frac{x^2}{2!} + \dotsc\tag{1}\label{1}
$$
Meanwhile, the Taylor expansion of $\sin\theta$ and $\cos\theta$ are given by
$$
\begin{align}
\sin x &= \sum^{\infty}_{n=0}\frac{(-1)^{n}}{(2n+1)!}x^{2n+1}  = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \dotsc\tag{2a}\label{2a}\\
\cos x &= \sum^{\infty}_{n=0}\frac{(-1)^{n}}{(2n)!}x^{2n} = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \dotsc\tag{2b}\label{2b}
\end{align}
$$
According to eq. $\eqref{1}$, the Taylor expansion for $\exp (iAx)$ is given by
$$
\begin{align}
\exp (iAx) &= \sum_{n=0}^{\infty}\frac{(iAx)^n}{n!} = 1 + iAx+\frac{i^2A^2x^2}{2!} + \frac{i^3A^3x^3}{3!} + \frac{i^4A^4x^4}{4!} + \dotsc \\
\end{align}\tag{3}\label{3}
$$
From eq. $\eqref{3}$ we can find that, 

* for $n$​ is even number we have
  $$
  n\text{ is even: }1 -\frac{A^2x^2}{2!} + \frac{A^4x^4}{4!} - \frac{A^6x^6}{6!} + \frac{A^8x^8}{8!} - \frac{A^{10}x^{10}}{10!}\dotsc \tag{4}\label{4}
  $$
  
* for $n$ is odd number we have
  $$
  n\text{ is odd: }iAx -\frac{iA^3x^3}{3!} + \frac{iA^5x^5}{5!} - \frac{iA^7x^7}{7!} + \frac{iA^9x^9}{9!} - \frac{iA^{11}x^{11}}{11!}\dotsc \tag{5}\label{5}
  $$

From eq. $\eqref{4}$ and $\eqref{5}$, and also note that $A^2 = I$, we could find that eq. $\eqref{3}$ can be re-written as
$$
\exp (iAx) = I\cos {\theta} + i A\sin {\theta} \tag{6}\label{6}
$$
