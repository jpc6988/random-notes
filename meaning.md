# Formalizing the Notion of *Meaning* As It Emerges in Deep Learning

**Note:** Throughout this note, the word *meaning* will be used a countable word, where "a meaning" refers to an instance of meaning, such as that of a particular sentence, and "all meanings" to the collection of all possible instances of *meaning*. The word *meaning*, whenver it is referred to under the proper grammatical rules and in its typical *meaning*, it will be rendered in italics.

Consider the machine learning task of machine translation. Whatever a sentence means in one language, there's always another sentence that means exactly that in another language — maybe not exactly, but by some $\epsilon>0$, at least.

Suppose $\mathcal L$ is the set of all language. Every language $\ell\in\mathcal L$ is $\ell=(V_\ell,S_\ell)$, where $V_\ell$ is a non-empty, finite set of vocabulary, and $S_\ell$, the set of all sentences is defined as
$$S_\ell\coloneqq\{\lambda_\ell\}\cup\bigcup_{n=1}^\infty V_\ell^n,$$
where $\lambda_\ell\in V_\ell$ is the "empty character," or the "null phrase."

Clearly, $S_\ell$ is countable.

Suppose now that every sentence has a corresponding meaning; that is, there exists a set $\mathcal M$ of all meanings, and a map $m_\ell\colon S_\ell\to\mathcal M$. Here, $\mathcal M$ is the Platonic ideal of all meanings, which *can* include meanings not yet conceived by man or meanings impossible to utter in any language. So $m_\ell$ may not but surjective.

Suppose $\ell_1,\ell_2\in\mathcal L$. We should expect $m(S_{\ell_1})\cong m(S_{\ell_2})$, whatever the "isomorphism" should mean. 

A weaker condition states that the meaning (as defined above through $m$) of a sentence in a language can be approximated arbitrarily well by sentences in any other fixed language:

$$\forall\ell_1,\ell_2\in\mathcal L,\forall s_1\in S_{\ell_1},\forall\epsilon>0,\exists s_2\in S_{\ell_2},d_{\mathcal M}(m(s_1),m(s_2))<\epsilon,$$

where $d_{\mathcal M}$ is a metric on $\mathcal M$, so $\mathcal M$ needs to be a metric space. This is reasonable as suggested by the use of sentence embeddings and similarity "metrics" like the cosine similarity.

This induces the structure of "infinitesimal refinement of meaning," which might allow the introduction of limits and convergence of meanings. [TK]

On the other hand, considering languages individually, we can only hope that $m(S_\ell)\cong\mathcal M$ for at least some $\ell\in\mathcal L$. This certainly requires that $\mathcal M$ be countable. I guess we can accept if $m(S_{\ell})$ is "dense" in $\mathcal M$, whatever that means. A "modernist" would definitely believe that $\mathcal M$ is, as such, countable lol.

## TODO

Investigate the vector representation of sentence $A$, sentence $B$, and sentence $A\circ B$, where $\circ$ simply joins two sentences. What does that mean? Does it admit some special product-ish structure in $\mathcal M$ under $m$? Clearly $\mathcal M^{\circ n}\subset\mathcal M$ for any $n\in\mathbb N$. Does there then exist some (minimal) generating set $M_0\subset\mathcal M$ such that $\bigcup_{n=1}^\infty\mathcal M_0^{\circ n}\cong\mathcal M$, or at least dense in $\mathcal M$, whatever that means?

I really want a metric. Why does the angle play nicely (as humans see) but not the magnitude? Can I quantify the degree to which they're "nice?"