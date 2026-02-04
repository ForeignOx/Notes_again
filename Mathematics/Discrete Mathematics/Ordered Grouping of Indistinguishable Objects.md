Suppose we have $n$ indistinguishable objects and $k$ groups, the number of ordering them is equal to:
$$
\begin{pmatrix}
n+k-1\\n
\end{pmatrix}=\begin{pmatrix}
n+k-1\\k-1
\end{pmatrix}
$$
### Stars and bars method
This is a way of visualising why this formula applies
![[Ordered Grouping of Indistinguishable Objects 2024-10-21 15.14.38.excalidraw]]
Each group is bounded by two bars, and there are $k-1$ bars total, since once you get to the last group, you only need to bound it in one bar
Now consider instead a version where you can place a bar in a space, rather than between two spaces, so in total there are $m+k-1$ spaces that can be filled either with the $m$ sheep or the $k$ vertical lines, so we are just looking at the number of ways to do this, and so we use [[Ordered Choice of Two Types of Objects|ordered choice of two types of objects]]. So if we look at the number of ways to organise stars is:
$$
\begin{pmatrix}
m+k-1\\m
\end{pmatrix}
$$
The number of ways to organise bars is:
$$
\begin{pmatrix}
m+k-1\\k-1
\end{pmatrix}
$$


#Mathematics #Discrete 