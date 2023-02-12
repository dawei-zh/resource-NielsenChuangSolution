# Exercise 2.51

The Hadamard gate is defined as

$$
H = \frac{1}{\sqrt{2}}\begin{pmatrix}
1 & 1 \\ 
1 & -1 
\end{pmatrix}
$$(eqn:2.51.1)

The Hermitian conjugate of $H$ is given by

$$
H^{\dagger} = \frac{1}{\sqrt{2}} \begin{pmatrix}
1 & 1 \\ 
1 & -1 
\end{pmatrix} = H
$$(eqn:2.51.2)

Thus, we could calculate 

$$
H^{\dagger}H =HH^{\dagger} = \frac{1}{2}\begin{pmatrix}
1 & 1 \\ 
1 & -1 
\end{pmatrix}\begin{pmatrix}
1 & 1 \\ 
1 & -1 
\end{pmatrix} = \frac{1}{2}\begin{pmatrix}
2 & 0 \\ 
0 & 2 
\end{pmatrix} = I 
$$(eqn:2.51.3)

Thus, we could conclude that the Hadamard gate H is unitary.