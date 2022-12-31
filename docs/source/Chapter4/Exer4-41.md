# Exercise 4.41

From the definition of Hadamard gate, we have

$$
H|0\rangle = |+\rangle = \frac{|0\rangle + |1\rangle}{\sqrt{2}}, H|1\rangle = |-\rangle =\frac{|0\rangle - |1\rangle}{\sqrt{2}}
$$(eqn:4.41.1)

 Given the input state $|00\psi\rangle$​, after two Hadamard gates in qubit $1$​ and qubit $2$​, we obtain 

$$
H_1H_2I_3 |00\psi\rangle = |++\psi\rangle = \frac{1}{2}(|00\psi\rangle + |01\psi\rangle +|10\psi\rangle +|11\psi\rangle )
$$(eqn:4.41.2)

where we use eq. {eq}`eqn:4.41.1` for calculation and the number $1,2,3$ denotes the number of qubit. For the first Toffoli gate, notice that it would only apply $X$ operation to the state with both first and second qubit as $|1\rangle$, then after the first Toffoli gate, we obtain

$$
{\rm Toffoli} |++\psi\rangle = \frac{1}{2}(|00\psi\rangle + |01\psi\rangle +|10\psi\rangle +I_1I_2X_3|11\psi\rangle )
$$(eqn:4.41.3)

The phase gate between two Toffoli gates only performs on the third qubit, then we have

$$
I_1I_2S_3({\rm Toffoli} |++\psi\rangle ) =\frac{1}{2}(S_3|00\psi\rangle + S_3|01\psi\rangle +S_3|10\psi\rangle +S_3X_3|11\psi\rangle )
$$(eqn:4.41.4)

The second Toffoli gate would also apply $X$ operation to the state with both first and second qubit as $|1\rangle$. Note that operations at the third qubit does not change the first and second qubit, so eq. {eq}`eqn:4.41.4` becomes

$$
{\rm Toffoli}(I_1I_2S_3){\rm Toffoli} |++\psi\rangle  =\frac{1}{2}(S_3|00\psi\rangle + S_3|01\psi\rangle +S_3|10\psi\rangle +X_3S_3X_3|11\psi\rangle )
$$(eqn:4.41.5)

The final two Hadamard gates change $|0\rangle$ to $|+\rangle$ and $|1\rangle$ to $|-\rangle$, so the final state is given by

$$
\begin{align}
\text{final state:}\;\frac{1}{2}(S_3|++\psi\rangle + S_3|+-\psi\rangle +S_3|-+\psi\rangle +X_3S_3X_3|--\psi\rangle )
\end{align}
$$(eqn:4.41.6)

Since we perform a $Z-$basis measurement on first and second qubit, we need to use eq. {eq}`eqn:4.41.1` to re-write eq. {eq}`eqn:4.41.6`. From eq. {eq}`eqn:4.41.1` we have

$$
\begin{align}
|++\rangle &=\frac{1}{2}(|0\rangle+|1\rangle)\otimes (|0\rangle+|1\rangle) \\
&=\frac{1}{2}(|00\rangle+|01\rangle+|10\rangle+|11\rangle)\\
|+-\rangle &=\frac{1}{2}(|0\rangle+|1\rangle)\otimes (|0\rangle-|1\rangle) \\
&= \frac{1}{2}(|00\rangle-|01\rangle+|10\rangle-|11\rangle)\\
|-+\rangle &=\frac{1}{2}(|0\rangle-|1\rangle)\otimes (|0\rangle+|1\rangle) \\
&= \frac{1}{2}(|00\rangle+|01\rangle-|10\rangle-|11\rangle)\\
|--\rangle &=\frac{1}{2}(|0\rangle-|1\rangle)\otimes (|0\rangle-|1\rangle) \\
&= \frac{1}{2}(|00\rangle-|01\rangle-|10\rangle+|11\rangle)\\
\end{align}
$$(eqn:4.41.7)

Thus, we could re-write the final state as

$$
\begin{align}
\text{final state:}\;&\frac{1}{2}(S_3|++\psi\rangle + S_3|+-\psi\rangle +S_3|-+\psi\rangle +X_3S_3X_3|--\psi\rangle ) \\
=&\frac{1}{4}[(|00\rangle+|01\rangle+|10\rangle+|11\rangle)\otimes S_3|\psi\rangle \\
&+ (|00\rangle-|01\rangle+|10\rangle-|11\rangle)\otimes S_3|\psi\rangle\\
&+(|00\rangle+|01\rangle-|10\rangle-|11\rangle)\otimes S_3|\psi\rangle \\
&+(|00\rangl-|01\rangle-|10\rangle+|11\rangle)\otimes X_3S_3X_3|\psi\rangle ] \\
=& \frac{1}{4}[(3|00\rangle+|01\rangle+|10\rangle-|11\rangle)\otimes S_3|\psi\rangle  +(|00\rangle-|01\rangle-|10\rangle+|11\rangle)\otimes X_3S_3X_3|\psi\rangle ] \\
=& |00\rangle\otimes \left(\frac{3}{4}S_3|\psi\rangle + \frac{1}{4}X_3S_3X_3|\psi\rangle\right) + \frac{1}{4}(|01\rangle+|10\rangle - |11\rangle) \otimes\left(S_3|\psi\rangle - X_3S_3X_3|\psi\rangle\right) 
\end{align}
$$(eqn:4.41.8)

---

## Measuring $00$

From the final state we know that, if the measurement of first two qubits are both $0$, the corresponding projector is $P = |00\rangle\langle 00|\otimes I$, and probability of getting both $0$ is

