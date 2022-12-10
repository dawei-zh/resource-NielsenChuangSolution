## Exercise 3.12

Consider $f(n) = n^k$ and $g(n) = n^{\log n}$, since 
$$
\frac{n^{\log n}}{n^k} = n^{\log n - k} \tag{1}
$$
and $\log n - k \to +\infty$ for any $k$ when $n\to \infty$, then $n^{\log n - k} > 1 $ and $n^{\log n}> n^k$. Thus, we can only have $n^k = O(n^{\log n})$ but not $n^{\log n} = O(n^k) $. 

