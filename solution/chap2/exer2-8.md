## Exercise 2.8

The Gram-Schmidt procedure converts a non-orthonormal basis $|w_1\rangle, \dotsc, |w_d\rangle$ in vector space $V$ into an orthonormal basis $|v_1\rangle, \dotsc, |v_d\rangle$. I will proof new basis $|v_1\rangle, \dotsc, |v_d\rangle$ is orthonormal below. The new vector $|v_{k+1}\rangle$ is given by $|v_1\rangle = |w_1\rangle/|||w_1\rangle||$ and for $1\leq k \leq d-1$ then $|v_{k+1}\rangle$ is defined by
$$
|v_{k+1}\rangle = \frac{|w_{k+1}\rangle - \sum_{i=1}^{k}\langle v_{i}|w_{k+1}\rangle |v_{i}\rangle}{|||w_{k+1}\rangle - \sum_{i=1}^{k}\langle v_{i}|w_{k+1}\rangle |v_{i}\rangle||}\tag{1}\label{1}
$$
I will prove for $i,j\in [1, d]$ we have $\langle v_i|v_j\rangle = \delta_{ij}$ by induction. That is,

* For $|v_1\rangle$, we have $\langle v_1|v_1\rangle = 1$.
* For $n=1$ or namely, for $|v_2\rangle$, $\langle v_1|v_2\rangle = 0$ and $\langle v_{2}|v_2\rangle = 1$. 
* If for $n=k$ we have $\langle v_{j}|v_{k+1}\rangle = \delta_{(k+1)j}$ for $j \leq i+1 $, then we have for $n=k+1$, $\langle v_{j}|v_{k+2}\rangle = \delta_{(k+2)j}$ for $j\leq k+2$. 

---

Here is the detail of proof of each statement. 

* For $|v_1\rangle$, we have $|v_1\rangle = |w_1\rangle / |||w_1\rangle||$, then 
  $$
  \langle v_1|v_1\rangle = \frac{\langle w_1|w_1\rangle} {|||w_1\rangle||^2} = 1 \tag{2}
  $$

* For $n=1$, we have
  $$
  |v_{2}\rangle = \frac{|w_{2}\rangle - \langle v_{1}|w_{2}\rangle |v_{1}\rangle}{|||w_{2}\rangle - \langle v_{1}|w_{2}\rangle |v_{1}\rangle||}\tag{3}
  $$
  Suppose $|a\rangle = |w_{2}\rangle - \langle v_{1}|w_{2}\rangle |v_{1}\rangle$ then 
  $$
  \langle v_2|v_2\rangle = \frac{\langle a|a\rangle}{|||a\rangle||^2} = 1\tag{4}
  $$
  Meanwhile, we have
  $$
  \langle v_1|v_{2}\rangle = \frac{\langle v_1|w_{2}\rangle - \langle v_{1}|w_{2}\rangle \langle v_1|v_{1}\rangle}{|||w_{2}\rangle - \langle v_{1}|w_{2}\rangle |v_{1}\rangle||} = 0\tag{5}
  $$

* Suppose $n=k$ if we have $\langle v_{j}|v_{k+1}\rangle = \delta_{(k+1)j}$, then when $n=k+1$, for $j\neq k+2$, 
  $$
  \begin{align}
  \langle v_j|v_{k+2}\rangle &= \frac{\langle v_j|w_{k+2}\rangle - \sum_{i=1}^{k+1}\langle v_{i}|w_{k+2}\rangle \langle v_j|v_{i}\rangle}{|||w_{k+2}\rangle - \sum_{i=1}^{k+1}\langle v_{i}|w_{k+2}\rangle |v_{i}\rangle||} \\
  &= \frac{\langle v_j|w_{k+2}\rangle - \langle v_{j}|w_{k+2}\rangle \langle v_j|v_{j}\rangle}{|||w_{k+2}\rangle - \sum_{i=1}^{k+1}\langle v_{i}|w_{k+2}\rangle |v_{i}\rangle||}  \\
  &= \frac{\langle v_j|w_{k+2}\rangle - \langle v_{j}|w_{k+2}\rangle }{|||w_{k+2}\rangle - \sum_{i=1}^{k+1}\langle v_{i}|w_{k+2}\rangle |v_{i}\rangle||} = 0
  \end{align}\tag{6}\label{6}
  $$
  For $j = k+2$, let $|a\rangle = |w_{k+1}\rangle - \sum_{i=1}^{k+1}\langle v_{i}|w_{k+2}\rangle |v_{i}\rangle$, then
  $$
  \langle v_{k+2}|v_{k+2}\rangle = \frac{\langle a|a\rangle}{|||a\rangle||^2} = 1 \tag{7} \label{7}
  $$
  From eq. $\eqref{6}$ and eq. $\eqref{7}$, we conclude that for $n=k+1$, $\langle v_{j}|v_{k+2}\rangle = \delta_{(k+2)j}$ for $j\leq k+2$. 

