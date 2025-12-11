---
{"dg-publish":true,"permalink":"/das-combinatorics-and-counting/"}
---

# Cardinality
Already mentioned in [[DAS Sets Notes#Set Notation\|DAS Sets Notes#Set Notation]].
It's just the size of a set.

> Question: If set $S$ is infinite, can we say $|S| = \infty$?

$$
\{2,4,6,...\} \subseteq \mathbb{N} \subseteq \mathbb{Z} \subseteq \mathbb{Q} \subseteq \mathbb{R}
$$

This implies that these "infinities" are not of the same size, since they are subsets of each other.

# Countability
A Set $A$ is *countable* if there exists an injective function $f:A \rightarrow \mathbb{N}$, and is *uncountable* otherwise.
$\Leftrightarrow$ a surjective function $g: \mathbb{N} \rightarrow A$  (use your head for this one).

Only countable sets can be represented by a computer. (Meaning there is at least one index $\in \mathbb{N}$ associated with each element of the set (I used my head for you)).

![[Lecture_6.pdf#page=35&rect=-28,11,1229,654|Lecture_6, p.7-7]]
TODO: Understand whatever this is

# Counting
$$
|A \times B| = |A| \times |B|
$$
(pretty obvious)

![[Lecture_6.pdf#page=50&rect=-18,416,846,581|Lecture_6, p.10-7]]

# Combinatorial Proofs
![[Lecture_6.pdf#page=60&rect=-13,480,608,647|Lecture_6, p.12-1]]
(in- and surjectivity are treated as exclusive cases here)

> [!WARNING] 
> Note that these theorems are not symmetric! (really note that, Wiehe said that like half of every course gets this wrong on the exam).

![[Lecture_6.pdf#page=78&rect=-18,78,1223,654|Lecture_6, p.13-14]]
**NOTE**: This slide is extremely confusing because it doesn't actually go into the main part of the proof, which is proving the bijection. Also there's a typo in $A = A_1...$, which should start with $A_0$.

TODO: Read the fuckass slide again and try to understand it
# "Drawing from sets" (Basic Combinatorics)
![[Lecture_6.pdf#page=86&rect=-14,25,802,648|Lecture_6, p.15-7]]
Main cases to distinguish
(**NOTE**: Replacement means not changing the set after drawing from it, as in "re-placing" the element we "took" from it (like taking a potato from a bag as Wiehe would say).

|                | ordered | unordered |
| -------------- | ------- | --------- |
| replacement    | 1       | 4         |
| no replacement | 2       | 3         |
**1**:
![[Lecture_6.pdf#page=89&rect=-21,387,792,651|Lecture_6, p.16-3]]
for a set this means: $r = |A|^{|k|}$.
The most prevalent example of this would be the max possible decimal representable by binary strings (like $S = \{1,0,0,0,0,1,1\}$).

**2**:
![[Lecture_6.pdf#page=103&rect=-23,321,1245,656|Lecture_6, p.17-9]]
$^{\underline{k}}$ means performing a faculty operation for k steps, meaning you stop after k multiplications (e.g. $5^{\underline{2}} = 5 \times 4$).

**3**:
![[Lecture_6.pdf#page=110&rect=-21,232,1243,656|Lecture_6, p.18-5]]
$\binom{n}{k}$ is the binomial coefficient defined as:
![[Lecture_6.pdf#page=111&rect=-14,260,728,325|Lecture_6, p.18-6]]
![[Lecture_6.pdf#page=116&rect=-2,4,1181,241|Lecture_6, p.18-11]]

**4**:
![[Lecture_6.pdf#page=130&rect=-14,51,1233,651|Lecture_6, p.20-7]]
TODO: Understand this

We use the formula $\binom{n+k-1}{n-1}$ (The last slide is wrong in the original version!)

Some combinatorial proof examples regarding the binomial coefficient and powersets: [[Lecture_6.pdf#page=118|Lecture_6, p.19-1]]

# Double Counting
Idea: We know $f: A \rightarrow B$ is bijective $\Rightarrow$ $|A| = |B|$

## Degrees
Let $R \subseteq A \times B, a \in A,b \in B$
- $deg(a) = |\{b \in B | (a,b) \in \mathbb{R}\}|$
- $deg(b) = |\{a \in A | (a,b) \in \mathbb{R}\}|$
So the degree is basically the set of all edges connected to $deg$'s argument vertex $deg(a) = |\{b \in B | (a,b) \in \mathbb{R}\}|$

> Theorem: $\sum_{a \in A} deg(a) = |R| = \sum_{b \in B} deg(b);\,deg(a)= |\{b \in B | (a,b) \in \mathbb{R}\}|$

This will partition $R$ into subsets, which $\cup$ will be $\subseteq R$
- Since $R_a$: all edges touching b
- $R_b$: all edges touching a
- $R$ only contains vertices which are part of an edge (from relation/vertex definition).
Since for any $deg(a) \cap deg(a') = \emptyset$ and the union rule:
$|R|$ can be represented by the sum of all degrees in $A$ or $B$ (since this sum will only contain each edge once)

	TODO: 1.12.25


