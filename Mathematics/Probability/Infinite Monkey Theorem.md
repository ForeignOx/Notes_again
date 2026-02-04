By the [[Borel-Cantelli Lemma|Borel-Cantelli lemma]], a monkey hitting keys at random on a typewriter keyboard for an infinite anount of time will almost surely (with [[Probabilities|probability]] one) type any particular chosen text, such as the complete works of William shakespeare or the equation for the theory of everything, in fact, infinitely many copies of any one of these texts.
## Idea of Argument
Suppose that the typewriter has $\hspace{0pt}50$ keys, and the word typed is "banana". The chance that the first letter typed is $b$ is $\frac{1}{50}$, as is the chance that the second letter is $a$, and so on. These events are independent, so the chance of the first $\hspace{0pt}6$ letters matching "banana" is $\frac{1}{50^{6}}$
For the same reason the chance that the next six letters match "banana" is also $\frac{1}{50^{6}}$ and so on
Now the chance of not typing banana in each block of six letters is $1-\frac{1}{50^{6}}$. Because each block is typed independently, the chance of not typing banana in any of the first $n$ blocks of $\hspace{0pt}6$ letters is $p=\left( 1-\frac{1}{50}^{6} \right)^{n}$ 
If we were to count occurences of banana that crossed blocks, $p$ would approach zero more quickly
Finally, once the first copy of the word banana appears, the process starts afresh independentlly of the past, so that the probability of obtaining the second copy of the word banan in the same number of blocks is still $p$
Then by the Borel-Cantelli lemma, the probability of this occurring infinitely often is 1
## Remark
By using an appropriate monotone approximation, one can deduce the result without the Borel-Cantelli lemma. Moreover, the same argument can be extended to the situations, when the probability $p_{n}$ of typing vanana in the $n$th block of six letters varies with $n$, but remains uniformly positive, i.e. $p_{n}\geq\delta>0$ for all $n\geq 1$. The true power of the lemma is seen in the situations when $p_{n}\to 0$ slowly enough to have $\sum_{n=0}^{\infty}p_{n}=\infty$ (provided the events in different blocks are independent)

