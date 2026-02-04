## Functions of $\hspace{0pt}1$ Variable
A [[Functions\Bigg{|}function]] $f:\mathbb{R}\to \mathbb{R}$ $f(s)$ has an [[Critical Points\Bigg{|}extremum]] (maximum or minimum) at $s=s_{0}$ if
$$
\frac{d f}{ds} \Bigg{|}_{s=s_{0}}=0
$$
Equivalently we can take the [[Taylor Series|taylor series]] at $s_{0}$:
$$
f(s+\delta s)=f(s_{0})+\delta s \frac{d f}{ds} \Bigg{|}_{s=s_{0}} + \frac{1}{2}(\delta s)^{2} \frac{d ^{2}f}{ds^{2}} \Bigg{|}_{s=s_{0}}+\dots 
$$
$$
 \iff f(s_{0}+\delta s)-f(s_{0})=\frac{1}{2}(\delta s)^{2} \frac{d ^{2}f}{ds^{2}} \Bigg{|}_{s=s_{0}}+\dots
$$
We define
$$
\delta f=f(s_{0}+\delta s)-f(s_{0})
$$
And [[o Notation|$\delta f=O((\delta s)^{2})$]] 
## Functions of $N$ Variables
A function $f:\mathbb{R}^{N}\to \mathbb{R}$, $f(s_{1},\dots,s_{N})$ has extrema at points $\underline{s}_{0}$ such that
$$
\underline{\nabla } f(\underline{s}_{0})=0
$$
$$
 \iff \frac{ \partial f }{ \partial s_{i} } \Bigg{|}_{\underline{s}= \underline{s}_{0}}=0\forall i\in \overline{N}
$$
In this case we define
$$
\delta f=f(\underline{s}+\underline{\delta s})-f(\underline{s}_{0})=f(\underline{s}_{0})-f(\underline{s}_{0})+ \sum_{i=1}^{N} \frac{ \partial f }{ \partial s } \Bigg{|}_{\underline{s}=\underline{s}_{0}}+\frac{1}{2}\sum_{i,j}\delta s_{i}\delta s_{j}\frac{ \partial^{2}f }{ \partial s_{i} \partial s_{j} }
$$
$$
= \frac{1}{2}\sum_{i,j}\delta s_{i}\delta s_{j}\frac{ \partial^{2}f }{ \partial s_{i} \partial s_{j} }=O(\underline{\delta s}^{2}) 
$$

![[Calculus of Variations 2026-01-12 14.49.21.excalidraw]]
For $N$ dimensions,
$$
\frac{d f(\underline{s}_{0}+\epsilon \underline{z})}{d\epsilon} \Bigg{|}_{\epsilon=0}= \frac{d }{d\epsilon}  \left[ f(\underline{s}_{0})+\epsilon \sum_{i=1}^{N} z_{i}\frac{ \partial f }{ \partial s_{i} } +O(\epsilon^{2}) \right]_{\epsilon=0}=0
$$
$$
= 0+\sum_{i=1}^{N}z_{i}\frac{ \partial f }{ \partial s_{i} } +O(\epsilon)\Bigg{|}_{\epsilon=0}=0
$$
From now we call $\epsilon z(t)=\delta y(t)$, so we rewrite this concept as:
$$
S[y(t)+\delta y(t)]=S[y(t)]+\epsilon \frac{d S[y(t)+\delta y(t)]}{d\epsilon}\Bigg{|}_{\epsilon=0}+O(\epsilon^{2})
$$
$$
\implies S[y(t)+\delta y(t)]-S[y(t)]=O(\epsilon^{2}) 
$$
We call this $\delta S$ similarly to above
$$
\delta S=S[y(t)+\delta y(t)]-S[y(t)]=O((\delta y)^{2})
$$
We can consider the $y(t)$ as paths
