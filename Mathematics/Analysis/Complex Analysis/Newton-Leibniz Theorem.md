## Theorem
Let $U\subset \mathbb{C}$ be an [[Open Sets|open set]] and let $F:U\to \mathbb{C}$ be a [[Holomorphicity|holomorphic]] [[Complex Functions|function]] with [[Continuity|continuous]] [[Differentiation|derivative]] $f$. Then for any [[Contour Integration|contour]] $\gamma:[a,b]\to U$, we have
$$
\int _{\gamma}f(z) \, dz=F(\gamma(b))-F(\gamma(a)) 
$$
In particular, if $\gamma$ is closed, that is, $\gamma(a)=\gamma(b)$, then we have that
$$
\int _{\gamma} f(z) \, dz=0 
$$
### Proof
Let us start by considering $C^{1}$ paths. For a $C^{1}$ path $\gamma$, we have that
$$
\int _{\gamma } f(z) \, dz=\int ^{b}_{a} f(\gamma(t))\gamma'(t) \, dt =\int ^{b}_{a} F'(\gamma(t))\gamma'(t) \, dt 
$$
$$
= \int ^{b}_{a} (F(\gamma(t)))' \, dt=\int ^{b}_{a} \mathfrak{R}(F(\gamma(t)))' \, dt+i\int ^{b}_{a} \mathfrak{I}(F(\gamma(t)))' \, dt 
$$
$$
= \mathfrak{R}(F(\gamma(t)))\bigg{|}_{a} ^{b}+i\mathfrak{I}(F(\gamma(t)))\bigg{|}_{a}^{b}=F(\gamma(t))\bigg{|}_{a}^{b}=F(\gamma(b))       -F(\gamma(a)) 
$$
Where we have used the [[Chain Rule|chain rule]] for paths and the [[Fundamental Theorem of Calculus|fundamental theorem of calculus]] on $\mathbb{R}$
We now turn our attention to piecewise contours. Let $\gamma$ be a contour and let $a=a_{0}<a_{1}<\dots<a_{n}=b$ be a [[Set Partition|partition]] of $[a,b]$ for which $\gamma_{i}=\gamma \big{|}_{[a_{i-1},a_{i}]}$ are $C^{1}$ curves. Then
$$
\int _{\gamma} f(z) \, dz = \sum_{i=1}^{n} \int _{\gamma_{i}}f(z) \, dz =\sum_{ i=1} ^{ n}  (F(\gamma(a_{i}))-F(\gamma(a_{i-1})))
$$
$$
= F(\gamma(a_{n}))-F(\gamma(a_{0}))=F(\gamma(b))-F(\gamma(a))
$$
As the sum is telescoping and the middle terms cancel
## Remark
Finding antiderivatives is not a trivial thing, and this is our main restriction
Due to Morera's lemma, 
## Example
For $r>0$ we have for any $a\in \mathbb{C}$,
$$
\int _{\left| z-a \right| =r}(z-a)^{n} \, dz =\begin{cases}
0 & n\neq -1 \\
2\pi i & n=-1
\end{cases} 
$$
So $f(z)=\frac{1}{z}$ is holomorphic on $\mathbb{C}\setminus \left\{  0 \right\}$ but doesn't have a holomorphic antiderivative, as that would mean its integral would have to be $\hspace{0pt}0$, contradicting Newton-Leibniz
We do know that it kinda has the antiderivative $\log$, but this has the issue that the branch cut is messing things up :/