# Exercise 4.32

Consider a two qubit density matrix $\rho$​, if we perform projective measurement to the second qubit with operator

$$
P_0 = I\otimes |0\rangle\langle 0|, P_1 = I\otimes |1\rangle\langle 1|
$$(eqn:4.32.1)

The post-measurement state after measuring $P_0$ is $P_0\rho P_0/p_0$ where $p_0$ is the probability of measuring $0$, and the post-measurement state after measuring $P_1$ is $P_1\rho P_1/p_1$ where $p_1$ is the probability of measuring $1$. If an observer did not know the measurement result, then we will have probability $p_0$ to get $P_0\rho P_0/p_0$, and have probability $p_1$ to get $P_1\rho P_1/p_1$. So 

$$
\rho' =p_0\cdot \frac{P_0\rho P_0}{p_0} + p_1\cdot \frac{P_1\rho P_1}{p_1} = P_0\rho P_0+P_1\rho P_1 
$$(eqn:4.32.2)

We can calculate the partial trace for the first qubit as

$$
{\rm Tr}_{2}(\rho) = (I\otimes \langle 0|) \rho (I\otimes | 0\rangle ) + (I\otimes \langle 1|) \rho (I\otimes | 1\rangle )
$$(eqn:4.32.3)

Similarly, the partial trace of $\rho'$​ for the first qubit is

$$
\begin{align}
{\rm Tr}_{2}(\rho') =& (I\otimes \langle 0|) \rho' (I\otimes | 0\rangle ) + (I\otimes \langle 1|) \rho' (I\otimes | 1\rangle ) \\
=& (I\otimes \langle 0|) P_0\rho P_0 (I\otimes | 0\rangle ) +(I\otimes \langle 0|) P_1\rho P_1 (I\otimes | 0\rangle ) \\
&+ (I\otimes \langle 1|) P_0\rho P_0 (I\otimes | 1\rangle ) +(I\otimes \langle 1|) P_1\rho P_1 (I\otimes | 1\rangle )\\
=& (I\otimes \langle 0|) (I\otimes |0\rangle\langle 0|)\rho (I\otimes |0\rangle\langle 0|) (I\otimes | 0\rangle ) \\
&+(I\otimes \langle 0|) (I\otimes |1\rangle\langle 1|)\rho (I\otimes |1\rangle\langle 1|)(I\otimes | 0\rangle ) \\
&+ (I\otimes \langle 1|) (I\otimes |0\rangle\langle 0|)\rho (I\otimes |0\rangle\langle 0|) (I\otimes | 1\rangle ) \\
&+(I\otimes \langle 1|) (I\otimes |1\rangle\langle 1|)\rho (I\otimes |1\rangle\langle 1|)(I\otimes | 1\rangle )\\

=& (I\otimes \langle 0|0\rangle\langle 0|) \rho (I\otimes |0\rangle\langle 0|0\rangle ) \\
&+(I\otimes \langle 0|1\rangle\langle 1|) \rho (I\otimes |1\rangle\langle 1|0\rangle )  \\
&+ (I\otimes \langle 1|0\rangle\langle 0|) \rho (I\otimes |0\rangle\langle 0|1\rangle )  \\
&+(I\otimes \langle 1|1\rangle\langle 1|) \rho (I\otimes |1\rangle\langle 1|1\rangle ) \\
=& (I\otimes \langle 0|) \rho (I\otimes |0\rangle)+(I\otimes \langle 1|) \rho (I\otimes |1\rangle) 
\end{align}
$$(eqn:4.32.4)

which is the same as eq. {eq}`eqn:4.32.3`. Thus, we have ${\rm Tr}_{2}(\rho)={\rm Tr}_{2}(\rho')$.