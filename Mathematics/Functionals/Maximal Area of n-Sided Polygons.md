Let us consider the product of two numbers $x$, $y$, whose sum is constant; it is known that this product is a maximum when the two numbers are equal. This can be converted to geometrical language by saying that among all the rectangles which have the sum of two consecutive sides constant, and therefore have a constant perimeter, the square is the one of maimum area
We can then extend this to the ore general problem of determining, among all planar polygons of $n$ sides whose permeter is constant, the one of maximum area whill be the regular polygon of $n$ sides
If we denote the $2n$ coordinates of the $n$ vertices of the polygon by $(x_{1},y_{1}),(x_{2},y_{2}),\dots,(x_{n},y_{n})$, the quantity to be made a maximum is the area $A$, given by the expression:
$$
A=\frac{1}{2}\sum_{ i=1} ^{ n}  \left| \begin{matrix}
x_{i}&x_{i+1}\\y_{i}&y_{i+1}
\end{matrix}\right|=\frac{1}{2}\sum_{ i=1} ^{ n}  (x_{i}y_{i+1}-y_{i}x_{i+1})=\frac{1}{2}\sum_{ i=1} ^{ n}  (x_{i}(y_{i+1}-y_{i})-y_{i}(x_{i+1}-x_{i}))
$$
$$
= \frac{1}{2}\sum_{ i=1} ^{ n}  (x_{i}\Delta y_{i}-y_{i}\Delta x_{i})
$$
A function, in this case, of the $2n$ variables $x_{i},y_{i}$ with:
$$
\sum_{ i=1} ^{ n}  \sqrt{ \Delta x_{i}^{2}+\Delta y_{i}^{2} }=k,k\in \mathbb{R}
$$
And in which:
$$
x_{n+1}=x_{1}
$$
$$
y_{n+1}=y_{1}
$$
$$
\Delta x_{i}=x_{i+1}-x_{i}
$$
$$
 \Delta y_{i}=y_{i+1}-y_{i}
$$
But if we pass from the case of a polygon of constant perimeter to the more general problem of determining, among all the closed curves $C$ of a given length $l$, the one that includes the maximum area $A$ (the circle), the quantity $A$ that we have to consider is given by the formula:
$$
A=\frac{1}{2}\int _{C}(xdy-ydx)
$$
With:
$$
\int _{C}\sqrt{ dx^{2}+dy^{2} }=l,l\in n\mathbb{R}
$$
And thus no longer depends on a finite number of variables, but on the values of the coordinates of all the infinite number of points of the line $C$. Instead of a problem of the ordinary differential calculus on maxima and minima, in which we have to determine a certain finite number of unknown quantities, we have a problem of the calculus of variations, in which the unknown is a [[Functions|function]] (its values for all the points of the [[Intervals|interval]] considered) or a curve (the coordinates of all its points)
In the case of the polygon of $n$ sides it is sufficient to find quantities $(x_{1},y_{1}),(x,y_{2}),\dots,(x_{n},y_{n})$, depending on the index $i$, discontinuous and variable for integral values from $\hspace{0pt}1$ to $n$, in order to determine the polygon itself. In the case of any closed curve $C$, however, it will be necessary, in order to etermine it, to give the coordinates $x$ and $y$ of all its points
$$
x=x(t),y=y(t)
$$
$$
x(b)=x(a),y(b)=y(a)
$$
In which now the quantities $x,y$ depend on the parameter $t$ which varies ontinuously in a certain intervl $(a,b)$; this continuous parameter $t$ takes the place of the dicontinuous index $i$, so corresponding to the formulas containing sums with respect to the index $i$, we get instead the formulae containing integrals in which we may take the parameter $t$ as the variable of integration
The path followed in this particular example to pass fro a problem with a finite number of unknowns to a problem in which the unknown is a function (a problem with an infinite number of unknowns) has the character of a general method. In many other cases in which this eventuality arises, it will in fact be sufficient to replace a discontinuous index $i$ by a continuous index, or parameter $t$, and the sum with respect to this index $i$ by the integral with respect to the variable of integration $t$
There are however problems in which the unknown is a function, but which we have a different character. Thus, for instance, if we wish to determine a curve, $y=y(x)$, whose subtangent is constant $(=a)$, we shall get the differential equation:
$$
a \frac{dy}{dx}=y
$$
and in this equation, theree is no integral with respect to $x$; all the infinite number of values of the unknown $y$ corresponding to the infinite number of values of $x$ do not simultaneously enter into consideration; we can say rather that this equation establishes a relation solely between a value of $y$ and the value it has at an infinitely near point determined by $\frac{d y}{dx}$. More generally, all the problems that give rise to an ordinary differential equation:
$$
f(x,y,y',\dots,y^{(n)})=0
$$
which establishes a relation only between the values taken by $y$ at a point $x$ and at $n$ infinitely near points, are of this type
## Similar(ish) Problem
A related problem is that of determining a plane curbe (of equation $y=y(x)$) passing through two given points inthe plane (of coordinates $(x_{0},y_{0}): y_{0}=y(x_{0}),(x_{1},y_{1}): y_{1}=y(x_{1})$) such that when it rotates round a line fixed in the plane, for example the $x$-axis, it generates the surface of minimum area. In this case, the area $A$, the quantity to be made a minimum, is given by the expression:
$$
A=2\pi \int _{x_{0}}^{x_{1}}y\sqrt{ 1+y'^{2} } \, dx 
$$
And therefore depends on all the values of $y$ in the interval $(x_{0},x_{1})$