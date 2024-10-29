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
![[Pasted image 20240821122530.png|300]]
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

Double quant: DeMorgan allows to move neg inside if swap quant.
Only have to be same x and y if in same scope. (Like programming)
 
| Statement  | The statement is true when…                         | The statement is false when…                                         |
| ---------- | --------------------------------------------------- | -------------------------------------------------------------------- |
| ∀x∀yP(x,y) | P(x,y) is true for all pairs x,y                    | There is a pair x,y that makes P(x,y) false                          |
| ∀x∃yP(x,y) | For each x, you can find a y that makes P(x,y) true | There is a value for x such that no value for y can make P(x,y) true |
| ∃x∀yP(x,y) | There is an x that makes P(x,y) true for every y    | There is not a single x that makes P(x,y) true for every y           |
| ∃x∃yP(x,y) | There is a pair x,y that makes P(x,y) true          | There are no pairs x,y that make P(x,y) true                         |
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

## Intro to Proofs: Direct Proof
**Theorem** a statement that can be shown to be true.
**Proof** a valid argument that establishes the truth of a theorem
**Lemma** less important theorems usually used to prove complicated theorems
**Corollary** a theorem that is established directly from a theorem that has been proved
**Conjecture** a statment that is being proposed as true
* Proving one makes it a theorem

Useful definitions and axioms
1. The integer n is even if there exists an integer k such that n = 2k, and 
2. n is odd if there exists an integer k such that n = 2k + 1. 
3. Closure of multiplication in integers:  The product of two integers is an integer.  
4. Closure of addition in integers: The sum of two integers is an integer
5. Closure of subtraction in integers:  The difference of any two integers is an integer
6. There is no closure of division (because of zero)
7. # 3-5 above also work for real numbers.  replace all instances of the word integer with real number
8. The real number r is rational if there exist integers p and q with q ≠ 0 such that r = p∕q.
9. A real number that is not rational is called irrational.
10. A number m is a perfect square iff there exists some integer k such that $m = k^2$

Proof Format
Introduction: Specify the type of proof technique you are using.  E.g. I proceed with a direct proof. If proving a theorem in the form of conditional. State “Assume the hyp. Is true” where hyp. Is the hypothesis of the conditional. Outline any other things you may need to use to build this proof. Body: Write your argument for your proof.  This step may typically contain multiple parts depending on both the proof technique and the theorem you are proving. Always define the domains of new variables you introduce See each proof technique for specifics. All simplification can be done in a single step. Any argument given should have a reason to go along with it.  e.g. Let n be odd.  By definition of odd, there's an integer k such that n = 2k+1. Conclusion. State “Therefore by (insert proof technique)…is proven.” where … was the thing you were proving. Be careful to specify the entire theorem and not just the conclusion.

**Direct Proof** is a type of proof that directly leads to a conclusion, i.e. $p \implies q$. The assumption is that p is true, and we prove that q must follow.

**Two Column Proof** a proof with statements and reasons. 

$\mathbb{Z}$ set of int
$\mathbb{R}$ set of real
$\mathbb{Q}$ set of rational
$\mathbb{C}$ set of complex

Example:
Give a direct proof of "If n is an even integer then $n^2$ is an even integer"

Pf: 
I proceed directly and assume $n$ is even.

| Statement                                  | Reasons                                   |
| ------------------------------------------ | ----------------------------------------- |
| n is even                                  | Premise                                   |
| Let n = 2k, where $k \in \mathbb{Z}$       | Definition of even<br>                    |
| $n^2 = 4k^2$                               | Square both sides of the equation         |
| $n^2 = 2(2k^2)$                            | Factoring out a 2                         |
| Let $j = 2k^2$ for some $j \in \mathbb{Z}$ | Closure of multiplication in $\mathbb{Z}$ |
| $n^2 = 2j$                                 | Substitution                              |
| $n^2$ is even                              | Definition of even                        |
We see that if $n$ is even, then $n^2$ is also even is proven. Have proved $p \implies q$

**Paragraph proof** do your proof in a paragraph.

You write a box at the end or smth.

## Proof by Contraposition
$p \implies q$ goes to $\neg q \implies \neg p$

#### Example 1:
*Prove that if $n^2$ is an even and n is an integer, then n is even*
This proof is probably easier using the contrapositive

n is odd $\implies$ $n^2$ is odd
This is the contrapositive

