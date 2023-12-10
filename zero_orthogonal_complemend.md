# When is $U^\perp=0$?

We first look at a specific example from MATH 436 and examine the technique, before diving in to greater generality.

**Proposition 1**. Suppose $V=C^0([0,1])$ is the inner product space of continuous functions from $[0,1]$ to $\mathbb R$ with
$$\langle f,g\rangle=\int_0^1f(x)g(x)\\,\mathrm dx.$$
Let $U=\mathcal P(\mathbb R)$ be the subspace of polynomials with domain restricted to $[0,1]$. Then, $U^\perp=\{0\}$.

**Hint (Stone-Weierstrass).** Suppose $f$ is a continuous real-valued function defined on the real interval $[a,b]$. For every $\epsilon\gt0$, there exists a polynomial $p\in\mathcal P(\mathbb R)$ such that $\Vert f-p\Vert_\infty\lt\epsilon$.

*Proof.* We first show that we can replace the supremum norm $\Vert\cdot\Vert_\infty$ in the hint with the norm induced by $\langle\cdot,\cdot\rangle$. Indeed, having fixed $p$ by the hint given $f$ and $\epsilon$ with $\Vert f-p\Vert_\infty\lt\epsilon$, we have
```math
$$\Vert f-p\Vert=\sqrt{\int_0^1|f(x)-p(x)|^2\\,\mathrm dx}\lt\sqrt{\int_0^1\epsilon^2\\,\mathrm dx}=\epsilon.$$
```

It is trivial that $0\in U^\perp$, and we now show $f\notin U^\perp$ for any $f\in V\backslash\{0\}$. Let $a=\Vert f\Vert\gt0$ and fix $p\in U$ such that $\Vert f-p\Vert\lt a/2$. Then, 
```math
$$\begin{aligned}|\langle f,p\rangle|&=|\langle f,p+f-f\rangle|\\&\ge|\langle f,f\rangle|-|\langle f,f-p\rangle|\\&\ge\Vert f\Vert^2-\Vert f\Vert\cdot\Vert f-p\Vert\\&\ge a\cdot(a-a/2)\\&=a^2/2\gt0.\end{aligned}$$
```
Because $f$ is arbitrarily chosen, this implies the only element in $U^\perp$ is 0. Q.E.D.
