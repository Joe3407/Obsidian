## 📘Lec 1

- **Sample Space:** it's the set of all possible outcomes of an experiment 
- **Event:** it's a subset of a sample space
- **Complement:** all elements in sample space except its own event
- {${x|x<0}$ } = the set x where( | ) x is smaller than zero 
- **Sample Mean:** there sum over there number
- **Sample Median:** the middle term after sorting ascendingly, (if there number is even, then the median is the mean of the two center elements)
- **Rule Method:** $((x,y)|x^2+y^2<9;x \ge 0, y \ge 0)$ 

---
## 📘Lec 2

- **Multiplication(Product) Rule:** we use it when having independent choices 
- **Permutation:**  we use it in arranging or ordering items, and order matters ($ab \neq ba$)
     - **With Repetition:** $n^r$ (r=number of repetition)
     - **Without Repetition:** $nPr$ 
     - **Circular:**  $(n-1)!$ 
 - **Combination:** we use it in arranging or ordering items, but order doesn't matter ($ab = ba$)
 - **Multinomial Coefficient:** when choosing from groups having same elements 
     - **Example:** having two groups of 5 boys and 8 girls, we can arrange them in $\frac{\mathbf{13!}}{\mathbf{5! \, 8!}}$ different ways 

---
## 📘Lec 3

- $P(A) = \frac{n}{N}, \text{ where } n \text{ is the number of outcomes for event } A \text{ and } N \text{ is the total number of outcomes in the sample space}$
- **Intersection:**
     - **Disjoint:** $A \cap B=\emptyset$ → $P(A \cap B)=0$ 
     - **Independent:** $P(A \cap B)=P(A).p(B)$ 
     - **Dependent:** $P(A \cap B)=P(A).P(B|A)$ 
 - **Union:** $P(A \cup B)=P(A)+P(B)-P(A \cap B)$ 
 - **Rules:**
     - $P(A)+P(\overline{A})=1$
     - $P(\overline{A} \cap \overline{B})=P(\overline{A \cup B})=1-P(A \cup B)$
     - $P(A \cap \overline{B})=P(A)-P(A \cap B)$ 

---
## 📘Lec 4

- **Conditional Probability:** $P(B|A)=\frac{P(A \cap B)}{P(A)},(P(A) \neq 0)$ 
- **Note:** if $P(A|B) = P(A)$, or $P(B|A)=P(B)$, then A & B are independent 
- **Bayes' Rule:** Determine future probabilities using prior knowledge 
     - Making tree diagram having the event and the conditional probabilities 
     - calculating the intersection of each event 
     - taking the sum to know the probability of the defective itself
     - $P(A \cap B \cap C | D)=P(A|D)P(B|D)P(C|D)$ 

---
## 📘Lec 5

