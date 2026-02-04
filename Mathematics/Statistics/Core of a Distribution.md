For a [[Random Variables|random variable]] $X$ with pdf $f(x)$, if we can express theits pdf $f(x)$ in the form
$$
f(x)=C\kappa(x)
$$
Where $C>0$ is a constant that doesn't depend on $x$, then we call $\kappa(x)$ the core, or [[Kernel|kernel]] of the density $f(x)$
## Lemma
Each core of a distribution $\kappa(x)$ corresponds to a unique pdf, $f(x)$
### Proof
Following the definition above, let $\kappa(x)$ be such hat $f(x)=C\kappa(x)$, where $f(x)$ is a valid pdf. For $f(x)$ to be valid, we must have that
$$
\int_{-\infty}^{\infty} f(x) \, dx =1\implies \int_{-\infty}^{\infty} \kappa(x) \, dx=\frac{1}{C} 
$$
Now suppose there exists another valid pdf $g(x)$ which also is associated with $\kappa(x)$, so $g(x)=B\kappa(x)$, then
$$
\int_{-\infty}^{\infty} g(x) \, dx =B\int_{-\infty}^{\infty} \kappa(x) \, dx =\frac{B}{C}
$$
But for $g(x)$ to be valid, it must integrate to $\hspace{0pt}1$, which implies $B=C$. Therefore
$$
g(x)=C\kappa(x)=f(x)
$$
So $f(x)$ is unique