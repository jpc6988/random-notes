# Constructing Undecidable Languages

**Claim.** Let $`\Sigma`$ be an alphabet and suppose $`P\colon\mathcal P(\Sigma^*)\to\{\rm T,F\}`$ is a predicate on languages over $\Sigma$ such that there exist languages $A,B\subseteq\Sigma^*$ with $P(A)=\rm T$ and $P(B)=\rm F$. Then, $`P_{\text{TM}}\coloneqq\{\langle M\rangle\mid M\text{ is a TM with }P(L(M))=\rm T\}`$ is undecidable.

*Incorrect Proof.* Suppose on the contrary that $T$ decides $P_{\rm TM}$. We define a TM $D$ which shall decide $A_{\rm TM}$, in which we define another TM $N$ on whose encoding $A_{\rm TM}$ will be run. By assumption, $A$ and $B$ are decidable, whereby we fix $X$ and $Y$ which decide them respectively.
```python
def D(M: TuringMachine, w: str) -> bool:
    def N(x: str) -> bool:
        if M(w) == True:
            return X(x)
        else:
            return Y(x)
    return T(N)
```
Note that
```math
L(N)=\begin{cases}A,\quad&\text{if }w\in L(M),\\B,&\text{otherwise}.\end{cases}
```
Therefore, by construction, $P(L(N))$ is true if and only if $w\in L(M)$. Hence, $D$ decides $A_{\rm TM}$, a contradiction. Q.E.D.

---

The proof above is incorrect because $M$ may not halt. While $N$ is not ran—but rather *run on* as an input—this remains an issue for us. When $M$ does not halt on $w$, the `else` branch in $N$ is never run and $N$ never halts. As a result, $x\notin L(N)$ even though we expect $L(N)=B$; that is, $L(N)\ne B$ in general, even when $w\notin L(M)$.
