# Exercise 4.20

Consider a $\rm CNOT$ gate with first qubit as control and second qubit as target, we could write the $\rm CNOT$ gate in the following form, 

$$
{\rm CNOT} = |0\rangle\langle 0|\otimes I + |1\rangle\langle 1| \otimes X
$$(eqn:4.20.1)

Similarly, we should have ${\rm CNOT} = I\otimes |0\rangle\langle 0| +X\otimes  |1\rangle\langle 1| $ for $\rm CNOT$ gate with second qubit as control and first qubit as target. For Hadamard gate, we have the following properties, 

$$
H|0\rangle = \frac{|0\rangle+|1\rangle}{\sqrt{2}} = |+\rangle, H|1\rangle = \frac{|0\rangle-|1\rangle}{\sqrt{2}} = |-\rangle, HXH = Z
$$(eqn:4.20.2)

With eq. {eq}`eqn:4.20.1` and eq. {eq}`eqn:4.20.2`, we could write the circuit shown in the question as unitary operator $U$, and 

$$
\begin{align}
U &= (H\otimes H)(|0\rangle\langle 0|\otimes I + |1\rangle\langle 1| \otimes X)(H\otimes H) \\
&= H|0\rangle\langle 0|H\otimes I + H|1\rangle\langle 1|H \otimes HXH \\
&= |+\rangle\langle +|\otimes I + |-\rangle\langle -| \otimes Z 
\end{align}
$$(eqn:4.20.3)

Note that for identity, $X$ gate and $Z$ gate, we could write them in the spectral decomposition form,  

$$
\begin{align}
I &= |0\rangle\langle 0 | + |1\rangle \langle 1| \\
&= |+\rangle \langle + | + |-\rangle\langle -| \\
X &= |+\rangle\langle + | - |-\rangle \langle -| \\
Z &= |0\rangle\langle 0 | - |1\rangle \langle 1| \\
\end{align}
$$(eqn:4.20.4)

Then we could use eq. {eq}`eqn:4.20.4` and re-write eq. {eq}`eqn:4.20.3` as

$$
\begin{align}
U =& |+\rangle\langle +|\otimes I + |-\rangle\langle -| \otimes Z \\
=&|+\rangle\langle +|\otimes |0\rangle\langle 0 | +|+\rangle\langle +|\otimes |1\rangle\langle 1 |  \\
&+ |-\rangle\langle -|\otimes |0\rangle\langle 0 |  -|-\rangle\langle -|\otimes |1\rangle\langle 1 |  \\
=& I\otimes |0\rangle\langle 0| + X \otimes |1\rangle\langle 1|
\end{align}
$$(eqn:4.20.5)

We could find that the circuit shown in the problem is equivalent to $\rm CNOT$ gate with **second qubit as control** and **first qubit as target**. Then the circuit identity is proved. 

---

In order to verify equation $(4.24)-(4.27)$ in the book for $\rm CNOT$ gate with **first qubit as control** and **second qubit as target**, we could <u>make use of the circuit identity</u> and the properties of Hadamard gate in eq. {eq}`eqn:4.20.2`. 

For $\rm CNOT(|+\rangle\otimes |+\rangle)$, according to eq. {eq}`eqn:4.20.2` and eq. {eq}`eqn:4.20.3`, we could have

$$
\begin{align}
{\rm CNOT}(|+\rangle\otimes |+\rangle) &= {\rm CNOT}(H\otimes H)(|0\rangle\otimes |0\rangle) \\
&= (H\otimes H)^{\dagger}(H\otimes H){\rm CNOT}(H\otimes H)(|0\rangle\otimes |0\rangle) \\
&= (H\otimes H)(H\otimes H){\rm CNOT}(H\otimes H)(|0\rangle\otimes |0\rangle) \\
&= (H\otimes H)U(|0\rangle\otimes |0\rangle)
\end{align}
$$(eqn:4.20.6)

where we have $(H\otimes H)^{\dagger} = H^{\dagger}\otimes H^{\dagger} = H\otimes H$. It means that we could use the result of $U$ to calculate $\rm CNOT(|+\rangle\otimes |+\rangle)$, that is, 

$$
\begin{align}
{\rm CNOT}(|+\rangle\otimes |+\rangle) &=(H\otimes H)U(|0\rangle\otimes |0\rangle) \\
&=(H\otimes H)(I\otimes |0\rangle\langle 0| + X \otimes |1\rangle\langle 1|)(|0\rangle\otimes |0\rangle)\\ 
&= (H\otimes H)(I|0\rangle\otimes |0\rangle\langle 0|0\rangle + X|0\rangle \otimes |1\rangle\langle 1|0\rangle) \\
&= (H\otimes H)(|0\rangle\otimes |0\rangle) = |+\rangle\otimes |+\rangle
\end{align}
$$(eqn:4.20.7)

For $\rm CNOT(|-\rangle\otimes |+\rangle)$, we have

$$
begin{align}
{\rm CNOT}(|-\rangle\otimes |+\rangle) &=(H\otimes H)U(|1\rangle\otimes |0\rangle) \\
&= (H\otimes H)(I\otimes |0\rangle\langle 0| + X \otimes |1\rangle\langle 1|)(|1\rangle\otimes |0\rangle) \\
&= (H\otimes H)(I|1\rangle\otimes |0\rangle\langle 0|0\rangle + X|1\rangle \otimes |1\rangle\langle 1|0\rangle) \\
&= (H\otimes H)(|1\rangle\otimes |0\rangle) = |-\rangle\otimes |+\rangle
\end{align}
$$(eqn:4.20.8)

For $\rm CNOT(|+\rangle\otimes |-\rangle)$, we have

$$
\begin{align}
{\rm CNOT}(|+\rangle\otimes |-\rangle) &=(H\otimes H)U(|0\rangle\otimes |1\rangle)\\
&=(H\otimes H)(I\otimes |0\rangle\langle 0| + X \otimes |1\rangle\langle 1|)(|0\rangle\otimes |1\rangle) \\
&= (H\otimes H)(I|0\rangle\otimes |0\rangle\langle 0|1\rangle + X|0\rangle \otimes |1\rangle\langle 1|1\rangle) \\
&= (H\otimes H)(|1\rangle\otimes |1\rangle) = |-\rangle\otimes |-\rangle
\end{align}
$$(eqn:4.20.9)

For $\rm CNOT(|-\rangle\otimes |-\rangle)$, we have

$$
\begin{align}
{\rm CNOT}(|-\rangle\otimes |-\rangle) &=(H\otimes H)U(|1\rangle\otimes |1\rangle)\\
&= (H\otimes H)(I\otimes |0\rangle\langle 0| + X \otimes |1\rangle\langle 1|)(|1\rangle\otimes |1\rangle) \\
&= (H\otimes H)(I|1\rangle\otimes |0\rangle\langle 0|1\rangle + X|1\rangle \otimes |1\rangle\langle 1|1\rangle) \\
&= (H\otimes H)(|0\rangle\otimes |1\rangle) = |+\rangle\otimes |-\rangle
\end{align}
$$(eqn:4.20.10)

