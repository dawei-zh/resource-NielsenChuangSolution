# Exercise 4.49

## Proof for 4.103
To study the relation between $e^{i(\hat{A}+\hat{B})\Delta t}$ and $ e^{i\hat{A}\Delta t}e^{i\hat{B}\Delta t}$, we firstly consider operation $e^{i(\hat{A}+\hat{B})\Delta t}$ and expand it follows Taylor expansion as

$$
\begin{align}
e^{i(\hat{A}+\hat{B})\Delta t} &= \sum_{n=0}^{\infty}\frac{(i\Delta t)^n(\hat{A}+\hat{B})^n}{n!} = 1 + i\hat{A}\Delta t+i\hat{B}\Delta t + \mathcal{O}(\Delta t^2)\\
\end{align}
$$(eqn:4.49.1)

Meanwhile, we can also expand $ e^{i\hat{A}\Delta t}e^{i\hat{B}\Delta t}$ as

$$
\begin{align}
 e^{i\hat{A}\Delta t}e^{i\hat{B}\Delta t} =& 
\left[\sum_{n=0}^{\infty}\frac{(i\hat{A}\Delta t)^n}{n!} \right]
\left[\sum_{n=0}^{\infty}\frac{(i\hat{B}\Delta t)^n}{n!} \right]
 \\
=& \left[1 + i\hat{A}\Delta t + \mathcal{O}(\Delta t^2)\right]
\left[1 + i\hat{B}\Delta t + \mathcal{O}(\Delta t^2)\right]
 \\
=& 1 + i\hat{A}\Delta t + i\hat{B}\Delta t+ \mathcal{O}(\Delta t^2)
\end{align}
$$(eqn:4.49.2)

Compare eq. {eq}`eqn:4.49.1` and eq. {eq}`eqn:4.49.2`, we should have

$$
e^{i(\hat{A}+\hat{B})\Delta t} =  e^{i\hat{A}\Delta t}e^{i\hat{B}\Delta t} + \mathcal{O}(\Delta t^2)
$$(eqn:4.49.3)

## Proof for 4.104

To study the relation between $e^{i(\hat{A}+\hat{B})\Delta t}$ and $ e^{i\hat{A}\Delta t/2}e^{\hat{B}\Delta t}e^{i\hat{A}\Delta t/2}$, we firstly consider operation $e^{i(\hat{A}+\hat{B})\Delta t}$ and expand it follows Taylor expansion as

$$
\begin{align}
e^{i(\hat{A}+\hat{B})\Delta t} &= \sum_{n=0}^{\infty}\frac{(\hat{A}+\hat{B})^n(i\Delta t)^n}{n!} \\
&= 1 + i(\hat{A}+\hat{B})\Delta t + \frac{(\hat{A}+\hat{B})^2(i\Delta t)^2}{2} + \mathcal{O}[(\Delta t)^3]\\
&= 1 + i{\hat{A}\Delta t+i\hat{B}\Delta t} + \frac{i^2}{2}(\hat{A}\Delta t+\hat{B}\Delta t)(\hat{A}\Delta t+\hat{B}\Delta t) + \mathcal{O}[(\Delta t)^3]\\
&= 1 + i{\hat{A}\Delta t+i\hat{B}\Delta t}+ \frac{i^2}{2}(\hat{A}\hat{A} + \hat{A}\hat{B}+ \hat{B}\hat{A}+ \hat{B}\hat{B})(\Delta t)^2 + \mathcal{O}[(\Delta t)^3]\\
\end{align}
$$(eqn:4.49.4)

Meanwhile, we can also expand $e^{i\hat{A}\Delta t/2}e^{\hat{B}\Delta t}e^{i\hat{A}\Delta t/2}$​ as

