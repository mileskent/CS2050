# 1 Fundamental Counting Principles
### 1.1 [[Sum Rule]]
**1.1.1** A student rolls a fair six-sided die. What is the probability of rolling a number that is either 2 or 4?
>[!solution]-
$P(2) = P(4) = \frac{1}{6}$
2 and 4 are mutually exclusive
$P(2) + P(4) - P(2 \cap 4) = \frac{1}{6} + \frac{1}{6} - 0 = \frac{1}{3}$

**1.1.2** In a deck of 52 playing cards, what is the probability of drawing
a card that is either a heart or a king?
> [!help]- Hint
> Use the [[Principle of Inclusion-Exclusion]]

> [!solution]-
The overall set of 52 cards can be $C$
The set of all kings can be $K$
The set of all hearts can be $H$
$P(\text{King or Heart}) = \frac{|K \cup H|}{|C|}$
Using [[Principle of Inclusion-Exclusion]]:
$|K \cup H| = |K| + |H| - |K \cap H|$
$|K \cup H| = 4 + 13 - 1 = 16$
$P(\text{King or Heart}) = \frac{16}{52}$

**1.1.3** A bag contains 4 red balls, 5 blue balls, and 3 green balls. A
ball is randomly drawn. What is the probability that the ball
is either red or green?
> [!solution]-
$P(\text{Red or Green}) = \frac{|G \cup R|}{|B|} = \frac{3 + 4 - 0}{12} = \frac{7}{12}$

**1.1.4** A group of students is playing a card game using two standard decks of 52 cards each. If a single card is randomly drawn from the shuffled decks:
a) What is the probability that the card is a face card? #keydisagrees 
> [!solution]-
$P(\text{Face Card}) = \frac{|F_1 \cup F_2|}{|D_1 \cup D_2|} = \frac{24}{104} = \frac{12}{52}$

b) How about a diamond? 
> [!solution]-
$P(\text{Diamond}) = \frac{|\diamond_1 \cup \diamond_2|}{|D_1 \cup D_2|} = \frac{26}{104} = \frac{13}{52}$

c) Lastly, a black card that isn’t a face card nor a club? #keydisagrees

> [!help]- Hint
> Use [[Principle of Inclusion-Exclusion]]

> [!solution]-
$P(\text{Given Black, Not Face nor Club}) = \frac{|B| - |F \cup C|}{|B|}$
Where $F$ is black face cards, where $C$ is black clubs
$|B| = 26$, $|F| = 6$, $|C| = 13$, $|F \cap C| = 3$
$|F \cup C| = |F| + |C| - |F \cap C| = 6 + 13 - 3 = 16$
$P(\text{Given Black, Not Face nor Club}) = \frac{10}{26}$

### 1.2 [[Product Rule]]
**1.2.1** A factory produces items, 95% of which are non-defective. If two items are randomly selected one after the other, what is the probability that both are non-defective?
> [!solution]-
The drawing of the first item does not effect the odds of the second item. Therefore they are independent events and the [[Product Rule]] applies
$P(\text{Two consecutive non-defective}) = P(\text{non-defective})^2 = 0.95^2 = 0.9025$

**1.2.2** In a group of students, 60% like math and 40% like physics.
Assuming the two preferences are independent, what is the probability that a randomly selected student likes both math and physics?
> [!solution]-
> Apply [[Product Rule]]
$P(M \cap P) = P(M) \cdot P(P) = 0.6 \cdot 0.4 = 0.24$


**1.2.3** A bag contains 3 red balls and 2 blue balls. A ball is drawn, its
color is noted, and it is not replaced. Another ball is drawn.
What is the probability that:
• The first ball is red and the second ball is blue? #nokey
> [!solution]-
$P(R)$ in the original universe = $\frac{3}{5}$
$P(B)$ in the universe once one red ball is drawn = $\frac{2}{4}$
Apply [[Product Rule]]
$P(R) \cdot P(B) = \frac{3}{5} \cdot \frac{2}{4} = \frac{6}{20}$

