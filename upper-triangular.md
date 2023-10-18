# Some Notes on Upper Triangular Matrix.

We have this useful piece of machinery.

**Proposition.** Let $V$ be a finite-dimensional vector space and $T\in\mathcal L(V)$. Then, for any basis $v_1,\cdots,v_n$ of $V$, $\mathcal M(T)$ is upper triangular if and only if $T(v_k)\in\text{span}(v_1,\cdots,v_k)$ for any $k=1,\cdots,n$.

Here's an easier proof for the last half of the result from class.

**(Part of) Theorem.** Let $V$ be a finite-dimensional vector space and suppose that $\mathcal M(T)$ is upper triangular for some basis $v_1,\cdots,v_n$ of $V$. If any diagonal element $\lambda_k=0$, then $T$ is not invertible.

*Proof.* Because $\textcolor{red}{\lambda_k=0}$, we have

$$\begin{align}T(v_1)&\in\text{span}(v_1)\\
T(v_2)&\in\text{span}(v_1,v_2)\\
&~~\vdots\\
T(v_{k-1})&\in\text{span}(v_1,\cdots,{v_{k-1}})\\
T(v_k)&\in\text{span}(v_1,\cdots,\textcolor{red}{v_{k-1}}).\end{align}$$

So, we have $k$ vectors, $T(v_1),\cdots,T(v_k)$, in a $(k-1)$-dimensional subspace $\text{span}(v_1,\cdots,v_{k-1})$, which must be linearly dependent. 

We also know that injective maps take LI vectors to LI vectors. But now, $v_1,\cdots,v_k$ is LI while $T(v_1),\cdots,T(v_k)$ is LD, so $T$ cannot be injective, and thus it is not invertible.