$n = 2k + 1$
$n^2 = 4k^2 + 4k + 1$
$n^2 = 2(2k^2+ 2k) + 1$
$z = 2k^2 +2k$
$n^2 = 2z + 1$
$n^2$ is odd

Not all full proof btw, just showing how you can use the contrapositive

#### Example 2
Actual proof
Prove that if n = ab, where a and b are positive integers, then a ≤ √n or b ≤ √n.

We will be using a contrapositive
n = ab
$\sqrt{n} = \sqrt{a}\sqrt{b}$
dead end, so use cp

Scratch
!( a ≤ √n or b ≤ √n) $\implies$ !(n = ab)
 (a $>$ √n and b $>$ √n) $\implies$ n != ab
 (ab $>$ b√n and b$\sqrt{n}$ $>$ $√n^2$ ) $\implies$ n != ab
 (ab $>$ b√n and b$\sqrt{n}$ > n ) $\implies$ n != ab

Pf:
I proceed by proving the contrapositive which states
if a > $\sqrt{n}$ and $b > \sqrt{n}$, then n != ab, for all a, b, $\in \mathbb{Z}$

| 1   | $a>\sqrt{n}$             | Premise               |
| --- | ------------------------ | --------------------- |
| 2   | $b> \sqrt{n}$            | Premise               |
| 3   | $ab > b\sqrt{n}$         | mult 1 by b           |
| 4   | $b\sqrt{n} > \sqrt{n}^2$ | mult 2 by $sqrt{n}$   |
| 5   | $b\sqrt{n} > n$          | simplify 4            |
| 6   | ab > n                   | Transitivity on 3 & 5 |
| 7   | $ab \not = n$            | def of >              |
Therefore, our proof by contrapositive suceeded, and thus, the equivalent "For all a, b $\in \mathbb{Z}$, if n = ab then $a $\leq$ $\sqrt{n}$ || b $\leq$ $\sqrt{n}$" is true.
$\square$

## Proof by Contradiction
All props are either true or false
When trying to prove p is true, assume that p is false. Given this, break some equality or property of mathematics. Thus, p is true.

We'd assume if p then q is false
Giving us: $\neg(p\implies q)$
Leading to $p \land \neg q$ (with simplification) is true

#### Example 1
Give a proof by contradiction of the theorem “If 5n + 2 is odd, then n is odd.”

In a proof by contradiction, assume $p \land \neg q$ is true, and find a contradiction.

Pf:
I proceed using a proof by contradiction, where I assume 5n + 2 is odd, and n is even.


| 1   | 5n+2 is odd                       | premise                                                                                                 |
| --- | --------------------------------- | ------------------------------------------------------------------------------------------------------- |
| 2   | n is even                         | premise                                                                                                 |
| 3   | n = 2k, for some k                | def of even                                                                                             |
| 4   | 5n = 10k                          | multi (3) by value of 5                                                                                 |
| 5   | 5n + 2 = 10k + 2                  | add 2 to (4)                                                                                            |
| 6   | 5n + 2 = 2(5k + 1)                | factor (5)                                                                                              |
| 7   | 5k + 1 = z, for z in $\mathbb{Z}$ | ***closure mult + add in z, meaning that multiplication and addition with integers, gives an integer*** |
| 8   | 5n + 2 = 2z                       | sub (7) into (6)                                                                                        |
| 9   | 5n + 2 is even                    | def. even                                                                                               |
By (9) and (1), 5n+2 is both even and odd, which is a contradiction. Therefore, the original assumption that n is even is false, and "if 5n + 2 is odd, then n is odd" is proven.
$\square$

#### Example 2
Show that at least four of any 22 days must fall on the same day of the week.

Scratch:
Assume not p.
At most, 3 of any 22 days must fall on the same day of the week.
3 * 7 = 21
Contradiction

Pf:
Using proof by contradiction, I assume "At most, 3 of any 22 days must fall on the same day of the week".
Since there are 7 named days, and at most 3 fall on the same day, we have used at most 
3x7=21 days, which contradicts that we have 22 days. Thus, our assumption was wrong, and at least 4 of any 22 days must feel on the same day of the week"
$\square$

