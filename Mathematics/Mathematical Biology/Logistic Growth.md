## Example
Consider a population that has some self competition, so consider the greenflies from [[Exponential Growth#Example|this example]] so instead:
$$
\frac{d x}{dt} =ax\left( 1-\frac{x}{K} \right)
$$
Which is called the logistic equation with growth rate $a$ and carrying capacity $K$.
So we want for small $x$ it to not do anything, but as $x$ gets bigger, we want it to grow smaller. $K$ is usually the limiting thingy and is known as the carrying capacity 
Can we guess what this looks like? Without integrating just yet, we know that equilibrium is when $\frac{d x}{dt}=0$, so when $x=0$ and when $x=K$
We can also see when the population is increasing or decreasing, so if $x<K$, then $1-\frac{x}{K}>0$ for $x<K$, $1-\frac{x}{K}<0$ for $x>K$, so $x$ should approach $K$
Let's now solve it, it is clearly separable:
$$
\int \frac{1}{x\left( 1-\frac{x}{K} \right)} \, dx =\int a \, dt 
$$
$$
\implies \log(x)-\log\left( 1-\frac{x}{K} \right) =at+c 
$$
$$
\implies \frac{x}{1-\frac{x}{K}}=Ae^{ at }
$$
And note that $A$ is not $x(0)$ this time, so
$$
x= \frac{Ae^{ at }}{1+\frac{A}{K}e^{ at }}
$$
What is the long term behaviour?? It just goes to $K$, but also it has come from an equilibrium at $x=0$, if we make a small change to $x=K$ so going to $x=K-\varepsilon$, after some time you go back to $x=K$ so we call this stable
However if we make a small change to $x=0+\varepsilon$, in time it goes to $x=K$, so we call this unstable
Interestingly we don't need to actually solve to see this, we just need to plot $\frac{d x}{dt}$ against $x$, which is an upside-down parabola
```desmos-graph
K=3
y=x*(1-x/K)
```
