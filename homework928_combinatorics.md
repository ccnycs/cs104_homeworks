# Combinatorics
## Problem 1

1. How many different three letter initials that begin with an A can people have? 

    A. $26^2$

    There are 3 slots to fill: initial 1, initial 2, and initial 3. The first slot fixed because the initials being with A. The other __2__ slots can be any letter, and there are __26__ letters in the English alphabet: 26 * 26 = $26^2$ 


2. How many different bit-strings are there of length ten that begin and end with 1?

    A. $2^{8}$

    A bit string is a string composed of letters from the binary alphabet {0,1},  meaning that there are 2 choices {0,1} for each letter. The string in this question has 10 letters (is of length 10), but the first and last letters are fixed at 1. This leaves 8 letters that each can either be a 0 or 1: $2 * 2 * 2 * 2 * 2 * 2 * 2 * 2 = 2^8$

3.  How many different license plates can be made using either two or three letters followed by either two or three digits?

    A. $(26^2 + 26^3)* (10^2 + 10^3)$

    There are __26__ possible letters and __10__ possible digits. This problem has two stages: 1) two or three letters and 2) two or three numbers. For two letters, there are $26*26$ options, and for three letters thare are $26*26*26$ options. Because these outcomes are mutually exclusive - the choice is between two __or__ three letters-rule of sum dictates that for stage 1, there are $26^2 + 26^3$ options. This is also true of the digits, where 2 digits is $10*10$ choices and 3 digits are $10*10*10$ choices, so the total amount of choices is $10^2 + 10^3$. The problem states that there are two stages, choice of letters __followed by__ choice of digits, so the total number of choices is found by applying rule of product  $(26^2 + 26^3)* (10^2 + 10^3)$

4. How many different bit-strings of length seven begin with two 0s or end with three 1s? 

    A. $2^5 + 2^4 - 2^2$

    There are __7__ bits in the string `bbbbbbb`, and there are 2 mutually exclusive cases:
    
    * `00bbbbb` begins with __2__ 0s, so there are $7-2 = 5$ bits unaccounted for
    * `bbbb111` ends with __3__ 1s, so there are $7-3=4$ bits unaccounted for
    
    The unaccounted bits are the ones that can be either be 0 or 1. So for the begins with 000 case, there are $2*2*2*2*2=2^5$ choices. And for the ends with 111 case, there are $2*2*2*2$ choices. Since these are exclusive, the number of choices is  $2^5 + 2^4$. Because there is no restriction on the free bits, the strings that start with 00 and ends with 111 `00bb111` are possible in both cases. The number of possible `00bb111` strings is equal to the unassigned bs - which here is __2__, so $2*2=2^2$. Subtracting the number of possible `00bb111` from the total number of choices removes the double counting of permutations of the `00bb111` string: $2^5 + 2^4 - 2^2$


5. How many different license plates can be made using either two or three digits?

    A. $10^2 + 10 ^3$.

    As in 3., there are __10__ digits. The choice is either $10^2$ or $10^3$ and so by rule of sum (because there is only one license plate), the answer is $10^2 + 10 ^3$.

## Problem 2
An awards committee is preparing a celebration for 10 distinguished students.

