---
{"dg-publish":true,"permalink":"/stochastics-chapter-1/"}
---

# Introduction
Mostly irrelevant, we'll be doing mostly probability with a bit of Statistics (both sub-topics of stochastics)
# Probability Spaces
## Discrete Probability Spaces
### Random Experiment
- unpredictable outcome
- repeatable
### Sample Space $\Omega$
**Set of all possible outcomes**
E.g.:
- dice roll: $\Omega = \{1,...,6\}$
- n coin tosses: $\Omega = \{0,1\}^n$
$w \in \Omega$: **elementary event** (directly observable outcome, e.g. $6$ for dice roll)
$A \in \Omega$: **event** (composite of elementary events, e.g. all die faces $\geq 3$, or just an *elementary event*)
Power set of $\Omega$: $P(\Omega)= \{ A:A \subseteq \Omega \}$ (E.g. $P(\{0,1\}) = \{\{\},\{0\},\{1\},\{0,1\}\}$)

A Set $M$ is *at most countable*:
$:\Leftrightarrow$ M is finite or its elements can be indexed by an $n \in \mathbb{N}$
$|M|$: Cardinality of M

### Definition 2.1
A *discrete probability space* is a pair $(\Omega, P)$ of an at most countable $\Omega \neq \varnothing$ and a function $P: P(\Omega) \rightarrow [0,1]$ such that:
1. $P(\Omega) = 1$
2. for (pairwise) disjoint sets $A_1, A_2, ... \in P(\Omega)$ (i.e. $A_i \cap A_1 = \varnothing$ for $i \neq 1$), means **$\sigma$-additivity** ($P(\cup_{k=1}^\infty A_k) = \sum_{k=1}^\infty P(A_k)$)
### Remark 2.2
- $P(\varnothing) = 0$
- If $|\Omega| < \infty$, 2. is equivalent to $P(A \cup B) = P(A) + P(B)$ for $A,B$ with $A \cap B = \varnothing$

E.g. Throwing a four-sided die: $(\Omega, P)$ with $\Omega = \{1,2,3,4\}$ and $P(A) = \frac{|A|}{4}$ for $A \subseteq \{1,...,4\}$,
$P('even \, number') = P(\{2,4\}) = \frac{|\{2,4\}|}{4} = \frac{2}{4} = \frac{1}{2}$

Alternative probability:
$P(A) =$
- $1$, $4 \in \Omega$
- $0, 4 \notin A$
for $A \subseteq \Omega$
(no idea what this means)

- Repeat the random experiment many times
- $K_n(A)$: Number of occurences of $A$ in first $n$ trials
- Observation: $\frac{K_n(A)}{n} \rightarrow^{n\rightarrow \infty} P_A \leftarrow$ desired probability, this is the relative frequency

### Example 2.4: Tossing a fair coin $n$ times
$(\Omega,P)$ with $\Omega = \{0,1\}^n$ and $P(A) = \frac{|A|}{2^n}$
for $A \subseteq \{0,1\}^n$, e.g. $P('exactly\,one\,head') = P((1,0,..,0),...,(0,...,0,1)) = \frac{n}{2^n}$
*Laplace probability space*:
- $\Omega = \varnothing$ finite
- $P(A) = \frac{|A|}{|\Omega|}$ for $A \subseteq \Omega$
