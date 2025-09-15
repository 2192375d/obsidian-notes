---
title: STAB52 final exam
created: Wednesday 30th July 2025 15:00
last_modified: Wednesday 30th July 2025 14:33
tags:
  - probability
  - exam-review
course:
  - STAB52
---
# todo
- STAB52 fin 2020 _half way done need to do the rest_
- STAB52 fin 2021 _one question skipped, need to redo_
- STAB52 fin 2022 _done_
- STAB52 fin 2023 _done_
- STAB52 fin 2024 _done_

- ps9 _done_
- ps10 _done_
- ps11 _done_
- ps12 _done_

- Review different distributions' definition, for example, the meaning of the parameters of a negative binomial distribution.
- Review permutation/combination with replacement

# interesting problems
- 3.5.16 (a very easy problem if done correctly)


# questions to keep in mind
- ps9 q4 ($F_{X|X<1}=P(X\leq x|X<1)???$)
- ps9 q5 (just doesn't know how to calculate the stupid fucking bullshit variance :<
- ps9 q7 _a trap question_
- ps10 q2 (super creative use of negative binomial distribution) _not important question_
- ps10 q4 ($X$ is not indepdent from $X$!!!)
- ps10 q8 _to redo_
- ps11 q2 (WTF)
- ps11 q5 (WTF?!!!!- - - -, how on the world things just canceled out so nicely???)
- ps11 q6 (cause you skipped it lol) _to do_
- ps12 q4 (literally don't know how to do it) _to do_
- ps12 q5 (literally don't know how to do it, in a different sense, like none of the words on the solution makes sense) _to do_

- STAB52 fin 2021 Q2 (review convolution) _mistaken_
- STAB52 fin 2021 Q5b (mistake easy to make about CDF, also often happens with normal distribution or any distribution from $-\infty$ to $\infty$) _mistaken_ _PLEASE REVIEW THIS LATER, DOUBLE CHECK YOUR MISTAKE_ _checked_
- STAB52 fin 2021 Q7c (some weird mistakes...) _mistaken_ _to redo_
- STAB52 fin 2022 Q3b (Variation of central limit theorem...?) _mistaken_
- STAB52 fin 2022 Q4e (mistake on bonding absolute value, also mistakes on very basic stuffs regarding $P(-y\leq x\leq y)=P(x\leq y)-P(x\leq-y)$) _mistaken to redo_
- STAB52 fin 2022 Q5e (didn't realize $m_{Y}(t)=E(m_{Y|N}(t))$)
- STAB52 fin 2023 Q3a (average of variance not on formula sheet...)
- STAB52 fin 2023 Q3 entire question (weirdo application questions that screwed me over) __
- STAB52 fin 2023 Q4a (forgot about Cauchy Schwartz inequality...) _mistaken_
- STAB52 fin 2023 Q5b (difficult combinatorics problem) _mistaken_ 
- STAB52 fin 2023 Q5c (forgot definition of NegativeBinomial) _mistaken_ 
- STAB52 fin 2023 Q6c (super hard combinatorics problem... wanna kill myself right now OMG) _mistaken_ 
- STAB52 fin 2024 Q4c (remember central value theorem takes $\mu$ and $\sigma$ from the iid RVs, not the average) _mistaken_
- STAB52 fin 2024 Q4d (did not realize I need to manually compute the exact values for parameters of gamma distribution) _mistaken_
- STAB52 fin 2024 Q6 weird symmetry problem 
- STAB52 fin 2024 Q5 (too lazy to do) _to do_

# to ask
[[Sotirios (STAB52 prof) to talk]]
- STAB52 fin 2022 Q3b, why do we neglect $\sqrt{ n }$ in the formula?
- When applying Chebyshev's ineq, a lot of the times, we sort of just ignore the absolute value in the formula  (e.g. STAB52 fin 2022 Q3d)

# Important content not on the formula sheet
- MGF method formula ($m_{X_{1}+\dots+X_{n}}(t)=m_{X_{1}}(t)\dots m_{X_{n}}(t)$) _important_
- moment definition and r'th central moment definition
- average of mean, average of variance for iid RVs _important_
- convergence in probability/distribution
- conditional expected value, conditional variance _important_
- $\displaystyle E(Z)=E[g(X,Y)]=\sum_{x}\sum_{y}g(x,y)p_{X,Y}(x,y)$ _important_
- Binomial theorem ($\displaystyle\binom{n}{k}=\binom{n-1}{k-1}+\binom{n-1}{k}$)
- sum of iid RVs [[distributions as sum of i.i.d. RVs]] _important_
- our negative binomial formula counts number of trials, not number of failures. The formula for number of failures is $\displaystyle P(X=x)=\binom{x+r-1}{x}p^r(1-p)^x$ _important_

# questions to talk about
- STAB52 fin 2021 Q5b, really cool question about CDF mistake
- STAB52 fin 2022 Q5b, really cool application of distributions as sum of iid RVs [[distributions as sum of i.i.d. RVs]]

At the end, tell them to take a walk before the exam, eat well, drink well, SLEEP WELL (most importantly). Get some coffees before the exam, I usually prefer to drink it around 45 minutes before it, as it takes affect usually in 45 minutes. Try not to give yourself too much work on the day of the exam, do everything before it, it's gonna help a lot. Get up early, do your best.

# notes
## general notes
- $\displaystyle \lim_{ n \to \infty }P(X_{n})$ does not necessarily equal to $\displaystyle P\left(\lim_{ n \to \infty }X_{n}\right)$
- For finding $E(X|Y)$, if $X=g(y)$, then $E(X|Y)=E(g(Y)|Y)=g(y)$ (_IMPORTANT! YOU FORGOT IT TWICE!!!!- - - -_)
- $m_{Y}(t)=E(m_{Y|N}(t))$, this is a result of LOTE
- remember central value theorem takes $\mu$ and $\sigma$ from the iid RVs, not the average's $\mu$ and $\sigma$

## Application of LOTE or LOTV
For questions asking for $E(X)$, steps:
- Find the distribution of $X|Y$
- Use the formula sheet to find $E(X|Y)$, you should get $g(y)=E(X|Y)$, for some function $g$
- Plugin into $E(X)=E(E(X|Y))$, where you evaluate the expected value in terms of $y$

For questions asking for $V(X)$, follow a similar steps as above

## less useful notes
- (ps11 q5) for a sequence of RVs $\displaystyle \{ X_{n} \}_{n=0}^\infty$, $X_{n}\sim Poisson(n)$, $X_{n}$ converges to a normal distribution.
