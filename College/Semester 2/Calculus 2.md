## 📘Lec 1 

- **Exponential Function:**
	- $f(x)=b^x \ where \ b>0,\ b\ne 1$ 
		- Domain $\to R$ 
		- Range $\to [0,\infty]$ 
		- Growth $\to b>1$ 
		- Decay $\to 0<b<1$ 
	- $f(x)=e^x$ (Natural Exponential function)
		- $f(x)$ between $2^x \ and\ 3^x$ 
		- $2<e<3$ 
- **Logarithmic Function:**
	- $f(x)=log_bx\ where\ b>0,\ b\ne 1$ 
		- Domain $\to$ Range of Exponential function $\to$ $[0,\infty]$ 
		- Range $\to$ Domain of Exponential function $\to$ $R$ 
		- Growth $\to b>1$ 
		- Decay $\to 0<b<1$ 
	- **Inverse Properties:**
		- $b^{log_bx}=x, \ e^{lnx}=x$ 
		- $log_bb^x=x,\ ln(e^x)=x$ 
	- **Rules:**
		- $log_b(xy)=log_bx+log_by$
		- $log_b(\frac{x}{y})=log_bx-log_by$
		- $log_b(x^y)=ylog_bx$
		- $log_bb=1,\ log_b1=0$ 
- **Change Bases:**
	- $b^x=c^{log_c(b^x)}=c^{xlog_cb}$ 
	- $log_bx=\frac{log_cx}{log_cb}$ 
