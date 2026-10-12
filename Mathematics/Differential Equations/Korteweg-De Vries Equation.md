This is a partial differential equation given by:
$$
u_{t}+6u u_{x}+u_{xxx}=0
$$
For the real field $u(x,t)$, which represents the height of a wave in one space dimension $x$ at time $t$.
This equation describes long wavelength shallow water waves propagating in one spacial dimension and is a subtle limit of the equation describing real water waves in one space dimension in coordinates moving with the wave
## Remarks
The KdV equation is non-linear, so superposition fails
It is first order in $t$, so the solution is determined by its initial condition $u(x,0)$
It looks simple but hides rich mathematical structure
## Intuition
We can consider the initial condition 
$$
u(x,0)=\frac{2}{\cosh ^{2}(x)}
$$
First consider dropping the non-linear term to obtain the Linearised KdV equation:
$$
u_{t}+u_{xx x}=0
$$
Which has the initial wave dispersing to the left and $u\to0$ as $t\to \infty$
Next consider dropping the dispersive term $u_{x x x }$ to obtain the dispersionless KdV equation:
$$
u_{t}+6u u_{x}=0
$$
In this case the non-linearity causes the wave to pile up and break after a finite time and $\left| u_{x} \right|\to \infty$ as $t\to \frac{\sqrt{ 3 }}{16}$ which is interesing
If we keep all terms to recover the full equation, the two effects cancel and we see a travelling wave which keeps its form and just moves to the right
This initial condition is actually very special, general solutions have much more complicated behaviour, a slightly more general calss is:
$$
u(x,0)=\frac{N(N+1)}{\cosh ^{2}x}
$$
Where $N\in\mathbb{N}$