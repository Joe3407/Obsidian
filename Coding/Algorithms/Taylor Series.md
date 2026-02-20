
## Overview

- **Taylor Series** simplifies complex functions such as $sin,\ cos,\ etc...$ into polynomial functions that are easier to handle
- **Taylor Series** matches the function and all its derivatives at $x=a$
- Calculates high accuracy near $a$
- Accuracy decreases as we move further from $a$, with respect to **radius of convergence** $R$ 
- **Graphically** it takes the shape of the complex function slowly as we increase the number of terms
- If the function is **Analytic**, the Taylor Series is exactly equal to the function for all $x$ within its **radius of convergence** $R$ 
- In general we want to prove that $T^{(n)}(a)=f^{(n)}(a)$, for all $n \ge 0$ 
<img src="attachments/Screenshot_4.png" style="display:block; margin:auto;" width="400"/> 

---
## Equation 

$$T(x)=\sum_{n=0}^{\infty}\frac{f^{(n)}(a)}{n!}(x-a)^n$$
- **Why $(x-a)^n$ ?:**
	- **$(x-a)$:** 
		- We're computing the distance from $a$, so by doing $(x-a)$, we see how far are we from $a$ 
	- **The power $n$:**
		- Plays a very important role as it gets the value of the derivative of this power
		- Meaning that the Summation is divided into three parts: $(let\ k\ the\ number\ of\ derivative)$ 
			- Before $k\to$ All derivatives are $zero$ 
			- At $k\to$ $T^{(k)}(x)=f^{(k)}(x)$ 
			- After $k\to$ $(x-a)^{n-k}$ so by substituting $x=a$, all values will be equal $zero$ 
		- In general the power is like a **knob**, where each power represents its own derivative 
- **Why Summation Notation ?:**
	- After having the value of each derivative alone so by summing them we get the final value 
- **Why divide by $n!$ ?:**
	- As we want $T^{(n)}(a)=f^{(n)}(a)$ so by differentiating $(x-a)^n$ gives $n!$, so the coefficient must be divided by $n!$ to ensure $T^{(n)}(a) = f^{(n)}(a)$ exactly
- **Note:**
	- $T^{(n)}(a)=f^{(n)}(a)$
	- $T^{(n)}(x)=f^{(n)}(a)+\sum_{k=n+1}^{\infty}\frac{f^(k)(a)}{(k-n)!}(x-a)^{k-n}$ 

---
## Condition 

- 