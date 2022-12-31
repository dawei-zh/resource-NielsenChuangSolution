# Exercise 10.5

Consider the 9-qubits Shor's code with codeword as

$$
\begin{align}
|0_L\rangle = \frac{(|000\rangle + |111\rangle)(|000\rangle + |111\rangle)(|000\rangle + |111\rangle)}{2\sqrt{2}} \\
|1_L\rangle = \frac{(|000\rangle - |111\rangle)(|000\rangle - |111\rangle)(|000\rangle - |111\rangle)}{2\sqrt{2}} \\
\end{align} 
$$(eqn:10.5.1)

We can encode an arbitrary state in the form $|\psi\rangle = a|0_L\rangle + b|1_L\rangle$. 

## No error occur

If there is no phase flip error occur, we have an arbitrary state as $|\psi\rangle = a|{0}_L\rangle + b|{1}_L\rangle$. Since $X|0\rangle = |1\rangle$ and $X|1\rangle = |0\rangle$ we have 

$$
\begin{align}
&\frac{X_1X_2X_3X_4X_5X_6(|000\rangle + |111\rangle)(|000\rangle + |111\rangle)(|000\rangle + |111\rangle)}{2\sqrt{2}}\\
=& \frac{(|111\rangle + |000\rangle)(|111\rangle + |000\rangle)(|000\rangle + |111\rangle)}{2\sqrt{2}} = |{0}_L\rangle\\
&\frac{X_1X_2X_3X_4X_5X_6(|000\rangle - |111\rangle)(|000\rangle - |1111\rangle)(|000\rangle - |111\rangle)}{2\sqrt{2}}\\
=& \frac{(|111\rangle - |000\rangle)(|111\rangle - |000\rangle)(|000\rangle - |111\rangle)}{2\sqrt{2}} = |{1}_L\rangle\\
\end{align}
$$(eqn:10.5.2)

Then measuring $X_1X_2X_3X_4X_5X_6$ for $|\psi\rangle = a|{0}_L\rangle + b|{1}_L\rangle$, the outcome is $+1$, and the probability of getting $_1$ is

$$
\begin{align}
p(m_{123456}=-1) &= \langle \psi|(X_1X_2X_3X_4X_5X_6)^{\dagger}X_1X_2X_3X_4X_5X_6|\psi\rangle\\
&= (a^*\langle {0}_L|+b^*\langle {1}_L|)(a| {0}_L\rangle+b| {1}_L\rangle)  = 1
\end{align}
$$(eqn:10.5.3)

The post-measurement state is then

$$
\frac{X_1X_2X_3X_4X_5X_6|\psi\rangle}{p(m_{123456}=-1)} = a|{0}_L\rangle+b|{1}_L\rangle
$$(eqn:10.5.4)

After measuring $X_1X_2X_3X_4X_5X_6$ we perform the measurement $X_4X_5X_6X_7X_8X_9$, and we have 

$$
X_4X_5X_6X_7X_8X_9|{0}_L\rangle = 
\frac{(|000\rangle + |111\rangle)(|111\rangle + |000\rangle)(|111\rangle + |000\rangle)}{2\sqrt{2}} = |{0}_L\rangle\\

X_4X_5X_6X_7X_8X_9|{1}_L\rangle =  \frac{(|000\rangle - |111\rangle)(|111\rangle - |000\rangle)(|111\rangle - |000\rangle)}{2\sqrt{2}} = |{1}_L\rangle
$$(eqn:10.5.5)

Then measuring $X_4X_5X_6X_7X_8X_9$ for $|\psi\rangle = a|{0}_L\rangle + b|{1}_L\rangle$, the outcome is $+1$, and the probability of getting $+1$ is

$$
\begin{align}
p(m_{456789}=+1) &= \langle \psi|(X_4X_5X_6X_7X_8X_9)^{\dagger}X_4X_5X_6X_7X_8X_9|\psi\rangle\\
&= (a^*\langle {0}_L|+b^*\langle {1}_L|)(a| {0}_L\rangle+b| {1}_L\rangle) = 1
\end{align}
$$(eqn:10.5.6)

The post-measurement state is then

$$
\frac{X_4X_5X_6X_7X_8X_9|\psi\rangle}{p(m_{456789}=+1)} = a|{0}_L\rangle+b|{1}_L\rangle
$$(eqn:10.5.7)

## Phase flip at first three qubits set

If there is a phase flip error in the first three qubit, the state $|0_L\rangle$ and $|1_L\rangle$ becomes 

