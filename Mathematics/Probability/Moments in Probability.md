## Definition
Let $X$ be a [[Random Variables|random variables]], then its $k$th moment when it exists, is defined by $\mathbb{E}(X^{k})$ for $k\geq 1$
## Theorem
If $X$ has [[probability Generating Functions|generating function]] $G(s)$, then the $k$th factorial moment of $X$ satisfies
$$
\mathbb{E}(X(X-1)\dots (X-k+1))=\frac{d ^{k}}{ds^{k}} G_{X}(1_{-}):=\lim_{ s\nearrow 1 } \frac{d ^{k}}{ds^{k}} G(s) 
$$
### Proof
Recall we can differentiate generating functions termwise, so we fix $s\in(0,1)$ and differentiate $G(s)$ $k$ times to get
$$
\frac{d ^{k}}{dx^{k}} G(s)=\mathbb{E}(s^{X-k}X(X-1)\dots(X-k+1))
$$
Taking the limit $s\nearrow 1$ and using Abel's theorem, we obtain the result
## Remark
We can rearrange a factorial moment to obtain the normal or polynomial moments, for exampe the second moment of $X$ satisfies
$$
\mathbb{E}(X^{2})=G''_{X}(1)+G'_{X}(1)
$$
## Remark
We also have
$$
\lim_{ s\nearrow 1 } \mathbb{E}(s^{X})=\mathbb{P}(X<\infty)
$$
This allows us to check whether a variable is finite, if we don't know this a priory


#Mathematics #Probability  #Definition 