• The first ball is blue and the second ball is red? #nokey
> [!solution]-
> $P(B)$ in the original universe = $\frac{2}{5}$
> $P(R)$ in the universe once one blue ball is drawn = $\frac{3}{4}$
> Apply [[Product Rule]]
> $P(B) \cdot P(R) = \frac{2}{5} \cdot \frac{3}{4} = \frac{6}{20}$ 

### 1.3 Inclusion Exclusion Principle
**1.3.1** How many bit strings of length 8 begin with 111 or end with 010?
> [!help]- Hint
> Apply [[Principle of Inclusion-Exclusion]]

> [!solution]-
> Let $A$ be the set of 8 length binary strings that begin with 111.
> Let $B$ be the set of 8 length binary strings that end with 010.
> We want to find $|A \cup B|$
> $|A \cup B| = |A| + |B| - |A \cap B|$
> 	[[Principle of Inclusion-Exclusion]]
> $|A|$:
> 	*`1 1 1 _ _ _ _ _`*
> 	*How many 5 length binary strings are there = $|C|$*
> 	*$|A| = |C| = 2^5$*
>
> $|B|$:
> 	`_ _ _ _ _ 0 1 0`
> 	How many 5 length binary strings are there = $|C|$
> 	$|B| = |C| = 2^5$
>
> $|A \cap B|$:
> 	`1 1 1  _ _ 0 1 0`
> 	How many 2 length binary strings are there = $|D|$
> 	$|A \cap B| = |D| = 2^2$
>
> $\therefore |A \cup B| = 2^5 + 2^5 - 2^2 = 60$

**1.3.2** How many numbers below 100 are divisible by 2,3, or 5?
> [!help]- Hint
> Involves lcm and [[Principle of Inclusion-Exclusion]]

> [!solution]-
> Use [[Principle of Inclusion-Exclusion]]
> $|S_{5} \cup S_{2} \cup S_{3}| = |S_{5}| + |S_{3}| + |S_{2}| - |S_{3} \cap S_{2}| - |S_{3} \cap S_{5}| - |S_{5} \cap S_{2}| + |S_{5} \cap S_{3} \cap S_{2}|$
> 
> $|S_5| = \frac{100}{5} - 1 = 19, |S_{2}| = \frac{100}{2} - 1 = 49, |S_{3}| = \frac{100}{3} = 33$ 
> 
> $|S_{3} \cap S_{2}|$:
> $lcm(3, 2) = 6$
> $|S_{3} \cap S_{2}| = |S_6| = \frac{100}{6} = 16$
> 
> $|S_{3} \cap S_{5}|$:
> $lcm(3,5) = 15$
> $|S_{3} \cap S_{5}| = |S_{15}| = \frac{100}{15} = 6$
> 
> $|S_{5} \cap S_{2}|$:
> $lcm(5,2) = 10$
> $|S_{5} \cap S_{2}| = |S_{10}| = \frac{100}{10} - 1 = 9$
> 
> $|S_{5} \cap S_{3} \cap S_{2}|$:
> $lcm(2, 3, 5) = 30$
> $|S_{5} \cap S_{3} \cap S_{2}| = |S_{30}| = \frac{100}{30} = 3$
> 
> $|S_{5} \cup S_{2} \cup S_{3}| = 19 + 49 + 33 - 16 - 6 - 9 + 3 = 73$

**1.3.3** Suppose you need to come up with a password that uses only the letters A, B, and C and which must use each letter at least once. How many such passwords of length 8 are there?
> [!solution]-
> Let $S$ be the set that uses all characters (A, B, or C) without constraints. This is the universe. Equal to $3^8$
> 
> Let $S_{BC}$ be only Bs and Cs = $2^8$
> Let $S_{AC}$ be only As and Cs = $2^8$
> Let $S_{AB}$ be only As and Bs = $2^8$
> Use [[Principle of Inclusion-Exclusion]] to find invalid passwords
>
> $|S_{BC} \cup S_{AC} \cup S_{AB}| = |S_{BC}| + |S_{AC}| + |S_{AB}|$
> $- |S_{BC} \cap S_{AC}| - |S_{BC} \cap S_{AB}| - |S_{AC} \cap S_{AB}|$
> $+ |S_{BC} \cap S_{AC} \cap S_{AB}|$
>
> $|S_{BC} \cup S_{AC} \cup S_{AB}| = 2^8 + 2^8 + 2^8 - 1 - 1 - 1 + 0$
> 
> $|S| -|S_{BC} \cup S_{AC} \cup S_{AB}| = 3^8 - 3 \cdot 2^8 + 3 \cdot 1 = 5796$

