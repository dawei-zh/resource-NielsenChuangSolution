#### Properties of Density Matrix

The density matrix of a certain quantum state $|\psi\rangle = \sum_i c_i|i\rangle$ is defined by
$$
\rho = |\psi\rangle\langle \psi| =\sum |c_i|^2|i\rangle\langle i|\tag{1}
$$
Density matrix formulism is another kind of description of quantum state and corresponding evolution. 

Density matrix has following properties

* Density matrix has unit trace, ${\rm Tr}\rho = 1$
* Density matrix is Hermitian, $\rho^{\dagger} = \rho$
* Density matrix is positive defined, $\langle \phi|\rho|\phi\rangle \geq 0$

---

We can use the density matrix operator to describe the 5 axioms. 

* The probability of measuring $E_{k}$ is ${\rm Tr}(E_k\rho)$. 

* The evolution of $\rho(t)$ is given by
  $$
  \rho(t) = U(t)\rho(0)U^{\dagger}(t)
  $$
   The corresponding differential equation is then given by
  $$
  \frac{\partial \rho}{\partial t} = \cdots
  $$
  

#### Pure and Mixed State

The above is for pure state, and the below would concern mixed state. The expectation value of mixed state is given by
$$
\langle A\rangle = \sum_{i}p_{i} \langle \psi_i|A|\psi_i\rangle = \sum p_i {\rm Tr}(A|\psi\rangle\langle \psi|) = {\rm Tr}(A\rho)
$$
