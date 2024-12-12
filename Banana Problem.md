The formula to find the number of distinct arrangements of a set of objects, some of which are indistinguishable
where $n$ is the count of items
where each $k_i$ is the number of repetitions of an object
$$
\frac{n!}{k_{1}! \cdot k_{2}! \cdot\ \cdots\ \cdot k_{n}!} = \frac{\text{Orderings ignoring repeats}}{\text{Product of orderings of each repeated item}}
$$

For example,
How many distinct arrangements can be made using the letters
in the word: BANANA?
> [!solution]-
> - Pretend like there are no duplicate letters:
> $6!$ arrangements
> - Of those arrangements some will be exactly the same
> Consider BANANA. We want to elimate the repeated arrangements
> How many ways can you arrange 3 As? $3!$
> How many ways can you arrange 2 Ns? $2!$
> $$
> \frac{6!}{3!2!} = 60
> $$