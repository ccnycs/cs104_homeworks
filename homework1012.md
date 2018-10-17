# Chap 2. Supplementary Exercises: Q 6
1. Let p, q, and r denote primitive statements. Write the converse, inverse, and contrapositive for:
    1. $p \rightarrow (q \land r)$
    2. $(p \lor q) \rightarrow r$

__Solution__:

Apply the definitions of converse, inverse, and contrapositive to the premises:
 * premise: $p \rightarrow  q$
 * converse: $q \rightarrow p$
 * inverse: $\lnot p \rightarrow \lnot q$
 * contrapositive: $\lnot q \rightarrow \lnot p$

Where $p$ and $q$ are standins for premises with any number of primitives and logical operators. 

And use De Morgan's laws for alternative forms of the negations:
* $\lnot (p \land q) \Leftrightarrow (\lnot p \lor \lnot q)$
* $\lnot (p \lor q) \Leftrightarrow (\lnot p \land \lnot q)$


1. __$p \rightarrow(q \land r)$__

$(q \land r)$ takes on the role of $q$ in the definitions listed above. 
* converse: $(q \land r) \rightarrow p$
* inverse: $[\lnot p \rightarrow \lnot (q \land r)]\Leftrightarrow [\lnot p \rightarrow (\lnot q \lor \lnot r)]$
* contrapositive: $[\lnot (q \land r) \rightarrow \lnot p] \Leftrightarrow [(\lnot q \lor \lnot r) \rightarrow \lnot p]$

2. __$(p \lor q) \rightarrow r$__

$(p \lor q)$ takes on the role of $p$ in the defintions listed above, while $r$ takes on the role of $q$. 
* converse: $r \rightarrow (p \lor q)$
* inverse: $[\lnot (p \lor q) \rightarrow \lnot r] \Leftrightarrow [(\lnot p \land \lnot q) \rightarrow \lnot r]$
* contrapositive: $[\lnot r \rightarrow \lnot(p \lor q)] \Leftrightarrow [\lnot r \rightarrow \lnot p \land \lnot q)]$


# Section 3.2: Q 1
2. For $\mathscr{U} = \{1, 2, 3, ..., 9, 10\}$ let:
    * $A = \{1, 2, 3, 4, 5\}$
    * $B = \{1, 2, 4, 8\}$
    * $C = \{1, 2, 3, 5, 7\}$
    * $D = \{2, 4, 6, 8\}$

    Determine the following:
    1.  $(A \cup B) \cap C$
    2.  $A \cup (B \cap C)$
    3. $\overline{C} \cup \overline{D}$
    4. $\overline{C \cap D}$
    5. $(A \cup B) - C$
    6. $A \cup (B - C)$
    7. $(B - C) - D$
    8. $B - (C - D)$
    9. $(A \cup B) - (C \cap D)$

__solution__

First let's list the set definitions (Section 3.2, definitions: 3.5, 3.6, 3.7, https://www.probabilitycourse.com/chapter1/1_2_2_set_operations.php)
* $A \cup B$: union, combine elements in A with elements in B
* $A \cap B$: intersection, elements in both A and B
* $A \delta B$: symmetric difference, elements in A or in B but not in both
* $\overline{A}$: complement, elements in the universal set $\mathscr{U}$ but not in A
* $A - B$: set difference/relative complement, elements in A that are not in B 

1.  $(A \cup B) \cap C$
    * $A = \{1, 2, 3, 4, 5\}$
    * $B = \{1, 2, 4, 8\}$
    * $C = \{1, 2, 3, 5, 7\}$

    Parenthesis first and remove duplicates when combining sets:
    1. combine sets $(A \cup B)$: $\{1, 2, 3, 4, 5\} \cup \{1, 2, 4, 8\} =\{1, 2, 3, 4, 5, 8\}$
    2. find elements common to both sets $\{1, 2, 3, 4, 5, 8\} \cap C$: $\{1, 2, 3, 4, 5, 8\} \cap \{1, 2, 3, 5, 7\} = \{1, 2, 3, 5\}$

    __Answer:__ $\{1, 2, 3, 5\}$


