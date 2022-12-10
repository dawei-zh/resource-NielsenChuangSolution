## Exercise 3.11

Let $f(n) = \log n$ and $g(n) = n^{k}$ where $k>0$, consider 
$$
h(n) = g(n) - f(n) =n^k - \log n \tag{1}
$$
The derivative of $h(n)$ is obtained by
$$
\frac{\mathrm{d}h}{\mathrm{d}n} = \frac{1}{n^{1-k}} - \frac{1}{n} = \frac{n^k - 1}{n} \tag{2}
$$
If $n\to \infty$ we should have $n^k$ is greater than $1$, so ${\mathrm{d}h}/{\mathrm{d}n} >0$ at $n\to \infty$. It means that $h(n)$ must be increasing and $h(n)$ would finally greater than $0$. Namely, when $n\to \infty$ we have $h(n) \geq 0$ and $\log n \leq cn^k$ with $c=1$, so $\log n = O(n^k)$. 
