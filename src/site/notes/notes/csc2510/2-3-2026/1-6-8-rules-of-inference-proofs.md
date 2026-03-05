---
{"dg-publish":true,"permalink":"/notes/csc2510/2-3-2026/1-6-8-rules-of-inference-proofs/"}
---

# 👟 SUMMARY
- **proofs** are statements that form an argument.
- **rules of inference** are patterns of deductions (hypotheses to conclusions)
	- ![inference-rule.png|169x86](/img/user/zimages/2-3-2026/inference-rule.png)
- some rules to know: rule of **addition**, **simplification**, **conjunction**, **modus ponens**, **modus tollens**, **hypothetical syllogism**, **disjunctive syllogism**
- **formal proofs** = sequence of steps (inference rules or prev. established statements) to create a new statement

## intro
- what is a **proof**?
	- a sequence of statements that form an **argument**.
	- must be **correct** (well-reasoned, logical, valid) and **complete** (clear, detailed).
		- establishes the **truth** of a mathematical statement.
		- **correctness** = prevention from **fooling** ourselves
		- **completeness** = allows anyone to **verify** the result.
## rules of inference
- **rules of inference** = **patterns** of **logically valid deductions** from hypotheses to conclusions
- review "**inference rules**" and "**proof methods**"
- **inference rule** = pattern establishing that if we **know** a set of hypotheses are true, then a certain **conclusion** statement is true.
	- each logical inference rule corresponds to an implication that it is a **tautology**.
	- ![inference-rule.png|169x86](/img/user/zimages/2-3-2026/inference-rule.png)
	- corresponding tautology: $((Hypoth.\,1) \land (Hypoth.\,2) \land \ldots) \rightarrow conclusion$
- some inference rules:
	- rule of addition $$\frac{p}{\therefore p \lor q}$$
		- it is below freezing now. therefore, it is either below freezing or raining now.
	- rule of simplification $$\frac{p \land q}{\therefore p}$$
		- it is below freezing and raining now. therefore, it is below freezing now.
	- rule of conjunction 
		- $p$ / $q$ // $\therefore p \land q$
		- it is below freezing. it is raining now. therefore, it is below freezing and it is raining now.
	- rule of modus ponens
		- "the mode of affirming"
		- $p$ / $p \rightarrow q$ // $\therefore q$
		- if it snows today, then we will go skiing **AND** it is snowing today **IMPLIES** we will go skiing
	- rule of modus tollens
		- "the mode of denying"
		- $\lnot p$ / $p \rightarrow q$ // $\therefore \lnot p$
			- if it snows today, then we will go skiing **AND** it is not snowing today **IMPLIES** we will not go skiing
	- rule of hypothetical syllogism
		- $p \rightarrow q$ / $q \rightarrow r$ // $\therefore p \rightarrow q$
	- rule of disjunctive syllogism
		- $p \lor q$ / $\lnot p$ // $\therefore q$
## formal proofs
- a **formal proof** of a conclusion $C$, given premises $p_1, p_2, \ldots , p_n$ consists of a **sequence of steps**, each of which applies some **inference rule** to **premises** or **previously proven statements** to yield a new true statement.
	- a proof demonstrates that **if** the premises are true, **then** the conclusion is true.
- example
	- premises:
		- $(p \lor r) \rightarrow q$
		- $q \rightarrow t$
		- $r$
	- conclusion:
		- $t$
	- **proof**:
		1. $r$ (premise 3)
		2. $p \lor r$ (addition, *1*)
		3. $(p \lor r) \rightarrow q$ (premise 1)
		4. $q$ (modus ponens, *2*, *3*)
		5. $q \rightarrow t$ (premise 2)
		6. $t$ (modus ponens, *4*, *5*)
