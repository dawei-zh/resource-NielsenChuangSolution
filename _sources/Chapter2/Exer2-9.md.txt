# Exercise 2.9

Suppose $V$ is a vector space with basis vector $|v_1\rangle = |0\rangle$ and $|v_2\rangle = |1\rangle $, and Pauli operators are linear operator $V\to V$. From eq. (2.25) in the book, we could conclude that the outer product representation for a linear operator $A:V\to V$ is given by

$$
A = \sum_{i,j}\langle v_j |A|v_i\rangle |v_j\rangle\langle v_i| 
$$(eqn:2.9.1)

where $|v_i\rangle$ is the $i-$th basis for vector space $V$ and $\langle v_j|A|v_i\rangle$ is the matrix element $A_{ji}$ of $A$. According to eq. {eq}`eqn:2.9.1`​, for Pauli matrices $\sigma_0,\sigma_1,\sigma_2,\sigma_3$ shown below, 

$$
\sigma_0 = I = \begin{pmatrix}
1 & 0 \\ 0 & 1
\end{pmatrix}, \sigma_1 = X = \begin{pmatrix}
0 & 1 \\ 1 & 0
\end{pmatrix}, \sigma_2 = Y = \begin{pmatrix}
0 & -i \\ i & 0
\end{pmatrix}, \sigma_3 = Z = \begin{pmatrix}
1 & 0 \\ 0 & -1
\end{pmatrix} 
$$(eqn:2.9.2)

we have their corresponding outer product representation as 

$$
\begin{align}
\sigma_0 = I &= I_{11} |v_1\rangle\langle v_1| + I_{12} |v_1\rangle\langle v_2|+I_{21} |v_2\rangle\langle v_1|+I_{22} |v_2\rangle\langle v_2| \\
&=  |v_1\rangle\langle v_1| + |v_2\rangle\langle v_2| \\
&=  |0\rangle\langle 0| + |1\rangle\langle 1| \\
\end{align}
$$(eqn:2.9.3)

$$
\begin{align}
\sigma_1 = X &= X_{11} |v_1\rangle\langle v_1| + X_{12} |v_1\rangle\langle v_2|+X_{21} |v_2\rangle\langle v_1|+X_{22} |v_2\rangle\langle v_2| \\
&=  |v_1\rangle\langle v_2| + |v_2\rangle\langle v_1| \\
&=  |0\rangle\langle 1| + |1\rangle\langle 0| \\
\end{align}
$$(eqn:2.9.4)

$$
\begin{align}
\sigma_2 = Y &= Y_{11} |v_1\rangle\langle v_1| + Y_{12} |v_1\rangle\langle v_2|+Y_{21} |v_2\rangle\langle v_1|+Y_{22} |v_2\rangle\langle v_2| \\
&=  -i|v_1\rangle\langle v_2| + i|v_2\rangle\langle v_1| \\
&=  -i|0\rangle\langle 1| + i|1\rangle\langle 0| \\
\end{align}
$$(eqn:2.9.5)

$$
\begin{align}
\sigma_3 = Z &= Z_{11} |v_1\rangle\langle v_1| + Z_{12} |v_1\rangle\langle v_2|+Z_{21} |v_2\rangle\langle v_1|+Z_{22} |v_2\rangle\langle v_2| \\
&=  |v_1\rangle\langle v_1| - |v_2\rangle\langle v_2| \\
&=  |0\rangle\langle 0| - |1\rangle\langle 1| \\
\end{align}
$$(eqn:2.9.6)
