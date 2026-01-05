---
title: regex properties
created: Wednesday 1st October 2025 20:16
last_modified: Wednesday 1st October 2025 20:16
aliases: []
tags:
  - computer-science/string/regex
course:
  - CSCB36
LEC:
  - "5"
---
# equivalence of regexes
- communitivity of union: $(R+S)\equiv(S+R)$
- associativity of union: $((R+S)+T)\equiv(R+(S+T))$
- associativity of concatenation: $((RS)T)\equiv(R(ST))$
- left distributivity: $(R(S+T))\equiv((RS)+(RT))$
- right distributivity: $((R+S)T)\equiv((RT)+(ST))$
- identity for union: $(R+\emptyset)\equiv R$
- identity for concatenation: $(R\epsilon)\equiv R$
- annihilator for concatenation: $R \emptyset \equiv \emptyset$
- idempotence of Kleene star: $R^*=(R^*)^*$
