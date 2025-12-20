## 📘Lec 1

- **∀ (For each / For all):** `∀x ∈ {1,2,3}, x < 5` → Every number in {1,2,3} is less than 5 → **True**  
- **∃ (There exists):** `∃x ∈ {1,2,3} such that x > 2` → There is at least one number greater than 2 → **True (x = 3)**

- **Domain:** all x-values for which f(x) is defined (avoid division by 0, square roots of negatives, etc.) 
- **Range:** all y-values that f(x) can produce → solve y = f(x) for x to find valid y (the domain of the inverse function is the range of the function with respect to the values of the original function)

---
## 📘Lec 2

- Function tends to go towards y-axis by increasing the power, tends to go towards x-axis by increasing the fraction value in root function 
- $y=f(x)+d$, the function is shifted vertically by changing the value d 
- $y=f(x-b)$, the function is shifted horizontally by changing the value of b (if b is positive then it shifts in the positive direction)
- $y=cf(x)$, the function gets wider when c decreases 
- $f \circ g(x)$ → Domain is $f(g(x)) \cap g(x)$ 

---
## 📘Lec 3

- $sin(\alpha + \beta)=sin(\alpha)cos(\beta)+sin(\beta)cos(\alpha)$
- $cos(\alpha + \beta)=cos(\alpha)cos(\beta)-sin(\beta)sin(\alpha)$  
- **Unit Circle:** 
     - $0^\circ$ → $(1, 0)$ 
     - $30^\circ$ → $(\frac{\sqrt{3}}{2}, \frac{1}{2})$ 
     - $45^\circ$ → $(\frac{\sqrt{2}}{2}, \frac{\sqrt{2}}{2})$  
     - $60^\circ$ → $(\frac{1}{2},\frac{\sqrt{3}}{2} )$ 
     -  $90^\circ$ → $(0, 1)$ 
 - **One to One:** $f(A)==f(B)$ 
 - **Inverse:** get the "x equal" and just change the x and y, and then this y is the inverse function
 - $sin(A)=cos(B) → A+B=90^\circ$ 
 - $f(f^{-1}(x))=f^{-1}(f(x))=x$ 

--- 
## 📘Lec 4

