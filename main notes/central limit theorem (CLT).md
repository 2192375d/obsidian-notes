---
title: central limit theorem (CLT)
created: Before 28th July, 2025
last_modified: Thursday 24th July 2025 11:40
tags:
  - probability/average
  - probability/convergence
  - theorem
course:
  - STAB52
LEC: 11
---
# theorem
Standardized averages of independent RVs with finite means and variance converge in distribution to $(standard)\ normal(\mu=0,\sigma=1)$
$$
Z_{n}=\sqrt{ n }\left( \frac{\overline{X}_{n}-\mu}{\sigma} \right)\to^DN(0,1)
$$
Result can be used to approximate probabilities of $\overline{X}_{n}$ for "large" $n$, based on normal distribution
$$
\overline{X}_{n}\sim^{appr}N(\mu,\sigma^2/n)
$$
_example_
![[Pasted image 20250722155047.png]]
## proof
![[central limit theorem 2025-07-24 11.21.12.excalidraw]]
_example_
![[central limit theorem (CLT) 2025-07-29 14.42.31.excalidraw]]