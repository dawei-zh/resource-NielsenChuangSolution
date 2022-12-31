# Exercise 2.6

Consider an inner product $(\cdot, \cdot)$ and we should have

$$
\left(|v\rangle, \sum_{i}\lambda _i |w_i\rangle\right) = \sum_i \lambda_i (|v\rangle, |w\rangle) 
$$(eqn:2.6.1)

Then using $(|v\rangle, |w\rangle) =  (|w\rangle, |v\rangle)^*$, we can compute

$$
 \left(\sum_{i}\lambda _i |w_i\rangle, |v\rangle\right) =\left(|v\rangle, \sum_{i}\lambda _i |w_i\rangle\right)^* =\sum_i \lambda^*_i (|v\rangle, |w\rangle)^* =  \sum_i \lambda^*_i (|w\rangle, |v\rangle) 
$$(eqn:2.6.2)

where we use relation $\left(\sum_{i} z_i\right)^* = \sum_i z^*_i$ and $(z_1z_2)^* = z^*_1 z^*_2$. Therefore, we can conclude that any inner product $(\cdot, \cdot)$ is conjugate-linear in the first argument. 