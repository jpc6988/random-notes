# Denseness of $\\{m+\sqrt2n\mid n\in\mathbb N\\}$ in $\mathbb R$

Prove that the set $S\coloneqq\\{m+\sqrt2n\mid n\in\mathbb N\\}\subset\mathbb R$ is dense in $\mathbb R$.

*Proof:* Let $r=\sqrt 2-1$. Assume that $r\in(0,1)$ (without proof), so $\lim r^n=0$. (Also, binomial expansion tells us that $r^n\in S$ for any $n\in\mathbb S$.)

## Old Idea

If (and only if) $S$ isn't dense in $\mathbb R$, then there'd be an interval $(x,y)$ that contains no numbers from $S$. My approach is to start from $a_1\coloneqq\lfloor x\rfloor\le x$. Then, inductively define
$$a_{n+1}=a_n+r^{k_n}\quad(n\in\mathbb N),$$
where $r^{k_n}\in\mathbb N$ takes on the largset value that still makes $a_{n+1}\lt y$; that is,
$$k_n\coloneqq\max\\{\kappa\in\mathbb N\mid a_n+r^\kappa\lt y\\},$$
which can always be chosen since $r^n$ can get arbitrarily small for big enough $n$.

Clearly, $(a_n)$ is strictly increasing, bounded from below (by $a_1$), and bounded from above (by $y$), so it has to converge to some number $\ell\in[a_1,y]$. I just realized that since it's a limit, there's no guarantee that $\ell\in S$!

This is almost feels like computing a division by hand: if I do $5\div 3$, I'd first get $1$ which is the largset number such that $1\cdot 3<5$. And then we keep doing the same thing to the remainder. I feel like this *could* work but still kind of challenging.

<!-- 
## New Idea

What if I could consider the $(k-1)$-tail of the partial sums of $r^n$?

Define $\tilde S_n\coloneqq r^n+r^{n+1}+\cdots$ for $n\in\mathbb N$. Note that $\lvert\tilde S_n\rvert\lt\infty$ as a geometric series for any $n\in\mathbb N$. In fact, I can say that $S$ a ring  $\lim \tilde S_n=0$ too. -->

Alternative: The [Dirichlet Approximation Theorem](https://en.wikipedia.org/wiki/Dirichlet%27s_approximation_theorem) states that for any $N\in\mathbb N$, there exists $p,q\in\mathbb N$ with $q\lt N$ such that
$$\left\lvert q\sqrt2-p\right\rvert\le\displaystyle\frac1N.$$
So basically, there is a rational number $p/q$ that approximates $\sqrt2$ really well (difference $\lt1/N^2$) with a small enough denominator.

## ChatGPT's "Proof" 😳

At least it tried 😂

Me: "prove that the set $\\{ m + \sqrt{2} n \mid  m, n ~\rm integers \\}$ is dense is $\mathbb R$."

ChatGPT: "This is a great problem in real analysis! Here's an outline of a proof to get you started:

"First, we can observe that the set $\\{ m + \sqrt{2} n \mid m, n \in \mathbb{Z} \\}$ is not empty. For example, $0 = 0 + \sqrt{2} \cdot 0$ is in the set.

"Next, we need to show that for any $x \in \mathbb{R}$ and any $\epsilon > 0$, there exists an element of the set that is within $\epsilon$ of $x$.

"To do this, fix $x \in \mathbb{R}$ and $\epsilon > 0$. Consider the interval $[x-\epsilon, x+\epsilon]$. We need to find an element of the form $m+\sqrt{2}n$ that lies in this interval.

"We know that there exist integers $p$ and $q$ such that $|x-(p+\sqrt{2}q)| \leq \frac{1}{2\epsilon}$. This is a consequence of the fact that the set ${ p+\sqrt{2}q \mid p, q \in \mathbb{Z} }$ is dense in $\mathbb{R}$.

"Now, we can use the fact that $\sqrt{2}$ is irrational to show that we can find integers $m$ and $n$ such that $|p-m| \leq 1$ and $|q-n| \leq 1$. This is because the set $\{ p+\sqrt{2}q \mid p, q \in \mathbb{Z} \}$ is not only dense, but also has no repeated elements, since $\sqrt{2}$ is irrational.

"Putting this all together, we have:

$$\begin{align*}
|m+\sqrt{2}n - x| &= |(m-p) + \sqrt{2}(n-q)| \\
&\leq |m-p| + \sqrt{2} |n-q| \\
&\leq \sqrt{2} (|m-p|+|q-n|) \\
&\leq \sqrt{2} \cdot 2 \\
&= 2\sqrt{2} < \epsilon
\end{align*}$$
"Therefore, there exists an element $m+\sqrt{2}n$ of the form we are considering that lies within $\epsilon$ of $x$. This proves that the set is dense in $\mathbb{R}$."

