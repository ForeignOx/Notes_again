Say we have $f(x,y)$ as a [[Functions|function]] of $x$ and $y$, and $x$ and $y$ are each functions of $u$ and $v$, so
$$
x=x(u,v),y=y(u,v)
$$
$$
 u=u(x,y),v=v(x,y)
$$
Can I write $\frac{ \partial f }{ \partial u }$ in terms of $\frac{ \partial f }{ \partial x }$ and $\frac{ \partial f }{ \partial y }$ 
![[Changing Coordinates 2025-01-28 14.11.28.excalidraw]]
From what we know about [[Directional Derivatives|directional derivatives]], if all the functions are [[Differentiation|differentiable]], using the [[Chain Rule|chain rule]], we can write $\frac{ \partial f }{ \partial u }$ as a [[Linear Combinations|linear combination]] of $\frac{ \partial f }{ \partial x },\frac{ \partial f }{ \partial y }$.
$$
df=\frac{ \partial f }{ \partial x } dx+\frac{ \partial f }{ \partial y } dy
$$
$$
 df=\frac{ \partial f }{ \partial u } du+\frac{ \partial f }{ \partial v } dv
$$
$$
dx=\frac{ \partial x }{ \partial u } du+\frac{ \partial x }{ \partial v } dv
$$
$$
 dy=\frac{ \partial y }{ \partial u } du+\frac{ \partial y }{ \partial v } dv
$$
Substituting the last two into the first one, we have:
$$
df=\frac{ \partial f }{ \partial x } \left( \frac{ \partial x }{ \partial u } du+\frac{ \partial x }{ \partial v } dv \right)+\frac{ \partial f }{ \partial y } \left( \frac{ \partial y }{ \partial u } du+\frac{ \partial y }{ \partial v } dv \right)
$$
$$
= \left( \frac{ \partial f }{ \partial x } \frac{ \partial x }{ \partial u } +\frac{ \partial f }{ \partial y } \frac{ \partial y }{ \partial u }  \right)du+\left( \frac{ \partial f }{ \partial x } \frac{ \partial x }{ \partial v } +\frac{ \partial f }{ \partial y } \frac{ \partial y }{ \partial v }  \right)dv
$$
So comparing with the second equation, we get:
$$
\frac{ \partial f }{ \partial u }= \frac{ \partial x }{ \partial u } \frac{ \partial f }{ \partial x } +\frac{ \partial y }{ \partial u } \frac{ \partial f }{ \partial y } 
$$
$$
 \frac{ \partial f }{ \partial v } =\frac{ \partial x }{ \partial v } \frac{ \partial f }{ \partial x } +\frac{ \partial y }{ \partial v } \frac{ \partial f }{ \partial y } 
$$
Which we can also write in a [[Matrices|matrix]] form:
$$
\begin{pmatrix}
\frac{ \partial  }{ \partial u }\\\frac{ \partial  }{ \partial v }  
\end{pmatrix}=\begin{pmatrix}
\frac{ \partial x }{ \partial u } &\frac{ \partial y }{ \partial u } \\\frac{ \partial x }{ \partial v } &\frac{ \partial y }{ \partial v } 
\end{pmatrix}\begin{pmatrix}
\frac{ \partial  }{ \partial x } \\\frac{ \partial  }{ \partial y } 
\end{pmatrix}
$$
And we see in the centre we have the [[Jacobian Transformation|Jacobian matrix]]
## Examples
$f(x,y)=x^{2}+xy+y^{2}$, $x=u-v$, $u=\frac{1}{2}(x+y)$, $y=u+v$, $v=\frac{1}{2}(y-x)$, then
$$
\frac{ \partial f }{ \partial u } =\frac{ \partial x }{ \partial u } \frac{ \partial f }{ \partial x } +\frac{ \partial y }{ \partial u } \frac{ \partial f }{ \partial y } =1(2x+y)+1(x+2y)=3x+3y=6u
$$
$$
 \frac{ \partial f }{ \partial v } =\frac{ \partial x }{ \partial v } \frac{ \partial f }{ \partial x } +\frac{ \partial y }{ \partial v } \frac{ \partial f }{ \partial y } =-(2x+y)+(x+2y)=y-x=2v
$$
Or we could do this a more "manual" way by substituting directly:
$$
f=(u-v)^{2}+(u-v)(u+v)+(u+v)^{2}
$$
$$
= u^{2}-2uv+v^{2}+u^{2}-v^{2}+u^{2}+2uv+v^{2}
$$
$$
= 3u^{2}+v^{2}
$$
Hence
$$
\frac{ \partial f }{ \partial u } =6u,\frac{ \partial f }{ \partial v } =2v
$$
___
Calculate $f_{uu}$ in terms of $x,y$ and $x,y$ of $f$, where $x=e^{ u+v },y=e^{ u-v }$
$$
f_{u}=\frac{ \partial x }{ \partial u } f_{x}+\frac{ \partial y }{ \partial u } f_{y}=e^{ u+v }f_{x}+e^{ u-v }f_{y}=xf_{x}+yf_{y}
$$
$$
f_{uu}=\frac{ \partial  }{ \partial u } (f_{u})=\frac{ \partial x }{ \partial u } \frac{ \partial f_{u} }{ \partial x } +\frac{ \partial y }{ \partial u } \frac{ \partial f_{u} }{ \partial y } =x\frac{ \partial f_{u} }{ \partial x } +y\frac{ \partial f_{u} }{ \partial y }
$$
$$
= \left( x\frac{ \partial  }{ \partial x } +y\frac{ \partial  }{ \partial y }  \right)\underbrace{ (xf_x+yf_{y})  }_{ f_{u} }
$$
$$
= x(f_{x}+xf_{xx}+yf_{xy})+y(xf_{xy}+f_{y}+yf_{yy})
$$
So
$$
f_{uu}=xf_{x}+yf_{y}+2xyf_{xy}+x^{2}f_{x x}+y^{2}f_{yy}
$$




#Mathematics #Calculus 