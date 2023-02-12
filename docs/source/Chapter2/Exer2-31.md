# Exercise 2.31

Suppose $V$ is a vector space with orthonormal basis $\{|i\rangle_{V}\}$ and $A:V\to V$ is a $m\times m$ positive operator. Suppose $W$ is a vector space with orthonormal basis $\{|j\rangle_{W}\}$ and $B:W\to W$ is a $n\times n$ positive operator. Then the tensor product of $A$ and $B$ is an operator $A\otimes B : V\otimes W\to V\otimes W$, and the basis in vector space $V\otimes W$ is $\{|i\rangle_{V}\otimes|j\rangle_{W}\}$. To prove operator $A\otimes B$ is positive, we need to prove for arbitrary vector $|\psi\rangle \in V\otimes W$, we have 

$$
\langle \psi|A\otimes B |\psi\rangle \geq 0, \text{where }|\psi\rangle = \sum_{i,j} c_{ij} |i\rangle_{V}\otimes|j\rangle_{W}
$$(eqn:2.31.1)

We could compute $\langle \psi|A\otimes B|\psi\rangle $ directly as 

$$
\begin{align}
\langle \psi|A\otimes B|\psi\rangle  &= \left(\sum_{i',j'} c^{*}_{i'j'} \langle i'|_{V}\otimes\langle j'|_{W}\right)A\otimes B \left(\sum_{i,j} c_{ij} |i\rangle_{V}\otimes|j\rangle_{W}\right) \\
&= \sum_{i,i',j,j'} c^{*}_{i'j'}c_{ij}  \langle i'|A|i\rangle \langle j'|B|j\rangle \\
&= \sum_{i,j} |c_{ij}|^2  \langle i|A|i\rangle \langle j|B|j\rangle \\
\end{align}
$$(eqn:2.31.2)

Note that $A$ and $B$ are positive operator, then for basis vector $|i\rangle_{V}$ and $|j\rangle_W$, we should always have $\langle i|A|i\rangle\geq 0$ and $\langle j|B|j\rangle\geq 0$. Also, since for any coefficient $c_{ij}$, we have $|c_{ij}|^2 \geq0$, for eq. {eq}`eqn:2.31.2` we should have 

$$
\langle \psi|A\otimes B|\psi\rangle = \sum_{i,j} |c_{ij}|^2  \langle i|A|i\rangle \langle j|B|j\rangle  \geq 0
$$(eqn:2.31.3)

Then we could conclude that, $\langle \psi|A\otimes B|\psi\rangle \geq 0 $ for arbitrary state $|\psi\rangle \in V\otimes W$, and the tensor product of two positive operators is positive. 