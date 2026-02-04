## Real [[Sequences|Sequences]]
Let $(x_{n})_{n\in\mathbb{N}}$ and $(y_{n})_{n\in\mathbb{N}}$ be sequences which are [[Convergence|convergent]] with $x=\lim_{ n \to \infty }x_{n}$ and $y=\lim_{ n \to \infty }y_{n}$. Also let $a,b\in\mathbb{R}$. Then:
$$
\lim_{ n \to \infty } (ax_{n}+by_{n})=ax+by
$$
$$
\lim_{ n \to \infty } (x_{n}y_{n})=xy
$$
$$
\lim_{ n \to \infty } \left( \frac{x_{n}}{y_{n}} \right)=\frac{x}{y}
$$
(Provided $y\neq 0$ and $y_{n}\neq 0\forall n\in\mathbb{N}$)
### Proof
Proof of the second part:
We need to know about $|x_{n}y_{n}-yx|<\varepsilon$ for all $n\geq N_\varepsilon$
$$
|x_{n}y_{n}-xy|=|x_{n}y_{n}-x_{n}y+x_{n}y-xy|
$$
And by the triangle inequality:
$$
\leq|x_{n}(y_{n}-y)|+|(x_{n}-x)y|=|x_{n}||y_{n}-y|+|x_{n}-x| |y|
$$
We can now make $|x_{n}-x|$ and $|y_{n}-y|$arbitrarily small, and then we only have $|x_{n}|$ to worry about
Note there is a $c>0$ with $|x_{n}|\leq c$ since [[Every Convergent Sequence is Bounded|convergent sequences are bounded]]
We can also assume that $c\geq|y|$, then
$$
|x_{n}y_{n}-xy|\leq c(|y_{n}-y|+|x_{n}-x|)
$$
Now let $\varepsilon>0$, there exists an $N_{\varepsilon1}$ and $N_{\varepsilon 2}$ with
$$
|y_{n}-y|<\frac{\varepsilon}{2c} \forall n\geq N_{\varepsilon 1}
$$
$$
|x_{n}-x|<\frac{\varepsilon}{2c} \forall n\geq N_{\varepsilon 2}
$$
Then for all $n\geq \text{max}(N_{\varepsilon 1},N_{\varepsilon2})$ we have:
$$
|x_{n}y_{n}-xy|\leq c(|y_{n}-y|+|x_{n}-x|)<c\left( \frac{\varepsilon}{2c}+\frac{\varepsilon}{2c} \right)=\varepsilon
$$
$W^5$
### Consequences
#### Double of a Convergent Sequence Converges to Double the Limit
If $a_{n}$ is a sequence which converges to $l$ and $b_{n}$ is the sequence defined by $b_{n}=2a_{n}$, then $b_{n}$ converges to $2l$
##### Proof
Given $a_{n}$ converges to $l$ and $b_{n}=2a_{n}$
If $\varepsilon>0$ then $\exists N_{\varepsilon}:n\geq N_{\varepsilon}\implies \left| a_{n}-l \right|<\varepsilon$
Also since $\frac{\varepsilon}{2}>0$, then $\exists N_{a}:n\geq N_{a}\implies \left| a_{n} -l \right|<\frac{\varepsilon}{2}$ so
$$
-\frac{\varepsilon}{2}<a_{n}-l<\frac{\varepsilon}{2}
$$
$$
\implies -\varepsilon<2a_{n}-2l<\varepsilon 
$$
$$
\implies \left| 2a_{n}-2l \right|<\varepsilon 
$$
$$
\implies \left| b_{n}-2l \right|<\varepsilon
$$
So $b_{n}$ converges to $2l$
___
#### The Sum of Two Sequences which Converge to 0 will Converge to 0
If $a_{n}$ and $b_{n}$ are sequences of real numbers which both converges to 0, then $a_{n}+b_{n}$ converges to 0
##### Proof
Given $a_{n}$ and $b_{n}$ both converge to 0, then if $\varepsilon>0$ then there also exists $\frac{\varepsilon}{2}>0$ such that:
$$
\exists N_{a}:n\geq N_{a}\implies \left| a_{n} \right|<\frac{\varepsilon}{2}
$$
$$
\exists N_{b}:n\geq N_{b}\implies \left| b_{n} \right|<\frac{\varepsilon}{2}
$$
So if $N=max(N_{a},N_{b})$, then if $n\geq N$ then $\left| a_{n} \right|<\frac{\varepsilon}{2}$ and $\left| b_{n} \right|<\frac{\varepsilon}{2}$ so
$$
\left| a_{n}+b_{n} \right|\leq \left| a_{n} \right|+\left| b_{n} \right|
$$
From [[Triangle Inequality|this]] theorem
$$
\implies \left| a_{n}+b_{n} \right|<\frac{\varepsilon}{2}+\frac{\varepsilon}{2}=\varepsilon 
$$
$$
\implies \left| a_{n}+b_{n}-0 \right|<\varepsilon
$$
So $a_{n}+b_{n}$ converges to 0
___
#### The Negative of a Convergent Sequence Converges to the Negative Limit
If $a_{n}$ is a sequence which converges to $l$ and $b_{n}=-a_{n}$, then $b_{n}$ converges to $-l$
##### Proof
If $a_{n}$ is a sequence converging to $l$ and $b_{n}=-a_{n}$ then:
$$
\forall\varepsilon>0,\exists N_{\varepsilon}\in\mathbb{N}:n\geq N_{\varepsilon}\implies \left| a_{n}-l \right|<\varepsilon 
$$
$$
\implies -\varepsilon <a_{n}-l<\varepsilon 
$$
$$
\implies \varepsilon>-a_{n}+l>-\varepsilon 
$$
$$
\implies \varepsilon>b_{n}-(-l)<-\varepsilon 
$$
$$
\implies \left| b_{n}-(-l) \right|<\varepsilon
$$
So $b_{n}$ converges to $-l$
___
#### If a Sequence Converges to 0, then a Vertical Translation of the Sequence will Converge to the Translation Factor
If $a_{n}$ is a [[Sequences|sequence]] which [[Convergence|converges]] to 0 and $b_{n}=a_{n}+k$, then $b_{n}$ converges to $k$
##### Proof
Given $a_{n}$ converges to 0 and $b_{n}=a_{n}+k$
Then $\forall\varepsilon>0,\exists N_{\varepsilon}\in\mathbb{N}:n\geq N_{\varepsilon}\implies \left| a_{n} \right|<0$ so
$$
-\varepsilon<a_{n}<\varepsilon 
$$
$$
\implies -\varepsilon<a_{n}+k-k<\varepsilon 
$$
$$
\implies -\varepsilon<b_{n}-k<\varepsilon 
$$
$$
\implies \left| b_{n}-k \right|<\varepsilon
$$
So $b_{n}$ converges to $k$
___
### Example
Consider a sequence:
$$
x_{n}=\frac{n^{3}-2n^{2}+3n-4}{3n^{4}+10n^{2}-8}=\frac{n^{3}\left( 1-\frac{2}{n}+\frac{3}{n^{2}}-\frac{4}{n^{3}} \right)}{n^{4}\left( 3+\frac{10}{n^{2}}-\frac{8}{n^{4}} \right)}
$$
$$
= \frac{1}{n}\left( \frac{1-\frac{2}{n}+\frac{3}{n^{2}}-\frac{4}{n^{3}}}{3+\frac{10}{n^{2}}-\frac{8}{n^{4}}} \right)
$$
Each part divided by $n^{r}$ goes to $\hspace{0pt}0$, and so by COLT,
$$
\lim_{ n \to \infty } x_{n}=0\times \frac{1}{3}=0
$$
___
$x_{1}=1$, $x_{n}=\frac{x_{n-1}}{2}+\frac{1}{x_{n-1}}$ for $n\geq 2$
$x_{n}\in[1,2]$ by induction, since $x_{1}\in[1,2]$
If $x_{n-1}\in[1,2]$, then
$$
\frac{x_{n-1}}{2}\in \left[ \frac{1}{2},1 \right]
$$
$$
\frac{1}{x_{n-1}}\in \left[ \frac{1}{2},1 \right]
$$
So by adding them, 
$$
x_{n}\in [1,2]
$$
Let us assume that $x_{n}$ converges to $x$, then $x_{n-1}$ also converges to $x$, so by COLT:
$$
x=\lim_{ n \to \infty } x_{n}=\lim_{ n \to \infty }\left( \frac{x_{n-1}}{2}+\frac{1}{x_{n-1}} \right)=\frac{x}{2}+\frac{1}{x}
$$
$$
\implies x^{2}=2
$$
So we have two candidates, $x=\sqrt{ 2 }$ or $x=-\sqrt{ 2 }$, but $-\sqrt{ 2 }$ is not in our interval, so we can ignore it
Now we can use the [[Squeeze Theorem|squeeze thorem]] to show convergence:
$$
|x_{n}-\sqrt{ 2 }|=\left|\frac{x_{n-1}}{2}+\frac{1}{x_{n-1}}-\sqrt{ 2 } \right|=\left| \frac{x_{n-1}^{2}+2-2\sqrt{ 2 }x_{n-1}}{2x_{n-1}} \right|=\frac{(x_{n-1}-\sqrt{ 2 })^{2}}{2x_{n-1}}
$$
As the numerator is squared, and $x_{n-1}\in[1,2]$
$$
\therefore |x_{n}-\sqrt{ 2 }|\leq \frac{|x_{n-1}-\sqrt{ 2 }|}{2}\leq \frac{|x_{n-2}-\sqrt{ 2 }|}{4}\leq\dots
$$
So
$$
|x_{n}-\sqrt{ 2 }|\leq \frac{1}{2^{n}}
$$
And we know $\frac{1}{2^{n}}$ is a case of [[Convergence#In the form of $x_{n}=c {n}$|$c^{n}$]], so we know it converges to $\hspace{0pt}0$, so $x_{n}-\sqrt{ 2 }$ tends to $\hspace{0pt}0$, so $x_{n}$ tends to $\sqrt{ 2 }$
## Complex Sequences
Limits in the complex plane follow the COLT rules (where $i$ is treated as constant)
## [[Series|Series]]
Assume the series $\sum_{k=0}^{\infty} a_{k}$ and $\sum_{k=0}^{\infty} b_{k}$ are convergent with limits $a$ and $b$ respectively, then:
$$
\sum_{k=0}^{\infty}a_{k}+b_{k}
$$
Converges to $a+b$
$$
\sum_{k=0}^{\infty}ca_{k}
$$
Converges to $ca$, where $c\in\mathbb{R}$
The proof is obtained by using CoLT for sequences on the partial sums
## [[Functions|Functions]]
Let $f(x)$ and $g(x)$ be functions which are convergent with $\lim_{ x \to c }f(x)=L_{1}$ and $\lim_{ x \to c }g(x)=L_{2}$ Then:
$$
\lim_{ x \to c } (af(x)+bg(x))=aL_{1}+bL_{2}
$$
$$
 \lim_{ x \to c }( f(x)g(x))=L_{1}L_{2}
$$
$$
\lim_{ x \to c } \left( \frac{f(x)}{g(x)} \right)=\frac{L_{1}}{L_{2}}
$$
Provided $L_{2}\neq 0$
### Proof
The proofs work by using the [[Limit#Link to Sequences|link to sequences]], and apply for sequences
For example, take $x_{n}\to c$, then
$$
\lim_{ n \to \infty } f(x_{n})g(x_{n})=\lim_{ n \to \infty } f(x_{n})\lim_{ x \to \infty } g(x_{n})=\lim_{ x \to c } f(x)\lim_{ x \to c } g(x)=L_{1}L_{2}
$$
## [[Continuity|Continuity]]
If we have $f,g$ continuous at $c$. Then
- $af(x)+bg(x)$ is continuous at $c$ 
- $f(x)g(x)$ is continous at $c$
- if $g(c)\neq 0$, then $\frac{f(x)}{g(x)}$ is continous at $c$
- if $f$ and $g$ are continuous on appropriate sets and the range of $f$ is in the domain of $g$, then $g\circ f$ is continuous
This is true for [[Real Functions|real]] and [[Complex Functions|complex]] functions
The proof is by using hte link to sequences
## [[Differentiation|Differentiability]]
If we have $f,g$ differentiable at $z_{0}$, then
- $f+g$ is differentiable at $z_{0}$, and
$$
(f+g)'(z_{0})=f'(z_{0})+g'(z_{0})
$$
- $fg$ is differentiable at $z_{0}$
- quotient rule
- chain rule 
Works for real and complex functions



#Mathematics #Analysis #Theorem 