## Lemma
Let [[Complex Functions|$f:U\to \mathbb{C}$]] be [[Holomorphicity|holomorphic]] on an [[open sets|open set]] $U$, then for any triangular region $\triangle \subset U$ (inside and boundary), then we have
$$
\int _{\partial\triangle}f(z) \, dz =0
$$
### Proof
Let $\triangle$ be a triangular region on which $f$ is holomorphic. Divide $\triangle$ into four smaller triangular regions $\triangle_{1},\triangle_{2},\triangle_{3},\triangle_{4}$ by considering the straight line that connect the midpoints of the sides bounding triangle $\partial\triangle$
![[Pasted image 20260220021621.png]]
We obtain, using properties of [[Contour Integration|contour integrals]]
$$
    \int _{\partial\triangle } f(z) \, dz=\sum_{i=1}^{4}\int _{\partial\triangle_{i}}f(z) \, dz  
$$
Since the sids of the smaller internal triangle are traversed twice in opposite directions by the contours (and this means their integral contribution cancels ou)