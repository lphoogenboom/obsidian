
Optimization always performed according to a framework. Although there are many classifications of optimization problems, the problem is always some variation of the framework below:
$$ \begin{aligned} 
\min_x f(x)&\\ \text{subject to:}
\\h(x)&=0\\ g(x)&\leq0
\end{aligned} $$
In this framework $f(x)$ denotes the **objective function**. This function in minimized for the variable $x$ **(can be a vector)**. $h(x)$ forms the equality constraints, and $g(x)$ forms the inequality constraints.

A maximisation problem can always be rewriten to a minimisation problem using: $\max_x f(x) = -\min_x (-f(x))$

## Linear programming
equality constrained:
$$ \begin{aligned} min_x c^\top x,\\ Ax = b,\\ x \geq 0  \end{aligned}$$
inequality constrained:
$$ \begin{aligned} min_x c^\top x,\\ Ax \leq b,\\ x \geq 0  \end{aligned}$$
## Quadratic programming
equality constrained:
$$ \begin{aligned} min_x \frac{1}{2}x^\top H x+c^\top x,\\ Ax = b,\\ x \geq 0  \end{aligned}$$
inequality constrained:
$$ \begin{aligned} min_x \frac{1}{2}x^\top H x+c^\top x,\\ Ax \leq b,\\ x \geq 0  \end{aligned}$$
## Convex optimization
$$\begin{aligned} min_x f(x),\\ g \leq 0 ,\\ f(x)\text{ and }g(x)\text{ convex}. \end{aligned}$$
## Nonlinear optimization
$$\begin{aligned} min_x f(x), \\ h(x) = 0, \\ g(x)\leq0, \\ f(x),h(x)\text{ and }g(x)\text{ non-convex \& nonlinear} \end{aligned}$$
