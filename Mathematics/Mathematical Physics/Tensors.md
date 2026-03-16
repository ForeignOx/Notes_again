## Definition
A tensor is an object that transforms like a tensor
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
## Examples
For any two vectors $V^{\mu},W^{\nu}$, then
$$
\eta^{\mu \nu}=V^{\mu}W^{\nu}
$$
Is a ${2 \choose 0 }$ tensor, we can check how it transforms:
$$
\eta^{\mu'\nu'}=V^{\mu'}W^{\nu'}=(\Lambda^{\mu}\,_{\rho}V^{\rho})(\Lambda^{\nu}\,_{\sigma}W^{\sigma})=\Lambda^{\mu}\,_{\rho}\Lambda^{\nu}\,_{\sigma}V^{\rho}W^{\sigma} =\Lambda^{\mu}\,_{\rho}\Lambda^{\nu}\,_{\sigma}\eta^{\rho\sigma}
$$
___
For any vector $V^{\mu}$ and covector $W_{\nu}$, then
$$
\eta^{\mu}\,_{\nu}=V^{\mu}W_{\nu}
$$
Is a ${1 \choose  1}$ tensor
We can check it satisfies transformation:
$$
\eta^{\mu'}\,_{\nu'}=V^{\mu'}W_{\nu'}=(\Lambda^{\mu}\,_{\rho}V^{\rho})(\Lambda_{\nu}\,^{\sigma}W_{\sigma})=\Lambda^{\mu}\,_{\rho}\Lambda_{\nu}\,^{\sigma}V^{\rho}W_{\sigma}=\Lambda^{\mu}\,_{\rho}\Lambda_{\nu}\,^{\sigma}\eta^{\rho}\,_{\sigma}
$$
___
For any vector field $W^{\mu},\eta_{\nu}\,^{\mu}=\partial_{\nu}W^{\mu}$ is a ${1 \choose 1 }$ tensor, again we check transformation:
$$
\eta_{\nu'}\,^{\mu'}=\partial_{\nu'}W^{\mu'}=\Lambda_{\nu}\,^{\rho}\partial_{\rho}(\Lambda^{\mu}\,_{\sigma}W^{\sigma})=\partial_{\nu}W^{\mu}
$$
## Properties of Tensors
- The sum of two ${m \choose n }$ tensors is a tensor of the same type
- The product of a ${m_{1} \choose n_{1} }$ and a ${m_{2} \choose n_{2} }$ tensor is a ${m_{1}+m_{2} \choose n_{1}+n_{2} }$
- Raising (or lowering) and index of an ${m \choose n }$ tensor produces a ${m+1 \choose n-1 }$ for raising and a ${m-1 \choose n+1 }$ tensor for lowering
- The partial derivative of an ${m \choose n }$ tensor produces a ${m \choose n+1 }$ tensor
- If a tensor is equal to zero in one frame, then it is equal to zero in all frames
___
The previous examples exploit the second and fifth properties
We can also see an example for the fourth, it makes a contraction for a ${1 \choose 2 }$ tensor $T^{\alpha}\,_{\beta\gamma}$
Here tere are two possible contractions $T^{\alpha}\,_{\alpha\gamma}$ or $T^{\alpha}\,_{\beta\alpha}$
Picking $V_{\gamma}=T^{\alpha}\,_{\alpha\gamma}$ and show that it transforms like a $(0,1)$ tensor
$$
V_{\gamma'}=T^{\alpha'}\,_{\alpha'\gamma'}=(\Lambda^{\alpha'}\,_{\rho}\Lambda_{\alpha'}\,^{\sigma})\Lambda_{\gamma'}\,^{\tau}T^{\rho}\,_{\sigma \tau} 
$$
$$
= \delta_{\rho}^{\sigma}\Lambda_{\gamma}\,^{\tau}T^{\rho}\,_{\sigma \tau}=\Lambda_{\gamma}\,^{\tau}T^{\rho}\,_{\sigma \tau}=\Lambda_{\gamma}\,^{\tau}V_{\tau}
$$

