In a lot of contexts, the eigenvalues describe a spectrum
## Theorem
A Hermitian operator $\hat{A}$ with distinct [[eigenvalues|eigenvalues]] $a_{1},\dots,a_{m}$ can be written:
$$
\hat{A}=\sum_{k=1}^{m}a_{k} \hat{P}_{a_{k}}
$$
Where $\hat{P}_{a_{k}}$ are the [[projectors|projectors]] onto eigenspace of $a_{k}$
### Proof
For any vector $\psi$, we have $\hat{P}_{a_{k}}\ket{\psi}$ is in the $a_{k}$ eigenspace, so $\hat{A}\hat{P}_{a_{k}}\ket{\psi}=a_{k}\hat{P}_{a_{k}}\ket{\psi}$, so for any $\ket{\psi}$, 
$$
\hat{A}\ket{\psi}=\hat{A}\mathbb{1}\ket{\psi}=\hat{A}\sum_{k=1}^{m}\hat{P}_{a_{k}}\ket{\psi} =\sum_{k=1}^{m}\hat{A}\hat{P}_{a_{k}}\ket{\psi} =\sum_{k=1}^{m}a_{k}\hat{P}_{a_{k}}\ket{\psi} 
$$
$W^{5}$
