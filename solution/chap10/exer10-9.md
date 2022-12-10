## Exercise 10.9

Consider a three qubit phase flip code with logical qubit as $|0_{L}\rangle = |+++\rangle$ and $|1_{L}\rangle = |---\rangle$, the projector onto the codespace is 
$$
P = |+++\rangle\langle +++|+ |---\rangle\langle ---|\tag{1}
$$
where $P$ is a Hermitian operator. If we consider $P_i$ and $Q_i$ be the projectors onto $|0\rangle$ and $|1\rangle$ states of the $i-$th qubit, we could write these projectors explicitly as  
$$
\begin{align}
P_1 &= |0\rangle\langle 0| \otimes I \otimes I, P_2 = I \otimes |0\rangle\langle 0|\otimes I, P_3 = I \otimes I \otimes |0\rangle\langle 0| \\
Q_1 &= |1\rangle\langle 1| \otimes I \otimes I, Q_2 = I \otimes |1\rangle\langle 1|\otimes I, Q_3 = I \otimes I \otimes |1\rangle\langle 1| \\
\end{align}\tag{2}
$$
where $P_i$ and $Q_i$ are all Hermitian operators. The $|+\rangle$ and $|-\rangle$ states is given by
$$
|+\rangle = \frac{|0\rangle+|1\rangle}{\sqrt{2}}, |-\rangle = \frac{|0\rangle-|1\rangle}{\sqrt{2}}\tag{3}
$$
then we can compute the following formula as
$$
|0\rangle\langle 0|+\rangle = \frac{1}{\sqrt{2}}|0\rangle, |0\rangle\langle 0|-\rangle = \frac{1}{\sqrt{2}}|0\rangle, \\
|1\rangle\langle 1|+\rangle = \frac{1}{\sqrt{2}}|1\rangle, |1\rangle\langle 1|-\rangle = -\frac{1}{\sqrt{2}}|1\rangle\tag{4}\label{4}
$$
Consider $E=\{E_1=I, E_2=P_1, E_3=Q_1, E_4=P_2, E_5=Q_2, E_6=P_3, E_7=Q_3\}$, we can compute $P_i P$​ as  
$$
\begin{align}
P_1P &= (|0\rangle\langle 0| \otimes I \otimes I)(|+++\rangle\langle +++|+ |---\rangle\langle ---|) \\
&= \frac{1}{\sqrt{2}}(|0++\rangle\langle +++|+ |0--\rangle\langle ---|) \\
P_2P &= ( I \otimes |0\rangle\langle 0| \otimes I)(|+++\rangle\langle +++|+ |---\rangle\langle ---|) \\
&= \frac{1}{\sqrt{2}}(|+0+\rangle\langle +++|+ |-0-\rangle\langle ---|) \\
P_3P &= (I \otimes I\otimes |0\rangle\langle 0|)(|+++\rangle\langle +++|+ |---\rangle\langle ---|) \\
&= \frac{1}{\sqrt{2}}(|++0\rangle\langle +++|+ |--0\rangle\langle ---|) \\
\end{align}\tag{5}
$$
For $Q_iP$​, we have
$$
\begin{align}
Q_1P &= (|1\rangle\langle 1| \otimes I \otimes I)(|+++\rangle\langle +++|+ |---\rangle\langle ---|) \\
&= \frac{1}{\sqrt{2}}(|1++\rangle\langle +++|- |1--\rangle\langle ---|) \\
Q_2P &= ( I \otimes |1\rangle\langle 1| \otimes I)(|+++\rangle\langle +++|+ |---\rangle\langle ---|) \\
&= \frac{1}{\sqrt{2}}(|+1+\rangle\langle +++|- |-1-\rangle\langle ---|) \\
Q_3P &= (I \otimes I\otimes |1\rangle\langle 1|)(|+++\rangle\langle +++|+ |---\rangle\langle ---|) \\
&= \frac{1}{\sqrt{2}}(|++1\rangle\langle +++|- |--1\rangle\langle ---|) \\
\end{align}\tag{6}
$$
For $PP_i$​, we have
$$
\begin{align}
PP_1 &= (|+++\rangle\langle +++|+ |---\rangle\langle ---|)(|0\rangle\langle 0| \otimes I \otimes I) \\
&= \frac{1}{\sqrt{2}}(|+++\rangle\langle 0++|+ |---\rangle\langle 0--|) \\
PP_2 &= (|+++\rangle\langle +++|+ |---\rangle\langle ---|)( I \otimes |0\rangle\langle 0| \otimes I) \\
&= \frac{1}{\sqrt{2}}(|+++\rangle\langle +0+|+ |---\rangle\langle -0-|) \\
PP_3 &= (|+++\rangle\langle +++|+ |---\rangle\langle ---|)(I \otimes I\otimes |0\rangle\langle 0|) \\
&= \frac{1}{\sqrt{2}}(|+++\rangle\langle ++0|+ |---\rangle\langle --0|) \\
\end{align}\tag{7}
$$
For $PQ_i$​, we have
$$
\begin{align}
PQ_1 &= (|+++\rangle\langle +++|+ |---\rangle\langle ---|)(|1\rangle\langle 1| \otimes I \otimes I) \\
&= \frac{1}{\sqrt{2}}(|+++\rangle\langle 1++|- |---\rangle\langle 1--|) \\
PQ_2 &= (|+++\rangle\langle +++|+ |---\rangle\langle ---|)( I \otimes |1\rangle\langle 1| \otimes I) \\
&= \frac{1}{\sqrt{2}}(|+++\rangle\langle +1+|- |---\rangle\langle -1-|) \\
PQ_3 &= (|+++\rangle\langle +++|+ |---\rangle\langle ---|)(I \otimes I\otimes |1\rangle\langle 1|) \\
&= \frac{1}{\sqrt{2}}(|+++\rangle\langle ++1|- |---\rangle\langle --1|) \\
\end{align}\tag{8}
$$
With above calculation, we can compute $PE^{\dagger}_1E_j P$ as 
$$
\begin{align}
PE^{\dagger}_1 E_1P &= PI IP = P \iff \alpha_{11} = 1\\
PE^{\dagger}_1 E_2P &= PI P_1P = \frac{1}{2}P \iff \alpha_{12} = \frac{1}{2}\\
PE^{\dagger}_1 E_3P &= PI Q_1P = \frac{1}{2}P\iff \alpha_{11} = \frac{1}{2}\\
PE^{\dagger}_1 E_4P &= PI P_2P = \frac{1}{2}P\iff \alpha_{11} = \frac{1}{2}\\
PE^{\dagger}_1 E_5P &= PI Q_2P = \frac{1}{2}P\iff \alpha_{11} = \frac{1}{2}\\
PE^{\dagger}_1 E_6P &= PI P_3P = \frac{1}{2}P\iff \alpha_{11} = \frac{1}{2}\\
PE^{\dagger}_1 E_7P &= PI Q_3P = \frac{1}{2}P\iff \alpha_{11} = \frac{1}{2}\\
\end{align}\tag{9}
$$
For $PE^{\dagger}_2E_j P$​, we have
$$
\begin{align}
PE^{\dagger}_2 E_2P &= PP_1 P_1P = P \iff \alpha_{22} = 1\\
PE^{\dagger}_2 E_3P &= PP_1 Q_1P = 0\iff \alpha_{23} = 0\\
PE^{\dagger}_2 E_4P &= PP_1 P_2P = \frac{1}{4}P\iff \alpha_{24} = \frac{1}{4}\\
PE^{\dagger}_2 E_5P &= PP_1 Q_2P = \frac{1}{4}P\iff \alpha_{25} = \frac{1}{4}\\
PE^{\dagger}_2 E_6P &= PP_1 P_3P = \frac{1}{4}P\iff \alpha_{26} = \frac{1}{4}\\
PE^{\dagger}_2 E_7P &= PP_1 Q_3P = \frac{1}{4}P\iff \alpha_{27} = \frac{1}{4}\\
\end{align}\tag{10}
$$
For $PE^{\dagger}_3E_j P$​, we have
$$
\begin{align}
PE^{\dagger}_3 E_3P &= PQ_1 Q_1P = P\iff \alpha_{33} = 1\\
PE^{\dagger}_3 E_4P &= PQ_1 P_2P = \frac{1}{4}P\iff \alpha_{34} = \frac{1}{4}\\
PE^{\dagger}_3 E_5P &= PQ_1 Q_2P = \frac{1}{4}P\iff \alpha_{35} = \frac{1}{4}\\
PE^{\dagger}_3 E_6P &= PQ_1 P_3P = \frac{1}{4}P\iff \alpha_{36} = \frac{1}{4}\\
PE^{\dagger}_3 E_7P &= PQ_1 Q_3P = \frac{1}{4}P\iff \alpha_{37} = \frac{1}{4}\\
\end{align}\tag{11}
$$
For $PE^{\dagger}_4E_j P$​, we have
$$
\begin{align}
PE^{\dagger}_4 E_4P &= PP_2 P_2P = P\iff \alpha_{44} = 1\\
PE^{\dagger}_4 E_5P &= PP_2 Q_2P = 0\iff \alpha_{45} = 0\\
PE^{\dagger}_4 E_6P &= PP_2 P_3P = \frac{1}{4}P\iff \alpha_{46} = \frac{1}{4}\\
PE^{\dagger}_4 E_7P &= PP_2 Q_3P = \frac{1}{4}P\iff \alpha_{47} = \frac{1}{4}\\
\end{align}\tag{12}
$$
For $PE^{\dagger}_5E_j P$​, we have
$$
\begin{align}
PE^{\dagger}_5 E_5P &= PQ_2 Q_2P = 1\iff \alpha_{55} = 1\\
PE^{\dagger}_5 E_6P &= PQ_2 P_3P = \frac{1}{4}P\iff \alpha_{56} = \frac{1}{4}\\
PE^{\dagger}_5 E_7P &= PQ_2 Q_3P = \frac{1}{4}P\iff \alpha_{57} = \frac{1}{4}\\
\end{align}\tag{13}
$$
For $PE^{\dagger}_6E_j P$​, we have
$$
\begin{align}
PE^{\dagger}_6 E_6P &= PP_3 P_3P = P\iff \alpha_{66} = 1\\
PE^{\dagger}_6 E_7P &= PP_3 Q_3P = 0\iff \alpha_{67} = 0\\
\end{align}\tag{14}
$$
For $PE^{\dagger}_7E_j P$​, we have
$$
\begin{align}
PE^{\dagger}_7 E_7P &= PQ_3 Q_3P = P\iff \alpha_{77} = 1\\
\end{align}\tag{15}
$$
Note that projector $P$ and all error are Hermitian operator, then 
$$
\alpha_{ij}P = PE^{\dagger}_iE_j P = PE_iE_j P = (PE_iE_j P)^{\dagger} = PE_jE_i P = PE^{\dagger}_jE_i P = \alpha_{ji}P\tag{16}
$$
so $\alpha_{ij} = \alpha_{ji}$. Since $\alpha_{ij}$ for $i\leq j$ are all real number, we know that the phase flip code satisfies the quantum error correcting condition. 
