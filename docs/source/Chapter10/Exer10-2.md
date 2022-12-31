# Exercise 10.2

Consider two eigenstates of $X$ operator, 

$$
|+\rangle = \frac{|0\rangle + |1\rangle}{\sqrt{2}}, |-\rangle = \frac{|0\rangle - |1\rangle}{\sqrt{2}}
$$(eqn:10.2.1)

We can write the corresponding projector as

$$
\begin{align}
P_{+} &= |+\rangle\langle +| =\frac{1}{2}(|0\rangle\langle 0| + |0\rangle\langle 1|+|1\rangle\langle 0|+|1\rangle\langle 1| ) \\
P_{-} &= |-\rangle\langle -| =\frac{1}{2}(|0\rangle\langle 0| - |0\rangle\langle 1|-|1\rangle\langle 0|+|1\rangle\langle 1| ) \\
\end{align}
$$(eqn:10.2.2)

Notice that $P_{+} = P^{\dagger}_{+}$ and $P_{-} = P^{\dagger}_{-}$. We can compute $ P_+ \rho P_+$​ as 

$$
\begin{align}
 pP_+ \rho P_+ =& \frac{1}{4}p(|0\rangle\langle 0| + |0\rangle\langle 1|+|1\rangle\langle 0|+|1\rangle\langle 1| )\rho \\
 &\cdot(|0\rangle\langle 0| + |0\rangle\langle 1|+|1\rangle\langle 0|+|1\rangle\langle 1| ) \\
=& \frac{1}{4}p(|0\rangle\langle 0|\rho|0\rangle\langle 0| + |0\rangle\langle 0|\rho|0\rangle\langle 1|+|0\rangle\langle 0|\rho|1\rangle\langle 0|+|0\rangle\langle 0|\rho|1\rangle\langle 1| ) \\
 &+\frac{1}{4}p(|0\rangle\langle 1|\rho|0\rangle\langle 0| + |0\rangle\langle 1|\rho|0\rangle\langle 1|+|0\rangle\langle 1|\rho|1\rangle\langle 0|+|0\rangle\langle 1|\rho|1\rangle\langle 1| ) \\
 &+\frac{1}{4}p(|1\rangle\langle 0|\rho|0\rangle\langle 0| + |1\rangle\langle 0|\rho|0\rangle\langle 1|+|1\rangle\langle 0|\rho|1\rangle\langle 0|+|1\rangle\langle 0|\rho|1\rangle\langle 1| ) \\
 &+\frac{1}{4}p(|1\rangle\langle 1|\rho|0\rangle\langle 0| + |1\rangle\langle 1|\rho|0\rangle\langle 1|+|1\rangle\langle 1|\rho|1\rangle\langle 0|+|1\rangle\langle 1|\rho|1\rangle\langle 1| ) \\
\end{align}
$$(eqn:10.2.3)

Also, we can compute $ P_- \rho P_-$​ as

$$
\begin{align}
 pP_- \rho P_- =& \frac{1}{4}p(|0\rangle\langle 0| - |0\rangle\langle 1|-|1\rangle\langle 0|+|1\rangle\langle 1| )\rho \\
 &\cdot(|0\rangle\langle 0| - |0\rangle\langle 1|-|1\rangle\langle 0|+|1\rangle\langle 1| ) \\
=& \frac{1}{4}p(|0\rangle\langle 0|\rho|0\rangle\langle 0| - |0\rangle\langle 0|\rho|0\rangle\langle 1|-|0\rangle\langle 0|\rho|1\rangle\langle 0|+|0\rangle\langle 0|\rho|1\rangle\langle 1| ) \\
 &+\frac{1}{4}p(-|0\rangle\langle 1|\rho|0\rangle\langle 0| + |0\rangle\langle 1|\rho|0\rangle\langle 1|+|0\rangle\langle 1|\rho|1\rangle\langle 0|-|0\rangle\langle 1|\rho|1\rangle\langle 1| ) \\
 &+\frac{1}{4}p(-|1\rangle\langle 0|\rho|0\rangle\langle 0| + |1\rangle\langle 0|\rho|0\rangle\langle 1|+|1\rangle\langle 0|\rho|1\rangle\langle 0|-|1\rangle\langle 0|\rho|1\rangle\langle 1| ) \\
 &+\frac{1}{4}p(|1\rangle\langle 1|\rho|0\rangle\langle 0| - |1\rangle\langle 1|\rho|0\rangle\langle 1|-|1\rangle\langle 1|\rho|1\rangle\langle 0|+|1\rangle\langle 1|\rho|1\rangle\langle 1| ) \\
\end{align}
$$(eqn:10.2.4)

Combine eq. {eq}`eqn:10.2.3` and eq. {eq}`eqn:10.2.4`, we have

$$
\begin{align}
 pP_+ \rho P_+ +  pP_- \rho P_- =& \frac{1}{2}p(|0\rangle\langle 0|\rho|0\rangle\langle 0| +|0\rangle\langle 0|\rho|1\rangle\langle 1| ) +\frac{1}{2}p( |0\rangle\langle 1|\rho|0\rangle\langle 1|+|0\rangle\langle 1|\rho|1\rangle\langle 0|) \\
 &+\frac{1}{2}p(|1\rangle\langle 0|\rho|0\rangle\langle 1|+|1\rangle\langle 0|\rho|1\rangle\langle 0|) +\frac{1}{2}p(|1\rangle\langle 1|\rho|0\rangle\langle 0|+|1\rangle\langle 1|\rho|1\rangle\langle 1| ) \\
=& \frac{1}{2}p(|0\rangle\langle 0|+|1\rangle\langle 1| )\rho(|0\rangle\langle 0| +|1\rangle\langle 1|) +\frac{1}{2}p(|0\rangle\langle 1|+|1\rangle\langle 0|)\rho(|0\rangle\langle 1|+|1\rangle\langle 0|) \\
=& \frac{1}{2}p I\rho I + \frac{1}{2}p X\rho X = \frac{1}{2}p \rho + \frac{1}{2}p X\rho X 
\end{align}
$$(eqn:10.2.5)

From eq. {eq}`eqn:10.2.5`, we could find that 

$$
2pP_+ \rho P_+ +  2pP_- \rho P_- = p\rho + pX\rho X \iff pX\rho X = 2pP_+ \rho P_+ +  2pP_- \rho P_- - p\rho
$$(eqn:10.2.6)

With above equation, we could re-write the bit flip channel as 

$$
\begin{align}
\mathcal{E}(\rho) &= (1-p)\rho + pX\rho X  \\
&= (1-p)\rho+2pP_+ \rho P_+ +  2pP_- \rho P_- - p\rho \\
&= (1-2p)\rho+2pP_+ \rho P_+ +  2pP_- \rho P_-
\end{align}
$$(eqn:10.2.7)
