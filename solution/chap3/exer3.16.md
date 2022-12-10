## Problem 1

To prove that there exists Boolean function $f$ that maps $n$ input bits to $1$ output bit that require at least $2^n/n$ classical logical gates, we need to prove

* **Claim 1:** There are totally $2^{2^n}$ different Boolean functions with $n$ inputs and $1$ outputs
* **Claim 2:** There are totally $\left[16\binom{s+n}{2}\right]^{s}/s!$ distinct circuits that takes $n$ bits input and has totally $s$ logical gates
* **Claim 3:** If we have $2^n/n$ logical gates, it can only creates less than $2^{2^n}$ distinct circuits

---

To prove **Claim 1**, we consider a Boolean function $f$ that maps $n$ input bits to $1$ output bit, that is, $f: \{0,1\}^{n} \to \{0, 1\}$. For Boolean function $f$, we have $2^n$ possible $n$ bits input string. Meanwhile, if we input each $n$ bits string into Boolean function, we will get a group of output with $2^n$ output bits in the group. Obviously, the group of output is different for different Boolean function. Since the output bit of each input $n$ bits for any Boolean function is either $0$ or $1$, there are totally $2^{2^n}$ different groups of output for all possible Boolean functions $ f: \{0,1\}^{n} \to \{0, 1\}$. Thus, there are totally $2^{2^n}$ different Boolean functions with $n$ inputs and $1$ output. 

---

To prove **Claim 2**, suppose we have $n$ input bits and $s$ logical gates. Since every logical gates take $2$ bits and output $1$ bit, we could have $\binom{n+s}{2}$ possible inputs for each logical gate. Since we have $2^{2^2} = 16$ different Boolean functions with $2$ inputs and $1$ outputs, we cound have $16\binom{n+s}{2}$ circuit connection for each gate. Then we could construct $\left[16\binom{s+n}{2}\right]^{s}$ different circuit with $s$ logical gates. Note that each permutation of gates would gives the same circuit, so we need to add a factor $1/s!$​ to bound the total number of distinct circuits
$$
H(n, s) \leq \frac{1}{s!}\cdot\left[16\binom{s+n}{2}\right]^{s}\tag{1}\label{1}
$$
Note that a $\rm NOT$ gate has two bit inputs since it can takes two bits input and output the negation of the first bit. 

---

To prove **Claim 3**, we firstly write eq. $\eqref{1}$​ in its logarithm form, 
$$
\begin{align}
\log H(n, s) \leq& s\log 16 + s\log\binom{s+n}{2}-\log s! \\
=& 4s + s\log \frac{(s+n)(s+n-1)}{2} -\log s!  \\
<& 4s + s\log (s+n)^2 -\log s!  \\
=& 4s + 2s\log (s+n) -\log s!
\end{align} \tag{2}\label{2}
$$
According to Stirling's approximation, 
$$
\log s! = s\log s - s\log e + \Theta(\log s)\tag{3}
$$
where $e$ is the Euler's number, we could write eq. $\eqref{2}$ as
$$
\begin{align}
\log H(n, s) <& 4s + 2s\log (s+n) -\log s!\\
\leq & 4s + 2s\log (s+n) - s\log s + s\log e
\end{align}\tag{4}
$$
Since we have $s\geq n$, then 
$$
\begin{align}
\log H(n, s) \leq & 4s + 2s\log (s+n) - s\log s + s\log e \\
\leq & 4s + 2s\log 2s - s\log s + s\log e\\
= & 4s + 2s\log 2 + 2s\log s - s\log s + s\log e\\
= & 6s + s\log s + s\log e
\end{align}\tag{5}
$$
Suppose we have $s = 2^n/n$​, then 
$$
\begin{align}
\log H(n, 2^n/n) \leq & 6s + s\log s + s\log e \\
=& 6 \cdot \frac{2^n}{n} + \frac{2^n}{n}(\log 2^n - \log n) + \frac{2^n}{n} \log e\\
=& \frac{2^n}{n}(n - \log n+6+\log e)\\
= & 2^n - \frac{2^n}{n}(\log n-6-\log e)
\end{align}\tag{6}
$$
Thus, 
$$
H(n, 2^n/n) \leq \frac{2^{2^n}}{2^{\frac{2^n}{n}(\log n-6-\log e)}} = \frac{2^{2^n}}{2^{\frac{2^n}{n}(\log n-O(1))}} \leq 2^{2^n}\tag{7}
$$
Then we could conclude that, if we have $2^n/n$ logical gates, it can creates less than $2^{2^n}$ circuits. 

---

According to **Claim 3**, it means that if we need to construct all possible $2^{2^n}$ Boolean functions, we need more than $2^n/n$ logical gates. Equvalently, we can say, there exists Boolean function $f$ that maps $n$ input bits to $1$ output bit that require at least $2^n/n$ classical logical gates. 
