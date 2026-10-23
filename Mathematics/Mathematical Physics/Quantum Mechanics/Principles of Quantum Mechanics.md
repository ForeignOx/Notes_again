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
\mathbb{P}(a)=\bra{\psi} \hat{P}_{a}\ket{\psi} 
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
> In particular, $\ket{\psi'}$ is an eigenvector of $\hat{A}$ with measured eigenvalue: $\hat{A}\ket{\psi'}=a\ket{\psi'}$, and if $a$ is non-degenerate, this simplifies to
$$
\ket{\psi'} =\ket{a} 
$$
## Consequences
- The probabilities add up to one:
$$
\sum_{a}\mathbb{P}(a)=\bra{\psi}  \sum_{a}\hat{P}_{a}\ket{\psi} =\braket{ \psi | \psi } =1
$$
    Using $\sum_{a}\hat{P}_{a}=\mathbb{1}$, this is why states are normalised
- $\mathbb{P}(a)=\bra{\psi}\hat{P}_{a}\ket{\psi}=\bra{\psi}\hat{P}_{a}^{\dagger}\hat{P}_{a}\ket{\psi}=\lvert \lvert \hat{P}_{a}\ket{\psi} \rvert \rvert ^{2}$ is the squared length of the projection of $\psi$ onto the eigenspace, so $0\leq \mathbb{P}(a)\leq 1$
![[Pasted image 20261023092528.png]]
- If the eigenspace has an orthonormal basis $\ket{a,1},\dots,\ket{a,d}$, then $\hat{P}_{a}=\sum_{k}\ket{a,k}\bra{a,k}$ and $\mathbb{P}(a)=\sum_{k}\left| \braket{ a,k | \psi } \right|^{2}$
- Repeating measurement gives the ssame result: Since $\hat{A}\ket{\psi'}=a\ket{\psi'}$ and $\ket{\psi'}$ lies in the eigenspace of $a$, so $\hat{P}_{a}\ket{\psi'}=\ket{\psi'}$ and measusring $A$ again gives $a$ with probability
$$
\bra{\psi'}  \hat{P}_{a}\ket{\psi'} =\frac{\bra{\psi} \hat{P}_{a}^{\dagger}\hat{P}_{a}\hat{P}_{a}\ket{\psi} }{\bra{\psi} \hat{P}_{a}\ket{\psi} }=1
$$
- $\ket{\psi'}$ is normalised; dividing by $\sqrt{ \mathbb{P}(a) }=\lvert \lvert \hat{P}_{a}\ket{\psi} \rvert \rvert$ makes it length 1
- An overall phase has no physical effect. For real $\alpha$, the states $\ket{\psi}$ and $e^{ i\alpha }\ket{\psi}$ give the same probabilities for every meassurement, since $\bra{\psi}e^{ -i\alpha }\hat{P}_{a}e^{ i\alpha }\ket{\psi}=\bra{\psi}\hat{P}_{a}\ket{\psi}$ and after a measurement they collapse to states that again differ by only the factor $e^{ i\alpha }$, so they describe the same physical state and we are free to multiply by any state or any eigenvector, by a phase