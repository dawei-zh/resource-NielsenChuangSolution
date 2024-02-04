# Exercise 5.2

Following Eq.(5.5)-Eq.(5.10) in the textbook, the Fourier transformation of state $|j\rangle$ can be written as

$$
|j\rangle \to \frac{1}{2^{n/2}}\left(|0\rangle + e^{2\pi i 0.j_n}|1\rangle\right)\left(|0\rangle + e^{2\pi i 0.j_{n-1}j_n}|1\rangle\right)\cdots \left(|0\rangle + e^{2\pi i 0.j_1\dotsc j_n}|1\rangle\right)
$$(eqn:5.2.1)

According to the textbook, $j_1\dotsc j_n$ is binary representation of integer $j$, and

$$
0.j_{l}j_{l+1}\dotsc j_{m} = j_l/2 +  j_{l+1}/4 + \dotsc + j_m/2^{m-l+1}
$$(eqn:5.2.2)

If we have a $n-$qubit state $|j\rangle = |0\rangle = |00\dotsc 0\rangle$, then $j_k = 0$ for any $1\leq k\leq n$ in the binary representation. Also, it always have $0.j_{k}\dotsc j_n = 0$ for any $k$ from eq. {eq}`eqn:5.2.2`. Thus, the Fourier transformation of $n-$qubit state $|00\dotsc 0\rangle$ is given by

$$
|00\dotsc 0\rangle \to \frac{1}{2^{n/2}}\left(|0\rangle + |1\rangle\right)\left(|0\rangle + |1\rangle\right)\cdots \left(|0\rangle + |1\rangle\right) = |+\rangle^{\otimes n}
$$(eqn:5.2.3)

where $|+\rangle = (|0\rangle + |1\rangle)/\sqrt{2}$. 