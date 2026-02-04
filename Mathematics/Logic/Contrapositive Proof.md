The general technique:
Let $A$ and $B$ be [[Proposition|propositions]], the statement “If $A$, then $B$” is equivalent to “If not $B$ then not $A$”
We can see this from a truth table:

| $A$ | $B$ | $A\implies B$ | not $B$ | not $A$ | not $B\implies$ not $A$ |
| --- | --- | ------------- | ------- | ------- | ----------------------- |
| T   | T   | T             | F       | F       | T                       |
| T   | F   | F             | T       | F       | F                       |
| F   | T   | T             | F       | T       | T                       |
| F   | F   | T             | T       | T       | T                       |

## Example
If $n\in\mathbb{Z}$ is an even [[Integers|integer]], then $n^{2}$ is even, so $n=2k$, $k\in\mathbb{Z}$, so $n^{2}=(2k)^{2}=4k$ which is even
If $n^{2}\in\mathbb{Z}$, then $n$ is even we could try the same technique, $n^{2}=2k$, but then we are stuck
If $n$ is odd, then $n^{2}$ is odd, so $n=2k+1$, so $n^{2}=(2k+1)=4k^{2}+4k+1=2(2k^{2}+2k)+1$, so is odd
We can then return to our second statement, so for it to be false we need $n\in\mathbb{Z}$ such that $n^{2}$ is even and $n$ is odd, but because of our proof above, we see that this cannot be the case, so it is true

#Mathematics #Logic 