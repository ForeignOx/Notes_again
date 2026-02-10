## Definition
Let $X:\Omega\to \mathbb{R}$ be a [[Random Variables|random variable]] then the moment generating function of $X$ is defined and denoted by:
$$
M_{X}(t)=\mathbb{E}(x^{tx}),t\in \mathbb{R}
$$
Note that the mgf may not always exist
This is the [[Probability Generating Functions|probability generating function]] with $s=e^{ t }$, $M_{X}(t)=G_{X}(e^{ t })$
$e^{ tx }\geq 0$, hence from the monotonicity of expectaittions, we know that $M_{X}\geq 0$
By LoTUS,
$$
\mathbb{E}(e^{ tx })=\begin{cases}
\sum_{x\to \infty}e^{ tx }p(x&\text{if }X\text{ is discrete with pmf }p)\\
\int_{-\infty}^{\infty} e^{ tx }f(x) \, dx &\text{if }X\text{ is continuous with pdf }f
\end{cases}
$$
From the taylor expansion:
$$
e^{ x }=1+x+\frac{x^{2}}{2}+\dots
$$
$$
e^{ tx }=1+tx+\frac{t^{2}x^{2}}{2!}+\dots 
$$
$$
 \mathbb{E}(e^{ tx })=1+t\mathbb{E}(x)+\frac{t^{2}}{2}\mathbb{E}(X^{2})+\dots
$$
RHS is a power series ($\sum_{k=0}^{\infty} a_{k}x^{k}$, for coefficients $a_{k}$) which are related to the moments of $X$
## Properties
For every $k\in\mathbb{N}$,
$$
\mathbb{E}(X^{k})=\frac{d ^{k}}{dt^{k}} M_{X}(t)\mid_{t=0}=\frac{d ^{k}M_{X}(0)}{dt^{k}} 
$$
$$
\mathbb{E}(X)=\frac{d }{dt} =M_{X}(t)\mid_{t=0}
$$
Scaling:
Let $X$ be a random variable, then $M_{aX+b }=e^{ bx }M_{X}(at)$
Product:
Let $X_{1},X_{2},\dots,X_{n}$ be independent with mgf $M_{X_{i}}(t)$, then 
$$
Y:=\sum_{ i=1} ^{ n} X_{i}
$$
$$
 M_{Y}(t) =\prod_{i=1}^{n}M_{X_{i}}(t)
$$
The mgf of the sum is the product of corresponding mgfs
##### Proof
Let $Y=\sum_{ i=1} ^{ n} X_{i}$, then 
$$
M_{Y}(t)=E\left( e^{ t\sum_{ i=1} ^{ n}   X_{i}} \right)=\mathbb{E}(e^{ tX_{1} }e^{ tX_{2} }\dots e^{ tX_{n} })
$$
Which, since they are independent, is equal to
$$
=\prod_{ i=1} ^{ n}  \mathbb{E}(e^{ tX_{i} })=2
$$
Convergence:
Let $X_{1},X_{2},\dots$ be an infinite sequence of independent random variables and let $X$ be some random variable, then if there is $n>0$ such that
$$
\lim_{ n \to \infty } M_{X_{n}}(t)=M_{X}(t)<\infty \forall t\in -h,h
$$
$$
\lim_{ n \to \infty } F_{X_{n}}(x)=F_{X}(x)
$$
For all $x\in\mathbb{R}$, where $F_{X}(\cdot)$ is continuous. We say "$X_{n}$ converges in distribution to $X$"
## Example
If [[Poisson Distribution|$X\sim Po(\lambda)$]], we have $G_{X}(s)=e^{ \lambda(s-1) }$. Therefore $M_{X}(t)\equiv G_{X}(e^{ t })=\exp(\lambda(e^{ t }-1))$



#Mathematics #Probability #Definition 