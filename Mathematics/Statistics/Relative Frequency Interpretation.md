This is an interpretation of the [[Equally Likely Outcomes|equally likely outcomes]] model in probability that makes it more useful in real life applications. This interpretation applies to trials giving chance outcomes of an experiment that can be repeated indefinitely under essentially unchanged conditions and which exhibits long term regularity. Suppose that we run $n$ trials of an experiment with a known list of possible outcomes and the umber of trials on which event $A$ occurs is $n_{A}$ ($A$ is again a [[Sets|set]] of possible [[Outcomes|outcomes]]), the relative frequency of occurrence of $A$ is $\frac{n_{A}}{n}$
As a mathematical idealization, we suppose that there is a unique, empirical limiting value for $\frac{n_{A}}{n}$, as $n$ tends to infinity, which we call the relative frequency [[Probabilities|probability]] of $A$:
$$
\mathbb{P}(A)=\lim_{ n \to \infty } \frac{n_{A}}{n}
$$
## Example
Suppose we toss a coin $1000$ times and observe $\hspace{0pt}490$ heads, then the relative frequency of heads is $\frac{490}{1000}$, for some experiments, it may be reasonable to suppose that relative frequencies are stable for very large $n$
For example if we toss a fair coin one billion times, we might expect that the relative frequency of heads after the first few thousand throws would remain very close to $\frac{1}{2}$
For our coin, the statement $\mathbb{P}(\text{heads})=\frac{1}{2}$ means 'if we tossed the poin an extremely large number of times, then the proportion of heads would be arbitrarily close to $\frac{1}{2}$'
___
This interpretation is widely used, epecially in physics, where experiments are designed for repeatability, and we can expect future trials to behave like those in the past. In this view, probability is a property of the experimental setup and may be 'objectively' discovered by sufficient repetitions of the experiment
Amonst the problems with this interpretation are: it is often impossible to decide what "essentially unchanged contditions" are; we often have no way of knowing when limiting frequencies become stable; we can only use it in situations that are repeatable. For example when you throw a die, there is no way of throwing it in exactly the same way, there will be very small changes to the enviromnent, so there is in fact no real repeatable experiment. There are machines that can come very close, but these aren't very helpful, for example you can have a machine that tosses a coin and gets heads every time, so to make this a repeatable experiment, you have to introduce some initial conditions to how it is tossed, and so this has to follow some distribution. This is what we mean by repeatable experiment, which is very flawed...


#Mathematics #Statistics 