- **Limits Operations:**
     - $lim_{x \to a}(f(x)+g(x))=lim_{x \to a}f(x)+lim_{x \to a}g(x)$, (works for `+`, `−`, `×`, `÷`)
     - $lim_{x \to a}cf(x)=c lim_{x \to a}f(x)$ 
     - $lim_{x \to a}f(x)^n =(lim_{x \to a}f(x))^n$, (n is positive, works with root when n is positive)
     - $lim_{x \to a}c =c$ 
     - $lim_{x \to a}x=a$ 
 - **Determined Values:** $\infty+\infty=\infty, -\infty-\infty=-\infty, 0^\infty=0, 0^{-\infty}=\infty(as \frac{1}{0}=\infty), \infty *\infty=\infty$  
 - **Squeeze Theorem:** $f(x) \le g(x) \le h(x), lim_{x \to a}f(x)=lim_{x \to a}h(x)=L$, then $lim_{x\to a}g(x)=L$ 
 - **One-Sided Limits:** The limit when x tends to a only exists when limit of $f(a^-)=f(a^+)$ 
 - **Trigonometric:** $lim_{x \to a}\frac{sin(ax)}{bx}=\frac{a}{b}$, (this rule came from squeeze theorem), $lim_{x\to a}\frac{1-cos(x)}{x}=0$, (it came from multiplying by the conjugate)
 - **Oscillating Behavior:** $lim_{x \to 0}sin(\frac{1}{x}) = DNE$, (as the limit approach 0 it starts to oscillate crazy between -1 & 1), but $lim_{x \to 0}xsin(\frac{1}{x}) = 0$, (from squeeze theorem)
 - **Unbounded Behavior:** $lim_{x \to 0}\frac{1}{x^2} = \infty$, (as we get closer to 0 y increases without bounds so its value is infinity)
 - Asymptotes:
     - Vertical Asymptote:
         - at x=a $\to$ $den=0, num\ne 0$ (don't simplify the function to avoid mistakes)
         - Check limit when x tends to a from +ve and -ve, if any of them is +ve or -ve infinity 
     - Horizontal Asymptote:
         - take the limit of the function when x tends to +ve and -ve infinity, and all the values that come is a HA, except if the value is +ve or -ve infinity 
 - **Note:** 
     - $f(x)=undefined$, but $lim_{x \to a}f(x)=DNE$
     - $\frac{1}{0^+}=\infty$, $\frac{1}{0^-}=-\infty$  

---
## 📘Lec 5

- **Limits at infinity:** 
     - $lim_{x \to \infty}x=\infty$ 
     - $lim_{x\to \infty}\frac{1}{x}=0$, (x=10 → 0.1, x=100 → 0.01, x=$\infty$ → 0)
 - **Rules:**
     - **Bottom heavy:** the degree of denominator is higher → always equals zero
     - **Equal:** the degree of denominator & numerator are equal → coefficient of num/den  
     - **Top heavy:** the degree of numerator is higher → divide all numbers with highest degree of bottom 
 - **Function is Continuous:** function is defined, limit of function exists, both function and limit at x are equal 
 - **Intermediate Value Theorem:** given f(x) where it's continuous in $[a,b]$, and $f(a) \le N \le f(b)$, there exists c where f(c)=N
 - **Continuity at End Points:** It's to check weather the interval will include the end point or not, so when we have ($-\infty , 3$) we see if $lim_{x\to 3^-}f(x)=f(3)$, if equal then we include it in the interval, and it becomes ($-\infty , 3$ ]

---
## 📘Lec 6

- $V_{av}=\frac{s(t)-s(a)}{t-a}$, $V_{inst}=lim_{t\to a}\frac{s(t)-s(a)}{t-a}$ 
- $\frac{dx}{dy}=lim_{h\to 0}\frac{f(x+h)-f(x)}{h}$ 
- If f is differentiable at a, then it's continuous on a, but not vice versa  
- **Differentiable:** f at a is continuous, f at a doesn't have a corner, f at a isn't a vertical tangent

--- 
## 📘Lec 7

- **Chain Rule:** $F(x)=f(g(x))$, $F'(x)=f'(g(x))g'(x)$ 
- **Implicit:** $x^2+2y=1$
- **Explicit:** $y=\frac{1}{2} (1-x^2)$ 

---
## 📘Lec 8

- Absolute Extreme Values $\to$ Abs. Max, Abs. Mini 
- Absolute = Global
- **Critical Point:** 
     - $f'(x)=0$
     - $f'(x)= DNE$, (corner, vertical line)
 - **Absolute Extreme Values:**
     - Find Critical Points
     - Find the value of $f(x)$, for $x=C.P, a, b$ 
 - **Local Values:**
     - Test the values before and after each C.P 
     - $inc, dec \to local\max$ 
     - $dec, inc \to local \min$ 
 - **Inflection Point:**
     - $f''(x)=0$
     - $f''(x)=DNE$
     - Before and after this point $\to concave\ up\ concave\ down\ or\ concave\ down\ concave\ up$ 
 - **Mean Value Theorem:**
     - $f\ is\ continuous\ on\ [a,b]$
     - $f\ is\ differentiable \ on (a,b)$ 
     - then there exists at least one point c where $f'(c)=\frac{f(b)-f(a)}{b-a}$ 
 - **Notes:** 
     - $f''(x)>0 \to local\ min\ and \ concave up$  
     - $f''(x)<0 \to local \ max\ and\ concave down$   
     - If $f''(x)=0 \to$ The second derivative failed and we must use first derivative 

---
## 📘Lec 9

- Symmetric:
     - Graphs: 
         - About y-axis $\to (x,y) \to (-x,y)$ 
         - About x-axis $\to$ $(x, y) \to (x, -y)$ 
         - About origin $\to (x,y) \to (-x,-y)$ 
     - Functions:
         - Even $\to f(-x)=f(x) \to$ about y-axis
         - Odd $\to f(-x)=-f(x)\to$ about x-axis
         - Neither $\to$ No symmetry 
 - Graphing Steps:
     - Identify Domain
     - Exploit Symmetry
     - Find First and Second derivatives
     - Find C.P & I.P
     - Determine Inc., Dec. & Concavity 
     - Classify Extreme Values (Absolute)
     - Locate Asymptote and behavior 
     - Find x and y intercepts 
 - Slant Asymptote:
     - Bottom Heavy $\to$ Vertical Asymptote at y=0, No Slant Asymptote 
     - equal $\to$ Vertical Asymptote at y=coefficient, No Slant Asymptote 
     - Top Heavy $\to$ No Vertical Asymptote, Slant Asymptote = Long division 
     - Long Division: 
	     - Divide
	     - Multiply
	     - Subtract
	     - Down
	 - Note: When doing long division we stop when the reminder power is less than the power of denominator or if reminder is equal zero 
- L'Hopital's Rule: 
	- $\frac{0}{0} \ or \ \frac{\infty}{\infty} \to$ $lim_{x\to a}\frac{f(x)}{g(x)}= lim_{x\to a}\frac{f'(x)}{g'(x)}$, (where a could be $\infty, \ a^+, \ a^-$)
	- $0.\infty \ or\ \infty - \infty \to$ We try to rewrite them in the $\frac{0}{0} \ or \ \frac{\infty}{\infty}$ form if we cannot then L'Hopital's Rule isn't the right way for this problem 