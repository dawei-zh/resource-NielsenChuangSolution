## Exercise 2.64

I would provide two solutions to this problem which are equivalent with each other in some sense. 

### Solution One

Suppose we have $m$ linearly independent vectors $|\psi_1\rangle, |\psi_2\rangle, \dotsc, |\psi_m\rangle$, and they can be considered as a basis of vector space $V$. Then, any subset of $\{|\psi_j\rangle\}_{j=1}^{m}$ is also linearly independent and can be considered as a basis of a subspace. We could construct the POVM based on above property. 

* For $i = 1, \dotsc, m$, if define $P_i$ as a projector to subspace ${\rm span}\{|\psi_j\rangle\}_{j=1, \dotsc, m\text{ and } j\neq i}$, then
  $$
  E_{i} = a_i(I - P_i), a_i > 0\tag{1}\label{11}
  $$
  Here $I - P_i$ is an orthogonal complement of project $P_i$ operator, and it is a projector to the subspace spanned by only $|\psi_i\rangle$ according to the textbook. Then the probability of getting $E_i$ for state $|\psi_i\rangle$, i.e., $\langle \psi_i|E_i|\psi_i\rangle$ is non-zero, while the probability of getting outcome $E_i$ if given state $|\psi_j\rangle$ where $i\neq j$ is zero since $|\psi_j\rangle$ is not in the subspace spanned by only $|\psi_i\rangle$. Thus, if outcome $E_i$ occurs, Bob knows with certainty that he was given the state $|\psi_i\rangle$. 

  To construct projector $P_i$, one can apply the Gram-Schimidt procedure to convert an ordinary basis $\{|\psi_j\rangle\}_{j=1, \dotsc, m\text{ and } j\neq i}$ into an orthonormal basis $\{|\phi_{ik}\rangle\}_{k=1, \dotsc, m-1}$.  Then $P_i = \sum_k |\phi_{ik}\rangle\langle \phi_{ik}|$.

* For $i = m+1$, we define 
  $$
  E_{m+1} = I - \sum_{i=1}^{m} E_i\tag{2}\label{12}
  $$
  The last POVM operator is constructed to make sure the sum of all POVM operators is identity. 

To illustrate that eq. $$\eqref{11}-\eqref{12}$$ is a valid POVM, we still need to verify that $E_{i}$ is postive operator. 

* For $i = 1,\dotsc, m$, since projector $P_i$ is Hermitian, then we can compute 
  $$
  (I - P)^{\dagger}(I - P) = (I - P)(I - P) = I - P - P + P^2 = I - P
  $$
  Note that $(I - P)^{\dagger}(I - P)$ is postive due to Exer2.25 in the textbook, so $I- P$ is also positive and $E_i$ is positive for $a_i> 0$. 
  
* For $i = m+1$, consider an arbitrary state $|v\rangle$, then
  $$
  \langle v|E_{m+1}|v\rangle = \langle v|v\rangle - \sum_{i=1}^{m}\langle v|E_i|v\rangle
  $$
  and for positive $E_i$ we have $\langle v|E_i|v\rangle \geq 0$. By setting $a_i$ as a small enough number, we can always have $\langle v|E_{m+1}|v\rangle\geq 0$ and $E_{m+1}$ can be positive. 

### Solution Two

We could also consider a POVM in the following form. 

* For $i = 1, \dotsc, m$, let 
  $$
  E_i = a_i|v_i\rangle\langle v_i|, a_i > 0\tag{3}\label{15}
  $$
  where $\langle v_i|\psi_j\rangle = 0$ for $i\neq j$ and $\langle v_i|\psi_i\rangle \neq 0$. From the definition, the probability of getting $E_i$ for state $|\psi_i\rangle$, i.e., $\langle \psi_i|E_i|\psi_i\rangle = |\langle v_i|\psi_i\rangle|$ is non-zero, while the probability of getting outcome $E_i$ if given state $|\psi_j\rangle$ where $i\neq j$ is zero. Thus, if outcome $E_i$ occurs, Bob knows with certainty that he was given the state $|\psi_i\rangle$. 

  To construct $|v_i\rangle$, one can first apply the Gram-Schimidt procedure to convert an ordinary basis $\{|\psi_j\rangle\}_{j=1, \dotsc, m\text{ and } j\neq i}$ into an orthonormal basis $\{|\phi_{ik}\rangle\}_{k=1, \dotsc, m-1}$, then perform the $m-$th step of Gram-Schimidt procedure to create $|v_i\rangle$ from $\{|\phi_{ik}\rangle\}_{k=1, \dotsc, m-1}$ and from $|\psi_i\rangle$. Note that $|v_i\rangle$ is orthonormal to $\{|\phi_{ik}\rangle\}_{k=1, \dotsc, m-1}$ so $I - P_i = |v_i\rangle\langle v_i|$ and the two solutions are equivalent with each other. 

* For $i = m+1$, we define 
  $$
  E_{m+1} = I - \sum_{i=1}^{m} E_i\tag{4}\label{16}
  $$
  The last POVM operator is constructed to make sure the sum of all POVM operators is identity. 

To prove that eq. $\eqref{15}-\eqref{16}$ gives a valid POVM measurement, we need to verify each $E_i$ is positive operator. Consider an arbitrary state $|\phi\rangle$, then

* For $i = 1,\dotsc, m$, 
  $$
  \langle \phi|E_i|\phi\rangle = a_i\langle \phi|v_i\rangle\langle v_i|\phi\rangle = a_i |\langle \phi|v_i\rangle|^2 \geq 0
  $$
  which shows $E_i$ is positive operator. 

* For $i = m+1$, 
  $$
  \begin{align}
  \langle \phi|E_{m+1}|\phi\rangle &= \langle \phi|\phi\rangle - \sum_{i=1}^{m} a_i\langle \phi|v_i\rangle\langle v_i|\phi\rangle = \langle \phi|\phi\rangle -\sum_{i=1}^{m} a_i|\langle \phi|v_i\rangle|^2
  \end{align}
  $$
  By setting $a_i$ as a small enough number, we can always have $\langle v|E_{m+1}|v\rangle\geq 0$ and $E_{m+1}$ can be positive. 
