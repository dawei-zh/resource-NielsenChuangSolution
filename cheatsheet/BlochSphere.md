### Bloch Sphere

#### What is Bloch sphere?

Bloch sphere is a method to visualize all cases of one qubit, $|\psi\rangle = a|0\rangle + b|1\rangle$. In Bloch sphere, 

* the $|0\rangle$ state is at the north pole (on $z-$axis)
* $|1\rangle$ is at the south pole
* The $x-$ and $y-$axis are on the middle of the sphere
* The radius of the sphere is $1$. 
* The $\varphi$ and $\theta$ are angular coordinate the same as spherical coordinate

We need to obey the following rule to find the position of a one qubit vector
$$
|\psi\rangle = a|0\rangle + b|1\rangle = e^{i\gamma}\left(\cos\frac{\theta}{2}|0\rangle + \sin\frac{\theta}{2}e^{i\varphi}|1\rangle \right)
$$
where 
$$
a = e^{i\gamma}\cos\frac{\theta}{2}, b = e^{i(\gamma+\varphi)}\sin\frac{\theta}{2}
$$

#### What is the quantum operation in Bloch sphere?





---

### Appendix

#### How to prove that every point on Bloch sphere corresponding to only one qubit state, and all one qubit state is in Bloch sphere?



#### How to get the rule of position and qubit for Bloch sphere?

$$
\begin{align}
|\psi\rangle &= |a|e^{i\gamma}|0\rangle + |b|e^{i\beta}|1\rangle \\
&= |a|e^{i\gamma}|0\rangle + |b|e^{i(\gamma + \varphi)}|1\rangle \\
&= e^{i\gamma}\left(|a||0\rangle + {|b|}e^{i\varphi}|1\rangle \right)
\end{align}
$$

Note that $|a|^2+|b|^2 = 1$, and $|a|$ and $|b|$ is non-negative, so we can assume
$$
|a| = \cos\frac{\theta}{2}, |b| = \sin\frac{\theta}{2}
$$
where $\theta$ is the angular coordinate in the sphere, so $|a|$ and $|b|$ is non-negative and 
$$
|\psi\rangle = e^{i\gamma}\left(\cos\frac{\theta}{2}|0\rangle + \sin\frac{\theta}{2}e^{i\varphi}|1\rangle \right)
$$
