### Unconstrained optimisation
Because there are no constraints only the objective function needs consideration. Not all unconstrained methods guarantee a finite time to find the optimum, or find a optimum at all. Hence usually a convergence margin $\epsilon_\nabla$ is used.

- Gradient conditions:    
	- $\nabla f(x)\leq \epsilon_\nabla$

### Equality Constrained Optimisation

- Lagrange conditions:    
	- $\nabla f(x)+\lambda \nabla h(x)=0$
	- $h(x) = 0$

### Inequality Constrained Optimisation

- Karush-Kuhn-Tucker conditions (KKT):
	- $\nabla f(x) + \nabla h(x)\mu + \nabla h(x)\lambda =0$
	- $\mu^\top g(x)=0$
	- $\mu\geq =0$
	- $h(x)=0$
	- $g(x)\leq0$