$$
\begin{align}
p_{00} =& \langle \text{final state}|P |\text{final state}\rangle  \\
=& \frac{1}{16}\langle \psi|(3S_3 + X_3S_3X_3)^{\dagger}(3S_3 + X_3S_3X_3)|\psi\rangle  \\
=& \frac{1}{16}\langle \psi|(3S^{\dagger}_3 + X^{\dagger}_3S^{\dagger}_3X^{\dagger}_3)(3S_3 + X_3S_3X_3)|\psi\rangle  \\
=& \frac{1}{16}\langle \psi|(9S^{\dagger}_3S_3 + 3S^{\dagger}_3 X_3S_3X_3+ 3X^{\dagger}_3S^{\dagger}_3X^{\dagger}_3S_3 + X^{\dagger}_3S^{\dagger}_3X^{\dagger}_3 X_3S_3X_3)|\psi\rangle \\
=& \frac{1}{16}\langle \psi|(9I + 3S^{\dagger}_3 X_3S_3X_3+ 3X^{\dagger}_3S^{\dagger}_3X^{\dagger}_3S_3 + I)|\psi\rangle
\end{align}
$$(eqn:4.41.9)

where we use the fact that $S$ and $X$ are unitary matrices and $X$ is Hermitian matrix. Note that 

$$
S^{\dagger}_3X_3S_3X_3 = \begin{pmatrix}
1 & 0 \\ 0 & -i
\end{pmatrix}\begin{pmatrix}
0 & 1 \\ 1 & 0
\end{pmatrix}\begin{pmatrix}
1 & 0 \\ 0 & i
\end{pmatrix}\begin{pmatrix}
0 & 1 \\ 1 & 0
\end{pmatrix} = \begin{pmatrix}
i & 0 \\ 0 & -i
\end{pmatrix}\\
X^{\dagger}_3S^{\dagger}_3X^{\dagger}_3S_3  = (S^{\dagger}_3X_3S_3X_3)^{\dagger} = \begin{pmatrix}
-i & 0 \\ 0 & i
\end{pmatrix}
$$(eqn:4.41.10)

Then we could obtain the probability of getting $00$ as 

$$
\begin{align}
p_{00} =& \frac{1}{16}\langle \psi|(9I + 3S^{\dagger}_3 X_3S_3X_3+ 3X^{\dagger}_3S^{\dagger}_3X^{\dagger}_3S_3 + I)|\psi\rangle = \frac{10}{16}= \frac{5}{8} \\
\end{align}
$$(eqn:4.41.11)

After measuring $00$, we will obtain the state at the third qubit as

$$
\frac{1}{\sqrt{p_{00}}}\left(\frac{3}{4}S_3|\psi\rangle + \frac{1}{4}X_3S_3X_3|\psi\rangle\right)
$$(eqn:4.41.12)

To see whether it is equivalent with adding a $R_z(\theta)$ on $|\psi\rangle$, we need to compute

$$
\begin{align}
3S_3 + X_3S_3X_3 &= 3\begin{pmatrix}
1 & 0 \\ 0 & i
\end{pmatrix} + \begin{pmatrix}
0 & 1 \\ 1 & 0
\end{pmatrix}\begin{pmatrix}
1 & 0 \\ 0 & i
\end{pmatrix}\begin{pmatrix}
0 & 1 \\ 1 & 0
\end{pmatrix} \\
&=\begin{pmatrix}
3+i & 0 \\ 0 & 3i+1
\end{pmatrix} = \begin{pmatrix}
(1+i)(2-i) & 0 \\ 0 & (1+i)(2+i)
\end{pmatrix} \\
&= (1+i) (2I - iZ)
\end{align}
$$(eqn:4.41.13)

Therefore, the post-measurement state becomes 

$$
\begin{align}
\frac{1}{\sqrt{p_{00}}}\left(\frac{3}{4}S_3|\psi\rangle + \frac{1}{4}X_3S_3X_3|\psi\rangle\right) &= \frac{1}{\sqrt{10}}(1+i) (2I - iZ) \\
&= e^{i\pi/4}\left(\frac{2}{\sqrt{5}}I - i\frac{1}{\sqrt{5}}Z\right)
\end{align}
$$(eqn:4.41.14)

From the definition of $R_{z}(\theta)$ gate, we know that 

$$
\cos\frac{\theta}{2} = \frac{2}{\sqrt{5}} \iff \cos\theta = 2\cos^2\frac{\theta}{2}-1 = \frac{3}{5}
$$(eqn:4.41.15)

---

## Not measuring $00$

From the final state we know that, if the measurement of first two qubits are not both $0$, the post-measurement state becomes 

$$
\begin{align}
\frac{1}{\sqrt{1-p_{00}}}\frac{1}{4}(S_3|\psi\rangle - X_3S_3X_3|\psi) &= \frac{1}{\sqrt{6}}(S_3|\psi\rangle - X_3S_3X_3|\psi)
\end{align}
$$(eqn:4.41.16)

Since 

$$
\begin{align}
S_3 - X_3S_3X_3 &= \begin{pmatrix}
1 & 0 \\ 0 & i
\end{pmatrix} - \begin{pmatrix}
0 & 1 \\ 1 & 0
\end{pmatrix}\begin{pmatrix}
1 & 0 \\ 0 & i
\end{pmatrix}\begin{pmatrix}
0 & 1 \\ 1 & 0
\end{pmatrix} \\
&=\begin{pmatrix}
1-i & 0 \\ 0 & i-1
\end{pmatrix} = (1-i) Z
\end{align}
$$(eqn:4.41.17)

the post measurement state is given by $(1-i)Z|\psi\rangle /\sqrt{6}$. 

If we want to repeat the whole process to obtain a precise $R_{z}(\theta)$ operation, we need to execute the circuit for many times, and add $Z$ gate to the third qubit if the measurement outcome is not $00$.  

