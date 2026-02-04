Let $a,b\in\mathbb{R}$, with $b>0$, then there exists $n\in\mathbb{N}$ with $nb>a$
If we think for $b=1$, then this is saying for every $a\in\mathbb{R}$, there is $n\in\mathbb{N}$ with $n>a$, so there is no number larger than the natural numbers, so they are not [[Boundedness|bounded]] above
## Proof
Assume the statement is not true, so the set $X=\{ nb\in\mathbb{R}\mid n\in\mathbb{N} \}$ is bounded avove by $a$ and is non-[[Empty Set|empty]], by the [[Real Numbers#Completeness Axiom|completeness axiom]], we have a supremum $C=\text{sup}(X)$
Look at $C-b<C$, this $C-b$ cannot be an upper bound of $X$, because if it were, then $C$ would not satisfy the second condition for a supremum. So there is $x\in X$ with:
$$
nb=x>C-b\iff nb+b=\underbrace{ (n+1)b }_{ \in  X }>C
$$
But then $C$ cannot be an upper bound of $X$, so is not the supremum, so yeah

#Mathematics #Theorem 