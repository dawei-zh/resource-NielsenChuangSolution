# Exercise 4.17

Suppose that we have control-$X$ operation as  

$$
{\rm CNOT}: |0\rangle\langle 0| \otimes I + |1\rangle\langle 1| \otimes X 
$$(eqn:4.17.1)

control-$Z$​ operation can be expressed as follow, 

$$
{\rm control-}Z: |0\rangle\langle 0| \otimes I + |1\rangle\langle 1| \otimes Z 
$$(eqn:4.17.2)

Then we could simply add one Hadamard gate before the target operation, and one Hadamard gate after the target operation. That is, 

$$
\begin{align}
(I\otimes H){\rm control-}Z(I\otimes H) &= (I\otimes H)(|0\rangle\langle 0| \otimes I + |1\rangle\langle 1| \otimes Z )(I\otimes H) \\
&= (|0\rangle\langle 0| \otimes H + |1\rangle\langle 1| \otimes HZ )(I\otimes H)\\
&= |0\rangle\langle 0| \otimes HH + |1\rangle\langle 1| \otimes HZH
\end{align}
$$(eqn:4.17.3)

Note that $H = H^{\dagger}$ and $H^{\dagger}H = I$, and $HZH = X$, we could conclude that

$$
{\rm CNOT} = (I\otimes H){\rm control-}Z(I\otimes H)
$$(eqn:4.17.4)

Similarly, if the control-$Z$ gate is in the following form, 

$$
{\rm control-}Z_2: I\otimes |0\rangle\langle 0| + Z\otimes |1\rangle\langle 1|
$$(eqn:4.17.5)

we could also write a $\rm CNOT$ gate as

$$
(H\otimes I){\rm control-}Z_2(H\otimes I) = I\otimes |0\rangle\langle 0| + X\otimes |1\rangle\langle 1| 
$$(eqn:4.17.6)