**1.3.4** Suppose that 4 people are standing in line. How many ways are there to rearrange the line so that nobody is standing in their original place
> [!solution]-
> Let the original order be a string 1234, where person 1 is in position 1 at character 1, etc etc.
> 
> Let $S$ be the universe of possible line configurations. $|S| = 4!$
> Let $S_1$ be the set of all configurations of the line where person 1 is in position 1
> Let $S_2$ be the set of all configurations of the line where person 2 is in position 2
> Let $S_3$ be the set of all configurations of the line where person 3 is in position 3
> Let $S_4$ be the set of all configurations of the line where person 4 is in position 4
> 
> Solution is $|S| - |S_{1} \cup S_{2} \cup S_{3} \cup S_{4}|$
> 
> Find $|S_1|$:
> Assume position 2 is already set. How many configurations are there of a 3 person line? This corresponds to $|S_1|$
> 
> $|S_1| = |S_2| = |S_{3}| = |S_{4}| = 3!$
> The fixed position sets are not mutually exclusive, so we have to use [[Principle of Inclusion-Exclusion]]
> $$
> \begin{align*}
> |S_{1} \cup S_{2} \cup S_{3} \cup S_{4}| &=\\
> &|S_{1}| + |S_{2}| + |S_{3}| + |S_{4}|\\
> & - |S_{1} \cap S_{2}| - |S_{1} \cap S_{3}| - |S_{1} \cap S_{4}|\\
> & - |S_{2} \cap S_{3}| - |S_{2} \cap S_{4}|\\
> & - |S_{3} \cap S_{4}|\\
> & + |S_{1} \cap S_{2} \cap S_{3}|+ |S_{4} \cap S_{2} \cap S_{3}|\\
> & + |S_{1} \cap S_{4} \cap S_{3}|+ |S_{1} \cap S_{2} \cap S_{4}|\\
> & - |S_{1} \cap S_{2} \cap S_{3} \cap S_{4}|
> \end{align*}
> $$
> 
> 1 fixed 
> - cardinality = $3!$
> - count = 4
> Intersection of 2 fixed 
> - cardinality = $2!$
> - count = 6
> intersection of 3 fixed 
> - cardinality = 1
> - count = 4
> intersection of 4 fixed 
> - cardinality = 1
> - count = 1
> 
> $|S_{1} \cup S_{2} \cup S_{3} \cup S_{4}| = 4 \cdot 3! - 6 \cdot 2! + 4 \cdot 1 - 1 = 15$
> $|S| = 4! = 24$
> $|S| - |S_{1} \cup S_{2} \cup S_{3} \cup S_{4}| = 9$

### 1.4 Permutations
1.4.1 What is the formula for nPr?


1.4.2 How many ways are there to select a first prize winner a
second prize winner and a third prize winner from 100 different
people who have entered a contest

1.4.3 How many permutations of the letters ABCDEFGH contain
the string ABC

### 1.5 Combinations
1.5.1 What is the formula for $n\choose{r}$?

1.5.2 What is the value of C(9, 4) you can leave your answer in fac-
torial format?

1.5.3 A club has 8 members, they must choose 3 members to form
their executive board. In what ways can they choose an exec-
utive board?

### 1.6 Pigeonhole Principle
1.6.1 If there are 11 pairs of socks in your drawer, and you blindly
take out one sock at a time until you get a pair. How many
socks do you need to take out to guarantee that you have at
least one pair of socks?

