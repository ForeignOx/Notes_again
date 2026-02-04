Let $A,B$ be two [[Events|events]] such that $\mathbb{P}(A)>0$, $\mathbb{P}(B)>0$, then:
$$
\mathbb{P}(A|B)=\frac{\mathbb{P}(B|A)\mathbb{P}(A)}{\mathbb{P}(B)}
$$
Or more generally if you have a thid event $C$ such that $\mathbb{P}(C)>0$, then
$$
\mathbb{P}( A|B\cap C) =\frac{\mathbb{P}(A|C)\mathbb{P}(B|A\cap C)}{\mathbb{P}(B|C)}
$$
The most general form is:
Let $A_{1},\dots A_{k}$ be a [[Set Partition|partition]] and, and let $B$ e an even with $\mathbb{P}(B)>0$, then:
$$
\mathbb{P}(A_{j}|B)=\frac{\mathbb{P}(A_{j})\mathbb{P}(B|A_{j})}{\sum_{ i=1} ^{ k} \mathbb{P}(B|A_{i})\mathbb{P}(A_{i}) }
$$
Which is obtained using the [[Partition Theorem|Partition Theorem]]
## Example
If it rains, Charlie the cat will go out with probability $\frac{1}{10}$, if it is dry, the probability will be $\frac{3}{5}$. If Charlie goes out, find the probability that it rains
Let
$$
R:=\{ \text{it rains} \}
$$
$$
 C:=\{ \text{Charlie goes out} \}
$$
$$
\mathbb{P}(R)=\frac{1}{2},\mathbb{P}(C|R)=\frac{1}{10}
$$
We want to find:
$$
\mathbb{P}(R|C)=\frac{\mathbb{P}(R)\mathbb{P}(C|R)}{\mathbb{P}(C)}=\frac{\mathbb{P}(R)\mathbb{P}(C|R)}{\mathbb{P}(C|R)\mathbb{P}(R)+\mathbb{P}(C|R^c)\mathbb{P}(R^c)}=\frac{\frac{1}{2}\times \frac{1}{10}}{\frac{1}{2}\times \frac{7}{10}}=\frac{1}{7}
$$



#Mathematics #Probability #Theorem 