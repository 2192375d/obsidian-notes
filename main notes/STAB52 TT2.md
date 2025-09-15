---
title: STAB52 TT2
created: Before 28th July, 2025
last_modified: Monday 21st July 2025 16:37
tags:
  - exam-review
  - probability
course:
  - STAB52
---
## general info
- time: July 21st 17:00-18:30
- location: IC130
- __BRING A CALCULATOR!!!__

## coverage
- continuous RVs
- CDF
- PDF
- uniform distribution
- exponential distribution
- gamma distribution
- normal distribution _to review, not on previous exams_

- transformations
- discrete univariate transformations
- continuous univariate transformations
- general method
- CDF method
- PDF method

- joint PMF
- joint CDF
- joint PDF

- marginal PMF
- marginal CDF
- marginal PDF

- multinomial distribution _to review, not on previous exams_
- multivariate normal distirbution _to review, not on previous exams_

- conditional PMF
- conditional CDF
- conditional PDF
- independent RVs (and it's properties)

- multivariate transformations
- PMF method for multivariate transformations
- CDF method for multivariate transformations
- PDF method for multivariate transformations

- ordered statistics _to review, not on previous exams_
- independent and identically distributed RVs (i.i.d.) _to review, not on previous exams_
- ordered statistics' max/min _to review, not on previous exams_
- sum of RVs (convolution)

- expected value for discrete RV
- expected value of continuous RVs
- expected value of indicators _to review, not on previous exams_
- expected value of functions of RVs
- expected value properties (linearity all that shit)

- variance
- covariance
- variance/covariance properties

## Todo
- Double check previously planned to ask questions, maybe add them on the list

- midterm 2020 (done)
- midterm 2021 (done)
- midterm 2022 (done)
- midterm 2023 (done)
- midterm 2024 (done)

- redo quiz 5
- redo quiz 6
- redo quiz 7
- redo quiz 8

- Do PS5 (worksheet and textbook done)
- Do PS6 (worksheet done)
- Do PS7 (half done)
- Do PS8 (half done)

__TODOs for tomorrow (21st)__
- __Complete PS8 latter half if have time, derive all the formulas__
- __review multinomial distribution, ordered stats, i.i.d., ordered stats max and min__
- __Carefully double check the questions to ask TAs, make sure everything are clear, and note the answers down__
- __Remember to address to to everyone to join the study session__

## notes
- distribution can be PDF, or CDF, or PMF, even MGF, it's anything that describes a RV
- $\displaystyle \phi(x)=\frac{1}{\sqrt{ 2\pi }}\exp \left\{  -\frac{x^2}{2}  \right\}$, is the bell-shape curve, as well as a density function
- To prove a function $F_{X}$ is a CDF, check end of this :[[cumulative distribution function (CDF)]]
- Not only continuous RV can have PDF/CDF, discrete RV have that as well (check 2.5.13 for specific example). In other words, a RV with PDF/CDF can have cases where $F(X\leq a)\neq F(X<a)$ _mistaken_
- When dealing with joint distributions, just break down into every sub sub sub cases if necessary (e.g. PS6 Q7)
- Check PS6 Q9, weirdo question and make sure that you know if this will be on the exam
- bivariate distributions are (probably) not on the exam? Except for multivariate normal distribution
- When dealing with LEC6 contents (joint PMF, CDF, PDF), try drawing the graph for the area we care about. More specifically, review and make sure not to make the same mistake from PS6 Q11 c) _mistaken_ _IMPORTANT_
- A lower dimensional subspace of two RV's joint distribution has a probability of 0.0 (PS6 Q11 d) _mistaken_
- Conditional PMF's sum is still 1 (e.g. $\displaystyle \sum_{x}P(X=x|Y=3)=1.0$)
- if $P(X)=P(Y)$, then $P(X|Y)=P(Y|X)$
- sometimes it's just more helpful to rewrite $F_{X}(x)=P(X\leq x)$ (Q7a) 2020 tt2) _mistaken_
- when doing change in variable, change the RV, not the bound (e.g. $P(Y\leq y)=P\left( \frac{1}{X} \leq y\right)\neq P\left( Y\leq \frac{1}{x} \right)$, given $Y=\frac{1}{X}$, mistaken on Q8b) 2020 tt2) _mistaken_
- Memorize the correlation coefficient cause for some reason it's not on the formula sheet $\displaystyle p_{X,Y}=\frac{Cov(X,Y)}{\sigma_{X}\sigma_{Y}}$ _IMPORTANT_
- REMEMBER TO WRITE THE DOMAIN AFTER DERIVING AN EQUATION _IMPORTANT_
- Although variance is always positive, covariance can be negative (direction wise)
- when computing Jacobian, e.g. $|J(h^{-1}(w,z))|$, make sure to first get $J(x,y)$ first, then plug in $h^{-1}(w,z)$, instead of differentiating with respect to $w,z$. _IMPORTANT_ (tt2 2024 Q2d)


