$f(x)$ is considered quasi convex if:
1. Domain of $f(x)$ is a convex set
2. $\forall x,y \in dom(f(x))$ and $0\leq\lambda\leq1$ there holds: $$ f((1-\lambda)x+\lambda y)\leq \max (f(x),f(y))$$
note that for a [[convex function]] and a [[quasi convex function]] **both require a convex function domain**. The difference lies in that a quasi convex function may be convex, but is not necessarily so. e.g.:![[quasiConvexFunction.png]]

criterion 1: Whether the domain of $f(x)$ is convex cannot be seen from the plot. So assume it is already proven.

criterion 2: Function evaluations between two points on the line will always be lower-valued than at least one of the two points.

Hence, the plot above is of a [[quasi convex function]]. True convexity would have implied that the for criterion 2 the function evaluation would always be below a linear interpolation between the two points, not just the points themselves. See: [[convex function]].