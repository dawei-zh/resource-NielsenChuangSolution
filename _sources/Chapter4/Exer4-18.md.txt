# Exercise 4.18

The control-$Z$​ operation on the left can be expressed as follow, 

$$
{\rm control-}Z_1: |0\rangle\langle 0| \otimes I + |1\rangle\langle 1| \otimes Z \tag{1} \label{1}
$$(eqn:4.18.1)

The control-$Z$ operation on the right can be expressed as follow, 

$$
{\rm control-}Z_2: I\otimes |0\rangle\langle 0| + Z\otimes |1\rangle\langle 1|\tag{2}\label{2}
$$(eqn:4.18.2)

If we write eq. {eq}`eqn:4.18.1` in the matrix form, we have

$$
\begin{align}
{\rm control-}Z_1&: \begin{pmatrix}
1 & 0 \\ 0 & 0
\end{pmatrix} \otimes \begin{pmatrix}
1 & 0 \\ 0 & 1
\end{pmatrix} + \begin{pmatrix}
0 & 0 \\ 0 & 1
\end{pmatrix} \otimes \begin{pmatrix}
1 & 0 \\ 0 & -1
\end{pmatrix} \\
&= \begin{pmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 
\end{pmatrix} + \begin{pmatrix}
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & -1 
\end{pmatrix} \\
&= \begin{pmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & -1 
\end{pmatrix}
\end{align}\tag{3}\label{3}
$$(eqn:4.18.3)

If we write eq. {eq}`eqn:4.18.2` in the matrix form, we have

$$
\begin{align}
{\rm control-}Z_2&:  \begin{pmatrix}
1 & 0 \\ 0 & 1
\end{pmatrix} \otimes \begin{pmatrix}
1 & 0 \\ 0 & 0
\end{pmatrix} +  \begin{pmatrix}
1 & 0 \\ 0 & -1
\end{pmatrix}\otimes\begin{pmatrix}
0 & 0 \\ 0 & 1
\end{pmatrix}  \\
&= \begin{pmatrix}
1 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 0 
\end{pmatrix} + \begin{pmatrix}
0 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & -1 
\end{pmatrix} \\
&= \begin{pmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & -1 
\end{pmatrix}
\end{align}\tag{4}\label{4}
$$(eqn:4.18.4)

Compare eq. {eq}`eqn:4.18.3` and eq. {eq}`eqn:4.18.4`, we could conclude that the ${\rm control-}Z_1 = {\rm control-}Z_2$. 