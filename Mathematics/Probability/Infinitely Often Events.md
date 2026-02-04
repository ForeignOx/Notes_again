## Definition
Given a [[Probabilities|probability]] [[Probability Spaces|space]] $(\Omega,\mathfrak{F},\mathbb{P})$, let $A_{n},n\geq 1$ be a [[Sequences|sequence]] of [[Events|events]], we define the event $\left\{ A_{n}\text{ infinitely often} \right\}$
Informally, this event contains all $\omega \in\Omega$ such that $\omega \in A_{n}$ for infinitely many values of $n$
Formally,
$$
\left\{ A_{n}\text{ infinitely often} \right\}=\bigcap_{n=1}^{\infty}\left( \bigcup_{k=n}^{\infty}A_{k} \right)
$$
$$
= \left\{ \omega \in \Omega:\middle|: \forall n\geq 1 \exists k\geq n:\omega \in A_{k} \right\}
$$
$$
= \left\{ \omega \in \Omega:\middle|:\omega \in A_{n}\text{ for infinitely many }n\geq 1 \right\}
$$
A separate notation is
$$
\limsup_{n\to \infty}A_{n}\equiv \left\{ A_{n}\text{ infinitely often} \right\}
$$
## Proposition
We claim that $\omega \in\left\{ A_{n}\text{ infinitely often} \right\}$ iff there is an infinite sequence $n_{1}<n_{2}<\dots$ such that $\omega \in A_{n_{k}}$ for every $k$
### Proof
Suppose 
$$
\omega \in \bigcap_{n=1}^{\infty}\left( \bigcup_{n=1}^{\infty}A_{k} \right)
$$
For $n=1$, 
$$
\omega \in  \bigcup_{n=1}^{\infty}A_{k}\implies \omega \in A_{n_{1}} \text{ for some }n\geq 1
$$
Take $n=n_{1}+1$, then
$$
\omega \in \bigcup_{k=n_{1}+1}^{\infty}A_{k}\implies \omega \in A_{n_{2}}\text{ with }k=n_{2}\geq n_{1}+1>n_{1}
$$
Take $n=n_{2}+1$, 
$$
\omega \in \bigcup_{k=n_{2}+1}^{\infty}A_{k}\implies \omega \in A_{n_{3}}

$$
$$
\vdots
$$
By induction, this is shown
___
## Remark
Notice that for each $n\geq 1$
$$
B_{n}:= \bigcup_{k=n}^{\infty}A_{k}=\left\{ \omega \in \Omega:\middle|:\omega \in A_{k}\text{ for at least one }k\geq n \right\}
$$
Is an event satisfying $B_{n}=A_{n}\cup B_{n+1}\supseteq B_{n+1}$ so that $(B_{n})_{n\in\mathbb{N}}$ forms a [[Monotone Events|decreasing]] sequence of events, therefore
$$
\left\{ A_{n}\text{ infinitely often} \right\}=\bigcap_{n=1}^{\infty}B_{n}
$$
Is a monotone [[Infinite Sequences of Independent Random Variables|limit of events]] whose probability can be computed from $\mathbb{P}(B_{n})$ by continuity
## Finitely Often Events
Taking the complement of our definition, we get:
$$
\left\{ A_{n}\text{ finitely often} \right\}=\left\{ A_{n}\text{ infinitely often} \right\}^{c}=\bigcup_{n\geq 1}\bigcap_{k\geq n}A_{k}^{c}
$$
Or, in the extended form:
$$
\left\{ A_{n}\text{ finitely often} \right\}=\bigcup_{n=1}^{\infty}\bigcap_{k=n}^{\infty}A_{k}^{c}=\left\{ \omega \in \Omega:\middle|: \exists n\geq 1:\omega \not\in A_{k} \forall k\geq n \right\}
$$
## Example
Let $X$ be a positve random variable with $\mathbb{P}(X<\infty)=1$. For $n\geq 1$, denote $X_{n}= \frac{1}{n}X$ and, for $\varepsilon>0$ let 
$$
A_{n}(\varepsilon)=\left\{ \omega \in \Omega:\middle|: \left| X_{n}(\omega) \right| >\varepsilon \right\}\equiv \left\{ \left| X \right| >n\varepsilon \right\}
$$
We obviously have $A_{n}(\varepsilon)\supseteq A_{n+1}(\varepsilon)$ for fixed $\varepsilon>0$ and all $n\geq 1$, therefore
$$
\bigcap_{n=1}^{\infty}A_{n}(\varepsilon)=\lim_{ n \to \infty } A_{n}(\varepsilon)\equiv \left\{ X=\infty \right\}
$$
Which has [[Probabilities|probability]] zero by the assumption that $\mathbb{P}(X<\infty)=1$. On the other han, since $A_{n}(\varepsilon)$ is a decreasing sequence, the event
$$
\left\{ A_{n}\text{ infinitely often} \right\}=\bigcap_{m=1}^{\infty}\bigcup_{n=m}^{\infty}A_{n}(\varepsilon)\equiv \bigcap_{m=1}^{\infty}A_{m}(\varepsilon)=\left\{ X=\infty \right\}
$$
Has probability zero. By taking the complement, we conclude that $\left\{ A_{n}(\varepsilon) \text{ finitely often}\right\}\equiv \left\{ X<\infty \right\}$ for each $\varepsilon>0$
