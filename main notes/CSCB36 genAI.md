# gen AI tool used
- ChatGPT 5.0
- Grok 4

# input prompt (same for both AI tools, the exact copy and paste)
We define a subset of $\mathbb{Z}^2$ as follows.

Let $V$ be the smallest set such that:
basis: $(1,1),(1,2),(2,1),(2,2)\in V$.
induction step: if $(s,t)\in V$, then $(s+1,t+2),(s+2,t+1)\in V$.

We define a predicate on $\mathbb{Z}$ as follows: $P(n):$ If $x$ and $y$ are integers such that $x+y=n,x\leq 2y$ and $y\leq 2x$, then $(x,y)\in V$.

Use induction to prove that $P(n)$ holds for every integer $n\geq 2$.

# ChatGPT response
![[Pasted image 20250926023715.png]]

# Grok response
![[Pasted image 20250929165439.png]]

# comment on ChatGPT's proof
## base cases proof
For base cases, instead of "$n=2,3,4$", it should be "Consider cases: $n=2,n=3,n=4$" as this follows the structure for proof by cases taught in class.

For each cases, ChatGPT need to mention the case and the case number (eg case 1: $n=2$), also it would be best to write "let $n=2$"

At the end of each individual cases, ChatGPT should mention "As wanted", instead of "Thus $P(2),P(3),P(4)$ hold" after individual cases are proven.

## inductive step proof
At the start of the proof, ChatGPT did not say "Let $n>4$", then $n$ is used directly, this is usage of a variable that is not universally instantiated.

The first line from ChatGPT is:
- "Assume $P(m)$ holds for all $2\leq m\leq n$, we prove $P(n+1)$"
From what we are taught in this class for PCI's format, this should be instead (note the lack of IH indication as well)
- "Assume $P(m)$ holds for all $2\leq m<n$, we prove $P(n)$ (IH)"
Or even better, we can say 
- "Suppose $P(j)$ holds for every $2\leq i<n$ (IH)"
	WTS $P(n)$

ChatGPT did not suppose the antecedent of $P(n)$, instead, it just says:
- "Let integers $x,y$" satisfy $x+y=n+1,x\leq 2y,y\leq 2x$
This should instead be:
- Suppose $x,y$ are integers S.T. $x+y=n,x\leq 2y,y\leq 2x$
As for a direct proof, we must suppose the antecedent, instead of universally instantiating numbers like this.

For the line:
- "We claim at least one of $A$ or $B$" also satisfies the cone constraints $x'\leq 2y',y'\leq 2x'$
This line did not instantiate $x'$ or $y'$, in other words, we don't know what ChatGPT meant by $x'$ and $y'$

Before going to cases, ChatGPT did not say "Consider $2y-x\geq 3$, $2x-y\geq 3$", and then dive into each cases.

The last line "The remaining values $n+1\in \{ 2,3,4 \}$ were handled in the base cases, therefore $P(n+1)$ holds"

There is no need to mention $n+1\in \{ 2,3,4 \}$ as it is not required for the inductive step in a PCI taught in class.

## thing(s) ChatGPT did good
ChatGPT successfully avoided stacks for each case in the induction step.

# comment on Grok's proof
## base case proof
At the start of the proof, Grok said:
- "Verify $P(n)$ for $n=2,3,4$"
This should instead be "Consider cases: $n=2,n=3,n=4$", 
__This is mistake is made by both ChatGPT and Grok__

For each case, instead of "For $n=2$, (proof of $P(2)$)" (or other numbers for $n$), it should be instead: "case 1: $n=2$, (proof of $P(2)$)", and same for $n=3$ and $n=4$
__This mistake is made by both ChatGPT and Grok__

For each case, similar to ChatGPT, Grok did not mention "as wanted" at the end, instead it wrote "Thus $P(2),P(3),P(4)$ hold" at the very end of basis case
__This mistake is made by both ChatGPT and Grok__

## inductive step proof
Grok did not instantiate $n$ (eg writing "Let $n\geq5$"), although it did write "..., where $n\geq 5$", $n$ is still only instantiated in that scope.
__This mistake is made by both ChatGPT and Grok, but Grok did better__

Similar to ChatGPT, Grok did not suppose the antecendent of $P(m)$, instead it universally instantiated the values
__This mistake is made by both ChatGPT and Grok__

There are a lots of "Infamous stack" throughout the inductive step, one example been right after substituting $y=n-x$
$$
n-x\geq 2x-2\to n+2\geq 3x\to x\leq \frac{n+2}{3}
$$
Although Grok did you logical symbol $\to$ to indicate implication, this can still be made better by going from my side to another.

In the end of induction step, Grok did not say "As wanted"
__This mistake is made by both ChatGPT and Grok__


## parts Grok did better
The inductive setup from Grok: 
- "Assume $P(k)$ holds for all integers $2\leq k<n$, where $n\geq 5$"
This is way better than ChatGPT writing:
- "Assume $P(m)$ holds for all $2\leq m\leq n$, we prove $P(n+1)$"
As ChatGPT's inductive setup does not follow what we are taught about PCI in class

For IH, ChatGPT did not mention which one is IH but Grok did

Grok did not make the mistake of not universally instantiating $x',y'$, as they are not even used as a variable, better than ChatGPT instantiating them.

## parts ChatGPT did better
ChatGPT had no "Infamous Stack", but stacks are almost everywhere in induction step for Grok.

# Overall impression
The logics do hold on the most part, and I'm suprised that ChatGPT did the induction step using proof by cases while Grok used contradiction.

However, the format do not exactly follow CSCB36 (especially with regards to the 5 points mentioned on this assignment), but justifications are overall understandable.

# feedback for the assignment
I think the assignment is pretty creative as we get to view and analyze the advantages/flaws of AI doing the proof work for us. One thing I like about this assignment is that this is the only time I know two different AIs can work on the same question and have a much different solution structure. Another thing I liked is that I'm always curious how other people approach to the same question and it always makes me happy to see and realize that the same problem have multiple solutions.

However, there is one thing I don't really like about this assignment, which is that there might be situations where some AI generate like 5 pages of proof (eg Gemini), which takes forever to check. The beginning of the assignment feels very frustrating because of this, as I have to sort of just do trial and error on each models to find out which one actually gives me a short enough proof. This can be improved by leaving a note at the top of the assignment reminding students that we can always try more models if the current one is too challenging to analyze, since if I were a TA and see a 2 pages problem solved in 5 pages, I would not really be happy about it. This also encourages students to try around more AIs which is also beneficial for this assignment.