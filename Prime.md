See also: [[Fundamental Theorem of Arithmetic]]

$\forall\ (n  \in \mathbb{Z}, \ n > 1)$ ($n$ prime $\iff$ $n$ only has factors $1,\ n$)

If an integer is not prime and is strictly greater then 1 it is composite


### Prime Divisor Theorem
All composite integers $n$ have a prime divisor less than or equal to $\sqrt{n}$

**Pf:**
We first show that $n$ has a divisor $\leq \sqrt{n}$
Since $n$ is composite and by def of divides $\exists a,b \in Z$, 
such that $n = ab$ and WLOG $1 < a \leq b < n$
We show either $a \leq \sqrt{n}$ or $b \leq \sqrt{n}$
using contradiction:
Suppose $a > \sqrt{n} \land b > \sqrt{n}$
Then $ab > n$, CONTR
Thus $a \leq \sqrt{n} \lor b \leq \sqrt{n}$

We now show $n$ has a prime divisor $\leq \sqrt{n}$
By the fundamental theorem of arthimetic, $a$ has a unique prime factorization. Therefore, $\exists c \in Z \mid c | a \land c$ is prime. Since $c \leq a \leq \sqrt{n} \land c|a  \land a|n$ 
$c$ is a prime divisor of $n$ with $c \leq \sqrt{n}$
$\square$

### Sieve of Eratosthenes
Because of [[#Prime Divisor Theorem]]
Find all primes $\leq n$
When you find a prime number, remove all of its multiples
Repeat until you reach $\sqrt{n}$

### Infinite Primes Theorem
There are infinitely many primes
**Pf:** Suppose there are not infinitely many prime, then there are a finite amount of primes. Then we can list them: $p_1, p_2, \cdots, p_n$
Let P = $\Pi^{n}_{i = 1}\ p_i$
Let Q = P + 1. Q must be compistive bc its larger then all primes. Thus $\exists q \in Z$ such that q is prime and $q | Q$. Since Q is prime, $q | P$. Thus $q | Q - P$, which implies $q | P+1 - P = 1. Thus $q | 1$, which implies q = 1, which is not prime. CONTR, q is prime.

### Mersenne Primes
$2^p - 1$, where $p$ is prime is a Mersenne prime. However, $p$ is prime does not neccessarily imply $2^p -1$ is prime.


