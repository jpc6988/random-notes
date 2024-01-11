# Justifying a Simplified Group Definition

The common definition of a group is:

**Definition 1.** A pair $(S,*)$ is said to be a group if $S$ is a set and $*\colon S\times S\to S$ satisfies associativity, existence of identity, and existence of inverse.

It may be proposed that the following seemingly looser definition is equivalent:

**Definition 2.** A pair $(S, * )$ is said to be a group if $S$ is a set and $*\colon S\times S\to S$ satisfies
- The operation $*$ is associative;
- There exists a left identity $e\in G$ such that $e*x=x$ for all $x\in G$;
- For each $x\in G$, there exists a left inverse $x'\in G$ such that $x'*x=e$.

The proof that Definition 2 implies Definition 1 is as follows.

## Proof

### The left identity is unique.

Suppose $e_1,e_2\in G$ are both left identities; that is, $e_1*x=e_2*x=x$ for all $x\in G$. Let $(e_2)'_1\in G$ be an $e_1$-inverse of $e_2$ and $(e_2)'_2\in G$ be an $e_2$-inverse of $e_2$; that is, $(e_2)'_1*e_2=e_1$ and $(e_2)'_2*e_2=e_2$. Then,
$$\begin{aligned}\phantom{\implies}&e_1*e_2=e_2=(e_2)'_2*e_2\\\implies&(e_2)'_1*\cancel{e_2}*e_2=(e_2)'_2*e_2\\\implies&e_1=e_2.\end{aligned}$$

Note that the third item is quantified by the existence of $e$ from the second item. Therefore, this does not directly prove $(\forall x,a*x=x)\implies a=e$.


### The only idempotent element is the left identity

Suppose $x*x=x$ where $x\in G$. Then, for some left inverse $x'\in G$, $x'*x*x=x'*x$, so $e*x=x=e$.

### The left inverse is two-sided.

Now, whenever $x'\in G$ is a left inverse $x\in G$, we have $(x*x')*(x*x')=x*e*x'=x*x'$, so $x*x'=e$.

### The left identity is two-sided.

For any $x\in G$ and for some inverse $x'\in G$, $x*e=x*x'*x=e*x=x$.

### Bonus: The inverse is unique.

Fix a particular $x\in G$ and suppose both $x',x''\in G$ are left and hence two-sided inverses of $x$. Then, $x'=e*x'=x''*x*x'=x''*e=x''$.
