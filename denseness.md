# Denseness of $\\{m+\sqrt2n\mid n\in\mathbb N\\}$ in $\mathbb R$

Prove that the set $S\coloneqq\\{m+\sqrt2n\mid n\in\mathbb N\\}\subset\mathbb R$ is dense in $\mathbb R$.

*Proof:* Let $r=\sqrt 2-1$. Assume that $r\in(0,1)$ (without proof), so $\lim r^n=0$. (Also, binomial expansion tells us that $r^n\in S$ for any $n\in\mathbb S$.)

## Old Idea

If (and only if) $S$ isn't dense in $\mathbb R$, then there'd be an interval $(x,y)$ that contains no numbers from $S$. My approach is to start from $a_1\coloneqq\lfloor x\rfloor\le x$. Then, inductively define
$$a_{n+1}=a_n+r^{k_n}\quad(n\in\mathbb N),$$
where $r^{k_n}\in\mathbb N$ takes on the largset value that still makes $a_{n+1}\lt y$; that is,
$$k_n\coloneqq\max\\{\kappa\in\mathbb N\mid a_n+r^\kappa\lt y\\},$$
which can always be chosen since $r^n$ can get arbitrarily small for big enough $n$.

Clearly, $(a_n)$ is strictly increasing, bounded from below (by $a_1$), and bounded from above (by $y$), so it has to converge to some number $\ell\in[a_1,y]$.

Basically, this is almost like computing a division by hand: if I do $5/3$, I'd first get $1$ which is the largset number such that %1\cdot 3<5$. And then we keep doing the same thing to the remainder. I feel like this could work but still kind of challenging.

## New Idea

What if I could consider the $(k-1)$-tail of the partial sums of $r^n$?

Define $\tilde S_n\coloneqq r^n+r^{n+1}+\cdots$ for $n\in\mathbb N$. Note that $\lvert\tilde S_n\rvert\lt\infty$ as a geometric series for any $n\in\mathbb N$.

Alternative: The [Dirichlet Approximation Theorem](https://en.wikipedia.org/wiki/Dirichlet%27s_approximation_theorem) states that for any $N\in\mathbb N$, there exists $p,q\in\mathbb N$ with $q\lt N$ such that
$$\left\lvert q\sqrt2-p\right\rvert\le\displaystyle\frac1N.$$
So basically, there is a rational number $p/q$ that approximates $\sqrt2$ really well (difference $\lt1/N^2$) with a small enough denominator.
