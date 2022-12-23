# Exercise 4.2

Suppose $A$ is a matrix such that $A^2 = I$ and $x$ is a real number. We can use Taylor expansion to calculate $\exp (iAx)$ as
$$
\begin{align}
\exp (iAx) &= \sum_{n=0}^{\infty}\frac{(iAx)^n}{n!} = I + iAx+\frac{i^2A^2x^2}{2!} + \frac{i^3A^3x^3}{3!} + \frac{i^4A^4x^4}{4!} + \dotsc \\
\end{align}\tag{1}\label{1}
$$
From eq. $\eqref{1}$ we can find that, 

* If $n$​ is even number, we have
  $$
  \begin{align}
  n\text{ is even: }&I -\frac{A^2x^2}{2!} + \frac{A^4x^4}{4!} - \frac{A^6x^6}{6!} + \frac{A^8x^8}{8!} - \frac{A^{10}x^{10}}{10!}+\dotsc  \\
  =& I -\frac{x^2}{2!}I + \frac{x^4}{4!}I - \frac{x^6}{6!}I + \frac{x^8}{8!}I - \frac{x^{10}}{10!}I+\dotsc 
  \end{align}\tag{2}\label{2}
  $$

* If $n$ is odd number we have
  $$
  \begin{align}
  n\text{ is odd: }&iAx -\frac{iA^3x^3}{3!} + \frac{iA^5x^5}{5!} - \frac{iA^7x^7}{7!} + \frac{iA^9x^9}{9!} - \frac{iA^{11}x^{11}}{11!}+\dotsc  \\
  =& iAx -\frac{iAx^3}{3!} + \frac{iAx^5}{5!} - \frac{iAx^7}{7!} + \frac{iAx^9}{9!} - \frac{iAx^{11}}{11!}+\dotsc 
  \end{align}\tag{3}\label{3}
  $$

where we simplify eq. $\eqref{2}$ and $\eqref{3}$ using $A^2 = I$​. Note that 
$$
\begin{align}
\sin x &= \sum^{\infty}_{n=0}\frac{(-1)^{n}}{(2n+1)!}x^{2n+1}  = x - \frac{x^3}{3!} + \frac{x^5}{5!}- \frac{x^7}{7!} + \frac{x^9}{9!} - \frac{x^{11}}{11!}+\dotsc \tag{4a}\label{4a}\\
\cos x &= \sum^{\infty}_{n=0}\frac{(-1)^{n}}{(2n)!}x^{2n} = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \frac{x^6}{6!}I + \frac{x^8}{8!}I - \frac{x^{10}}{10!}I+\dotsc \tag{4b}\label{4b}
\end{align}
$$
we could rewrite eq. $\eqref{2}$ as $\cos(x) I$ and eq. $\eqref{3}$ as $i\sin(x)A$. Thus, we could re-write eq. $\eqref{1}$ as 
$$
\exp (iAx) = \cos(x)I+  i\sin(x)A \tag{5}\label{5}
$$
From the textbook, we know that the rotation operator about the $\hat{x}, \hat{y}, \hat{z}$ axes are defined by
$$
R_x(\theta) = e^{-i\theta X/2}, R_y(\theta) = e^{-i\theta Y/2}, R_z(\theta) = e^{-i\theta Z/2} \tag{6}\label{6}
$$
Let $x = -\theta/2$ and $A = X, Y, Z$ for $R_x(\theta), R_y(\theta), R_z(\theta)$, respectively, we could rewrite the rotation operator as 