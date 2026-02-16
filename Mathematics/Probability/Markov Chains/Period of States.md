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