- **Derivative Rules:**
	- $\frac{d}{dx}ln|f(x)|=\frac{f'(x)}{f(x)}$
	- $\frac{d}{dx}log_b|f(x)|=\frac{f'(x)}{f(x)lnb}$ 
	- $\frac{d}{dx}b^{f(x)}=b^{f(x)}.lnb.f'(x)$ 
---
## 📘Lec 2

- $\frac{d}{dx}[sin^{-1}(f(x))]=\frac{f'(x)}{\sqrt{1-(f(x))^2}}$ 
- $\frac{d}{dx}[cos^{-1}(f(x))]=-\frac{f'(x)}{\sqrt{1-(f(x))^2}}$ 
- $\frac{d}{dx}[tan^{-1}(f(x))]=\frac{f'(x)}{1+(f(x))^2}$ 
- $\frac{d}{dx}[cot^{-1}(f(x))]=-\frac{f'(x)}{1+(f(x))^2}$ 
- $\frac{d}{dx}[sec^{-1}(f(x))]=\frac{f'(x)}{|f(x)|\sqrt{(f(x))^2-1)}}$  
- $\frac{d}{dx}[csc^{-1}(f(x))]=-\frac{f'(x)}{|f(x)|\sqrt{(f(x))^2-1)}}$  

---
## 📘Lec 3

- **Riemann Sum:**
	- **Steps:**
		- Divide the interval into $n$ subintervals of equal length 
		- Get the length of base of each subinterval,  $\Delta x=\frac{b-a}{n}$ 
		- Determine value inside each rectangle to calculate its height, it could be Left, Right, or Mid point,  $x_k^*$ 
		- Calculate the area of each rectangle,  $(Area=base*height) \to (Area=f(x_k^*)\Delta x)$ 
		- Sum all the Areas of Rectangles,  $\sum_{k=1}^nf(x_k^*)\Delta x$
	- **Rules:**
		- Right $\to x_k=a+k\Delta x$ 
		- Left $\to x_k=a+(k-1)\Delta x$
		- Mid $\to (x_k=a+(k-1)\Delta x + \frac{1}{2}\Delta x)  \to (x_k=a+(k-\frac{1}{2})\Delta x)$ 
		- $\sum_{k=1}^nk=\frac{n(n+1)}{2}$ 
		- $\sum_{k=1}^nk^2=\frac{n(n+1)(2n+1)}{6}$ 
		- $\sum_{k=1}^nk^3=\frac{n^2(n+1)^2}{4}$ 
	- **Graph:** 
		- **Increasing:**
			- **Right** $\to$ Overestimate 
			- **Left**   $\to$ Underestimate 
		- **Decreasing:**
			- **Right** $\to$ Underestimate
			- **Left**   $\to$ Overestimate 
		- **Note:**
			- **Mid** $\to$ Best Estimation 
	- **Note:**
		- $n\uparrow\ \to Accuracy\uparrow$,  where $n$ tends to Infinity
		- $\Delta x\downarrow \ \to Accuracy \uparrow$, where $\Delta x$ tends to Zero
	- **Net Area:**
		- When getting the Area of negative parts using Riemann Sum, then the area becomes negative, which means when getting the area of a graph that has positive and negative parts, the Area is the Net Area or Definite Integral, and not the actual area 
		- **Net Area = Definite Integral = Riemann Sum** 
		- $Net\ Area = \int_a^bf(x)dx=lim_{n\to \infty}\sum_{k=1}^nf(x_k^*)\Delta x$ 
	- **Definite Integral:**
		- It's the integration that has definite range $[a,b]$ 
		- $\int_a^b|f(x)|dx \to$ gives the total area of the whole graph, where the negative part is considered positive 

--- 
## 📘Lec 4

- **Area function:**
	- We can use it as a general equation that gets the net area from a fixed point $a$ to any other point $x$ in one step instead of doing every time integration 
	- $A(x)=\int_a^xf(t)dt$ 
	- **The Relation between $A(x)$ and $f(t)$ (Fundamental Theorem of Calculus):** 
		- **Part one:** $A'(x)=f(x)$       $(\frac{d}{dx}A(x)=\frac{d}{dx}\int_a^xf(t)dt) \to (A'(x)=\frac{d}{dx} (\int f(x) -\int f(a))) \to (A'(x)=f(x))$ 
		- **Part two:** $\int_a^bf(t)dt=A(b)-A(a)= \int_s^bf(t)dt-\int_s^af(t)dt$, (where s is constant) 
	- **Rules:**
		- $\int_a^x\frac{d}{dt}f(t)dt=f(x)$ 
		- $\int_a^b\frac{d}{dt}f(t)dt=f(b)-f(a)$  
		- $\frac{d}{dx}\int_{h(x)}^{g(x)}f(t)dt=(\frac{d}{dx}[A(g(x))-A(h(x))]) = (\frac{d}{dx}A(g(x))-\frac{d}{dx}A(h(x))) = (f(g(x))g'(x)-f(h(x))h'(x))$,   (where $\frac{d}{dx}A(x)= f(x)$, Fundamental Theorem of Calculus) 
- **Notes:**
	- **Even:**  $\int_{-a}^af(x)dx=2\int_0^af(x)dx$,  like $cos(x)$
	- **odd:**  $\int_{-a}^af(x)dx=0$ ,    like $sin(x)$ 
	- **Antiderivative:** $x^2$ is an antiderivative of $2x$, and $2$ is the derivative of $2x$,  so in conclusion antiderivative is the inverse of derivative 
- **Average Value of Function:**
	- If we have an interval $[a,b]$ and we take the average at point $c$ then  $\overline{f}=f(c)$, so if we wanted area under the graph from $a\to b$ so we can get the area of the rectangle which is base * height which is $(b-a)*\overline{f}$, which is the same as the Integration from $a$ to $b$, as the extra parts will cancel each other 
	- $\overline{f}=f(c)=\frac{1}{b-a}\int_a^bf(x)dx$ 

---
## 📘Lec 5

- **Basic Integration:**
	- **Basic:**
		- $\int kdx=kx+c$ 
		- $\int x^ndx=\frac{x^{n+1}}{n+1}+c$, $n\ne -1$ 
		- $\int e^{ax}dx=\frac{1}{a}e^{ax} +c$ 
		- $\int f'(x)e^{f(x)}dx=e^{f(x)}+c$ 
		- $\int a^{kx}dx=\frac{1}{klna}a^{kx}+c$ 
		- $\int f'(x)a^{f(x)}dx=\frac{1}{lna}a^{f(x)}+c$  
		- $\int \frac{(ax+b)^{p-1}}{(ax+b)^p}dx=\frac{ln|ax+b|}{a} +c$ 
	- **Trig:**
		- $\int cosxdx=sinx+c$
		- $\int f'(x)cos(f(x))dx=sin(f(x))+c$ 
		- $\int sinxdx=-cosx+c$
		- $\int f'(x)sin(f(x))dx=-cos(f(x))+c$  
		- $\int sec^2xdx=tanx +c$ 
		- $\int f'(x)sec^2(f(x))dx=tan(f(x))+c$ 
		- $\int csc^2xdx=-cotx +c$ 
		- $\int f'(x)csc^2(f(x))dx=-cot(f(x))+c$ 
		- $\int secxtanxdx=secx+c$ 
		- $\int f'(x)sec(f(x))tan(f(x))dx=sec(f(x))+c$ 
		- $\int cscxcotxdx=-cscx+c$ 
		- $\int f'(x)csc(f(x))cot(f(x))dx=-csc(f(x))+c$ 
	- **Inverse:**
		- $\int \frac{f'(x)}{\sqrt{a^2-(f(x))^2}}dx=sin^{-1}(\frac{f(x)}{a})+c$  
		- $\int \frac{f'(x)}{a^2+(f(x))^2}dx=\frac{1}{a}tan^{-1}(\frac{f(x)}{a})+c$ 
		- $\int \frac{f'(x)}{|f(x)|\sqrt{(f(x))^2-a^2}}dx=sec^{-1}(\frac{|f(x)|}{a})+c$  
- **Substitution Rule:**
	- **Indefinite Integral:** 
		- $u=g(x)$
		- $du=g'(x)dx$ 
		- **Rules:**
			- $\int tan(ax)dx=\frac{1}{a}ln|sec(ax)|+c$ 
			- $\int cot(ax)dx=\frac{1}{a}ln|sin(ax)|+c$  
			- $\int sec(ax)dx=\frac{1}{a}ln|sec(ax)+tan(ax)|+c$  
			- $\int csc(ax)dx=\frac{-1}{a}ln|csc(ax)+cot(ax)|+c$  
			- $\int cos^2(x)dx=\frac{1}{2}[x+\frac{1}{2}sin(2x)]+c$ 
			- $\int sin^2(x)dx=\frac{1}{2}[x-\frac{1}{2}sin(2x)]+c$ 
	- **Definite Integral:** 
		- $u=g(x)$
		- $du=g'(x)dx$ 
		- $u_{lower}=g(a)$
		- $u_{upper}=g(b)$ 
		- $\int_{u_{lower}}^{u_{upper}}f(u)du$ 
- **Notes:**
	- $sin(A)cos(B)=\frac{1}{2}[sin(A+B)+sin(A-B)]$ 

---
## 📘Lec 6

- **Integration by Part:**
	-  **Indefinite Integral:**
		- $u$          , $dv$
		- $du$         , $v$ 
		- $uv-\int vdu$ 
	- **Definite Integral:**
		- - $u$          , $dv$
		- $du$         , $\int_a^bv$  
		- $uv|_a^b-\int_a^b vdu$  
- **Complete the Square:** 
	- Rewriting a quadratic expression in the form $(x+h)^2+k$, to simplify integrals to the standard form of inverse trigonometric 
	- **Note:** Take half of the coefficient of $x$ and let it be $a$,  then it will be $(x+a)^2-a^2$ 
- **Integrating Rational Functions:** 
	- If the degree of the numerator greater than the degree of denominator, then we do long division
	- After long division, we integrate the number resulted at the top plus the reminder from the bottom divided the denominator,  $\int top+\frac{bottom}{denominator}dx$ 

--- 
## 📘Lec 7

- **Partial Fractions:**
	- When the denominator degree is greater than the numerator degree, then we can break it to multiple fractions which are easier to integrate 
	- $\int \frac{3x}{x^2+2x-8}dx \to \int \frac{1}{x-2} \frac{2}{x+4}dx$ 
	- **Steps:**
		- Factorizing denominator                        $\frac{3x}{(x-2)(x+4)}$ 
		- Partial fraction decomposition                $\frac{3x}{(x-2)(x+4)}= \frac{A}{x-2}+\frac{B}{x+4}$  
		- Multiply both sides with denominator    $3x=A(x+4)+B(x-2)$ 
		- Equate like powers of x                            $3x=(A+B)x+(-2A+4B)$ 
	- **Partial Fractions with repetition:**
		- **linear:**
			- $(x-r)^m \to \frac{A_1}{(x-r)^1}+\frac{A_2}{(x-r)^2}+...+\frac{A_m}{(x-r)^m}$ 
		- **Quadratic:**
			- $(ax^2+bx+c)^m \to \frac{A_1x+B}{(ax^2+bx+c)^1}+\frac{A_2x+B}{(ax^2+bx+c)^2}+...+\frac{A_mx+B}{(ax^2+bx+c)^m}$ 
- **Improper Integrals:**
	- **Infinite:**
		- $\int_a^{\infty}f(x)dx\to lim_{b\to \infty}\int_a^bf(x)dx$ 
		- $\int_{-\infty}^bf(x)dx\to lim_{a\to -\infty}\int_a^bf(x)dx$  
		- $\int_{-\infty}^{\infty}f(x)dx \to lim_{a\to -\infty}\int_a^cf(x)dx+lim_{b\to \infty}\int_c^bf(x)dx$ 
	- **Unbounded Integrals:**
		- $(a,b] \to \int_a^bf(x)dx=lim_{c\to a^+}\int_c^bf(x)dx$ 
		- $[a,b) \to \int_a^bf(x)dx=lim_{c\to b^-}\int_a^cf(x)dx$ 
		- $[a,b]\ except\ p \to \int_a^bf(x)dx=lim_{c\to p^-}\int_a^cf(x)dx+lim_{d\to p^+}\int_d^bf(x)dx$ 
	- **Note:**
		- If limit exists, then the improper integrals **converge** 
		- If limit DNE, then the improper integrals **diverge** 

--- 
## 📘Lec 8

- **Integrating Powers of $sin x$ or $cos x$:**
	- **Odd Power:**
		- $(\int cos^nxdx)\to (\int cos^{n-1}xcosxdx)\to (\int (cos^2x)^{\frac{n-1}{2}}cosxdx) \to (\int (1-sin^2x)^{\frac{n-1}{2}}cosxdx)$ 
		- $(\int sin^nxdx)\to (\int sin^{n-1}xsinxdx)\to (\int (sin^2x)^{\frac{n-1}{2}}sinxdx) \to (\int (1-cos^2x)^{\frac{n-1}{2}}sinxdx)$ 
	- **Even Power:**
		- $(\int cos^nxdx)\to (\int (cos^2x)^{\frac{n}{2}}dx) \to (\int (\frac{1+cos2x}{2})^{\frac{n}{2}}dx)$ 
	- **What if the power is $n>2 \to$ we use Integration by part:**
		- $\int cos^nxdx=\frac{1}{n}[cos^{n-1}x.sinx+(n-1)I_{n-2}]+C$ 
		- $\int sin^nxdx=\frac{1}{n}[-sin^{n-1}x.cosx+(n-1)I_{n-2}]+C$ 
- **Integrating Products of Powers of $sin x$ and $cos x$:**
	- **Power of $sinx$ is odd:**
		- $(\int sin^mxcos^nxdx)\to (\int (1-cos^2x)^{\frac{m-1}{2}}cos^nxsinx)dx$ 
	- **Power of $cosx$ is odd:**
		- $(\int sin^mxcos^nxdx)\to (\int sin^mx (1-sin^2x)^{\frac{n-1}{2}}cosx)dx$ 
	- **Power of $sinx$ & $cosx$ are even:**
		- $sin^mx=(\frac{1-cos2x}{2})^{\frac{m-1}{2}}$,     $cos^nx=(\frac{1+cos2x}{2})^{\frac{n-1}{2}}$ 
- **Integration of power of $tanx$ and power of $secx$:** 
	- **Main Rule:** $tan^2x=sec^2x-1$ 
	- **Integrating $tanx$ with odd power:** $tan^nx=(sec^2x-1)^{\frac{n-1}{2}}tanx$ 
	- **Integrating $tanx$ with even power:** $tan^nx=(sec^2x-1)tan^{n-2}x$  
	- **Integrating Products of Powers of $tanx$ and $secx$:** 
		- **Power of $secx$ is even:** $sec^nx=(1+tan^2x)sec^{n-2}x$ 
		- **Power of $tanx$ is odd:** $tan^mx=tan^{m-1}xtanx$ 
- **Integrating products of $sinx$ & $cosx$ with different angles:**
	- $\sin(mx)\sin(nx) = \frac{1}{2}\left[\cos((m-n)x) - \cos((m+n)x)\right]$ 
	- $\cos(mx)\cos(nx) = \frac{1}{2}\left[\cos((m-n)x) + \cos((m+n)x)\right]$ 
	- $\sin(mx)\cos(nx) = \frac{1}{2}\left[\sin((m-n)x) + \sin((m+n)x)\right]$ 

---
## 📘Lec 9

- **Trigonometric Substitution:**
	- $\sqrt{a^2-x^2}  \to x=asin(\theta)$ 
	- $\sqrt{a^2+x^2}\to x=atan(\theta)$ 
	- $\sqrt{x^2-a^2}\to x=asec(\theta)$ 
- **Length of Curve:**
	- $\int_a^b\sqrt{1+(f'(x))^2}dx$ 

---
## 📘Lec 10

- **Area Between Two Curves:**
	- **Integration with respect with $x$:**
		- **Riemann Sum:** $A=lim_{n\to \infty }\sum_{k=1}^n(f(x_k^*)-g(x_k^*))\Delta x$ 
		- **Rule:** $A=\int_a^b(f(x)-g(x))dx$,   where $f(x)>g(x)$ 
	- **Integration with respect with $y$:**
		- **Riemann Sum:** $A=lim_{n\to \infty }\sum_{k=1}^n(f(y_k^*)-g(y_k^*))\Delta y$ 
		- **Rule:** $A=\int_c^d(f(y)-g(y))dy$,   where $f(y)>g(y)$ 
	- **Note:**
		- **How to know the top function:**
			- Equalize both functions
			- Get the $x$ values 
			- Determine its ranges, meaning  from $x_1\to x_2$ 
			- Substitute at any number in the range in both functions
			- The greater function is top

---
## 📝Exam Notes

- $tanx \to [-\frac{\pi}{2},\frac{\pi}{2}]$, therefore $tan^{-1}x$ is defined at $[-\frac{\pi}{2},\frac{\pi}{2}]$ 
- $cotx \to [0,\pi]$, therefore $cot^{-1}x$ is defined at $[0,\pi]$ 
- $sinx\to [-\frac{\pi}{2},\frac{\pi}{2}]$, therefore $sin^{-1}x$ is defined at $[-\frac{\pi}{2},\frac{\pi}{2}]$ 
- $cosx \to [0,\pi]$, therefore $cos^{-1}x$ is defined at $[0,\pi]$ 
- $secx\to [0,\pi ]$ \ {$\frac{\pi}{2}$}, therefore $sec^{-1}x$ is defined at $[0,\pi ]$ \ {$\frac{\pi}{2}$}
- $cscx \to [-\frac{\pi}{2},0) \cup (0,\frac{\pi}{2}]$, therefore $csc^{-1}x$ is defined at $[-\frac{\pi}{2},0) \cup (0,\frac{\pi}{2}]$ 
- Length of curve:  $\int_a^b\sqrt{1+(f'(x))^2}dx$ 
- $\int secx dx\to$ multiply by $\frac{secx+tanx}{secx+tanx}$,  $\int cscx dx\to$ multiply by $\frac{cscx+cotx}{cscx+cotx}$ 
- $\int lnxdx\to$  Integration by part
- $\sin(mx)\sin(nx) = \frac{1}{2}\left[\cos((m-n)x) - \cos((m+n)x)\right]$ 
- $\cos(mx)\cos(nx) = \frac{1}{2}\left[\cos((m-n)x) + \cos((m+n)x)\right]$ 
- $\sin(mx)\cos(nx) = \frac{1}{2}\left[\sin((m-n)x) + \sin((m+n)x)\right]$ 
- $\int sec^3xdx\to$ $u=secx$   $dv=sec^2xdx$ 
- $a^{lnx}=x^{lna}$ 
