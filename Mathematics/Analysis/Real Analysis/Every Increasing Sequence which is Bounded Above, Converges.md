## Proof
If $a_{n}$ is an [[Sequences|increasing sequence]] which is [[Boundedness|bounded above]], then $a_{n+1}\geq a_{n}\forall n\in\mathbb{N}$ and $\exists U\in\mathbb{R}:a_{n} \leq U,\forall n\in\mathbb{N}$ so there must be a [[Supremum and Infimum|supremum]] $M\in\mathbb{R}$ by the [[Real Numbers#Completeness Axiom|completeness axiom]] 
Let $\varepsilon>0$
Consider $M-\varepsilon<M$, so $M-\varepsilon$ cannot be an upper bound because $M$ is the supremum, so there must exist some $i\in\mathbb{N}:a_{i}>M-\varepsilon$ 
And $a_{i+1}\geq a_{i}$ and $a_{n}\geq a_{i}$ if $n>i$, so take $N_{\varepsilon}=i$
If
$$
n\geq N_{\varepsilon}
$$
$$
\implies a_{n}\geq a_{i}>M-\varepsilon 
$$
$$
\implies -\varepsilon<a_{n}-M
$$
Also, $\forall n,a_{n}\leq M$ so $a_{n}<M+\varepsilon$

$$
\implies\varepsilon>a_{n}-M
$$
Sooo
$$
-\varepsilon<a_{n}-M<\varepsilon 
$$
$$
\implies \left| a_{n}-M \right|<\varepsilon
$$
So $a_{n}$ [[Convergence|converges]] to $M$
A similar result can be shown using [[Calculus of Limits Theorem|CoLT]] and $-a_{n}$ to show that a decreasing sequence converges to the infimum
## Examples
Let
$$
x_{n}=\left( 1+\frac{1}{n} \right)^{n}=\sum_{k=0}^{n}{n \choose k } \frac{1}{n^{k}}=1+1+\sum_{k=2}^{n}{n \choose k } \frac{1}{n^{k}}
$$
We can show that
$$
\frac{1}{m^{k}}{m \choose k }<\frac{1}{n^{k}}{n \choose k }\leq \frac{1}{2^{k-1}}
$$
For $m<n$, so $x_{m}<x_{n}$, and so the sequence is monotonically increasing
Also, 
$$
x_{n}\leq 2+\underbrace{ \frac{1}{2}+\frac{1}{4}+\frac{1}{8}+\dots+\frac{1}{2^{n-1}} }_{ \to 1 }<3
$$
So the sequence is bounded, so the limit exists and is in $[2,3]$
The limit is Euler's number $e$
$$
e=\lim_{ n \to \infty } \left( 1+\frac{1}{n} \right)^{n}=2.718281828459045\dots
$$
___
$$
y_{n}=\left( 1+\frac{2}{n} \right)^{n}=\left( \frac{n+2}{n} \right)^{n}=\frac{(n+2)^{n}}{n^{n}} \frac{(n+1)^{n}}{(n+1)^{n}}=\left( \frac{n+1}{n} \right)^{n}\left( \frac{n+2}{n+1} \right)^{n}=\frac{\left( \frac{n+1}{n} \right)^{n}\left( 1+\frac{1}{n+1} \right)^{n+1}}{1+\frac{1}{n+1}}
$$
By CoLT, this converges to $e\times \frac{e}{1}=e^{2}$
Now by induction, we can show that 
$$
\left( 1+\frac{k}{n} \right)^{n}\to e ^{k}
$$
For $k\in\mathbb{N}$
___
$$
z_{n}=\left( 1-\frac{1}{n} \right)^{n}=\left( \frac{n-1}{n} \right)^{n}=\frac{1}{\left( \frac{n}{n-1} \right)^{n}}=\frac{1}{\left( 1+\frac{1}{n-1} \right)^{n-1}\left( 1+\frac{1}{n-1} \right)}
$$
By CoLT converges to $\frac{1}{e\times 1}=e^{-1}$
___
We are then motivated to define:
$$
e^{ x }=\lim_{ n \to \infty } \left( 1+\frac{x}{n} \right)^{n}
$$
For $x\in\mathbb{R}$, thus we have the [[Exponential Functions|exponential]] 



#Mathematics #Analysis  #Theorem 