- **Random Variable:** It's a variable that represents the outcome of a trail 
- **Discrete Random Variable:** X=1,2,3,.... (it can be finite or infinite but not interval)
- **Continuous Random Variable:** 0<X<2 (it's an interval including all number in between)
- **Probability Distribution of Random Variable:** $f(x)$
     - **Probability Mass Function(p.m.f):** $f(x) \ge 0$, $\sum_{x} f(x)=1$, $p(X=x)=f(x)$ 
     - **Probability Density Function(p.d.f):** $f(x) \ge 0$, $\int_{x}f(x)dx=1$, $p(a<x<b)= \int_{a}^bf(x)dx$ 
 - Cumulative Distribution Function: $F(x)$ 
	 - Discrete: $F(x)=p(X \le x)=\sum_{X \le x}f(x)$ 
	 - Continuous: $F(x)=p(X \le x)= \int_{X \le x}f(t)dt$ 
- Note:
     - $\int_{-\infty}^{\infty}f(x)dx=1$ 
     - **Normalization:** We have to check if the sum or integration is equal 1, if not we divide f(x) to the value that isn't equal to one 

--- 
## 📘Lec 6

- **Mean of a Random Variable (x):** 
     - No=      9   7   4        20
     - Grade= 88 91 61
     - Average=$\frac{88 \times 9+91\times7+61\times4}{20}$ = $88 \times \frac{9}{20} +91 \times \frac{7}{20} +61 \times \frac{4}{20}$ 
     - **Conclusion:** that the Average or Mean or Expected Value = sum of product between x and its probability f(x)
     
     - **Discrete:** $\mu_x = E[x]= \sum_x xf(x)$
     -  **Continuous:** $\mu_x = E[x]= \int_x xf(x)dx$
 - **Mean of a Random Variable (g(x)):** 
     - **Discrete:** $\mu_{g(x)} = E[g(x)]= \sum_x g(x)f(x)$
     - **Continuous:** $\mu_{g(x)} = E[g(x)]= \int_x g(x)f(x)dx$ 
 - **Properties:** 
     - $a<x<b \to a<E[x]<b$
     - $E[a]=a$
     - $E[ax]=aE[x]$
     - $E[g(x)$$+\atop -$ $h(x)]=$$E[g(x)]$ $+\atop-$ $E[h(x)]$  
 - **Variance:** 
     - If we have 2 classes both have the same Expected value 80, this doesn't mean that all the individuals have the same grades, so to differentiate between them we use Variance, so it calculates the difference between each individual grade to the average grade to know if the deviation(distance) is big or small, if it's big then this means that the grades are far from the average, and if small then the grades around the average
     - **Why the power 2?:** the power is used instead of absolute to avoid negative numbers, and the power is much easier to calculate with in (integration, properties of Expected value, and doesn't have undefined values), also the power makes the number difference huge so it's much easier to read 
     - **Rule:**   
         - **Discrete:** $\sigma_x^2=var[x]=E[(x_i-\mu x)^2]=\sum_x(x-\mu_x)^2f(x)$
         - **Continuous:** $\sigma_x^2=var[x]=E[(x_i-\mu x)^2]=\int_x(x-\mu_x)^2f(x)dx$ 
         - **Final Rule:** $\sigma_x^2=var[x]=E[x^2]-E[x]^2$ 
         - **Note:** same rules if it's $var[g(x)]$, replace all x to g(x) except the f(x) it remains as it is 
 - **Standard Deviation:** 
     - $\sigma_x=SD[x]=\sqrt{\sigma_x^2}$ 
 - **Properties:**
     - $var[a]=0$
     - $var[ax]=a^2 var[x]$
     - $var[ax+b]=a^2var[x]$, (only if a, b are constants and that b doesn't have x)

--- 
## 📘Lec 7

- **Overview:** We use some distribution formulas to make it easier and faster to calculate the probability of some events with a general formula rather than taking time in doing the PMF for each event  
- **Bernoulli:**
     - **Bernoulli Trail:** success/fail, defective/not, pass/not
     - **Bernoulli Random Variable:** X={0, 1}
     - **Bernoulli Distribution:** $p \to x=1$ , $p-1 \to x=0$ 
     - $E[x]=p$
     - $var[x]=pq$ 
     - $\sigma = \sqrt{pq}$ 
     - **Bernoulli Process:** It's a sequence of Bernoulli Trails, for example (1 0 1 0 1 1),(DNNDD)
         - Have repeated trails
         - Each trail has two outcomes (0, 1)
         - Probability of success remains constant (it's not constant if we for example select without replacement)
         - Repeated trails are independent
 - **Binomial:** 
     - **Binomial Random Variable:** it counts the number of success in a Bernoulli Process (1 0 1 0 1 1 $\to$ 4),(DNNDD $\to$ 3), X $\in$ {0, 1, .., n}
         - Have repeated Bernoulli trails
         - Fixed number of trails (n)
         - Each trail has two outcomes (0, 1)
         - Probability of success remains constant 
         - Repeated trails are independent 
     - **Binomial Distribution:** 
         - $f(x)=p(X=x)=\binom{n}{x}p^xq^{n-x}$ 
         - $E[x]=np$
         - $var[x]=npq$
         - $\sigma_x=\sqrt{npq}$ 
         - **Note:** $p(X>4)=1-p(X \le 4)$ 
 - **Poisson:**
	 - **Usage:** It helps in binomial as if we have a huge n and very small p binomial will be very ugly as it will have huge powers and small numbers but Poisson helps here as it takes the average $\lambda =np$, and uses it in its equation, it's used to know the number of outcome during a given interval of time 
     - **Poisson Distribution:** $p(x)=p(X=x)=\frac{e^{-\lambda}\lambda^x}{x!}$, (when x is a non-negative integer) 
     - **Expectation & Variance:** $E[x]=var[x]=\lambda$ 
 - **Poisson Process:** 
     - **Properties:** 
         - **Events occur independently:** meaning that if an event happens it doesn't make another event more or less likely to happen, (like if a person goes to a shop then tells his friends how good it was so it's more likely that his friends will increase the number of people who will enter in the next hour)
         - **Constant $\lambda$:** meaning that in 1hour $\lambda$=5, in 2hours $\lambda$=10, (it's not a Poisson process if customers come at noon faster than midnight)
         - **No two events occur at the same moment:** meaning that 1 event can occur in 0.00001sec(which is rare), but 2 events are impossible to occur in this exact moment,(it's not Poisson process if we're talking about the messages sent on a group as 2 or more messages can be sent at an instant)
     - **Probability distribution of Poisson Process:**  $p(N(t)=x)=\frac{e^{-\lambda t}(\lambda t)^x}{x!}$ 
     -  **Expectation & Variance:** $E[N(t)]=var[N(t)]=\lambda t$ 
     - **Note:** N(t) it's an object that represents infinite random variables, meaning N(1), N(2), and so on, are all random variables but under the same object 

---
## 📘Lec 8

- Continuous Uniform Distribution: 
	- It's when all the probabilities in a range are equal 
	- from x=a to x=b, and the area of this range must equal 1, so the $height=\frac{area}{width}\to height=\frac{1}{b-a}$ 
	- $P(3 \le x \le 9)=\int_3^9\frac{1}{b-a}dx$, (where $[3,9]\in [a,b]$)
- Normal (Gaussian) Distribution: 
	- For Continuous Random Variables, has a bell shaped curve 
	- Depends on two Parameters:
		- Mean or Center ($\mu$)
		- Standard Deviation ($\sigma$) 
	- $N(x;\mu ,\sigma)=\frac{1}{\sigma \sqrt{2\pi}}e^{-\frac{1}{2} (\frac{x-\mu}{\sigma})^2}$ 
- Area Under the Curve:
	- $p(x_1<X<x_2)=\int_{x_1}^{x_2}\frac{1}{\sigma \sqrt{2\pi}}e^{-\frac{1}{2} (\frac{x-\mu}{\sigma})^2}dx$ 
	- But since the integration will be complicated so we will assume that the RV Z is equal RV X but the $\mu=0, \sigma=1$, and even then it's still complicated so a Z-Table will be given to get the values of integration 
- Z-Table: 
	- $p(Z<a)=directly \ form \ table$
	- $p(a<Z<b)=p(Z<b)-p(Z<a)$ 
	- $p(Z>a)=1-p(Z<a)$ 
	- $p(Z<-a)=p(Z>a)=1-p(Z<a)$ 
- General Formula:
	- If we have different values of $\mu, \sigma$ then it will be impossible to get the probability as we will then have infinite number of Tables and graphs, so we have a general rule 
	- $p(X<a)=p(Z<\frac{a-\mu}{\sigma})$, where($z=\frac{x-\mu}{\sigma}$)
	- Note: when getting the z value from the table and we find multiple approximations we take the closer one, and if there are multiple with the exact approximation we take the average 

---
## 📘Lec 9

- **Joint Distribution:**
	- **PMF:** 
		- $0 \le f(x,y) \le 1$  
		- $\sum_x \sum_y f(x,y)=1$ 
		- $p(X=x,Y=y)=f(x,y)$ 
	- **PDF:**
		- $f(x,y) \ge 0$ 
		- $\int_y \int_x f(x,y) dxdy=\int_x \int_y f(x,y) dydx=1$ 
		- $p[(x,y) \in A]=\int\int_Af(x,y)dxdy$ 
- **Marginal Distribution:**
	- **PMF:**
		- $g(x)=\sum_yf(x,y)$ 
		- $h(y)=\sum_xf(x,y)$ 
	- **PDF:**
		- $g(x)=\int_yf(x,y)dy$ 
		- $h(y)=\int_xf(x,y)dx$ 
- **Conditional Distribution:**
	- **PMF:**
		- $f(x|y)=p(X=x|Y=y)=\frac{f(x,y)}{h(y)}$ 
		- $f(y|x)=p(Y=y|X=x)=\frac{f(x,y)}{g(x)}$ 
		- **Notes:**
			- $p(X\le 1|Y=0)=p(X=0|Y=0)+p(X=1|Y=0)$ 
			- $p(X\le 1 | Y\ge 1)=p(A|B)=\frac{p(A \cap B)}{p(B)}=\frac{p(X\le 1,Y\ge 1)}{\sum_{Y\ge 1}h(y)}$  
	- **PDF:**
		- $f(x|y)=\frac{f(x,y)}{h(y)}$ 
		- $f(y|x)=\frac{f(x,y)}{g(x)}$ 
		- **Notes:**
			- $p(X=a,Y=b)=p(X=a,b<Y<c)=p(a<X<b,Y=c)=0$ 
			- $p(X=a|Y=b)=p(X=a|b<Y<c)=0$ 
			- $p(a<X<b|Y=c)=\frac{p(a<X<b,Y=c)}{p(Y=c)}=\frac{0}{0}$, undefined value, but we can solve it using the rule above of $f(x|y)=\frac{f(x,y)}{h(y)}$ 
			- $p(a<X<b|Y=c)=\int_a^bf(x|y)|_{y=c}dx$ 
			- $p(a\le X\le b | c\le Y\le d)=p(A|B)=\frac{p(A \cap B)}{p(B)}=\frac{p(a\le X\le b,c\le Y\le d)}{p(c\le Y\le d)}=\frac{\int_c^d\int_a^bf(x,y)dxdy}{\int_c^dh(y)dy}$  
- **Statistical Independence:** 
	- $f(x|y)=g(x)$
	- $f(y|x)=h(y)$
	- $f(x,y)=g(x)h(y)$, for all values of x & y within the interval 
	- $p(a<X<b,c<Y<d)=p(a<X<b)p(c<Y<d)=\int_a^bg(x)dx\int_c^dh(y)dy$ 
	- $p(a<X<b|c<Y<d)=p(a<X<b)$ 

---
## 📝Final Notes

- Expected and Variance of binomial Distribution $\to np,\ npq$, respectively 
- $p(X=a)=0, Continuous$ 
- $p(X>k)=a \to p(X<k)=1-a$ 

- Events that cannot happen in the same time are called Mutually Exclusive  

- Verify the second condition of the definition of the joint probability $\to \int_y \int_x f(x,y) dxdy=\int_x \int_y f(x,y) dydx=1$ 

- $p(|X|>a)=p(X>a)+p(X<-a)$ 
- $p(|X|<a)=p(-a<X<a)$ 
