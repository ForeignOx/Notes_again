If $f(x)$ and $g(x)$ are both [[Differentiation|differentiable]] [[Functions|functions]], that are differentiable $n$ times, then so is the product $(fg)(x)$
Denote this function$h(x)=f(x)g(x)$:
$$
h'(x)=\lim_{ \delta x \to 0 } \frac{h(x+\delta x)-h(x)}{\delta x}
$$
$$
=\lim_{ \delta x \to 0 } \frac{f(x+\delta x)g(x+\delta x)-f(x)g(x)}{\delta x}
$$
$$
=\lim_{ \delta x \to 0 } \frac{f(x+\delta x)g(x+\delta x)-f(x)g(x+\delta x)+f(x)g(x+\delta x)-f(x)g(x)}{\delta x}
$$
$$
=\lim_{ \delta x \to 0} \frac{(f(x+\delta x)-f(x))g(x+\delta x)+f(x)(g(x+\delta x)-g(x)))}{\delta x}
$$
$$
=\lim_{ \delta x \to 0 } \frac{g(x+\delta x)(f(x+\delta x)-f(x))}{\delta x}+\lim_{ \delta x \to 0 } \frac{f(x)(g(x+\delta x)-g(x))}{\delta x}
$$
$$
=(\lim_{ h \to 0 } g(x+\delta x))\left( \lim_{ \delta x \to 0 } \frac{f(x+\delta x)-f(x)}{\delta x} \right)+(\lim_{ \delta x \to 0 } f(x))\left( \lim_{ \delta x \to 0 } \frac{g(x+\delta x)-g(x)}{\delta x} \right)
$$
$$
g(x)f'(x)+f(x)g'(x)
$$
Hence:
$$
\frac{d }{dx} f(x)g(x)=g(x)f'(x)+f(x)g'(x) 
$$
Another way of writing this is:
$$
D(fg)=(Df)g+f(Dg)
$$
Then this can be applied again for the second derivative:
$$
D^{2}(fg)=(D^{2}f)g+(Df)(Dg)+(Df)(Dg)+f(D^{2}g)=(D^{2}f)g+2(Df)(Dg)+f(D^{2}g)
$$
This looks a lot like the [[Binomial Theorem|binomial expansion]], and we can in fact expand upon this and say:
$$
D^{n}(fg)=\sum_{ k=0} ^{ n}\begin{pmatrix}
n\\k
\end{pmatrix}(D^{k}f)(D^{n-k}g)  
$$
## Examples
Calculate $D^{3}(x^{2}\sin x)$, we know:
$$
D^{3}(fg)=(D^{3}f)g+3(D^{2}f)(Dg)+3(Df)(D^{2}g)+f(D^{3}g)
$$
Letting $f(x)=x^{2}$, $Df=2x$, $D^{2}f=2$, $D^{3}f=0$, $g(x)=\sin x$, $Dg=\cos x$, $D^{2}g=-\sin x$, $D^{3}g=-\cos x$, so:
$$
D^{3}(x^{2}\sin x)=3(2)\cos x+3(2x)(-\sin x)+x^{2}(-\cos x)=(6-x^{2})\cos x=6x\sin x
$$
# For Differential Operators
If $f,g:\mathbb{R}^{3}\to \mathbb{R}$ are [[Scalar Fields|scalar fields]], and $\underline{f},\underline{g}:\mathbb{R}^{3}\to \mathbb{R}^{3}$ are [[Vector Fields|vector fields]] and are all $C^{1}$ ([[Continuity|continuously]] differentiable), then using the differential operators [[Gradient of Scalar Fields|gradient]], [[Divergence and Curl|divergence and curl]], we get $\hspace{0pt}6$ product rules:
- $\underline{\nabla }(fg)\equiv g \underline{\nabla }f+f\underline{\nabla }g$
- $\underline{\nabla }\cdot(g \underline{f})\equiv(\underline{\nabla }g)\cdot \underline{f}+g\underline{\nabla} \cdot \underline{f}$
- $\underline{\nabla }\cdot(\underline{f}\times \underline{g})\equiv \underline{g}\cdot(\underline{\nabla} \times \underline{f})-\underline{f}\cdot(\underline{\nabla} \times \underline{g})$
- $\underline{\nabla }\times(g \underline{f})\equiv g(\underline{\nabla} \times \underline{f})+(\underline{\nabla }g)\times \underline{f}$
- $\underline{\nabla }\times(\underline{f}\times \underline{g})\equiv (\underline{g}\cdot  \underline{\nabla })\underline{f}-(\underline{f}\cdot \underline{\nabla })\underline{g}+\underline{f}(\underline{\nabla} \cdot \underline{g})-\underline{g}(\underline{\nabla} \cdot \underline{f})$ 
- $\underline{\nabla }(\underline{f}\cdot \underline{g})\equiv(\underline{g}\cdot \underline{\nabla })\underline{f}+(\underline{f}\cdot \underline{\nabla })\underline{g}+\underline{f}\times(\underline{\nabla} \times \underline{g})+\underline{g}\times (\underline{\nabla} \times \underline{f})$
Where we define the operator $(\underline{g}\cdot \underline{\nabla })\underline{f}$ has $i$th (cartesian) component $g_{j}\frac{ \partial f_{i} }{ \partial x_{j} }$, and can be defined as:
$$
(\underline{g}\cdot \underline{\nabla } )\underline{f} = \lim_{ d(S) \to 0 } \frac{1}{\left| V \right| }\oint_{S} \underline{f}(\underline{g}\cdot  \underline{\hat{n}})\,dS
$$
### Proof
Since both sides are [[Coordinates|coordinate]] independent, it suffices to prove them in cartesian coordinates
- For the first:
$$
\underline{\nabla } (fg)=\frac{ \partial  }{ \partial x } (fg)\underline{e}_{1}+\frac{ \partial  }{ \partial y } (fg)\underline{e}_{2}+\frac{ \partial  }{ \partial z } (fg)\underline{e}_{3}
$$
    And we can use the usual 1D product rule to get:
