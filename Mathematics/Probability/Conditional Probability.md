Let $A,B\in\Omega$ be two [[Events|events]]. We define the conditional probability of $A$ given $B$, and denote it by $\mathbb{P}(A|B)$, as follows:
$$
\mathbb{P}(A|B):=\frac{\mathbb{P}(A\cap B)}{\mathbb{P}(B)}
$$
When $\mathbb{P}(B)>0$
Another way of thinking about this is to find the probability of $A$ whan we have observed $B$
Note we have only defined it as a probability, $A|B$ does not have a definition
## Examples
Roll of the die:
$$
A=\{ \text{score is odd} \}=\{ 1,3,5 \}
$$
$$
B=\{ \text{score is less than 4} \}=\{ 1,2,3 \}
$$
$$
\mathbb{P}(A|B)=\frac{\mathbb{P}(A\cap B)}{\mathbb{P}(B)}
$$
$$
A\cap B=\{ 1,3 \},|A|=2
$$
$$
\implies \mathbb{P}(A\cap B)=\frac{2}{6}=\frac{1}{3}
$$
$$
\mathbb{P}(B)=\frac{3}{6}=\frac{1}{2}
$$
$$
\therefore \mathbb{P}(A|B)=\frac{\frac{1}{3}}{\frac{1}{2}}=\frac{2}{3}
$$
A family has two children, both sexes are eqully likely:
$$
\Omega=\{ BB,BG,GB,GG \}
$$
Where the first element represents the sex of the first child, and the second, the sex of the younger child
Consider the following events:
$$
A_{1}:=\{ \text{both girls} \}=\{ GG \},\mathbb{P}(A_{1})=\frac{1}{4}
$$
$$
A_{2}:=\{ \text{at least one girl} \}=\{ BG,GB,GG \},\mathbb{P}(A_{2})=\frac{3}{4}
$$
$$
 A_{3}:=\{ \text{elder is a girl} \}=\{ GB,GG \},\mathbb{P}(A_{3})=\frac{1}{2}
