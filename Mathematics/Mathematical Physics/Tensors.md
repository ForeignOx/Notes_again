## Build Up for Special Relativity
We have defined vectors $V^{\mu}$ where
$$
V^{\mu'}=\Lambda^{\mu}_{~ ~\nu}V^{\mu}
$$
And covectors $V_{\mu}$, where
$$
V_{\mu}=V_{\mu'}=\Lambda_{\mu}^{~ ~\nu}V_{\nu}
$$
Where
$$
\Lambda_{\mu}^{~ ~\nu}=\eta_{\mu\rho}\eta^{\nu\sigma}\Lambda^{\rho}_{~ ~\sigma}
$$
And also $\Lambda_{\mu}^{~ ~\nu}\Lambda^{\mu}_{~ ~\sigma}=\delta^{\nu}_{\sigma}$
We can generalise this to an object with $m$ vector and $n$ covector indices
$$
T^{\mu_{1}\mu_{2}\dots \mu_{m}} \,_{\nu_{1}\nu_{2}\dots \nu_{n}}
$$
Is a tensor of the type ${m \choose n }$
This is a tensor as it satisfies transformation property
$$
T^{\mu_{1}'\mu_{2}'\dots \mu_{m}'}\,_{\nu_{1}'\nu_{2}'\dots \nu_{n}'}=\Lambda^{\mu_{1}}\,_{\alpha_{1}}\dots \Lambda^{\mu_{m}}\,_{\alpha_{m}}\Lambda_{\nu_{1}}\,^{\beta_{1}}\dots\Lambda_{\nu_{n}}\,^{\beta_{n}}T^{\alpha_{1}\dots\alpha_{m}}\,_{\beta_{1}\dots\beta_{n}}
$$
In $d$ dimensions, an ${m \choose n }$ tensor has $d^{m+n}$ independent components
Vectors are ${1 \choose 0 }$ tensors, covectors are ${0 \choose 1 }$ tensors, scalar functions are ${0 \choose 0 }$ tensors
## Example
For any two vectors $V^{\mu},W^{\nu}$, then
$$
M^{\mu \nu}=V^{\mu}W^{\nu}
$$
Is a ${2 \choose 0 }$ tensor, we can check how it transforms:
$$
M^{\mu'\nu'}=V^{\mu'}W^{\nu'}=(\Lambda^{\mu}\,_{\rho}V^{\rho})(\Lambda^{\nu}\,_{\sigma}W^{\sigma})=\Lambda^{\mu}\,_{\rho}
$$
## Definition
A tensor is an object that transforms like a tensor