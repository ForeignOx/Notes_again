## Definition
Let $(\Omega,\mathfrak{F},\mathbb{P})$ be a [[Probability Spaces|probability space]]. A random variable $X$ on [[Sample Spaces|$\Omega$]] is a mapping from $\Omega$ to some set of possible values
$$
X:\Omega\to \chi\text{ (some arbitrary space)}
$$
$$
X(\Omega)=\left\{ X(\omega)|\omega \in \Omega \right\}
$$
$$
X(\omega)\in \chi
$$

For us, we will be concerned with $X(\Omega)\subset \mathbb{R}$ or $\mathbb{R}^n$
We require that for every open set $\mathcal{U}\subseteq \chi$,
$$
\left\{ \omega:\middle|: X(\omega)\in \mathcal{U} \right\} = \left\{ X\in  \mathcal{U} \right\}\in  \mathfrak{F}
$$
In fact, the same holds for closed sets and a further equivalent statement is for every $y\in \mathbb{R}$,
$$
\left\{ X\leq y\right\}=\left\{ \omega \in \Omega:\middle|: X(\omega)\in (-\infty,y] \right\}\in  \mathfrak{F}
$$
We now define [[Probabilities|probability]] function $\mathbb{P}_{X}(B)$, where $B\in\chi$:
$$
\mathbb{P}_{X}(B):X(\Omega)\to[0,1]
$$
$$
\mathbb{P}_{X}(B):=\mathbb{P}((X \in B))=\mathbb{P}(X ^{-1}(B))=\mathbb{P}(\left\{ \omega:\middle|: X(\omega) \in B \right\})
$$
Where $X ^{-1}$ is the [[Image|pre-image]] of $X$, this is also known as the distribution/cumulative density/distribution function of $X$
The random variables we might see are either discrete or continuous or neither
## Examples
Tossing a fair coin thrice and let $X$ denote the number of heads:

| $\omega$    | HHH | HHT | HTT | HTH | THT | THH | TTH | TTT |
| ----------- | --- | --- | --- | --- | --- | --- | --- | --- |
| $X(\omega)$ | 3   | 2   | 1   | 2   | 1   | 2   | 1   | 0   |
Let $A_{1}=\left\{ X=2 \right\},A_{2}=\left\{ X \in[0,1.5] \right\},A_{3}=\left\{ 2.5\leq X\leq 4.5 \right\}$,
$$
A_{1}=\left\{ X=2 \right\}=\left\{ \omega:X(\omega)=2 \right\}=X ^{-1}(\left\{ 2 \right\})=\left\{ HHT,HTH,THH \right\}\subseteq\Omega
$$
$$
\mathbb{P}(A_{i})=\frac{|A_{i}|}{|\Omega|}=\frac{3}{2^{3}}=\frac{3}{8}
$$
$$
A_{2}=\left\{ \omega:\middle|:0\leq X(\omega)\leq 1.5 \right\}=X ^{-1}([0,1.5])=\left\{ \omega:\middle|: X(\omega)=0\text{, or }X(\omega)=1 \right\}
$$
$$
= \left\{ TTT,HTT,THT,TTH \right\}
$$
$$
\mathbb{P}(A_{2})=\frac{|A_{2}|}{|\Omega|}=\frac{4}{2^{3}}=\frac{1}{2}
$$
___
Tossing $\hspace{0pt}2$ fair dice and let $X$ be the random variable denoting the sum of the scores. For this example,
$$
\Omega=\left\{ (1,1),(1,2),\dots,(1,6),(2,1),\dots \right\}=\left\{ (i,j):\middle|:1\leq i\leq 6,1\leq j\leq 6 \right\}
$$
$$
|\Omega|=6^{2}
$$
$$
 X:\Omega\to \mathbb{R}
$$
$$
 \omega \mapsto X(\omega)
$$
$$
(i,j)\mapsto X(i,j)=i+j
$$
Here $\chi=\left\{ 0,1,2,3 \right\}$, so let's find the [[Discrete Random Variables#Probability Mass Function|pmf]] of $X$, note that $|\Omega|=2^{3}=8$:

