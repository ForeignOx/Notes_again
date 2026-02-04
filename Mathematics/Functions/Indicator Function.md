The function $\mathbb{1}$ is a function of a [[Subsets|subset]] of a [[Sets|set]] that maps elements of the subset to one, and all other elements to $\hspace{0pt}0$. That is, if $A\subset X$:
$$
\mathbb{1}_{A}(x)=\begin{cases}
1&\text{if }x\in A\\0&\text{otherwise}
\end{cases}
$$
## In Probability
Let [[Sample Spaces|$A\subseteq\Omega$]], then the indicator of $A$, denoted by $\mathbb{1}_{A}$ is defined as follows:
$$
\mathbb{1}_{A}(\omega)=\begin{cases}
1&\text{if }\omega \in A\\0&\text{if }\omega \not\in A
\end{cases}
$$
The number of ways the indicator function gives $\hspace{0pt}1$ is also the [[Cardinality of Sets|cardinality]] of $A$, so
$$
\mathbb{P}(A)=\frac{|A|}{|\Omega|}
$$
$$
 |A|=\sum_{\omega \in A}\mathbb{1}_{A}(\omega)
$$
But also since the other $\omega_{i}$ will give zero, we can in fact say
$$
|A|=\sum_{\omega \in \Omega}\mathbb{1}_{A}(\omega)
$$
We can also say
$$
\mathbb{P}_{A}(\{ 1 \})=\mathbb{P}(\{ \omega\mid \mathbb{1}_{A}(\omega)=1 \})=\mathbb{P}(A)
$$
$$
\mathbb{P}_{A}(\{ 0 \})=\mathbb{P}(\{ \omega\mid \mathbb{1}_{A}(\omega)=0 \})=\mathbb{P}(A^{c})
$$
Now we will abuse notation slightly and consider these as the same:
$$
\mathbb{P}_{X}(\{ x \})=\mathbb{P}_{X}(x)
$$
## Example
$$
\mathbb{1}_{A\cap B}=\mathbb{1}_{A}\mathbb{1}_{B}
$$
Because if $\omega \in A$ and $\omega \in B$, then $\mathbb{1}_{A}=1$, $\mathbb{1}_{B}=1$, so $\mathbb{1}_{A\cap B}=1$, in any other case $\mathbb{1}_{A\cap B}=0$ as one of $\mathbb{1}_{A}$ or $\mathbb{1}_{B}$ is zero

#Mathematics #Probability #Definition 