1.6.2 25 crates of apples are delivered to a store. The apples are of
3 different types. All crates only have one type of apple. Show
that there is at least one type of apple that has 9 crates of it.

1.6.3 Fifteen squirrels collected 100 acorns, show that at least one
pair of squirrels collected the same amount of acorns

### 1.7 Stars and Bars
1.7.1 How many ways can you give 7 cookies to 4 children

1.7.2 Find the number of non-negative integer solutions to the equa-
tion:
x1 + x2 + x3 + x4 = 12

1.7.3 Determine the number of non-negative integer solutions to the
equation:
x1 + x2 + x3 = 15
where x1 ≥ 3, x2 ≥ 1, and x3 ≥ 5.

### 1.8 Counting Indistinguishable Objects
1.8.1 How many distinct arrangements can be made using the letters
in the word:
BANANA?

1.8.2 You have 7 identical apples, 5 identical oranges, and 3 identical
bananas. In how many ways can these be distributed into 4
distinct baskets?

### 1.9 Bionomial Theorem
1.9.1 A fair coin is flipped 6 times. What is the probability of getting
exactly 3 heads?

1.9.2 A factory produces light bulbs, and 95% of the light bulbs
pass the quality control test. If 15 light bulbs are randomly
selected, what is the probability that exactly 12 pass the qual-
ity control test?

1.9.3 In a classroom, 40% of the students are left-handed. If 5 stu-
dents are randomly selected, what is the probability that ex-
actly 2 students are left-handed?

### 1.10 Baye’s
1.10.1 A person uses his car 30% of the time, walks 30% of the time
and rides the bus 40% of the time as he goes to work. He
is late 10% of the time when he walks; he is late 3% of the
time when he drives; and he is late 7% of the time he takes
the bus. What is the probability he walked if he is on time?

1.10.2 Company A supplies 40% of the computers sold and is late
5% of the time. Company B supplies 30% of the computers
sold and is late 3% of the time. Company C supplies another
30% and is late 2.5% of the time. A computer arrives late -
what is the probability that it came from Company A?

# 2 Advanced Problems (These are exam level difficulty)
### 2.1 Word Problems
2.1.1 10 2050 TA’s all are waiting to collect their paychecks. Kavya,
and Anthony being Head TA’s get to collect their paychecks
before the other TA’s. How many different orders are there
for the TA’s to collect their paychecks?

2.1.2 Brito is getting pizza’s for the TA grading party. He is buying
24 pizzas in total. He can buy pepperoni, chicken, sausage,
and cheese pizzas. In how many ways can he buy pizzas if he
has to buy at least 4 of each type of pizza?

2.1.3 Saksham is using Prize Picks to make a parlay. He wants
to make a 4 pick parlay based around picking players to score
above their projected points for a game in the upcoming Celtics
vs Cavs game. To make his parlay he wants to pick at least
one of the two star players on the Celtics (Jaylen Brown and
Derrick White), but not both. Outside of these 2 players there
are 6 other players that Saksham could pick for his parlay (Ja-
son Tatum, Donovan Mitchell, Ty Jerome, Luke Kornet, Max
Strus, Craig Porter Jr.

2.1.4 Ronnie decides to reward everyone on the last day of classes
by letting everyone get their own McDonald’s Happy Meal.
Each student has an option of choosing an entree (Hamburger,
McNuggets, McChicken), an appetizer (Fries, Apple Slices), a
drink (Chocolate Milk, Coke, Water, Orange Juice), and a toy
(Boo Bucket, Mini Crocs, A Batman action figure). How many
students must give Ronnie their orders for it to be guaranteed
that at least 2 students share the same order.

2.1.5 How many different strings can be made from ”GOODLUCK-
ONFINALS”

### 2.2 Combinatorial Proofs
2.2.1 Prove with a combinatorial proof that ${n\choose{k}} = {n\choose{n-k}}$

2.2.2 Prove with a combinatorial proof that $1n + 2(n-1) + 3(n-2) + \cdots + (n-1)\cdot 2+n \cdot 1 = \frac{n(n+1)}{2}$
