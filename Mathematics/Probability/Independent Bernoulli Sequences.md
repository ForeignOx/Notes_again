For a Borel set $A\in\mathcal{B}[0,1)$, define
$$
\rho_{A}(\omega):=\mathbb{1}_{A}(\omega)-\mathbb{1}_{A^{c}}(\omega)\equiv2\mathbb{1}_{A}(\omega)-1
$$
We need the following general result:
## Lemma
For integer $n>1$, let $\left\{ A_{k} \right\}_{k=1}^{n}$ be [[Events|events]] in the [[Canonical Probability Space|canonical probability space]] $([0,1),\mathcal{B}[0,1),\mathbb{P})$ each having the same probability $\mathbb{P}(A_{k})=\frac{1}{2}$
Then the events $\left\{ A_{k} \right\}_{k=1}^{n}$ are mutually independent iff
$$
\forall \mathcal{J}\subseteq \left\{ 1,\dots,n \right\},\emptyset\neq \mathcal{J}\implies \mathbb{E}\left( \prod_{\ell \in \mathcal{J}}\rho_{A_{\ell}} \right)=0
$$
### Proof
Let the events $\left\{ A_{k} \right\}_{k=1}^{n}$ be mutually independent. Then for each index subset $\mathcal{I}\subseteq \left\{ 1,\dots,n \right\}$, the intersection has probability
$$
\mathbb{P}\left( \bigcap_{\ell \in  \mathcal{I}}A_{\ell} \right)=2^{-\left| \mathcal{I} \right| }
$$
Equivalently,
$$
\mathbb{E}\left( \prod_{\ell \in \mathcal{I}}2\mathbb{1}_{A_{\ell}} \right)=2^{\left| \mathcal{I} \right| }\mathbb{E}\left( \mathbb{1}_{\bigcap_{\ell \in \mathcal{I}}A_{\ell}} \right)=1
$$
As a result, and by the property of Borel sets,
$$
\mathbb{E}\left( \prod_{\ell \in \mathcal{J}} \rho_{A_{\ell}} \right)=\mathbb{E}\left( \sum_{\mathcal{I}\subseteq \mathcal{J}} (-1)^{\left| \mathcal{J} \right|-\left| \mathcal{I} \right|  }\prod_{\ell \in \mathcal{I}}(2\mathbb{1}_{A_{\ell}}) \right) = \sum_{\mathcal{I}\subseteq \mathcal{J}}(-1)^{\left| \mathcal{J} \right|-\left| \mathcal{I} \right|  }\mathbb{E}\left( \prod_{\ell \in  \mathcal{I}}(2\mathbb{1}_{A_{\ell}}) \right)=\sum_{\mathcal{I}\subseteq \mathcal{J}}(-1)^{\left| \mathcal{J} \right|-\left| \mathcal{I} \right|  }
$$
Where the last sum is just:
$$
\sum_{\left| \mathcal{I} \right| =0}^{\left| \mathcal{J} \right| }{\left| \mathcal{J} \right|  \choose \left| \mathcal{I} \right|  }(-1)^{\left| \mathcal{J} \right| -\left| \mathcal{I} \right| } \cdot 1^{\left| \mathcal{I} \right| }=(1-1)^{\left| \mathcal{J} \right| }=0
$$
For the converse, assume the condition holds, we want to show the sets are independent
Foir each index subset $\mathcal{J}\subseteq \left\{ 1,\dots,n \right\}$, we get
$$
2^{\left| \mathcal{J} \right| }\mathbb{E}\left( \mathbb{1}_{\bigcap_{\ell \in \mathcal{J}}A_{\ell}} \right)=\mathbb{E}\left( \prod_{\ell \in \mathcal{J}}(2\mathbb{1}_{A_{\ell}}) \right)\equiv \mathbb{E}\left( \prod_{\ell \in \mathcal{J}}(\rho_{A_{\ell}}+1) \right)
$$
$$
 =\mathbb{E}\left( \sum_{\mathcal{I}\subseteq \mathcal{J}}\prod_{\ell \in \mathcal{I}}\rho_{A_{\ell}} \right)=1+\sum_{\emptyset\neq \mathcal{I}\subseteq \mathcal{J}}\mathbb{E}\left( \prod_{\ell \in \mathcal{I}}\rho_{A_{\ell}} \right)=1
$$
And so the intersection $\bigcap_{\ell \in\mathcal{J}}~A_{\ell}$ has probability $2^{-\left| \mathcal{J} \right|}$; equivalently, the sets $\left\{ A_{\ell} \right\}_{\ell \in \mathcal{J}}$

