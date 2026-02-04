The potential, $V$, at a point $P$ in an [[Electric Fields|electric field]] is the [[Work]] done by the field per unit [[Electric Charge|charge]] on a test charge as it goes from $P$ to infinity. The potential due to a point charge, $Q$ at distance $r$ from $Q$ is:
$$
V=\frac{Q}{4\pi\epsilon_{0}r}
$$
## Derivation
Recall that work is force multiplied by distance in direction of force. The force on $q$ is $qE$, radially outwards from $Q$. But $E$ decreases as we go from $P$ to infinity, this is because:
$$
E=\frac{Q}{4\pi \epsilon_{0}r^{2}}
$$
 We can therefore calculate the work done in small steps at a time, with distance $\delta r$, and we can see that that the work done on $q$ as $q$ moves a distance $\delta r$ from $Q$ is equal to:
 $$
W=\int_{r_{P}}^{\infty} qE \, dr =\frac{qQ}{4\pi\epsilon_{0}}\int _{r_{P}}^{\infty} \frac{1}{r^{2}} \, dr 
$$
$$
=\frac{qQ}{4\pi\epsilon_{0}}\left[ -\frac{1}{r} \right]_{r_{P}}^{\infty}=\frac{qQ}{4\pi\epsilon_{0}}\left( 0-\left( -\frac{1}{r_{P}} \right) \right)
$$
The limits in the above integration have been ignored
$$
=\frac{qQ}{4\pi\epsilon_{0}r_{P}}
$$
Which can be generalised to
$$
W=\frac{qQ}{4\pi\epsilon_{0}r}
$$
And since the potential is the work done per unit charge,
$$
V=\frac{Q}{4\pi\epsilon_{0}r}
$$
## More than one charge
In principle we can calculate the electric potential due to any spatial distribution of charges by viewing the charge distribution as a collection of point charges, calculating $V$ at $P$ due to each point charge and adding them as scalars

#Physics #Fields #Equation #Definition