2.  $A \cup (B \cap C)$
    * $A = \{1, 2, 3, 4, 5\}$
    * $B = \{1, 2, 4, 8\}$
    * $C = \{1, 2, 3, 5, 7\}$
    
    Always tackle the parenthesis first
    1. shared elements $(B \cap C)$: $\{1, 2, 4, 8\} \cap \{1, 2, 3, 5, 7\} = \{1, 2\}$
    2. combine $A \cup \{1, 2\}$: $\{1, 2, 3, 4, 5\} \cup \{1, 2\} = \{1, 2, 3, 4, 5\}$
    
    __Answer:__$\{1, 2, 3, 4, 5\} = A$

3. $\overline{C} \cup \overline{D}$
    * $\mathscr{U} = \{1, 2, 3, ..., 9, 10\}$
    * $C = \{1, 2, 3, 5, 7\}$
    * $D = \{2, 4, 6, 8\}$
    
    $\overline{S} = \mathscr{U}-S$ and $\overline{S}$ takes precedence since it's a negation of sorts. 

    1. in $\mathscr{U}$ and not C: $\overline{C} = \{1, 2, 3, ..., 9, 10\} - \{1, 2, 3, 5, 7\} = \{4, 6, 8, 9, 10\}$
    2. in $\mathscr{U}$ and not D: $\overline{D} =  \{1, 2, 3, ..., 9, 10\} - \{2, 4, 6, 8\} = \{1, 3, 5, 7, 9, 10\}$
    3. Join: $\{4, 6, 8, 9, 10\} \cup \{1, 3, 5, 7, 9, 10\} =\{1, 3, 4, 5, 6, 7, 8, 9, 10\}$

    __Answer:__$\{1, 3, 4, 5, 6, 7, 8, 9, 10\} = \mathscr{U}-\{2\}$

4. $\overline{C \cap D}$
    * $\mathscr{U} = \{1, 2, 3, ..., 9, 10\}$
    * $C = \{1, 2, 3, 5, 7\}$
    * $D = \{2, 4, 6, 8\}$

    $C \cap D$ takes precedence because the complement is applied to the compound clause. 

    1. in both: $\{1, 2, 3, 5, 7\} \cap \{2, 4, 6, 8\} = \{2\}$
    2. in $\mathscr{U}$ and not $\{2\}$: $\{1, 2, 3, ..., 9, 10\} - \{2\} = \{1, 3, 4, 5, 6, 7, 8, 9\}$
    
    __Answer__: $\{1, 3, 4, 5, 6, 7, 8, 9\} = \mathscr{U} - \{2\}$

5. $(A \cup B) - C$
    * $A = \{1, 2, 3, 4, 5\}$
    * $B = \{1, 2, 4, 8\}$
    * $C = \{1, 2, 3, 5, 7\}$

    1. $(A \cup B)$ =  $\{1, 2, 3, 4, 5\} \cup \{1, 2, 4, 8\} = \{1, 2, 3, 4, 5, 8\}$
    2. In joint (A,B) but not in C $\{1, 2, 3, 4, 5, 8\} - C$: $\{1, 2, 3, 4, 5, 8\} - \{1, 2, 3, 5, 7\} = \{4, 8\}$
    
    __Answer:__$\{4, 8\}$

6. $A \cup (B - C)$
    * $A = \{1, 2, 3, 4, 5\}$
    * $B = \{1, 2, 4, 8\}$
    * $C = \{1, 2, 3, 5, 7\}$

    1. in B and not C $B-C$: $\{1, 2, 4, 8\} -  \{1, 2, 3, 5, 7\} = \{4, 8\}$
    2. $A \cup \{4, 8\}$: $\{1, 2, 3, 4, 5\} \cup \{4, 8\} = \{1,2, 3, 4, 5, 8\}$
    
    __Answer__:$\{1, 2, 3, 4, 5, 8\}$


7. $(B - C) - D$
    * $B = \{1, 2, 4, 8\}$
    * $C = \{1, 2, 3, 5, 7\}$
    * $D = \{2, 4, 6, 8\}$

    1. $(B-C)$ =  $\{1, 2, 4, 8\} - \{1, 2, 3, 5, 7\} = \{4, 8\}$
    2. In $(B-C)$ and not D $\{4, 8\} - D$:  $\{4, 8\} - \{2, 4, 6, 8\} = \{\}$

    __Answer__: $\{\} = \emptyset$

