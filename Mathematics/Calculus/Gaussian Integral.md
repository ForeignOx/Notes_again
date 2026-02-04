The [[Integration|integral]]:
$$
\int_{-\infty}^{\infty} e^{ -ax^{2} } \, dx 
$$
For $a>0$ is known as the Gaussian integral and is important in a range of contexts, such as the [[Normal Distribution|normal distribution]]
We can derive this result using a [[Double Integrals|double integral]]; let
$$
I=\int_{-\infty}^{\infty} e^{ -ax^{2} } \, dx 
$$
$$
\implies I^{2}=\int_{-\infty}^{\infty} e^{ -ax^{2} } \, dx \int_{-\infty}^{\infty} e^{ -ay^{2} } \, dy 
$$
$$
= \int_{-\infty}^{\infty} \int_{-\infty}^{\infty} e^{ -a(x^{2}+y^{2}) } \, dx  \, dy 
$$
$$
= \iint_{\mathbb{R}^{2}}e^{ -a(x^{2}+y^{2}) }\,dxdy
$$
Now we can switch to polar coordinates using a [[Jacobian Transformation|Jacobian transformation]]:
$$
I^{2}=\iint_{\mathbb{R}^{2}}e^{ -ar^{2} }r \,drd\theta=\int _{0}^{\infty}\int _{0}^{2\pi} re^{ -ar^{2} }\, d\theta  \, dr 
$$
$$
= 2\pi \int _{0}^{\infty}re^{ -ar^{2} } \, dr  =2\pi\left[  \frac{-e^{ ar^{2} }}{2a} \right]_{0}^{\infty}=2\pi\left( \frac{1}{2a} \right)=\frac{\pi}{a}
$$
Therefore:
$$
I=\sqrt{ \frac{\pi}{a} }
$$

#Mathematics #Calculus #Definition