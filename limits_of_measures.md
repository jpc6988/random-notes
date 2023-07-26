# On the Continuity Properties of the Cumulative Distribution Function

**Property 4.10.2:** Suppose $F\colon\mathbb R\to\mathbb R$ is the CDF of a real-valued random variable. Then, $\lim_{b\to\infty}F(b)=1$.

The [textbook](https://github.com/yaduvanshirishi/GATE-CSE/blob/master/A-First-Course-in-Probability-8th-Edition.pdf) implicitly uses the following fact to prove this property, requiring a "weaker" sequential condition to establish the limit at $+\infty$:

**Proposition 1:** Suppose that $f(x_n)$ tends to $L\in\mathbb R$ for any *non-decreasing* real sequence $\\{x\_n\\}\_{n=1}^\infty$ that tends to $+\infty$. Then, $\lim_{x\to\infty}F(x)$ exists and equals $L$.

This contrasts the typical sequential characterization, which is established for metric spaces, _without an order on the space to talk about monotonicity_. Of course, here we consider the compatified domain $\mathbb R^\*=\mathbb R\cup\\{-\infty,+\infty\\}$ (which justifies the use of Bolzano–Weierstrass in my proof). The more common statement is as follows:

**Proposition 2:** Suppose $f(x_n)$ tends to $L\in\mathbb R$ for any real sequence $\\{x_n\\}_{n=1}^\infty$ that tends to $+\infty$ (which needs not be monotone). Then, $\lim\_{x\to\infty}F(x)$ exists and equals $L$.

I was previously confused in class since I didn't know this fact. I've also tried checking "Baby Rudin," but with no luck. I do vaguely recall this being an exercise when I took MATH 401 at Harrisburg, and I have attempted a proof as follows:

_Proof:_ We first suppose for the sake of contradiction that $\lim_{x\to\infty}f(x)$ does not exist. We therefore fix a particular $\epsilon\gt0$ such that for any $X\in\mathbb R$, there exists some $x>X$ for which $|f(x)-L|\ge\epsilon$. We now construct a sequence $\\{x^\*\_n\\}\_{n=1}^\infty$ as follows: for each $n\in\mathbb N$, set $X\coloneqq n$ and choose a particular $x^\*\_n>X=n$ such that $|f(x^\*\_n)-L|\ge\epsilon$. We use the Bolzano–Weierstrass theorem to extract a subsequence $\\{x^\*\_{n\_k}\\}\_{k=1}^\infty$ that tends to the limit superior $+\infty$ (since $\\{x^\*\_n\\}>\\{n\\}$ is unbounded). However, $\\{x^\*\_{n\_k}\\}$ never intersects the $\epsilon$-neighborhood of $L$ by construction, which contradicts the given condition that implies $f(x^\*\_{n\_k})\to L$. Thus, $\lim_{x\to\infty}f(x)$ exists.

Then, the continuous limit equals any sequential limit. Consider an arbitrary non-decreasing sequence $\\{x\_n\\}\_{n=1}^\infty$ that tends to $+\infty$, for which we are given that $f(x\_n)\to L$. Then the continuous limit must equal $L$. Q.E.D.
