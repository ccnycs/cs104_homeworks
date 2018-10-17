# Logic
## 2.1
### Question 7
Q .  Rewrite each of the following statements as an implication in the if-then form:
  1.  Practice her serve daily is a sufficient condition for Darice to have a good chance of winning the tennis tournament.

  2.  Fix my air conditioner or I won't pay the rent.

  3.  Mary will be allowed on Larry's motorcycle only if she wears her helmet. 

A . 
1. __If__ Darice practices her daily serve, __then__ she will have a good chance of winning the tennis tournament. 

   __p__ *is a sufficient condition for* __q__ means *if* __p__ *then* __q__ because it is good enough (sufficient) to know that if __p__ occurs, then __q__ follows  (section 2.1, 2) c)Implication, https://en.wikipedia.org/wiki/Necessity_and_sufficiency)
 
 2.  __If__ you don't fix my air conditioner, __then__ I won't pay the rent. 
   
      The statement $\lnot p \lor q$ is logically equivalent to $p \implies q$ (section 2.2, table 2.6). So assigning the clauses in 2. to primitives:
      * $\lnot$ p: Fix my air conditioner 
      * q:  I won't pay the rent

      The negation of *fix my air conditioner* is *don't fix my air conditioner*.
   
 3. __If__ Mary is to be allowed on Larry's motorcycle, __then__ she must wear a helmet. 

    The *only if* means that the only way the sentence/implication can be true is if the clause *must wear a helmet* is true. Given the truth table for implication:

    | p | q| p $\implies$ q |
    | --| --| :-----------:|
    | 0 | 0 | 1 |
    | 0 | 1 | 1 |
    | 1 | 0 | 0 |
    | 1 | 1 | 1 |

    The only way for the statement to be false when Mary is not wearing a helmet is if *Mary wears her helmet* is the result (__q__).

 ### Question 13
Q. If if statement q has a truth value of 1, determine all truth value assignments for the primitive statements p, r, and s, for which the truth value of the following statement is 1:

$$(q \implies [(\lnot p \lor r) \land \lnot s]) \land [\lnot s \implies (\lnot r \land q)]$$

A. p: 0, r: 0, s: 0 

By permutation with repetition, there are $2^3$ total possible combinations of p, q, and s: {0, 1} x {0, 1} x {0, 1} = 8. Create a truth table and break the compound statement down into its component parts:

|  |q | p | r |s |$\lnot$ p| $\lnot$ r |$\lnot$ s|
|--|--|-- |---|--|---------|-----------|---------|
|0| 1| 0 | 0  | 0|  1      | 1         | 1      |
|1| 1| 0 | 0  | 1|  1      | 1         | 0       |
|2| 1| 0 | 1  | 0|  1      | 0         | 1       |
|3| 1| 0 | 1  | 1|  1      | 0         | 0       |
|4| 1| 1 | 0  | 0|  0      | 1         | 1       |
|5| 1| 1 | 0  | 1|  0      | 1         | 0       |
|6| 1| 1 | 1  | 0|  0      | 0         | 1       |
|7| 1| 1 | 1  | 1|  0      | 0         | 0       |

|  | $(\lnot p \lor r)$ | $[(\lnot p \lor r) \land \lnot s]$  | $(q \implies [(\lnot p \lor r) \land \lnot s])$  | $(\lnot r \land q)$ | $[\lnot s \implies (\lnot r \land q)]$ |
|--|:-------------------:|:----------------------------------:|:------------------------------------------------:|:-------------------:| :-------------------------------------:|
|0| 1 | 1 | 1 | 1 | 1
|1| 1 | 0 | 0 | 1 | 1
|2| 1 | 1 | 1 | 0 | 0
|3| 1 | 0 | 0 | 0 | 1
|4| 0 | 0 | 0 | 1 | 1
|5| 0 | 0 | 0 | 1 | 1
|6| 1 | 1 | 1 | 0 | 0
|7| 1 | 0 | 0 | 0 | 1

|  |  $(q \implies [(\lnot p \lor r) \land \lnot s])$ | $[\lnot s \implies (\lnot r \land q)]$ |$(q \implies [(\lnot p \lor r) \land \lnot s]) \land [\lnot s \implies (\lnot r \land q)]$|
|--|:-------------------:|:------------------------:|:----------------------------:|
| 0| 1 | 1 | __1__ |
|1| 0 | 1 | 0 |
|2| 1 | 0 | 0 |
|3| 0 | 1 | 0 |
|4|0 | 1 | 0 |
|5|0 | 1 | 0 |
|6| 1 | 0 |0|
|7| 0 | 1 | 0|

The only row where the statement is true is row 0, where p, r, and s are set to 0.

## 2.2
### Question 5
Q. Negate and express each of the following statements in smooth english: 
  
a. Kelsey will get a good education if she puts her studies before her interest in cheerleading.

b. Norma is doing her homework, and Karen is practicing her piano lessons.

c. If Harold passes his C++ course and finishes his data structures project, then he will graduate at the end of the semester.

A. 

a) Kelsey placed her studies before cheerleading, but she did not get a good education. 

  Statement a) in if-then format is *if Kelsey puts her studies before cheerleading, then she will get a good education*. $\lnot(p \implies q)$ is the equivalent of $p \land \lnot q$ which is *Kelsey puts her studies before cheerleading __and__ she __did not__ get a good education*. Since *__and__ __not__* is the equivalent of __but__, this becomes *Kelsey placed her studies before cheerleading, but she did not get a good education* (section 2.2, example 2.13)

b) Norma is not doing her mathematics homework or Karen is not practicing her piano lesson.

By DeMorgan's Law, $\lnot (p \land q)$ is equal to $\lnot p \lor \lnot q$ (section 2.2, Laws of Logic). *Norma is doing her homework* becomes *Norma is not doing her homework*, *Karen is practicing her piano" becomes "Karen is not practicing her piano* and *and* becomes *or*.

c) Harold did pass his C++ course and he did finish his data structure project, but he did not graduate at the end of the semester. 

In statement form, the sentence is:
* p: Harold passes his C++ course
* q: finishes his data structures project
* r: he will graduate at the end of the semester
* $(p \land q) \implies r$

 $\lnot((p \land q) \implies r)$ is $(p \land q) \land \lnot q$, which (like in 5 a) translates to *Harold passes his C++ course and finishes his data structures project* $(p \land q)$ *and does not graduate at the end of the semester* $(\land \lnot q)$. And like in 5a, *__and__ __not__* is *__but__*.
 

