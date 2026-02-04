Let $A,B,C$ be $\hspace{0pt}3$ [[Events|events]] such that $\mathbb{P}(A\cap B\cap C)>0$, then the following are equivalent:
$$
\mathbb{P}(A\cap B|C)=\mathbb{P}(A|C)\mathbb{P}(B|C)
$$
$$
 \mathbb{P}(A|B\cap C)=\mathbb{P}(A|C)
$$
$$
 \mathbb{P}(B|A\cap B)=\mathbb{P}(B|C)
$$
We say A and $B$ are conditionally [[Independence|independent]] given $C$
The equivalence can be understood as, if we know $C$, then learning about $B$ will not tell us anything new about $A$, and similarly, if we know $C$, then learning about $A$ will not tell us anything new about $B$
## Multiple Events
A collection of events $\mathcal{A}\in\mathfrak{F}$, are mutually conditionally independent if given another event $B$ if for every finite non-empty subcollection $\mathcal{C}\subseteq \mathcal{A}$,
$$
\mathbb{P}\left( \bigcap_{A\in \mathcal{C}}A\mid B \right)=\prod_{A\in \mathcal{C}}\mathbb{P}(A|B)
$$


#Mathematics #Probability 