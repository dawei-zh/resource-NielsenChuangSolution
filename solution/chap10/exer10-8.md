## Exercise 10.8

Consider a three qubit phase flip code with logical qubit as $|0_{L}\rangle = |+++\rangle$ and $|1_{L}\rangle = |---\rangle$, the projector onto the codespace is 
$$
P = |+++\rangle\langle +++|+ |---\rangle\langle ---|
$$
Since $Z|+\rangle = |-\rangle$ and $Z|-\rangle = |+\rangle$, we have
$$
\begin{align}
Z_1P = |-++\rangle\langle +++|+ |+--\rangle\langle ---|\\
Z_2P = |+-+\rangle\langle +++|+ |-+-\rangle\langle ---|\\
Z_3P = |++-\rangle\langle +++|+ |--+\rangle\langle ---|\\
PZ_1 = |+++\rangle\langle -++|+ |---\rangle\langle +--|\\
PZ_2 = |+++\rangle\langle +-+|+ |---\rangle\langle -+-|\\
PZ_3 = |+++\rangle\langle ++-|+ |---\rangle\langle --+|\\
\end{align}
$$
If $E = \{E_1 = I, E_2 = Z_1, E_3 = Z_2, E_4 = Z_3\}$​, we could compute that
$$
PE^{\dagger}_1E_1 P = PII P = P^2 = P \iff \alpha_{11} = 1\\
PE^{\dagger}_2E_2 P = PZ_1Z_1 P =P^2 =  P \iff \alpha_{22} = 1\\
PE^{\dagger}_3E_3 P = PZ_2Z_2 P = P^2 = P \iff \alpha_{33} = 1\\
PE^{\dagger}_4E_4 P = PZ_3Z_3 P = P^2 = P \iff \alpha_{44} = 1\\
$$

Also, we could find that for $i\neq j$ we have $PE^{\dagger}_iE_j P = 0$ since we have $PE^{\dagger}_i \neq E_j P$ when $i\neq j$, and the product of states with orthonormal basis can only be zero. Therefore, we could find that $\alpha_{ij} = \delta_{ij}$ where $\delta_{ij} = 1$ if $i=j$ and $\delta_{ij} = 0$ when $i\neq j$. So the error set $E = \{E_1 = I, E_2 = Z_1, E_3 = Z_2, E_4 = Z_3\}$ satisfies the quantum error-correction conditions and matrix $\alpha$ is Hermitian matrix (identity matrix).



