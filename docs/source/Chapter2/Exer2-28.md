# Exercise 2.28

Let $A = \sum_{i,j}a_{ij}|i\rangle \langle j|$ be a $p\times q$ matrix and $B = \sum_{m,n}b_{mn}|m\rangle\langle n|$ be a $r\times s$ matrix, we can write the tensor product $A\otimes B$ as

$$
A\otimes B = \sum_{i,m;j,n} a_{ij}b_{mn}(|i\rangle \otimes |m\rangle)(\langle j|\otimes \langle n|) 
$$(eqn:2.28.1)

The matrix representation of $A\otimes B$ is given by

$$
A\otimes B = \begin{pmatrix}
a_{11}B & a_{12}B & \cdots & a_{1q}B \\
a_{21}B & a_{22}B & \cdots & a_{2q}B \\
\vdots & \vdots & \ddots & \vdots \\
a_{p1}B & a_{p2}B & \cdots & a_{pq}B \\
\end{pmatrix} = \begin{pmatrix}
a_{11}b_{11} & a_{11}b_{12} & \cdots & a_{1q}b_{1s} \\
a_{11}b_{21} & a_{11}b_{22} & \cdots & a_{1q}b_{2s} \\
\vdots & \vdots & \ddots & \vdots \\
a_{p1}b_{r1} & a_{p2}b_{r2} & \cdots & a_{pq}b_{rs} \\
\end{pmatrix}
$$(eqn:2.28.2)

I will prove the following relations about tensor product,

$$
(A\otimes B)^{t} = A^{t}\otimes B^{t}, (A\otimes B)^{*} = A^{*}\otimes B^{*}, (A\otimes B)^{\dagger} = A^{\dagger}\otimes B^{\dagger}
$$(eqn:2.28.3)

For $(A\otimes B)^{t}$, eq. {eq}`eqn:2.28.2` tell us that $(A\otimes B)^{t}$ is given by

$$
(A\otimes B)^{t} = \begin{pmatrix}
a_{11}b_{11} & a_{11}b_{21} & \cdots & a_{p1}b_{r1} \\
a_{11}b_{12} & a_{11}b_{22} & \cdots & a_{p2}b_{r2} \\
\vdots & \vdots & \ddots & \vdots \\
a_{1q}b_{1s} & a_{1q}b_{2s} & \cdots & a_{pq}b_{rs} \\
\end{pmatrix}
$$(eqn:2.28.4)

If we write eq. {eq}`eqn:2.28.4` into a form like eq. {eq}`eqn:2.28.1`, 

$$
(A\otimes B)^{t} = \sum_{i,m;j,n} a_{ji}b_{nm }(|i\rangle \otimes |m\rangle)(\langle j\otimes \langle n|) 
$$(eqn:2.28.5)

For $A^{t}\otimes B^{t}$, we have $A^{t} = \sum_{i,j}a_{ji}|i\rangle \langle j|$ and $B^{t} = \sum_{m,n}b_{nm}|m\rangle\langle n|$, then according to eq. {eq}`eqn:2.28.1`$​, we have

$$
A^{t}\otimes B^{t} = \sum_{i,m;j,n} a_{ji}b_{nm}(|i\rangle \otimes |m\rangle)(\langle j\otimes \langle n|) 
$$(eqn:2.28.6)

From eq. {eq}`eqn:2.28.5` and {eq}`eqn:2.28.6`, we have $(A\otimes B)^{t} = A^{t}\otimes B^{t}$. 

For $(A\otimes B)^{*}$, according to eq. {eq}`eqn:2.28.1`, we have

$$
(A\otimes B)^{*} = \sum_{i,m;j,n} a^{*}_{ij}b^{*}_{mn}(|i\rangle \otimes |m\rangle)(\langle j\otimes \langle n|)
$$(eqn:2.28.7)

For $A^{*}\otimes B^{*}$, I notice that $A^{*} = \sum_{i,j}a^{*}_{ij}|i\rangle \langle j|$ and $B^{*} = \sum_{m,n}b^{*}_{mn}|m\rangle\langle n|$, then according to eq. {eq}`eqn:2.28.1`, we have

$$
A^{*}\otimes B^{*} = \sum_{i,m;j,n} a^{*}_{ij}b^{*}_{mn}(|i\rangle \otimes |m\rangle)(\langle j\otimes \langle n|)
$$(eqn:2.28.8)

From eq. {eq}`eqn:2.28.7` and {eq}`eqn:2.28.8`, we have $(A\otimes B)^{*} = A^{*}\otimes B^{*}$. 

For $(A\otimes B)^{\dagger}$, since the hermitian conjugate of a matrix $A^{\dagger}$ is equivalent with the transpose of complex conjugate of matrix $A$, that is, $A^{\dagger} = (A^{*})^{T}$. So we can make use of the above two relations and get

$$
(A\otimes B)^{\dagger} = ((A\otimes B)^*)^{T} = ((A^*\otimes B^*))^{T} = (A^*)^T\otimes (B^*)^T = A^\dagger\otimes B^\dagger
$$(eqn:2.28.9)