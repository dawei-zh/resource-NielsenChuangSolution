# Exercise 10.6

Consider an arbitrary encoded logical qubit $|\psi_L\rangle$ of Shor's code as 

$$
|\psi_L\rangle = \alpha |0_L\rangle  + \beta |1_L\rangle
$$(eqn:10.6.1)

where 

$$
\begin{align}
|0_L\rangle &= \frac{(|000\rangle + |111\rangle)(|000\rangle + |111\rangle)(|000\rangle + |111\rangle)}{2\sqrt{2}}\\
|1_L\rangle &= \frac{(|000\rangle - |111\rangle)(|000\rangle - |111\rangle)(|000\rangle - |111\rangle)}{2\sqrt{2}}
\end{align}
$$(eqn:10.6.2)

Consider a phase flip error on any of first three qubits, since $Z|0\rangle = |0\rangle$ and $Z|1\rangle = -|1\rangle$, we will have noisy $|0_L\rangle$ and $|1_L\rangle$ state as

$$
\begin{align}
|0_L\rangle &\to \frac{(|000\rangle - |111\rangle)(|000\rangle + |111\rangle)(|000\rangle + |111\rangle)}{2\sqrt{2}}\\
|1_L\rangle &\to \frac{(|000\rangle + |111\rangle)(|000\rangle - |111\rangle)(|000\rangle - |111\rangle)}{2\sqrt{2}}
\end{align}
$$(eqn:10.6.3)

Then apply $Z_{1}Z_{2}Z_{3}$ to noisy states, we have

$$
\begin{align}
 &\frac{Z_{1}Z_{2}Z_{3}(|000\rangle + |111\rangle)(|000\rangle + |111\rangle)(|000\rangle + |111\rangle)}{2\sqrt{2}} \\
 &= \frac{(|000\rangle + |111\rangle)(|000\rangle + |111\rangle)(|000\rangle + |111\rangle)}{2\sqrt{2}}=|0_L\rangle \\
 &\frac{Z_{1}Z_{2}Z_{3}(|000\rangle - |111\rangle)(|000\rangle - |111\rangle)(|000\rangle - |111\rangle)}{2\sqrt{2}} \\
 &= \frac{(|000\rangle - |111\rangle)(|000\rangle - |111\rangle)(|000\rangle - |111\rangle)}{2\sqrt{2}}=|1_L\rangle
\end{align}
$$(eqn:10.6.4)

Therefore, applying $Z_{1}Z_{2}Z_{3}$ to noisy state recover noisy $|0_L\rangle$ and $|1_L\rangle$ state from a phase flip error on any of the first three qubits, and it can naturally recover a phase flip error on any of the first three qubits of arbitrary state $|\psi\rangle = \alpha |0_L\rangle + \beta |1_L\rangle$.