$$
= \left( \frac{ \partial f }{ \partial x } g+f\frac{ \partial g }{ \partial x }  \right)\underline{e}_{1}+\left( \frac{ \partial f }{ \partial y } g+f\frac{ \partial g }{ \partial y }  \right)\underline{e}_{2}+\left( \frac{ \partial f }{ \partial z } g+f\frac{ \partial g }{ \partial z }  \right)\underline{e}_{3}
$$
$$
= \left( \frac{ \partial f }{ \partial x } \underline{e}_{1}+\frac{ \partial f }{ \partial y } \underline{e}_{2}+\frac{ \partial f }{ \partial z } \underline{e}_{3} \right)g+f\left( \frac{ \partial g }{ \partial x } \underline{e}_{1}+\frac{ \partial g }{ \partial y } \underline{e}_{2}+\frac{ \partial g }{ \partial z } \underline{e}_{3} \right)
$$
$$
= g\underline{\nabla } f+f \underline{\nabla } g
$$
- For the second:
$$
\underline{\nabla } \cdot(g\underline{f})=\underline{\nabla } \cdot(gf_{1}\underline{e}_{1}+gf_{2}\underline{e}_{2}+gf_{3}\underline{e}_{3})
$$
$$
= \underline{\nabla } (gf_{1})\cdot \underline{e}_{1}+\underline{\nabla }(gf_{2})\cdot \underline{e}_{2}+\underline{\nabla } (gf_{3})\cdot \underline{e}_{3}
$$
$$
= (g \underline{\nabla } f_{1}+f_{1}\underline{\nabla } g)\cdot \underline{e}_{1}+(g \underline{\nabla } f_{2}+f_{2}\underline{\nabla } g)\cdot \underline{e}_{2}+(g \underline{\nabla } f_{3}+f_{3}\underline{\nabla } g)\cdot \underline{e}_{3}
$$
$$
= g\frac{ \partial f_{1} }{ \partial x } +f_{1}\frac{ \partial g }{ \partial x } +g\frac{ \partial f_{2} }{ \partial y } +f_{2}\frac{ \partial g }{ \partial y } +g\frac{ \partial f_{3} }{ \partial z }  +f_{3}\frac{ \partial g }{ \partial z } 
$$
$$
= g\left( \frac{ \partial f_{1} }{ \partial x } +\frac{ \partial f_{2} }{ \partial y } +\frac{ \partial f_{3} }{ \partial z }  \right)+(f_{1}\underline{e}_{1}+f_{2}\underline{e}_{2}+f_{3}\underline{e}_{3})\cdot\left( \frac{ \partial g }{ \partial x } \underline{e}_{1}+\frac{ \partial g }{ \partial y } \underline{e}_{2}+\frac{ \partial g }{ \partial z } \underline{e}_{3} \right)
$$
$$
= g (\underline{\nabla} \cdot \underline{f} )+\underline{f}\cdot (\underline{\nabla } g)
$$
- For the third part:
$$
\underline{\nabla } \cdot(\underline{f}\times \underline{g})=\underline{\nabla } \cdot \det \begin{pmatrix}
\underline{e}_{1} & \underline{e}_{2} & \underline{e}_{3} \\
f_{1} & f_{2} & f_{3} \\
g_{1} & g_{2} & g_{3} 
\end{pmatrix}
$$
$$
= \frac{ \partial  }{ \partial x } (f_{2}g_{3}-f_{3}g_{2})+\frac{ \partial  }{ \partial y } (f_{3}g_{1}-f_{1}g_{3})+\frac{ \partial  }{ \partial z }(f_{1}g_{2}-f_{2}g_{1})
$$
$$
= g_{1}\left( \frac{ \partial f_{3} }{ \partial y } -\frac{ \partial f_{2} }{ \partial z }  \right)+g_{2}\left( \frac{ \partial f_{1} }{ \partial z } -\frac{ \partial f_{3} }{ \partial x }  \right)+g_{2}\left( \frac{ \partial f_{2} }{ \partial x } -\frac{ \partial f_{1} }{ \partial y }  \right)
$$
$$
 +f_{1}\left( \frac{ \partial g_{2} }{ \partial z } -\frac{ \partial g_{3} }{ \partial y }  \right)+f_{2}\left( \frac{ \partial g_{3} }{ \partial x } -\frac{ \partial g_{1} }{ \partial z }  \right)+f_{3}\left( \frac{ \partial g_{1} }{ \partial y } -\frac{ \partial g_{2} }{ \partial x }  \right)
