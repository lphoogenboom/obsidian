
Optimisation always performed according to a framework. Although there are many classifications of optimisation problems, the problem is always some variation of the framework below:
$$ \begin{aligned} 
\min_x f(x)&\\ \text{subject to:}
\\h(x)&=0\\ g(x)&\leq0
\end{aligned} $$
In this framework $f(x)$ denotes the **objective function**. This function in minimised for the variable $x$ **(can be a vector)**. $h(x)$ forms the equality constraints, and $g(x)$ forms the inequality constraints.

A maximisation problem can always be rewritten to a minimisation problem using: $\max_x f(x) = -\min_x (-f(x))$

- ## Linear programming
	- Equality constrained:
		- $$ \begin{aligned} min_x c^\top x,\\ Ax = b,\\ x \geq 0  \end{aligned}$$
		- [[stopping conditions]]: Guaranteed optimum found in finite steps.
	- Inequality constrained:
		- $$ \begin{aligned} min_x c^\top x,\\ Ax \leq b,\\ x \geq 0  \end{aligned}$$
		- [[stopping conditions]]: Guaranteed optimum found in finite steps.
- ## Quadratic programming
	- Equality constrained:
		- $$ \begin{aligned} min_x \frac{1}{2}x^\top H x+c^\top x,\\ Ax = b,\\ x \geq 0  \end{aligned}$$
		- [[stopping conditions]]: Guaranteed optimum found in finite steps.
	- Inequality constrained:
		- $$ \begin{aligned} min_x \frac{1}{2}x^\top H x+c^\top x,\\ Ax \leq b,\\ x \geq 0  \end{aligned}$$
		- [[stopping conditions]]: Guaranteed optimum found in finite steps.
- ## Convex optimisation
	- $$\begin{aligned} min_x f(x),\\ g \leq 0 ,\\ f(x)\text{ and }g(x)\text{ convex}. \end{aligned}$$
	- [[stopping conditions]]:
		- Ellipsoid method: $$\begin{aligned} |f(x_k)-f(x^*)|\leq \epsilon_f,\\g(x_k)\leq \epsilon_g,\\||x_k-x^*||\leq \epsilon_x  \end{aligned}$$
		- Others: $$\begin{aligned} |f(x_k)-f(x^*)|\leq \epsilon_f,\\g(x_k)\leq \epsilon_g\end{aligned}$$
- ## Nonlinear optimisation
	- $$\begin{aligned} min_x f(x), \\ h(x) = 0, \\ g(x)\leq0, \\ f(x),h(x)\text{ and }g(x)\text{ non-convex \& nonlinear} \end{aligned}$$
	- [[stopping conditions]]:
		- Unconstrained:
			- $$ ||\nabla f(x_k) ||_2 \leq \epsilon_\nabla$$
		- Constrained (These are KKT):
			- $$\begin{aligned}||\nabla f(x_k) + \nabla h(x_k)\mu + \nabla h(x_k)\lambda||_2 =\epsilon_{KT1},\\ |\mu^\top g(x)|\leq\epsilon_{KT2},\\ \mu\geq -\epsilon_{KT3},\\ ||h(x)||_2\leq\epsilon_{KT4},\\ g(x)\leq\epsilon_{KT5}\end{aligned}$$
			- **Note: The KKT is modified with absolution, 2-norms, and (negative) $\epsilon$.**

- *Each optimisation problem includes [[stopping conditions]]. These do not only depend on the the type of optimisation problems, but also on type the constraints. See: [[stopping conditions]].*


