## Exercise 2.17

In this exercise we need to prove
$$
\text{A normal matrix is Hermitian} \iff \text{A normal matrix has real eigenvalues}\tag{1}
$$

---

To check whether a Hermitian operator $A$ as normal operator has real eigenvalues (from the left to the right), we first notice that any normal operator is diagonalizable, so could write down the diagonal representation of normal operator $A$, 
$$
A = \sum_{i}\lambda_i|i\rangle\langle i|\tag{2}\label{2}
$$
where $\lambda_i$ is eigenvalue of $A$ and $|i\rangle$ is corresponding eigenvector of $\lambda_i$. Note that $A$ is also Hermitian, it means that 
$$
A = A^{\dagger} \iff \sum_{i}\lambda_i|i\rangle\langle i| = \left(\sum_{i}\lambda_i|i\rangle\langle i|\right)^{\dagger} = \sum_{i}\lambda^{*}_i|i\rangle\langle i|\tag{3}\label{3}
$$
where $\lambda^*_i$ is the conjugate of $\lambda_i$. From eq. $\eqref{3}$ we could conclude that $\lambda_i = \lambda^*_i$ and thus $A$ has real eigenvalues if $A$ is a normal operator and Hermitian operator. 

---

To check whether a normal operator $A$ that has real eigenvalues is a Hermitian operator (from the right to the left), since any normal operator is diagonalizable, we could still have
$$
A = \sum_{i}\lambda_i|i\rangle\langle i|\tag{4}\label{4}
$$
From eq. $\eqref{4}$ we could directly calculate $A^{\dagger}$ as
$$
A^{\dagger} = \left(\sum_{i}\lambda_i|i\rangle\langle i|\right)^{\dagger} = \sum_{i}\lambda^{*}_i|i\rangle\langle i| =\sum_{i}\lambda_i|i\rangle\langle i| = A \tag{5}\label{5}
$$
where $\lambda^*_i$ is the conjugate of $\lambda_i$. From eq. $\eqref{5}$ we could conclude that $A=A^{\dagger}$ and thus $A$ is a Hermitian operator if $A$ is a normal operator with all eigenvalues as real. 
