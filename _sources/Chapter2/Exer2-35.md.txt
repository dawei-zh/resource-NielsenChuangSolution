# Exercise 2.35

Suppose that $\vec{v}$ is a 3-dimensional unit vector, $\theta$ is real number, and we can use Taylor expansion to calculate $\exp (i\theta \vec{v}\cdot\vec{\sigma})$. The Taylor expansion of $e^{A}$ is given by

$$
e^{A} = \sum_{n=0}^{\infty}\frac{A^n}{n!} = I + A + \frac{A^2}{2!} + \dotsc
$$(eqn:2.35.1)

where $A$ is a operator. Meanwhile, the Taylor expansion of $\sin A$ and $\cos A$ are given by

$$
\begin{align}
\sin A &= \sum^{\infty}_{n=0}\frac{(-1)^{n}}{(2n+1)!}A^{2n+1}  = A - \frac{A^3}{3!} + \frac{A^5}{5!} - \dotsc\\
\cos A &= \sum^{\infty}_{n=0}\frac{(-1)^{n}}{(2n)!}A^{2n} = I - \frac{A^2}{2!} + \frac{A^4}{4!} - \dotsc
\end{align}
$$(eqn:2.35.2)

According to eq. {eq}`eqn:2.35.1`, the Taylor expansion for $\exp (i\theta \vec{v}\cdot\vec{\sigma})$ is given by

$$
\begin{align}
\exp (i\theta \vec{v}\cdot\vec{\sigma}) =& \sum_{n=0}^{\infty}\frac{(i\theta \vec{v}\cdot\vec{\sigma})^n}{n!} = I + i\theta \vec{v}\cdot\vec{\sigma}+\frac{i^2\theta^2(\vec{v}\cdot\vec{\sigma})^2}{2!} \\
&+ \frac{i^3\theta^3(\vec{v}\cdot\vec{\sigma})^3}{3!} 
+ \frac{i^4\theta^4(\vec{v}\cdot\vec{\sigma})^4}{4!} + \dotsc \\
=& \sum_{n=0}^{\infty}\frac{(i\theta \vec{v}\cdot\vec{\sigma})^n}{n!} = I + i\theta \vec{v}\cdot\vec{\sigma}-\frac{\theta^2(\vec{v}\cdot\vec{\sigma})^2}{2!} \\
&- \frac{i\theta^3(\vec{v}\cdot\vec{\sigma})^3}{3!} 
+ \frac{\theta^4(\vec{v}\cdot\vec{\sigma})^4}{4!} + \dotsc
\end{align}
$$(eqn:2.35.3)

From eq. {eq}`eqn:2.35.3` we can find that, 

* If $n$​ is even number we have

  $$
  n\text{ is even: }I -\frac{A^2}{2!} + \frac{A^4}{4!} - \frac{A^6}{6!} + \frac{A^8}{8!} - \frac{A^{10}}{10!}\dotsc 
  $$(eqn:2.35.4)

  where $A = \theta(\vec{v}\cdot\vec{\sigma})$

* If $n$ is odd number we have

  $$
  n\text{ is odd: }iA -\frac{iA^3}{3!} + \frac{iA^5}{5!} - \frac{iA^7}{7!} + \frac{iA^9}{9!} - \frac{iA^{11}}{11!}\dotsc 
  $$(eqn:2.35.5)

  where $A = \theta(\vec{v}\cdot\vec{\sigma})$. 

According to eq. {eq}`eqn:2.35.2`, eq. {eq}`eqn:2.35.4` and eq. {eq}`eqn:2.35.5`, we could rewrite eq. {eq}`eqn:2.35.3` as

$$
\exp (i\theta \vec{v}\cdot\vec{\sigma}) = \cos {[\theta(\vec{v}\cdot\vec{\sigma})]} + i(\vec{v}\cdot\vec{\sigma}) \sin {[\theta(\vec{v}\cdot\vec{\sigma})]}
$$(eqn:2.35.6)

We could simplify eq. {eq}`eqn:2.35.6` by following properties of $\vec{v}\cdot\vec{\sigma}$. Note that for $\vec{v}\cdot\vec{\sigma}$, we have

$$
\begin{align}
\vec{v}\cdot\vec{\sigma} &= v_{x}\sigma_x + v_y\sigma_y + v_z\sigma_z \\
&= \begin{pmatrix}
0 & v_x\\ v_x &0
\end{pmatrix} + i\begin{pmatrix}
0 & -v_y\\ v_y &0
\end{pmatrix}+ \begin{pmatrix}
v_z & 0\\ 0 &-v_z
\end{pmatrix} \\
&= \begin{pmatrix}
v_z & v_x-iv_y\\ v_x+iv_y &-v_z
\end{pmatrix}
\end{align}
$$(eqn:2.35.7)

So for $(\vec{v}\cdot\vec{\sigma})^2$, we have

$$
\begin{align}
(\vec{v}\cdot\vec{\sigma})^2 &= \begin{pmatrix}
v_z & v_x-iv_y\\ v_x+iv_y &-v_z
\end{pmatrix}\begin{pmatrix}
v_z & v_x-iv_y\\ v_x+iv_y &-v_z
\end{pmatrix} \\
&= \begin{pmatrix}
v^2_z+(v_x-iv_y)(v_x+iv_y) & v_z(v_x-iv_y)-v_z(v_x-iv_y)\\ 
v_z(v_x+iv_y)-v_z(v_x+iv_y) & (v_x-iv_y)(v_x+iv_y) + v^2_z
\end{pmatrix} \\
&= \begin{pmatrix}
v^2_z+v^2_x+v^2_y & 0\\ 
0 & v^2_x+v^2_y + v^2_z
\end{pmatrix} = \begin{pmatrix}
1 & 0\\ 
0 & 1
\end{pmatrix} = I
\end{align}
$$(eqn:2.35.8)

where we use $v^2_x+v^2_y+v^2_z = 1$ since $\vec{v}$ is a unit vector. From eq. {eq}`eqn:2.35.7` and eq. {eq}`eqn:2.35.8`, we can re-write eq. {eq}`eqn:2.35.4` and eq. {eq}`eqn:2.35.5`​ as

$$
\begin{align}
n\text{ is even: }& I -I\frac{\theta^2}{2!} + I\frac{\theta^4}{4!} - I\frac{\theta^6}{6!} + I\frac{\theta^8}{8!} - I\frac{\theta^{10}}{10!}\dotsc \\
n\text{ is odd: }&i\theta(\vec{v}\cdot\vec{\sigma}) -(\vec{v}\cdot\vec{\sigma})\frac{i\theta^3}{3!} + (\vec{v}\cdot\vec{\sigma})\frac{i\theta^5}{5!} - (\vec{v}\cdot\vec{\sigma})\frac{i\theta^7}{7!} +\dotsc 
\end{align}
$$(eqn:2.35.9)

According to eq. {eq}`eqn:2.35.2` and eq. {eq}`eqn:2.35.9`, we could re-write eq. {eq}`eqn:2.35.6` as

$$
\exp (i\theta \vec{v}\cdot\vec{\sigma}) = I\cos {\theta} + i(\vec{v}\cdot\vec{\sigma}) \sin {\theta} 
$$(eqn:2.35.10)