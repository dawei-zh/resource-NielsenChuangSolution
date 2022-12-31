# Exercise 4.1

For a arbitrary single qubit state $|\psi\rangle$, its Bloch sphere representation $(\theta, \varphi)$ can be obtained as follow, 

$$
|\psi\rangle = \cos\frac{\theta}{2}|0\rangle + \sin\frac{\theta}{2}e^{i\varphi}|1\rangle
$$(eqn:4.1.1)

Here are eigenvalues and eigenstates of Pauli matrices. 

* For $X$,  the eigenvalues $\lambda_1=1$ and $\lambda_2=-1$, and  their corresponding eigenvectors are

  $$
  |v_1\rangle = \frac{1}{\sqrt{2}}\begin{pmatrix}
  1 \\ 1
  \end{pmatrix}, |v_2\rangle = \frac{1}{\sqrt{2}}\begin{pmatrix}
  1\\ -1
  \end{pmatrix}
  $$(eqn:4.1.2)

  We can obtain the Bloch coordinate of $|v_1\rangle$ and $|v_2\rangle$ via
  
  $$
  \begin{align}
  |v_1\rangle &= \frac{1}{\sqrt{2}} |0\rangle + \frac{1}{\sqrt{2}}|1\rangle \\
  &= \cos\frac{\pi/2}{2}|0\rangle + \sin\frac{\pi/2}{2}e^{i\cdot0}|1\rangle \\
  |v_2\rangle &= \frac{1}{\sqrt{2}} |0\rangle - \frac{1}{\sqrt{2}}|1\rangle \\
  &= \cos\frac{\pi/2}{2}|0\rangle + \sin\frac{\pi/2}{2}e^{i\pi}|1\rangle \\
  \end{align}
  $$(eqn:4.1.3)

  So the Bloch coordinate is $(\pi/2, 0)$ for $|v_1\rangle$ and $(\pi/2, \pi)$ for $|v_2\rangle$

* For $Y$​, the eigenvalues $\lambda_1=1$​ and $\lambda_2=-1$​, and their corresponding eigenvectors are

  $$
  |v_1\rangle =  \frac{1}{\sqrt{2}}\begin{pmatrix}
  1 \\ i
  \end{pmatrix}, |v_2\rangle =  \frac{1}{\sqrt{2}}\begin{pmatrix}
  1\\ -i
  \end{pmatrix}
  $$(eqn:4.1.4)

  We can obtain the Bloch coordinate of $|v_1\rangle$ and $|v_2\rangle$ via

  $$
  \begin{align}
  |v_1\rangle &= \frac{1}{\sqrt{2}} |0\rangle + \frac{1}{\sqrt{2}}i|1\rangle \\
  &= \cos\frac{\pi/2}{2}|0\rangle + \sin\frac{\pi/2}{2}e^{i\cdot \pi/2}|1\rangle \\
  |v_2\rangle &= \frac{1}{\sqrt{2}} |0\rangle - \frac{1}{\sqrt{2}}i|1\rangle \\
  &= \cos\frac{\pi/2}{2}|0\rangle + \sin\frac{\pi/2}{2}e^{-i\pi/2}|1\rangle \\
  \end{align}
  $$(eqn:4.1.5)

  So the Bloch coordinate is $(\pi/2, \pi/2)$ for $|v_1\rangle$ and $(\pi/2, -\pi/2)$ for $|v_2\rangle$

* For $Z$​, the eigenvalues $\lambda_1=1$​ and $\lambda_2=-1$​, and their corresponding eigenvectors are

  $$
  |v_1\rangle = \begin{pmatrix}
  1 \\ 0
  \end{pmatrix}, |v_2\rangle = \begin{pmatrix}
  0\\ 1
  \end{pmatrix}
  $$(eqn:4.1.6)

  We can obtain the Bloch coordinate of $|v_1\rangle$ and $|v_2\rangle$ via

  $$
  \begin{align}
  |v_1\rangle &= |0\rangle = \cos\frac{0}{2}|0\rangle + \sin\frac{0}{2}e^{i\cdot 0}|1\rangle \\
  |v_2\rangle &= |1\rangle = \cos\frac{\pi}{2}|0\rangle + \sin\frac{\pi}{2}e^{-i\cdot 0}|1\rangle \\
  \end{align}
  $$(eqn:4.1.7)

  So the Bloch coordinate is $(0, 0)$ for $|v_1\rangle$ and $(\pi, 0)$ for $|v_2\rangle$. 