$$
\begin{align}
e^{(\hat{A}\Delta t)/2}e^{\hat{B}\Delta t}e^{(\hat{A}\Delta t)/2} =& 
\left[\sum_{n=0}\frac{(\hat{A}\Delta t)^n}{2^n n!} \right]
\left[\sum_{n=0}\frac{(\hat{B}\Delta t)^n}{n!} \right]
\left[\sum_{n=0}\frac{(\hat{A}\Delta t)^n}{2^n n!} \right] \\
=& \left[1 + \frac{\hat{A}\Delta t}{2} + \frac{(\hat{A}\Delta t)^2}{8} +\mathcal{O}(\Delta t^3)\right]
\left[ 1 + \hat{B}\Delta t + \frac{(\hat{B}\Delta t)^2}{2} +\mathcal{O}(\Delta t^3)  \right]
\left[ 1 + \frac{\hat{A}\Delta t}{2} + \frac{(\hat{A}\Delta t)^2}{8} +\mathcal{O}(\Delta t^3)  \right] \\
=& \left[1 + \hat{B}\Delta t+ \frac{(\hat{B}\Delta t)^2}{2} + \frac{\hat{A}\Delta t}{2} + \frac{\hat{A}\hat{B}\Delta t^2}{2} + \frac{(\hat{A}\Delta t)^2}{8} + \mathcal{O}(\Delta t^3)\right] \\
&\cdot \left[ 1 + \frac{\hat{A}\Delta t}{2} + \frac{(\hat{A}\Delta t)^2}{8} +\mathcal{O}(\Delta t^3)  \right] \\
=&  1 + \frac{\hat{A}\Delta t}{2} + \frac{(\hat{A}\Delta t)^2}{8} +  \hat{B}\Delta t + \frac{\hat{B}\hat{A}\Delta t^2}{2} +\frac{(\hat{B}\Delta t)^2}{2} \\
&+\frac{\hat{A}\Delta t}{2} + \frac{\hat{A}^2\Delta t^2}{4}+\frac{\hat{A}\hat{B}\Delta t^2}{2} + \frac{(\hat{A}\Delta t)^2}{8}+\mathcal{O}(\Delta t^3) \\
=&   1 + \left(\frac{\hat{A}}{2} +\hat{B}+ \frac{\hat{A}}{2}\right)\Delta t
+ \left(\frac{\hat{A}^2}{8} +\frac{\hat{B}\hat{A}}{2}+ \frac{\hat{B}^2}{2} + \frac{\hat{A}^2}{4} +\frac{\hat{A}\hat{B}}{2} +\frac{\hat{A}^2}{8}\right)\Delta t + \mathcal{O}(\Delta t^3)
\\
=& 1 + {(\hat{A}+\hat{B})\Delta t} + \frac{1}{2}(\hat{A}\hat{A} + \hat{A}\hat{B}+ \hat{B}\hat{A}+ \hat{B}\hat{B})\Delta t+ \mathcal{O}(\Delta t^3) 
\end{align}
$$(eqn:4.49.5)

Note that $\Delta t$ is a scalar and we can add them up together, and from eq. {eq}`eqn:4.49.4` and eq. {eq}`eqn:4.49.5` we could conclude that $e^{(\hat{A}+\hat{B})\Delta t} = e^{(\hat{A}\Delta t)/2}e^{\hat{B}\Delta t}e^{(\hat{A}\Delta t)/2} +\mathcal{O}(\Delta t^3)$. **Note that we could also have**

$$
e^{i(\hat{A}+\hat{B})\Delta t} = e^{i\hat{B}\Delta t/2}e^{i\hat{A}\Delta t}e^{i\hat{B}\Delta t/2}
$$(eqn:4.49.6)

## Proof for 4.105

To study the relation between $e^{(\hat{A}+\hat{B})\Delta t}$​ and $ e^{\hat{A}\Delta t}e^{\hat{B}\Delta t}e^{-[\hat{A},\hat{B}]\Delta t^2/2}$​, we firstly consider operation $e^{(\hat{A}+\hat{B})\Delta t}$​ and expand it follows Taylor expansion as