#### Example 3
Prove that  √2 is irrational by giving a proof by contradiction
Pf: I proceed using contradiction and assume $\sqrt{2} \in \mathbb{Q}$
We also note that a rational number can be written in simplest form.
Thus, we have $\sqrt{2} = \frac{p}{q}$ where $p, q \in \mathbb{Z}$, $q \not = 0$, and $p, q$ have no common factors
$2 = \frac{p^2}{q^2}$, by squaring
$2q^2 = p^2$
Thus $p^2$ is even, by closue prop. and def of even
Since $p^2$ is even, p is also even. And p = 2k for some $k \in \mathbb{Z}$
Then through sub, we have $2q^2 = (2k)^2$
$2q^2 = 4k^2$
$2q^2 = 2(2k^2)$
$q^2 = 2k^2$
and thus, $q^2$ is even
Thus q is even, and so q = 2m for some $m \in \mathbb{Z}$
We see p and q both have a common factor of 2, which contradicts the premise that they had no common factors.
Thus, our assumption that $\sqrt{2}$ is ration is false, and we are left with $\sqrt{2}$ as irrational.

#### Example 6
Let a and b be positive integers with the property that ab+1 divides a^2+b^2. Show that (a^2+b^2)/ (ab+1) is a perfect square.

Pf:
Just watch the lecture, view the notes later
$\square$


# When to use direct vs indirect proofs
Simple suggestion:  Just try it.  Start with a direct proof and see what happens.  Do scratch work.  Never try to write a proof before doing scratch work. 
Longer suggestion:  Hypotheses that can’t be easily reasoned from might suggest that you use an indirect proof. Look back to example 3.

**Vacuous Proof**, with $p \implies q$, if $p \equiv F$, then the original statement must be true, regardless of q.

**Trivial Proof**
with $p \implies q$, whenever $q \equiv T$, then the original statement must be true, regardless of q.

**Backwards Reasoning (Strategy)**
This is a strategy that you can use in your scratch work. 
- Suppose you're proving that q is true from a list of givens.
- However, you're unable to figure out where to start based on those givens.
- In this case, you might start with q and work backwards to something that you can prove using your givens.
- Then when you write up your formal proof, you can do all the steps backwards.

Example:
Prove that (x+y)/2 >  √(xy) for all distinct positive real numbers x,y

$x \not = y, x \geq 0, y \geq 0$
Scratch:
Start assuming conclusion is true.
$\frac{x + y}{2} > \sqrt{xy}$
$x + y > 2\sqrt{xy}$
$(x + y)^2 > 4xy$
$x^2 + y^2 + 2xy > 4xy$
$x^2 + y^2 - 2xy > 0$
$(x - y)^2 > 0$
Not equal, thus LHS will be gt0
Now for the Pf, just go backwards

**Pf:**
Let $x, y \in \mathbb{R}$, be arb. where $x \not = y$. Then $x - y \not = 0$.
Thus, $(x - y)^2 > 0$ * since the square of a nonzero real number is postive.

| S                                | R          |
| -------------------------------- | ---------- |
| 1) $(x - y)^2 > 0$               | By *       |
| 2) $x^2 + y^2 - 2xy > 0$         | Distr.     |
| 3) $x^2 + y^2 + 2xy > 4xy$       | Add 4xy    |
| 4) $(x + y)^2 > 4xy$             | Factor LHS |
| 5) $xy > 2\sqrt{xy}$             | sqrt 4)    |
| 6) $\frac{x + y}{2} > \sqrt{xy}$ | div by 2   |
We see that whenever x, y are distinct real \# s, then $\frac{x + y}{2} > \sqrt{xy}$
$\square$

## Exhaustive Proofs
In an exhaustive proof we try every possibility of the proposition.  If all cases are true, then the proposition is proven.

e.g. 
Prove that $(n + 1)^3 ≥ 4^n$ if n is a positive integer with n ≤ 3.

**Pf:**
I proceed by exhaustion
Let $P(n) \equiv (n + 1)^3 ≥ 4^n$
**Case: P(1)**
$P(1) \equiv (1 + 1)^3 ≥ 4^1 \equiv 8 \geq 4 \equiv T$

**Case: P(2)**
$P(2) \equiv (2 + 1)^3 ≥ 4^2 \equiv 27 \geq 16 \equiv T$

**Case: P(3)**
$P(3) \equiv (3 + 1)^3 ≥ 4^3 \equiv 64 \geq 64 \equiv T$

$\therefore$ By exhaustion, $P(n)$ is true for all pos. int. where $n \leq 3$
$\square$

