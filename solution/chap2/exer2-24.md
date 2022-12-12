## Exercise 2.24

According to the Hint, we can show at first that an arbitrary operator $A$ can be written as $A = B+iC$ where $B$ and $C$ is Hermitian. We can construct 
$$
B = \frac{A + A^{\dagger}}{2}, C = \frac{A - A^{\dagger}}{2i} = \frac{iA^{\dagger} - iA}{2} \tag{1}
$$
and with above construction, we can recover $A$ by
$$
B + iC = \frac{A + A^{\dagger}}{2} +i\frac{A - A^{\dagger}}{2i} = \frac{A + A^{\dagger}}{2} +\frac{A - A^{\dagger}}{2} = A \tag{2}
$$
It is easy to verify that $B$ and $C$ are Hermitian, since
$$
B^{\dagger} = \frac{A^{\dagger}+A}{2} = B, C^{\dagger} = \frac{-iA +i A^{\dagger}}{2} = C\tag{3}
$$
where we use
$$
\left(\sum_{i} a_i A_i\right)^{\dagger} = \sum_{i} a^{*}_i A^{\dagger}_i\tag{4}
$$
Then for arbitrary vector $|v\rangle$, using $A = B + iC$ we have
$$
\langle v|A|v\rangle = \langle v|B|v\rangle + i\langle v|C|v\rangle\tag{5}
$$
Note that $B$ and $C$ are Hermitian, so we can use spectral decomposition and compute
$$
\begin{align}
\langle v|A|v\rangle =& \langle v|B|v\rangle + i\langle v|C|v\rangle \\
=& \left\langle v\left|\left(\sum_{i}\lambda_i |b_i\rangle\langle b_i|\right)\right|v\right\rangle + i\left\langle v\left|\left(\sum_{x}\mu_x |c_x\rangle\langle c_x|\right)\right|v\right\rangle \\
=& \left(\sum_j v^*_{bj}\langle b_j|\right)\left|\left(\sum_{i}\lambda_i |b_i\rangle\langle b_i|\right)\right|\left(\sum_k v_{bk}|b_k\rangle\right) \\
&+ i\left(\sum_y v^*_{cy}\langle c_y|\right)\left|\left(\sum_{x}\mu_x |c_x\rangle\langle c_x|\right)\right|\left(\sum_z v_{cz}|c_z\rangle\right) \\
=& \sum_{i,j,k}v^*_{bj}v_{bk}\lambda_i \langle b_j|b_i\rangle\langle b_i|b_k\rangle + i\sum_{x,y,z}v^*_{cy}v_{cz}\mu_x \langle c_y|c_x\rangle\langle c_x|c_z\rangle \\
=& \sum_{i}|v_{bi}|^2\lambda_i  + i\sum_{x}|v_{cx}|^2\mu_x  \\
\end{align}\tag{6}\label{6}
$$
Note that generally $B$ and $C$ do not have common eigenvector, but their own eigenvectors are orthogonal to each other, and we adopt two orthonormal basis $\{|b_i\rangle\}$ and $\{|c_i\rangle\}$ to decompose $|v\rangle$ in the above calculation. 

For positive operator $A$, we should have $\langle v|A|v\rangle  >0$ is a real number. So from eq. $\eqref{6}$ we have
$$
\langle v|A|v\rangle =  \sum_{i}|v_{bi}|^2\lambda_i  + i\sum_{x}|v_{cx}|^2\mu_x >0 \iff \lambda_i \geq 0, \mu_x = 0  \tag{7}
$$
Therefore, for positive operator $A$ we have $A = B + iC$ where $B$ is Hermitian and $C = 0$, which indicates that $A$ is Hermitian. 
