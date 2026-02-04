The binomial distribution is the sum of $n$ (given and fixed) [[Independence|independent]] [[Bernoulli Distribution|Bernoulli distributions]] with probability of success $p$
So if:
$$
X_{n}\sim \text{Bernoulli}(p)
$$
$$
Y\sim B(n,p) \iff Y=\sum_{ r=1} ^{ n}  X_{r}
$$
$X:=$ numer of successes in $n$ trials,
$$
\Omega=\{ \omega\mid\omega=(\omega_{1}\omega_{2}\dots\omega_{n}),\text{ where each }\omega_{i} \text{ is a success or failure for }1\leq i\leq n\}
$$
Let us assign the value $\hspace{0pt}1$ to sucess and $\hspace{0pt}0$ to failure, so $\omega_{i}=1$ if success, and $\omega_{i}=0$ if zero
For a given $\omega=(\omega_{1}\omega_{2}\dots\omega_{n})$, $X(\omega)$ is the number for which $\omega_{i}=1$, so
$$
X(\omega)=\sum_{ i=1} ^{ n}  \omega_{i}
$$
Let $\omega=(\omega_{1}\omega_{2}\dots\omega_{n})\in\Omega$ with $x$ successes and $n-x$ failures,
$$
\mathbb{P}(\{ \omega \})=p^{x}(1-p)^{n-x}
$$
So
$$
\mathbb{P}(X=x)=\mathbb{P}\left( \bigcup_{\omega:\sum_{ i=1} ^{ n}  \omega_{i}=x}\{ \omega \} \right)=\sum_{\omega:\sum_{ i=1} ^{ n}  \omega_{i}=x}\mathbb{P}(\{ \omega \})
$$
So, since $\{ X=x \}=\{ \omega:X(\omega)=x \}=\left\{  \omega:\omega=(\omega_{1}\omega_{2}\dots\omega_{n}),\text{ then }\sum_{ i=1} ^{ n} \omega_{i}=x  \right\}$, so
$$
\sum_{\omega:\sum_{ i=1} ^{ n}  \omega_{i}=x}\mathbb{P}(\{ \omega \})={n \choose x }p^{x}(1-p)^{n-x}
$$
Which is how we obtain the pmf below
___
## [[Discrete Random Variables#Probability Mass Function|PMF]]
The probability mass function is as follows:
$$
\mathbb{P}(X=r)=f(x|n,p)=\begin{pmatrix}
n\\r
\end{pmatrix}p^{r}q^{n-r}
$$
For $r \in \{ 0,1,\dots,n \}$
This is because $p^rq^{n-r}$ is the probability of obtaining the sequence of $n$ Bernoulli trials in which the first $r$ trials are successes and the remaining $n-r$ trials result in failure. Since the trials are independent with probabilities remaining constant between them, any sequence of $n$ trials with $x$ successes has the same probability of being achieved. There are $^nC_{r}=\frac{n!}{r!(n-r)!}$ such sequences. The binomial distribution is concerned with the probability of obtaining any of these sequences, meaning the probability of one of them must be added $^nC_{r}$ times
___
## [[Expectation]]
Since a binomial distribution is the sum of $n$ independent bernoulli distributions:
$$
\mathbb{E}(Y)=\sum_{ r=1} ^{ n}  \mathbb{E}(X_{r})=\sum_{ r=1} ^{ n}p=np
$$
___
## [[Variance]]
Since a binomial distribution is the sum of $n$ independent bernoulli distributions:
$$
\mathbb{V}\mathrm{ar}(Y)=\sum_{ r=1} ^{ n}  \mathbb{V}\mathrm{ar}(X_{r})=\sum_{ r=1} ^{ n}  pq=npq
$$
___
## [[Moment Generating Functions|Moment Generating Function]]
$$
\psi(t)=\mathbb{E}(e^{ tX })=\prod_{i=1}^{n}\mathbb{E}(e^{ tX_{i} })=(pe^{ t }+q)^{n}
$$
## Requirements
The binomial distribution is a suitable modelling distribution if the following hold:
- Each trial has only two possible outcomes, success, or failure
- The number of trials, $n$, is fixed
- The probability of success, $p$, is also fixed throughout all the trials
- Trials are [[Independence|independent]] of one another
## Approximation to Normal
Let $X\sim B(n,p)$ and $0<p<1$, then
$$
B_{n}=\frac{1}{n}X
$$
and
$$
Z_{n} = \frac{X_{n}-np}{np(1-p)}=\frac{B_{n}-p}{\sqrt{ p(1-p) }}
$$
Then $\lim_{ n \to \infty }F_{Z_{n}}(z)=\lim_{ n \to 0 }\mathbb{P}(Z_{n}\leq z)=\Phi(z_{n})$





#Mathematics #Statistics #Distribution 