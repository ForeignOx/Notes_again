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
### Proof
We suppose that $(X_{n})_{n\geq 0}$ is $Markov(\lambda,P)$, and $(Y_{n})_{n\geq 0}$ is $Markov(\underline{\pi},P)$, and they are independent of each other. Taking $b\in I$, then the [[first passage time|first passage time]] of $(X_{n},Y_{n})$ to $(b,b)$ is 
$$
T=\min\left\{ n\geq 0:\middle|: X_{n}=Y_{n}=b \right\}
$$
We perform this proof in $\hspace{0pt}3$ steps:
1. Show that $\mathbb{P}(T<\infty)=1$,
2. Show that
$$
Z_{n}=\begin{cases}
X_{n} & n<T \\
Y_{n} & n\geq T
\end{cases}
$$
    Is $Markov(\lambda,P)$. This is the "switched" Markov chain
3. Argue that $\hspace{0pt}1$ and $\hspace{0pt}2$ imply our theorem
Step 1:
We define
$$
W_{n}:=(X_{n},Y_{n}),~n\geq 0
$$
We claim $(W_{n})_{n\geq 0}$ is $Markov(\mu,Q)$ on the state space $I\times I$, where
- $\mu_{(i,k)}=\lambda_{i}\pi_{k}$
- $Q_{(i,k)(j,\ell)}=P_{ij}P_{k\ell}$ ($X$ goes from $i$ to $j$, $Y$ goes from $k$ to $\ell$)
To prove this claim, we use independence to split the step of $X_{n}$ and of $Y_{n}$, use separately the Markov property for $X_{n}$ and $Y_{n}$, and use independence again to put them back together. We do this as follows:
$$
\mathbb{P}(W_{n}=(i_{n},k_{n})\mid W_{0}=(i_{0},k_{0}),\dots,W_{n-1}=(i_{n-1},k_{n-1})) 
$$
$$
= \frac{\mathbb{P}(X_{0}=i_{0},\dots,X_{n}=i_{n},Y_{0}=k_{0},\dots,Y_{n}=k_{n})}{\mathbb{P}(X_{0}=i_{0},\dots,X_{n-1}=i_{n-1},Y_{0}=k_{0},\dots,Y_{n-1}=k_{n-1})} 
$$
$$
=  \frac{\mathbb{P}(X_{0}=i_{0},\dots,X_{n}=i_{n})}{\mathbb{P}(X_{0}=i_{0},\dots,X_{n-1}=i_{n-1})} \frac{\mathbb{P}(Y_{0}=k_{0},\dots,Y_{n}=k_{n})}{\mathbb{P}(Y_{0}=k_{0},\dots,Y_{n-1}=k_{n-1})} 
$$
$$
= \mathbb{P}(X_{n}=i_{n}\mid X_{0}=i_{0},\dots X_{n-1}=i_{n-1})\mathbb{P}(Y_{n}=k_{n}\mid Y_{0}=k_{0},\dots Y_{n-1}=k_{n-1}) 
$$
$$
= \mathbb{P}(X_{n}=i_{n}\mid X_{n-1}=i_{n-1})\mathbb{P}(Y_{n}=k_{n}\mid Y_{n-1}=k_{n-1}) 
$$
$$
= \frac{\mathbb{P}(X_{n}=i_{n},X_{n-1}=i_{n-1})}{\mathbb{P}(X_{n-1}=i_{n-1})} \frac{\mathbb{P}(Y_{n}=k_{n},Y_{n-1}=k_{n-1})}{\mathbb{P}(Y_{n-1}=k_{n-1})}
$$
$$
= \frac{\mathbb{P}(X_{n}=i_{n},X_{n-1}=i_{n-1},Y_{n}=k_{n},Y_{n-1}=k_{n-1})}{\mathbb{P}(X_{n-1}=i_{n-1},Y_{n-1}=k_{n-1})} 
$$
$$
= \mathbb{P}(W_{n}=(i_{n},k_{n})\mid W_{n-1}=(i_{n-1},k_{n-1}))
$$
Next we claim that $Q$ is positive recurrent. To prove this, we need to show that:
 - $Q$ is irreducible on the state space $I\times I$
 - $Q$ has a stationary distribution
