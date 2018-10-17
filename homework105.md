# section 1.2: 22
1. How many positive integers n can we form using the digits 3, 4, 4, 5, 5, 6, 7 if we want n to exceed 5,000,000?

__solution__

There are 7 digits in the set $\{3, 4, 4, 5, 5, 6, 7\}$, so we need to use all of them to form a number n that's greater than 5,000,000. In our selection set of digits $\{3, 4, 4, 5, 5, 6, 7\}$, there only 3 digits greater than or equal to 5: 5, 6, and 7. One of these digits must necessarily be the first digit in *n*

For this problem, first choose a starting digit, and then compute the number of possible arrangements of the remaining digits in the set. 

Case 1:  First digit is 5:

After removing the 5, the set is now $\{3, 4, 4, 5, 6, 7\}$. There are 6 digits, so 6! ways of arranging them. There are 2 4s in the set and they are interchangable, so they are removed via division. This means that for case 1, the total number of arrangments is $\frac{6!}{2!}$

Case 2: First digit is 6: 

After removing 6, the set is $\{3, 4, 4, 5, 5, 7\}$. Both the 4 and 5 repeats and so need to be factored out. This means the total number of arrangements in case 2 is $\frac{6!}{2!2!}$

Case 2: First digit is 7:

After removing the set is $\{3, 4, 4, 5, 5, 6\}$, so the total number of combinations is $\frac{6!}{2!2!}$

These choices are mutually exclusive, so the total number of positive integers n that can be formed are: 
$\frac{6!}{2!} + \frac{6!}{2!2!} + \frac{6!}{2!2!} = \frac{6!}{2!} (1 + \frac{1}{2} + \frac{1}{2}) = \frac{6!}{2!} * 2 = 6!$

# section 1.2: 30
2. A sequence of letters of the form abcba, where the expression is unchanged upon reversing order, is an example of a palindrome (of five letters).


(a) If a letter may appear more than twice, how many palindromes of five letters are there? of six letters?

(b) repeat part (a) under the condition that no letter appears more than twice.

__solution__
A 5 letter palindrome is abcba, where a, b, and c can be any letter.

a) Because letters are allowed to repeat, a, b, and c can be any letter from the alphabet. Therefore there are $26\times26\times 26 = 26^3$ choices of letters for both the 5 and 6 case. 

b) The limitation that no letter repeats more than twice means that in the palindrome abcba or abccba, the mirrored side cba is the repeat. This means that a, b, and c must be distinct, so the number of choices is $26 \times 25 \times 24$ (As a letter is chosen, it is taken out of the set of choices of letters)

# section 1.3: 18
3. In studies of algebraic coding theory and the theory of computer languages, we consider certain arrangements, called strings, made up from a prescribed alphabet of symbols. If the prescribed alphabet consists of the symbols 0, 1, and 2, for exampled, then 01, 11, 21, 12, and 20 are five of the nine strings of length 2. Among the 27 strings of length 3 are 000, 012, 202, and 110. 

In general, if n is any positive integer, then by the rule of product there are 3n strings of length n for the alphabet 0,1 and 2. if $x = x_1, x_2, x_3,...x_i, ..., x_n$ is one of these strings, we define the weight of x, denoted wt(x), as  $wt(x) = x_1 + x_2 + x_3 +...+x_i+...+ x_n$

For strings of length 10 made up from the alphabet (0,1,2), how many have

a) Four 0's, three 1's, and three 2's,

b) at least eight 1's

c) weight 4?

__solution__

__a__) Four 0's, three 1's, and three 2's:

The selection set is $\{0, 0, 0, 0, 1, 1, 1, 2, 2, 2\}$. There are 10 symbols in the selection set, so there are 10! arrangements for a string of length 10. We then divide out the repetitions, yielding $\frac{10!}{4!3!3!}$ choices. 

__b__) at least eight 1's

for a string of length 10, there are 3 possible mutually exclusive arrangements: 
1. eight 1s + 2 numbers (either 0 or 2)

There are 10 choices of location in which to slot the eight ones ${10 \choose 8}$. In the remaining two locations, either number from the set $\{0, 2\}$ can be repeated, for a total of $2 \times 2 = 2^2$ choices. In all, there are   ${10 \choose 8}2^2$ arrangements when there are eight 1s. 


2. nine 1s + 1 number (either 0 or 2)

There are ${ 10 \choose 9}$ locations in which to place the 1s and 2 options $\{0, 2\}$ for the remaining slot, so the total number of arrangements is ${ 10 \choose 9}2$

3. ten 1s:

There are 10 slots for 10 choices of 1, which means there's only 1 possible arrangement (since order does not matter for a combination and the ones are not distinct.)

The total number of arrangements is ${10 \choose 8}2^2 + { 10 \choose 9}2 + 1$

__c__) weight 4?

For the alphabet $\{0, 1, 2\}$, the question is how many possible solutions are there for the equation:
$a*0 + b*1 + c*2 = 4$ where $a + b + c = 10$

In this example, it is possible to list all mutually exclusive options:

1. $6*0 + 4*1 + 0*2 = 4$

There are 10 possible locations to choose from for the 4 ones: ${10 \choose 4}$ Once this choice is made, the remaining slots are 0. 

2. $7*0 + 2*1 +  1*2 = 4$

First choose two slots for the 1 out of 10 possible slots, and then 1 slot for the 2 out of the remaining 8 slots: ${10 \choose 2}{8 \choose 1}$. The remaining slots are 0. 

3. $8*0 + 0*1 + 2*2 = 4$
Choose 2 slots for the 2s and set the remaining slots to 0 $\{10 \choose 2}$

