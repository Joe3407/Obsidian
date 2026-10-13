## 📘Lec 1

- **Terminologies:**
	- **Radix:** It's the base of the number system, e.g. decimal $\to$ base 10, binary $\to$ base 2 
	- **Digit Position:** Left of the dot positive, right of the dot negative 
	- **Digit Weight:** $Base^{Position}$ 
	- **Magnitude:** The sum of $Digit\ Value*Weight$ 
	- **Notes:**
		- $2^{10}\to$ K (kilo)
		- $2^{20}\to$ M (Mega)
		- $2^{30}\to$ G (Giga)
		- $2^{40}\to$ T (Tera)
- **Conversions:**
	- **Decimal to Any Base:**
		- **Integer:** Divide Base 
		- **Fraction:** Multiply 
	- **Any Base to Decimal:** 
		- **Integer Part:** Get the magnitude while the powers increase from $0 \to \infty$  
		- **Fraction Part:** Get the magnitude while the powers decrease from $-1 \to -\infty$ 
	- **Note:**
		- Every 4 bits is equivalent to one Hexadecimal digit 
		- Every 3 bits is equivalent to one Octal digit 

---
## 📘Lec 2

- **Arithmetic Operations:**
	- **Addition:** If sum is more than the base, then we carry 1 to the next digits, and leave the reminder as the result of the current digit 
	- **Subtraction:** If first digit is smaller than the second digit, then we take base from the bigger digit, meaning decrease 1 from tens digits and increase base with the units digit 
- **Complements:**
	- **Diminished Radix Complement (r-1)’s Complement:**
		- **1's Complement:** 
			- All digits are toggled, and by adding the number to its 1's complement we get all the digits as ones
			- **Subtraction M-N is done By:**
				- Get 1’s Complement of N
				- Add M + N
				- If carry then Add carry to summation
				- If no carry then result = - 1’s complement of result
	- **Radix Complement r's complement:**
		- **2's Complement:**
			- Take 1’s complement then add 1, OR Toggle all bits to the left of the first ‘1’ from the right
			- **Subtraction M-N is done By:**
				- Get 2’s Complement of N
				- Add M + N
				- If carry then discard carry
				- If no carry then result = - 2’s complement of result
- **Rules:**
	- **Distributive:**
		- $x.(y+z)=(x.y)+(x.z)$ 
		- $x+(y.z)=(x+y).(x+z)$
	- **DeMorgan's Theorem:**
		- $(x+y)'=x'.y'$
		- $(x.y)'=x'+y'$
	- **Absorption:**
		- $x+(x.y)=x$
		- $x.(x+y)=x$ 
	- **Consensus Theorem:**
		- $xy+x'z+yz=xy+x'z$ 
		- $(x+y).(x'+z).(y+z)=(x+y).(x'+z)$ 
- **Precedence:**
	- Parentheses $\to$ NOT $\to$ AND $\to$ OR

---
## 📘Lec 3

- **Complement ($F'$):** Toggle all bits
- **Minterm:** It's an AND term containing every variable exactly once, either complemented or uncomplemented
- **Maxterm:** It's an OR term containing every variable exactly once, either complemented or uncomplemented
- **Sum of Product (SOP):** AND first then OR, e.g. $F=xy+x'z$ 
- **Product of Sum (POS):** OR first then AND, e.g. $F=(x+y)(x'+z)$ 
- **Canonical & Standard Forms:**
	- **Terminology:**
		- **Canonical:** Every term must contain all variables exactly once, either complemented or not,            e.g.   (SOP) $\to xyz+xy'z$,             (POS) $\to (x+y+z)(x+y'+z)$ 
		- **Standard:** The equation is arranged into SOP or POS, but terms don't have to contain all variables, e.g.  (SOP) $\to x+yz$,                    (POS) $\to x(y+z)$
	- **Conversions:**
		- **Standard $\to$ Canonical:**
			- **SOP:** $(X+X')$, e.g. $F=xy \to F=xy(z+z') \to F=xyz+xyz'$ 
			- **POS:** $XX'$, e.g. $F=x+y\to F=x+y+zz'\to F=(x+y+z)(x+y+z')$ 
		- **Canonical $\to$ Indices:**
			- **Minterm:** $x\to0$,  $x'\to 1$      Notation $\to$ $\sum ()$ 
			- **Maxterm:** $x\to 1$,  $x'\to 0$     Notation $\to$ $\prod()$ 

---