To show that $Q$ is irreducible, we recall the proposition that says that a state $i$ is aperiodic iff $P^{n}_{ii}>0$ for all sufficiently large $n$. Since $P$ is irreducible, for any $i,j\in I$, there exists $k>0$ such that $P^{k}_{ij}>0$. Therefore
$$
P_{ij}^{n}\geq P_{ii}^{n-k}P_{ij}^{k}>0
$$
For all $n$ large enough. Similarly, $P^{n}_{k\ell}>0$ for all $n$ large enough, hence,
$$
Q^{n}_{(i,k)(j,\ell)}=P_{ij}^{n}P_{k\ell}^{n}>0
$$
for all $n$ large enough, in particular, $Q$ is irreducible
Next to show that $Q$ has a stationary distribution, we define
$$
\psi((i,k)):=\pi(i)\pi(k)~(i,k)\in  I\times I
$$
We claim that $\psi$ is a stationary distribution for $Q$. We firstly check it's a distribution:
$$
\psi((i,k))=\pi(i)\pi(k)\geq 0
$$
for all $i,k\in I$
$$
\sum_{(i,k)\in  I\times I}\psi((i,k))=\sum_{i\in I}\sum_{k\in  I}\pi(i)\pi(k)=\underbrace{ \left( \sum_{i\in I}\pi(i) \right) }_{ =1 }\underbrace{ \left( \sum_{k\in  I}\pi(k) \right) }_{ =1 }=1
$$
Now to see that $\psi$ is stationary for $Q$, observe that
$$
(\psi Q)_{(j,\ell)}=\sum_{(i,k)\in  I\times I} \psi_{(i,k)}Q_{(i,k)(j,\ell)} 
$$
$$
= \sum_{(i,k)\in  I\times I} \pi(i)\pi(k)P_{ij}P_{k\ell} 
$$
$$
= \underbrace{ \left( \sum_{i\in I}\pi (i)P_{ij} \right) }_{ =\pi(j) }\underbrace{ \left( \sum_{k\in  I}\pi(k)P_{k\ell} \right) }_{ =\pi(\ell) }=\psi(j,\ell)
$$
We have now proven that $Q$ is irreducible and has a stationary distribution on the state space $I\times I$, hence it is positive recurrent
Recall that
$$
T:=\min\left\{ n\geq :\middle|: X_{n}=Y_{n}=b \right\}
$$
This is precisely the first passage time of $W_{n}$ to $(b,b)$. Since $Q$ is positive recurrent, we have
$$
\mathbb{P}(T<\infty)=\mathbb{P}(W_{n}=(b,b)\text{ for some }n<\infty)=1
$$
So we are done for step 1
Step 2:
We want to show that
$$
Z_{n}=\begin{cases}
X_{n} & n<T  \\
Y_{n} & n\geq T
\end{cases}
$$
Is $Markov(\lambda,P)$
We firstly observe that $Z_{0}=X_{0}$ (since $T\geq 1$ by definition), so $\mathbb{P}(Z_{0}=i)=\mathbb{P}(X_{0}=i)=\lambda(i)$ for all $i\in I$
The main task is to check that it's Markov with stochastic matrix $P$. We want to show:
$$
\mathbb{P}(Z_{n+1}=i_{n+1}\mid Z_{0}=i_{0},\dots,Z_{n}=i_{n},T=k)=P_{i_{n}i_{n+1}}\text{ for }1\leq k\leq n
$$
$$
\mathbb{P}(Z_{n+1}=i_{n+1}\mid Z_{0}=i_{0},\dots,Z_{n}=i_{n},T>n)=P_{i_{n}i_{n+1}}
$$
The idea is to use the strong Markov property
Since $(W_{n})_{n\geq 0}$ is $Markov(\mu,Q)$ and $T$ is an (almost surely finite) stopping time (as it's a hitting time) with $W_{T}=(b,b)$, the strong Markov property implies that $(W_{T+n})_{n\geq 0}$ is $Markov(\delta_{(b,b)},Q))$, and independent of $W_{0},W_{1},\dots,W_{T}$
Then since $X_{n}$ is the first coordinate of $W_{n}$ and $Y_{n}$ the second coodinate, we have
$$
\mathbb{P}(Z_{n+1}=i_{n+1}\mid X_{0}=i_{0},\dots,Z_{n}=i_{n},T=k) 
$$
$$
= \mathbb{P}(Y_{T+n-k+1}=i_{n+1}\mid X_{0}=i_{0},\dots,X_{k}=i_{k},T=k,Y_{T+1}=i_{k+1},\dots,Y_{T+n-k}=i_{n}) 
$$
$$
= \frac{\mathbb{P}(Y_{T+n-k+1}=i_{n+1},X_{0}=i_{0},\dots,X_{k}=i_{k},T=k,Y_{T+1}=i_{k+1},..,Y_{T+n-k}=i_{n})}{\mathbb{P}(X_{0}=i_{0},\dots ,X_{k}=i_{k},T=k,Y_{T+1}=i_{k+1},\dots,Y_{T+n-k}=i_{n})} 
$$
$$
= \frac{\mathbb{P}(Y_{T+n-k+1}=i_{n+1},Y_{T+1}=i_{k+1},\dots,Y_{T+n-k}=i_{n})}{\mathbb{P}(Y_{T+1}=i_{k+1},\dots,Y_{T+n-k}=i_{n})} \cancelto{ 1 }{ \frac{\mathbb{P}(X_{0}=i_{0},\dots,X_{k}=i_{k})}{\mathbb{P}(X_{0}=i_{0},\dots,X_{k}=i_{k})} 
 } 
$$
$$
= \mathbb{P}(Y_{T+n-k+1}=i_{n+1}\mid Y_{T+1}=i_{k+1},\dots,Y_{T+n-k}=i_{n})
 $$
 Since $(W_{T+n})_{n\geq 0}$ is $Markov(\delta_{(b,b)},P)$, the two coordinates of $(W_{T+n})_{n\geq 0}$ are independent $Markov(\delta_{b},P)$
 The second coordinate is precisely $(Y_{T+n})_{n\geq 0}$, hence
 $$
\mathbb{P}(Y_{T+n-k+1}=i_{n+1}\mid Y_{T+1}=i_{k+1},\dots,Y_{T+n-k}=i_{n})=P_{i_{n}i_{n+1}} 
$$
$$
\implies \mathbb{P}(Z_{n+1}=i_{n+1}\mid Z_{0}-i_{0},\dots,Z_{n}=i_{n},T=k)=P_{i_{n}i_{n+1}}
$$
For all $1\leq k\leq n$
On the other hand
$$
\mathbb{P}(Z_{n+1}=i_{n+1}\mid Z_{0}=i_{0},\dots,Z_{n}=i_{n},T>n) 
$$
$$
 =\mathbb{P}(Z_{n+1}=i_{n+1}\mid X_{0}=i_{0},\dots,X_{n}=i_{n},T>n) 
$$
$$
= \mathbb{P}(X_{n+1}=i_{n+1}\mid X_{0}=i_{0},\dots,X_{n}=i_{n},T>n) 
$$
$$
= \mathbb{P}(X_{n+1}=i_{n+1}\mid X_{0}=i_{0},X_{1}=i_{1}\neq Y_{1},X_{2}=i_{2}\neq Y_{2},\dots,X_{n}=i_{n}\neq Y_{n})  
$$
$$
= \mathbb{P}(X_{n+1}=i_{n+1}\mid X_{0}=i_{0},X_{1}=i_{1},\dots,X_{n}=i_{n})=P_{i_{n}i_{n+1}}
$$
By the Markov property for $X_{n}$
We now calculate
$$
\mathbb{P}(Z_{n+1}=i_{n+1}\mid Z_{0}=i_{0},\dots,Z_{n}=i_{n}) 
$$
$$
= \sum_{k=1}^{n}\mathbb{P}(Z_{n+1}=i_{n+1},T=k\mid Z_{0}=i_{0},\dots,Z_{n}=i_{n})
$$
$$
 +\mathbb{P}(Z_{n+1}=i_{n+1},T>n\mid Z_{0}=i_{0},\dots,Z_{n}=i_{n})  
$$
$$
= \sum_{k=1}^{n}\mathbb{P}(Z_{n+1}=i_{n+1}\mid Z_{0}=i_{0},\dots,Z_{n}=i_{n},T=k)\mathbb{P}(T=k\mid Z_{0}=i_{0},\dots,Z_{n}=i_{n}) 
$$
$$
 +\mathbb{P}(Z_{n+1}=i_{n+1} \mid Z_{0}=i_{0},\dots,Z_{n}=i_{n},T>n)\mathbb{P}(T>n\mid Z_{0}=i_{0},\dots,Z_{n}=i_{n}) 
$$
$$
= \sum_{k=1}^{n} P_{i_{n}i_{n+1}} \mathbb{P}(T=k\mid Z_{0}=i_{0},\dots,Z_{n}=i_{n})+P_{i_{n}i_{n+1}}\mathbb{P}(T>n\mid Z_{0}=i_{0},\dots,Z_{n}=i_{n}) 
$$
$$
= P_{i_{n}i_{n+1}}\left( \sum_{k=1}^{n} \mathbb{P}(T=k\mid Z_{0}=i_{0},\dots,Z_{n}=i_{n})+\mathbb{P}(T>n\mid Z_{0}=i_{0},\dots,Z_{n}=i_{n}) \right) 
$$
$$
= P_{i_{n}i_{n+1}} \mathbb{P}(\left\{ T\leq n \right\}\cup \left\{ T>n \right\}\mid Z_{0}=i_{0},\dots,Z_{n}=i_{n})
$$



Step 3:
We have
$$
\mathbb{P}(Z_{n}=j)=\mathbb{P}(Z_{n}=j,T>n)+\mathbb{P}(Z_{n}=j,T\leq n) 
$$
$$
 = \mathbb{P}(X_{n}=j,T>n)+\mathbb{P}(Y_{n}=j,T\leq n)
$$
Then since $\pi$ is stationary,
$$
\left| \mathbb{P}(Z_{n}=j)-\pi(j) \right| =\left| \mathbb{P}(Z_{n}=j)-\mathbb{P}(Y_{n}=j) \right|  
$$
$$
= \left| \mathbb{P}(Z_{n}=j,T>n)+\mathbb{P}(Z_{n}=j,T\leq n)-\mathbb{P}(Y_{n}=j,T>n) -\mathbb{P}(Y_{n}=j,T\leq n) \right|  
$$
$$
= \left| \mathbb{P}(Z_{n}=j,T>n)-\mathbb{P}(Y_{n}=j,T>n) \right| 
$$
$$
\leq \mathbb{P}(Z_{n}=j,T>n)-\mathbb{P}(Y_{n}=j,T>n)
$$
$$
 \leq 2\mathbb{P}(T>n)\to 0\text{ as }n\to\infty
$$
By step $\hspace{0pt}1$, to see that step $\hspace{0pt}1$ implies that $\mathbb{P}(T>n)\to 0$, we see that
$$
\lim_{ n \to \infty } \mathbb{P}(T>n )=\lim_{ n \to \infty } \mathbb{P}\left( \bigcap_{k=0}^{n}\left\{ T>n \right\} \right)=\mathbb{P}(T=\infty)=0
$$
And we are done!
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
So we need to check $p$ at $x=0$ and $x\to \infty$ (as the endpoints) ehhhh
## Example
Describing the flux of neutrons in a nuclear rector is offundamental importance for safely and effectively controlling nuclear reactors. However, the neutron flux solves a 6-dimensional PDE, which is very hard to solve accurately and efficiently
Fortunately, the neutron flux can be described as the stationary distribution of a Markov chain describing how a single neutron moves
By running this Markov chain and sampling the ergodic averages, we get a better description of the neutron flux, and better descriptions of how we should control the reactor