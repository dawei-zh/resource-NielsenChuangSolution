## Exercise 2.53

The Hadamard gate is defined as
$$
H = \frac{1}{\sqrt{2}}\begin{pmatrix}
1 & 1 \\ 
1 & -1 
\end{pmatrix}\tag{1}
$$
We could calculate the eigenvalue of $H$ via solving
$$
|H - \lambda I|= \begin{vmatrix}
1/\sqrt{2}-\lambda & 1/\sqrt{2} \\
1/\sqrt{2}& -1/\sqrt{2}-\lambda 
\end{vmatrix} = \lambda^2 - 1 = 0 \iff \lambda = \pm 1 \tag{2}
$$
The corresponding normalized eigenvectors are given by
$$
\begin{align}
H|v_1\rangle &= \frac{1}{\sqrt{2}}\begin{pmatrix}
1 & 1 \\ 
1 & -1 
\end{pmatrix}\begin{pmatrix}
a \\ b
\end{pmatrix} = \begin{pmatrix}
a \\ b
\end{pmatrix} \iff |v_1\rangle = \frac{1}{\sqrt{4-2\sqrt{2}}}\begin{pmatrix}
1 \\ \sqrt{2}-1
\end{pmatrix} \tag{3a}\label{3a}\\

H|v_2\rangle &= \frac{1}{\sqrt{2}}\begin{pmatrix}
1 & 1 \\ 
1 & -1 
\end{pmatrix}\begin{pmatrix}
c \\ d
\end{pmatrix} = -\begin{pmatrix}
c \\ d
\end{pmatrix} \iff |v_2\rangle = \frac{1}{\sqrt{4+2\sqrt{2}}}\begin{pmatrix}
1 \\ -\sqrt{2}-1
\end{pmatrix}\tag{3b}\label{3b}
\end{align}
$$
Since $4\pm\sqrt{2} = 2\sqrt{2}(\sqrt{2}\pm1)$, we could simplify eq. $\eqref{3a}-\eqref{3b}$ and obtain the normalized eigenvector of Hadamard gate, 
$$
|v_1\rangle = \begin{pmatrix}
\frac{1}{\sqrt{4-2\sqrt{2}}} \\ \frac{1}{\sqrt{2\sqrt{2}}}
\end{pmatrix}, |v_2\rangle = \begin{pmatrix}
\frac{1}{\sqrt{4+2\sqrt{2}}} \\ -\frac{1}{\sqrt{2\sqrt{2}}}
\end{pmatrix}\tag{4}
$$
