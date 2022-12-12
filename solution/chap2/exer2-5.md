## Exercise 2.5

In the textbook, we define an operation as 
$$
((y_1, \dotsc, y_n), (z_1, \dotsc, z_n)) \equiv \sum_{i}y_i^{*}z_i \tag{1}\label{eq:operation}
$$
To check whether eq. $\eqref{eq:operation}$ defines an inner product, we need to check the following properties of inner product.

* $(\cdot, \cdot)$ is linear in the second argument. Suppose we have $N$ vectors and the $k-$th vector is defined by 
  $$
  \mathbf{z}_{k} = (z_{k1}, z_{k2}, \dotsc, z_{kn}) \tag{2}
  $$
  Then we can compute
  $$
  \sum_{k=1}^{N} \lambda_k\mathbf{z}_{k} = \left(\sum_{k=1}^{N}\lambda_kz_{k1}, \sum_{k=1}^{N}\lambda_kz_{k2}, \dotsc, \sum_{k=1}^{N}\lambda_kz_{kn}\right)\tag{3}
  $$
  From eq. $\eqref{eq:operation}$, we can compute  
  $$
  \left((y_1, \dotsc, y_n), \sum_{k} \lambda_k\mathbf{z}_{k}\right) = \sum_{i=1}^n y_i^{*}\sum_{k=1}^{N}\lambda_kz_{k1} = \sum_{i=1}^n\sum_{k=1}^{N} y_i^{*}\lambda_kz_{k1} \tag{4}\label{4}
  $$
  Meanwhile, we can compute 
  $$
  \sum_{k=1}^{N}\lambda_k\left((y_1, \dotsc, y_n),  (z_{k1}, z_{k2}, \dotsc, z_{kn})\right) = \sum_{k=1}^{N}\lambda_k \sum_{i=1}^{n}y_i^{*}z_i  =  \sum_{i=1}^n\sum_{k=1}^{N} y_i^{*}\lambda_kz_{k1} \tag{5}\label{5}
  $$
  From eq. $\eqref{4}$ and eq. $\eqref{5}$, we conclude that the given definition of $(\cdot, \cdot)$ is linear in the second argument. 

* $(|v\rangle, |w\rangle) = (|w\rangle, |v\rangle)^*$. From eq. $\eqref{eq:operation}$​ we can compute 
  $$
  ((z_1, \dotsc, z_n), (y_1, \dotsc, y_n)) = \sum_{i}z_i^{*}y_i = \sum_{i}(y_i^*z_i)^* = \left(\sum_{i}y_i^*z_i\right)^*  \tag{6}\label{6}
  $$
  where we use relation $\left(\sum_{i} z_i\right)^* = \sum_i z^*_i$ and $(z_1z_2)^* = z^*_1 z^*_2$ (see appendix). Compare with eq. $\eqref{eq:operation}$ we could see that 
  $$
  ((z_1, \dotsc, z_n), (y_1, \dotsc, y_n))  = \left(\sum_{i}y_i^*z_i\right)^* =((y_1, \dotsc, y_n), (z_1, \dotsc, z_n))^* \tag{7}
  $$
  Therefore, we could conclude that under the definition in eq. $\eqref{eq:operation}$, we have $(|v\rangle, |w\rangle) = (|w\rangle, |v\rangle)^*$
  
* $(|v\rangle, |v\rangle) \geq 0$, and $(|v\rangle, |v\rangle) = 0$ iff $|v\rangle = 0$. For $(|v\rangle, |v\rangle)$ we have 
  $$
  ((y_1, \dotsc, y_n), (y_1, \dotsc, y_n)) = \sum_{i}y_i^{*}y_i =\sum_{i} |y_i|^2 \tag{8}\label{8}
  $$
  Since for any complex number $|y_i|^2 \geq 0$, we should have $((y_1, \dotsc, y_n), (y_1, \dotsc, y_n)) \geq 0$. Moreover,

  * If $((y_1, \dotsc, y_n), (y_1, \dotsc, y_n)) = 0$, from eq. $\eqref{8}$ we know that can only have $|y_1| = \dotsc = |y_n| = 0$, or equivalently, $|y\rangle = 0$
  * If $|y_1| = \dotsc = |y_n| = 0$, from eq. $\eqref{8}$ we know that  $((y_1, \dotsc, y_n), (y_1, \dotsc, y_n)) = 0$.

  Therefore, we can conclude that with eq. $\eqref{eq:operation}$, we have $(|v\rangle, |v\rangle) \geq 0$, and $(|v\rangle, |v\rangle) = 0$ iff $|v\rangle = 0$.

From the proof above, we can conclude that eq. $\eqref{eq:operation}$ defines an inner product on $\mathbb{C}^n$. 

---

### Appendix

We use the following two relations above to prove $(|v\rangle, |w\rangle) = (|w\rangle, |v\rangle)^*$, 
$$
\left(\sum_{j} z_j\right)^* = \sum_j z^*_j\text{ and } \left(\prod_i z_i \right)^* = \prod_i z_i^*
$$
To prove these two relations, we need to write complex number in the form $z_j = x_j + iy_j$. Then we can compute
$$
\sum_{j} z_j = \sum_{j} (x_j + iy_j) = \sum_{j} x_j + i\sum_{j}y_j
$$
and also, 
$$
\sum_{j} z^*_j = \sum_{j} (x_j - iy_j) = \sum_{j} x_j - i\sum_{j}y_j
$$
Compare above two equations, we have
$$
\left(\sum_{j} z_j \right)^* = \left(\sum_{j} x_j + i\sum_{j}y_j\right)^* = \sum_{j} x_j - i\sum_{j}y_j =  \sum_j z^*_j
$$
To prove the second relation, we need to firstly prove $(z_1z_2)^* = z^*_1 z_2^*$. For $(z_1z_2)^*$ we have 
$$
(z_1z_2)^* = [(x_1+iy_1)(x_2+iy_2)]^* = [x_1x_2 +ix_2y_1+ix_1y_2 - y_1y_2)]^* = x_1x_2  - y_1y_2-i(x_2y_1+x_1y_2)
$$
Then we have, 
$$
z^*_1 z_2^* = (x_1-iy_1)(x_2-iy_2) = x_1x_2  -ix_2y_1-ix_1y_2-y_1y_2 = (z_1z_2)^*
$$
For $z^*_1 z_2^*z_3^*$ and $(z_1z_2z_3)^*$, we can make use of the relation $(z_1z_2)^* = z^*_1 z_2^*$ to prove. That is, 
$$
(z_1z_2z_3)^* = (z_1z_2)^*z_3^* = z_1^*z_2^*z_3^*
$$
Similarly, we can prove by induction that if 
$$
\left(\prod_{i=1}^n z_i \right)^* = \prod_{i=1}^n  z_i^*
$$
We should have 
$$
\left(\prod_{i=1}^{n+1} z_i \right)^* = \left[\left(\prod_{i=1}^{n} z_i\right)  \cdot z_{n+1}\right]^* =\left(\prod_{i=1}^{n} z_i\right)^* z^*_{n+1} = \left(\prod_{i=1}^n  z_i^*\right)\cdot z^*_{n+1} = \prod_{i=1}^{n+1}  z_i^*
$$
