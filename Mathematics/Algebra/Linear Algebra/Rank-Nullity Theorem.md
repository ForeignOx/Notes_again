Suppose $V$ and $W$ are finite dimensional [[Vectorspaces|vectorspaces]], and [[Linear Maps|$T:V\to W$]] is linear, then the [[Kernel|nullity]] and [[Image|rank]] are related to the [[Dimension|dimension]] of $V$ like so:
$$
\text{rk}(T)+\text{null}(T)=\dim(V)
$$
## Proof
Let $\{ \underline{u}_{1},\dots,\underline{u}_{s} \}$ be a [[Basis|basis]] for $\text{ker}(T)$, and $\{ \underline{w}_{1},\dots,\underline{w}_{t} \}$ be a sbasis for $\text{im}(T)$, and suppose $\{ \underline{v}_{1},\dots,\underline{v}_{t} \}\subseteq V$ with $T(\underline{v}_{i})=\underline{w}_{i}$ for all $i$, then we are claiming $\{ \underline{u}_{1},\dots,\underline{u}_{s},\underline{v}_{1},\dots,\underline{v}_{t} \}$ is a basis for $V$. If the claim is true, we have $\text{rk}(T)+\text{null}(T)=t+s=\dim(V)$
To prove the claim we need to first check it is [[Linear Span|spanning]]:
Suppose $\underline{v}\in V$, then $\exists\lambda_{i}$ such that 
$$
\text{im}(T)\ni T(\underline{v})=\lambda_{1}\underline{w}_{1}+\dots+\lambda_{t}\underline{w}_{t}=T(\lambda_{1}\underline{v}_{1}+\dots+\lambda_{t}\underline{v}_{t})
$$
So we see
$$
T(\underline{v}-\lambda_{1}\underline{v}_{1}-\dots-\lambda_{t}\underline{v}_{t})=\underline{0}
$$
So $\underline{v}-\lambda_{1}\underline{v}_{1}-\dots-\lambda_{t}\underline{v}_{t}$ is in the kernel of $T$, so $\exists \mu_{j}$ with
$$
\underline{v}-\lambda_{1}\underline{v}_{1}-\dots-\lambda_t\underline{v}_{t}=\mu_{1}\underline{u}_{1}+\dots+\mu_{s}\underline{u}_{s}
$$
So
$$
\underline{v}=\lambda_{1}\underline{v}_{1}+\dots+\lambda_{t}\underline{v}_{t}+\mu_{1}\underline{u}_{1}+..+\mu_{s}\underline{u}_{s}
$$
So we have spanning, next we need [[Linear Independence|linear independence]]
Suppose
$$
\lambda_{1}\underline{v}_{1}+\dots+\lambda_{t}\underline{v}_{t}+\mu_{1}\underline{u}_{1}+\dots+\mu_{s}\underline{u}_{s}=\underline{0}
$$
By applying $T$:
$$
\lambda_{1}\underline{w}_{1}+\dots+\lambda_{t}\underline{w}_{t}+\underline{0}+\dots+\underline{0}=T(\underline{0})=\underline{0}
$$
So we must have $\lambda_{1}=\dots=\lambda_{t}=0$, since $\underline{w}_{i}$s formed a basis, so the original equation becomes:
$$
\mu_{1}\underline{u}_{1}+\dots+\mu_{s}\underline{u}_{s}=\underline{0}
$$
So since the $\underline{u}_{i}$'s also formed a basis, $\mu_{1}=\dots=\mu_{s}=0$, hence linearly independent 
$W^{5}$

#Mathematics #LinAlg #Theorem 