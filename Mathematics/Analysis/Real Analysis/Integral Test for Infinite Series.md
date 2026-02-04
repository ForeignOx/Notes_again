Consider a [[Continuity|continuous]] [[Monotonic Functions|monotone decreasing]] function $f:N\to \infty$, set $a_{k}=f(k)$, then the [[Series|series]]:
$$
\sum_{k=N}^{\infty} a_{k} 
$$
[[Convergence|Converges]] iff 
$$
\int_{N}^{\infty} f(t) \, dt 
$$
Converges
This is cool because we have lots of techniques for integrals, whereas relatively few for series
## Proof
$$
\sum_{k=N+1}^{x} a_{k} \leq \int_{N}^{x} f(t) \, dt\leq \sum_{k=N}^{x-1} a_{k} \leq \int_{N+1}^{x+1} f(t) \, dt 
$$
Which we see more clearly from a diagram:
![[Integral Test for Infinite Series 2025-03-20 11.43.30.excalidraw]]
Hence by squeezing, and taking limits, we complete the proof (apparently)
## Corollary
$$
\sum_{k=1}^{\infty} k^{\alpha} 
$$
Converges iff $\alpha<-1$
For $\alpha=-1$,
$$
\sum_{k=2}{n} \frac{1}{k}<\int_{1}^{n} \frac{1}{x} \, dx \ln(n)=\sum_{k=1}^{n-1} \frac{1}{k}<\sum_{k=1}^{n} \frac{1}{k}<\ln(n+1)+1
$$
$$
 0<\sum_{k=1}^{n} \frac{1}{k}-\ln(n)<\ln(n+1)-\ln(n)+1  =1+\ln\left( \frac{n+1}{n} \right)
$$
Which for $n=0$ is $1$, this is an increasing and bounded series, so it converges to the Euler-Mascherini constant:
$$
\lim_{ n \to \infty } \left( \sum_{k=1}^{n} \frac{1}{k} -\ln(n) \right)\approx0.577
$$
Which is kinda cool and stuff
(the end of analysis y1 :sob:)

