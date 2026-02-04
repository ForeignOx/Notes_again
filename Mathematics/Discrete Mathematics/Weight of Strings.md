Consider a [[Strings|string]] $x$ with digits $x=x_{1}x_{2}x_{3}\dots x_{n}$, we define the weight of $x$, denoted by $\text{wt}(x)$ as:
$$
\text{wt}(x)=x_{1}+x_{2}+x_{3}+\dots+x_{n}
$$
For example, $\text{wt}(12)=3$, $\text{wt}(3401)=8$ and so on...
## Example
Consider an alphabet with only $\hspace{0pt}0$, $\hspace{0pt}1$, and $\hspace{0pt}2$, among the $3^{10}$ strings of length $\hspace{0pt}10$, we wish to determine how many have even weight. Such a string has even weight precisely when the number of 1's in the string is even
There are six different cases to consider. If the string $x$ contains no 1's, then each of the $\hspace{0pt}10$ locations of $x$ can be filled with either $\hspace{0pt}0$ or $\hspace{0pt}2$, and by the [[Rule of Product|rule of product]], there are $2^{10}$ such strings. When the string contains two 1's, the locations for these two 1's can be selected in [[Combinations|${10 \choose 2 }$]] ways. Once these two locations have been specified, there are $2^{8}$ ways to place either $\hspace{0pt}0$ or $\hspace{0pt}2$ in the other eight positions, using a similar method, the number of strings for the four other cases are given below:

| Number of 1's | Number of Strings      |
| ------------- | ---------------------- |
| 4             | ${10 \choose 4 }2^{6}$ |
| 6             | ${10 \choose 6 }2^{4}$ |
| 8             | ${10 \choose 8 }2^{2}$ |
| 10            | ${10 \choose 10 }$     |
Consequently, by [[Rule of Sum|rule of sum]], the number of strings of length $\hspace{0pt}10$ that have even weight is:
$$
2^{10}+{10 \choose 2 }2^{8}+{10 \choose 4 }2^{6}+{10 \choose 6 }2^{4}+{10 \choose 8 }2^{2}+{10 \choose 10 }=\sum_{ n=0} ^{ 5}{10 \choose 2n }2^{10-2n}
$$

#Mathematics #Discrete #Functions #Definition 