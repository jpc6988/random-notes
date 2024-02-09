# $\mathbb Z^n\not\simeq\mathbb Z^m$

Consider positive integers $n>m$. We claim that $\mathbb Z^n\not\simeq\mathbb Z^m$, where the power denotes the direct product of the additive group $\mathbb Z$. 

It is clear that the $n$ "unit vectors" $(1,0,\cdots,0)$, $(0,1,\cdots,0)$, $\cdots$, $(0,\cdots,0,1)$ generates $\mathbb Z^n$. To show that $\mathbb Z^n\not\simeq\mathbb Z^m$, we can show that the minimal generating set (in terms of cardinality) of $\mathbb Z^n$ must have $n$ elements.

Note that in an **abelian** group $G$, a subset set $\\{g_1,\cdots,g_k\\}\subseteq G$  generates the set
$$\\{g_1^{p_1}\cdots g_k^{p_k}\mid p_1,\cdots,p_k\in\mathbb Z\\}.$$

This helps since we can narrow down the specific form of this generated subgroup. We're ready to show the following:

**Proposition.** Let $n\in\mathbb Z_{>0}$. Then, any minimal generating set of $\mathbb Z^n$ has cardinality $n$.

*Proof.* We first show that any minimal generating set must have cardinality at least $n$. Suppose on the contrary that $\\{g^{(1)},\cdots,g^{(k)}\\}\subseteq\mathbb Z^n$ generates $\mathbb Z^n$, where $0\lt k\lt n$. Denote
```math
\begin{aligned}g^{(1)}&=(g^{(1)}_1,\cdots,g^{(1)}_n),\\&~~\vdots\\g^{(k)}&=(g^{(k)}_1, \cdots, g^{(k)}_n),\end{aligned}
```
where each $`g^{(i)}_j\in\mathbb Z`$. Then, for any $a=(a_1,\cdots,a_n)\in\mathbb Z^n$, there exist coefficients $p_1,\cdots,p_k\in\mathbb Z$ such that
$$\vec a=p_1\times_{\mathbb Z}\vec g^{(1)}+\cdots+p_k\times_{\mathbb Z}\vec g^{(k)}.$$

Let $A_{i,j}=\\{g^{(j)}_i\\}$ be a $n\times k$ (tall) matrix with integral entries. In this perspective, we would have $\text{range}~A\supset\mathbb Z^n$. We claim that this is impossible from our knowledge of matrices.

Indeed, viewed as a real matrix, the dimension of the domain of $A\colon\mathbb R^k\to\mathbb R^n$ is less than that of its range. The fundamental theorem of linear maps then implies that $\text{range}~A$ has dimension at most $k\lt n$. If the range contains $\mathbb Z^n$, then it must contain the $n$ unit vectors in particular. Because the range is a subspace, it must contain the span of the unit vectors, namely the entirety of $\mathbb R^n$ — a contradiction. Now, because the "unit vectors" generate $\mathbb Z^n$, this implies that the minimal generating set of $\mathbb Z^n$ has exactly $n$ elements. Q.E.D.

Now, the original claim is a direct corollary.

**Corollary.** If $n\ne m$ are positive integers, then $\mathbb Z^n\not\simeq\mathbb Z^m$. 

*Proof.* Because the minimal generating sets of $\mathbb Z^n$ and $\mathbb Z^m$ have different cardinality, it must be that $\mathbb Z^n\not\simeq\mathbb Z^m$.
