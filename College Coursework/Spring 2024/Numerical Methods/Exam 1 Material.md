# 1.1 Bisection Method

> Consider solving for a root of $f(x)=4-\dfrac{16}{1+x}$. 
> 1. Is $f(x)$ continuous? If not, where is it discontinuous?
> $f(x)$ is discontinuous at $x=-1$.
> 2. Show that there exists at least one root on the interval $[1,7]$.
> $f(1) = 4-\dfrac{16}{2}=-4$ and $f(7)=4-\dfrac{16}{8}=2$. By the MVT, there exists $x\in[1,7]$ such that $f(x)=0$. 
> 3. Show that there exists exactly one root on the interval $[1,7]$.
> $f'(x)=\dfrac{16}{(1+x)^2}>0$, which means that for any $x\in(1,7)$, $f(1)<f(x)<f(7)$. Therefore, there must only exist exactly one root. 

If an expression is less than zero at one value of the unknown and greater at another value AND **the function is continuous**, there is at least one solution on the interval.

If we bisect the interval and see whether the function is positive or negative at the midpoint, we can figure out on which half of the interval a solution must lie. 

Repeat until the interval width is within our tolerance or the function value is acceptable.

> Approximate $\sqrt{ 2 }$ using bisection.

| $a$ | $f(a)$ | $b$ | $f(b)$ | $c=\dfrac{a+b}{2}$ | $f(c)$ |
| ---- | ---- | ---- | ---- | ---- | ---- |
| 1 | -1 | 2 | 2 | 1.5 | 0.25 |
| 1 | -1 | 1.5 | 0.25 | 1.25 | -0. |
## Error of Bisection

The error after $n$ steps of bisection is $$
\epsilon < \dfrac{1}{2^{n+1}}(b_{0}-a_{0})
$$
The number of steps needed within a certain number is found by solving for $n$. 

# Forward and Backward Error

**Forward error** (error in $x$): $\epsilon=|x-x^*|$
**Backward error** (error in $y$): $|f(x)|$

**Secant method** - don't force bracketing root
- Take 2 most recent x-values
**Regular Falsi** - force bracketing root
- Take x-values such that f(a)f(b) < 0