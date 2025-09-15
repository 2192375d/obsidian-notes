Given multiple constraints
$$
g_{1}=c_{1},g_{2}=c_{2},\dots,g_{k}=c_{k}
$$
S.T. $\nabla g_{1}(\mathbf{x}_{0}),\nabla g_{2}(\mathbf{x}_{0}),\dots,\nabla g_{k}(\mathbf{x}_{0})$ are linearly independent. Let $S$ be the set where all constraints are satisfied, e.g.
$$
S=\{ \mathbf{x}:g_{1}(\mathbf{x})=c_{1},\dots,g_{k}(\mathbf{x})=c_{k}\}
$$
, and $\mathbf{x}_{0}\in S$, then the method of __Lagrange multiplier__ generalizes to multiple constraints as follows

#### theorem
If $f|_{S}$ has a local extremum at $\mathbf{x}_{0}$, then there are constants $\lambda_{1},\dots,\lambda_{k}$ S.T.
$$
\nabla f(\mathbf{x}_{0})=\lambda_{1}\nabla g_{1}(\mathbf{x}_{0})+\dots+\lambda_{k}\nabla g_{k}(\mathbf{x}_{0})
$$
