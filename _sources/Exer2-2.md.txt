# Exercise 2.2

Suppose $V$​ is a vector space with basis vector $|v_1\rangle = |0\rangle$​ and $|v_2\rangle = |1\rangle $​, and $A: V\to V$​ is a linear operator. Since we have $A|0\rangle = |1\rangle$​ and $A|1\rangle = |0\rangle$​, according to eq. (2.12) in the book, we could find the matrix entries from 
$$
\begin{cases}
A|v_1\rangle = A|0\rangle = A_{11}|0\rangle + A_{21}|1\rangle = |1\rangle\\
A|v_2\rangle = A|1\rangle = A_{12}|0\rangle + A_{22}|1\rangle = |0\rangle\\
\end{cases} \tag{1}\label{1}
$$
From eq. $\eqref{1}$ we could conclude that 
$$
A = \begin{pmatrix}
A_{11} & A_{12} \\
A_{21} & A_{22} \\
\end{pmatrix} = \begin{pmatrix}
0 & 1 \\
1 & 0 \\
\end{pmatrix}\tag{2}
$$
Suppose we have a different basis of $V$ with 
$$
|+\rangle = \frac{|0\rangle + |1\rangle}{\sqrt{2}}, |-\rangle = \frac{|0\rangle - |1\rangle}{\sqrt{2}} \tag{3}\label{3}
$$
To check whether they are basis, we could do
$$
\begin{align}
\langle +|+\rangle &= \frac{\langle 0 | + \langle 1|}{\sqrt{2}}\cdot\frac{|0\rangle + |1\rangle}{\sqrt{2}} = \frac{\langle 0 |0\rangle + \langle 1|1\rangle}{2} = 1 \\
\langle +|-\rangle &= \frac{\langle 0 | + \langle 1|}{\sqrt{2}}\cdot\frac{|0\rangle - |1\rangle}{\sqrt{2}} = \frac{\langle 0 |0\rangle - \langle 1|1\rangle}{2} = 0 \\
\langle -|+\rangle &= \frac{\langle 0 | - \langle 1|}{\sqrt{2}}\cdot\frac{|0\rangle + |1\rangle}{\sqrt{2}} = \frac{\langle 0 |0\rangle - \langle 1|1\rangle}{2} = 0 \\
\end{align}\tag{4}\label{4}
$$
Then we could conclude from eq. $\eqref{4}$ that the basis defined in eq. $\eqref{3}$ is a valid orthonormal basis. Under the basis of eq. $\eqref{3}$, basis vectors $|0\rangle$ and $|1\rangle$ becomes
$$
|0\rangle = \frac{|+\rangle+|-\rangle}{\sqrt{2}}, |1\rangle = \frac{|+\rangle-|-\rangle}{\sqrt{2}}\tag{5}\label{5}
$$
From eq. $\eqref{5}$, eq. $\eqref{3}$ becomes
$$
\begin{dcases}
A|0\rangle = A\left(\frac{|+\rangle + |-\rangle }{\sqrt{2}}\right) = \frac{A|+\rangle + A|-\rangle }{\sqrt{2}} = |1\rangle = \frac{|+\rangle-|-\rangle}{\sqrt{2}}\\
A|1\rangle = A\left(\frac{|+\rangle - |-\rangle }{\sqrt{2}}\right) = \frac{A|+\rangle - A|-\rangle }{\sqrt{2}} = |0\rangle = \frac{|+\rangle+|-\rangle}{\sqrt{2}}\\
\end{dcases} \tag{6}\label{6}
$$
From eq. $\eqref{6}$ we could find that 
$$
\begin{cases}
A|+\rangle = |+\rangle \\
A|-\rangle = -|-\rangle
\end{cases} \tag{7}
$$
Using similar method with eq. $\eqref{1}$, we obtain
$$
\begin{cases}
A|v_1\rangle = A|+\rangle = A_{11}|+\rangle + A_{21}|-\rangle = |+\rangle\\
A|v_2\rangle = A|-\rangle = A_{12}|+\rangle + A_{22}|-\rangle = -|-\rangle\\
\end{cases}\tag{8}
$$
Thus, the matrix representation of $A$ in basis $|+\rangle$ and $|-\rangle$ becomes
$$
A = \begin{pmatrix}
A_{11} & A_{12} \\
A_{21} & A_{22} \\
\end{pmatrix} = \begin{pmatrix}
1 & 0 \\
0 & -1 \\
\end{pmatrix}\tag{9}
$$
Then under basis $|+\rangle$ and $|-\rangle$, the matrix representation of $A$ is different. 