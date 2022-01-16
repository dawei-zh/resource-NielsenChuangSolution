## Exercise 2.11

The Pauli matrices are given by
$$
\sigma_x = \begin{pmatrix}
0 & 1\\ 1 &0
\end{pmatrix},\sigma_y = \begin{pmatrix}
0 & -i\\ i &0
\end{pmatrix},\sigma_z = \begin{pmatrix}
1 & 0\\ 0 &-1
\end{pmatrix} \tag{1}\label{1}
$$
The eigenvectors, eigenvalues and diagonal representation of Pauli matrices are shown below.

* For $\sigma_x$​, the eigenvalue $\lambda$ is the solution of the following equation,
  $$
  |\sigma_{x} - \lambda I|= \begin{vmatrix}
  -\lambda & 1 \\ 1 & -\lambda 
  \end{vmatrix} = \lambda^2 - 1 = 0 \iff \lambda = \pm 1\tag{2}
  $$
  The corresponding eigenvectors are given by
  $$
  \begin{align}
  \sigma_{x}|v_1\rangle &= \begin{pmatrix}
  0 & 1\\ 1 &0
  \end{pmatrix}\begin{pmatrix}
  a \\ b
  \end{pmatrix} = \begin{pmatrix}
  a \\ b
  \end{pmatrix} \iff |v_1\rangle = \frac{1}{\sqrt{2}}\begin{pmatrix}
  1 \\ 1
  \end{pmatrix} \tag{3a}\\
  
  \sigma_{x}|v_2\rangle &= \begin{pmatrix}
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
  The coefficient $1/\sqrt{2}$ is to normalized the eigenvector. From the eigenvalues and eigenvectors, we can find that the diagonalizing matrix $D$ is 
  $$
  D = \frac{1}{\sqrt{2}}\begin{pmatrix}
  1 & 1 \\ 1 & -1
  \end{pmatrix} \iff D^{-1} = \frac{1}{\sqrt{2}}\begin{pmatrix}
  1 & 1 \\ 1 & -1
  \end{pmatrix}\tag{4}
  $$
  and thus
  $$
  \sigma_x = \begin{pmatrix}
  0 & 1\\ 1 &0
  \end{pmatrix} = \frac{1}{2}\begin{pmatrix}
  1 & 1 \\ 1 & -1
  \end{pmatrix}\begin{pmatrix}
  1 & 0 \\ 0 & -1
  \end{pmatrix}\begin{pmatrix}
  1 & 1 \\ 1 & -1
  \end{pmatrix}  = D\Lambda D^{-1}\tag{5}
  $$
  
* For $\sigma_y$​, the eigenvalue $\lambda$​ is the solution of the following equation,
  $$
  |\sigma_{y} - \lambda I|= \begin{vmatrix}
  -\lambda & -i \\ i & -\lambda 
  \end{vmatrix} = \lambda^2 - 1 = 0 \iff \lambda = \pm 1\tag{6}
  $$
  The corresponding eigenvectors are given by
  $$
  \begin{align}
  \sigma_{y}|v_1\rangle &= \begin{pmatrix}
  0 & -i\\ i &0
  \end{pmatrix}\begin{pmatrix}
  a \\ b
  \end{pmatrix} = \begin{pmatrix}
  a \\ b
  \end{pmatrix} \iff |v_1\rangle = \frac{1}{\sqrt{2}}\begin{pmatrix}
  1 \\ i
  \end{pmatrix} \tag{7a}\\
  
  \sigma_{y}|v_2\rangle &= \begin{pmatrix}
  0 & -i\\ i &0
  \end{pmatrix}\begin{pmatrix}
  c \\ d
  \end{pmatrix} = -\begin{pmatrix}
  c \\ d
  \end{pmatrix} \iff |v_2\rangle = \frac{1}{\sqrt{2}}\begin{pmatrix}
  1 \\ -i
  \end{pmatrix}\tag{7b}
  \end{align}
  $$
  The coefficient $1/\sqrt{2}$ is to normalized the eigenvector. From the eigenvalues and eigenvectors, we can find that the diagonalizing matrix $D$​ is
  $$
  D = \frac{1}{\sqrt{2}}\begin{pmatrix}
  1 & 1 \\ i & -i
  \end{pmatrix} \iff D^{-1} = \frac{1}{\sqrt{2}}\begin{pmatrix}
  1 & -i \\ 1 & i
  \end{pmatrix}\tag{8}
  $$
  and thus
  $$
  \sigma_y = \begin{pmatrix}
  0 & -i\\ i &0
  \end{pmatrix} = \frac{1}{2}\begin{pmatrix}
  1 & 1 \\ i & -i
  \end{pmatrix}\begin{pmatrix}
  1 & 0 \\ 0 & -1
  \end{pmatrix}\begin{pmatrix}
  1 & -i \\ 1 & i
  \end{pmatrix}  = D\Lambda D^{-1}\tag{9}
  $$
  
* For $\sigma_y$​, the eigenvalue $\lambda$​ is the solution of the following equation,
  $$
  |\sigma_{z} - \lambda I|= \begin{vmatrix}
  1-\lambda & 0 \\ 0 & -1-\lambda 
  \end{vmatrix} = \lambda^2 - 1 = 0 \iff \lambda = \pm 1\tag{10}
  $$
  The corresponding eigenvectors are given by
  $$
  \begin{align}
  \sigma_{z}|v_1\rangle &= \begin{pmatrix}
  1 & 0\\ 0 & -1
  \end{pmatrix}\begin{pmatrix}
  a \\ b
  \end{pmatrix} = \begin{pmatrix}
  a \\ b
  \end{pmatrix} \iff |v_1\rangle = \begin{pmatrix}
  1 \\ 0
  \end{pmatrix} \tag{11a}\\
  
  \sigma_{z}|v_2\rangle &= \begin{pmatrix}
  1 & 0\\ 0 & -1
  \end{pmatrix}\begin{pmatrix}
  c \\ d
  \end{pmatrix} = -\begin{pmatrix}
  c \\ d
  \end{pmatrix} \iff |v_2\rangle = \begin{pmatrix}
  0 \\ 1
  \end{pmatrix}\tag{11b}
  \end{align}
  $$
  The coefficient $1/\sqrt{2}$ is to normalized the eigenvector. From the eigenvalues and eigenvectors, we can find that the diagonalizing matrix $D$​ is
  $$
  D = \begin{pmatrix}
  1 & 0 \\ 0 & 1
  \end{pmatrix} \iff D^{-1} = \begin{pmatrix}
  1 & 0 \\ 0 & 1
  \end{pmatrix}\tag{12}
  $$
  and thus
  $$
  \sigma_z = \begin{pmatrix}
  1 & 0\\ 0 & -1
  \end{pmatrix} =\begin{pmatrix}
  1 & 0 \\ 0 & 1
  \end{pmatrix}\begin{pmatrix}
  1 & 0 \\ 0 & -1
  \end{pmatrix}\begin{pmatrix}
  1 & 0 \\ 0 & 1
  \end{pmatrix}  = D\Lambda D^{-1}\tag{13}
  $$

