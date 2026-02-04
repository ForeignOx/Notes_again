A powerful method for simplifying [[Vectors|vector]] equations, for example
$$
\underline{c}=\underline{a}+\underline{b}\to c_{i}=a_{i}+b_{i}
$$
Where it is understood that this holds for any $i=1,\dots,n$
Tensors may have more than $\hspace{0pt}1$ index, for example Einstein's field equations in General Relativity:
$$
\underbrace{ G_{ij}+\Lambda g_{ij} }_{ \text{curvature of spacetime} }=\underbrace{ \kappa T_{ij} }_{ \text{stress-energy-momentum content} }
$$
An index that appears once in each term is called a free index. A vector is an object with $\hspace{0pt}1$ free index. The choice of letter is arbitrary, but all terms in an equation must have the same free index (or indices)
## Einstein Summation Convention
In index notation, we write a [[Dot Product|scalar product]] as:
$$
\underline{a}\cdot  \underline{b}=a_{j}b_{j}
$$
Where repeated index implies a sum from $\hspace{0pt}1$ to $n$. This is called the Einstein summation convention
An index that appears exactly twice in the same term is called a dummy index, and always implies a summation. Again, the choice of letter is arbitrary
Never use the same index more than twice (unless you are getting freaky with it)
### Example
Express $(\underline{a}\cdot \underline{b})(\underline{c}\cdot \underline{d})$ in index notation:
$$
(\underline{a}\cdot \underline{b})(\underline{c}\cdot \underline{d})=a_{j}b_{j}c_{k}d_{k}
$$
We can't use $j$ again
___
Express $a_{j}b_{i}c_{j}$ in vector notation
Here $i$ appears once, so it is a free index, and $j$ appears twice, so it is a dummy index and thus summed over. Since the expression has $\hspace{0pt}1$ free index, it is the $i$th component of a vector, so it is:
$$
a_{j}b_{i}c_{j}=[(\underline{a}\cdot \underline{c})\underline{b}]_{i}
$$
Note we have to put the $i$, otherwise it might be considered a vector, and the LHS is a scalar
___
Express the equation $\underline{u}+(\underline{a}\cdot \underline{b})\underline{v}=\left| \underline{a} \right|^{2}(\underline{b}\cdot \underline{v})\underline{a}$
Each side is a vector, but in index notation, we have to write an equation for the $i$th component:
$$
u_{i}+(\underline{a}\cdot \underline{b})v_{i}=\left| \underline{a} \right|^{2}(\underline{b}\cdot \underline{v})a_{i}
$$
Next we need to introduce dummy indices:
$$
u_{i}+a_{j}b_{j}=a_{j}a_{j}b_{k}v_{k}a_{i}
$$
___
Another way to think of $\underline{a}\cdot \underline{b}$ is as a quadratic form:
$$
\underline{a}\cdot \underline{b} = \underline{a}^{\top} I \underline{b}
$$
Or with other matrices, but we can write this in index notation:
$$
\underline{a}\cdot \underline{b}=\delta_{ij}a_{i}b_{j}
$$
Where $\delta_{ij}$ is the [[Kronecker Delta Function|Kronecker delta function]] 
## Proposition#
Multiplying an expression with free index $i$ by $\delta_{ij}$, this is equivalent to replacing $i$ with $j$ in the original expression
### Proof
$$
a_{i}\delta_{ij}=\sum_{i=1}^{n}a_{i}\delta_{ij}=a_{j}
$$
Here $i$ becomes a dummy, and $j$ is a free index, since the Kronecker delta cancels all other terms and only keeps the ones where $i=j$
### Example
Sinplify $\delta_{ij}\delta_{jk}$
By the proposition, multiplying by $\delta_{jk}$ is equivalent to replacing $j\to k$ in $\delta_{ij}$, giving
$$
\delta_{ij}\delta_{jk}=\delta_{ik}
$$
___
Simplify $\delta_{ij}\delta_{ji}$, by the proposition, multiplying by $\delta_{ji}$ is equivalent to replacing $j\to i$, giving:
$$
\delta_{ij}\delta_{ji}=\delta_{ii}=\sum_{i=1}^{n}\delta_{ii}=n
$$
## [[Cross Product|Vector Products]]
In $\mathbb{R}^{3}$, we can write $\underline{a}\times \underline{b}$ in index notation by introducing the [[Alternating Tensor|alternating tensor]] or the Levi-Civita symbol:

$$
[\underline{a}\times \underline{b}]_{i}=\epsilon_{ijk}a_{j}b_{k}
$$
For example, the first component of the right hand side is:
$$
\epsilon_{1jk}a_{j}b_{k}=\underbrace{ \epsilon_{11k}a_{1}b_{k} }_{ =0 }+\epsilon_{12k}a_{2}b_{k}+\epsilon_{13k}a_{3}b_{k}
$$
$$
= \underbrace{ \epsilon_{121} }_{ =0 }a_{2}b_{1}+\underbrace{ \epsilon_{122} }_{ =0 }a_{2}b_{2}+\underbrace{ \epsilon_{123} }_{ =1 }a_{2}b_{3}+\underbrace{ \epsilon_{131} }_{ =0 }a_{3}b_{1}+\underbrace{ \epsilon_{132} }_{ =-1 }a_{3}b_{2}+\underbrace{ \epsilon_{133} }_{ =0 }a_{3}b_{3} 
$$
$$
= a_{2}b_{3}-a_{3}b_{2}=(\underline{a}\times \underline{b})\cdot \underline{e}_{1}
$$
### Example
Use index notation to show that $\underline{a}\cdot(\underline{b}\times \underline{c})=\underline{c}\cdot(\underline{a}\times \underline{b})$
$$
\underline{a}\cdot(\underline{b}\times \underline{c})=a_{i}[\underline{b}\times \underline{c}]_{i} 
$$
$$
= a_{i}\epsilon_{ijk}b_{j}c_{k}
$$
$$
= \epsilon_{ijk}a_{i}b_{j}c_{k}
$$
$$
= \epsilon_{ijk}c_{k}a_{i}b_{j}
$$
$$
= \epsilon_{kij}c_{k}a_{i}b_{j}
$$
$$
= c_{k}\epsilon_{kij}a_{i}b_{j}
$$
$$
= c_{k}[\underline{a}\times \underline{b}]_{k}=\underline{c}\cdot (\underline{a}\times \underline{b})
$$
## Proposition ($\epsilon$-$\delta$ identity)
When simplifying more complicated expressions, there is a useful identity for the product of two $\epsilon$'s that share an index:
$$
\epsilon_{ijk}\epsilon_{klm}=\delta_{il}\delta_{jm}-\delta_{im}\delta_{jl}
$$
### Proof
Left hand side is:
$$
\epsilon_{ijk}\epsilon_{klm}=\begin{cases}
+1  & \text{if }(klm)\text{ is an even permutation of }(ijk)\\
-1  & \text{if }(klm)\text{ is an odd permutation of }(ijk)\\
0 & \text{if }(klm)\text{ is not a permutation of }(ijk)
\end{cases}
$$
Sooo
$$
\epsilon_{ijk}\epsilon_{klm}=\delta_{ik}\delta_{jl}\delta _{km}-\delta_{ik}\delta_{kl}\delta_{jm}+\delta_{kk}\delta_{il}\delta_{jm}-\delta_{jk}\delta _{il}\delta_{km}+\delta_{jk}\delta_{kl}\delta_{im}-\delta_{kk}\delta_{jl}\delta_{im}
$$
Applying the proposition above,
$$
=\delta_{im}\delta_{jl}-\delta_{il}\delta_{jm}+3\delta_{il}\delta_{jm}-\delta_{jm}\delta_{il}+\delta_{jl}\delta_{im}-3\delta_{jl}\delta _{im} 
$$
$$
= \delta_{il}\delta_{jm}-\delta_{im}\delta_{jl}
$$
