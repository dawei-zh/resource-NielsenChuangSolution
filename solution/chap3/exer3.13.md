## Exercise 3.13

Consider $f(n) = c^n$ with $c>1$. Note that $c = 2^{\log c}$ and $n = 2^{\log n}$, we have
$$
c^n = 2^{n\log c }, n^{\log n} = 2^{(\log n)^2} \tag{1}
$$
From Exercise 3.11, we have $\log n = O(n^k)$, then at $n\to \infty$, there exists constant $c$ such that
$$
\log n \leq  cn^{1/2}\iff (\log n)^2 \leq  c^2n\tag{2}\label{2}
$$
For $\forall c >1$, we have $\log c >0$ and $(\log n)^2 <  \log c\cdot n^2$, so we always have
$$
2^{n\log c } = c^n>2^{(\log n)^2}= n^{\log n} \tag{3}
$$
and we will never have $c_0 \cdot c^n\leq n^{\log n}$ with any constant $c_0$. That is, we will always have $c^n = \Omega(n^{\log n}) $ but never $n^{\log n} = \Omega (c^n)$. 
