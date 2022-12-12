## Exercise 2.34

To calculate the square root and logarithm of the given matrix 
$$
A = \begin{pmatrix}
4 &3 \\ 3 &4
\end{pmatrix}\tag{1}
$$
we need to firstly calculate its eigenvalues as follow, 
$$
|A - \lambda I| = \begin{vmatrix}
4-\lambda & 3 \\ 3 & 4-\lambda 
\end{vmatrix} = (4-\lambda)^2 - 9 = 0 \iff \lambda_{1}=7, \lambda_2 = 1\tag{2}
$$
The corresponding normalized eigenvectors are given by
$$
\begin{align}
A|v_1\rangle &= \begin{pmatrix}
4 &3 \\ 3 &4
\end{pmatrix}\begin{pmatrix}
a \\ b
\end{pmatrix} = 7\begin{pmatrix}
a \\ b
\end{pmatrix} \iff |v_1\rangle = \frac{1}{\sqrt{2}}\begin{pmatrix}
1 \\ 1
\end{pmatrix} \tag{3a}\\

A|v_2\rangle &= \begin{pmatrix}
4 &3 \\ 3 &4
\end{pmatrix}\begin{pmatrix}
c \\ d
\end{pmatrix} = \begin{pmatrix}
c \\ d
\end{pmatrix} \iff |v_2\rangle = \frac{1}{\sqrt{2}}\begin{pmatrix}
1 \\ -1
\end{pmatrix}\tag{3b}
\end{align}
$$
where the coefficient $1/\sqrt{2}$ makes sure the eigenvector is unit vector. Note that the reason we need to normalized the eigenvector is that we need to use the spectral decomposition of matrix $A$ as a starting point to calculate the function of $A$. We can also verify that the normalized eigenvectors give a spectral decomposition of $A$, 
$$
\begin{align}
A = \sum_{i} \lambda_{i}|i\rangle\langle i| =& 7\cdot\frac{1}{2}\begin{pmatrix}1 \\ 1\end{pmatrix}\begin{pmatrix}1&1\end{pmatrix} + \frac{1}{2}\begin{pmatrix}1 \\ -1\end{pmatrix}\begin{pmatrix}1&-1\end{pmatrix} \\
=& \frac{7}{2}\begin{pmatrix}
1 & 1\\
1 & 1
\end{pmatrix} + \frac{1}{2}\begin{pmatrix}
1 & -1\\
-1 & 1
\end{pmatrix}  = \begin{pmatrix}
4 & 3\\
3 & 4
\end{pmatrix}
\end{align}\tag{4}
$$
Then we could calculate 

* The square root of $A$, 
  $$
  \begin{align}
  \sqrt{A} = \sum_{i} \sqrt{\lambda_{i}}|i\rangle\langle i| &= \sqrt{7}\cdot\frac{1}{2}\begin{pmatrix}1 \\ 1\end{pmatrix}\begin{pmatrix}1&1\end{pmatrix} + \frac{1}{2}\begin{pmatrix}1 \\ -1\end{pmatrix}\begin{pmatrix}1&-1\end{pmatrix} \\
  &=\frac{1}{2}\begin{pmatrix}
  \sqrt{7} + 1 & \sqrt{7} - 1 \\
  \sqrt{7} - 1 & \sqrt{7} + 1
  \end{pmatrix}
  \end{align}\tag{5}
  $$

* The logarithm of $A$,
  $$
  \begin{align}
  \log{A} = \sum_{i} \log{\lambda_{i}}|i\rangle\langle i| &= \log{7}\cdot\frac{1}{2}\begin{pmatrix}1 \\ 1\end{pmatrix}\begin{pmatrix}1&1\end{pmatrix} + \log 1\cdot\frac{1}{2}\begin{pmatrix}1 \\ -1\end{pmatrix}\begin{pmatrix}1&-1\end{pmatrix} \\
  &=\frac{\log 7}{2}\begin{pmatrix}
   1 & 1\\
  1 & 1
  \end{pmatrix}
  \end{align}\tag{6}
  $$
