The partin theorem is also known as the law of total probability
Let $E_{1},E_{2},\dots$ be a [[Set Partition|partition]] or [[Sample Spaces|$\Omega$]], then for any [[Events|event]] $A$, we have:
$$
\mathbb{P}(A)=\sum_{ i=1} ^{ k}\mathbb{P}(E_{i})\mathbb{P}(A|E_{i})  
$$
More generally, if $\mathbb{P}(B)>0$,
$$
\mathbb{P}(A|B)=\sum_{i=1}^{k}\mathbb{P}(E_{i}|B)\mathbb{P}(A|E_{i}\cap B)
$$
## Proof
![[Partition Theorem 2024-10-25 14.15.24.excalidraw]]
Since $E_{i}$'s form a partition, $(A\cap E_{i})\cap(A\cap E_{j})=\emptyset$ for all $i\neq j$, so we can use the third axiom of probability to get:
$$
\mathbb{P}(A)=\sum_{ i=1} ^{ k} \mathbb{P}(A\cap E_{i}) 
$$
Using $\mathbb{P}(A\cap B)=\mathbb{P}(B)\mathbb{P}(A|B)$, we can get:
$$
\mathbb{P}(A)=\sum_{ i=1} ^{ k}\mathbb{P}(E_{i})\mathbb{P}(A|E_{i})  
$$
## Example
There are $\hspace{0pt}3$ machines $A$, $B$, and $C$, $10\%$ of the components produced by $A$ are faulty, $20\%$ of the components produced by $B$ are faulty, $30\%$ of the components produced by $C$ are faulty
Equal number of components are collected from each machine. One pomponent is selected at random. Find $\mathbb{P}(\text{component is faulty})$
Let $F:=\{ \text{the component is fauly} \}$, $M_{A}:=\{ \text{component comes from }A \}$, similarly define $M_{B},M_{C}$
$$
\mathbb{P}(M_{A})=\mathbb{P}(M_{B})=\mathbb{P}(M_{C})=\frac{1}{3}
$$
$$
\mathbb{P}(F|M_{A})=\frac{10}{100}, \mathbb{P}(F|M_{B})=\frac{20}{100}, \mathbb{P}(F|M_{C})=\frac{30}{100}
$$
By partition theorem:
$$
\mathbb{P}(F)=\mathbb{P}(M_{A})\mathbb{P}(F|M_{A})+\mathbb{P}(M_{B})\mathbb{P}(F|M_{B})+\mathbb{P}(M_{C})\mathbb{P}(F|M_{C})
$$
$$
= \frac{1}{3}\left( \frac{10+20+30}{100} \right)=0.2
$$
## Joint Distribution
$$
\mathbb{P}((X=x)|(Y=y))=p_{X}(x)=\sum_{y\in \Gamma}p_{y|x}(y|x)p_{X}(x)
$$
Let $X$ and $Y$ be jointly continuous, with pdf $f$, then:
$$
f_{X}(x)=\int_{-\infty}^{\infty} f_{X|Y}(x|y)f_{Y}(y) \, dx 
$$
## [[Expectation|Expectation]]
Let $E_{1},E_{2},\dots,E_{k}$ be a finite partition, then
$$
E(X)=\sum_{i=1}^{k}E(X|E_{i})\mathbb{P}(E_{i})
$$
If you have a countably infinite partition, $E_{1},E_{2},\dots$. then
$$
E(X)=\sum_{ i=1} ^{\infty}  E(X|E_{i})\mathbb{P}(E_{i})
$$
### Proof
Note that
$$
\Omega=\bigcup_{i=1}^{k}E_{i}
$$
And 
$$
\mathbb{1}_{\Omega}=\sum_{i=1}^{k}\mathbb{1}_{E_{i}}
$$
Only for disjoint sets, and
$$
E(X)=E(X\mathbb{1}_{\Omega})=E\left( X\sum_{i=1}^{k}\mathbb{1}_{E_{i}} \right)=E\left( \sum_{i=1}^{k}X\mathbb{1}E_{i} \right)=\sum_{i=1}^{k}E(X\mathbb{1}_{E_{i}})=\sum_{i=1}^{k}E(X|E_{i})\mathbb{P}(E_{i})
$$
___
Let $X$ and $Y$ be two random variables, then
$$
E(X)=E(E(X|Y))
$$
### Proof
Assume that $Y$ is discrete:
$$
E(X)=\sum_{y}\mathbb{P}(X|Y=y)\mathbb{P}(Y=y)
$$
As our partition is $\{ Y=y \}$, and using $g(y)=\mathbb{P}(X|Y=y)$
$$
=\sum_{y}g(y)\mathbb{P}(Y=y)=E(g(Y)=E(E(X|Y))
$$
### Example
Toss a coin $\hspace{0pt}3$ times, and let $H$ denote number of heads, then roll a fair dice $H$ times
Let $T$ be the total score, what is $E(T)$
Let $X_{1},X_{2},\dots$ denote the score of the $i$th throw of the die, so
$$
T=\sum_{i=1}^{H}X_{i}
$$
We know that
$$
H\sim \text{Bin}\left( 3,\frac{1}{2} \right)
$$
So
$$
E(T)=E(E(T|H))
$$
Observe that:
$$
E(X_{i})=\frac{1}{6}(1+2+\dots+6)=\frac{7}{2}
$$
Give $\{ H=h \}$, observe that
$$
E(T|H=h)=E\left( \sum_{i=1}^{h}X_{i} \right)=\sum_{i=1}^{h}E(X_{i})=\sum_{i=1}^{h} \frac{7h}{2}
$$
Substituting back, we get:
$$
E(T)=E\left( \frac{7H}{2} \right)=\frac{7}{2}E(H)
$$
$$
 E(H)=3\times \frac{1}{2}=\frac{3}{2}
$$
So
$$
E(T)=\frac{7}{2}\times \frac{3}{2}=\frac{21}{4}
$$



#Mathematics #Probability #Theorem  