---
title: program correctness sample
created: Wednesday 17th September 2025 15:54
last_modified: Wednesday 17th September 2025 15:54
aliases: []
tags:
  - computer-science/computation-logic/program-correctness
course:
  - CSCB36
LEC:
  - "3"
---
# program correctness proof sample (loop)
Consider example
``` py
s = 0; d = 1; i = 0
while i < n:
	s = s + d
	d = d + 2
	i = i + 1
return s
```


## trace (rough work)
`n = 3`

| `i` | `d` | `s` |
| --- | --- | --- |
| 0   | 1   | 0   |
| 1   | 3   | 1   |
| 2   | 5   | 4   |
| 3   | 7   | 9   |

## step 1: Define LI
a) find looping variable (`i` in this case) and it's range: $0\leq i\leq n$ (\*)
b) $s=i^2$
c) $d=2i+1$

(\*) Note that it's not $0\leq i<n$ because by the final iteration, `i+=1` reaches to `n`

## step 2: Prove LI holds
- Basis: On entry to loop:
	`i = 0, s = 0` (by line 1)
	Therefore, `s = i^2`
	as wanted

- induction step: Consider an arbitrary interation
	Suppose LI holds before the iteration (IH)
	WTP: LI holds after the iteration (ie holds for i', s')
	`i' = i + 1, s' = s + d` (by lines 3,5)
	By line 2, `i < n`
	Therefore, 
	`0 <= i'` (by LI)
	`  = i + 1`
	`  <= n`
	As wanted for LI(a)
	
	`s' = s + d`
	`   = i^2 + 2i + 1` (by IH)
	`   = (i + 1)^2`
	`   = (i')^2`
	As wanted for LI(b)
	
	`d' = d + 2`
	`   = 2i + 1 + 2` (by IH)
	`   = 2(i + 1) + 1`
	`   = 2i' + 1`
	As wanted for LI(c)

## step 3: Prove partial correctness
Suppose loop halts and consider the values of `i` and `s` on exit
By exit condition, `i >= n`
By LI(a), `i <= n`
Therefore, `i = n`
By LI(b), `s = i^2 = n^2`, which is returned on line 6, as wanted


## step 4: find expression
With each iteration of the loop we associate the expression
`e = n - i`

## step 5: Prove (A) and (B), $e\in\mathbb{N}$
- (A) By LI(a), $e\geq 0$
- Consider arbitrary iteration
$$
\begin{align}
e'&=n-i' \\
&=n-(i+1)&&\text{by line 5} \\ \\
&=(n-i)+1 \\
&=e-1 \\
&<e \\
\end{align}
$$
as wanted

