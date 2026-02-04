A [[Series|series]] $\sum_{k=1}^{\infty} a_{k}$ is called alternating, if $a_{2k}\geq 0$ and $a_{2k+1}\leq 0$  or if $a_{2k}\leq 0$ and $a_{2k+1}\geq 0$ for all $k\in\mathbb{N}$
## Alternating Sign Test
Let $(a_{k})_{k\in\mathbb{N}}$ be a monotonically decreasing [[Sequences|sequence]] (cannot be alternating) of positive numbers, with $\lim_{ k \to \infty }a_{k}=0$, then the alternating series:
$$
\sum_{ k=1} ^{ n}(-1)^{k+1}a_{k}
$$
Then this alternating
For the squence of partial sums $(s_{n})n\in\mathbb{N}$ 
$$
s_{2}\leq s_{n}\leq\dots \leq s_{2n}\leq\dots \leq \sum_{ k=1} ^{\infty}  (-1)^{k+1}a_{k}\leq\dots \leq s_{2n-1}\leq\dots \leq s_{3}\leq s_{1}
$$
and:
$$
\left|s_{n}-\sum_{ k=1} ^{\infty}  (-1)^{k+1}a_{k}\right|\leq a_{n+1}
$$
## Proof
Since the $a_{k}$ are monotonically decreasing, we hve $a_{k}-a_{k+1}\geq 0$. Hence, 
$$
s_{2n+2}=s_{2n}+a_{2n+1}-a_{2n+2}\leq s_{2n}
$$
Similalarly:
$$
s_{2n+1}=s_{2n-1}-a_{2n}+a_{2n+1}\leq s_{2n-1}
$$
So $(s_{2n})_{n\in\mathbb{N}}$ is monotonically increeasing, and the even terms are monotonically decreasing, so we get $s_{2}\leq s_{2n}\leq s_{2n-1}\leq s_{1}$, so sequences are bounded, hence convergent
Write
$$
s ^{e}=\lim_{ n \to \infty } s_{2n}
$$
Note $s_{2n}=s_{2n-1}-a_{2n}$, that is $a_{2n}=s_{2n-1}-s_{2n}$, by colt, $\lim_{ n \to \infty }s_{2n}=\lim_{ n \to \infty }s_{2n+1}=s\in\mathbb{R}$
To show
$$
\lim_{ n \to \infty } s_{n}=s
$$
Let $\varepsilon>0$, then there exists $n_\text{even}\in\mathbb{N}$ with $|s_{2n}-s|<\varepsilon$ whenever $2n\geq n_\text{even}$, and there exists $n_\text{odd}$ with $|s_{2n-1}-s|<\varepsilon$ whenever $2n-1\geq n_\text{odd}$
Take $n_{0}=\text{max}\{ n_\text{odd},n_\text{even} \}$, for $n\geq n_{0}$, we get $|s_{n}-s|<\varepsilon$, since $n$ is either even or odd, but since $n\geq n_\text{even}$ and $n\geq n_\text{odd}$, we can use either inequality
## Example
The series $\sum_{k=1}^{\infty} \frac{(-1)^{k+1}}{k}$, letting $a_{k}=\frac{1}{k}$ but tends to $\hspace{0pt}0$ as $k\to \infty$, we get that it is divergent, check that it is monotonically decreasing, as $\frac{1}{k+1}<\frac{1}{k}\iff k<k+1$, so by the alternating series test the series must tend to 0
___
The series $\sum_{k=1}^{\infty} \frac{(-1)^{k}}{\sqrt{ k }}$ converges by alternating sign theorem and colt, as it is equal to $-\sum_{k=1}^{\infty} \frac{(-1)^{k+1}}{\sqrt{ k }}$, and it is monotonically decreasing as $\frac{1}{\sqrt{ k+1 }}\leq \frac{1}{k}\iff k\leq k+1$ and $\frac{1}{\sqrt{ k }}\to0$ 
___
The series $\sum_{k=1}^{\infty} \frac{1}{k}+\frac{(-1)^{k+1}}{\sqrt{ k }}$, note $\frac{1}{k}<\frac{1}{\sqrt{ k }}$ for $k>1$, the summand for $k=1$ is $1+1$, the summand for $k=2$ is $\frac{1}{2}-\frac{1}{\sqrt{ 2 }}<0$, for $k=3$, it will be positive, but the evens are negative, but consider the series being written as: $\sum_{k=1}^{\infty}(-1)^{k+1}| \frac{1}{k}+\frac{(-1)^{k+1}}{\sqrt{ k }}|=b_{k}$, then $0\leq b_{k}\leq \frac{1}{k}+\frac{1}{\sqrt{ k }}\to0$
Note that the sequence is not monotonically decreasing, so we can't use the alternating sign teest here, so it is not convergent

#Mathematics #Analysis #Theorem 