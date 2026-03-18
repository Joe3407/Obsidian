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
		- $log_b=1,\ log_b1=0$ 
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

