## Odd Functions
If $f_{\text{odd}}(x)$ is an [[Integration|integrable]] [[Odd Functions|odd]] [[Functions|function]] on [[Intervals|$[-a,a]$]], then
$$
\int _{-a}^{a}f_{\text{odd}}(x) \, dx =0
$$
### Proof
$$
I=\int _{-a}^{a}f_{\text{odd}}(x) \, dx=\int _{-a}^{0}f_{\text{odd}}(x) \, dx+\int _{0}^{a}f_{\text{odd}}(x) \, dx
$$
Letting $x=-y$, then relable the $y$ as $x$, so
$$
I=-\int _{a}^{0}f_{\text{odd}}(-x) \, dx+\int _{0}^{a}f_{\text{odd}}(x) \, dx
$$
$$
=\int _{0}^{a}f_{\text{odd}}(-x) \, dx+\int _{0}^{a}f_{\text{odd}}(x) \, dx=\int ^{a}_{0}f_{\text{odd}}(-x)+ f_{\text{odd}}(x) \, dx 
$$
$$
= \int ^{a}_{0}-f_{\text{odd}}(x)+ f_{\text{odd}}(x) \, dx =0
$$
## Even Functions
If $f_{\text{even}}(x)$ is an integrable [[Even Functions|even]] function on $[-a,a]$
$$
\int _{-a}^{a}f_{\text{even}}(x) \, dx =2\int _{0}^{a}f_{\text{even}}(x) \, dx 
$$
## Turning Functions into Odd and Even
Recall tha any function can be decomposed into the sum of an odd and even function,
$$
f(x)=f_{\text{even}}(x)+f_{\text{odd}}(x)=\frac{1}{2}(f(x)+f(-x))+\frac{1}{2}(f(x)-f(-x))
$$
From this we can see that:
$$
\int _{-a}^{a}f(x) \, dx =2\int _{0}^{a}f_{\text{even}}(x) \, dx 
$$

#Mathematics #Calculus 