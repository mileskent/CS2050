[Living Schedule](https://docs.google.com/spreadsheets/d/1YJEb0nwD_ZhwjeUb3OkVpvrcvOUag-DTkvBzlKcSgkw/edit?gid=135811296#gid=135811296)

# Propositional Logic

A **proposition** is a declarative sentence that is either true or false, but not both
A **declarative sentence** is a sentence that declares something verifiable

Examples:
> 7 - 4 = 3
> prop
> 
> Odin is on our side
> prop
> 
> What is a Viking's favorite food?
> not prop
> 
> Every Saxon is under attack.
> prop
> 
> x+y=3
> not prop, because x and y vary

**Propositional Variables** are variables used to denote propositions.
* Typically: p, q, r, s, ...
* never use capitals as they are reserved for propositional functions

### Negation
Negation of $p$ denoted by $\neg p$
* *You must use $\neg$ to mean "not"
* same as !

Examples:
> 1. Ronnie likes Taco Bell
> $r$: "Ronnie likes Taco Bell"
> $\neg r$: "It is not the case that Ronnie likes Taco Bell", "Ronnie does not like Taco Bell"
> 
> 2. Thor's hammer is not named Mjölnir
> *always define prop vars as positive as below*
> m: "Thor's hammer is named Mjolnir"
> Negate original:
> $\neg(\neg m) \implies m$
> "Double negation rule"
### Truth Values and Truth Tables
1. Suppose we have a proposition $p$. Create a truth table for $p$ and $\neg p$

| $p$ | $\neg p$ |
| --- | -------- |
| T   | F        |
| F   | T        |

A **conjunction** of $p$ and $q$ is the statement "p and q"
* it is denoted as $p \land q$
* same as &&
* **Both** p and q must be true for $p \land q$ to be true

A **disjunction** of p and q is the statement "p or q"
* it is denoted as $p \lor q$
* it is same as ||
* $p \lor q$ is true whenever p is true, q is true, or both p, q are true

Examples:
> $p$: "Ronnie has 3 cats"
> $q$: "Ronnie does CrossFit"
> 
> 1. Find $p \lor q$
> Ronnie has 3 cats or Ronnie does CrossFit
> 2. Find $\neg p \land q$
> Ronnie does not have 3 cats and Ronnie does CrossFit

The **exclusive or** of p and q is the statement p XOR q
* $p \oplus q$
* Same as ^
* In order to eval to true, p can be true or q can be true, but not both
* $p \oplus q = (p \lor q) \land \neg(p \land q)$

# Conditionals & More!
Let p and q be propositions
* A statement in the form "if p, then q" is called a **conditional statement**
* written as $p \implies q$
* False when p is true and q is false, otherwise true
* p is called the hypothesis, sufficient condition
* q is called the conclusion or the necessary condition
* if sufficient condition happens, then the necessary condition *must* happen

### Truth Tables: $p \land q, p \lor q, p \oplus q, p \implies q$
- List all possible combinations of truth values
- If $n$ is the # of unique prop vars, then there are $2^n$ rows in the truth table

| p   | q   | $p \land q$ | $p \lor q$ | $p \oplus q$ | $p \implies q$ |
| --- | --- | ----------- | ---------- | ------------ | ----------------- |
| T   | T   | T           | T          | F            | T                 |
| T   | F   | F           | T          | T            | F                 |
| F   | T   | F           | T          | T            | T                 |
| F   | F   | F           | F          | F            | T                 |

### $p \implies q$
- if p, then q
- if p, q
- p is sufficient for q
- q if p
- q when p
- a necessary condition for p is q
- q unless ￢p
- p implies q
- p only if q (follows)
- a sufficient condition for q is p
- q whenever p
- q is necessary for p
- q follows from p
- q provided that p

### Converses, Inverses, Contrapositives
Given $p \implies q$
1. Converse: $q \implies p$
2. Inverse: $\neg p \implies \neg q$
3. Contrapositive: $\neg q \implies \neg p$

* $q \implies p = \neg p \implies \neg q$
* $\neg q \implies \neg p = p \implies q$

### Biconditional
* p iff q
* p $\iff$ q $\equiv$ (p $\implies$ q) $\land$ (q $\implies$ p)
* $p \iff q$

### Precedence of Logical Operators
1. $\neg$
2. $\land$
3. $\lor$
4. $\implies$
5. $\iff$

### Logic Puzzles
In the Vikings age, there lived 2 types of people
* Vikings, who are honorable and always tell the truth
* Saxons, who are not honorable so they never tell the truth
Determine who is a Viking or Saxon between Ragnar and Egbert who say the following:
Ragnar: I am a Viking only when Egbert is not
					^[only if]
Egbert: I am not a Saxon and Ragnar is a Saxon
p: Ragnar is a viking, $\neg p$: Ragnar is a saxon
q: Egbert is a viking, $\neg q$: Egbert is a saxon
Ragnar says: $p \implies \neg q$
Egbert sats: $q \land \neg p$

| p       | q       | $\neg p$ | $\neg q$ | $p \implies \neg q$ | $p \iff p \implies \neg q$Whether Ragnar statement and identity align | $q \iff q \land \neg p$ Whether Egbert statement and identity align | $(p \iff p \implies \neg q) \land (q \iff q \land \neg p)$ Ragnar aligned && Egbert Aligned, i.e. do they go together |
| ------- | ------- | -------- | -------- | ------------------- | --------------------------------------------------------------------- | ------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| T       | T       | F        | F        | F                   | F                                                                     | F                                                                   | F                                                                                                                     |
| ***T*** | ***F*** | ***F***  | ***T***  | ***T***             | ***T***                                                               | ***T***                                                             | T                                                                                                                     |
| F       | T       | T        | F        | T                   | F                                                                     | T                                                                   | F                                                                                                                     |
| F       | F       | T        | T        | T                   | F                                                                     | T                                                                   | F                                                                                                                     |
Based on the truth table, $p \equiv T, q \equiv F$

Now same situation, but different statements
Ragnar says: We are both Saxons
Egbert says: We are both Vikings
p: Ragnar is a viking, $\neg p$: Ragnar is a saxon
q: Egbert is a viking, $\neg q$: Egbert is a saxon
Ragnar says: $\neg p \land \neg q$
Egbert says: $p \land q$


| p   | q   | $\neg p$ | $\neg q$ | $\neg p \land \neg q$ | $p \iff (\neg p \land \neg q)$ | $p \land q$ | $q \iff (p \land q)$ | $[p \iff (\neg p \land \neg q)] \land [q \iff (p \land q)]$ |
| --- | --- | -------- | -------- | --------------------- | ------------------------------ | ----------- | -------------------- | ----------------------------------------------------------- |
| T   | T   | F        | F        | F                     | F                              | T           | T                    | F                                                           |
| T   | F   | F        | T        | F                     | F                              | F           | T                    | F                                                           |
| F   | T   | T        | F        | F                     | T                              | F           | F                    | F                                                           |
| F   | F   | T        | T        | T                     | F                              | F           | T                    | F                                                           |
No solution

If $>=1$ solution, "unable to determine"

Loki has heard of your exploits and wishes to honor you with a prize. However, being the deceiver that he is, he requires that you earn your prize by correctly determining which of three Chests actually holds the treasure. Only one Chest holds any treasure but the others are empty. You begin looking at the Chests and notice that Chests 1 and 2 are each inscribed with the message, "This Chest is empty." The third Chest is inscribed with the message, "The treasure is in Chest 2." Forseti, an honorable fellow, tells you that ***only one of these inscriptions are true***. Which Chest do you select?

p: Treasure is in chest one
q: Treasure is in chest two
r: Treasure is in chest two
1: I'm empty ($\neg p$)
2: I'm empty ($\neg q$)
3: Treasure in 2 ($q$)

1 is true: $(\neg p \land \neg q \land q) \equiv F$
2 is true: $(p \land \neg q \land \neg q) \equiv p \land \neg q \equiv T$
3 is true: $(p \land q \land q) \equiv p \land q \equiv F$

Treasure in one
### Definitions
**Compound proposition**: any expression formed from propositional variables using logical operators
**Tautology**: always true compound prop.
**Contradiction**: a compound prop. that is always false
**Contingency**: everything else

# Laws
![[Pasted image 20240821122530.png]]
### Conditional Disjunction Equivalence
$p \implies q \equiv \neg p \lor q$
### Absorption
$p \lor (p \land q) \equiv p$
$p \land (p \lor q) \equiv p$


### Prove Equivalence
$$p \equiv q \text{ iff: }$$$$
p \iff q \equiv T$$


### A Proof for DeMorgan's First Law
Law: $\neg (p \land q) \equiv \neg p \lor q$

| p   | q   | $\neg p$ | $\neg q$ | $p \land q$ | $\neg (p \land q)$ | $\neg p \land \neg q$ |
| --- | --- | -------- | -------- | ----------- | ------------------ | --------------------- |
| T   | T   | F        | F        | T           | F                  | F                     |
| T   | F   | F        | T        | F           | T                  | T                     |
| F   | T   | T        | F        | F           | T                  | T                     |
| F   | F   | T        | T        | F           | T                  | T                     |

Prove logical equivalences without truth tables by using logical equivalences

Show that $(p \land q) \implies (p \lor q)$  is a tautology

| $(p \land q) \implies (p \lor q)$      | Given              |
| -------------------------------------- | ------------------ |
| $\neg(p \land q) \lor (p \lor q)$      | Cond. Disj. Equiv. |
| $(\neg p \lor \neg q) \lor (p \lor q)$ | DeMorgan's         |
| $(\neg p \lor p) \lor (\neg q \lor q)$ | Asoc. & Comm.      |
| $T \lor (\neg q \lor q)$               | Negation law       |
| $T$                                    | Domination Law     |

## Satisfiability
A compound proposition is satisfiable if there is an assignment of truth vaues to its variables that make it true (when it is a tautology or contingency)
A compound proposition will be unsatisfiable if and only if it is a contradiction

# Predicates and Quantifiers
## Propositional Logic vs Predicate Logic
Example:
* x > 3
* x is the **subject**
* "less than 3" is the **predicate**
	* a property of x 
* "x < 3" can be represented by $P(x)$
	* P denotes the predicate, x is the variable 
	* $P(77) = 77<3$
* Let $Q(x, y)$ denote $x = 3-y$

## Universal Quantifier
* The universal quantification of P(x) is the statement "P(x) for all values of x in the domain"
* $\forall x P(x)$ "for all x in P(x)"
* $\forall$ is the universal quantifier

Must include domain in statements

## Existential Quantifier
* The existential quantification of P(x) is the proposition: “There exists an element x in the domain such that P(x).”
* "For some", at least one / it **exists**
* $\exists x P(x)$

## Uniqueness Quantifier
* "There exists a **unique**", i.e. only one
* $\exists ! x P(x)$
* e.g. $\exists ! x (x^2 = 9) \equiv F$, due to -3, 3
* $\exists ! x P(x) \equiv \exists x (P(x) \land \forall y (y \neq x \implies \neg P(y))$

$\forall, \exists$ takes precedent over all logical operators

## Quantifiers over Finite Domains
If the domain of a quantifier is finite, then you can convert quantified statements to propositional logic
e.g. if domain = {$x_1, x_2$}
$\forall x P(x) \equiv P(x_1) \land P(x_2)$
$\exists x P(x) \equiv P(x_1) \lor P(x_2)$


## Domain Shorthand example
$\forall x < 0 (x^2 < 0)$ "for all x less than 0, $x^2<0$" 

## De Morgan's Laws for Quantifiers

| Negation              | Equivalent Statement  | Negation is true when...            | Negation is false when...          |
| --------------------- | --------------------- | ----------------------------------- | ---------------------------------- |
| $\neg \exists x P(x)$ | $\forall x \neg P(x)$ | P(x) is false for every x           | There is an x that makes P(x) true |
| $\neg \forall x P(x)$ | $\exists x \neg P(x)$ | There is an x that makes P(x) false | P(x) is true for every x.          |

# Insert the new things from 1.5
Double quant: DeMorgan allows to move neg inside if swap quant.
Only have to be same x and y if in same scope. (Like programming)
# End

# Argument
**Argument**: a set of initial statements, called premises, followed by a conclusion.
An argument is valid if and only if in every case where all the premises are true, the conclusion is true.  Otherwise, the argument is invalid.
* An argument can be valid even if the conclusion is false. This can occur if one of the premises is false.  The requirement here for “valid” is that the conclusion is true when all premises are true.
* To prove a valid argument, show that the conjunction of the premises, leading to the conclusion is a tautology

| Argument Name          | Logical Representation                                        |
| ---------------------- | ------------------------------------------------------------- |
| Modus Ponens           | $p$<br>$p \implies q$<br>$\therefore q$                       |
| Modus tollens<br>      | $\neg q$<br>$p \implies q$<br>$\therefore \neg p$             |
| Addition               | $p$<br>$\therefore p \lor q$                                  |
| Simplification         | $p \land q$<br>$\therefore p$                                 |
| Conjunction            | $p$<br>$q$<br>$\therefore p \land q$                          |
| Hypothetical syllogism | $p \implies q$<br>$q \implies r$<br>$\therefore p \implies r$ |
| Disjunctive syllogism  | $p \lor q$<br>$\neg p$<br>$\therefore q$                      |
| Resolution             | $p \lor q$<br>$\neg p \lor r$<br>$\therefore q \lor r$        |


### Example
Want conclusion to be $b$
$\neg d \land e$
$c \lor d$
$\neg a \implies \neg c$
$\neg a \lor b$

| Statements               | Reasons                                              |
| ------------------------ | ---------------------------------------------------- |
| $\neg d \land e$         | Given                                                |
| $c \lor d$               | Given                                                |
| $\neg a \implies \neg c$ | Given                                                |
| $\neg a \lor b$          | Given                                                |
| $\neg d$                 | Simplification on $\neg d \land e$                   |
| $c$                      | Disjunctive Syllogism on $c \lor d$ and $\neg d$<br> |
| $a$                      | Modus Tollens $c$ and $\neg a \implies \neg c$       |
| $b$                      | Disjunctive Syllogism on $\neg a \lor b$ and $a$     |
| $\therefore b$           |                                                      |

## Fallacy

