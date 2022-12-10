## Exercise 3.7

Suppose $M$ is a Turing machine with oracle for halting problem. Consider a function $g(M, x)$ which tells that $M$ will halt with input $x$, and
$$
g(M, x) = \begin{cases}
0 & \text{Turing machine with oracle for halting problem does not halt}\\
1 & \text{Turing machine with oracle for halting problem halts}
\end{cases}\tag{1}
$$
Then we could construct a program as follows, 

```pseudocode
Program(M, x):

y = g(M, x)
if y = 0 then
	halt
else
	loop forever
end if
```

The above program can be implemented in Turing machine, so if we add one oracle for the program to construct a Turing machine with oracle for halting problem as $M_0$, and calculate $g(M_0,x)$, we could conclude that

* From the definition of $g(M, x)$, if $g(M_0, x) = 1$, the program with oracle halts
* From the definition of the program, if $g(M_0, x)=0$, the program with oracle halts

Therefore, we cannot find a function $g(M,x)$ to determine whether $M$ will halt with input $x$. Equivalently, we cannot determine whether a program for the Turing machine with oracle will halt with Turing machine aided by an oracle for the halting problem. 
