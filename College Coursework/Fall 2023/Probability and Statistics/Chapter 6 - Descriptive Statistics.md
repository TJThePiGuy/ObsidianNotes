# Numerical Summaries of Data

### Sample Mean
> If the $n$ observations in a sample are denoted by $x_{1}, x_{2}, \dots, x_{n}$, the **sample mean** is
> $$
\bar{x}=\frac{x_{1}+x_{2}+x_{3}+\dots+x_{n}}{n}=\frac{\sum_{i=1}^n
x_{i}}{n}$$
### Sample Variance and Sample Standard Deviation
>  If the $n$ observations in a sample are denoted by $x_{1}, x_{2}, \dots, x_{n}$, the **sample variance** is $$
s^2 =\dfrac{\sum_{i=1}^n(x_{i}-\bar{x})^2}{n-1}
$$
>The **sample standard deviation**, $s$, is the positive square root of the sample variance.
> There are $n-1$ **degrees of freedom** in this calculation; since the sum of all deviations from the mean $(x_{i}-x)$ equals 0, knowing $n-1$ of these differences allows you to calculate the missing one.

#### Computation of $s^2$

$$
\begin{align}
s^2  & =\dfrac{\sum_{i=1}^n (x_{i}-\bar{x})^2}{n-1} \\
	 & = \dfrac{\sum_{i=1}^n (x_{i}^2-2x_{i}\bar{x}+\bar{x}^2)}{n-1} \\
	 & = \dfrac{\left( \sum_{i=1}^n x_{i}^2+n \bar{x}^2-2\bar{x}\sum_{i=1}^nx_{i} \right)}{n-1} \\
 & = \dfrac{\left( \sum_{i=1}^nx_{i}^2-\dfrac{\left( \sum_{i=1}^nx_{i} \right)^2}{n} \right)}{n-1} 
\end{align}
$$
### Population Variance and Population Standard Deviation
> The variability in the population is the **population variance** ($\sigma^2$). The positive square root of population variance is **population standard deviation** ($\sigma$). When population finite, the population variance is defined as $$
\sigma^2=\dfrac{\sum_{i=1}^N(x_{i}-\mu)^2}{N}
	$$
> where $\mu$ is the **population mean**. 
### Sample Range
> The **sample range** is defined as $$
r=\text{max}(x_{i})-\text{min}(x_{i})
$$
# Stem-and-Leaf Diagrams
A **stem-and-leaf diagram** allows us to create an informative visual display of a data set $x_{1}\dots x_{n}$ where each number consists of at least two digits.

### Steps to Construct a Stem-and-Leaf Diagram
1. Divide each number $x_i$ into two parts: a **stem**, consisting of one or more leading digits, and a **leaf**, consisting of the remaining digit.
2. List the stem values in a vertical column.
3. Record the leaf for each observation beside its stem.
4. Write the units for stems and leaves on the display.

### Median and Mode
The **sample median** is a measure of the "central tendency" that divides the data into two equal parts, half below the median and half above.
- If the number of observations are even, 