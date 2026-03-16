We recall a key theorem of invariant distributions, if $\left| I \right|<\infty$ and there exists $i\in I$ such that the limit
$$
\lim_{ n \to \infty } P_{ij}^{(n)}=\pi_{j}
$$
Exists for all $j\in I$, then $\pi=(\pi_{j})_{j\in I}$ is an invariant distribution for $P$
When does this convergence actually happen? Does it always happen?
## Counterexample
Consider the Markov chain:
![[Pasted image 20260316121246.png]]
Clearly this is periodic with period $\hspace{0pt}2$, $X_{n}$ simply alternates between $A$ and $B$, we see that
$$
P_{AA}^{n}=\begin{cases}
1 & n\text{ even} \\
0 & n\text{ odd}
\end{cases}
$$
Therefore $\lim_{ n \to \infty }P_{A A}^{n}$ doesn't exist
Periodicity turns out to be essentially the only problem!
## Theorem
Suppose $P$ is [[Irreducible Markov Chains|irreducible]] and [[period of states|aperiodic]] and suppose $P$ has an [[Invariant Distributions|invariant distribution]] $\pi$. Suppose $(X_{n})_{n\geq 0}$ is $Markov(\lambda,P)$, then for all $j\in I$,
$$
\lim_{ n \to \infty } \mathbb{P}(X_{n}=j)=\pi_{j}
$$
## Remark
In particular, take $\lambda=\delta_{i}$, then $P^{n}_{ij}\to \pi_{j}$ as $n\to \infty$ for all $i$
___
It is almost impossible to state how important this is. It's the key idea between the google search algorithm, the basis of Markov chain Monte Carlo methods and many other applications
## Example

___
Suppose $\mathbb{P}(X_{n}=H)=p \in(0,1)$ and where $Y_{n}$ is the number of heads amongst $X_{0},X_{1},\dots,X_{n}$. FInd
$$
\lim_{ n \to \infty } \mathbb{P}(X_{n}\text{ is a multple of }17)
$$
$(Y_{n})_{n\geq 0}$ is a Markov chain on $\mathbb{N}$. Let $Z_{n}=Y_{n}\mod 17$ 
We calim $(Z_{n})_{n\geq 0}$ is a Markov chain on $I=$
## Ergodic Theorem for Markov Chains
Suppose $(X_{n})_{n\geq 0}$ is $Markov(\lambda,P)$ and $P$ is irreducible, then
- $\mathbb{P}\left( \frac{1}{N}V_{i}(N)\to \frac{1}{\mathbb{E}_{i}(T_{i})} \text{ as }N\to \infty\right)=1$ where $V_{i}(N)$ is the number of visits to $i$ up to time $N$
- if in addition, $(X_{n})_{n\geq 0}$ is positive recurrent and $f:I\to \mathbb{R}$ is bounded, then
$$
\mathbb{P}\left( \frac{1}{N} \sum_{n=0}^{N-1}f(X_{n})\to \mathbb{E}_{\pi}(f)\text{ as }N\to \infty \right)=1
$$
### Proof
later
## Example
Consider the Markov chain with $X_{1}=A$ and 
$$
X_{n}=\begin{cases}
A & n\text{ even} \\
B & n\text{ odd}
\end{cases}
$$
Then $\mathbb{P}(X_{n}=A)$ doesn't converge to anything due to perioicity
But $V_{A}(N)$ which is the number of visits to $A$ up to time $N$, which is the number of even number less than or equal to $N, which is
$$
V_{A}(N)=\begin{cases}
\frac{N}{2}+1 & N\text{ even} \\
\frac{N}{2}+\frac{1}{2} & N\text{ odd}
\end{cases}
$$
$$
\implies \frac{1}{N} V_{A}(N)=\frac{1}{N}\begin{cases}
\frac{N}{2}+1 & N\text{ even} \\
\frac{N}{2}+\frac{1}{2} & N\text{ odd}
\end{cases} \to \frac{1}{2}=\pi_{A}
$$
## Interpreting Theorem
Take $(X_{n})_{n\geq 0}$ with 
$$
\mathbb{P}(X_{n}=H)=\mathbb{P}(X_{n}=T)=\frac{1}{2}
$$
This is a positive recurrent Markov chain on $\left\{ H,T \right\}$ with
$$
\mathbb{E}_{i}(T_{i})=\frac{1}{\pi_{i}}=2
$$
- Our theorem says that the fraction of time at $H$ tends to $\frac{1}{2}$ (by the strong law of large numbers) so we can think of the Ergodic theorem as the strong law of large numbers for Markov chains
- Suppose we earn £$\hspace{0pt}2$ for $H$ and lose £$\hspace{0pt}1$ for $T$, then the expected earnings divided by $N$ (by setting $f(H)=2,f(T)=-1$) $\mathbb{E}_{\pi}(f)=\frac{1}{2}f(H)+\frac{1}{2}f(T)=1-\frac{1}{2}=\frac{1}{2}$ as $N\to \infty$
## Example
A smuggler repeatedly sneaks goods through a border crossing. Each time, a corrupt border official refuses entry with probability $\frac{1}{2}$ and only resumes letting the smuggler through with probability $\sqrt{ x }$ if given a brible of £$1000x$ 
If each smuggled shipment earns £$\hspace{0pt}750$, how much should the smuggler spend on bribes to maximise profit?
![[Pasted image 20260316125044.png]]
This Markov chain is positive recurrent and irreducible if $x>0$, soo
$$
\frac{1}{N}\sum_{n=0}^{N-1}f(X_{n})\to \mathbb{E}_{\pi}(f)
$$
Where the first term is the average profit per attempt after $N$ smuggling runs, the last term is the equilibrium average profit
We recall that the stationary distribution for a two state Markov chain, thus
$$
\mathbb{E}_{\pi}(f)=750  \frac{\sqrt{ x }}{\frac{1}{2}+\sqrt{ x }}-1000x  \frac{\frac{1}{2}}{\frac{1}{2}+\sqrt{  x }}=\frac{1500\sqrt{ x }-1000x}{1+2\sqrt{ x }}
$$
So to maximie profit, we want to maximise this under the condition $x\geq 0$, this is a calculus exercise, taking the derivative,
$$
\frac{\left( 750x^{-\frac{1}{2}}-1000 \right)(1+2\sqrt{ x })-(1500\sqrt{ x }-1000x)x^{-\frac{1}{2}}}{(1+2\sqrt{ x })^{2}}
$$
Setting this to zero gives
$$
0=-1000\sqrt{ x }-1000+750x^{-\frac{1}{2}}
$$
Which gives
$$
4x+4\sqrt{ x }-3=0
$$
Which is a quadratic in $\sqrt{ x }$, so
$$
\sqrt{ x }=\frac{-1\pm 2}{2}=\frac{1}{2}
$$
(or $-\frac{3}{2}$ which we rule out)
So $x=\frac{1}{4}$
So we need to check $p$ at $x=0$ and $x\to \infty$ (as the enpoints)