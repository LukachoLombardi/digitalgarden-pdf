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
> f: X \rightarrow Y
> $$

Notation of all (co-)domain values' mapping:  
$$
x \mapsto f(x)
$$
## "-jectivity" types

- general function: codomain values can have many domain values ($f(x_1)=f(x_2) \rightarrow x_1=x_2$, )
- injective: codomain values have **at most one** domain value (every y element Y: y=f(x), A to B is {0,1}:1)
- surjective: codomain values have **at least one** domain value(A to B is \[1-n\]:1)
- bijective: There is **exactly one** domain value per codomain value (1:1 mapping of domain to codomain values)
### Proving mapping types

> [!NOTE] 
> Surjectivity proofs won't come up on exams (therefore bijectivity ones won't either).

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

> [!WARNING] Not bidirectional
> $x_n$ being a null sequence is a *conditon* for its series being convergent, it does however **not fully satisfy** convergence. See the harmonic series as an example.
> ![[Ana1_EN-1.pdf#page=31&rect=67,451,533,561|Ana1_EN-1, p.27]]


![[Ana1_EN-1.pdf#page=31&rect=70,330,533,431|Ana1_EN-1, p.27]]
$(s_m)_{m \in \mathbb{N}}$ again describes the series.
### The Geometric Sequence
![[Ana1_EN-1.pdf#page=29&rect=242,494,387,543|Ana1_EN-1, p.25]]
This proof is wedged into an example for some reason. 
### The Leibniz Rule
![[Ana1_EN-1.pdf#page=31&rect=68,61,534,179|Ana1_EN-1, p.27]]
We're basically looking at a series over a cauchy sequence here. No surprise then that the proof for this involves the *Cauchy Criterion* (see more on [[Ana1_EN-1.pdf#page=32|Ana1_EN-1, p.28]]).

### Absolute Convergence
![[Ana1_EN-1.pdf#page=32&rect=70,138,534,221|Ana1_EN-1, p.28]]
I don't get all of these Definitions without any clear way to apply them. Maybe something will follow later on. 

It goes without saying that *Absolute Convergence $\Rightarrow$ Convergence*.
### Operations on Convergent Series
![[Ana1_EN-1.pdf#page=33&rect=68,119,534,301|Ana1_EN-1, p.29]]
Ig just memorize this.

### Direct Comparison Tests
![[Ana1_EN-1.pdf#page=34&rect=70,474,535,624|Ana1_EN-1, p.30]]
We already need to know about another convergent series to argue like this.

### The Ratio Test
![[Ana1_EN-1.pdf#page=35&rect=69,513,534,635|Ana1_EN-1, p.31]]
I like this one.

### The Root Test
![[Ana1_EN-1.pdf#page=35&rect=66,158,533,278|Ana1_EN-1, p.31]]
Whatever that means.

### Comparing Convergence Tests
![[Ana1_EN-1.pdf#page=36&rect=70,347,533,693|Ana1_EN-1, p.32]]

### Series Convergence Testing Summary
![[Ana1_EN-1.pdf#page=38&rect=49,137,559,696|Ana1_EN-1, p.34]]


> [!NOTE] 
> I think the essence of this chapter is that you should just go fuck yourself. You're not gonna be able to understand or even memorize all of the proofs. Even this diagram is still way to much work considering the fact that you won't even really understand what you're doing.

# Topology of the Real Line
## $\varepsilon$-Neighborhood
![[Ana1_EN-1.pdf#page=39&rect=68,67,537,175|Ana1_EN-1, p.35]]
Basically just defined as "stuff that is in an $\varepsilon$ radius around $x$".
### Classifications of Points using the $\varepsilon$-neighborhood
![[Ana1_EN-1.pdf#page=40&rect=70,432,534,624|Ana1_EN-1, p.36]]
This is all pretty intuitive actually.
## Interior, Exterior, Boundaries
$\dot{\cup}$ means *disjoint union*, so $a \dot{\cup}b$ means $a \cup b \wedge a \cap b = 0$.
![[Ana1_EN-1.pdf#page=40&rect=68,96,535,259|Ana1_EN-1, p.36]]
Also note the Complement $A^c = \mathbb{R} \setminus A$.
> [!NOTE] Definition of "boundary"
> As you will see in a lot of range examples, a set containing an undefined/"limit"-boundary will not be treated as containing its boundaries, e.g. $(1,3)$ or $[1,3)$. The boundaries in these cases would be $\{1,3\}$.

## Open and Closed Sets
![[Ana1_EN-1.pdf#page=42&rect=68,394,536,654|Ana1_EN-1, p.38]]

> [!DANGER] Stupid Nomenclature
> If you look at the definitions of "open" and "closed" sets, you'll pick up on the fact they run contrary to  most people's intuition. They simply do not represent the property you would probably associate with these words normally. Also note (from the script) that they are not exclusive or opposites.
- **Open Sets** *only* contain their own interior points, meaning they *can't* have a defined boundary. Therefore, a set like $[1,2]$ is in fact **not open**, while the set $(1,2)$ **is**.
- **Closed Sets** are the complement to any open set. 
	- So they *can* contain their own boundary, if their complement doesn't. (*strictly closed*).
	- They can also not contain it, given their complement does (making them ***closed and open* at the same time**!) $\Rightarrow$ only case of "double-type" (i think?)
## Combining Sets
![[Ana1_EN-1.pdf#page=43&rect=68,354,537,548|Ana1_EN-1, p.39]]
## Bounded Sets
![[Ana1_EN-1.pdf#page=44&rect=69,204,534,621|Ana1_EN-1, p.40]]
## Compact Sets
Compactness is really just a simplified set of properties that, if we manage to get any given set to adhere to, will give us access to a lot of already discovered relations, properties, proofs and so on. So for now just tread the term "Compact" as an arbitrary definition (which you should of course remember!), don't try to guess it from your existing understanding of the term.
![[Ana1_EN-1.pdf#page=45&rect=70,280,532,606|Ana1_EN-1, p.41]]
Note that "every sequence from $A$" just means "any sequence with $A$ as its codomain".
![[Ana1_EN-1.pdf#page=45&rect=69,191,536,258|Ana1_EN-1, p.41]]
![[Ana1_EN-1.pdf#page=46&rect=69,501,534,559|Ana1_EN-1, p.42]]

# Continuity
The most intuitive idea of Continuity is probably a given function $f: D \rightarrow R; D \subset \mathbb{R}$ not having any "jumps" in its visual representation (on $D$). We'll explore shortly how we can actually note and describe this formally.
## "Local" Continuity
First, we need to establish what Continuity means for any $x_0 \in D$:
> A function $f$ is called Continuous *at* some $x_0 \in D$, if $\lim_{x \to{x_0}} f(x) = f(x_0)$, meaning the limit approaching $x_0$ is equal to $x_0$'s associated codomain value.

Note that $x_0$ is a "unique" member of $D$ here. It counterintuitively isn't part of some pattern $x_1, x_2, x_3, ...$ or similar.

### Special Case: Holes in the Domain
If our domain has isolated outliers (e.g. $D = [0,5] \cup \{10\}$), we still treat it as continuous.

# "Extended" Continuity
This is the actual meat and potatoes of what continuity means for a whole function:
> A function $f$ is called continuous, if the definition of "local" continuity (see above) holds for any $x_0 \in D$.

The slides note this as follows:
> a function $f$ is called continuous, if for $\forall x_0 \in D \subset \mathbb{R} : \lim_{x_n \in D \to{x_0}} = f(x_0)$, with $(x_n)_n$ being any sequence on $D$.

We can of course also find $\lim = \infty$ or $\lim = - \infty$, meaning there is no limit and therefore no continuity.

![[Ana1_EN-1.pdf#page=50&rect=68,532,535,652|Ana1_EN-1, p.46]]

## Sided Continuity
![[Ana1_EN-1.pdf#page=50&rect=68,65,535,254|Ana1_EN-1, p.46]]
Should be easy to imagine visually. This just depends on which side(s) of the graph converge to $f(x_0)$ for $x_n \to x_0$.

### Relation Between Continuity and Sided Continuity
![[Ana1_EN-1.pdf#page=52&rect=67,153,536,293|Ana1_EN-1, p.48]]
- (b) means: If the limit (...) exists, then the left-sided and right-sided limit *don't* exist, and may not be the same and equal to y.
- (c) means: If both the left-sided and right-sided limits exist (in addition to the condition written out below), are the same and equal to y,  then the limit (...) exists. 

![[Ana1_EN-1.pdf#page=53&rect=70,339,534,459|Ana1_EN-1, p.49]]
Kind of a redefinition.

## $\varepsilon-\delta$ Characterization and Continuity
![[Ana1_EN-1.pdf#page=53&rect=66,61,536,207|Ana1_EN-1, p.49]]
This brings us back to the sausage example at the beginning of the script. We basically just define two permissible ranges $\forall \varepsilon > 0$ and $\exists \delta > 0$ around both $y$ and $x_0$ respectively, and require that any $f(x)$, with $x \in D$ in the $\delta$ range around $x_0$, shall be within the $\varepsilon$ range around $y$. There's a proof to this but if it comes up in the exam imma just kill myself.

![[Ana1_EN-1.pdf#page=54&rect=68,322,533,567|Ana1_EN-1, p.50]]

## Some more bullshit implications to remember
![[Ana1_EN-1.pdf#page=54&rect=67,124,535,266|Ana1_EN-1, p.50]]
## Combinations on Continuous Functions
![[Ana1_EN-1.pdf#page=55&rect=68,202,536,273|Ana1_EN-1, p.51]]
![[Ana1_EN-1.pdf#page=56&rect=68,405,536,478|Ana1_EN-1, p.52]]
Seems intuitive, still don't understand the proofs.
## Continuity on Compact Sets
![[Ana1_EN-1.pdf#page=57&rect=68,477,535,535|Ana1_EN-1, p.53]]
![[Ana1_EN-1.pdf#page=57&rect=69,298,535,366|Ana1_EN-1, p.53]]
## The Intermediate Value Theorem
![[Ana1_EN-1.pdf#page=58&rect=69,569,535,661|Ana1_EN-1, p.54]]
I don't really get what you need to formally prove here?
- yes, if a function without codomain jumps crosses from negative to positive, it *will* have to hit 0 at some point.
- "$f(a) < f(x) < f(b)$ has $x \in [a,b]$" seriously?
![Pasted image 20260118003649.png](/img/user/Attachments/Pasted%20image%2020260118003649.png)
## Continuity and the Inverse Function

# Elementary Functions
## Monomials
### Inverse
## Polynomials
## Power Series
## Exponentials
### Inverse
## Trigonometrics

# Differentiation in One Variable
## The Basic Idea of Differentiation
This should all be intuitive for you by now, but just in case:
![[Ana1_EN-1.pdf#page=84&rect=67,375,537,509|Ana1_EN-1, p.80]]

TODO: everything from 18.12.25 (stuff like pole points and continuous extendability)
TODO: 8.1.26