$$
\begin{align}
e^{(\hat{A}+\hat{B})\Delta t} &= \sum_{n=0}^{\infty}\frac{(\hat{A}+\hat{B})^n(\Delta t)^n}{n!} \\
&= 1 + (\hat{A}+\hat{B})\Delta t + \frac{(\hat{A}+\hat{B})^2(\Delta t)^2}{2} + \mathcal{O}[(\Delta t)^3]\\
&= 1 + \hat{A}\Delta t+\hat{B}\Delta t + \frac{(\Delta t)^2}{2}(\hat{A}+\hat{B})(\hat{A}+\hat{B}) + \mathcal{O}[(\Delta t)^3]\\
&= 1 + \hat{A}\Delta t+\hat{B}\Delta t + \frac{(\Delta t)^2}{2}(\hat{A}\hat{A}+\hat{A}\hat{B}+\hat{B}\hat{A}+\hat{B}\hat{B}) + \mathcal{O}[(\Delta t)^3]\\
\end{align}
$$(eqn:4.49.7)

Meanwhile, we can also expand $e^{\hat{A}\Delta t}e^{\hat{B}\Delta t}e^{-[\hat{A},\hat{B}]\Delta t^2/2}$ as

$$
\begin{align}
e^{\hat{A}\Delta t}e^{\hat{B}\Delta t}e^{-\frac{1}{2}[\hat{A},\hat{B}]\Delta t^2} =& 
\left[\sum_{n=0}^{\infty}\frac{(\hat{A}\Delta t)^n}{n!} \right]
\left[\sum_{n=0}^{\infty}\frac{(\hat{B}\Delta t)^n}{n!} \right]
\left[\sum_{n=0}^{\infty}\frac{(-1)^{n}[\hat{A}, \hat{B}]^{n}[(\Delta t)^2]^n}{2^n n!} \right] \\
=& \left[ 1 + \hat{A}\Delta t + \frac{\hat{A}^2(\Delta t)^2}{2} +\mathcal{O}[(\Delta t)^3] \right]\cdot\left[ 1 + \hat{B}\Delta t + \frac{\hat{B}^2(\Delta t)^2}{2} +\mathcal{O}[(\Delta t)^3] \right] \cdot\left[ 1 - \frac{[\hat{A}, \hat{B}](\Delta t)^2}{2} +\mathcal{O}[(\Delta t)^4] \right]\\
=&\left[ 1 + \hat{B}\Delta t + \frac{\hat{B}^2(\Delta t)^2}{2} + \hat{A}\Delta t + \hat{A}\hat{B}(\Delta t)^2+ \frac{\hat{A}^2(\Delta t)^2}{2}+\mathcal{O}[(\Delta t)^3] \right] \cdot\left[ 1 - \frac{[\hat{A}, \hat{B}](\Delta t)^2}{2} +\mathcal{O}[(\Delta t)^4] \right] \\
=& 1 - \frac{[\hat{A}, \hat{B}](\Delta t)^2}{2} + \hat{B}\Delta t + \frac{\hat{B}^2(\Delta t)^2}{2} \\
&+ \hat{A}\Delta t + \hat{A}\hat{B}(\Delta t)^2+\frac{\hat{A}^2(\Delta t)^2}{2}+\mathcal{O}[(\Delta t)^3] \\
=& 1  +  \hat{A}\Delta t + \hat{B}\Delta t \\
&+ \frac{(\Delta t)^2}{2} \left(\hat{A}^2 + \hat{B}^2 + 2\hat{A}\hat{B} - \hat{A}\hat{B} + \hat{B}\hat{A}\right) +\mathcal{O}[(\Delta t)^3] \\
=& 1  +  \hat{A}\Delta t + \hat{B}\Delta t + \frac{(\Delta t)^2}{2} \left(\hat{A}\hat{A} + \hat{B}\hat{B}  + \hat{A}\hat{B} + \hat{B}\hat{A}\right) +\mathcal{O}[(\Delta t)^3] \\
\end{align}
$$(eqn:4.49.8)

Note that $\Delta t$ is a scalar and we can add them up together, and from eq. {eq}`eqn:4.49.7` and eq. {eq}`eqn:4.49.8` we could conclude that $ e^{(\hat{A}+\hat{B})\Delta t}=e^{\hat{A}\Delta t}e^{\hat{B}\Delta t}e^{-\frac{1}{2}[\hat{A},\hat{B}]\Delta t^2} +\mathcal{O}[(\Delta t)^3]$. 