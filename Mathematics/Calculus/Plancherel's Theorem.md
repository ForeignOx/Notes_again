$$
1=\int_{-\infty}^{\infty} \left| \psi(x) \right| ^{2} \, dx =\frac{1}{2\pi}\int_{-\infty}^{\infty} \left| \tilde{\psi}(p) \right| ^{2} \, dp 
$$
Recall by [[Fourier Transform|fourier transforms]], 
$$
\psi(x)=\frac{1}{2\pi}\int_{-\infty}^{\infty} \tilde{\psi}(p)e^{ ipx } \, dp 
$$
Now
$$
\int_{-\infty}^{\infty} \left| \psi \right| ^{2} \, dx =\int_{-\infty}^{\infty} \psi  \overline{\psi} \, dx =\int_{-\infty}^{\infty} \psi(x)\left( \frac{1}{2\pi}\int_{-\infty}^{\infty} \tilde{\psi}(p)e^{ -ipx } \, dp  \right) \, dx 
$$
$$
= \frac{1}{2\pi}\int_{-\infty}^{\infty} \overline{\tilde{\psi}(p)}\int_{-\infty}^{\infty} \psi(x)e^{ -ipx } \, dp  \, dx 
$$
$$
= \frac{1}{2\pi}\int_{-\infty}^{\infty} \overline{\tilde{\psi}(p)}\tilde{\psi}(p) \, dx =\frac{1}{2\pi}\int_{-\infty}^{\infty} \left| \tilde{\psi}(p) \right| ^{2} \, dp
$$
