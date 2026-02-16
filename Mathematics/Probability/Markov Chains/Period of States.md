## Definition
The period of a state $i$ of a [[Markov Chains|Markov chain]] is defined as
$$
period(i):= \gcd(\left\{ n:\middle|: P_{ii}^{n}>0 \right\})
$$
If $\left\{ n:\middle|:P_{ii}^{n} \right\}=\left\{ 0 \right\}$ (i.e. we immediately leave $i$ and never return), then we define $period(i):=\infty$
Period is a [[Class Properties|class property]]
___
A state $i$ is called aperiodic if $period(i)=1$
## Theorem
If $i$ and $j$ belong to the same communicating class, then $period(i)=period(j)$
## Corollary
Suppose that $P$ is the transition matrix for an [[Irreducible Markov Chains|irreducible]] Markov chain and that $i$ i aperiodic. Then all $j\in I$ are aperiodic
## Proposition
A state $i$ is aperiodic iff $P_{ii}^{n}>0$ for all sufficiently large $n$
___
These are essentially facts about number theory. 
In light of this, a Markov chain will be called aperiodic if all states are aperiodic, so an irreducible and aperiodic Markov chain is a chain which is irreducible and has at least one aperiodic states
## Example
Consider the following 4-cycle and 3-cycle:
![[Pasted image 20260216212626.png]]
For the 4-cycle,
$$
\left\{ n:\middle|: P^{n}_{AA}>0 \right\}=2\mathbb{N}_{0}=\left\{ 0,2,4,\dots \right\}
$$
Has greatest common divisor $2$
For the 3-cycle:
$$
\left\{ n:\middle|: \right\}
$$