# Exercise 10.3

## For $|\psi\rangle =  a|000\rangle + b|111\rangle$ 

Consider three qubit bit flip code $|0_{L}\rangle = |000\rangle$ and $|1_L\rangle = |111\rangle$, if we measure $Z_1Z_2$ of an arbitrary noiseless state $|\psi\rangle = a|0_L\rangle + b|1_L\rangle =  a|000\rangle + b|111\rangle$, the outcome should be eigenvalue of $Z_1Z_2$​​. Since $Z|0\rangle = |0\rangle$ and $Z|1\rangle = -|1\rangle$, we have

$$
Z_1Z_2 |000\rangle = |000\rangle, Z_1Z_2 |111\rangle = |111\rangle
$$(eqn:10.3.1)

and 

$$
Z_1Z_2 |\psi\rangle = Z_1Z_2(a|000\rangle + b|111\rangle) = a|000\rangle + b|111\rangle = |\psi\rangle
$$(eqn:10.3.2)

Therefore, $|\psi\rangle$ is the eigenstate of $Z_1Z_2$ and the outcome of measuring $Z_1Z_2$ for $|\psi\rangle$ is $+1$. The probability of getting $+1$ is then obtained by

$$
\begin{align}
{\rm Pr}(m_{12}=+1) =& \langle \psi|(Z_1Z_2)^{\dagger}Z_1Z_2|\psi\rangle  \\
=& (a^*\langle 000| + b^*\langle 111| )(a| 000\rangle + b| 111\rangle  ) = 1
\end{align}
$$(eqn:10.3.3)

After measuring $Z_1Z_2$ we obtain post-measurement state $Z_1Z_2|\psi\rangle/P(m_{12}=1) = |\psi\rangle$. Note that 

$$
Z_2Z_3 |\psi\rangle = Z_2Z_3(a|000\rangle + b|111\rangle) = a|000\rangle + b|111\rangle = |\psi\rangle
$$(eqn:10.3.4)

it means that the outcome of measuring $Z_2Z_3$ for $|\psi\rangle$ is $+1$, and similarly, the probability of getting $+1$ is 

$$
\begin{align}
{\rm Pr}(m_{23}=+1) =& \langle \psi|(Z_2Z_3)^{\dagger}Z_2Z_3|\psi\rangle  \\
=& (a^*\langle 000| + b^*\langle 111| )(a| 000\rangle + b| 111\rangle  ) = 1
\end{align}
$$(eqn:10.3.5)

and we obtain post-measurement state $Z_2Z_3|\psi\rangle/P(m_{23}=1) = |\psi\rangle$.

Now we measure arbitrary state $|\psi\rangle = a|0_L\rangle + b|1_L\rangle =  a|000\rangle + b|111\rangle$ with projector $P = P_0 + P_1 + P_2 + P_3$, where 

$$
\begin{align}
P_0 = |000\rangle\langle 000| + |111\rangle\langle 111|\\
P_1 = |100\rangle\langle 100| + |011\rangle\langle 011|\\
P_2 = |010\rangle\langle 010| + |101\rangle\langle 101|\\
P_3 = |001\rangle\langle 001| + |110\rangle\langle 110|\\
\end{align} 
$$(eqn:10.3.6)

Note that $P_0, P_1, P_2, P_3$ are all Hermitian operators, so the measurement outcome of them are their eigenvalues. Notice that $\langle \psi|P_{0}|\psi\rangle = 1$ and $\langle \psi|P_{1}|\psi\rangle = \langle \psi|P_{2}|\psi\rangle=\langle \psi|P_{3}|\psi\rangle=0$, so the probability of measuring $P$ is 

$$
\begin{align}
p =& \langle \psi|(P)^{\dagger}P|\psi\rangle  = \langle \psi|P_0|\psi\rangle = 1
\end{align}
$$(eqn:10.3.7)

and the post measurement state is

$$
\frac{P_0|\psi\rangle}{\langle \psi|P_{0}|\psi\rangle} = (|000\rangle\langle 000| + |111\rangle\langle 111|)(a|000\rangle + b|111\rangle) = a|000\rangle + b|111\rangle = |\psi\rangle
$$(eqn:10.3.8)

Thus, the probability of getting some measurement outcome is all $1$ for both measuring projectors and measuring $Z_1Z_2$ and $Z_2Z_3$, and the post-measurement state is the same as the post-measurement state after measuring $Z_1Z_2$ and $Z_2Z_3$. 

## For $|\psi\rangle =  a|100\rangle + b|011\rangle$

Consider a bit flip happen on the first qubit, if we measure $Z_1Z_2$ the outcome should be eigenvalue of $Z_1Z_2$​​. Since $Z|0\rangle = |0\rangle$ and $Z|1\rangle = -|1\rangle$, we have

$$
Z_1Z_2 |100\rangle = -|100\rangle, Z_1Z_2 |011\rangle = -|011\rangle
$$(eqn:10.3.9)

and

$$
Z_1Z_2 |\psi\rangle = Z_1Z_2(a|100\rangle + b|011\rangle) = -a|100\rangle - b|011\rangle = -|\psi\rangle
$$(eqn:10.3.10)

