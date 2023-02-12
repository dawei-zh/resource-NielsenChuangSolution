# Exercise 4.13

The Hadmard gate, Pauli $X, Y$ and $Z$ gate are defined as

$$
H = \frac{1}{\sqrt{2}}\begin{pmatrix}
1 & 1 \\ 1 & -1
\end{pmatrix}, \,X = \begin{pmatrix}
0 & 1\\ 1 &0
\end{pmatrix},\,Y = \begin{pmatrix}
0 & -i\\ i &0
\end{pmatrix},\, Z = \begin{pmatrix}
1 & 0\\ 0 &-1
\end{pmatrix}
$$(eqn:4.13.1)

Thus, we have

$$
\begin{align}
HXH &=\frac{1}{2}\begin{pmatrix}
1 & 1 \\ 1 & -1
\end{pmatrix}\begin{pmatrix}
0 & 1\\ 1 &0
\end{pmatrix}\begin{pmatrix}
1 & 1 \\ 1 & -1
\end{pmatrix} \\
&=  \frac{1}{2}\begin{pmatrix}
1 & 1\\ -1 & 1
\end{pmatrix}\begin{pmatrix}
1 & 1 \\ 1 & -1
\end{pmatrix}\\
&= \frac{1}{2}\begin{pmatrix}
2 & 0 \\ 0 & -2
\end{pmatrix} = \begin{pmatrix}
1 & 0 \\ 0 & -1
\end{pmatrix} = Z
\end{align}
$$(eqn:4.13.2)

and

$$
\begin{align}
HYH &=\frac{1}{2}\begin{pmatrix}
1 & 1 \\ 1 & -1
\end{pmatrix}\begin{pmatrix}
0 & -i\\ i &0
\end{pmatrix}\begin{pmatrix}
1 & 1 \\ 1 & -1
\end{pmatrix} \\
&=  \frac{1}{2}\begin{pmatrix}
i & -i\\ -i & -i
\end{pmatrix}\begin{pmatrix}
1 & 1 \\ 1 & -1
\end{pmatrix}\\
&= \frac{1}{2}\begin{pmatrix}
0 & 2i \\ -2i & 0
\end{pmatrix} = \begin{pmatrix}
0 & i \\ -i & 0
\end{pmatrix} = -Y
\end{align}
$$(eqn:4.13.3)

Also

$$
\begin{align}
HZH &=\frac{1}{2}\begin{pmatrix}
1 & 1 \\ 1 & -1
\end{pmatrix}\begin{pmatrix}
1 & 0\\ 0 &-1
\end{pmatrix}\begin{pmatrix}
1 & 1 \\ 1 & -1
\end{pmatrix} \\
&=  \frac{1}{2}\begin{pmatrix}
1 & -1\\ 1 & 1
\end{pmatrix}\begin{pmatrix}
1 & 1 \\ 1 & -1
\end{pmatrix}\\
&= \frac{1}{2}\begin{pmatrix}
0 & 2 \\ 2 & 0
\end{pmatrix} = \begin{pmatrix}
0 & 1 \\ 1 & 0
\end{pmatrix} = X
\end{align}
$$(eqn:4.13.4)
