If a procedure can be broken down into first and second stages, and if there are $m$ possible outcomes for the first stage and if, for each of these outcomes, there are $n$ possible outcomes for the second stage, then the total procedure can be carried out, in the designated order, in $mn$ ways
This is also referred to as the principle of choice or the multiplication principle
Note that the rule can be extended to more than two stages
If for $1\leq i\leq k$ there are $n_{i}$ choices for the $i$th item in a [[Arrangements old|list]] regardless of previous choices, then the number of possible lists is $n_{1\times}n_{2}\times\dots \times n_{k}$
## Examples
A label identifier for a computer system consists of one letter (A-Z) followed by $\hspace{0pt}3$ digits (0-9). How many distinct identifiers are possible
a) if repetitions are allowed
b) if repetitions are not allowed
### Solution
a)
![[Multiplication Principle 2024-10-15 15.36.49.excalidraw]]
so the answer would be $26\times 10\times 10\times 10=26000$
b)
![[Multiplication Principle 2024-10-15 15.37.51.excalidraw]]
so the answer would be $26\times 10\times 9\times 8$
___
Debit card pins have $\hspace{0pt}4$ places, each can hold a number from $0,1,\dots,9$ with the following restrictions: they cannot have the same digit in all $\hspace{0pt}4$ places and they cannot be an increasing or decreasing sequence of consecutive numbers
Counting all the possible pins would be a very long process, but counting all the ones that aren't allowed would greatly increase the speed of the process as the [[Cardinality of Sets|cardinality]] of the set of impossible pins is much smaller and using this we can work out the total number of pins as:
$$
|A^{c}|=|\Omega|-|A|
$$
The number of sequences satisfying the first issue is $\hspace{0pt}10$, as all the sequences are $[1,1,1,1],[2,2,2,2],\dots,[9,9,9,9]$
For the second issue the increasing sequences can start with any number from $0,1,2,\dots,6$ which gives $\hspace{0pt}7$ options, and there will be the same number of decreasing sequences by reflection, so $\hspace{0pt}14$ total, so the number of possible pins overall will be $10^4-24$

#Mathematics #Discrete 