Therefore, $|\psi\rangle$ is the eigenstate of $Z_1Z_2$ and the outcome of measuring $Z_1Z_2$ for $|\psi\rangle$ is $-1$. The probability of getting $-1$ is then obtained by

$$
\begin{align}
{\rm Pr}(m_{12}=-1) =& \langle \psi|(Z_1Z_2)^{\dagger}Z_1Z_2|\psi\rangle  \\
=& (a^*\langle 100| + b^*\langle 011| )(a| 100\rangle + b| 011\rangle  )  = 1
\end{align}
$$(eqn:10.3.11)

After measuring $Z_1Z_2$ we obtain post-measurement state $Z_1Z_2|\psi\rangle/P(m_{12}=1) = -|\psi\rangle$. Note that

$$
-Z_2Z_3 |\psi\rangle = Z_2Z_3(-a|100\rangle - b|011\rangle) = -a|100\rangle - b|011\rangle = -|\psi\rangle
$$(eqn:10.3.12)

it means that the outcome of measuring $Z_2Z_3$ for $|\psi\rangle$ is $+1$, and the probability of getting $+1$ is 

$$
\begin{align}
{\rm Pr}(m_{23}=+1) =& \langle \psi|(Z_2Z_3)^{\dagger}Z_2Z_3|\psi\rangle  \\
=& (-a^*\langle 000| - b^*\langle 111| )(-a| 000\rangle - b| 111\rangle  ) = 1
\end{align}
$$(eqn:10.3.13)

and we obtain post-measurement state $Z_2Z_3|\psi\rangle/P(m_{23}=1) = -|\psi\rangle$.

Now we measure state $|\psi\rangle = a|100\rangle + b|011\rangle$ with projector $P = P_0 + P_1 + P_2 + P_3$. Notice that $\langle \psi|P_{1}|\psi\rangle = 1$ and $\langle \psi|P_{0}|\psi\rangle = \langle \psi|P_{2}|\psi\rangle=\langle \psi|P_{3}|\psi\rangle=0$, so the probability of measuring $P$ is 

$$
\begin{align}
p =& \langle \psi|(P)^{\dagger}P|\psi\rangle  = \langle \psi|P_1|\psi\rangle = 1
\end{align}
$$(eqn:10.3.14)

and the post measurement state is

$$
\frac{P_1|\psi\rangle}{\langle \psi|P_{1}|\psi\rangle} = (|100\rangle\langle 100| + |011\rangle\langle 011|)(a|100\rangle + b|011\rangle) = a|100\rangle + b|011\rangle = |\psi\rangle
$$(eqn:10.3.15)

Thus, the probability of getting some measurement outcome is all $1$ for both measuring projectors and measuring $Z_1Z_2$ and $Z_2Z_3$, and the post-measurement state is the same as the post-measurement state after measuring $Z_1Z_2$ and $Z_2Z_3$ up to a global phase. 

## For $|\psi\rangle =  a|010\rangle + b|101\rangle$

Consider a bit flip happen on the first qubit, if we measure $Z_1Z_2$ the outcome should be eigenvalue of $Z_1Z_2$​​. Since $Z|0\rangle = |0\rangle$ and $Z|1\rangle = -|1\rangle$, we have

$$
Z_1Z_2 |010\rangle = -|010\rangle, Z_1Z_2 |101\rangle = -|101\rangle
$$(eqn:10.3.16)

and

$$
Z_1Z_2 |\psi\rangle = Z_1Z_2(a|010\rangle + b|101\rangle) = -a|010\rangle - b|101\rangle = -|\psi\rangle
$$(eqn:10.3.17)

Therefore, $|\psi\rangle$ is the eigenstate of $Z_1Z_2$ and the outcome of measuring $Z_1Z_2$ for $|\psi\rangle$ is $-1$. The probability of getting $-1$ is then obtained by

$$
\begin{align}
{\rm Pr}(m_{12}=-1) =& \langle \psi|(Z_1Z_2)^{\dagger}Z_1Z_2|\psi\rangle  \\
=& (a^*\langle 010| + b^*\langle 101| )(a| 010\rangle + b| 101\rangle  )  = 1
\end{align}
$$(eqn:10.3.18)

After measuring $Z_1Z_2$ we obtain post-measurement state $Z_1Z_2|\psi\rangle/P(m_{12}=1) = -|\psi\rangle$. Note that

$$
-Z_2Z_3 |\psi\rangle = Z_2Z_3(-a|010\rangle - b|101\rangle) = a|010\rangle + b|101\rangle = |\psi\rangle
$$(eqn:10.3.19)

it means that the outcome of measuring $Z_2Z_3$ for $|\psi\rangle$ is $-1$, and the probability of getting $-1$ is 

$$
\begin{align}
{\rm Pr}(m_{23}=-1) =& \langle \psi|(Z_2Z_3)^{\dagger}Z_2Z_3|\psi\rangle  \\
=& (-a^*\langle 000| - b^*\langle 111| )(-a| 000\rangle - b| 111\rangle  ) = 1
\end{align}
$$(eqn:10.3.20)

