## Sketch of the Construction
The modern approach to the theory of Lebesgue [[Integration|integration]] has two distinct parts:
- A theory of measureable sets and [[Measures|measures]] of these [[Sets|sets]]
- A theory of [[Measurable Functions|measurable functions]] and integrals of these functions
In the Lebesgue theory, integrals are limited to a class of functions called measurable functions
___
Let a [[Measure Spaces|measure space]] $(\Omega,\mathfrak{F},\mu)$ be fixed. The Lebesgue integral $\int _{\Omega}f \, d\mu$ for measurable functions $f:\Omega\to \mathbb{R}$ is constructed in stages:
### Indicator Functions
If $S\in\mathfrak{F}$, i.e. the set $S$ is measurable, then define the integral of its [[Indicator Function|indicator function]] $\mathbb{1}_{S}$ bia
$$
\int \mathbb{1}_{S} \, d\mu=\mu(S) 
$$
### Simple Functions
For non-negative simple functions, equivalently, [[Linear Combinations|linear combinations]] of indicator functions:
$$
f=\sum_{k=1}^{n}a_{k}\mathbb{1}_{S_{k}}
$$
Where the sum is finite and all $a_{k}\geq 0$, we use linearity to define]
$$
\mu(f)\equiv \int \sum_{k=1}^{n}a_{k}\mathbb{1}_{S_{k}} \, d\mu =\sum_{k=1}^{n}a_{k}\int \mathbb{1}_{S_{k}} \, d\mu=\sum_{k=1}^{n}a_{k}\mu(S_{k})
$$
This construction is obviously [[Linear|linear]] and monotone
Moreover, even if a simple function can be written as $\sum_{k=1}^{n}a_{k}\mathbb{1}_{S_{k}}$, in many ways, its integral always gives the same value
Also, if any two functions $f_{1}$ and $f_{2}$ coincide almost everywhere, i.e. they differe on a set of measure zero, $\mu(x:f_{1}(x)\neq f_{2}(x))=0$, then their integrals are equal, $\mu(f_{1})=\mu(f_{2})$
### Non-negative Functions
Let $f:\Omega\to[0,\infty]$ be measurable. We put
$$
\int _{\Omega}f \, d\mu:=\sup \left\{ \int _{\Omega}h \, d\mu :\middle|: h\leq f,0\leq h\text{ is simple}  \right\} 
$$
We need to check whether this construction is consistent, i.e. if $0\leq f$ is simple, we need to verify whether this definition coincides with the preceding one. Another question is: if $f$ as above is [[Riemann Integrals|Riemann-integrable]], does this definition give the same value of the integral?
It is not hard to prove that the answer to both questions is yes.
Clearly, if $f:\Omega\to[0,\infty]$ is arbitrary and measurable function, its integral $\int f \, d\mu$ may be infinite
### Signed Functions
If $f:\Omega\to[0,\infty ]$ is measurable, we decompose it into the positive and negative parts, $f=f^{+}-f^{-}$, where
$$
f^{+}(x)=\begin{cases}
f(x) & f(x)>0 \\
0 & \text{otherwise}
\end{cases}
$$
$$
 f^{-}(x)=\begin{cases}
-f(x) & f(x)<0 \\
0 & \text{otherwise}
\end{cases}

$$
Notice that the functions $f^{+}\geq 0$ and $f^{-}\geq 0$ satisfy $\left| f \right|=f^{+}+f^{-}$
If $\int \left| f \right| \, d\mu$ is finite, then $f$ is called Lebesgue integrable. In this case, both integrals $\int f^{+} \, d\mu$ and $\int f^{-} \, d\mu$ converge, and it makes sense to define:
$$
\int f \, d\mu =\int f^{+} \, d\mu-\int f^{-} \, d\mu  
$$
It turns out that this definition gives the desirable properties of the integral, namely, linearity, monotonicity and regularity when taking limits
Note that complex-valued functions can be similarly integrated by considering the real part and the imaginary part separately
The functions, which can be obtained from the above constructions are calle Borel functions, the class of Borel functions is very big and is sufficient for most practical considerations
## Application to Probability
A recurring question often finds in [[Probabilities|probability]] is the following: suppose a [[Sequences|sequence]] of [[Random Variables|random variables]] [[Convergence of Random Variables|converges]]; do their [[Expectation|expectations]] converge to the expectation of their limit?
That is, assuming $X_{n}\to X$ in some sense, is it true that $\mathbb{E}(X_{n})\to \mathbb{E}(X)$
The answer is helpfully "not always", but there are several theorems to provide ufficient conditions
