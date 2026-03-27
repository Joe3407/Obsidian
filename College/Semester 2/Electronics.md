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
- **Node Analysis:**
	- Current is complicated and can't be solved by ohm law
	- We take each node and do KCL at each node till we get number of equations equal to number of unknowns 
- **Systematic Methods:**
	- **Node Analysis:**
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
			- **Independent Current Source:**
				- **CCCS:** Express the controlling current in terms of node voltages using Ohm's Law
				- **VCCS:** Express the controlling voltage directly in terms of node voltages
			- **Voltage Source:**
				- If connected directly with ground, then the voltage node is equal the voltage source with respect with the sign connecting it 
					- If the voltage node is connected to the + sign of voltage source then its voltage is positive and vice versa
				- If connected between two voltage nodes, then we use **Super Node** 
				- **Super Node:**
					- It's taking 2 or more voltage nodes, and considering them as one node

---
