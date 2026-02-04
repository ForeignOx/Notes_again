A vector triple product is defined to be 
$$
\underline{a}\times (\underline{b}\times \underline{c})
$$
## Bac of Cab Identity
$$
\underline{a}\times(\underline{b}\times \underline{c})=\underline{b}(\underline{a}\cdot \underline{c})-\underline{c}(\underline{a}\cdot \underline{b})
$$
### Proof
$$
\underline{b}\times \underline{c}=(b_{2}c_{3}-b_{3}c_{2})\underline{e}_{1}+(b_{3}c_{1}-b_{1}c_{3})\underline{e}_{2}+(b_{1}c_{2}-b_{2}c_{1})\underline{e}_{3}
$$
So
$$
\underline{a}\times(\underline{b}\times \underline{c})=\det \begin{pmatrix}
\underline{e}_{1} & \underline{e}_{2} & \underline{e}_{3} \\
a_{1} & a_{2} & a_{3} \\
b_{2}c_{3}-b_{3}c_{2} & b_{3}c_{1}-b_{1}c_{3} & b_{1}c_{2}-b_{2}c_{1}
\end{pmatrix}
$$
$$
= \underline{e}_{1}(a_{2}b_{1}c_{2}-a_{2}b_{2}c_{1}-a_{3}b_{3}c_{1}+a_{3}b_{1}c_{3})
$$
$$
 +\underline{e}_{2}(a_{3}b_{2}c_{3}-a_{3}b_{3}c_{2}-a_{1}b_{1}c_{2}+a_{1}b_{2}c_{1})
$$
$$
 +\underline{e}_{3}(a_{1}b_{3}c_{1}-a_{1}b_{1}c_{3}-a_{2}b_{2}c_{3}+a_{2}b_{3}c_{2})
$$
$$
= b_{1}\underline{e}_{1}(a_{2}c_{2}+a_{3}c_{3})-c_{1}\underline{e}_{1}(a_{2}b_{2}+a_{3}b_{3})
$$
$$
 +b_{2}\underline{e}_{2}(a_{3}c_{3}+a_{1}c_{1})-c_{2}\underline{e}_{2}(a_{3}b_{3}+a_{1}b_{1})
$$
$$
 +b_{3}\underline{e}_{3}(a_{1}c_{1}+a_{2}c_{2})-c_{3}\underline{e}_{3}(a_{1}b_{1}+a_{2}b_{2})
$$
### Proof with [[Index Notation|Index Notation]]
Use index notation to prove that $\underline{a}\times(\underline{b}\times \underline{c})=(\underline{a}\cdot \underline{c})\underline{b}-(\underline{a}\cdot \underline{b})\underline{c}$:
The $i$th component of the left hand side is:
$$
[\underline{a}\times(\underline{b}\times \underline{c})]_{i}=\epsilon_{ijk}a_{j}[\underline{b}\times \underline{c}]_{k}
$$
$$
= \epsilon_{ijk}a_{j}(\epsilon_{klm}b_{l}c_{m})
$$
$$
= \epsilon_{ijk}\epsilon_{klm}a_{j}b_{l}c_{m}
$$
$$
= (\delta_{il}\delta_{jm}-\delta_{im}\delta_{jl})a_{j}b_{l}c_{m}
$$
$$
= \delta_{il}\delta_{jm}a_{j}b_{l}c_{m}-\delta_{im}\delta_{jl}a_{j}b_{l}c_{m} 
$$
$$
= \delta_{il}a_{j}b_{l}c_{j}-\delta_{jl}a_{j}b_{l}c_{i}
$$
$$
= a_{j}b_{i}c_{j}-a_{j}b_{j}c_{i}
$$
$$
= (\underline{a}\cdot \underline{c})b_{i}-(\underline{a}\cdot \underline{b})c_{i}=[(\underline{a}\cdot \underline{c})\underline{b}-(\underline{a}\cdot \underline{b})\underline{c}]_{i}
$$