$$
Note that:
$$
\mathbb{P}(A_{1}|A_{2})=\frac{\mathbb{P}(A_{1}\cap A_{2})}{\mathbb{P}(A_{2})}
$$
And $A_{1}\subseteq A_{2}\implies A_{1}\cap A_{2}=A_{1}$, so $\mathbb{P}(A_{1}|A_{2})=\frac{\mathbb{P}(A_{1})}{\mathbb{P}(A_{2})}=\frac{1}{3}$
Consider $\mathbb{P}(A_{2}|A_{1})$l:
$$
\mathbb{P}(A_{2}|A_{1})=\frac{\mathbb{P}\left( A_{1}\cap A_{2} \right)}{\mathbb{P}(A_{1}}= \frac{\mathbb{P}(A_{1})}{\mathbb{P}(A_{1})}=1
$$
## Properties of Conditional Probability
- Let $B$ be an event, such that $\mathbb{P}(B)>0$, then $\mathbb{P}(\cdot|B)$ (the $\cdot$ represents any set) satisfies the axioms of [[Probabilities|probability]]
    Given the event $B$, let us define:
$$
\mathbb{P}_{B}:\mathfrak{F}\to \mathbb{R}:\forall A\in \mathfrak{F},\mathbb{P}_{B}(A):=\mathbb{P}(A|B)
$$
    So $\mathbb{P}_{B}$ is a probability on $(\Omega,\mathfrak{F})$, so satisfies the axioms of probability:
    - $\mathbb{P}_{B}(A)\geq 0$
    - $\mathbb{P}_{B}(\Omega)=1$
    - $\mathbb{P}_{B}(A_{1} \cup A_{2})=\mathbb{P}_{B}(A_{1})+\mathbb{P}_{B}(A_{2})$ if $A_{1}\cap A_{2}=\emptyset$
### Proof
$$
\mathbb{P}_{B}(A)=\frac{\mathbb{P}(A\cap B)}{\mathbb{P}(B)}
$$
And since $\mathbb{P}(A\cap B)$ and $\mathbb{P}(B)$ are both probabilities, so by the first axiom, are both positive, so $\mathbb{P}_{B}(A)\geq 0$
Since $\mathbb{P}(B\cap\Omega)=\mathbb{P}(B)$,
$$
\mathbb{P}_{B}(\Omega)=\frac{\mathbb{P}(B\cap\Omega)}{\mathbb{P}(B)}=\frac{\mathbb{P}(B)}{\mathbb{P}(B)}=1
$$
$$
\mathbb{P}_{B}(A_{1}\cup A_{2})= \frac{\mathbb{P}((A_{1}\cup A_{2})\cap B)}{\mathbb{P}(B)}
$$
Since $A_{1}\cap A_{2}=\emptyset$, $(A_{1}\cap B)\cap (A_{2}\cap B)=\emptyset$, therefore we have:
$$
(A_{1}\cup A_{2})\cap B=(A_{1}\cap B)\cup (A_{2}\cap B)
$$
So:
$$
\mathbb{P}((A_{1}\cup A_{2})\cap B)=\mathbb{P}((A_{1}\cap B)\cup (A_{2}\cap B))=\mathbb{P}(A_{1}\cap B)+\mathbb{P}(A_{2}\cap B)
$$
Since $(A_{1}\cap B)$ and $(A_{2}\cap B)$ are mutually exclusive, so substituting this, we get:
$$
\mathbb{P}_{B}(A_{1}\cup A_{2})=\frac{\mathbb{P}(A_{1}\cap B)+\mathbb{P}(A_{2}\cap B)}{\mathbb{P}(B)}=\frac{\mathbb{P}(A_{1}\cap B)}{\mathbb{P}(B)}+\frac{\mathbb{P}(A_{2}\cap B)}{\mathbb{P}(B)}=\mathbb{P}_{B}(A_{1})+\mathbb{P}_{B}(A_{2})
$$
Which is what we want
___
- Since it satisfies the axioms, it must also satisfy the consequences:
    - $\mathbb{P}(A^{c}|B)=1=\mathbb{P}(A|B)$
    - If $A_{1}\subseteq A_{2}$, $\mathbb{P}(A_{1}|B)\leq \mathbb{P}(A_{2}|B)$
    - $\mathbb{P}(A_{1}\cup A_{2}|B)=\mathbb{P}(A_{1}|B)+\mathbb{P}(A_{2}|B)-\mathbb{P}(A_{1}\cap A_{2}|B)$
    - If $A_{1},A_{2},\dots$ are pairwise disjoint, then:
$$
\mathbb{P}\left( \bigcup_{i=1}^{n}A_{i}|B \right)=\sum_{i=1}^{n}\mathbb{P}(A_{i}|B)
$$
- The multiplication rule: for any $\hspace{0pt}2$ events $A,B\in\mathfrak{F}$, with $\mathbb{P}(A)\neq 0$, $\mathbb{P}(B)\neq 0$, we have, by rearranging the definition:
$$
\mathbb{P}(A\cap B)=\mathbb{P}(A|B)\mathbb{P}(B)=\mathbb{P}(B|A)\mathbb{P}(A)
$$
    A more general statement is also true:
$$
\mathbb{P}(A\cap B|C)=\mathbb{P}(B|C)\mathbb{P}(A|B\cap C),\text{ if }\mathbb{P}(B\cap C)>0
$$
Since:
$$
\mathbb{P}(B|C)\mathbb{P}(A|B\cap C)=\frac{\mathbb{P}(B\cap C)}{\mathbb{P}(C)} \frac{\mathbb{P}(A\cap B\cap C)}{\mathbb{P}(B\cap C)}=\frac{\mathbb{P}(A\cap B\cap C)}{\mathbb{P}(C)}=\mathbb{P}(A\cap B|C)
$$

It is enough to assume that $\mathbb{P}(B\cap C)>0$ because $B\cap C\subseteq C$, so $0<\mathbb{P}(B\cap C)\leq \mathbb{P}(C)$, therefore $\mathbb{P}(C)>0$ and hence we can define conditional probability of events given $C$
- General multiplication rule: Let $A_{0},A_{1},A_{2},\dots$ be events such that:
$$
\mathbb{P}\left(\bigcap_{i=1}^{k}A_{i}\right)>0
$$
    Then:
$$
\mathbb{P}\left( \bigcap_{i=0}^{k}A_{i}|A_{0} \right)=\mathbb{P}(A_{1}|A_{0})\mathbb{P}(A_{2}|A_{1}\cap A_{0})\mathbb{P}(A_{3}|A_{2}\cap A_{1}\cap A_{0})\dots \mathbb{P}\left( A_{k-1}|\bigcap_{i=0}^{k-2}A_{i} \right)\mathbb{P}\left( A_{k}|\bigcap_{i=1}^{k-1}A_{i} \right)
$$
___
## Multivariate Distributions#
### Discrete
$$
\mathbb{P}(A|B)=\frac{\mathbb{P}(A\cap B)}{\mathbb{P}(B)}
$$
When $\mathbb{P}(B)>0$, this is applicable to $\hspace{0pt}2$ random varibales, $X$ and $Y$, the conditional probability of $X$ given $Y=y$ is defined as:
$$
p_{X|Y}(x|y)=\frac{p_{(X,Y)}(x,y)}{p_{Y}(y)}=\mathbb{P}(X=x|Y=y)
$$
Where $p_{Y}(y)>0$
Similarly:
$$
p_{Y|X}(y|x)=\frac{p(x,y)}{p_{X}(x)}=\mathbb{P}(Y=y|X=x)
$$
### Continuous
Let $X$ and $Y$ be joint continuous with joint pdf $f(x,y)$, then the conditional pdf of $X$ given $Y=y$ is given by:
$$
f_{X|Y}(x|y)=\frac{f(x,y)}{f_{Y}(y)}
$$
Derivation:
$$
\mathbb{P}(X|Y)=\mathbb{P}(X \in [x,x+dx]|Y \in [y,y+dy])=\frac{\mathbb{P}(X \in [x,x+dx]\cap Y\in [y,y+dy])}{\mathbb{P}(Y\in [y,dy])}
$$
$$
 \approx \frac{f(x,y)dxdy}{f_{Y}(y)dy}\approx \frac{f(x,y)}{f_{Y}(y)}
$$
When $f_{Y}(y)>0$, and similarly the conditional pdf of $Y$ given $X=x$ is:
$$
f_{Y|X}(y|x)=\frac{f(x,y)}{f_{X}(x)}
$$




#Mathematics #Probability #Definition 