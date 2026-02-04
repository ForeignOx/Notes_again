## Definition
For some [[Rings|ring]] $R$ and some [[Ideals|ideal]] $I$, we will construct the quotient ring $R\mod I$ denoted $R / I$, it consitst of all cosets of elements of $R\mod I$. We sometimes call $R /I$ the quotient of $R$ by $I$. Its elements can be written $x+I$ or $\overline{x}$
We need to be able to add/multiply cosets, we define 
$$
(x+I)+(y+I):=(x+y)+I
$$
$$
 (x+I)\cdot(y+I)=xy+I
$$
It is not yet clear that these are well-defined, i.e. that the choice of representatives do not change the result of addition/multiplication
Recall that we encountered this for [[Integers Modulo n|$\mathbb{Z} /n$]] 
Suppose we have two representatives $x,x'\in R$ for $x+I$ and $y,y'\in R$ for $y+I$, this means
$$
x+I=x'+I
$$
$$
 y+I=y'+I
$$
To show addition is well-defined, we want
$$
(x+y)+I=(x'+y')+I
$$
Indeed, 
$$
x-x'+y-y'=(x+y)-(x'+y')\in  I
$$
Thus $(x+y)+I=(x'+y')+I$
To show multiplication is well defined, we want
$$
xy+I=x'y'+I
$$
Again $x-x'\in I$ and $y-y'\in I$, so
$$
(x-x')y\in  I,\, x'(y-y')\in  I
$$
By absorption (which is why we need absorption in the definition of an ideal)
We can add these two relations, using that $I$ is closed under addition:
$$
(x-x')y+x'(y-y')=xy-x'y'\in  I
$$
Which is what we wanted.
Now $R/I$ (the set of all cosets) with addition and multiplication as above is a ring because it inherits all the properties of $R$. Similarly, if $R$ is commutative, so is $R /I$
## Remarks
If $I=(1)=R$, then $R /R=\left\{ 0 \right\}=\left\{ \overline{0} \right\}$
If $I=0$, then $R /0\cong R$, because $x,y\in R$ are equivalent $\mod 0$ if $x-y\in \left\{ 0 \right\}$, ie. if $x=y$