## Exercise 2.19

The Pauli matrices are given by
$$
I= \begin{pmatrix}
1 & 0\\ 0 & 1
\end{pmatrix}, X = \begin{pmatrix}
0 & 1\\ 1 &0
\end{pmatrix},Y = \begin{pmatrix}
0 & -i\\ i &0
\end{pmatrix},Z = \begin{pmatrix}
1 & 0\\ 0 &-1
\end{pmatrix} \tag{1}\label{1}
$$
The Hermitian conjugate of Pauli matrices can be directly obtained by
$$
I^{\dagger}= \begin{pmatrix}
1 & 0\\ 0 & 1
\end{pmatrix}, X^{\dagger} = \begin{pmatrix}
0 & 1\\ 1 &0
\end{pmatrix},Y^{\dagger} = \begin{pmatrix}
0 & -i\\ i &0
\end{pmatrix},Z^{\dagger} = \begin{pmatrix}
1 & 0\\ 0 &-1
\end{pmatrix} \tag{2}\label{2}
$$
Compare eq. $\eqref{1}$ and eq. $\eqref{2}$ we could conclude that $I=I^{\dagger}, X=X^{\dagger}, Y=Y^{\dagger}, Z=Z^{\dagger}$​ and $I, X, Y, Z$ are all Hermitian operators. Meanwhile, we could calculate 
$$
\begin{align}
I^{\dagger}I &= II^{\dagger} = \begin{pmatrix}
1 & 0\\ 0 & 1
\end{pmatrix}\begin{pmatrix}
1 & 0\\ 0 & 1
\end{pmatrix} = \begin{pmatrix}
1 & 0\\ 0 & 1
\end{pmatrix} = I \\
X^{\dagger}X &= XX^{\dagger} = \begin{pmatrix}
0 & 1\\ 1 &0
\end{pmatrix}\begin{pmatrix}
0 & 1\\ 1 &0
\end{pmatrix} = \begin{pmatrix}
1 & 0\\ 0 & 1
\end{pmatrix} = I \\
Y^{\dagger}Y &= YY^{\dagger} = \begin{pmatrix}
0 & -i\\ i &0
\end{pmatrix}\begin{pmatrix}
0 & -i\\ i &0
\end{pmatrix} = \begin{pmatrix}
1 & 0\\ 0 & 1
\end{pmatrix} = I \\
Z^{\dagger}Z &= ZZ^{\dagger} = \begin{pmatrix}
1 & 0\\ 0 &-1
\end{pmatrix}\begin{pmatrix}
1 & 0\\ 0 &-1
\end{pmatrix} = \begin{pmatrix}
1 & 0\\ 0 & 1
\end{pmatrix} = I \\
\end{align}\tag{3}\label{3}
$$
Note that we have $I^{\dagger}I = II^{\dagger}$, $X^{\dagger}X = XX^{\dagger}$, $Y^{\dagger}Y = YY^{\dagger}$ and $Z^{\dagger}Z = ZZ^{\dagger}$ since $I, X, Y, Z$ are Hermitian operators. From eq. $\eqref{3}$ we could conclude that, $I, X, Y, Z$ are all unitary matrices. 
