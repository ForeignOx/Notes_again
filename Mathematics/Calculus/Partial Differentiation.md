[[Differentiation|Differentiating]] a multivariable [[Functions|function]] with respect to a variable (usually) means that you treat all other variables as constants and differentiate normally
The partial derivative of $f$ with respect to $x$ can be written:
$$
\frac{ \partial f }{ \partial x } =f_{x}(x,y,\dots)=\lim_{ h \to 0 } \frac{f(x+h,y,\dots)-f(x,y,\dots)}{h}
$$
We can take partial derivatives of partial derivatives, to get 2nd partial derivatives, such as:
$$
\frac{ \partial^{2}f }{ \partial x^{2} } =\frac{ \partial  }{ \partial x } \left( \frac{ \partial f }{ \partial x }  \right)=f_{xx}
$$
$$
 \frac{ \partial^{2}f }{ \partial x\partial y }=\frac{ \partial  }{ \partial x } \left( \frac{ \partial y }{ \partial y }  \right) =f_{yx}
$$
(note that notationally, some places denote it $f_{xy}$ instead)
## Two Variables
We can consider $f(x,y)$ as the height of a function over the $xy$-plane
![[Partial Differentiation 2024-11-01 15.29.51.excalidraw]]
We can now think of the rate of change of $f(x,y)$ as we vary $x$ or $y$, keeping the other fixed
### First Principles
$$
\delta f=f(x,y)-f(x_{0},y_{0})=M(x-x_{0})+N(y-y_{0})+R(x,y)
$$
Letting $x=x_{0}+\delta x,y=y_{0}+\delta y$, then
$$
\delta f=M\delta x+N\delta y+R(x,y)\approx M\delta x+N\delta y
$$
As $R(x,y)$ goes to $\hspace{0pt}0$ faster than $\delta x,\delta y$ as $\delta x,\delta y\to 0$
In two or more dimensions the slope I experience depends on which direction I move in
Suppose we move parallel to $x$ axis, $\underline{x}=(x_{0}+\delta x,y_{0})$, $\delta y=0$
Then
$$
\delta f=f(x_{0}+\delta x,y_{0})=M\delta x+\underbrace{ N\delta y }_{ =0 }+R(x_{0}+\delta x,y_{0})
$$
$$
\implies \frac{f(x_{0}+\delta x,y_{0})-f(x_{0},y_{0})}{\delta x}=M+\frac{R(x_{0}+\delta x,y_{0})}{\delta x}
$$
Taking limts we get:
$$
\lim_{ \delta x \to 0 } \frac{f(x_{0}+\delta x,y_{0})-f(x_{0},y_{0})}{\delta x}=M+\lim_{ \delta x \to 0 } \frac{R(x_{0}+\delta x,y_{0})}{\delta x}
$$
And
$$
\lim_{ \delta x \to 0 } \frac{R(x,y)}{\left| \underline{x}-\underline{x}_{0} \right| }=0
$$
Since $f(x,y)$ is [[Differentiation#Differentiability for Functions of $ hspace{0pt}2$ Variables $f(x,y)$|differentiable]] 
Hence
$$
\frac{ \partial f }{ \partial x } (x_{0},y_{0})=\lim_{ \delta x \to 0 } \frac{f(x_{0}+\delta x,y_{0})-f(x_{0},y_{0})}{\delta x}=f_{x}(x_{0},y_{0})=\partial_{x}f(x_{0},y_{0})
$$
Now this limit coincides with the ordinary derivative of $F(x)=f(x,y_{0})$, so normal rules still apply (such as [[Chain Rule|chain rule]])
Without loss of generality, we can define:
$$
\frac{ \partial f }{ \partial y } (x_{0},y_{0})=\lim_{ \delta y \to 0 } \frac{f(x_{0},y_{0}+\delta y)-f(x_{0},y_{0})}{\delta y}=f_{y}(x_{0},y_{0})=\partial_{y}f(x_{0},y_{0})
$$
We have shown that if the function is differentiable, then the partial derivatives exist, but the converse is not in fact true unlike in 1D. You can think of this as partial derivatives only travel in one axis, so have no information about the other directions, so it is a weaker result
___
If $f(x,y)$ is differentiable, then we can find $f_{x},f_{y}$, and these in turn may be differentiable, in which case we can differentiate again:
$$
\frac{ \partial  }{ \partial x } \left( \frac{ \partial f }{ \partial x }  \right)=\frac{ \partial^{2}f }{ \partial x^{2} } =(f_{x})_{x}=f_{xx}
$$
### Example
Let $f(x,y)=x^{2}y^{3}-\sin x\cos y-y$, then
$$
\frac{ \partial f }{ \partial x } =2xy^{3}-\cos x\cos y
$$
$$
\frac{ \partial f }{ \partial y } =3x^{2}y^{2}+\sin x\sin y-1
$$
$$
\frac{ \partial^{2}f }{ \partial x^{2} } =2y^{3}+\sin x\cos y
$$
$$
 \frac{ \partial^{2} f }{ \partial y^{2} }=6x^{2}y+\sin x\cos y
$$
$$
 \frac{ \partial^{2}f }{ \partial x\partial y }=6xy^{2}+\cos x\sin y
$$
$$
\frac{ \partial^{2} f }{ \partial y\partial x }=6xy^{2}+\cos x\sin y
$$
Note the last two are equal, but that is not generally the case, but is true is $f$ and all 1st and 2nd partial derivatives are [[Continuity|continuous]] ([[Clairaut's Theorem|Clairaut's theorem]])

#Mathematics #Calculus