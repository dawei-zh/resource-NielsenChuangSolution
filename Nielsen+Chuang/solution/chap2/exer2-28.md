## Exercise 2.28

The tensor product is defined as follows. Let $A = \sum_{i,j}a_{ij}|i\rangle \langle j|$ is a $p\times q$ matrix and $B = \sum_{m,n}b_{mn}|m\rangle\langle n|$ is a $r\times s$ matrix, then we have
$$
A\otimes B = \sum_{i,m;j,n} a_{ij}b_{mn}(|i\rangle \otimes |m\rangle)(\langle j\otimes \langle n|) \tag{1}\label{1}
$$
If $|i\rangle, |j\rangle,|m\rangle, |n\rangle$ is $|0\rangle = (1\;\;0)^{t}$ or $|1\rangle = (0\;\;1)^{t}$, the result of tensor product eq. $\eqref{1}$ can be re-written as
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
\end{pmatrix}\tag{2}\label{2}
$$
I will prove the following relations about tensor product,
$$
(A\otimes B)^{t} = A^{t}\otimes B^{t}, (A\otimes B)^{*} = A^{*}\otimes B^{*}, (A\otimes B)^{\dagger} = A^{\dagger}\otimes B^{\dagger} \tag{3}
$$

* For $(A\otimes B)^{t}$, eq. $\eqref{2}$ tell us that $(A\otimes B)^{t}$ is given by
  $$
  (A\otimes B)^{t} = \begin{pmatrix}
  a_{11}b_{11} & a_{11}b_{21} & \cdots & a_{p1}b_{r1} \\
  a_{11}b_{12} & a_{11}b_{22} & \cdots & a_{p2}b_{r2} \\
  \vdots & \vdots & \ddots & \vdots \\
  a_{1q}b_{1s} & a_{1q}b_{2s} & \cdots & a_{pq}b_{rs} \\
  \end{pmatrix}\tag{4}\label{4}
  $$
  If we write eq. $\eqref{4}$ into a form like eq. $\eqref{1}$​, 
  $$
  (A\otimes B)^{t} = \sum_{i,m;j,n} a_{ji}b_{nm }(|i\rangle \otimes |m\rangle)(\langle j\otimes \langle n|) \tag{5}\label{5}
  $$
  For $A^{t}\otimes B^{t}$, we have $A^{t} = \sum_{i,j}a_{ji}|i\rangle \langle j|$ and $B^{t} = \sum_{m,n}b_{nm}|m\rangle\langle n|$, then according to eq. $\eqref{1}$​, we have
  $$
  A^{t}\otimes B^{t} = \sum_{i,m;j,n} a_{ji}b_{nm}(|i\rangle \otimes |m\rangle)(\langle j\otimes \langle n|) \tag{6}\label{6}
  $$
  From eq. $\eqref{5}$ and $\eqref{6}$, we have $(A\otimes B)^{t} = A^{t}\otimes B^{t}$. 

* For $(A\otimes B)^{*}$, according to eq. $\eqref{1}$, we have
  $$
  (A\otimes B)^{*} = \sum_{i,m;j,n} a^{*}_{ij}b^{*}_{mn}(|i\rangle \otimes |m\rangle)(\langle j\otimes \langle n|)\tag{7}\label{7}
  $$
  For $A^{*}\otimes B^{*}$, I notice that $A^{*} = \sum_{i,j}a^{*}_{ij}|i\rangle \langle j|$ and $B^{*} = \sum_{m,n}b^{*}_{mn}|m\rangle\langle n|$, then according to eq. $\eqref{1}$, we have
  $$
  A^{*}\otimes B^{*} = \sum_{i,m;j,n} a^{*}_{ij}b^{*}_{mn}(|i\rangle \otimes |m\rangle)(\langle j\otimes \langle n|)\tag{8}\label{8}
  $$
  From eq. $\eqref{7}$ and $\eqref{8}$, we have $(A\otimes B)^{*} = A^{*}\otimes B^{*}$. 

* For $(A\otimes B)^{\dagger}$, according to eq. $\eqref{1}$, we have
  $$
  (A\otimes B)^{\dagger} = \sum_{i,m;j,n} a^{*}_{ij}b^{*}_{mn}(|i\rangle \otimes |m\rangle)(\langle j\otimes \langle n|)\tag{9}\label{9}
  $$
  For $A^{\dagger}\otimes B^{\dagger}$, I notice that $A^{\dagger} = \sum_{i,j}a^{*}_{ji}|i\rangle \langle j|$ and $B^{\dagger} = \sum_{m,n}b^{*}_{nm}|m\rangle\langle n|$, then according to eq. $\eqref{1}$, we have
  $$
  A^{\dagger}\otimes B^{\dagger} = \sum_{i,m;j,n} a^{*}_{ji}b^{*}_{nm}(|i\rangle \otimes |m\rangle)(\langle j\otimes \langle n|)\tag{10}\label{10}
  $$
  From eq. $\eqref{9}$ and $\eqref{10}$, we have $(A\otimes B)^{\dagger} = A^{\dagger}\otimes B^{\dagger}$. 
