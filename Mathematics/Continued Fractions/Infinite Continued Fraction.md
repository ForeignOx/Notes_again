For some $a_{0}\in\mathbb{Z}$, and $a_{k}\in\mathbb{Z}^+$, we define the infinite [[Continued Fraction]] $[a_{0},a_{1},a_{2},\dots]=\lim_{ n \to \infty }c_{n}$ (where $c_{n}$ is the $n$th [[Convergents|convergent]]). An infinite continued fraction looks like
$$
a_{0}+\frac{1}{a_{1}+\frac{1}{a_{2}+\frac{1}{\ddots}}}
$$
## An infinite continued fraction [[Convergence|converges]] if the sequence of convergents, $\{ c_{n} \}$ converges
### Proof
Firstly note that [[Convergents#A real number $x$ with convergents $c_{n}= frac{p_{n}}{q_{n}}$ satisfies $ x-c_{n} < frac{1}{q_{n}q_{n+1}}$|this lemma]] holds if $y_{n+1}$ is not necessarily rational. We know
$$
\left| x-c_{n} \right|<\frac{1}{q_{n}q_{n+1}}\leq \frac{1}{q_{n}(q_{n})}
$$
As $q_{n+1}\geq a_{n}\forall n$
$$
=\frac{1}{q_{n}^{2}}\leq \frac{1}{n^{2}}
$$
As $q_{n}\geq n\forall n$
So we want to choose some $N_{\epsilon}$ such that $\frac{1}{N_{\epsilon}}<\epsilon$: let $N_{\epsilon}=\left\lceil  \frac{1}{\sqrt{ \epsilon }}  \right\rceil+1$
Then, given that we know $\left| x-c_{n} \right|<\frac{1}{n^{2}}$ and $\epsilon>0$, if $n\geq N_{\epsilon}$:
$$
n\geq c\left\lceil  \frac{1}{\sqrt{ \epsilon }}  \right\rceil +1>\left\lceil  \frac{1}{\sqrt{ \epsilon }}  \right\rceil \geq \frac{1}{\sqrt{ \epsilon }}
$$
$$
\implies \sqrt{ \epsilon }>\frac{1}{n}
$$
as $\epsilon>0,n\geq N_{\epsilon}>0$
$$
\implies \epsilon>\frac{1}{n^{2}}
$$
Hence $\left| x-c_{n} \right| <\frac{1}{n^{2}}<\epsilon$ and so $c_{n}$ converges to $x$ as required


#Mathematics #Fractions #Definition #Theorem