We do not compute a combination for the remaining 0s because combinations are not concerned with ordering and so in computing how the 1s and 2s are distributed, we've also computed that the remaining slots must be 0. 

Total number of possible arrangements: 
${10 \choose 4} + {10 \choose 2}{8 \choose 1} + {10 \choose 2}$

# section 1.5: 7

4. In how many ways can one parenthesize the product abcdef?

__solution__

In example 1.43 in the book, the general rule is that one can parenthezise the product $x_1x_2x_3...x_n$ in $b_{n-1}$ ways. Since abcdef has 6 numbers, there are $b_5$ ways to parenthesize the product. 

# section 2.2, 19 
5. Provide the steps and reasons, as in Exercise 18, to establish the following logical equivalences:

a) $p \lor [p\land(p\lor q)] \Leftrightarrow p$

b) $p \lor q \lor (\lnot p \land \lnot q \land r) \Leftrightarrow p \lor q \lor r$ 

c) $[(\lnot p \lor \lnot q) \rightarrow (p \land q \land r)] \Leftrightarrow p \land q$

__solution__

Start with the parenthesis and work outwards to respect rules of association. 

a) $p \lor [p\land(p\lor q)] \Leftrightarrow p$
| Steps | Reasons | Reference | notes |
| :----- | :---| :----|---|
|$p \lor [p\land(p\lor q)]$ | | |
|$p \lor p$| absorption| def 2.2, ex 2.9| $p\land(p\lor q)$ is equal to whatever p is. P=1: $1 \land (1 \lor q)$ q doesn't matter since 1 sets the or true. P=0: $0 \land (0 \lor q)$ q doesn't matter since 0 means and is false. |
| p | idempotent | def 2.2, ex 2.9 | |

b) $p \lor q \lor (\lnot p \land \lnot q \land r) \Leftrightarrow p \lor q \lor r$ 
| Steps | Reasons | Reference | notes |
| :----- | :---| :----|---|
|$p \lor q \lor (\lnot p \land \lnot q \land r)$ | | |
|$(p \lor q) \lor [\lnot(p \lor q) \land r)]$| DeMorgan's | def 2.2, ex 2.9 | breaks up the 2nd clause so that r is a standalone element|
| $[(p \lor q) \lor \lnot(p \lor q)] \land (p \lor q \lor r)$| Distributive| def 2.2, ex 2.9 | yields the equivalence $p \lor q \lor r$ |
|$T_0 \land (p \lor q \lor r)$ |Inverse|def 2.2, ex 2.9|$[(p \lor q) \lor \lnot(p \lor q)$ is always true ($T_0$)|
|$(p \lor q \lor r)$| Identity| def 2.2, ex 2.9 | And is true when both sides are true, and by definition $T_0$ is true, so the truth of the statement is determined by $(p \lor q \lor r)$|

c)$[(\lnot p \lor \lnot q) \rightarrow (p \land q \land r)] \Leftrightarrow p \land q$
| Steps | Reasons | Reference | notes |
| :----- | :---| :----|---|
|$[(\lnot p \lor \lnot q) \rightarrow (p \land q \land r)]$ | | |
|$\lnot (\lnot p \lor \lnot q) \lor (p \land q \land r)$|$(\lnot p \lor q) \Leftrightarrow (p\rightarrow q)$ |def 2.1, table 2.6| puts everything into ands and ors-which have logic laws |
|$\lnot \lnot (p \land q) \lor (p \land q \land r)$| DeMorgan's| 2.2/2.9 | factors out negative|
|$(p \land q) \lor (p \land q \land r)$ | Double Negation | 2.2/2.9 | |
|$(p \land q)$| Absorption | 2.2/2.9 | $(p \land q)$ determines whether the whole statement is true since an or statement requires that only one side of the clause be true|

# section 2.3, 8
6. Give the reasons for the steps verifying the following argument:

$$(\lnot p \lor q) \rightarrow r\\
r \rightarrow (s \lor t)\\
\lnot s \land \lnot u\\
\lnot u \rightarrow \lnot t\\
\therefore p
$$

__solution__
Use table 2.19 in section 2.3.. 

|#| Steps | Reasons | Notes |
|--|:-----| :----| :----|
|1 |$\lnot s \land \lnot u$ |premise | |
|2 |$\lnot u$ | (1) and conjunctive simplication | conjunctive simplification only needs the conjunctive premise |
|3| $\lnot u \rightarrow \lnot t$| premise | |
|4|$\lnot t$ | (2) (3) and detachment/modus ponens | given (3) $\lnot u \rightarrow \lnot t$ and (2) $\lnot u$, we can infer $\lnot t$ |
|5|$\lnot s$|(1) and conjunctive simplification | conjunctive simplification works with either premise of the conjunction since the truth of the statement requires both premises be true|
|6|$\lnot s \land \lnot t$ | (4), (5), and conjunction | can combine any premises in the proof since they're all implicitly joined |
|7|$r \rightarrow (s \lor t)$ | premise||
|8|$\lnot (s \lor t) \rightarrow \lnot r$| (7) and the contrapositive identity| the contra positive is when you negate both premisis and switch the if-then order|  
|9|$(\lnot s \land \lnot t) \rightarrow \lnot r$| (8) and De Morgan's| |
|10|$\lnot r$ |(9), (6), and Detachement | |
|11|$(\lnot p \lor q) \rightarrow r$ premise ||
|12|$\lnot r \rightarrow \lnot(\lnot p \lor q)$ (11) and the contrapositive identity | |
|13|$\lnot r \rightarrow (p \land \lnot q)$| (12) and double negation ||
|14|$p \land \lnot q$ (13), (10), and rule of detachment | |
|15|$p$ (14) and conjective simplification | 