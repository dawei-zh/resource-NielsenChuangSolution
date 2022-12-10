## Exercise 3.9

#### Part (i) - $f(n) = O(g(n)) \iff g(n) = \Omega(g(n))$

In order to prove $f(n) = O(g(n)) \iff g(n) = \Omega(g(n))$, we need to prove the relation from both sides. 

---

To prove from the left to the right, consider $f(n)$ and $g(n)$ and if $f(n) = O(g(n))$, then there exist nonzero constant $c_1$ such that at $n\to \infty$, 
$$
f(n)\leq c_1 g(n)\tag{1}\label{1}
$$
Rewrite eq. $\eqref{1}$, we have
$$
g(n) \geq \frac{1}{c_1}f(n)\tag{2}\label{2}
$$
Let $1/c_1 = c_2$, eq. $\eqref{2}$ becomes
$$
c_2f(n)\leq  g(n)  \tag{3}\label{3}
$$
From eq. $\eqref{3}$ we could conclude that, $f(n) = O(g(n))\to g(n) = \Omega(f(n))$. 

---

To prove from the right to the left, consider $f(n)$​ and $g(n)$​ and if $g(n) = \Omega(f(n))$​, then there exist nonzero constant $c_3$​ such that at $n\to \infty$​, 
$$
c_3f(n)\leq  g(n)  \tag{4}\label{4}
$$
Rewrite eq. $\eqref{4}$, we have
$$
f(n)\leq  \frac{1}{c_3}g(n)\tag{5}\label{5}
$$
Let $1/c_3 = c_4$, eq. $\eqref{5}$ becomes
$$
f(n)\leq  c_4g(n)  \tag{6}\label{6}
$$
From eq. $\eqref{6}$ we could conclude that, $g(n) = \Omega(f(n))\to f(n) = O(g(n))$. 

#### Part (ii) - $f(n) = \Theta(g(n)) \iff g(n) = \Theta(f(n))$

In order to prove $f(n) = \Theta(g(n)) \iff g(n) = \Theta(f(n))$, we need to prove the relation from both sides. 

---

To prove from the left to the right, consider $f(n)$ and $g(n)$ and if $f(n) = \Theta(g(n))$, then there exist nonzero constant $c_1$ and $c_2$ such that at $n\to \infty$, 
$$
c_1 g(n)\leq f(n)\leq c_2 g(n)\tag{7}\label{7}
$$
Rewrite eq. $\eqref{7}$, we have
$$
\begin{cases}
c_1 g(n)\leq f(n) \iff g(n) \leq \frac{1}{c_1}f(n) \\
f(n)\leq c_2 g(n) \iff \frac{1}{c_2}f(n) \leq g(n) \\
\end{cases} \tag{8}\label{8}
$$
Let $1/c_2 = c_3$ and $1/c_1 = c_4$, eq. $\eqref{8}$ becomes
$$
c_3f(n)\leq  g(n) \leq c_4f(n) \tag{9}\label{9}
$$
From eq. $\eqref{9}$ we could conclude that, $f(n) = \Theta(g(n))\to g(n) = \Theta(f(n))$. 

---

To prove from the left to the right, consider $f(n)$ and $g(n)$ and if $g(n) = \Theta(f(n))$, then there exist nonzero constant $c_1$ and $c_2$ such that at $n\to \infty$, 
$$
c_1 f(n)\leq g(n)\leq c_2 f(n)\tag{10}\label{10}
$$
Rewrite eq. $\eqref{10}$, we have
$$
\begin{cases}
g(n)\leq c_2 f(n) \iff \frac{1}{c_2}g(n) \leq f(n) \\
c_1 f(n)\leq g(n) \iff f(n) \leq \frac{1}{c_1}g(n) \\
\end{cases} \tag{11}\label{11}
$$
Let $1/c_2 = c_3$ and $1/c_1 = c_4$, eq. $\eqref{11}$ becomes
$$
c_3g(n)\leq  f(n) \leq c_4g(n) \tag{12}\label{12}
$$
From eq. $\eqref{12}$ we could conclude that, $g(n) = \Theta(f(n))\to f(n) = \Theta(g(n))$. 
