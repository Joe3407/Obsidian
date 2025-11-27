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
         - **Note:** $p(X>4)=1-p(x \le 4)$
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
     - **Note:** N(t) it's an object that represents infinite random variables, meaning N(1),N(2), and so on are all random variables but under the same object 
