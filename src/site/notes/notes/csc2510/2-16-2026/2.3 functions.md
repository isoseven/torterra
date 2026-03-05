---
{"dg-publish":true,"permalink":"/notes/csc2510/2-16-2026/2-3-functions/"}
---

## what is a function?
- given set $A$, $B$, a **function** $f$ from $A$ to $B$ ($f: A \rightarrow B$) is an assignment of **exactly one** element $f(x) \in B$ to each element $x \in A$
- functions can be represented graphically in many ways:
	- ![function-graphical-representation.png|409x171](/img/user/zimages/2-16-2026/function-graphical-representation.png)
- definition of functions
	- **todo: when reviewing, please look at ppt and fill in**

## function terminology
- if $f:A \rightarrow B$ and $f(a) = b$ (where $a \in A$ and $b \in B$) then
	- $A$ is the **domain** of $f$.
		- set of **all possible inputs**
	- $B$ is the **codomain** of $f$.
		- set of **all possible outputs**
	- $b$ is the **image** of $a$ under $f$.
		- a **specific output** for a single input
	- $a$ is a **pre-image** of $b$ under $f$.
		- the **input** that leads to a specific output
		- in general, $b$ may have **more than one** pre-images.
	- the **range** $R \subseteq B$ of $f$ is $\{ b\, | \,\exists a: f(a)=b\}$
		- the set of **all actual outputs**
- *range vs codomain?*
		- suppose: "$f$ is a function mapping students in this class to the set of grades $\{ A, B, C, D, E\}$."
		- $f$'s codomain is $\{ A, B, C, D, E\}$ and its range is **unknown**!
			- if the grades turn out to be **all** $A$ and $B$s, then the range becomes $\{ A, B \}$ and the codomain is still $\{ A, B, C, D, E\}$.

## function operators
- $f, g : \mathbb{R} \rightarrow \mathbb{R}$ 
	- (addition) $(f+g): \mathbb{R} \rightarrow \mathbb{R}$, where $(f+g)(x) = f(x) + g(x)$
	- (multiplication) $(f\times g): \mathbb{R} \rightarrow \mathbb{R}$, where $(f \times g)(x) = f(x) \times g(x)$
- for functions $g : A \rightarrow B$ and $f: B \rightarrow C$ there is a **special operator** called **compose** ($\circ$).
	- $(f \circ g)(x) : A \rightarrow C$, where $(f \circ g)(a) = f(g(a))$
	- note that $g(a) \in B$, so $f(g(a))$ **must be defined** and in $C$.
	- **the range of $g$ must be a subset of $f$'s domain!**
	- compose is not commutative. ($f \circ g \neq g \circ f$)

## one-to-one functions
- a function is **one-to-one** (injective/an injection) if and only if every element of its range has **only one** pre-image.
- only **one** element of the domain is mapped to any given **unique element** of the range.
	- domain + range have the same cardinality. (codomain may be larger)
- **todo again.**
- definitions:
	- $f$ is **strictly** increasing IFF $x > y \rightarrow f(x) > f(y)$ for all $x, y$ in domain.
	- $f$ is **strictly** decreasing IFF $x < y \rightarrow f(x) < f(y)$ for all $x, y$ in domain.
	- (if $f$ is **strictly** increasing or decreasing, then $f$ is one-to-one.)

## onto functions
- a function is **onto** (surjective/a surjection) if and only if its **range** is **equal** to its **codomain**.
- it maps the set $A$ onto (over, covering) the **entirety** of set $B$, not just a part of it.
- a function $f$ is a one-to-one correspondence, or a **bijection** (or reversible/invertible) if and only if it is **both** one-to-one and onto.

## inverse of a function

## identity of a function

## other important functions

