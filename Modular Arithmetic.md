### Modular Congruence
**Informal Definition:**
An integer a is considered congruent to an integer b modulo m if a and b have the same remainder when divided by m. 
Example: 
- 3 is congruent to 5 under modulo 2 
- $3 \equiv 5\ (\text{mod } 2)$
	- the mod 2 is not an operation. This is the modulo that we are discussion for our congruence.
**Formal Definition:**
Let a and b be integers and m be a positive integer. If m | a-b, then  a is congruent to b modulo m.  
- We will use the notation $a ≡_m b$, $a \equiv b\ (\text{mod } m)$ to indicate that  a is congruent to b modulo m
- Note $a \equiv b\ (\text{mod } m)$ not the same as $a = b \mod m$

### Modular Congruence Theorems
**Theorem 1**
$$\displaylines{
\text{Let } a,b \in \mathbb{Z}\quad m \in \mathbb{Z}^{+}\\
a \equiv b (\mod m) \iff a \mod m = b \mod m
}
$$
**Theorem 2**
$$\displaylines{
\text{Let } a,b,k \in \mathbb{Z}\quad m \in \mathbb{Z}^{+}\\
a \equiv b (\mod m) \iff a = b + km
}
$$
**Theorem 3**
$$\displaylines{
\text{Let } a,b,c,d \in \mathbb{Z}\quad m \in \mathbb{Z}^{+}\\
a + c \equiv b + d (\mod m)\\
ac \equiv bd (\mod m)
}
$$
In modular arithmetic problems, modularly congruent expressions can be interchanged.

### Modular Congruence Properties
$\text{Let } a,b \in \mathbb{Z}\quad m \in \mathbb{Z}^{+}$
- (a+b) mod m = ((a mod m) + (b mod m)) mod m
- ab mod m = ((a mod m)(b mod m)) mod m

**Ex:**
Find $(19^2\mod 17)^3 \mod23$
$(19^2\mod 17)^3\mod23$
$(19\cdot 19 \mod 17)^3 \mod 23$
$(2\cdot2 \mod 17)^3 \mod23$
$((2\mod 17 \cdot 2 \mod 17) \mod 17)^3 \mod 23$
$(2\cdot 2 \mod 17)^3 \mod 23$
$(4 \mod 17)^3 \mod 23$
$4^3 \mod 23$
$64 \mod 23$
$18$

Ex: 
(27 + 53) mod 7
27 mod 7 = 6
53 mod 7 = 4
(27 + 53) mod 7 = (6 + 4) mod 7 = 10 mod 7 = 3
or
(27 + 53) mod 7
(77 + 3) mod 7
3

# Arithmetic Modulo m
- Define $\mathbb{Z}_m$ to be the set of nonnegative integers less than m {0,1,...,m-1}
- We define addition on the integers by $+_m$ by 
	- a $+_m$ b = (a+b) mod m
- We define multiplication on these integers by $⋅_m$ by 
	- a $⋅_m$ b = (a ⋅ b) mod m

## Properties of addition modulo m and multiplication modulo m
![](https://lh7-rt.googleusercontent.com/slidesz/AGV_vUcZTBDt0SwncvxVM8XLBK9j3iK-PPKw0ApqJwQpHwJ75E-faycaHrv8-xU_w_FucfUkJMjnz9zGM6qUzGVp2ykgtntKRtQowXGoK3rfmc9nKoXP8JlYL_vArXR5xOsAbx1rb1Ee0m62dmMc1AieNAHqhGLNYEDN4Zny6AjHXaXnVIXFGSKrFvc=s2048?key=h77F5V3n-EVo5m3NnoMhkQ)