## Proof By Cases
A proof by cases is used when you must break your proof up into different cases due to a single argument not being enough to prove all cases.
e.g.
Prove that if n is an integer, then $n^2 ≥ n$.
$n = 0\ \implies \ n^2 = 0 = n \implies n^2 = n$
$n <  0 \implies n \leq -1 \implies n^2 \geq 0 \implies n^2> 01 \geq n \implies n^2 \geq n$
$n>1 \implies n^2 > n$

**Pf:**
Assume $n \in \mathbb{Z}$ is arbitrary. We have 3 cases: $n = 0, n\leq-1, n\geq1$
Case: $n = 0$
Since $n = 0$, $n^2 = 0= n \implies n^2 = n \implies n^2 \geq n$
Case: $n \leq -1$
$n^2 \geq 0$ since the square of an int is nonnegative. We know $0 \geq -1 \geq n$ by transitivity, we have $n^2 \geq n$
Case: $n \geq 1$
Mult ineq by $n$ gives $n^2 \geq n$
Since we have proven all cases, then the original statement is true.
$\square$

## Without Loss of Generality
Sometimes we can eliminate cases inproof when the cases are very similar.
e.g.
$x>0, y<0$ vs $y>0, x<0$
You can say WLOG because the proofs for these cases with be exactly the same, except the x's and y's with be flipped.

## Induction
Let P(n) be a proposition. To prove P(n) for all integers k.
1. Basis step where we show P(1)
2. Inductive step where we show that if P(k) then P(k+1)

Ex:
Prove that 
$\sum^{n}_{j=1} j \frac{n(n+1)}{2}, n\in \mathbb{Z}^{+}$

Pf:
Let P(n) be $\sum^{n}_{j=1} j \frac{n(n+1)}{2}$. I use inductionto show P(n) is true for all int. n >= 1.

Basis:
P(1) is true bc $1 = \frac{1\cdot2}{2} = \frac{1(1 + 1)}{2}$

Inductive Hypothesis:
Assume that $P(k) = 1 + 2 + ... + k = \frac{k(k+1)}{2}$ is true for a fixed arbitrary integer $k \geq 1$


Inductive Step:

| 1 + 2 + ... k           | $\frac{k(k+1)}{2}$           |     |
| ----------------------- | ---------------------------- | --- |
| 1 + 2 + ... k + (k + 1) | $\frac{k(k+1)}{2} + (k + 1)$ |     |
| """"                    | $\frac{k^2 + k + 2k + 2}{2}$ |     |
| """"                    | $\frac{k^2 + 3k + 2}{2}$     |     |
| """"                    | $\frac{(k+1)(k+2)}{2}$       |     |
| """"                    | $\frac{(k+1)((k+1)+1)}{2}$   |     |
We see that $P(k) \implies P(k+1)$ is true, completing the inductive step.
By math induction, P(n) is true for all int n >= 1
$\square$

Make sure to add the $(k+1)^{\text{th}}$ term, not just k + 1

Let a be constant and r be a common ratio
$\sum_{j=0}^{n} ar^j = a + ar + ar^2 + ... + ar^n = \frac{ar^{n+1}-a}{r-1}, r \not = 1$

Pf: Let  P(n) be $\sum_{j=0}^{n} ar^j = a + ar + ar^2 + ... + ar^n = \frac{ar^{n+1}-a}{r-1}, r \not = 1$. We us math. ind. to prove P(n) for all in $n \geq 0$

Basis Step:
P(0) is true because $\sum_{j=0}^{0} ar^0 = ar^0 = \frac{ar-a}{r-1}, r \not = 1$

Inductive Hypothesis:
Assume $\sum_{j=0}^{k} ar^j = a + ar + ar^2 + ... + ar^k = \frac{ar^{k+1}-a}{r-1}, r \not = 1, k \geq 0$

Inductive Step:

| $\sum_{j=0}^{k} ar^j = a + ar + ar^2 + ... + ar^k = \frac{ar^{k+1}-a}{r-1}, r \not = 1, k \geq 0$ | IH             |
| ------------------------------------------------------------------------------------------------- | -------------- |
| $"""" = a + ar + ar^2 + ... + ar^k + ar^{k+1} = \frac{ar^{k+1}-a}{r-1} + ar^{k+1}$                | add $ar^{k+1}$ |
| $\sum_{j=0}^{k+1} ar^j = \frac{ar^{k+1}-a}{r-1} + ar^{k+1}$                                       | Summation def  |
| $"""" = \frac{ar^{k+1}-a + ar^{k+1}(r-1)}{r-1}$                                                   | Simplify       |
| $"""" = \frac{ar^{k+1}-a + ar^{k+1+1}-ar^{k+1}}{r-1}$                                             | Distributive   |
| $"""" = \frac{-a + ar^{k+1+1}}{r-1}$                                                              | Simplify       |
| $"""" = \frac{ar^{(k+1)+1} - a}{r-1}$                                                             | Commutative    |

Thus $P(k) \implies P(k + 1)$ is proven, completing the inductive step. By induction, P(n) is true for all int. $n \geq 0$

## Induction with Inequalities and Division
Use backwards reasoning in induction proofs in the SW to get the answer


~
Prove that $n$ people can divide the cake fairly.

n = 1 -> whole cake
n = 2 -> 1/2 of whole cake
n = 3 -> 1/3 of each 1/2
n = 4 -> 1/4 of each 1/3

Pf:
Let $P(n)$ be that $n$ people can divide a cake fairly, so that each person has $\frac{1}{n}$ of the cake. I use induction to prov $P(n)$ is true for all integers $n \geq 1$

Basis:
$P(1)$ is true because one person would get the entire cake. 1/1

Inductive Hypothesis:
Assume $k$ people can divide the cake equally into $\frac{1}{k}$ pieces where $k \in \mathbb{Z}^{+}$

Inductive Step:
Consider $k$ people, by the inductive hypothesis, they split the cake such that each person has $\frac{1}{k}$ of the cake. Let another person join, now we have $k+1$ people. We will take $\frac{1}{k+1}$ of each existing person's slice.
In order words, they take $\frac{1}{k+1}\cdot\frac{1}{k}$ of the original cake, from each of the original $k$ people.
Since this occurred k times, they now have $k\frac{1}{k+1}\cdot\frac{1}{k} = \frac{1}{k+1}$. Each of the original $k$, originally had $\frac{1}{k}$ from which we took away $\frac{1}{1+k}$. Meaning $\frac{1}{k} - (\frac{1}{k+1} \cdot \frac{1}{k}) = \frac{1}{k+1}$ each other person also has $\frac{1}{k+1}$ of the original cake.
Thus by math ind, $P(k) \implies P(k+1)$; $\forall n\in \mathbb{Z}^{+} P(n)$
$\square$

# Strong Induction
Induction but you do $(P(1) \land P(2) \land ... P(k)) \implies P(k+1)$
You can also be like $P(j)$ for $j \in$ domain such that $b <= j <= k$

# Sets
An *unordered* collection of distinct objects
- Made of elements
- Denoted by capital letters
- $a\in A$ means the element $a$ is in the set
- $a \not \in A$ means the element $a$ is not in the set
- $A = \{1, 2, 3, 4\}$
Note: Before performing operations, reduce your sets so they contain no duplicates!!!
### Set Builder Notation
- All positive even integers less than a thousand
	- $\{x \mid x \in \mathbb{Z}^{+} \land \text{x is even } \land x < 1000\}$
### Relevant Sets
- $\mathbb{N} = \{0, 1, 2, 3, ...\}$ 
- $\mathbb{Z} = \{..., -1, 0, -1, ...\}$ 
- $\mathbb{Q} = \{\frac{p}{q} \mid p,q \in \mathbb{Z} \land q \not = 0\}$
- $\mathbb{R} = \{..., -1.223, 0, 2, ...\}$ 

Note: $\{\mathbb{N}, \mathbb{R}, \mathbb{C}\}$ has only 3 elements, even though each element itself is an infinite set, and even though they overlap with one another. "A list of lists"

### Equal set
- $A = B$
- $(A=B) \iff \forall x (x \in A \iff x \in B)$
- $(A \subseteq B \land B \subseteq A) \iff A = B$
### Empty Set
$\varnothing = \{\}$ contains nothing
note $\varnothing \not = \{\varnothing\}$
### Singleton
A set with one element
note: $1 \not = \{1\}$
### Venn Diagrams
There is a universe set $U$, usually represented by a rectangle.

### Subset
- A is a subset of B
	- $A \subseteq B$
	- Could be equal
- A is a proper subset of B
	- $A \subset B$
	- Cannot be equal

### Superset
Exist, but we don't really use the notation. Like how $<, >, \geq, \leq$ works
$B \supseteq A$
$B \supset A$


# Functions
- Definition 1: Let A and B be nonempty sets. A function f from A to B is an assignment of exactly one element of B to each element of A. We write f (a) = b if b is the unique element of B assigned by the function f to the element a of A. If f is a function from A to B, we write f : A → B.
- Definition 2: If f is a function from A to B, we say that A is the domain of f and B is the codomain of f. If f (a) = b, we say that b is the image of a and a is a preimage of b. The range, or image, of f is the set of all images of elements of A. Also, if f is a function from A to B, we say that f maps A to B.
- You must specify the domain, codomain and the mapping of elements of the domain to elements in the codomain when defining a function. The range does not need to be explicitly specified
- Two functions are equal when they have the same domain, codomain, and map each element of their common domain to the same element in their common domain.  
	- Changing the domain, codomain or mapping creates a new function

### Ex:
1. What is the domain, codomain, and range of a function that assigns the last two bits of a bit string of length 2 or greater to that string.  (E.g. f(11010) = 10)
- Domain
	- The *set* of all bit strings $\geq$ 2
- Codomain
	- {11, 01, 10, 00}
- Range
	- {11, 01, 10, 00}
Range and Codomain here happen to be equal

2. Let f : R→ R assign the square of a real number to this real number. Then, f (x) = $x^2$ .. What is the domain, codomain, and range of f.
* Domain
	* $\mathbb{R}$
* Codomain
	* $\mathbb{R}$
* Range
	* $\mathbb{R} - \mathbb{R}^{-}$
set operators have to order of precedence, except with union, intersect, and remove
1. ()
2. ~ complement
3. Everything else left to right

### Real-valued and Integer-Valued
- A function is called real-valued if its codomain is the set of real numbers
- it is called integer-valued if its codomain is the set of integers.
- You can add and multiply both real-valued and integer-valued functions

![[Pasted image 20241008082029.png]]
A not necessarily a set of numbers

### Ex
Let f1 and f2 be functions from R to R such that f1 (x) = x2 and 
f2 (x) = x − x2 . What are the functions f1 + f2 and f1 f2 ?

$(f_1 + f_2)(x) = f_1(x) + f_2(x) = x^2 + x - x^2 = x$
$(f_1 - f_2)(x) = f_1(x) - f_2(x) = x^2 - x + x^2 = 2x^2-x$

# One-to-One Functions
Some functions never assign the same value to two different domain elements. These functions are said to be one-to-one.
- At most one mapping from the domain for every element of the codomain
- Note that a function f is one-to-one if and only if f (a) ≠ f (b) whenever a ≠ b, and vice versa.
- Note 2 in the codomain below

![](https://lh7-rt.googleusercontent.com/slidesz/AGV_vUdIlsuNJGqV81tpa465oTgKUMSMv9bB1LBt2caguXrkt0L1F117_4ZkTseH6R6jorMiluJ3SNYFJSkNHm0lITSz9ejTjWgLIPjrmYcUYV0bCzfhhh2605BCBB3fAGvRvK13_cp5TGrWmXJ11LbZITwOYvbnsH0a=s2048?key=2mZ9gCSz0BcdwA6VqOVR1g)
Example: Determine whether the function f (x) = x2 from the set of integers to the set of integers is one-to-one.
- False, every value square is also hit by its opposite squared
- Assume domain if not given, to be the most reasonable real numbered domain or something similar.

Example: Prove that the function f (x) = x + 1 from the set of real numbers to itself is one-to-one.
- You need to show that if f(a) = f(b), then a = b
By inspection it is 1-1 because it just shifts any value in the domain up by one.
f: R->R
Pf:
Let a,b $\in \mathbb{R}$ be arbitrary and assume f(a) $\not =$ f(b). Then by def of f(x):
a + 1 = b+1
a=b
Since f(a)=f(b) -> a=b f(x) is 1-1, by definition

A function has to map all element in the domain to something in the codomain. Let the domain be R, the codomain be R. then f(x) = 1/x is not a function.

# Increasing and Decreasing
Given $x < y$, and x, y are in the proper domains, f is called:
- increasing if f (x) ≤ f (y)
- strictly increasing if f (x) < f (y)
- decreasing if f (x) ≥ f (y)
- strictly decreasing if    f (x) > f (y)

Its defined exactly as what you'd think it would mean.
Not all function match.
Horizontal line would be both. Vertical line would be neither.

Example: show that  $f(x) = x^2$  from R+ to R+ is strictly increasing.
let x, y be positive reals and $x<y$
$x<y$
$x^2 < xy$
$xy < y^2$
$x^2 < y^2$
$f(x) < f(y)$
$\therefore x<y \implies f(x) < f(y)$

# Onto Functions
A function f from A to B is called onto, or a surjection, if and only if for every element b ∈ B there is an element a ∈ A with f (a) = b. A function f is called surjective if it is onto.
- The range of the function equals the codomain. (every element in codomain is used.)
- All elements of codomain are hit at least once
- range = codomain
![](https://lh7-rt.googleusercontent.com/slidesz/AGV_vUcjeKre7qiIh_XTjfxl8Qp6v-j6rVfncyVcohzNJi0L4zzvbZjqTcoeR9053iyVuMBbpWqjlIxuxHAP5wJazMLXu_PO_cCct29AHFbKM0FoeKzsobmqBuDFDcLB8x3TH9c0LdWeB3kUX91IDX5zfcQcb3Nv6Z5k=s2048?key=2mZ9gCSz0BcdwA6VqOVR1g)

Let f be the function from {a, b, c, d} to {1, 2, 3} defined by f (a) = 3, f (b) = 2, f (c) = 1, and f (d) = 3. Is f an onto function?
Yes.

Is the function f (x) = $x^2$ from the set of integers to the set of integers onto?
No. Not onto. All non square integers will be missed from the codomain. For example: 2,$\mathbb{Z}^{-}$


Is  f (x) = x + 1 from the set of integers to the set of integers onto?
- Consider an arbitrary element y ∈ B and find an element x ∈ A such that f (x) = y.
Let y in Z (codomain). Try to find x in the domain that makes x+1=y. 
x = y-1 <- Guaranteed to be in domain? (Yes for this case bc closure).

# Bijections
The function f is a one-to-one correspondence, or a bijection, if it is both one-to-one and onto. We also say that such a function is bijective. Exactly one domain element for every codomain element.
- Bijections have special properties
- All bijections have an inverse function
![[Pasted image 20241008085642.png|500]]

# Inverse
Let f be a one-to-one correspondence from the set A to the set B. The inverse function of f is the function that assigns to an element b belonging to B the unique element a in A such that f (a) = b. The inverse function of f is denoted by f −1 . Hence, f −1(b) = a when f (a) = b.
![](https://lh7-rt.googleusercontent.com/slidesz/AGV_vUdCu6jqo0kDgzIlMMdR2flSiRz3IQ2y3gfK171UL4CLeuLbxSJtwwxwzjEKI6PGkxoZki00HAcNqfZJvSE2zwOOSZRU9hlaidKJyJB9JA7VFJKObEHzACyj-tqfP_Jv4Kv1PSO9ySXJQaY0ymAv3Sqy_HxiANtG=s2048?key=2mZ9gCSz0BcdwA6VqOVR1g)

Let f : Z → Z be such that f (x) = x + 1. Is f invertible, and if it is, what is its inverse?
f(x) is a bijection $\implies$ f(x) is invertible

Get inverse.
Replace f(x) with x. Replace x with $f(x)^{-1}$

Let f be the function from R to R with f (x) = $x^2$. Is f invertible?
f(x) not a bijection

# Composition of Functions
Let g be a function from the set A to the set B and let f be a function from the set B to the set C. The composition of the functions f and g, denoted for all a ∈ A by f ◦g, is the function from A to C defined by
(f ◦ g)(a) = f (g(a)).
![](https://lh7-rt.googleusercontent.com/slidesz/AGV_vUdHPYRlsSLoCYFKlsSDZ6u7ieSKCrKv5teiTEq-YRWQ9GLmMybFousDCzg-pubTYhTDGk6rO4vlJFF29Vton-2WFW5-pzKIrN1637cMFRB5xAOaY0xOPaYehN05fM8QbkFSd3vQww0VVr0cCktduQaw1-m5Yilp=s2048?key=2mZ9gCSz0BcdwA6VqOVR1g)

Let g be the function from the set {a, b, c} to itself such that g(a) = b, g(b) = c, and g(c) = a.
Let f be the function from the set {a, b, c} to the set {1, 2, 3} such that   f (a) = 3, f (b) = 2, and f (c) = 1. 
What is the composition of f and g, and what is the composition of g and f ?
a -> 3, c->1,b->2
a->undefined; g(f(x)) undefined, so the composition does not exist

Let f and g be the functions from the set of integers to the set of integers defined by
f (x) = 2x + 3 and g(x) = 3x + 2. 
What is the composition of f and g?
$f(g(x)) = 2(3x+2) + 3 = 6x + 4 + 3 = 6x + 7$
What is the composition of g and f ?
$g(f(x)) = 3(2x+3) + 2 = 6x + 9 + 2 = 6x + 11$

$f(g(x)) \not = g(f(x))$, but it is possible, just in general

# Floor and Ceiling Functions
### Floor
largest integer less than or equal to $x$
$\lfloor x \rfloor$

### Ceiling
smallest number greater than or equal to $x$
$\lceil x \rceil$

# Big-O Notation
### Definition
Memorize:
![](https://lh7-rt.googleusercontent.com/slidesz/AGV_vUcrthtaYtDyxYZDDJspf2hqD_nNpS0j-5_h_67DxhGZ56sRiBrWlRgtMkFK0K85y85-fSAalHLtgYvMe5bHJNVxcMbW65C2b3pyt95CH4g4Z22vAA43xjiRSapC107bXHctTGYMunzeRDeGvbu1qSMeRD4hN7kkj2qAUIPFo6k16YmkYEeDD38=s2048?key=DF8c9eFAL488vdpkHkTjbw)
C and k are called witnesses to the relationship f(x) is O(g(x)).
- Trying to find an upper bound estimate of our function, i.e. if $f(x)$ is a quadratic, its big O is $O(x^2)$
	- In this class, not trying to find smallest upper bound, unlike in computing
	- We are just finding an upper bound
	- $p(x^n) = O(x^n)$
- k for when g(x) is growing faster than f(x) and is $\geq$ than f(x)
	- k doesn't need to be the first x where this occurs, just one of them
- What C means is that we only care about the parent function, i.e. we consider if $f(x) = 3x^2$ then $C = 3$ where $g(x) = x^2$, so that the functions are comparable.

Pf:
show that $f(x) = x^2 + 2x + 1$ is $O(x^2)$
I proceed directly. (This proof only works for polynomials)
Prove each term is $O(x^2)$
$x^2 \leq \_x^2$
$2x \leq \_x^2$
$1 \leq \_x^2$
======
$|x^2| \leq |1x^2|, \forall x > 0$
$|2x| \leq |2x^2|, \forall x > 1$ Did not have to pick this value, its just easier
$|1| \leq |1x^2|, \forall x > 1$
$x^2 + 2x + 1 \leq 4x^2, \forall x > 1$
Thus C=4, k=1 as witnesses: $f(x)$ is $O(x^2)$
$\square$

## Big-O Complexity
1. $O(n^n)$
2. $O(n!)$
3. $O(2^n)$
4. $O(n^2)$
5. $O(n\ log\ n)$
6. $O(n)$ 
7. $O(log\ n)$
8. $O(1)$

Have to memorize the theorem numbers.

# Cardinality of Sets
#### Equal sets
Two sets A and B have the same cardinality if and only if you can find a bijection from A to B. When A and B have the same cardinality, we write |A| = |B|


#### Different  Sets
If there is only a one-to-one function from A to B, the cardinality of A is less than or the same as the cardinality of B and we write 
|A| ≤ |B|. 
Furthermore, if there is a one-to-one function from A to B but there is no bijection, then |A| < |B|

#### Countable
- Finite sets are countable
- The set of positive integers is countable
- Any infinite set that has the same cardinality as the set of of positive integers is countable.
- When an infinite set S is countable, we denote cardinality of S by $\aleph_0$ (read as aleph null). |S| = $\aleph_0$

#### Hilbert's Grand Hotel
Consider a hotel with a finite number of rooms.  Suppose all rooms are occupied. A new guest arrives.  Then there is no way to accommodate this guest without evicting a current guest.

Hilbert's Grand Hotel: Consider a hotel with an infinitely countable number of rooms.  Assume all rooms are occupied. Suppose a new guest arrives.  Show that this guest can always be accommodated. In other words, show that we can always find a room for this guest without evicting a current guest.

#### Cantor's Diagonalization Technique
The one that proves $\mathbb{Q}$ is countable with the diagonals
### Uncountable Sets
Show that the set of real numbers is uncountable.  Hint: Show that (0,1) as a subset of R is uncountable which would show R is also uncountable

# [[Division]]

# [[Modular Arithmetic]]
# [[Integer Representation]]
# [[Base Conversion]]
Note: on exam, must use base conversion algorithm, not guess and check.
# [[Prime]]