$$
$$
= \underline{g}\cdot (\underline{\nabla} \times \underline{f} )-\underline{f}\cdot (\underline{\nabla} \times \underline{g} ) 
$$
- For the fourth part
$$
\underline{\nabla } \times(g\underline{f})=\underline{\nabla } \times(gf_{1}\underline{e}_{1}+gf_{2}\underline{e}_{2}+gf_{3}\underline{e}_{3})
$$
$$
= \underline{\nabla } (gf_{1})\times \underline{e}_{1}+\underline{\nabla } (gf_{2})\times \underline{e}_{2}+\underline{\nabla } (gf_{3})\times \underline{e}_{3}
$$
$$
= \frac{ \partial  }{ \partial y } (gf_{1})\underline{e}_{2}\times \underline{e}_{1}+\frac{ \partial  }{ \partial z } (gf_{1})\underline{e}_{3}\times \underline{e}_{1}+\frac{ \partial  }{ \partial x } (gf_{2})\underline{e}_{1}\times \underline{e}_{2}+\frac{ \partial  }{ \partial z } (gf_{2})\underline{e}_{3}\times \underline{e}_{2}
$$
$$
 +\frac{ \partial  }{ \partial x }(gf_{3})\underline{e}_{1}\times \underline{e}_{3}+\frac{ \partial  }{ \partial y }  (gf_{3})\underline{e}_{2}\times \underline{e}_{3}
$$
$$
= g\left( \left( \frac{ \partial f_{3} }{ \partial y } -\frac{ \partial f_{2} }{ \partial z }  \right)\underline{e}_{1}+\left( \frac{ \partial f_{1} }{ \partial z } -\frac{ \partial f_{3} }{ \partial x } \underline{e}_{2} \right)+\left( \frac{ \partial f_{2} }{ \partial x } -\frac{ \partial f_{1} }{ \partial y } \underline{e}_{3} \right) \right)
$$
$$
 +\left( \frac{ \partial g }{ \partial y } f_{3}-\frac{ \partial g }{ \partial z } f_{2} \right)\underline{e}_{1}+\left( \frac{ \partial g }{ \partial z } f_{1}-\frac{ \partial g }{ \partial x } f_{3} \right)\underline{e}_{2}+\left( \frac{ \partial g }{ \partial x } f_{2}-\frac{ \partial g }{ \partial y } f_{1} \right)\underline{e}_{3}
$$
$$
= g(\underline{\nabla} \times \underline{f} )+(\underline{\nabla } g)\times \underline{f}
$$
- For the fifth using [[Index Notation|index notation]]:
$$
[\underline{\nabla} \times (\underline{f}\times \underline{g})]_{i}= \epsilon_{ijk}\frac{ \partial  }{ \partial x_{j} } [\underline{f}\times \underline{g}]_{k}
$$
$$
= \epsilon_{ijk}\frac{ \partial  }{ \partial x_{j} } (\epsilon_{klm}f_{l}g_{m})
$$
$$
= \epsilon_{ijk}\epsilon_{klm}\frac{ \partial  }{ \partial x_{j} } (f_{l}g_{m})
$$
$$
= \epsilon_{ijk}\epsilon_{klm}\left( \frac{ \partial f_{l}}{ \partial x_{j} } g_{m}+f_{l}\frac{ \partial g_{m} }{ \partial x_{j} }  \right)
$$
    By the usual product rule
