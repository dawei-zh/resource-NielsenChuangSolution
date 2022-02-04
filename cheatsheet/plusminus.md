## About the $|+\rangle$ or $|-\rangle$ states

The Hadamard gate is given by
$$
H= \frac{1}{\sqrt{2}}\begin{pmatrix}
1 & 1 \\ 1 & -1
\end{pmatrix}
$$
Here are several important properties of Hadmard gate:

* Hadmard gate is hermitian, $H^{\dagger} = H$

* Hadmard gate is unitary, $H^{\dagger}H = HH = I$, or 
  $$
  HH = \frac{1}{2}\begin{pmatrix}
  1 & 1 \\ 1 & -1
  \end{pmatrix}\begin{pmatrix}
  1 & 1 \\ 1 & -1
  \end{pmatrix} = \frac{1}{2}\begin{pmatrix}
  2 & 0 \\ 0 & 2
  \end{pmatrix} = I
  $$

* For state $|0\rangle$ and $|1\rangle$, 
  $$
  H|0\rangle = |+\rangle,H|1\rangle = |-\rangle, H|+\rangle = |0\rangle, H|-\rangle = |1\rangle
  $$
  or, 

$$
\begin{align}
H|0\rangle &= \frac{1}{\sqrt{2}}\begin{pmatrix}
1 & 1 \\ 1 & -1
\end{pmatrix}\begin{pmatrix}
1 \\0
\end{pmatrix} = \frac{1}{\sqrt{2}}\begin{pmatrix}
1 \\1
\end{pmatrix} = |+\rangle  \\

H|1\rangle &= \frac{1}{\sqrt{2}}\begin{pmatrix}
1 & 1 \\ 1 & -1
\end{pmatrix}\begin{pmatrix}
0 \\ 1
\end{pmatrix} = \frac{1}{\sqrt{2}}\begin{pmatrix}
1 \\ -1
\end{pmatrix} = |-\rangle \\

H|+\rangle &= \frac{1}{2}\begin{pmatrix}
1 & 1 \\ 1 & -1
\end{pmatrix}\begin{pmatrix}
1 \\ 1
\end{pmatrix} = \frac{1}{2}\begin{pmatrix}
2 \\ 0
\end{pmatrix} = |0\rangle  \\

