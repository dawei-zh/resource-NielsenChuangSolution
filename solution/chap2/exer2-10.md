## Exercise 2.10

Suppose $V$ is an inner product space with orthonormal basis $|v_i\rangle$, and $A = |v_j\rangle\langle v_k|$ is an operator in $V$. From eq. (2.25) in the book, we could conclude that the outer product representation for a linear operator $A:V\to V$ is given by
$$
A = \sum_{m,n}\langle v_n |A|v_m\rangle |v_n\rangle\langle v_m| \tag{1}\label{1}
$$
where $|v_m\rangle$ is the $m-$th basis for vector space $V$ and $\langle v_n|A|v_m\rangle$ is the matrix element $A_{nm}$ of $A$. Since $A = |v_j\rangle\langle v_k|$, from eq. $\eqref{1}$ we should have 
$$
\langle v_j |A|v_k\rangle = A_{nm}=\begin{cases}
1 & n=j, m=k \\
0 & {\rm otherwise}
\end{cases}\tag{2}
$$
Thus, the matrix representation for operator $|v_j\rangle\langle v_k|$ is a matrix with only the element in the $j-$th row and $k-$th column as $1$, and all other elements are $0$