$$
\begin{align}
|0_L\rangle \to |\tilde{0}_L\rangle = \frac{(|000\rangle - |111\rangle)(|000\rangle + |111\rangle)(|000\rangle + |111\rangle)}{2\sqrt{2}} \\
|1_L\rangle \to  |\tilde{1}_L\rangle = \frac{(|000\rangle + |111\rangle)(|000\rangle - |111\rangle)(|000\rangle - |111\rangle)}{2\sqrt{2}} \\
\end{align}
$$(eqn:10.5.8)

and the arbitrary state becomes $|\psi\rangle = a|\tilde{0}_L\rangle + b|\tilde{1}_L\rangle$. Since $X|0\rangle = |1\rangle$ and $X|1\rangle = |0\rangle$ we have 

$$
\begin{align}
&\frac{X_1X_2X_3X_4X_5X_6(|000\rangle - |111\rangle)(|000\rangle + |111\rangle)(|000\rangle + |111\rangle)}{2\sqrt{2}}\\
=& \frac{(|111\rangle - |000\rangle)(|111\rangle + |000\rangle)(|000\rangle + |111\rangle)}{2\sqrt{2}} = -|\tilde{0}_L\rangle\\
&\frac{X_1X_2X_3X_4X_5X_6(|000\rangle + |111\rangle)(|000\rangle - |1111\rangle)(|000\rangle - |111\rangle)}{2\sqrt{2}}\\
=& \frac{(|111\rangle + |000\rangle)(|111\rangle - |000\rangle)(|000\rangle - |111\rangle)}{2\sqrt{2}} = -|\tilde{1}_L\rangle\\
\end{align}
$$(eqn:10.5.9)

Then measuring $X_1X_2X_3X_4X_5X_6$ for $|\psi\rangle = a|\tilde{0}_L\rangle + b|\tilde{1}_L\rangle$, the outcome is $-1$, and the probability of getting $-1$ is

$$
\begin{align}
p(m_{123456}=-1) &= \langle \psi|(X_1X_2X_3X_4X_5X_6)^{\dagger}X_1X_2X_3X_4X_5X_6|\psi\rangle\\
&= (a^*\langle \tilde{0}_L|+b^*\langle \tilde{1}_L|)(a| \tilde{0}_L\rangle+b| \tilde{1}_L\rangle)  = 1
\end{align}
$$(eqn:10.5.10)

The post-measurement state is then

$$
\frac{X_1X_2X_3X_4X_5X_6|\psi\rangle}{p(m_{123456}=-1)} = -a|\tilde{0}_L\rangle-b|\tilde{1}_L\rangle
$$(eqn:10.5.11)

After measuring $X_1X_2X_3X_4X_5X_6$ we perform the measurement $X_4X_5X_6X_7X_8X_9$, and we have 

$$
X_4X_5X_6X_7X_8X_9|\tilde{0}_L\rangle = 
\frac{(|000\rangle - |111\rangle)(|111\rangle + |000\rangle)(|111\rangle + |000\rangle)}{2\sqrt{2}} = |\tilde{0}_L\rangle\\

X_4X_5X_6X_7X_8X_9|\tilde{1}_L\rangle =  \frac{(|000\rangle + |111\rangle)(|111\rangle - |000\rangle)(|111\rangle - |000\rangle)}{2\sqrt{2}} = |\tilde{1}_L\rangle
$$(eqn:10.5.12)

Then measuring $X_4X_5X_6X_7X_8X_9$ for $|\psi\rangle = -a|\tilde{0}_L\rangle - b|\tilde{1}_L\rangle$, the outcome is $+1$, and the probability of getting $+1$ is

$$
\begin{align}
p(m_{456789}=+1) &= \langle \psi|(X_4X_5X_6X_7X_8X_9)^{\dagger}X_4X_5X_6X_7X_8X_9|\psi\rangle\\
&= (-a^*\langle \tilde{0}_L|-b^*\langle \tilde{1}_L|)(-a| \tilde{0}_L\rangle-b| \tilde{1}_L\rangle) = 1
\end{align}
$$(eqn:10.5.13)

The post-measurement state is then

$$
\frac{X_4X_5X_6X_7X_8X_9|\psi\rangle}{p(m_{456789}=+1)} = -a|\tilde{0}_L\rangle-b|\tilde{1}_L\rangle
$$(eqn:10.5.14)

## Phase flip at second three qubits set

If there is a phase flip error in the second three qubit, the state $|0_L\rangle$ and $|1_L\rangle$ becomes 

$$
\begin{align}
|0_L\rangle \to |\tilde{0}_L\rangle = \frac{(|000\rangle + |111\rangle)(|000\rangle - |111\rangle)(|000\rangle + |111\rangle)}{2\sqrt{2}} \\
|1_L\rangle \to  |\tilde{1}_L\rangle = \frac{(|000\rangle - |111\rangle)(|000\rangle + |111\rangle)(|000\rangle - |111\rangle)}{2\sqrt{2}} \\
\end{align}
$$(eqn:10.5.15)