8. $B - (C - D)$
    * $B = \{1, 2, 4, 8\}$
    * $C = \{1, 2, 3, 5, 7\}$
    * $D = \{2, 4, 6, 8\}$
    1. in C and not D $(C-D)$: $ \{1, 2, 3, 5, 7\} - \{2, 4, 6, 8\} = \{1, 3, 5, 7\}$
    2. in B and not $(C-D)$: $\{1, 2, 4, 8\}- \{1, 3, 5, 7\}=\{2, 4, 8\}$

    __Answer__:$\{2, 4, 8\}$

9. $(A \cup B) - (C \cap D)$
    * $A = \{1, 2, 3, 4, 5\}$
    * $B = \{1, 2, 4, 8\}$
    * $C = \{1, 2, 3, 5, 7\}$
    * $D = \{2, 4, 6, 8\}$
    * $(A \cup B)$: $\{1, 2, 3, 4, 5\} \cup \{1, 2, 4, 8\} = \{1, 2, 3, 4, 5, 8\}$ 
    * $(C \cap D)$: $\{1, 2, 3, 5, 7\} \cap \{2, 4, 6, 8\} = \{2\}$
    * $\{1, 2, 3, 4, 5, 8\} - \{2\} = \{1, 3, 4, 5, 8\}$

    __Answer:__$\{1, 3, 4, 5, 8\}$


# Section 3.2: Q 8
3. Using Venn diagrams, investigate the truth or falsity of each of the following, for sets $A, B, C, \subseteq \mathscr{U}$

__solution__
Create the empty venn diagram:
![empty 3 elemnet venn diagram](venn\template.png)

1. $A \Delta (B \cap C) = (A \Delta B) \cap (A \Delta C)$

    1. $(B \cap C)$ is the area in both B and C:
    ![two overlapping circles, overlapping area is colored in green](venn\BintC.png)

    2. The symmetric difference $A \Delta (B \cap C)$ is any area that's in $B \cap C$, which is shaded above in green, and in $A$, but not in the overlap of the two. (Note: We're only interested in the orange sections)
    ![three overlapping circles, A is colored in everywhere except where it intersects with B and C](venn\axorbc.png??)

    3. Elements in A or B but not in both $(A \Delta B)$:
    ![venn diagram where A and B are colored in everywhere but overlap](venn\axorb.png??)
 
    4. $(A \Delta C)$ Elements in A or C but not in both:
    ![venn diagram where A and C are colored in everywhere but overlap](venn\xcorc.png??)

    5. Now we take the intersection (places that are colored in both diagrams) of the above two diagrams $(A \Delta B) \cap (A \Delta C)$ We only care about the orange highighted section
    ![](venn\acap.png)

__Answer__: *False*, because the diagrams for $A \Delta (B \cap C)$ and $(A \Delta B) \cap (A \Delta C)$ are different. 

2. $A - (B \cup C) = (A - B) \cap (A -C)$
    1. $B \cup C$: The union is the joint of of all elements in B and C
    ![](venn\bcupc.png??)
    2. $A - (B \cup C)$ elements in A but not in $(B \cup C)$ are in orange:
    ![](venn\ambcupc.png??)
    3. $A-B$:
    ![](venn\amb.png??)
    4. $(A -C)$
    ![](venn\amc.png)
    5. $(A - B) \cap (A -C)$
    ![](venn\acabcap.png??)

    __Answer:__ *True* because the same parts are in orange in the diagrams for $A - (B \cup C)$ and $(A - B) \cap (A -C)$

3. $A \Delta (B \Delta C) = (A \Delta B) \Delta C$

    1. $B \Delta C$ elements exclusively in B or C
    ![](venn\bdc.png??)

    2.  $A \Delta (B \Delta C)$ elements exclusively in A or in the area shaded in 1. 
    ![](venn\adbc.png??)

    3. $A \Delta B)$
    ![](venn\adb.png)

    4. $(A \Delta B) \Delta C$
    ![](venn\abdc.png)

    __Answer:__ *True* because the same parts are orange in the diagrams for $A \Delta (B \Delta C)$ and $(A \Delta B) \Delta C$