$$
=(\delta_{il}\delta_{jm}-\delta_{im}\delta_{jl})\left( \frac{ \partial f_{l} }{ \partial x_{j} } g_{m}+f_{l}\frac{ \partial g_{m} }{ \partial x_{j} }  \right)
$$
$$
= \delta _{il}\delta_{jm} \frac{ \partial f_{l} }{ \partial x_{j} } g_{m}+\delta_{il}\delta_{jm}f_{l}\frac{ \partial g_{m} }{ \partial x_{j} } -\delta_{im}\delta_{jl}f_{l}\frac{ \partial g_{m} }{ \partial x_{j} } -\delta_{im}\delta_{jl}\frac{ \partial f_{l} }{ \partial x_{j} } g_{m}
$$
$$
= \delta_{il}\frac{ \partial f_{l} }{ \partial x_{j} } g_{j}+\delta_{il}f_{l}\frac{ \partial g_{j} }{ \partial x_{j} } -\delta_{jl}f_{l}\frac{ \partial g_{i} }{ \partial x_{j} } -\delta_{jl}\frac{ \partial f_{l} }{ \partial x_{j} } g_{i}
$$
$$
= \frac{ \partial f_{i} }{ \partial x_{j} } g_{j}+f_{i}\underbrace{ \frac{ \partial g_{j} }{ \partial x_{j} } }_{ \underline{\nabla} \cdot \underline{g}  } -f_{j}\frac{ \partial g_{i} }{ \partial x_{j} } -\underbrace{ \frac{ \partial f_{j} }{ \partial x_{j} } }_{ \underline{\nabla} \cdot \underline{f}  } g;i
$$
$$
= [(\underline{g}\cdot \underline{\nabla })\underline{f}]_{i} +[\underline{f}(\underline{\nabla} \cdot \underline{g} )]_{i}-[(\underline{f}\cdot \underline{\nabla } )\underline{g}]_{i}-[(\underline{\nabla} \cdot \underline{f}  )\underline{g}]_{i}
$$
- For the sixth, here the right hand side has the triple products, so we'll start there
$$
[\underline{f}\times(\underline{\nabla} \times \underline{g} )]_{i}= \epsilon_{ijk}f_{j}[\underline{\nabla} \times \underline{g} ]_{k}
$$
$$
= \epsilon_{ijk}f_{j}\epsilon_{klm}\frac{ \partial g_{m} }{ \partial x_{l} } 
$$
$$
= \epsilon_{ijk}\epsilon_{klm}f_{j}\frac{ \partial g_{m} }{ \partial x_{l} } 
$$
$$
= (\delta_{il}\delta_{jm}-\delta_{im}\delta_{jl})f_{j}\frac{ \partial g_{m} }{ \partial x_{l} } 
$$
$$
= \delta_{il}\delta_{jm}f_{j}\frac{ \partial g_{m} }{ \partial x_{l} } -\delta_{im}\delta_{jl}f_{j}\frac{ \partial g_{m} }{ \partial x_{l} } 
$$
$$
= \delta_{il}f_{j}\frac{ \partial g_{j} }{ \partial x_{l} } -\delta_{jl}f_{j}\frac{ \partial g_{i} }{ \partial x_{l} } 
$$
$$
= f_{j}\frac{ \partial g_{j} }{ \partial x_{i} } -f_{j}\frac{ \partial g_{i} }{ \partial x_{j} } 
$$
    So $i$th component of the RHS of the identity is equal to 
$$
g_{j}\frac{ \partial f_{i} }{ \partial x_{j} } +f_{j}\frac{ \partial g_{i} }{ \partial x_{j} } +f_{j}\frac{ \partial g_{j} }{ \partial x_{i} } -f_{j}\frac{ \partial g_{i} }{ \partial x_{j} }+g_{j}\frac{ \partial f_{j} }{ \partial x_{i} } -g_{j}\frac{ \partial f_{i} }{ \partial x_{j} }  
$$
$$
= f_{j} \frac{ \partial g_{j} }{ \partial x_{i} } +g_{j}\frac{ \partial f_{j} }{ \partial x_{i} } 
$$
    Using the inverse of the normal product rule:
$$
= \frac{ \partial  }{ \partial x_{i} } (f_{j}g_{j})=\frac{ \partial  }{ \partial x_{i} } (\underline{f}\cdot \underline{g})=[\underline{\nabla } (\underline{f}\cdot \underline{g})]_{i}
$$

### Example
If $u,v:\mathbb{R}^{3}\to \mathbb{R}$ are scalar fields, show that $\underline{\nabla }u\times \underline{\nabla }v=\underline{\nabla }\times(u\underline{\nabla }v)$
We can start from the more complicated side (with the curl) by treating $u$ as a scalar field and $\underline{\nabla }v$ as a vector field, so using the fourth form,
$$
\underline{\nabla } \times(u \underline{\nabla } v)=u(\underbrace{ \underline{\nabla } \times(\underline{\nabla } v) }_{ =0 })+(\underline{\nabla } u)\times(\underline{\nabla } v)=\underline{\nabla } u\times \underline{\nabla } v
$$


#Mathematics #Calculus 