and the arbitrary state becomes $|\psi\rangle = a|\tilde{0}_L\rangle + b|\tilde{1}_L\rangle$. Since $X|0\rangle = |1\rangle$ and $X|1\rangle = |0\rangle$ we have 

$$
\begin{align}
&\frac{X_1X_2X_3X_4X_5X_6(|000\rangle + |111\rangle)(|000\rangle - |111\rangle)(|000\rangle + |111\rangle)}{2\sqrt{2}}\\
=& \frac{(|111\rangle + |000\rangle)(|111\rangle - |000\rangle)(|000\rangle + |111\rangle)}{2\sqrt{2}} = -|\tilde{0}_L\rangle\\
&\frac{X_1X_2X_3X_4X_5X_6(|000\rangle - |111\rangle)(|000\rangle + |111\rangle)(|000\rangle - |111\rangle)}{2\sqrt{2}}\\
=& \frac{(|111\rangle - |000\rangle)(|111\rangle + |000\rangle)(|000\rangle - |111\rangle)}{2\sqrt{2}} = -|\tilde{1}_L\rangle\\
\end{align}
$$(eqn:10.5.16)

Then measuring $X_1X_2X_3X_4X_5X_6$ for $|\psi\rangle = a|\tilde{0}_L\rangle + b|\tilde{1}_L\rangle$, the outcome is $-1$, and the probability of getting $-1$ is

$$
\begin{align}
p(m_{123456}=-1) &= \langle \psi|(X_1X_2X_3X_4X_5X_6)^{\dagger}X_1X_2X_3X_4X_5X_6|\psi\rangle\\
&= (a^*\langle \tilde{0}_L|+b^*\langle \tilde{1}_L|)(a| \tilde{0}_L\rangle+b| \tilde{1}_L\rangle) = 1
\end{align}
$$(eqn:10.5.17)

The post-measurement state is then

$$
\frac{X_1X_2X_3X_4X_5X_6|\psi\rangle}{p(m_{123456}=-1)} = -a|\tilde{0}_L\rangle-b|\tilde{1}_L\rangle
$$(eqn:10.5.18)

After measuring $X_1X_2X_3X_4X_5X_6$ we perform the measurement $X_4X_5X_6X_7X_8X_9$, and we have 

$$
X_4X_5X_6X_7X_8X_9|\tilde{0}_L\rangle = 
\frac{(|000\rangle + |111\rangle)(|111\rangle - |000\rangle)(|111\rangle + |000\rangle)}{2\sqrt{2}} = -|\tilde{0}_L\rangle\\

X_4X_5X_6X_7X_8X_9|\tilde{1}_L\rangle =  \frac{(|000\rangle - |111\rangle)(|111\rangle + |000\rangle)(|111\rangle - |000\rangle)}{2\sqrt{2}} = -|\tilde{1}_L\rangle
$$

Then measuring $X_4X_5X_6X_7X_8X_9$ for $|\psi\rangle = -a|\tilde{0}_L\rangle - b|\tilde{1}_L\rangle$, the outcome is $-1$, and the probability of getting $-1$ is

$$
\begin{align}
p(m_{456789}=-1) &= \langle \psi|(X_4X_5X_6X_7X_8X_9)^{\dagger}X_4X_5X_6X_7X_8X_9|\psi\rangle\\
&= (-a^*\langle \tilde{0}_L|-b^*\langle \tilde{1}_L|)(-a| \tilde{0}_L\rangle-b| \tilde{1}_L\rangle) = 1
\end{align}
$$(eqn:10.5.19)

The post-measurement state is then

$$
\frac{X_4X_5X_6X_7X_8X_9|\psi\rangle}{p(m_{456789}=-1)} = a|\tilde{0}_L\rangle+b|\tilde{1}_L\rangle
$$(eqn:10.5.20)

## Phase flip at third three qubit set

If there is a phase flip error in the second three qubit, the state $|0_L\rangle$ and $|1_L\rangle$ becomes 

$$
\begin{align}
|0_L\rangle \to |\tilde{0}_L\rangle = \frac{(|000\rangle + |111\rangle)(|000\rangle + |111\rangle)(|000\rangle - |111\rangle)}{2\sqrt{2}} \\
|1_L\rangle \to  |\tilde{1}_L\rangle = \frac{(|000\rangle - |111\rangle)(|000\rangle - |111\rangle)(|000\rangle + |111\rangle)}{2\sqrt{2}} \\
\end{align}
$$(eqn:10.5.21)

