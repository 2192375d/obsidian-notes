---
title: regex closed properties proof through FSA method
created: Wednesday 15th October 2025 15:17
last_modified: Wednesday 15th October 2025 15:17
aliases: []
tags:
  - computer-science/computation-logic/automata
  - computer-science/string/regex
course:
  - CSCB36
LEC:
  - "7"
---
In general, if languages $L_{1},L_{2}$ are regular, then, $\overline{L_{1}},L_{1}\cup L_{2},L_{1}\cap L_{2},L_{1}\cdot L_{2},L_{1}^*$ are regular

# closure properties - FSA method
<u>complement</u>
Let $M=(q,\Sigma,\delta,s,F)$ be a DFSA
Want a DFSA $\overline{M}=(\overline{Q},\Sigma,\overline{\delta},\overline{s},\overline{F})$ S.T. $\mathcal{L}(\overline{M})=\overline{\mathcal{L}(M)}$

Choose: 
- $\overline{Q}=Q$
- $\overline{\delta}=\delta$ 
- $\overline{s}=s$
- $\overline{F}=Q-F$

Then,
$$
\begin{align}
x\in\mathcal{L}(\overline{M}) & \iff \delta^*(s,x)\in Q-F \\
&\iff\delta^*(s,x)\not\in F \\
&\iff x\not\in\mathcal{L}(M)  \\
&\iff x\in\overline{\mathcal{L}(M)}
\end{align}
$$
As wanted

<u>union</u>
Let $M_{1},M_{2}$ be DFSAs, where $M_{1}=(Q_{1},\Sigma,\delta_{1},s_{1},F_{1}),M_{2}=(Q_{2},\Sigma,\delta_{2},s_{2},F_{2})$
Want NFSA $M_{\cup}$ S.T. $\mathcal{L}(M_{\cup})=\mathcal{L}(M_{1})\cup\mathcal{L}(M_{2})$

intuition: 
![[closed properties through FSA method 2025-10-15 15.26.47.excalidraw|50%]]

<u>intersection</u>
Let $M_{1},M_{2}$ be DFSAs, where $M_{1}=(Q_{1},\Sigma,\delta_{1},s_{1},F_{1}),M_{2}=(Q_{2},\Sigma,\delta_{2},s_{2},F_{2})$
Note that $L_{1}\cap L_{2}=\overline{L_{1}}\cup\overline{L_{2}}$
Want DFSA $M_{\cap}=(Q_{\cap},\Sigma,\delta_{\cap},s_{\cap},F_{\cap})$ S.T. $\mathcal{L}(M_{\cap})=\mathcal{L}(M_{1})\cap\mathcal{L}(M_{2})$

![[closed properties through FSA method 2025-10-15 15.37.26.excalidraw|100%]]

<u>concatenation</u>
Let $M_{1},M_{2}$ be DFSAs
Want NFSA $M_{\cdot}$ S.T. $\mathcal{L}(M_{\cdot})=\mathcal{L}(M_{1})\cdot\mathcal{L}(M_{2})$
![[closed properties through FSA method 2025-10-15 15.44.04.excalidraw|80%]]

<u>Kleene star</u>
Let $M$ be DFSA
Want a NFSA $M^*$ S.T $\mathcal{L}(M^*)=\mathcal{L}(M)^*$
![[language closed properties through FSA method 2025-10-15 15.54.48.excalidraw|100%]]