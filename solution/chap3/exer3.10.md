## Exercise 3.10

Let $g(n) = c_0 + c_1n + \dotsc + c_kn^{k}$ is a polynomial of degree $k$. To compare whether $g(n)$ is smaller than $c \cdot n^{l} $ where $l\geq k$, we compute 
$$
\frac{c\cdot n^l}{c_0 + c_1n + \dotsc + c_kn^{k}} = \frac{c\cdot n^{l-k}}{c_k + O (1)}\tag{1}\label{1}
$$
Note that at $n\to\infty$, $n^{l-k}\geq1$ when $l\geq k$. If constant $c$ and $c_k+O(1)$ are both positive or both negative, and if, for example, $c=10c_k$, then eq. $\eqref{1}$ must be greater than $1$ at $n\to \infty$. Namely, there exists a constant $c$ such that for $n\to \infty$, 
$$
g(n) \leq c n^{l} \tag{2}
$$
That is, we have $g(n) = O(n^l)$. 
