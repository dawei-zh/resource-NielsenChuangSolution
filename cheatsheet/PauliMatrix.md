#### Properties about the Pauli matrices

$$
\sigma_x = \begin{pmatrix}
0 & 1\\ 1 &0
\end{pmatrix},\sigma_y = \begin{pmatrix}
0 & -i\\ i &0
\end{pmatrix},\sigma_z = \begin{pmatrix}
1 & 0\\ 0 &-1
\end{pmatrix}
$$

Here are several important properties of Pauli matrices:

* All pauli matrices are hermitian, $\sigma_x = \sigma_x^{\dagger},\sigma_y = \sigma_y^{\dagger},\sigma_z = \sigma_z^{\dagger} $.

* All pauli matrices are unitary, $\sigma_x^{\dagger}\sigma_x = \sigma_y^{\dagger}\sigma_y = \sigma_z^{\dagger}\sigma_z = \mathbf{I}$.

* The eigenvectors and eigenvalues of Pauli matrices are shown below. 

  * For $\sigma_x$, the eigenvalues $\lambda_1=1$ and $\lambda_2=-1$, their corresponding eigenvectors are
    $$
    |v_1\rangle = \frac{1}{\sqrt{2}}\begin{pmatrix}
    1 \\ 1
    \end{pmatrix}, |v_2\rangle = \frac{1}{\sqrt{2}}\begin{pmatrix}
    1\\ -1
    \end{pmatrix}
    $$

  * For $\sigma_y$, the eigenvalues $\lambda_1=1$ and $\lambda_2=-1$, their corresponding eigenvectors are
    $$
    |v_1\rangle =  \frac{1}{\sqrt{2}}\begin{pmatrix}
    1 \\ i
    \end{pmatrix}, |v_2\rangle =  \frac{1}{\sqrt{2}}\begin{pmatrix}
    1\\ -i
    \end{pmatrix}
    $$

  * For $\sigma_z$, the eigenvalues $\lambda_1=1$ and $\lambda_2=-1$, their corresponding eigenvectors are
    $$
    |v_1\rangle = \begin{pmatrix}
    1 \\ 0
    \end{pmatrix}, |v_2\rangle = \begin{pmatrix}
    0\\ 1
    \end{pmatrix}
    $$

* The commutation rules for Pauli matrices are given by

  * Pauli matrices commute with themselves, 
    $$
    [\sigma_x, \sigma_x] = [\sigma_y, \sigma_y] = [\sigma_z, \sigma_z] = 0
    $$
     

  * One Pauli matrix does not commute with another Pauli matrix,
    $$
    [\sigma_x, \sigma_y] = 2i\sigma_z, [\sigma_y, \sigma_z] = 2i\sigma_x, [\sigma_z, \sigma_x] = 2i\sigma_y
    $$

* The anticommutation rules for Pauli matrices are given by

  * Pauli matrices do not anticommute with themselves,
    $$
    \{X, X\} = \{Y, Y\} = \{Z, Z\} = 2I
    $$

  * One Pauli matrix anticommute with another Pauli matrix, 
    $$
    \{X, Y\} = \{Y, X\} = \{Y, Z\} =  \{Z, Y\} = \{Z, X\} = \{X, Z\} =0
    $$

* For state $|0\rangle$ and $|1\rangle$, 
  $$
  \begin{cases}
  \sigma_{x}|0\rangle = |1\rangle,& \sigma_{x}|1\rangle = |0\rangle\\
  \sigma_{y}|0\rangle = i|1\rangle,& \sigma_{y}|1\rangle = -i|0\rangle\\
  \sigma_{z}|0\rangle = |0\rangle,& \sigma_{z}|1\rangle = -|1\rangle
  \end{cases}
  $$

---

#### Properties of raising/lowering Pauli matrix

$$
\sigma_{+} = |1\rangle\langle 0 | = \begin{pmatrix}
0&0\\1&0
\end{pmatrix}, \sigma_{-} = |0\rangle\langle 1 | = \begin{pmatrix}
0&1\\0&0
\end{pmatrix}
$$

* Both matrices are hermitian

* Both matrices are not unitary

* For state $|0\rangle$ and $|1\rangle$​, 
  $$
  \begin{cases}
  \sigma_{+}|0\rangle = |1\rangle,& \sigma_{+}|1\rangle = 0\\
  \sigma_{-}|0\rangle = 0,& \sigma_{-}|1\rangle = |0\rangle
  \end{cases}
  $$
  
  



