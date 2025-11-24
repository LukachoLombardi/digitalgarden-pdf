---
{"dg-publish":true,"permalink":"/analysis-maths-1/"}
---

# Some more stuff about Proofs
## Implications
![Pasted image 20251023114430.png](/img/user/Attachments/Pasted%20image%2020251023114430.png)
## Contrapositions
> [!SUMMARY]
> Proving the contraposition ($\lnot B ⇒ \lnot A$) is just as good as to proposition  ($B ⇒ A$) 

![Pasted image 20251023122747.png](/img/user/Attachments/Pasted%20image%2020251023122747.png)
# Functions

> [!SUMMARY] Definition
> A function is generally defined as a mapping between **domain** (let's call that Set X) and **codomain** (Y) values.
> $$
f: X \rightarrow Y
$$

Notation of all (co-)domain values' mapping:  $$x \mapsto f(x)$$
## "-jectivity" types

- general function: codomain values can have many domain values ($f(x_1)=f(x_2) \rightarrow x_1=x_2$, )
- injective: codomain values have **at most one** domain value (every y element Y: y=f(x), A to B is {0,1}:1)
- surjective: codomain values have **at least one** domain value(A to B is \[1-n\]:1)
- bijective: There is **exactly one** domain value per codomain value (1:1 mapping of domain to codomain values)
### Proving mapping types

> [!NOTE] 
> Surjectivity proofs won't come up on exams

- injectivity: **Prove** if $f(a) = f(a')$, then $a=a'$
- not injective: **find** $a \neq a'$ for $f(a) = f(a')$
- surjective: for every $b \in B$, **find** $a \in A$ such that $f(a) = b$ 
- not surjective: To check that f is not surjective: find $b ∈ B$ and **prove** that there is no $a ∈ A$ such that $f(a) = b$.
# Trigonometric functions
you learned this in school. x is cos, y is sin, imagine the circle, etc....
Derivatives follow the order: sin -> -sin -> cos -> -cos

# Sequences
A sequence is a function $x: \mathbb{N} \rightarrow \mathbb{R}$. Application of such a function is noted as $x_n$, **NOT** $\cancel{x(n)}$. The whole function can also be written as $(x_n)_{n \in \mathbb{N}}$, $(x_n)_{n=1}^{\infty}$ or just $(x_n)_n$.

## Convergence
This is basically just $\lim\limits_{x\to\infty} (x_n)_n$.
![[Ana1_EN-1.pdf#page=8&rect=69,77,534,258|Ana1_EN-1, p.4]]
(This defines it a bit more specifically, e.g. for discrete functions)

> [!INFO] Proposition of uniqueness
> A limit $x$ is proposed to be unique. There's a proof somewhere in the handout, but it should be pretty obvious.

### Notational Fluff
We can also write $x \stackrel{\varepsilon}{\approx} y$ instead of $|x-y| < \varepsilon$

### Triangle Inequality
Don't know what relevance this holds here, but $x \stackrel{\varepsilon}{\approx} y \stackrel{\delta}{\approx} z \Rightarrow x \stackrel{\varepsilon+\delta}{\approx} z$. We can deduce from this, that $|x − z| ≤ |x − y| + |y − z|$. If we take $a = |x-y|$, $b=|y-z|$ as sides of a triangle between $x,y/y,z$, this shows that the distance $y$ to $z$ is smaller than the distances $a,b$ added.

## Bounds
![[Ana1_EN-1.pdf#page=11&rect=69,299,534,477|Ana1_EN-1, p.7]]

As per later in the slide, symmetric bounds around 0 can also be chosen as 
$$x_n \in [c,c],: c = max(|a|,|b|)$$
Actually determinining bounds is mostly done by analyzing convergence. Lower bounds can often be found by finding monotonical increase and taking $x_1$'s value.

## $\lim$ notation
You should remember this from HS. Basically:
$$
x_n \rightarrow x:n \rightarrow \infty \Leftrightarrow \lim_{n \to \infty} x_n = x
$$

### Bounds and Convergence
![[Ana1_EN-1.pdf#page=12&rect=66,470,536,695|Ana1_EN-1, p.8]]
The proof probably isn't relevant for the exam, but you should try to at least follow it. 

## Null Sequences
Defined as a sequence $(x_n)_n: n \rightarrow \infty \Rightarrow x_n\rightarrow0$

![[Ana1_EN-1.pdf#page=13&rect=69,454,536,599|Ana1_EN-1, p.9]]

![[Ana1_EN-1.pdf#page=13&rect=67,259,538,316|Ana1_EN-1, p.9]]
Note for the proof of this lemma: if we add two functions at the same n, the limit for the result will be the addition of the original limits (separately for both bound directions).

> [!INFO] Lemmas
> Starting from [[Ana1_EN-1.pdf#page=13|this]] we have even more null sequence lemmas. These are probably good to know about.

The most important Lemma is probably the fact, that each convergent sequence can be written as a null sequence plus the limit.
## Commutation of lim
sequences commute with basic ops $+,-,\times, \div$.  (If using a shared counter n).
$$
(x_n)_n \, op \, (y_n)_n = (x_n \, op \, y_n)_n  
$$
![[Ana1_EN-1.pdf#page=15&rect=67,345,532,641|Ana1_EN-1, p.11]]

The proof around this is pretty long, you probably won't remember it, but at least try understanding it.

## $\leq$ extends to the limit
$$
(x_n)_n \leq (y_n)_n \Leftrightarrow \lim_{n \to \infty} x_n \leq \lim_{n \ \to \infty} y_n
\,
\text{; for every} \, n \in \mathbb{N}
$$
The proof is weird, but this honestly just makes sense.

## Sandwich Lemma
If a sequence is "sandwiched" between two sequences convergent to the same $x$ for every $n \in \mathbb{N}$, then the sandwiched sequence has the same limit.

## Convergence beating order
- higher powers beat lower powers
- exponential quotients beat power quotients
- factorials beat exponential quotients
## Cauchy Sequences
![[Ana1_EN-1.pdf#page=20&rect=68,363,536,473|Ana1_EN-1, p.16]]
Basically a function that "converges onto itself", but not necessarily to a single value:
![Pasted image 20251124142156.png](/img/user/Attachments/Pasted%20image%2020251124142156.png)

> [!WARNING] Nomenclature
> We probably can't call Cauchy sequences "convergent" by themselves, since that descriptor is already taken. You could remember it as "it's neighboring $x_n$ values get infinitely close for $n > n_0$ (for some $n_0$)"

> [!INFO] Regular Convergence vs Cauchy sequences
> Every convergent sequence is also a Cauchy sequence, but not necessarily the other way around! 
> Every Cauchy Sequence is also convergent (logically).

## Monotonicity and Convergence
![[Ana1_EN-1.pdf#page=21&rect=68,350,534,528|Ana1_EN-1, p.17]]
Pretty basic stuff
![[Ana1_EN-1.pdf#page=21&rect=69,210,534,299|Ana1_EN-1, p.17]]
Have another look through the proofs on [[Ana1_EN-1.pdf#page=21|Here]], at least as exam preparation.
## Extrema
![[Ana1_EN-1.pdf#page=23&rect=66,426,533,621|Ana1_EN-1, p.19]]
minimum and maximum are infimum and suprenums which are actually reached by $x_n$ at some point.

## Subsequences
Subsequences are basically sub-parts of another sequence (meaning either the same sequence, or a reduced mapping).
It is written as 
$$
(x_{n_k})k\in\mathbb{N}
$$
With k being the input to a sequence returning the used n's. Note that $(n_k)k\in\mathbb{N}$ is still an infinite sequence.

> [!INFO] Convergence
> Convergence is preserved between sequences and their subsequences. Since we can't add outliers, we cannot break the convergence. 
> [[Ana1_EN-1.pdf#page=24|Ana1_EN-1, p.20]]

![[Ana1_EN-1.pdf#page=25&rect=68,590,533,653|Ana1_EN-1, p.21]]
![[Ana1_EN-1.pdf#page=25&rect=68,245,535,410|Ana1_EN-1, p.21]]

# Series
![[Ana1_EN-1.pdf#page=28&rect=68,450,534,655|Ana1_EN-1, p.24]]

Series are basically running totals of an underlying sequence's $(x_n)_n$'s $x_n$'s up to a given $n = m$. 
## Convergence of Series
![[Ana1_EN-1.pdf#page=30&rect=70,635,534,692|Ana1_EN-1, p.26]]
Can be proven by utilizing dependence on the Sequence's relating Series.

![[Ana1_EN-1.pdf#page=31&rect=70,330,533,431|Ana1_EN-1, p.27]]