1. Facilities is asked to set up 10 chairs for the award winners. All chairs are identical except for their color, which may be red, green or blue. There are 200 chairs of each color available. How many distinct sets of 10 chairs can facilities prepare? Two arrangements are considered distinct only if there exists a color such that the number of chairs of that color in one of the sets differs from the number of chairs in the same color in the other set.

    A. ${ 10 + 3 -1 \choose 10}$

    This is a combination question because the arrangements are considered distinct if the __count__ of chairs of each color differ. The distinct objects are the colors {r, g, b}, which is a set of size __n=3__. 

    The following are distinct arrangements:
    grgrbgrbgg
    rgbggrbggg
    rrggrrgrgg

    Because combinations do not care about order, the above can be rewritten as:

    $$
    3r + 2b + 5g = 10\\
    2r + 2b + 6g = 10\\
    5r + 0b + 5g = 10\\
    $$

    Further, because the set gives an ordering {r,g,b}, the colors can be discarded and replaced with a symbol (such as 0) and the + with a 1
    ```
    000 1 00 1 00000
    00 1 00 1 000000
    00000 11 00000
    ```
    Furthermore, all possible combinations can be modeled as binary strings (strings where the letters are {0,1}), so the combination with repetition problem reduces to a permutation with repetition problem where the arrangement space is r (number of arrangements/0's) + n-1 (number of distinct objects -1/1's) and 0s and 1s are non distinct. 

    Another way of approaching this problem is to generalize:

    $$
    3r + 2b + 5g = 10\\
    2r + 2b + 6g = 10\\
    5r + 0b + 5g = 10\\
    $$
    
    to an algebraic equation where:
    * $x_1$ = number of red chairs
    * $x_2$ = number of green chairs
    * $x_3$ = number of blue chairs

   Because the equation says that in total there are 10 chairs (the 200 is a red herring to indicate that there are more than enough chairs of each color to fulfill a request for 10 total), this question can be modeled as the algebraic equation:

    $$x_1 + x_2 + x_3 = 10$$

    The combination question is equivalent to asking for the number of possible solutions to the above equation, which is also the set of all possible values for $x_1, x_2, x_3$. The general form of this equation for combination problems is:

    $$\sum_{i=1}^{n} {x_i} = r$$
    
    which yields that __n = 3__, __r = 10__


2. Facilities is now asked to prepare 10 tables where the 10 award winners will sit and to put on each table the name of the student who will sit there. All tables are identical except for their color, which may be yellow, blue, or white. There are two hundred tables available of each color. How many distinct arrangements of tables can facilities prepare? Two arrangements are considered distinct only if there exists a student to whom the two arrangements assign tables of two different colors.

    A. $3^{10}$

    As in 1., the 200 is a red herring indicating that there are more than enough tables to choose for. This is a permutation problem because there are 10 distinct students, and the question asks how to assign a table color to each student. 

    Student 1 has a choice of 3 colors {yellow, blue, white}. Student 2 has a choice of 3 colors {yellow, blue, white.} For all students:: $3*3*3*3*3*3*3*3*3*3 = 3^{10}$

3. The committee is selecting 4 students out of the 10 for a trip to New York, How many distinct sets of 4 travelers can be formed out off the 10 award winners?

    A. ${10 \choose 4}$

    The question does not indicate that the order in which the students are selected matters, so this is a combination w/o repetition (because the problem specifies distinct) problem. There are __n=10__ students to choose from, and __r=4__ slots to offer them. 

4. The committee is assigning final grades for the honors projects of the 10 awarded students. There are three possible final grades: A++, A+, and A. How many distinct grade sheets can the committee come up with? Two sheets are distinct only if the grade assigned to some student on one sheet differs from the grade assigned to the same student on the other sheet.
    
    A. $3^{10}$

    As in 2., there are __3__ choices of grades {A++, A+, A}, and each student is distinct from another, so the ordering of all assigned grades is important (permutation problem). Because two student can get the same grade, it is a permutation with reptition problem. As in 2., student 1 gets one grade from {A++, A+, A}, student 2 gets a grade from {A++, A+, A}... student 10 gets a grade from {A++, A+, A}. In all, the number of grade sheets is $3*3*3*3*3*3*3*3*3*3 = 3^{10}$

5. The committee is giving a total of 10 gifts to the awarded students: two $1000, three $500, and five $200 awards. How many distinct gift lists can the committee come up with? 2 gift lists are distinct only if the gift assigned to one student differs from the gift assigned to the same student on another list.

    A. ${10 \choose 2} \times {8 \choose 3} \times {5 \choose 5}$

    This problem is broken down into stages (rule of product) because each set of gifts is distinct and once students are chosen for one prize, they are out of the selection pool for another gift. Since the order in which the students are chosen for each gift does not matter, there are ${10 \choose 2}$ ways to award the top 2 gifts. Once those two gifts are given away, there are $10-2=8$ students left to give the $500 awards to. There are 3 awards, so there are ${8 \choose 3}$ choices, and $8-3=5$ students left to award the last 5 prizes to. The total number of awards is then ${10 \choose 2} \times {8 \choose 3} \times {5 \choose 5}$ 

