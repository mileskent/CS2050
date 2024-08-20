[Living Schedule](https://docs.google.com/spreadsheets/d/1YJEb0nwD_ZhwjeUb3OkVpvrcvOUag-DTkvBzlKcSgkw/edit?gid=135811296#gid=135811296)

# Propositional Logic

A **proposition** is a declarative sentence that is either true or false, but not both
A **declarative sentence** is a sentence that declares something verifiable

Examples:
7 - 4 = 3
prop

Odin is on our side
prop

What is a Viking's favorite food?
not prop

Every Saxon is under attack.
prop

x+y=3
not prop, because x and y vary

**Propositional Variables** are variables used to denote propositions.
* Typically: p, q, r, s, ...
* never use capitals as they are reserved for propositional functions

### Negation
Negation of $p$ denoted by $\neg p$
* *You must use $\neg$ to mean "not"
* same as !

Examples:
1. Ronnie likes Taco Bell
$r$: "Ronnie likes Taco Bell"
$\neg r$: "It is not the case that Ronnie likes Taco Bell", "Ronnie does not like Taco Bell"

2. Thor's hammer is not named Mjölnir
*always define prop vars as positive as below*
m: "Thor's hammer is named Mjolnir"
Negate original:
$\neg(\neg m) \rightarrow m$
"Double negation rule"

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
$p$: "Ronnie has 3 cats"
$q$: "Ronnie does CrossFit"

1. Find $p \lor q$
Ronnie has 3 cats or Ronnie does CrossFit
2. Find $\neg p \land q$
Ronnie does not have 3 cats and Ronnie does CrossFit

The **exclusive or** of p and q is the statement p XOR q
* $p \oplus q$
* Same as ^
* In order to eval to true, p can be true or q can be true, but not both
* $p \oplus q = (p \lor q) \land \neg(p \land q)$

# Conditionals & More!
Let p and q be propositions
* A statement in the form "if p, then q" is called a **conditional statement**
* written as $p \rightarrow q$
* False when p is true and q is false, otherwise true
* p is called the hypothesis, sufficient condition
* q is called the conclusion or the necessary condition
* if sufficient condition happens, then the necessary condition *must* happen

### Truth Tables: $p \land q, p \lor q, p \oplus q, p \rightarrow q$
- List all possible combinations of truth values
- If $n$ is the # of unique prop vars, then there are $2^n$ rows in the truth table

| p   | q   | $p \land q$ | $p \lor q$ | $p \oplus q$ | $p \rightarrow q$ |
| --- | --- | ----------- | ---------- | ------------ | ----------------- |
| T   | T   | T           | T          | F            | T                 |
| T   | F   | F           | T          | T            | F                 |
| F   | T   | F           | T          | T            | T                 |
| F   | F   | F           | F          | F            | T                 |

### $p \rightarrow q$
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
Given $p \rightarrow q$
1. Converse: $q \rightarrow p$
2. Inverse: $\neg p \rightarrow \neg q$
3. Contrapositive: $\neg q \rightarrow \neg p$

* $q \rightarrow p = \neg p \rightarrow \neg q$
* $\neg q \rightarrow \neg p = p \rightarrow q$

