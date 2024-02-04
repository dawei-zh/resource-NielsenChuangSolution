## Exercise 2.22

Suppose $A$ is a Hermitian operator, then the eigenvalue of $A$ are real number. Then consider $\lambda_1$ and $\lambda_2$ are eigenvalues of operator $A$ with eigenvectors $|v_1\rangle$ and $|v_2\rangle$, respectively. Then from the definition of eigenvalue and eigenvector, 
$$
A|v_1\rangle = \lambda_1|v_1\rangle, A|v_2\rangle = \lambda_2|v_2\rangle\tag{1}
$$
Since $A$ is Hermitian, we also have 
$$
\langle v_1|A = \langle v_1|A^{\dagger} = \lambda_1\langle v_1|,\langle v_2|A = \langle v_2|A^{\dagger} = \lambda_2\langle v_2|\tag{2}
$$
If compute $\langle v_2|A|v_1\rangle$, we would obtain
$$
\langle v_2|A|v_1\rangle = \langle v_2|(A|v_1\rangle) =(\langle v_2|A)|v_1\rangle\tag{3}
$$
or equivalently, $\lambda_1\langle v_2|v_1\rangle = \lambda_2\langle v_2|v_1\rangle$. If $\lambda_1 \neq \lambda_2$, then $\langle v_2|v_1\rangle = 0$, which indicates that two eigenvectors of a Hermitian operator with different eigenvalues are necessarily orthogonal. 

### A Wrong Solution

Since $A$ is Hermitian, we can write $A$ into spectral decomposition form, $A = \sum_{j}\lambda_j|j\rangle\langle j|$. Also, consider $|v\rangle$ is a eigenvector of $A$ with eigenvalue as $\lambda_v$, then $A|v\rangle = \lambda_v|v\rangle$, and 
$$
A|v\rangle =  \sum_{j}\lambda_j|j\rangle\langle j|v\rangle=\lambda_v|v\rangle \iff \sum_{j}\lambda_j\langle j|v\rangle |j\rangle - \lambda_v|v\rangle = 0\tag{4}\label{4}
$$
The solution of above equation is $\langle j|v\rangle = \delta_{jv}$, so we conclude that two eigenvectors with different eigenvalues (which means $j\neq v$) are orthogonal. 

Above solution is correct if $|v\rangle \in \{|j\rangle\}$, but $|v\rangle$ can also be a linear combination of eigenvectors that share same eigenvalues. This is because
$$
A(a|v_1\rangle + b|v_2\rangle) = aA|v_1\rangle + bA|v_2\rangle = a\lambda|v_1\rangle + b\lambda|v_2\rangle = \lambda(a|v_1\rangle + b|v_2\rangle)\tag{5}
$$
for any $a, b, \lambda$. In this case, $|v\rangle = \sum_{j'}c_{j'}|j'\rangle$ and eq.$\eqref{4}$ becomes 
$$
\sum_{j}\lambda_j\langle j|v\rangle |j\rangle - \lambda_v\sum_{j'}c_{j'}|j'\rangle = 0\tag{6}\label{6}
$$
where $|j'\rangle$ denotes those eigenvectors with same eigenvalues. Solving above equation cannot simply get something like $\langle j|v\rangle = 0$ if $\lambda_j \neq \lambda_v$, thus cannot come to a conclusion that two eigenvectors with different eigenvalues are orthogonal. 

### Other Comments

Note that even from eq. $\eqref{6}$ we find $\langle j|v\rangle = 0$ if $\lambda_j \neq \lambda_v$, it is still not enough to say two eigenvectors with different eigenvalues are orthogonal. We at least still need to consider the case of two eigenvectors that are both some linear combination of eigenvectors in the spectral decomposition but with different eigenvalues. 

Note also that the spectral decomposition formula may include eigenstates that share same eigenvalue. Moreover, here we focus on general vector, so vectors do not need to be normalized. 
