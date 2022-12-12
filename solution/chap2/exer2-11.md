## Exercise 2.11

The Pauli matrices are given by
$$
X = \begin{pmatrix}
0 & 1\\ 1 &0
\end{pmatrix},Y = \begin{pmatrix}
0 & -i\\ i &0
\end{pmatrix},Z = \begin{pmatrix}
1 & 0\\ 0 &-1
\end{pmatrix} \tag{1}\label{1}
$$
The eigenvectors, eigenvalues and diagonal representation of Pauli matrices are shown below.

* For $X$​, the eigenvalue $\lambda$ is the solution of the following equation,
  $$
  |X - \lambda I|= \begin{vmatrix}
  -\lambda & 1 \\ 1 & -\lambda 
  \end{vmatrix} = \lambda^2 - 1 = 0 \iff \lambda = \pm 1\tag{2}
  $$
  The corresponding normalized eigenvectors are given by
  $$
  \begin{align}
  X|v_1\rangle &= \begin{pmatrix}
  0 & 1\\ 1 &0
  \end{pmatrix}\begin{pmatrix}
  a \\ b
  \end{pmatrix} = \begin{pmatrix}
  a \\ b
  \end{pmatrix} \iff |v_1\rangle = \frac{1}{\sqrt{2}}\begin{pmatrix}
  1 \\ 1
  \end{pmatrix} \tag{3a}\\
  
  X|v_2\rangle &= \begin{pmatrix}
  0 & 1\\ 1 &0
  \end{pmatrix}\begin{pmatrix}
  c \\ d
  \end{pmatrix} = -\begin{pmatrix}
  c \\ d
  \end{pmatrix} \iff |v_2\rangle = \frac{1}{\sqrt{2}}\begin{pmatrix}
  1 \\ -1
  \end{pmatrix}\tag{3b}
  \end{align}
  $$
  The coefficient $1/\sqrt{2}$ is to normalized the eigenvector. Usually, we define $|+\rangle = |v_1\rangle $ and $|-\rangle = |v_2\rangle$. From the eigenvalues and eigenvectors, we could write the diagonal representation for $X$​ as
  $$
  X = |v_1\rangle\langle v_1| -  |v_2\rangle\langle v_2| = |+\rangle\langle +| -  |-\rangle\langle -|\tag{4} 
  $$
  
* For $Y$​, the eigenvalue $\lambda$​ is the solution of the following equation,
  $$
  |Y - \lambda I|= \begin{vmatrix}
  -\lambda & -i \\ i & -\lambda 
  \end{vmatrix} = \lambda^2 - 1 = 0 \iff \lambda = \pm 1\tag{5}
  $$
  The corresponding normalized eigenvectors are given by
  $$
  \begin{align}
  Y|w_1\rangle &= \begin{pmatrix}
  0 & -i\\ i &0
  \end{pmatrix}\begin{pmatrix}
  a \\ b
  \end{pmatrix} = \begin{pmatrix}
  a \\ b
  \end{pmatrix} \iff |w_1\rangle = \frac{1}{\sqrt{2}}\begin{pmatrix}
  1 \\ i
  \end{pmatrix} \tag{6a}\\
  
  Y|w_2\rangle &= \begin{pmatrix}
  0 & -i\\ i &0
  \end{pmatrix}\begin{pmatrix}
  c \\ d
  \end{pmatrix} = -\begin{pmatrix}
  c \\ d
  \end{pmatrix} \iff |w_2\rangle = \frac{1}{\sqrt{2}}\begin{pmatrix}
  1 \\ -i
  \end{pmatrix}\tag{6b}
  \end{align}
  $$
  The coefficient $1/\sqrt{2}$ is to normalized the eigenvector. From the eigenvalues and eigenvectors, we could write the diagonal representation for $Y$ as
  $$
  Y = |w_1\rangle\langle w_1| - |w_2\rangle\langle w_2|\tag{7}
  $$
  
* For $Z$​, the eigenvalue $\lambda$​ is the solution of the following equation,
  $$
  |Z - \lambda I|= \begin{vmatrix}
  1-\lambda & 0 \\ 0 & -1-\lambda 
  \end{vmatrix} = \lambda^2 - 1 = 0 \iff \lambda = \pm 1\tag{8}
  $$
  The corresponding normalized eigenvectors are given by
  $$
  \begin{align}
  Z|u_1\rangle &= \begin{pmatrix}
  1 & 0\\ 0 & -1
  \end{pmatrix}\begin{pmatrix}
  a \\ b
  \end{pmatrix} = \begin{pmatrix}
  a \\ b
  \end{pmatrix} \iff |u_1\rangle = \begin{pmatrix}
  1 \\ 0
  \end{pmatrix} = |0\rangle \tag{9a}\\
  
  Z|u_2\rangle &= \begin{pmatrix}
  1 & 0\\ 0 & -1
  \end{pmatrix}\begin{pmatrix}
  c \\ d
  \end{pmatrix} = -\begin{pmatrix}
  c \\ d
  \end{pmatrix} \iff |u_2\rangle = \begin{pmatrix}
  0 \\ 1
  \end{pmatrix} = |1\rangle\tag{9b}
  \end{align}
  $$
  From the eigenvalues and eigenvectors, we could write the diagonal representation for $Z$​ as
  $$
  Z = |0\rangle\langle 0| - |1\rangle\langle 1|\tag{10}
  $$