and we obtain post-measurement state $-Z_2Z_3|\psi\rangle/P(m_{23}=1) = |\psi\rangle$.

Now we measure state $|\psi\rangle = a|010\rangle + b|101\rangle$ with projector $P = P_0 + P_1 + P_2 + P_3$. Notice that $\langle \psi|P_{2}|\psi\rangle = 1$ and $\langle \psi|P_{0}|\psi\rangle = \langle \psi|P_{1}|\psi\rangle=\langle \psi|P_{3}|\psi\rangle=0$, so the probability of measuring $P$ is 

$$
\begin{align}
p =& \langle \psi|(P)^{\dagger}P|\psi\rangle  = \langle \psi|P_2|\psi\rangle = 1
\end{align}
$$(eqn:10.3.21)

and the post measurement state is

$$
\frac{P_2|\psi\rangle}{\langle \psi|P_{2}|\psi\rangle} = (|010\rangle\langle 010| + |101\rangle\langle 101|)(a|010\rangle + b|101\rangle) = a|010\rangle + b|101\rangle = |\psi\rangle
$$(eqn:10.3.22)

Thus, the probability of getting some measurement outcome is all $1$ for both measuring projectors and measuring $Z_1Z_2$ and $Z_2Z_3$, and the post-measurement state is the same as the post-measurement state after measuring $Z_1Z_2$ and $Z_2Z_3$.

## For $|\psi\rangle =  a|001\rangle + b|110\rangle$

Consider a bit flip happen on the first qubit, if we measure $Z_1Z_2$ the outcome should be eigenvalue of $Z_1Z_2$​​. Since $Z|0\rangle = |0\rangle$ and $Z|1\rangle = -|1\rangle$, we have

$$
Z_1Z_2 |001\rangle = |001\rangle, Z_1Z_2 |110\rangle = |110\rangle
$$(eqn:10.3.23)

and

$$
Z_1Z_2 |\psi\rangle = Z_1Z_2(a|001\rangle + b|110\rangle) = a|001\rangle +b|110\rangle = |\psi\rangle
$$(eqn:10.3.24)

Therefore, $|\psi\rangle$ is the eigenstate of $Z_1Z_2$ and the outcome of measuring $Z_1Z_2$ for $|\psi\rangle$ is $+1$. The probability of getting $+1$ is then obtained by

$$
\begin{align}
{\rm Pr}(m_{12}=+1) =& \langle \psi|(Z_1Z_2)^{\dagger}Z_1Z_2|\psi\rangle  \\
=& (a^*\langle 001| + b^*\langle 110| )(a| 001\rangle + b| 110\rangle  )  = 1
\end{align}
$$(eqn:10.3.25)

After measuring $Z_1Z_2$ we obtain post-measurement state $Z_1Z_2|\psi\rangle/P(m_{12}=1) =|\psi\rangle$. Note that

$$
Z_2Z_3 |\psi\rangle = Z_2Z_3(a|001\rangle + b|110\rangle) = -a|001\rangle - b|110\rangle = -|\psi\rangle
$$(eqn:10.3.26)

it means that the outcome of measuring $Z_2Z_3$ for $|\psi\rangle$ is $-1$, and the probability of getting $-1$ is 

$$
\begin{align}
{\rm Pr}(m_{23}=-1) =& \langle \psi|(Z_2Z_3)^{\dagger}Z_2Z_3|\psi\rangle  \\
=& (a^*\langle 000| + b^*\langle 111| )(a| 000\rangle +b| 111\rangle  ) = 1
\end{align}
$$(eqn:10.3.27)

and we obtain post-measurement state $Z_2Z_3|\psi\rangle/P(m_{23}=1) = -|\psi\rangle$.

Now we measure state $|\psi\rangle = a|001\rangle + b|110\rangle$ with projector $P = P_0 + P_1 + P_2 + P_3$. Notice that $\langle \psi|P_{3}|\psi\rangle = 1$ and $\langle \psi|P_{0}|\psi\rangle = \langle \psi|P_{1}|\psi\rangle=\langle \psi|P_{2}|\psi\rangle=0$, so the probability of measuring $P$ is 

$$
\begin{align}
p =& \langle \psi|(P)^{\dagger}P|\psi\rangle  = \langle \psi|P_3|\psi\rangle = 1
\end{align}
$$(eqn:10.3.28)

and the post measurement state is

$$
\frac{P_3|\psi\rangle}{\langle \psi|P_{3}|\psi\rangle} = (|001\rangle\langle 001| + |110\rangle\langle 110|)(a|001\rangle + b|110\rangle) = a|001\rangle + b|110\rangle = |\psi\rangle
$$(eqn:10.3.29)

Thus, the probability of getting some measurement outcome is all $1$ for both measuring projectors and measuring $Z_1Z_2$ and $Z_2Z_3$, and the post-measurement state is the same as the post-measurement state after measuring $Z_1Z_2$ and $Z_2Z_3$ up to a global phase. 

---

From above calculation we know that, measuring $Z_1Z_2$ followed by $Z_2Z_3$ result in the same measurement statistics and post-measurement states as measuring the four projectors. 