We can see from graphs that this appears to be true
![[Every Convergent Sequence is Bounded 2024-07-07 19.40.23.excalidraw]]
Note tht by the [[Contrapositive Proof|contrapositive]], an unbounded sequence is divergent
## Proof
If $a_{n}$ is a [[Convergence|convergent]] [[Sequences|sequence]] with limit $l$, then:
$$
\forall\varepsilon>0\exists N_{\varepsilon}:n\geq N_{\varepsilon}\implies \left| a_{n}-l \right|<\varepsilon
$$
So consider $\varepsilon>0$, $N_{\varepsilon}$ exists and if $n\geq N_{\varepsilon}$ then
$$
\left| a_{n}-l \right|<\varepsilon 
$$
$$
\implies -\varepsilon<a_{n}-l<\varepsilon 
$$
$$
\implies l-\varepsilon<a_{n}<l+\varepsilon 
$$
$$
\implies \left| a_{n} \right|<max(\left| l-\varepsilon \right|,\left| l+\varepsilon \right|)
$$
So $a_{n}$ is [[Boundedness|bounded]]
If $n<N_{\varepsilon}$, then $a_{n}$ forms a finite set, so $\left| a_{n} \right|\leq |a_{i}|$ for some $i<N_{\varepsilon}$ and $i \in\mathbb{N}$, so it is bounded
So if $M=max(\left| l-\varepsilon \right|,\left| l+\varepsilon \right|,\left| a_{i} \right|)$
then $\left| a_{n} \right|\leq M$ so $a_{n}$ is bounded
## Proposition: Every bounded sequence is convergent
This is not true, as we can consider $a_{n}=(-1)^{n}$
$$
\left| a_{n} \right|=1
$$
$$
\implies \left| a_{n} \right|<2
$$
So $a_{n}$ is bounded, but $a_{n}$ is not convergent

#Mathematics #Analysis #Theorem 