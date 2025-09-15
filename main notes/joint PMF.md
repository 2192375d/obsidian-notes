---
title: joint PMF
created: Before 28th July, 2025
last_modified: Monday 28th July 2025 16:48
tags:
  - probability/PMF
  - probability/joint
course: STAB52
LEC: 6
---


# definition
Let $X,Y$ be discrete RVs, and we are only interested in specific combinations of values, then their joint PMF is defined as 
$$p_{X,Y}(x,y)=P(X=x,Y=y)=P(\{X=x\}\cap\{Y=y\})$$
Same applies to when you have $\geq 3$ RVs

note that $p_{X,Y}(x,y)\geq 0,\forall x,y$ and $\sum_{x,y}p_{X,Y}(x,y)=1$

_example_
Roll two fair 6-sided cide and let $X_{min}$=minimum value, $X_{max}$=maximum value of roll. Find the joint PMF of $(X_{min},X_{max})$
	possible values at $(X_{min},X_{max})\in\{(x,y):1\leq x\leq y\leq 6\}$ $$p_{X_{min},X_{max}}(x,y)=p(X_{min}=x,X_{max}=y)=\begin{cases}\frac{1}{36},&x=y\in\{1,\dots,6\}\\\frac{1}{18},&x\neq y\text{ and }x,y\in\{1,\dots,6\}\\0,&otherwise\end{cases}$$
	(confirm this is a valid PMF)$$\sum_{x,y}p_{X_{min},X_{max}}(x,y)=\frac{1}{36}*6+\frac{2}{36}*15=\frac{6+30}{36}=1$$
kadnjfk;jdfsajdfjalkrehtrw3ruoidSDLFbkajhfljlrhweskgfhjlkadjyslfieura;wlUYEQWRIFEULK;LUXA;XSIDFUNKGJSYDKULSDJKFEHUOGILKYLDPUOSJHWIFKSFLUHDRYFGKJWDFUITGYDHRJWEKYV4DHUAYSRGFKAEJNUSDRJKEWHJRFSEDKSANBVGYNSCHJKADGEBVYWUI$LATEXING IS SO FUCKING HARD!!!!----$
