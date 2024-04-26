I wanted to justify the following definition, but I was afraid the infinite intersection (which is in general uncountable) creates a logic issue. I am also uncertain if I implicitly assumed the Axiom of Choice.

**Definition 1.** Suppose $`\alpha_1,\cdots,\alpha_k\in E\ge F`$. Define the field $`F(\alpha_1,\cdots,\alpha_k)`$ as the smallest field of $E$ containing $`\alpha_1,\cdots,\alpha_k`$ and $F$; that is, for all subfields $F'\le E$ such that $F'\ge F$ and $`\{\alpha_1,\cdots,\alpha_k\}\subseteq F'`$, we have $`F(\alpha_1,\cdots,\alpha_k)\le F'`$

**Corollary 1.** If $`F(\alpha_1,\cdots,\alpha_k)`$ exists, then it must be unique.

*Proof.* If $F_1,F_2$ are both such smallest fields, then $F_1\le F_2$ and $F_2\le F_1$. Q.E.D.

To show that the above definition always exists, we begin by framing the concept of the smallest as an intersection.

**Proposition 1. (The easy version)** The subfields of a field are closed under finite intersections.

*Proof.* Let $`F_1,F_2\le E`$, and suppose $`a,b\in F_1\cap F_2`$ are arbitrary. Then, $`a+b\in F_1`$, and $`a+b\in F_2`$. Similarly, one deduces that $`-a\in F_1\cap F_2`$ and $`a\cdot b\in F_1\cap F_2`$. This shows that $F_1\cap F_2\le E$. Now, by simple induction, we may extend this statement to any finite intersection of subfields. Q.E.D.

**Proposition 2. (Is this valid?)** The subfields of a field are closed under intersections.

*Proof.* Let $`\{F_i\}_{i\in A}`$ be a family of subfields of $E$ and let $\tilde F\coloneqq\bigcap_{i\in A}F_i$. Let $a,b\in\tilde F$. Then, for each $i\in A$, $a,b\in F_i$, so $a+b\in F_i$. The arbitrary choice of $i$ then implies $a+b\in\tilde F$. Similarly, one deduces that $-a\in\tilde F$ and $a\cdot b\in\tilde F$. Q.E.D.

**Corollary 3.** $`F(\alpha_1,\cdots,\alpha_k)`$ always exists; further, it is the intersection of all subfields of $E$ that contains $`\alpha_1,\cdots,\alpha_k`$ and $F$.

*Proof.* The intersection of all subfields of $F$ containing $`\alpha_1,\cdots,\alpha_k`$ and $F$, which we denote as $\tilde F$, clearly still contains $`\alpha_1,\cdots,\alpha_k`$ and $F$. Now, for every subfield $`F_i`$ containing $`\alpha_1,\cdots,\alpha_k`$ and $F$, $\tilde F$ is formed from the intersection of $`F_i`$ with other fields, so $`\tilde F\le F_i`$. Thus, $\tilde F$ is indeed the smallest field containing $`\alpha_1,\cdots,\alpha_k`$ and $F$.

**Proposition 3.** If $\alpha\in E\ge F$ is algebraic over $F$, then $F(\alpha)\simeq F[x]/\langle\mathrm{irr}(\alpha,F)\rangle$.

*Proof.* It is sufficient to show that there exists an isomorphism $\phi\colon F[x]/\langle\mathrm{irr}(\alpha,F)\rangle\to F(\alpha)$. Define $\phi$ as follows: for every element of the domain, choose a unique representative $f(x)+\langle\mathrm{irr}(\alpha,F)\rangle$ with $\deg f\lt\deg\mathrm{irr}(\alpha,F)$. Denote the coefficients of $f(x)$ as $`a_0,\cdots,a_n`$ and define the image as $`a_0+\cdots+a_n\alpha^n`$. Because $F(\alpha)$ contains $`\alpha`$ and $F$, it must contain the image, so $\phi$ is well-defined. That the map is an isomorphism follows the same argument from class. Q.E.D.

**Proposition 4.** If $\alpha\in E\ge F$ is transcendental over $F$, then $F(\alpha)\simeq F(x)$.

...
