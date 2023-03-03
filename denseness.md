# Denseness of $\\{m+\sqrt2n\mid n\in\mathbb N\\}$ in $\mathbb R$

Prove that the set $S\coloneqq\\{m+\sqrt2n\mid n\in\mathbb N\\}\subset\mathbb R$ is dense in $\mathbb R$.

*Proof:* Let $r=\sqrt 2-1$. Assume that $r\in(0,1)$ (without proof), so $\lim r^n=0$.

Define $a_n\coloneqq r^n$ ($n\in\mathbb N$). Binomial expansion tells us that $a_n\in S$ for any $n\in\mathbb S$.

Alternative: The [Dirichlet Approximation Theorem](https://en.wikipedia.org/wiki/Dirichlet%27s_approximation_theorem) states that for any $N\in\mathbb N$, there exists $p,q\in\mathbb N$ with $q\lt N$ such that
$$\left\lvert q\sqrt2-p\right\rvert\le\displaystyle\frac1N.$$
So basically, there is a rational number $p/q$ that approximates $\sqrt2$ really well (difference $\lt1/N^2$) with a small enough denominator.
