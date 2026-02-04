Let $a\geq 0$ and $p \in\mathbb{N}$, then there exists a unique $x\geq 0$ with $x^{p}=a$
We call $x$ the $p$th root of $a$ and write $\sqrt[p]{ a }=x$
This gives us [[Functions|Functions]]:
$$
\sqrt[p]{\cdot  }:[0,\infty)\to[0,\infty)
$$
For odd $p$ we can extend this to:
$$
\sqrt[p]{\cdot  }:\mathbb{R}\to \mathbb{R}
$$
If $a<0$, then let $\sqrt[p]{ a }=-\sqrt[p]{-a  }$
## Proof
If $a=0$, $x=0$ works
Assume $a>0$, look at $A=\{ x\in\mathbb{R}\mid x^{p}<a \}$, $0\in A$, so $A$ is non-empty, 
It is [[Boundedness|bounded]] above: if $a\geq 1$, $0\leq x^p<a\leq a^{p}$, so $x^{p}<a^{p}$ and hence $x<a$, so we can use $a$ as the upper bound
If $a\in(0,1)$, then $x^{p}<1\implies x<1$, so we can use $\hspace{0pt}1$ as an upper bound
Now we can use the [[Real Numbers#Completeness Axiom|completeness axiom]] to say the $\text{sup}A$ exists, $\xi=\text{sup}A$, we want $\xi^{p}=a$, we want to show that $\xi^{p}\not<a$ and $\xi^{p}\not>a$:
Assume $\xi^{p}<a$, note $\xi \in A$, consider $\xi+\frac{1}{n}$, with $n\in\mathbb{N}$:
$$
\left( \xi+\frac{1}{n} \right)^{p}=\sum_{i=1}^{p}\begin{pmatrix}
p\\i
\end{pmatrix} \frac{\xi^{i}}{n^{p-i}}=\xi^{p}+\begin{pmatrix}
p\\1
\end{pmatrix} \frac{\xi^{p-1}}{n}+\begin{pmatrix}
p\\2
\end{pmatrix} \frac{\xi^{p-2}}{n^{2}}+\dots+\frac{1}{n^{p}}
$$
$$
\leq \xi^{p}+\frac{1}{n}\left( \begin{pmatrix}
p\\1
\end{pmatrix}\xi^{p-1}+\begin{pmatrix}
p\\2
\end{pmatrix}\xi^{p-2}+\dots+1 \right)=\xi^{p}+\frac{\alpha}{n},\alpha>0
$$
Note $\alpha$ does not depend on $n$, it is simply a real number. We want
$$
\xi^{p}+\frac{\alpha}{n}<a\iff \frac{\alpha}{n}<a-\xi^{p}\iff\alpha<\underbrace{ (a-\xi^{p}) }_{ >0 }\times n
$$
By the [[Theorem of Archimedes|Theorem of Archimedes]], there exists such an $n\in\mathbb{N}$, so for such $n$, $\left( \xi+\frac{1}{n} \right)^{p}<a$ and therefore $\xi+\frac{1}{n}\in A$, contradicting $\xi$ as an upper bound for $A$
So assume $\xi^{p}>a, so consider $\xi-\frac{1}{n}$, with $n\in\mathbb{N}$
$$
\left( \xi-\frac{1}{n} \right)^{p}=\left( \xi\left( 1-\frac{1}{\xi n} \right) \right)^{p}=\xi^{p}\left( 1-\frac{1}{\xi n} \right)^{p}\geq \xi^{p}\left( 1-\frac{p}{\xi n} \right)=\xi^{p}-\frac{\xi^{p-1}p}{n}
$$
By the [[Bernoulli Inequality|Bernoulli inequality]] 
We want 
$$
\xi^{p}-\frac{\xi^{p-1}p}{n}>a \iff \underbrace{ \xi^{p}-a }_{ >0 }>\frac{\xi^{p-1}p}{n} \iff n(\xi^{p}-a)>\xi^{p-1}p \in \mathbb{R}
$$
So again by the Theorem of Archimedes, there exists such an $n\in\mathbb{N}$, so $\xi-\frac{1}{n}$ is also an upper bond of $A$
Contradicting $\xi$ being the supremum
By trichotomy, $\xi^{p}=a$ (since it is not less than or greater than $a$)
# 
___
Let $a>0$ an $r=\frac{p}{q}$, with $p,q\in\mathbb{N}$, then define:
$$
a^{r}=\sqrt[q]{a^{p}  },\,a^{-r}=\frac{1}{a^{r}}
$$
We also set
$$
a^{0}=1
$$



 #Mathematics #Functions #Definition 