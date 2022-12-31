# Exercise 4.8

## Solution of Part 1

From class we know that, an arbitrary single qubit unitary operator can be written as

$$
U = \exp\left[-\frac{it}{\hbar}(aI+bX+cY+dZ)\right], a,b,c,d\in \mathbb{R}
$$(eqn:4.8.1)

Also, for operator $A$ and $B$, if we have $[A, B] = 0$​, then we have 

$$
\exp[A+B] = \exp(A)\exp(B)
$$(eqn:4.8.2)

Since the identity matrix commutes with any matrices, we could re-write eq. {eq}`eqn:4.8.1` as

$$
\begin{align}
U &= \exp\left[-\frac{it}{\hbar}(aI+bX+cY+dZ)\right] \\
&= \exp\left[-\frac{iat}{\hbar}I\right]\exp\left[-\frac{it}{\hbar}(bX+cY+dZ)\right]
\end{align}
$$(eqn:4.8.3)

Let $l = \sqrt{b^2+c^2+d^2}$, we could re-write eq. {eq}`eqn:4.8.3` as

$$
\begin{align}
U &= \exp\left[-\frac{iat}{\hbar}I\right]\exp\left[-\frac{it}{\hbar}(bX+cY+dZ)\right] \\
&= \exp\left[-\frac{iat}{\hbar}\right]\exp\left[-\frac{ilt}{\hbar}\left(\frac{b}{l}X+\frac{c}{l}Y+\frac{d}{l}Z\right)\right] \\
&= \exp\left[-\frac{iat}{\hbar}\right]\exp\left[-\frac{ilt}{\hbar}\left(n_xX+n_yY+n_zZ\right)\right] \\
\end{align}
$$(eqn:4.8.4)

where we have $\exp(-{iat}I/{\hbar}) = \exp(-{iat}/{\hbar})$, and write $n_x = b/l,n_y = c/l,n_z = d/l$ and $(n_x, n_y, n_z)$ is naturally a unit vector. Compare with the definition of $R_{\hat{n}}(\theta) = \exp(-i\theta\hat{n}\cdot\vec{\sigma}/2)$, we could re-write eq. {eq}`eqn:4.8.4` as 

$$
\begin{align}
U &= \exp\left[-\frac{iat}{\hbar}\right]\exp\left[-\frac{ilt}{\hbar}\left(n_xX+n_yY+n_zZ\right)\right] \\
&= \exp\left[-i\cdot\frac{at}{\hbar}\right]\exp\left[-i\frac{2lt}{\hbar}\cdot\frac{\hat{n}\cdot\vec{\sigma}}{2}\right]\\
&= \exp(i\alpha)R_{\hat{n}}(\theta)
\end{align}
$$(eqn:4.8.5)

where $\alpha = -at/\hbar$ and $\theta = 2lt/\hbar$. 

## Solution of Part 2

The Hadamard gate can be written in the form $H = {X+Z}/{\sqrt{2}}$, then we could start from the assumption that $n_x = n_z = 1/\sqrt{2}$. In this case, we have 

$$
H = \exp(i\alpha)R_{\hat{n}}(\theta) =  \exp(i\alpha)\left[\cos \frac{\theta}{2}I - i\sin\frac{\theta}{2}(n_xX + n_yY + n_zZ)\right]
$$(eqn:4.8.6)

If $\theta = \pi$, we could write eq. {eq}`eqn:4.8.6` as

$$
H = \exp(i\alpha)R_{\hat{n}}(\theta) =  \exp(i\alpha)\left[- i(n_xX + n_yY + n_zZ)\right]
$$(eqn:4.8.7)

Then we could find $\exp(i\alpha) = i$ and $\alpha = \pi$. 

## Solution of Part 3

For $\hat{n} = \hat{z} = (0,0,1)$, we could write the phase gate as 

$$
\begin{align}
S = \begin{pmatrix}
1 & 0 \\ 0 & i
\end{pmatrix} &= \exp(i\alpha)R_{\hat{z}}(\theta)= \exp(i\alpha)\begin{pmatrix}
e^{-i\theta/2} & 0 \\ 0 & e^{i\theta/2}
\end{pmatrix} = \begin{pmatrix}
e^{i(\alpha - \theta/2)} & 0 \\ 0 & e^{i(\alpha + \theta/2)}
\end{pmatrix}
\end{align}
$$(eqn:4.8.8)

In order to find $(\alpha, \theta)$, we need to find the solution of below equations, 

$$
\begin{cases}
e^{i(\alpha - \theta/2)} = 1\\
e^{i(\alpha + \theta/2)} = i
\end{cases} \iff \begin{cases}
\alpha - \theta/2 = 0\\
\alpha + \theta/2 = \pi/2
\end{cases}
$$(eqn:4.8.9)

Solve the equation, we could find $\alpha = \pi/4$ and $\theta = \pi/2$​. Then 

$$
S =\exp(i\pi/4)R_{\hat{z}}(\pi/2) =\begin{pmatrix}
1 & 0 \\ 0 & i
\end{pmatrix}
$$(eqn:4.8.10)