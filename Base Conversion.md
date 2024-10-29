See also: [[Integer Representation]]

Use the following algorithm to construct base b expansions of an integer n.

1. First divide n by b to get a quotient and remainder
	$n = bq_0 + a_0, 0 ≤ a_0 < b$
	The remainder $a_0$ is the first digit in the base b expansion of n
2. Next divide $q_0$ by b to obtains
	 $q_0 = bq_1 + a_1,   0 ≤ a_1 < b.$
	 The remainder $a_1$ is the 2nd digit in the base b expansion of n
3. Repeat the steps above until you get 0 as a quotient.
##### Example
Find the find binary expansion of $(241)_{10}$
$241 / 2 = 120\ r\ 1$
$120 / 2 = 60 \ r \ 0$
$60 / 2 = 30 \ r \ 0$
$30 / 2 = 15 \ r \ 0$
$15 / 2 = 7 \ r \ 1$
$7 / 2 = 3 \ r \ 1$
$3 / 2 = 1 \ r \ 1$
$1 / 2 = 0 \ r \ 0$
### Conversion between binary, octal, hexadecimal
##### Example
Find the octal and hex expansions of $(11\ 1110\ 1011\ 1100)_2$
011|111|0 10|11 1|100
3   |  7 |   2  |  7  | 4
$(37274)_8$

0011|1110|1011|1100
3     | 14   |   11 |  12
$(3EBC)_{16}$

##### Example
Find the binary expansions of $(765)_8$ and $(A8D)_16$
(7   6     5$)_8$
$(111\ 110\ 101)_2$

(A      8       D$)_{16}$
$(1010\ 1000\ 1101)_2$