H|-\rangle &= \frac{1}{2}\begin{pmatrix}
1 & 1 \\ 1 & -1
\end{pmatrix}\begin{pmatrix}
1 \\ -1
\end{pmatrix} = \frac{1}{2}\begin{pmatrix}
0 \\ 2
\end{pmatrix} = |1\rangle
\end{align}
$$
For a random state $|\psi\rangle = \alpha |0\rangle + \beta |1\rangle$, we have
$$
\begin{align}
H|\psi\rangle &= \frac{1}{\sqrt{2}}\begin{pmatrix}
1 & 1 \\ 1 & -1
\end{pmatrix}\begin{pmatrix}
\alpha \\ \beta
\end{pmatrix} \\
&= \frac{1}{\sqrt{2}}\begin{pmatrix}
\alpha + \beta \\
\alpha - \beta
\end{pmatrix}\\
&= \frac{1}{\sqrt{2}}(\alpha + \beta)|0\rangle + \frac{1}{\sqrt{2}}(\alpha- \beta )|1\rangle \\
&=\alpha \frac{1}{\sqrt{2}}(|0\rangle + |1\rangle) + \beta \frac{1}{\sqrt{2}}(|0\rangle - |1\rangle) \\
&= \alpha |+\rangle + \beta |-\rangle
\end{align}
$$
For a random state $|\psi\rangle = \alpha |000\rangle + \beta|111\rangle$, 
$$
\begin{align}
H_1H_2H_3 |\psi\rangle &= H_1H_2H_3 (\alpha |0\rangle_{1} \otimes |0\rangle_{2} \otimes |0\rangle_{3} + \beta |1\rangle_{1} \otimes |1\rangle_{2} \otimes |1\rangle_{3})\\
&= \alpha (H_1|0\rangle_{1} \otimes H_2|0\rangle_{2} \otimes H_3|0\rangle_{3}) + \beta (H_1|1\rangle_{1} \otimes H_2|1\rangle_{2} \otimes H_3|1\rangle_{3})\\
&= \alpha|+++\rangle + \beta|---\rangle
\end{align}
$$
Note that $|+++\rangle$ is not the state$|000\rangle + |111\rangle /\sqrt{2}$. For CNOT gate, 
$$
{\rm CNOT} = \begin{pmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 0 & 1 \\
0 & 0 & 1 & 0 \\
\end{pmatrix}
$$
We have
$$
\begin{align}
{\rm CX}|+0\rangle &= {\rm CX}\frac{1}{\sqrt{2}}(|00\rangle + |10\rangle ) \\
&= \frac{1}{\sqrt{2}}(|00\rangle + |11\rangle )
\end{align}
$$
That is,
$$
\begin{align}
{\rm CX}|++\rangle &= |++\rangle \\
{\rm CX}|+-\rangle &= |--\rangle \\
{\rm CX}|-+\rangle &= |-+\rangle \\
{\rm CX}|--\rangle &= |+-\rangle 
\end{align}
$$
Note that the control bit is the first digit. Also,
$$
\begin{align}
{\rm CX}|++\rangle &= {\rm CX}\frac{1}{\sqrt{2}}(|0+\rangle + |1+\rangle ) \\
&={\rm CX} \frac{1}{2}(|00\rangle + |01\rangle + |10\rangle + |11\rangle )\\
&= \frac{1}{2}(|00\rangle + |01\rangle + |10\rangle + |11\rangle )\\
&= |++\rangle
\end{align}
$$
And
$$
\begin{align}
{\rm CX}|+-\rangle &= {\rm CX}\frac{1}{\sqrt{2}}(|0-\rangle + |1-\rangle ) \\
&={\rm CX} \frac{1}{2}(|00\rangle - |01\rangle + |10\rangle - |11\rangle )\\
&= \frac{1}{2}(|00\rangle - |01\rangle - |10\rangle + |11\rangle )\\
&= |--\rangle
\end{align}
$$
and 
$$
\begin{align}
{\rm CX}|-+\rangle &= {\rm CX}\frac{1}{\sqrt{2}}(|0+\rangle - |1+\rangle ) \\
&={\rm CX} \frac{1}{2}(|00\rangle + |01\rangle - |10\rangle - |11\rangle )\\
&= \frac{1}{2}(|00\rangle + |01\rangle - |10\rangle - |11\rangle )\\
&= |-+\rangle
\end{align}
$$
and 
$$
\begin{align}
{\rm CX}|--\rangle &= {\rm CX}\frac{1}{\sqrt{2}}(|0-\rangle - |1-\rangle ) \\
&={\rm CX} \frac{1}{2}(|00\rangle - |01\rangle - |10\rangle + |11\rangle )\\
&= \frac{1}{2}(|00\rangle - |01\rangle + |10\rangle - |11\rangle )\\
&= |+-\rangle
\end{align}
$$

---

We have for $|+\rangle$ and $|-\rangle$,
$$
\begin{align}
Z|+\rangle &= \frac{1}{\sqrt{2}}(Z|0\rangle + Z|1\rangle)= \frac{1}{\sqrt{2}}(|0\rangle - |1\rangle) = |-\rangle \\
Z|-\rangle &= \frac{1}{\sqrt{2}}(Z|0\rangle - Z|1\rangle)= \frac{1}{\sqrt{2}}(|0\rangle + |1\rangle) = |+\rangle \\
\end{align}
$$

#### Hadamard Gate

The Hadamard gate is given by
$$
H = \frac{1}{\sqrt{2}}\begin{pmatrix}
1 & 1 \\
1 & -1
\end{pmatrix}
$$

* For state $|0\rangle$ and $|1\rangle$,
  $$
  \begin{align}
  H|0\rangle &= \frac{1}{\sqrt{2}}(|0\rangle + |1\rangle) = |+\rangle \\
  H|1\rangle &= \frac{1}{\sqrt{2}}(|0\rangle - |1\rangle) = |-\rangle 
  \end{align}
  $$

* We can construct Pauli gate with Hadamard gate,
  $$
  X = HZH
  $$

  
