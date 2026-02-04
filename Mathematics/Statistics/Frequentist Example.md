We are polling station, $\hspace{0pt}485$ said Harris, $\hspace{0pt}515$ said Trump, what do I say about the result of the election? Do I trust this? Would I bet on it?
If we pick a person at random from Pennsylvania at random then they will have probability $p$ of saying (truthfully) that they will vote for Trump, where $p$ is the proportion of Trump voters in the state, so $p=\frac{N_\text{Trump}}{N}$, with $N$ being the total voters in the state, but this value of $p$ is unknown (we will assume people are telling the truth here)
If we choose $n$ random people (sample), then it is the same, each has probability $p$, provided the sample is small compared to the total population of voters $N$; $n\ll N$ 
## Probability vs Statistics
A typical probability question would involve telling you the probability $p$ and then having to calculate the probabilities of various configurations of $X_{1},\dots,X_{n}$. However, in statistics we want to go a step further: following a real world experiment, we would be told the results:
$$
X_{1}=x_{1},X_{2}=x_{2},\dots,X_{n}=x_{n}
$$
And then have to infer something meaningful about the unknown probability $p$. This is referred to as inference
## Statistical Inference
Think about what $p$ actually is:
real fixed with "true" value that is 
- just unknown (frequentist)
- an unknown quantity for which we should represent our subjective unceertainty about via a probability distribution (Bayesian/subjective)
## Totals and Samples Propotions as Estimators
First lets redefine $X$ to be the sum of all successes (values of 1) over the $n$ trials:
$$
X=\sum_{i=1}^{n}X_{i}
$$
With
$$
X_{i}=\begin{cases}
1&\text{if success}\\0&\text{if failure}
\end{cases}
$$
We want to estimate $p$, but first we want to examine the pmf for the set of Bernoulli trials $X_{1},\dots,X_{n}$. As the $X_{i}$'s are independent, we can just multiply their pmfs
$$
\implies f(x_{1},x_{2},\dots,x_{n}|p)=\prod_{i=1}^{n}f(x_{i}|p)=\prod_{i=1}^{n}p^{x_{i}}q^{1-x_{i}}
$$
$$
= p^{\prod_{i=1}^{n}x_{i}}q^{\prod_{i=1}^{n}(1-x_{i})}=p^{x}q^{n-x}
$$
Where
$$
x=\sum_{ i=1} ^{ n}  x_{i}
$$
Note this only depends on $p,n$ and $x$. This is a dramatic simplification of information, an example of dimensional reduction, data compression and sufficiency
Perhaps we should construct an estimator for $p$ using only $x$ and $n$? How about we ask what (proposed/estimated) value of $p$ would actually maximise the pmf $f(x_{1},\dots,x_{n}|p)$? Surely this will be good!
The trick is to maximise $\ln(f(x_{1},x_{2},\dots,x_{n}|p))$ as $\ln$ is monotonic, so maxima are the same (and it's easier to differentiate) so
$$
f(x_{1},x_{2},\dots,x_{n}|p)=p^{x}q^{n-x}
$$
$$
\implies \ln(f(x_{1},\dots,x_{n}|p))=x\ln p+(n-x)\ln(1-p)
$$
$$
\implies \frac{ \partial  }{ \partial p } \ln(f(x_{1},\dots,x_{n}|p))=\frac{x}{p}-\frac{n-x}{1-p}
$$
We set this equal to $\hspace{0pt}0$ to find our estimate $\hat{p}$
$$
\frac{x}{\hat{p}}- \frac{n-x}{1-\hat{p}}=0
$$
$$
\implies x(1-\hat{p})=(n-x)\hat{p}
$$
$$
\implies x=n\hat{p}
$$
$$
\implies \hat{p}=\frac{x}{n}
$$
So we have shown that a good estimator for the true $p$ is the sample proportion. This is a very intuitive/obvious result
We often dentote this as $Y$ and interms of random variables;
$$
\hat{p}=Y=\frac{X}{n}=\frac{1}{n}\sum_{i=1}^{n}X_{i}
$$
Note that $\hat{p} =Y$ is also the mean of the $X_{i}$'s but is $\hat{p}$ any good?
## Sample Proportion $\hat{p}$ as an Estimator $p$
How good is $\hat{p}=Y$ as an estimator for $p$
As $X\sim B(n,p)$
$$
E(\hat{p})=E(Y)=E\left( \frac{X}{n} \right)=\frac{1}{n}E(X)=\frac{1}{n}np=p
$$
Which is what we want to estimate, now importantly we want the variance, telling us how far from $p$ it will be:
$$
Var(\hat{p})=Var(Y)=Var\left( \frac{X}{n} \right)=\frac{1}{n^{2}}Var(X)=\frac{1}{n^{2}}npq=\frac{pq}{n}=\frac{p(1-p)}{n}
$$
We have that $E(\hat{p})=p$, so we say that the estimator is unbiased. As we have $Var(\hat{p})=\frac{p(1-p)}{n}$, we now have some understanding and some control over how accurate $\hat{p}$ is 
## Normal Approximation
As $X\sim B(n,p)$ and $\hat{p}=Y=\frac{X}{n}$, we can calculate probabilities for $\hat{p}$ but if $n$ is large, this can be cumbersome, so we can just use the Normal approximation;
$$
X\sim N(np,np(1-p))
$$
(Approximation is ok if $np\gg1$, and $n(1-p)\gg 1$), so 
$$
\hat{p}=Y\sim N\left(p, \frac{p(1-p)}{n}\right)
$$
(Also need a continuity correction)
## Margin of Error
So how accurate is $\hat{p}$? The Margin of Error of an estimate can be roughly defined as $\hspace{0pt}2$ standard deviations on either side of the estimate, suggesting the true value of $p$ may lie in an interval of the form:
$$
Y\pm2s\sqrt{ \frac{p(1-p)}{n} }
$$
This is pretty useless, since the accuracy involves $p$, which is what we are guessing
However we can find a bound on the Margin of Error by finding the max of $p\in[0,1]$, for the quadratic $p(1-p)=\frac{1}{4}$, when $p=\frac{1}{2}$, so the margin of error:
$$
2\sqrt{ \frac{p(1-p)}{n} }\leq 2\sqrt{ \frac{1}{4n} }=\frac{1}{\sqrt{ n }}
$$
No matter what value $p$ takes
Therefore we have the interval $Y\pm \frac{1}{\sqrt{ n }}$, a very widely used result
## US Presiential Election !!
It 22nd Oct $\hspace{0pt}2024$,we are about to ask $\hspace{0pt}1000$ people in our poll. 
Question 1: find the expected value and marginal error for the proportion of Trump voters in our sample if we were magically told that $p=0.5$, or $p=0.3$
The answer for $p=0.5$, is $E(X)=np=1000\times 0.5=500$, $E(\hat{p})=p=0.5$, $Var(X)=np(1-p)=250$
$SD(X)=15.8$ people, $Var(\hat{p})=\frac{p(1-p)}{n}=0.00025$, so our margin of error is equal to $2\sqrt{ \frac{p(1-p)}{n} }=0.0316$ or 3.16%
The answer for $p=0.3$, $E(\hat{p})=0.3$, and the margin of error is equal to $0.0290$, which is 2.90%
Question 2: Poll has been performed, $n=1000$, $\hspace{0pt}515$ for trump, $\hspace{0pt}485$ for Harris. What is your estimate for $p$ and its margin of Error?
$$
\hat{p}=\frac{x}{n}=\frac{515}{1000}
$$
We do not know $p$, so we use the maximum bound for the margin of error
$$
\frac{1}{\sqrt{ n }}=\frac{1}{\sqrt{ 1000 }}=0.0316=3.16\%
$$
So we think $p$ will lie in the interval
$$
51.5\%\pm3.16\%
$$
Question 3: Your company has time to perform one more poll before the election. How large a poll is needed to ensure a Margin of Error less than $1\%$?
The answer is that $\frac{1}{\sqrt{ n }}<0.01\iff n>10000$ so it unlikely we getting that

#Mathematics #Statistics 