6. The committee is issuing a rank list of the 10 awarded students, which assigns to each student a unique number between 1 and 10. How many rank lists can the committee come up with?

    A. 10!

    The number the student is assigned can be mapped to the students order in a list. The first slot in the list can have any of the 10 students, the second 9, etc...so the total number of arrangements of students is $10*9*8*...*2*1=10!$

## Problem 3
A construction dealer builds several types of houses. Each such house type is characterized by:

    number of rooms, which is at least 1 but does not exceed r;
    number of windows, which is at least 1 but does not exceed w;
    number of entrance doors, which is at least 1, but does not exceed d;
    number of balconies, which does not exceed b;
    number of floors, which is at least 1, but does not exceed f;
    number of staircases, which does not exceed s;

Two house types are identical if and only if they have an equal number of each of the above six features,

1. How many distinct house types are there that have exactly: 2 floors, 1 staircase, 1 balcony, 1 entrance door, and 1 window per room?

    A. r

    There are 6 attributes that characterize the house: {r, w, d, b, f, s}. The problem restricts the space of houses to those that have {2f, 1s, 1b, 1d, 1w}, which leaves *r* as the only varying attribute. The number of possible houses is equal to the number of possible rooms, which is *r* 

2. How many distinct house types are there without balconies and without staircases that have exactly 1 floor, 1 entrance door, and 2 windows per room?

    A. r

    The following are fixed: {1f, 1d, 2w, 0b, 0s}, so *r* is the only attribute that varies. 

3. If there is exactly 1 staircase between every two consecutive floors, on each floor exactly 1 room and 1 balcony, exactly 1 window per room, and just one entrance door, how many distinct house types are there?

    A. f

    Most of the attributes are either fixed {1d} or fixed relative to the number of floors {(1/2)fs, 1rf, 1bf, 1wr}. The only attribute that varies is *f*

4. If there is exactly 1 staircase between every two consecutive floors, on each floor exactly 1 room and 1 balcony, exactly one window per room, and just one entrance door , how many distinct house types with at least 3 floors are there?

    A. f-2

    As above, every variable is fixed except floors. Because there must be at least 3 floors, and f is minimally 1, the search space is reduced $3-1 = 2$ to f-2. 

5. If there is exactly one staircase between every 2 consecutive floors , on each floor exactly 1 room and 1 balcony and exactly 2 windows per room, how many distinct house types are there?

    A. f*d

    The fixed variables are {(1/2)sf, 1rf, 1bf, 2wr}, which leaves f and d to vary. The set of all possible houses is the set of possible numbers of floors f * the set of possible numbers of doors d = f*d

6. How many distinct house types are there without staircases that have exactly 1 floor, 1 room, 1 balcony, and 1 entrance door?

    A. w

    fixed: {0s, 1f, 1r, 1b, 1d}. This leaves w to vary. 

7. How many distinct house types are there that have exactly 2 floors, 1 staircase, 2 rooms, and 1 entrance door?

    A. (b+1)w

    fixed: {2f, 1s, 2e, 1d}. Varies: w and b. Because b can also be 0, the total number of balconies is (b+1). The total number of house types is balconies * windows = (b+1)*w

8. How many distinct house types are there without staircases that have exactly: 1 floor, 2 rooms, 1 entrance door, and at least 2 windows?

    A. (b+1)(w-1)

    fixed: {0s, 1f, 2r, 1d, }. Varies b and w. Because there must be two windows, the number of windows is restricted by 2-1 = 1. The total number of houses is (b+1)(w-1)