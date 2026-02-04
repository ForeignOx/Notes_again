## Definition
A function $y(t)$ is stationary for the [[Functionals|functional]] $S$ if
$$
\frac{dS[y(t)+\epsilon z(t)]}{d\epsilon} \Bigg{|}_{\varepsilon=0}=0
$$
For all smooth $z(t)$ such that $z(a)=z(b)=0$
## Remark
This definition encodes the idea that the path $y(t)$ extremises the action $S$ in the space f paths starting at $y_{a}$ and ending at $y_{b}$. To see this, think of the function $z(t)$ as an arbitrary choice of direction in the space of deformations. The condition is then saying that $S[y(t)]$ is extremised along this direction. ince $z(t)$ is arbitrary, we have that the condition is satisfied in every direction in function space. It might be help to compare with how you could impose that an ordinary function $f(\underline{x})$ depending on a vector $\underline{x}$ has an extremum at $\underline{x}_{0}$. You could impose
$$
\frac{d f(\underline{x}_{0}+\epsilon \underline{z})}{d\epsilon} \Bigg{|}_{\epsilon=0} =\left[ \frac{d }{d\epsilon} \left( f(\underline{x}_{0})+\epsilon \sum_{i}z_{i}\frac{ \partial f(\underline{x})x }{ \partial x_{i} } \Bigg{|}_{\underline{x}=\underline{x}_{0}} +\mathcal{O}(\epsilon^{2}) \right) \right]_{\epsilon=0}
$$
$$
 =\sum_{i=1}^{n}z_{i}\frac{ \partial f(\underline{x}) }{ \partial x_{i} } \Bigg{|}_{\underline{x}=\underline{x}_{0}} =0
$$
For every choice of vector $\underline{z}$. This is equivalent to iiposing the familiar condition
$$
\frac{ \partial f(\underline{x}) }{ \partial x_{i} } \Bigg{|}_{\underline{x}=\underline{x}_{0}} =0
$$
For all $i$ which ensures the existence of an [[Critical Points|extremum]] (or saddle point) at $\underline{x}=\underline{x}_{0}$
___
Consider the [[Taylor Series|Taylor]] expansion in $\epsilon$ (which is a constant) of $S[y(t)+\epsilon z(t)]$:
$$
S[y(t)+\epsilon z(t)]=S[y(t)]+\epsilon \frac{d S[y(t)+\epsilon z(t)]}{d\epsilon} \Bigg{|}_{\epsilon=0} +\frac{1}{2}\epsilon^{2} \frac{d ^{2}S[y(t)+\epsilon z(t)]}{d\epsilon^{2}} \Bigg{|}_{\epsilon=0} +\dots
$$
The condition for $y(t)$ to be stationary is that the term proportional to $\epsilon$ vanishes:
$$
\delta S:=S[y(t)+\epsilon z(t)]-S[y(t)]=\mathcal{O}(\epsilon^{2})
$$
It is useful to think of the combination $\epsilon z(t)$ as a small variation of $y(t)$, which we denote $\delta y(t):=\epsilon z(t)$
We define [[o Notation|$\mathcal{O}((\delta y(t))^{n})$]] to mean simply $\mathcal{O}(\epsilon^{n})$
In particular, we can rewrite the stationary condition as
$$
\delta S=\mathcal{O}((\delta y(t))^{2})
$$
One can always replace $\delta y(t)$ with $\epsilon z(t)$ and expand in the constant $\epsilon$, for example, the integral:
$$
\int g(t)(\delta y(t))^{n} \, dt 
$$
For any $n\in\mathbb{N}$ and function $g(t)$. I claim that this is $\mathcal{O}((\delta y(t))^{n})$; replacing $\delta y(t)$ with $\epsilon z(t)$ we have
$$
\int g(t)\epsilon^{n}z(t)^{n} \, dt=\epsilon^{n}\int g(t)z(t)^{n} \, dt  
$$
In our $\mathcal{O}((\delta y(t))^{n})$ notation, this means that
$$
\int \mathcal{O}((\delta y(t))^{n}) \, dt=\mathcal{O}((\delta y(t))^{n}) 
$$
That is, integration does not change the order in $\delta y(t)$ (which, once more, when talking about action functions is used to define the order in $\epsilon$)
___
Do to the relevance in dynamical problwems, one often refers to functions $y(t)$ as paths, so that the conditions above define a stationary path