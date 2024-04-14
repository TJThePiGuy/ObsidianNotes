Thomas Omiatek

## Problem 1

Let $P_0=360,000$ be the initial amount of money invested and $r=0.075$ be the annual interest. The interest rate $R_{0}$ after 30 days is calculated as 
$$\begin{align*}
R_{0}&= \left(1+\frac{r}{365}\right)^{30}\\
&= \left(1+\frac{.075}{365}\right)^{30}\\
&\approx 1.00618
\end{align*}$$
The amount owed on the mortgage $P_{m}$ after paying $M_{30}$ dollars in each pay period after $m$ pay periods (in this case, months) is 
$$P_{m}=P_{0}R_{0}^{m}-M_{30}\left(\frac{1-R_{0}^{m}}{1-R_{0}}\right)$$
To pay the loan off after $m=360$ pay periods, we set $P_{360}=0$ and solve for $M_{30}$:
$$\begin{gather*}
	0=P_{0}R_{0}^{360}-M_{30}\left(\frac{1-R_{0}^{360}}{1-R_{0}}\right)\\
	M_{30}\left(\frac{1-R_{0}^{360}}{1-R_{0}}\right)=P_{0}R_{0}^{360}\\
	M_{30}=P_0R_{0}^{360}\left(\frac{1-R_{0}}{1-R_{0}^{360}}\right)\\
	M_{30}\approx2497.32
\end{gather*}$$
### Part a

We now will be paying the mortgage, but biweekly with payments $N_{30}=\frac{M_{30}}{2}=1248.66$. Now, the interest rate $R_{1}$ will be different: 
$$\begin{align*}
R_{1}&= \left(1+\frac{r}{365}\right)^{14}\\
&= \left(1+\frac{.075}{365}\right)^{14}\\
&\approx 1.00288
\end{align*}$$
Our new amount owed after paying $m$ biweekly payments of $N_{30}$ is 
$$P_{m}=P_{0}R_{1}^{m}-N_{30}\left(\frac{1-R_{1}^{m}}{1-R_{1}}\right)$$
We want to find the amount of payments $m$ such that $P_{m}=0$, so we solve for $m$: 
$$\begin{gather}
0=P_{0}R_{1}^{m}-N_{30}\left(\frac{1-R_{1}^{m}}{1-R_{1}}\right)\\
0=\frac{P_{0}}{N_{30}}R_{1}^{m}-\frac{1}{1-R_{1}}+R_{1}^{m}\left(\frac{1}{1-R_{1}}\right)\\
\frac{1}{1-R_{1}}=R_{1}^{m}\left(\frac{P_0}{N_{30}}+\frac{1}{1-R_{1}}\right)\\
1=R_{1}^{m}\left(\frac{P_{0}(1-R_{1})}{N_{30}}+1\right)\\
\left(\frac{P_{0}(1-R_{1})}{N_{30}}+1\right)^{-1}=R_{1}^{m}\\
-\ln{\left(\frac{P_{0}(1-R_{1})}{N_{30}}+1\right)}=m\ln{R_{1}}\\
m=\frac{-\ln{\left(\frac{P_{0}(1-R_{1})}{N_{30}}+1\right)}}{\ln{R_{1}}}
\end{gather}$$
After plugging in our values for $P_{0}$, $R_{1}$, and $N_{30}$, I found that $m=618$, which means after 618 periods of two weeks, the mortgage will be paid off. 618 periods of two weeks is about 23 years 10 months, so you will pay off the same mortgage at the same interest rate 6 years 2 months sooner if you pay half the payment every other week than if you pay the full payment every month.
### Part b

The total amount saved is calculated below:
$$\begin{align*}
\text{Amount Saved}&= M_{30}\cdot360-N_{30}\cdot m\\
&= \$128,568.11
\end{align*}$$
You would save $120 thousand by paying biweekly vs. paying weekly.
### Part c

When taking out a 15 year mortgage with the same initial price and same interest rate, we return to the equation at the beginning of the problem: 
$$P_{m}=P_{0}R_{0}^{m}-M_{15}\left(\frac{1-R_{0}^{m}}{1-R_{0}}\right)$$
Now, instead of setting $P_{360}$=0, we set $P_{180}=0$ and solve for $M_{15}$:
$$\begin{gather*}
	0=P_{0}R_{0}^{180}-M_{15}\left(\frac{1-R_{0}^{180}}{1-R_{0}}\right)\\
	M_{15}\left(\frac{1-R_{0}^{180}}{1-R_{0}}\right)=P_{0}R_{0}^{180}\\
	M_{15}=P_0R_{0}^{180}\left(\frac{1-R_{0}}{1-R_{0}^{180}}\right)\\
	M_{15}\approx3320.77
\end{gather*}$$
### Part d

To find how much you would save by paying the mortgage off in 15 years instead of 30, we just perform the following calculation:
$$\begin{align*}
\text{Amount Saved}&= M_{30}\cdot 360-M_{15}\cdot 180\\
&= \$301,297.16
\end{align*}$$
You would save $300 thousand by paying the mortgage off in 15 years instead of 30. 