# Section 3.3: Q 7
4. How many permutations of the 26 different letters of the alphabet contain (a) either the pattern "OUT" or the pattern "DIG"? (b) neither the pattern "MAN" nor the pattern "ANT"?

__Solution__

(a) There are 26 possible positions in which to put the 26 letters of the alphabet. In the case of OUT, three of those positions are given over to OUT and the question is where that combined grouping is in the overall arrangement of letters. Therefore OUT is treated as one letter/element in the set of letters, meaning that there are 26 letters - the 3 letters in OUT + the 1 OUT group = 24 elements that can be arranged. This means that there are 24! permutations with the pattern OUT. Because DIG is also a 3 letter word, there are also 24! ways to arrange DIG. 

To remove cases that have both DIG and OUT, compute the case where both appear. Treat OUT as a singular element and DIG as a singular element because the letters must be kept together. This yields 26 letters - 3 letters in OUT + 1 OUT group - 3 letters in DIG + 1 DIG group = 22 elements to permute. 

__Answer:__ 24! (OUT) + 24! (DIG) - 22!(OUT&DIG) = 2(24!) - 22!

(b) First compute the positive case, where either MAN or ANT appears. As in (a), MAN and ANT can each be treated as one element for the purposes of computing the permutation, so the total number of permutations for MAN is 24! and ANT! is 24. 

MAN and ANT share letters, but the permutation is limited to the 26 letters of the alphabet with no repetition. The only possible way for both MAN and ANT to appear is when the arrangment MANT appears. This can also be treated as 1 element, so the total number of elements in the permutation set is 26 (letters) - 4 letters in MANT + 1 MANT element = 23. 

In all there are 2(24!) - 23! arrangements that contain either MAN or ANT. The number of permutations with neither MAN nor ANT is the total number of arrangements 26! - the number of arrangements that contain either MAN or ANT (2(24!) - 23!)

__Answer:__ 26! - [2(24!) - 23!]



# Section 3.1: Q 13
5. Let $S = \{1, 2, 3, ...., 29, 30\}$. How many subsets A of S satisfy:
    1. $|A| = 5$
    2. $|A| = 5$ and the smallest element of A is 5
    3. $|A| = 5$ and the smallest element in A is less than 5

__Solution__:

1. $|A| = 5$
 The cardinality (size) of A needs to be 5, but there are no restrictions on which elements need to be in A. Therefore A can be any 5 elements from the 30 elements in S. 

 __Answer:__ ${30 \choose 5}$

2. $|A| = 5$ and the smallest element of A is 5

There are 5 elements in A, and one of those elements is 5. This leaves 4 elements to select from S, and those elements must be greater than 5 (since 5 has already been chosen.) These conditions yield a selection set of $\{6,7,8,..., 29, 30\}$

__Answer:__ ${25\choose 4}$

3. $|A| = 5$ and the smallest element in A is less than 5

One element (let's call it *x*) in A is fixed. *x* can be one of 4 values: {1, 2, 3, 4}. The value chosen for *x* will then restrict the rest of the choices from S to values greater than the smallest value. Each choice of smallest value can be examined independently:

* *x*=1: there are no restrictions on choices from S except that 1 is already chosen, so there are ${29\choose 4}$ ways to choose the remaining 4 elements
* *x*=2: the remaining 4 choices for A have to be greater than 2, meaning that there are 28 values in S to choose from, so there are ${28\choose 4}$ possible subsets
* *x*=3: choices from S have to be greater than 3, so there are 27 values to choose from, yielding ${27 \choose 4}$ possible subsets
* *x*=4: choices must be > 4, so ${26 \choose 4}$ possible subsets

Since these cases are mutually exclusive, they are summed together for the total number of possible subsets: ${29 \choose 4}+{28 \choose 4}+{27 \choose 4}+{26 \choose 4}$

__Answer:__ ${29 \choose 4}+{28 \choose 4}+{27 \choose 4}+{26 \choose 4}$