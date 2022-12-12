## Exercise 2.32

Suppose $P_{V'}$ is a projector in vector space $V$ and $P_{W'}$ is a projector in vector space $W$. The tensor product of them is given by $P_{V'} \otimes P_{W'} $. To prove $P_{V'} \otimes P_{W'} $ is projector, we only need to prove $P_{V'} \otimes P_{W'} $ is Hermitian and $(P_{V'} \otimes P_{W'} )^2 = P_{V'} \otimes P_{W'} $. 

From Exercise 2.30 we know that since projector $P_{V'}$ and $P_{W'}$ are Hermitian, so $P_{V'} \otimes P_{W'}$ is also a Hermitian operator. Meanwhile, since we have
$$
(P_{V'} \otimes P_{W'})^2 = (P_{V'} \otimes P_{W'})(P_{V'} \otimes P_{W'})^2 = P_{V'}P_{V'} \otimes P_{W'}P_{W'} \tag{1}
$$
and for projector $P_{V'}$ and $P_{W'}$ we have $P_{V'}^2 = P_{V'}$ and $P_{W'}^2 = P_{W'}$, then we could have $(P_{V'} \otimes P_{W'})^2 = P_{V'} \otimes P_{W'}$. Therefore, we can conclude from the above statement that, the tensor product of two projectors is a projector. 
