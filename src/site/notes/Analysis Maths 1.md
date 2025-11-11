---
{"dg-publish":true,"permalink":"/analysis-maths-1/"}
---

Some more stuff about Proofs
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
(summarize this chapter a bit here)

TODO: Look at 2.3 and 2.4 again