| x      | 0             | 1             | 2             | 3             |
| ------ | ------------- | ------------- | ------------- | ------------- |
| $p(x)$ | $\frac{1}{8}$ | $\frac{3}{8}$ | $\frac{3}{8}$ | $\frac{1}{8}$ |
Note that the total is $\hspace{0pt}1$
## Theorem
Let $X:\Omega\to \mathbb{R}$ be a random variable, then $\mathbb{P}_{X}$ is a probability on $\mathbb{R}$
### Proof
We need to show $\mathbb{P}_{X}$ satisfies the axioms of probability:
$$
\mathbb{P}_{X}(\text{whole space})=\mathbb{P}_{X}(\mathbb{R})=1
$$
$$
\mathbb{P}_{X}(\mathbb{R})=\mathbb{P}(X ^{-1}(\mathbb{R}))=\mathbb{P}(\Omega)=1
$$
As $X ^{-1}(\mathbb{R})=\left\{ \omega :\middle|: X(\omega)\in\mathbb{R} \right\}=\Omega$ 
We want to show:
$$
\mathbb{P}_{X}(A\cup B)=\mathbb{P}_{X}(A)+\mathbb{P}_{X}(B)
$$
Where $A$ and $B$ are disjoint, $A,B\in\mathbb{R},A\cap B=\emptyset$
$$
X ^{-1}(A\cup B)=X ^{-1}(A) \cup X ^{-1}(B)
$$
And
$$
X ^{-1}(A)\cap X ^{-1}(B)=\emptyset
$$
So:
$$
\mathbb{P}_{X}(A\cup B)=\mathbb{P}(X ^{-1}(A\cup B))
$$
Now we want to prove $X ^{-1}(A\cup B)=X ^{-1}(A) \cup X ^{-1}(B)$, so we have to show that:
- $X ^{-1}(A\cup B)\subseteq X ^{-1}(A)\cup X ^{-1}(B)$
- $X ^{-1}(A\cup B)\supseteq X ^{-1}(A)\cup X ^{-1}(B)$
Let us show the first
Let $\omega \in X ^{-1}(A\cup B)$
$$
\implies X(\omega)\in A\cup B
$$
$$
\implies X(\omega)\in A\text{ or }X(\omega)\in B
$$
$$
\implies \omega \in X ^{-1}(A) \text{ or }\omega \in X ^{-1}(B)
$$
$$
\implies \omega \in  X ^{-1}(A)\cup X ^{-1}(B)
$$
Prove the second!
If $A\cap B=\emptyset$, then $X ^{-1}(A)\cap X ^{-1}(B)=\emptyset$, proof by contradiction:
$$
X ^{-1}(A)\cap X ^{-1}(B)\neq \emptyset
$$
$$
\therefore \exists \omega \in X ^{-1}(A)\cap X ^{-1}(B)
$$
For this $\omega$, we have
$$
X(\omega)\in A\text{ and }X(\omega)\in B
$$
$$
\implies A\cap B\neq \emptyset
$$
So we have a contradiction
So:
$$
\mathbb{P}(X ^{-1}(A)\cup X ^{-1}(B))=\mathbb{P}(X ^{-1}(A))+\mathbb{P}(X ^{-1}(B))=\mathbb{P}_{X}(A)+\mathbb{P}_{X}(B)
$$
### Functions of Random Variables
Let $X$ be a random variable on some probability space $(\Omega,\mathfrak{F},\mathbb{P})$ and let [[Functions|$f:\mathbb{R}\to \mathbb{R}$]] be a function. Assume that
$$
\forall y\in \mathbb{R},~f^{-1}((-\infty,y])\in \mathcal{B}(\mathbb{R})
$$
where $\mathcal{B}(\mathbb{R})$ is the Borel [[Sigma Algebra|sigma algebra]] in $\mathbb{R}$. Then the combined random map $Y(\omega):= f(X(\omega))$ is also a random variable
___
By using the standard properties of [[Inverses|inverse functions]], one can show that the relation above extends to
$$
\forall B\in  \mathcal{B}(\mathbb{R}),~f^{-1}(B)\equiv \left\{ x\in \mathbb{R}:\middle|: f(x)\in B \right\}\in \mathcal{B}(\mathbb{R})
$$
Functions satisfying this are called [[Measures|measureable]]
## Multiple Variables
Say we have two or multiple random variables:
$$
X:\Omega\to \chi 
$$
$$
Y:\Omega\to\Gamma
$$
$$
(X,Y):\Omega\to \chi \times\Gamma
$$
$$
(X,Y)(\omega)=(X(\omega),Y(\omega))
$$
Let $A\in\chi \times \Gamma$, what is $\mathbb{P}((X,Y)\in A)$?
$$
\left\{ (X,Y)\in A \right\}=\left\{ \omega:(X(\omega),Y(\omega))\in A \right\}
$$
### Example
Suppose $\chi=\mathbb{R}=\Gamma$; $A=[0,1]\times[0,1]$,
$$
\mathbb{P}((X,Y)\in [0,1]\times [0,1])
$$
$$
 \left\{ X=x,Y=y \right\}=\left\{ \omega:X(\omega)=x,Y(\omega)=y \right\}=\left\{ \omega:X(\omega)=x \right\}\cap \left\{ \omega:Y(\omega)=y \right\}
$$


#Mathematics #Probability #Definition 