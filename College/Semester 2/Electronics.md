## 📘Lec 1 

- **Charge(C):**
	- quantity, Coulomb
	- It's the amount of water 
- **Current(A):**
	- rate of flow of electric charge $I=\frac{Q}{t}$ 
	- It's how much water flows per second 
- **Voltage(V):**
	- Energy transferred per unit of Charge $V=\frac{W}{Q}$ 
	- It pushes the water 
	- $V=IR$
- **Power(W):**
	- Rate of energy transferred $J/s$  
	- $P=VI$ 
- **Passive Reference Configuration(PRC):**
	- When current enters from terminal marked positive 
- **Energy Absorbed:** Power is positive, (if battery then its charging)
- **Energy Supplied:** Power is negative, (if battery then its discharging)
- **Note:**
	- Measuring the Power of Battery if Current **enters** from the -ve part then Current is negative, and if Current **enters** from +ve part then Current is Positive 
	- With Current source if Current enters from the tail of the arrow(-ve part) then Current is negative and vice versa 
	- Total Charge is equal integrate the intensity from $0\to t$ 

- Rules:
	- $I=\frac{Q}{t}$ 
	- $V=\frac{W}{Q}$
	- $V=IR$
	- $P=VI$ 

--- 
## 📘Lec 2

- **KCL:**
	- $I_{input}=I_{output}$ 
- **KVL:**
	- Negative side of battery, Resistant against current $\to -V_b$ 
	- Positive side of battery, Resistant along current $\to V_b$ 
	- Current moves from higher Volt(+) to lower Volt(-)
	- Current source $\to$ fixed current, arrow goes from $-\to+$ 
	- $V_1=R_1\frac{V_t}{R_{eq}}$ 
- **Connections:**
	- **Current:**
		- Series: Constant
		- Parallel: Divided
	- **Voltage:**
		- Series: Divided
		- Parallel: Constant
	- **Resistance:**
		- **Series:** $R_{eq}=R_1+R_2+R_3$
		- **Parallel:** $\frac{1}{Req}=\frac{1}{R_1}+\frac{1}{R_2}+\frac{1}{R_3}$ 
- **Source Types:**
	- **Independent Sources (Circle):**
		- Independent voltage source (battery)
		- Independent current source (current source)
	- **Dependent Sources (Diamond):**
		- Voltage Controlled Voltage Source  VCVS
		- Voltage Controlled Current Source  VCCS
		- Current Controlled Voltage Source  CCVS
		- Current Controlled Current Source  CCCS

---
## 📘Lec 3

- **Current Division:**
	- $I_1=\frac{I_t}{R_t}R_1$ 
- **Systematic Methods:**
	- **Node Analysis (KCL + Ohm's Law):**
		- **Nodal Voltage Analysis:**
			- **Independent Current Source:** 
				- **Steps to determine Voltage node:**
					- Identify Nodes: Pick ground node
					- Define Voltages: Label remaining voltages $v_1,\ v_2$ 
					- Define Currents: Label them with direction 
					- Write KCL for all non-ground nodes 
					- Replace I with $i=\frac{v_+-v_-}{R}$ 
					- Solve equations together 
				- **Short-cuts:**
					- Don't label the current and name it
					- Instead assume all current directions go out from the node and use the current rule at once $i=\frac{v_+-v_-}{R}$  
			- **Dependent Current Source:**
				- **CCCS:** Express the controlling current in terms of node voltages using Ohm's Law
				- **VCCS:** Express the controlling voltage directly in terms of node voltages
			- **Voltage Source:**
				- If connected directly with ground, then the voltage node is equal the voltage source with respect with the sign connecting it 
					- If the voltage node is connected to the + sign of voltage source then its voltage is positive and vice versa
				- If connected between two voltage nodes, then we use **Super Node** 
				- **Super Node:**
					- It's taking 2 or more voltage nodes, and considering them as one node

---
## 📘Lec 4

- **Systematic Methods:**
	- **Mesh Analysis (KVL + Ohm's Law):**
		- **Overview:**
			- **Medium:** It works only on planar circuits ($2d$)
			- **Loop:** Any closed path in circuit, and doesn't path on same node more than once 
			- **Mesh:** Loop that contains no other loop inside it, (smallest closed loop)
			- **Independent Loop:** Any loop that provides new independent KVL equations 
		- **Steps:**
			- Identify meshes, and assume them clockwise, so that if we have a common resistor, the answer will be $R(i_1-i_2)$ (the difference between meshes)
			- Apply KVL
			- Solve equations to get mesh currents
			- Use mesh currents to get branch currents, and Voltage by doing KVL, and putting the unknown voltage in the place we want to calculate 
		- **Source Types:**
			- **Voltage Source:**
				- **CCVS:** Express the controlling current directly in terms of mesh currents 
				- **VCVS:** Express the controlling voltage in terms of mesh currents using Ohm's Law 
			- **Current Source:**
				- **Exists in One Branch:** Directly substitute the mesh current with current source 
				- **Exists Between Two Meshes:** We use **Super Mesh**  
			- **Super Mesh:**
				- Treat two or more meshes as one extended mesh 
				- **Note:**
					- The third equation is resulted from $I_{current source}=i_1\pm i_2$ 
					- If we wanna know voltage on current source, we substitute it with an unknown voltage and do KVL 

---
## 📘Lec 5

- **Remember:**
	- **No Independent Sources:**
		- Linear System remains at absolute zero 
		- All nodal voltages equal zero
		- All currents equal zero 
		- No power delivered 
- **Linearity Principle:**
	- **Overview:** A circuit is called linear if changing the input changes the output in the same way
	- **Types:**
		- **Additivity:** $f(x+y)=f(x)+f(y)$ 
		- **Homogeneity (Scaling):** $f(kx)=kf(x)$  
- **Superposition Principle:**
	- **Overview:** Used to know how each independent source contributes to the circuit, based on **Linearity Principle**
	- **Rule:** We kill all independent sources except one, so that we know how much current and voltage does this source contribute to the circuit 
	- **Note:**
		- When killing the sources, Current Source $\to$ Open circuit, Voltage Source $\to$ Short circuit 
		- Superposition only works on linear equations, meaning that Power can't be directly calculated by this principle as there is an extra $2i_1i_2$ in $(i_1+i_2)^2$ 

--- 
## 📘Lec 6

- Circuit Simplification:
	- Series-Parallel Combinations 
	- Source Transformation
- Source Transformation:
	- Overview:
		- It doesn't affect the rest of the circuit 
		- It can be applied to dependent and independent sources
		- Current source arrow points towards positive terminal 
	- Conditions:
		- Ideal Voltage Source: Can't have $R=0$, as when transforming it the current will be $\infty$ 
		- Ideal Current Source: Can't have $R=\infty$, as when transforming it the voltage will be $\infty$ 
	- Rule:
		- We can transform a **Series** Voltage Source and Resistance to **Parallel** Current Source and Resistance 
	- After Transformation:
		- Voltage and Current on Resistance change, so it has a new voltage and current as it has been rearranged internally 
		- Always evaluate at terminals $a-b$, meaning that terminal voltage and current remains the same 
	- Notes:
		- When applying source transformation, don't include the resistor of interest

--- 

