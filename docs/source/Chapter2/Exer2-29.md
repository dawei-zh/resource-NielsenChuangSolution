# Exercise 2.29

Suppose $A$ is a $m\times m$ unitary operator and $B$ is a $n\times n$ unitary operator, we have $A^{\dagger}A = AA^{\dagger} = I_{A}$ and $B^{\dagger}B = BB^{\dagger} = I_B$, where $I_{A}$ is $m\times m$ identity matrix and $I_B$ is $n\times n$ identity matrix. We could also obtain tensor product between $A$ and $B$ as $A\otimes B$, and the Hermitian conjugate of $A\otimes B$ as

$$
(A\otimes B)^{\dagger} = A^{\dagger}\otimes B^{\dagger} 
$$(eqn:2.29.1)

Then we could compute $(A\otimes B)^{\dagger}(A\otimes B)$ as

$$
(A\otimes B)^{\dagger}(A\otimes B) = (A^{\dagger}\otimes B^{\dagger})(A\otimes B) = A^{\dagger}A\otimes B^{\dagger}B = I_{A}\otimes I_{B} = I_{A\otimes B}
$$(eqn:2.29.2)

where $I_{A\otimes B}$ is $mn\times mn$ identity matrix. Similarly, 

$$
(A\otimes B)(A\otimes B)^{\dagger} = (A\otimes B)(A^{\dagger}\otimes B^{\dagger}) = AA^{\dagger}\otimes BB^{\dagger} = I_{A}\otimes I_{B} = I_{A\otimes B}
$$(eqn:2.29.3)

From eq. {eq}`eqn:2.29.2` and eq. {eq}`eqn:2.29.3`, we conclude that the tensor product of two unitary operators is unitary. 