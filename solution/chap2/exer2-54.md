## Exercise 2.54

#### Solution 1

Suppose $A$ and $B$ are commuting Hermitian operators, then $A$ and $B$ can be written in spectral decomposition form, 
$$
A = \sum_{i}\lambda_{i}|i_A\rangle\langle i_A|, B = \sum_{j}\mu_{j}|j_B\rangle\langle j_B| \tag{1}\label{eq:spec}
$$
where $|i_A\rangle$ is eigenvector of $A$ with eigenvalue as $\lambda_i$ and $|j_B\rangle$ is eigenvector of $B$ with eigenvalue as $\mu_j$. Since $[A, B] = 0$, $A$ and $B$ are simultaneously diagonalizable. In this case, we re-write eq. $\eqref{eq:spec}$ as 
$$
A = \sum_{i}\lambda_{i}|i\rangle\langle i|, B = \sum_{i}\mu_{i}|i\rangle\langle i| \tag{2}
$$
and therefore, 
$$
A+B = \sum_{i}(\lambda_{i}+\mu_i)|i\rangle\langle i| \tag{3}\label{eq:aplusb}
$$
which means that Hermitian operator $A+B$ has eigenvector $|i\rangle$ with eigenvalue $\lambda_i+\mu_i$. With above information, we could compute the exponential of $A$ and $B$ as
$$
e^A = \sum_{i}e^{\lambda_{i}}|i\rangle\langle i|, e^B = \sum_{i}e^{\mu_{i}}|i\rangle\langle i| \tag{4}
$$
and $e^{A}e^{B}$​ can be obtained by
$$
\begin{align}
e^Ae^B  =& \left(\sum_{i}e^{\lambda_{i}}|i\rangle\langle i|\right)\left(\sum_{j}e^{\mu_{j}}|j\rangle\langle j|\right) \\
=& \sum_{i,j}e^{\lambda_{i}}e^{\mu_{j}}|i\rangle\langle i|j\rangle\langle j|\\
=& \sum_{i}e^{\lambda_{i}}e^{\mu_{i}}|i\rangle\langle i|\\
\end{align}\tag{5}
$$
Since we have for the exponential of $A+B$ as
$$
e^{A+B} = \sum_{i}e^{\lambda_{i}+\mu_i}|i\rangle\langle i|  =\sum_{i}e^{\lambda_{i}}e^{\mu_i}|i\rangle\langle i| = e^Ae^B \tag{6}
$$
Therefore, we conclude that $\exp(A)\exp(B)=\exp(A+B)$ when $A$ and $B$ commutes. 

#### Solution 2

Suppose $A$ and $B$ are commuting Hermitian operators, then $AB= BA$. We can use Taylor expansion to calculate $\exp(A)\exp(B)$ and $\exp(A+B)$. The Taylor expansion of $e^{A}$ and $e^{B}$ is given by
$$
\begin{align}
e^{A} &= \sum_{m=0}^{\infty}\frac{A^m}{m!} = I + A + \frac{A^2}{2!} + \dotsc + \frac{A^m}{m!} + \dotsc \tag{1a}\\
e^{B} &= \sum_{n=0}^{\infty}\frac{B^n}{n!} = I + B + \frac{B^2}{2!}  + \dotsc + \frac{B^n}{n!} + \dotsc\tag{1b}
\end{align}
$$
Then we could calculate $\exp(A)\exp(B)$ as 
$$
\begin{align}
e^{A}e^{B} = \left(\sum_{m=0}^{\infty}\frac{A^m}{m!}\right)\left(\sum_{n=0}^{\infty}\frac{}{n!}\right) &= \sum_{m=0}^{\infty}\sum_{n=0}^{\infty}\frac{A^mB^n}{m!n!} 
\end{align} \tag{2}\label{eq:prod}
$$
If we put those terms with same $m+n$ together and re-write eq. $\eqref{eq:prod}$, we will obtain
$$
\begin{align}
e^{A}e^{B} &= A^0B^0 + A^{1}B^0 + A^0B^1 + \frac{A^2B^0}{2!} + A^1B^1 +  \frac{A^0B^2}{2!} + \dotsc \\
&= 1 + \sum_{m=0}^{1} \frac{A^mB^{(1-m)}}{m!(1-m)!} + \sum_{m=0}^{2} \frac{A^mB^{(2-m)}}{m!(2-m)!} + \dotsc + \sum_{m=0}^{N} \frac{A^mB^{(N-m)}}{m!(N-m)!} + \dotsc \\
&= 1+\sum_{N=1}^{\infty}\sum_{m=0}^{N}\frac{A^mB^{(N-m)}}{m!(N-m)!} 
\end{align}\tag{3}\label{eq:prod2}
$$
Meanwhile, we could also use the Taylor expansion to calculate $\exp(A+B)$, 
$$
e^{A+B} = \sum_{N=0}^{\infty}\frac{(A+B)^N}{N!} = I + (A+B) + \frac{(A+B)^2}{2!} + \dotsc + \frac{(A+B)^N}{N!} + \dotsc  \tag{4}\label{eq:expand}
$$
Note that when we expand $(A+B)^N$, we might see the term with random order of operator $A$ and $B$, e.g., $ABABABBBBAABAAABAABABAA$. Since $AB=BA$, we could always swap two adjacent operators and finally obtain a term in the form $A^{k}B^{N-k}$ . Namely, it means that we could expand $(A+B)^N$ using the binomial theorem,  
$$
(A+B)^N = \sum_{k=0}^{N}\binom{N}{k}A^{k}B^{N-k} \tag{5}\label{eq:binom}
$$
We could use eq. $\eqref{eq:binom}$ to re-write eq. $\eqref{eq:expand}$ as
$$
\begin{align}
e^{A+B} = \sum_{N=0}^{\infty}\frac{(A+B)^N}{N!} &= 1 + \sum_{N=1}^{\infty}\frac{(A+B)^N}{N!} \\
&= 1 + \sum_{N=1}^{\infty}\sum_{k=0}^{N}\frac{1}{N!}\binom{N}{k}A^{k}B^{N-k} \\
&= 1 + \sum_{N=1}^{\infty}\sum_{k=0}^{N}\frac{1}{N!}\frac{N!}{k!(N-k)!}A^{k}B^{N-k} \\ 
&= 1 + \sum_{N=1}^{\infty}\sum_{k=0}^{N}\frac{A^{k}B^{N-k} }{k!(N-k)!}
\end{align}\tag{6}\label{eq:sum}
$$
Compare eq. $\eqref{eq:prod2}$ with eq. $\eqref{eq:sum}$, we conclude that $\exp(A)\exp(B)=\exp(A+B)$ when $A$ and $B$ commutes. 
