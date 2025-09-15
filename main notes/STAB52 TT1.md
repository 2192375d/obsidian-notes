---
title: STAB52 TT1
created: Before 28th July, 2025
last_modified: Monday 28th July 2025 17:36
tags: [probability exam-review]
course: [STAB52]
---
time: Friday June 13, 15:00-16:30
location: IC130

**Remember to bring the calculator!!!!- - - -**
## coverage
- probability spaces
- axioms of probability
- derived rules

- product rule
- permutation
- combination
- permutation with repetition
- combination with replacement object

- conditional probability
- pairwise independence
- mutual independence
- Bayes' rule
- conditional independence

- discrete RV
- probability mass function
- Bernoulli distribution
- Geometric distribution
- Negative binomial distribution
- Hypergeometric distribution
- Poisson distribution

## notes
#### probability rules
__LOTP__
Let $B$ be an event and $A_1,\dots,A_n$ be a partition, then$$P(B)=P(B\cap A_1)+\dots+P(B\cap A_n)$$
__complement rule__
Let $A$ be an event, then$$P(A)=1.0-P(A^c)$$
__other rules__
Let $A, B$ be events, then$$P(A\cap B^C)=P(A)-P(A\cap B)$$$$P(A\Delta B)=P((A\cap B^c)\cup(B\cap A^c))=P(A)+P(B)-2P(A\cap B)$$
#### combinatorics
Consider choosing k objects out of n objects, then the number of ways to do each is

|                                         | care about order | don't care about order |
| --------------------------------------- | ---------------- | ---------------------- |
| don't put back a duplicate after taking | $Perm(n,k)$      | $\binom{n}{k}$         |
| put back a duplicate after taking       | $n^k$            | $\binom{n+k-1}{k}$     |

__multinomial coefficients (permutation with repetition)__
number of ways to seperate n objects into sets $s_1,...,s_l$, where 
- $|s_i|=|k_i|$, 
- order matters between each sets, but don't matter inside each set
is
$$Perm(n;k_1,...,k_n)=\binom{n}{k_1,...,k_n}$$
when $l=2$, we get combination formula.

#### conditional probability & independence
__independent__
Let $A, B$ be events, if $A\perp B$, then 
1. $P(A\cap B)=P(A)P(B)$
2. $P(A|B)=P(A),P(B|A)=P(B)$
__complement independence__
Let $A,B$ be events, if $A\perp B$, then$$A\perp B^c$$
__mutual independence__
Let $A_1,...,A_n$ be events, if $A_1,...,A_n$ are mutually independent, then $\forall A_{k_1},...,A_{k_m}\subset\{A_1,...,A_n\}$, $$P(A_{k_1}\cap\dots\cap A_{k_m})=P(A_{k_1})\dots P(A_{k_m})$$
__conditioning on mutual independence__
Let $A_1,...,A_n$ be mutually independent events
Suppose $A_{j_1},\dots,A_{k_l},A_{j_1},\dots,A_{j_l}\in\{A_1,\dots,A_n\}$ S.T. $\{A_{j_1},\dots,A_{k_l}\},\{A_{j_1},\dots,A_{j_l}\}$ are disjoint
Suppose $1\leq i\leq n$, then
1. $$P(A_i|A_{k_1},\dots A_{k_m})=\frac{P(A_i\cap A_{k_1}\cap\dots\cap A_{k_m})}{P( A_{k_1}\cap\dots\cap A_{k_m})},$$ 
2. $$P(A_{j_1}\cap\dots\cap A_{j_k}|(A_{k_1},\dots,A_{k_m}))=P(A_{j_1}\cap\dots\cap A_{j_l})$$
__conditional independence__
Just remember 
1. if $(A\perp B|C)$, then $(A\perp B^c|C$), however (IMPORTANT!!!), $P(A\cap B|C)\neq P(A\cap B|C^c)$
2. if $A,B,C$ are mutually indepent, then $(A\perp B|C)$

## todos
2017 exam: not done
2019 exam: not done
2020 exam: not done
2021 exam: _done_
2022 exam: _done_
2023 exam: _done_
2024 exam: _done_
quiz 1: not redone
quiz 2: not redone
quiz 3: _done_

## extra notes
1. (From 2022 exam Q2b))
	We proved if A and B are independent, then A and B$^c$ are independent. This is also true if A and B are independent over C, then A and B$^c$ are also independent over C. $$\text{if }P(A|B,C)=P(A|C)=P(B|C)\text{, then } P(A|B^c,C)=P(A|C)=P(B^c|C)$$
2. Review Q4 in 2021 midterm (don't make the same mistake!)
3. Remember that Law of Total Probability can be applied inside conditional probability $P(A|C)=1.0-P(A^c|C)=P(A\cup B|C)+P(A\cup B^c|C)$ (from 2022 exam Q2c)
4. Look up for integer partition (a + b + c = 7, find all integers a, b, c)
5. For questions of type "procedure A is done until result B is achived n times, remember that the last one must be result B"
## to ask
#### (already asked)
- Can we bring markers, color pencils on the exam? It is helpful dealing with Venn diagram-ish problems, like the ones with stuffs like $P((A\cup B)\cap C^c)$ type of problems
	_yes_
- For problems of type above, is there any general tips? I see two often used approaches (probably the only two) are via lots of algebraic manipulation or via Venn diagram. How do I choose between those?
	_go by feeling_
- On the exam, if we encounter problems like Q3 in midterm 2021, where we need to approximate using calculator, how exactly do we show our steps, is my step good?
	_either way is fine_
- On Q5 in midterm 2021, the solution used something called "by symmetry", do we have to know this for the exam?
	_yes_
- Do we have to know anything about independent over something?
	eg: A and B are independent over C (appeared in 2022 exam Q2)
	_yes_
- ~~For Q2d in midterm 2022, how did you get $P(R_3)$?~~
- Is it true that if $P(A)=P(B)$, then $P(A|C)=P(B|C)$?
	_no, obviously false by defn_
#### (to ask)
- We have lots of theorems that works for mutual independence (e.g. the complement theorem), which of them applies to conditional independence? Does the concept of mutual independence apply to conditional independence, if so, do we need to know this for the upcoming midterm?
- How does combination with repetition tie with negative binomial formula?