## stuffs to yap about during the review session by me
- $\mu_{X}$ is very misleading, throughout the exam, just think about it as $E(X)$, same goes for $\sigma$
- variance is always positive, you can prove it (easily), but covariance can be negative (and explain the intuition behind)

## fun questions
- 2.4.15, 2.4.16 (2.4.16 is a super cool proof)
- tt2 2022 Q2 b (build gamma equation from Scratch) _to yap_
- tt2 2022 Q3 _to yap_
- tt2 2023 Q2 (for d, mention how $p_{F|M}$ also sums up to 1, and why you should just write in the most standard notation $P(F=f|M\leq 2)$ when you are confused) _to yap_
- Same question as previous, spend as little time reading the quesiton as possible cause it's usually useless, the chart is what matters.
- tt2 2024 Q3 _to yap_


## extra questions I messed
- PS7 Q1
- tt2 2020 Q1a
- tt2 2020 Q9a
- tt2 2021 Q1b
- tt2 2021 Q2c (correlation coefficient one)
- tt2 2021 Q3c
- tt2 2021 Q4b (forgot to bound the integral...)
- tt2 2021 Q4c (weird domain issue in my to ask section)
- tt2 2022 Q1c (forgot how to do transformation)
- tt2 2022 Q2d
- tt2 2022 Q3
- __tt2 2024 Q2d__
- __tt2 2024 Q3e, g__

## important things not on cheat sheet
- ALL OF THOSE PDF->CDF->PMF distribution conversion
- what it means for to RVs to be independent
- convolution method on discrete values: $\displaystyle f_{Z}(z)=\sum_{x}p_{X,Y}(x,z-x)$
- multinomial distribution

## To ask
- Explain PS5 Q8 _done_
- Do we need to worry about correlation coefficient? _done, no worry_
- For any problem, do we have to provide the domain after deriving the distribution. _done, yes_
- Do we have to remember probability simulation stuffs? _done, no_
- Q1b on PS8, where did the 4 come from? It intuitively sounds right, but is there any formal way of doing it?
- Q7a, HOW THE HECK DO I PROVE WHICH VALUE IS $\displaystyle\sum_{x=1}^\infty \frac{x}{2^x}$ converges to???? Like bro wtf? I'm confident that no A37 convergence test does that crazy magic
- Q7b, how does it even make sense for me to receive $\infty$ amount of money? Like intuitively I don't feel like this will happen, is it due to it's high variance (how do we even find the variance for this though?)?
- ~~2021 4c, why do we need to state the domain to be $\sqrt{ y }\leq |x|\leq 1$? can we not just say $0\leq y\leq 1$ like part b? In other words, do we need to worry about the domain of the second variable for conditional functions? I thought the conditional functions are univariate so we only care about $y$ in this context
- ~~2022 2d, why can I not integrate both marginal pdfs to find the answer? _mistake_
- ~~same question as 2021 4c, in 2023 3c, why do we express the final domain in terms of $x$? mistake, isn't it supposed to be an univariate function on $y$? If not, how do we determine when the expression needs domain in $x$ or $y$ for $x|y$?


## thoughts
(after done 2020)
it's overall okayish, just lots of points I need to memorize, hope things will get better as I start 2021
(after done 2024)
There was a HUGE gap between 2023 to 2024, I think this is exactly the breaking point! I'm getting everything!