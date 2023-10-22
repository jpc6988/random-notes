# How to Find (All) Eigenvalues and Eigenvectors, Rigorously

We'll first spell out the definition:

Let $V$ be a vector space over $\mathbb F$ and $T\in\mathcal L(V)$. A scalar $\lambda\in\mathbb F$ is said to be an eigenvalue of $T$ if there exists $v\in V\backslash\{0\}$ such that $T(v)=\lambda\cdot v$. 

If $\lambda\in\mathbb F$ is an eigenvalue of $T$, then any vector $v\in V\backslash\{0\}$ such that $T(v)=\lambda\cdot v$ is said to be an eigenvector of $T$ *associated with $\lambda$.* Letting $E(T,\lambda)\coloneqq\{v\in V\mid T(v)=\lambda\cdot v\}$, the set of all $\lambda$-eigenvectors is precisely $E(T,\lambda)\backslash\{0\}$.

There can be many, many cases to discuss, which really makes it hard to track the logic. But, so long as we keep track of the quantifiers ("for all," "arbitrary," "there exists"), we'll be in good shape.

The big idea is not hard: first, let $\lambda\in\mathbb F$ be arbitary, and consider the proposition "$T(v)=\lambda\cdot v$ for some non-zero $v\in V$." **This proposition is true for this particular $\bm\lambda$ if and only if $\bm\lambda$ is an eigenvalue of $\bm T$.**

**Example 1.** Let $V\coloneqq\mathcal P(\mathbb R)$ and let $T(p)\coloneqq p'$ be the derivative operator. Find all eigenvalues of $T$ as well as all eigenvectors associated with each eigenvalue.

*Idea.* We need to first let $\lambda\in\mathbb R$ be **arbitrary**, and consider the proposition "there exists non-zero $p\in\mathcal P(\mathbb R)$ such that $T(p)=p'=\lambda\cdot p$." So, if we want to talk about different cases, we first consider the possibilities for $\lambda$ **always**. Now, if the proposition is true for a particular $\lambda$, then this $\lambda$ is an eigenvalue of $T$; otherwise, it is not.

*Solution.* If $\lambda=0$, then we are considering
$$\exists p\in\mathcal P(\mathbb R)\backslash\{0\},\quad\quad T(p)=0\cdot p;$$
that is, "there exists a non-zero polynomial $p\in\mathcal P(\mathbb R)$ such that $p'(x)=0$ for all $x\in\mathbb R$." This is indeed true: any constant (but non-zero) polynomial has derivative 0. Therefore, $0$ is an eigenvalue of $T$.

Now, if $\lambda\ne0$, then we are considering
$$\exists p\in\mathcal P(\mathbb R)\backslash\{0\},\quad\quad T(p)=\lambda\cdot p;$$
that is, "there exists a non-zero polynomial $p\in\mathcal P(\mathbb R)$ such that $p'(x)={\lambda\cdot p(x)}$ for all $x\in\mathbb R$." Note that for any **non-constant** $p\in\mathcal P(\mathbb R)$, $\deg p'=\deg p-1$ (because $\deg 0=-\infty$), and $\deg(c\cdot p)=\deg p$ for any non-zero $c\in\mathbb R$. Then, for a non-zero $\lambda$, $\lambda\cdot p$ has a **different** degree from $p'$.

If two objects $x,y$ are equal, then anything about them are also equal. Taking the contrapositive, because $\lambda\cdot p$ and $p'$ have different degrees, we can conclude $\lambda\cdot p\ne p'$ always, so no $\lambda\ne0$ is an eigenvalue of $T$.

We have now found **all** eigenvalues. To find all $0$-eigenvectors, we solve the equation
$$T(p)=0\cdot p$$
for $p$; that is, we are solving $p'=0$ where $p$ is a non-zero polynomial. An **arbitrary** non-zero polynomial has $p(x)=a_0+\cdots+a_nx^n$ (where $a_0,\cdots,a_n$ are not all zeros), so $p'(x)=a_1+2a_2x+\cdots+na_nx^{n-1}$. That is, we are now solving
$$a_1+2a_2x+\cdots+na_nx^{n-1}=0.$$
The zero polynomial is unique, so $a_1=2a_2=\cdots=na_n=0$, which implies $a_1=\cdots=a_n=0$. Note that we are **solving** for $p$, so any $p$ with $a_0\ne0$ and $a_1=\cdots=a_n=0$ works (note that $n$ is also **arbitary** because the polynomial was arbitrary, but that doesn't change anything).


Therefore, $T$ has a unique eigenvalue $0$, whose associated eigenvectors are any non-zero constant polynomial.

**Example 2.** Let $V\coloneqq C^\infty(\mathbb R)$ be the set of all smooth (i.e., infinitely differentiable) functions from $\mathbb R$ to $\mathbb R$ and let $T(p)\coloneqq p'$ be the derivative operator. Find all eigenvalues of $T$ as well as all eigenvectors associated with each eigenvalue.

*Idea.* Note that we don't have polynomials anymore, so we can't use the degree argument at all. But, the analysis is similar.

*Solution.* Let $\lambda\in\mathbb R$ be **arbitary**. Then,
$$\exists f\in C^\infty(\mathbb R)\backslash\{0\},\quad\forall x\in\mathbb R,\quad f'(x)=\lambda\cdot f(x).$$

This is actually a differential equation, which we know always has solution $f(x)=C\cdot\mathrm e^{\lambda x}$ for constant $C$—but this is not a rigorous argument. 

We claim that any $\lambda\in\mathbb R$ is an eigenvalue of $T$. Define a function $f_\lambda\in C^\infty(\mathbb R)\backslash\{0\}$ for each $\lambda$ by setting $f_\lambda(x)\coloneqq\mathrm e^{\lambda x}$. Then, $f_\lambda'(x)=\lambda\cdot\mathrm e^{\lambda x}=\lambda\cdot f_\lambda(x)$ indeed. Also, $f_\lambda\ne0$ cannot be the zero function, since the exponential function is never zero (so no $x\in\mathbb R$ exists such that $f_\lambda(x)=0$, which is a stronger condition than $f_\lambda\ne0$). Therefore, for each $\lambda\in\mathbb R$ we have found a nonzero $f_\lambda\in C^\infty(\mathbb R)\backslash\{0\}$ such that $T(f_\lambda)=\lambda\cdot f_\lambda$, so the eigenvalues of $T$ consists of entire field $\mathbb R$.

(We won't solve for all eigenvectors since this actually a lot of real analysis, which is beyond the point of this post.)