## Problem 2

For this problem, we wish to write a difference equation for the amount of red blood cells in the body per day. The general difference equation for this is $x_{n+1}=x_{n}-d(x_{n})+p(x_{n})$, where $d(x_{n})$ is the amount of red blood cells destroyed and $p(x_{n})$ is the amount of red blood cells created.

First, we assume that a constant fraction of red blood cells are destroyed every day. That would mean $d(x_{n}) = cx_{n}$ for some $c\in(0,1)$. 

Next, we make some assumptions about how red blood cells grow. More specifically, more are created when there are less in the system, so we know $p(x_n)$ will have a form similar to $r \cdot(L-x_{n})$, where $r\in(0,1)$ is some fraction at which they grow and $L$ is the maximum number of red blood cells produced. We also know that it takes some delay for the red blood cells to be produced, which we assume to be 3 days. Therefore, we can say that $p$ shouldn't be a function of $x_n$, but rather, a function of $x_{n-3}$. We then write $p(x_{n})=r \cdot(L-x_{n-3})$.

Our final difference equation, which ends up being fourth order, is 
$$x_{n+1}=x_{n}-cx_{n}+r \cdot(L-x_{n-3})$$

## Problem 3

### Part a

Let $a_n$ be the pollution in Lake Erie, and $b_n$ the pollution in Lake Ontario. We can write the pollution in each lake as shown here:
$$\begin{align*}
a_{n+1}&= a_{n}-0.38a_{n}=0.62a_{n}\\
b_{n+1}&= b_{n}-0.13b_{n}+0.38a_{n}+25=0.87b_{n}+0.38a_{n}+25
\end{align*}$$
### Part b

We are going to solve the second equation for $a_n$ in terms of $b_n$ and $b_{n+1}$:
$$\begin{gather*}
0.38a_{n}=b_{n+1}-0.87b_{n}-25\\
a_{n}=\frac{1}{0.38}(b_{n+1}-0.87b_{n}-25)
\end{gather*}$$

We then substitute this into the first equation:
$$\begin{gather*}
a_{n+1}=0.62a_{n}\\
\frac{1}{0.38}(b_{n+2}-0.87b_{n+1}-25)=\frac{0.62}{0.38}(b_{n+1}-0.87b_{n}-25)\\
b_{n+2}-0.87b_{n+1}-25=0.62b_{n+1}-0.5394b_{n}-15.5\\
b_{n+2}-1.49b_{n+1}+0.5394b_{n}-9.5=0
\end{gather*}$$
### Part c

To find the general solution of a second-order nonhomogeneous difference equation, we write $b_n$ as the sum of another sequence and the fixed point:
$$
b_{n}=\bar{b}+c_{n}
$$

Now, we find the fixed point: we set $b_{n+2}=b_{n+1}=b_{n}=\bar{b}$ in the second order difference equation:
$$
\begin{gather*}
\bar{b}-1.49\bar{b}+0.5394\bar{b}-9.5=0\\
0.0494\bar{b}=9.5\\
\bar{b}=\frac{9.5}{0.0494}\approx 192.308
\end{gather*}
$$
### Part d

### Part e

### Part f

## Problem 4

$$a_{n+1}=a_{n}-ka_{n}+b$$
### Part a

The parameter $k$ in this equation represents wat percentage of the drug is removed form the bloodstream each day, and $b$ represents the new dosage every day of the drug.

### Part b

To ensure that the model is biologically meaningful, $0\leq k\leq 1$ and $b \geq0$. 

### Part c

The fixed point of the model is found by replacing $a_{n}$ and $a_{n+1}$ with $\bar{a}$:
$$
\begin{gather*}
\bar{a}=\bar{a} - k \bar{a}+b\\
k \bar{a}=b\\
\bar{a}=\frac{k}{b}
\end{gather*}
$$

### Part d

The cobweb diagram below shows the cobweb diagram for $k=0.5, b=1$. The blue line represents $a_{n+1}=a_{n}$, the purple line $a_{n+1}=0.5a_{n}+1$, and the red point is the fixed point $(2,2)$. The yellow lines are evaluating $a_{n+1}$, and the green lines are moving over to the blue line $a_{n+1}=a_n$. Notice that we converge to the fixed point, which means that the fixed point is stable. 

![[HW2 P4.pdf]]

### Part e

$$
\begin{gather*}
a_{1}=0.5(0)+1=1\\
a_{2}=0.5(1)+1=1.5\\
a_{3}=0.5(1.5)+1=1.75\\
a_{\infty}=\frac{1}{0.5}=2
\end{gather*}
$$

### Part f

Our goal is to fix the fixed point between $4$ and $6$, so we write $$
\begin{gather*}
4\leq \frac{b}{0.5}\leq 6\\
2\leq b\leq 3
\end{gather*}
$$
To have an effective, but non-toxic, drug, $b$ must be on the interval $[2,3]$.

## Problem 5

### Part a