and the arbitrary state becomes $|\psi\rangle = a|\tilde{0}_L\rangle + b|\tilde{1}_L\rangle$. Since $X|0\rangle = |1\rangle$ and $X|1\rangle = |0\rangle$ we have 

$$
\begin{align}
&\frac{X_1X_2X_3X_4X_5X_6(|000\rangle + |111\rangle)(|000\rangle + |111\rangle)(|000\rangle - |111\rangle)}{2\sqrt{2}}\\
=& \frac{(|111\rangle + |000\rangle)(|111\rangle + |000\rangle)(|000\rangle - |111\rangle)}{2\sqrt{2}} = |\tilde{0}_L\rangle\\
&\frac{X_1X_2X_3X_4X_5X_6(|000\rangle - |111\rangle)(|000\rangle - |111\rangle)(|000\rangle +|111\rangle)}{2\sqrt{2}}\\
=& \frac{(|111\rangle - |000\rangle)(|111\rangle - |000\rangle)(|000\rangle + |111\rangle)}{2\sqrt{2}} = |\tilde{1}_L\rangle\\
\end{align}
$$(eqn:10.5.22)

Then measuring $X_1X_2X_3X_4X_5X_6$ for $|\psi\rangle = a|\tilde{0}_L\rangle + b|\tilde{1}_L\rangle$, the outcome is $+1$, and the probability of getting $+1$ is

$$
\begin{align}
p(m_{123456}=+1) &= \langle \psi|(X_1X_2X_3X_4X_5X_6)^{\dagger}X_1X_2X_3X_4X_5X_6|\psi\rangle\\
&= (a^*\langle \tilde{0}_L|+b^*\langle \tilde{1}_L|)(a| \tilde{0}_L\rangle+b| \tilde{1}_L\rangle)  = 1
\end{align}
$$(eqn:10.5.23)

The post-measurement state is then

$$
\frac{X_1X_2X_3X_4X_5X_6|\psi\rangle}{p(m_{123456}=+1)} = a|\tilde{0}_L\rangle+b|\tilde{1}_L\rangle
$$(eqn:10.5.24)

After measuring $X_1X_2X_3X_4X_5X_6$ we perform the measurement $X_4X_5X_6X_7X_8X_9$, and we have 

$$
X_4X_5X_6X_7X_8X_9|\tilde{0}_L\rangle = 
\frac{(|000\rangle + |111\rangle)(|111\rangle + |000\rangle)(|111\rangle - |000\rangle)}{2\sqrt{2}} = -|\tilde{0}_L\rangle\\

X_4X_5X_6X_7X_8X_9|\tilde{1}_L\rangle =  \frac{(|000\rangle - |111\rangle)(|111\rangle - |000\rangle)(|111\rangle + |000\rangle)}{2\sqrt{2}} = -|\tilde{1}_L\rangle
$$(eqn:10.5.25)

Then measuring $X_4X_5X_6X_7X_8X_9$ for $|\psi\rangle = a|\tilde{0}_L\rangle + b|\tilde{1}_L\rangle$, the outcome is $-1$, and the probability of getting $-1$ is

$$
\begin{align}
p(m_{456789}=-1) &= \langle \psi|(X_4X_5X_6X_7X_8X_9)^{\dagger}X_4X_5X_6X_7X_8X_9|\psi\rangle\\
&= (a^*\langle \tilde{0}_L|+b^*\langle \tilde{1}_L|)(a| \tilde{0}_L\rangle+b| \tilde{1}_L\rangle) = 1
\end{align}
$$(eqn:10.5.26)

The post-measurement state is then

$$
\frac{X_4X_5X_6X_7X_8X_9|\psi\rangle}{p(m_{456789}=-1)} = -a|\tilde{0}_L\rangle-b|\tilde{1}_L\rangle
$$(eqn:10.5.27)

---

From above calculation we know that, 

* If there is no error, we measure $+1$ for $X_1X_2X_3X_4X_5X_6$ and $+1$ for $X_4X_5X_6X_7X_8X_9$
* If there is a phase flip error at the first three qubit set, we measure $-1$ for $X_1X_2X_3X_4X_5X_6$ and $+1$ for $X_4X_5X_6X_7X_8X_9$
* If there is a phase flip error at the second three qubit set, we measure $-1$ for $X_1X_2X_3X_4X_5X_6$ and $-1$ for $X_4X_5X_6X_7X_8X_9$
* If there is a phase flip error at the third three qubit set, we measure $+1$ for $X_1X_2X_3X_4X_5X_6$ and $-1$ for $X_4X_5X_6X_7X_8X_9$

From above summary, we can easily see that, the syndrome measurement for detecting phase flip errors in the Shor code corresponds to measuring $X_1X_2X_3X_4X_5X_6$ and $X_4X_5X_6X_7X_8X_9$