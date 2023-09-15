$f(x)$ is considered convex if:
1. Domain of $f(x)$ is a convex set
2. $\forall x,y \in dom(f(x))$ and $0\leq\lambda\leq1$ there holds: $$ f((1-\lambda)x+\lambda y)\leq (1-\lambda)f(x)+\lambda f(y)$$
note that for a [[convex function]] and a [[quasi convex function]] **both require a convex function domain**. The difference lies in that, different from a quasi convex function, a convex function must always be below (or on top) an interpolation of the selected points. E.g.:
![[convexFunction.png]]


criterion 1: Whether the domain of $f(x)$ is convex cannot be seen from the plot. So assume it is already proven.

criterion 2: Function evaluations between two points on the line will always be lower-valued than at least one of the two points.

Hence, the plot above is of a [[quasi convex function]]. 