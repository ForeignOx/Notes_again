A key feature of observing the motion of fluids, is to consider that we need to view things in different perspectives
![[Pasted image 20261006102820.png]]Consider the above, it is strange how the fluid is accelerating despite the flow being steady. It turns out there are two ways of describing the velocity $\underline{u}$ of a fluid:
### Eulerian Description
Perhaps the most intuitive option is to pick fixed point $\underline{x}$ and ask for the velocity of the fluid particle there at time $t$. The velocity is given by $\underline{u}=\underline{u}(\underline{x},t)$ which answers the question:
"What is the velocity at time $t$ of the fluid particle that is currently at $\underline{x}$"
Here we would describe the above as a steady flow, defined by
$$
\frac{ \partial \underline{u} }{ \partial t } =0
$$
### Lagrangian Description
The other option is to pick a fluid particle at a fixed point $\underline{a}$ and keep track of this particle as it moves in time. The velocity of the fluid is therefore given by $\underline{\tilde{u}}=\underline{\tilde{u}}(\underline{a},t)$, which answers the question:
"What is the velocity at time $t$ of the fluid particle that started at $\underline{a}$"
Thias is useful as it allows us to use ideas from classical mechanics. This means that it is easy to say things like density is conserved by each particle