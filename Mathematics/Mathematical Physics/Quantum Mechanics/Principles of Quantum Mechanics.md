## Principle 1: States
> The state of a system is a normalised vector $\ket{ \psi}$ in a Hilbert space $\mathcal{H}$ 

Notes:
- Any normalised superposition (sum) of states is also an allowed state
- The state is supposed to contain all knowable information about the system
- The state is not itself an observable; it is not a measurable quantity, and it is not itself a probability, it is a mathematical objecct that allows us to calculate probabilities of measurement results
## Principle 2: Observables
> Each observable (measurable quantity) $A$ corresponds to a Hermitian operator $\hat{A}$. The possible results of measuring $A$ are the eigenvalues of $\hat{A}$, which are real
## Principle 3: The Born Rule
> If the system is in state $\ket{\psi}$ and the observable $A$ i measured, the probability of obtaining the result $a$ is:
$$
P(a)=\bra{\psi} \hat{P}_{a}\ket{\psi} 
$$
> Where $\hat{P}_{a}$ is the projector onto the eigenspace of $a$. If $a$ is non-degenerate, with normalised eigenvector $\ket{a}$, this is
$$
P(a)=\left| \braket{ a | \psi }  \right| ^{2}
$$
## Principle 4: Collapse
> Immediately after the measurement gives the result $a$, the state collapses to the normalised projection of $\ket{\psi}$ onto the eigenspace of $a$:
$$
\ket{\psi'} =\frac{\hat{P}_{a}\ket{\psi} }{\sqrt{ \bra{\psi} \hat{P}_{a}\ket{\psi} }}
$$
> In particular, $\ket{\psi'}$ is an eigenvector of $\hat{A}$ with measured eigenvalue: $\hat{A}\ket{\psi'}=a\ket{\psi'}$

