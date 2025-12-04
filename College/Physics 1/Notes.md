## 📘Lec 1

- $v = u + at$  
- $s = ut + 0.5at^2$  
- $v^2 = u^2 + 2as$  
- $X_f - X_i = \frac{1}{2} (V_i + V_f) t$
- $v_{\text{avg}} = \Delta s / \Delta t \ (\text{or } (s_2 - s_1)/(t_2 - t_1))$  
- $a_{\text{avg}} = \Delta v / \Delta t \ (\text{or } (v_2 - v_1)/(t_2 - t_1))$
- $x(t) \xrightleftharpoons[\text{integrate}]{\text{differentiate}} v(t) \xrightleftharpoons[\text{integrate}]{\text{differentiate}} a(t)$

---
## 📘Lec 2

- **Coordinate System:** Cartesian→(x, y), Polar→(r, θ)
- **Conversion:**
     - $r = \sqrt{x^2 + y^2}$, $\tan(\theta) = \frac{y}{x}$ 
     - $x=rcos(θ)$, $y=rsin(θ)$
 - **Vector Equality:** same magnitude & direction
 - Adding Vectors:
     - **Algebraically:** Resultant → Adding the i's and j's of both vectors, Magnitude → $| \vec{A} \pm \vec{B} | = \sqrt{A^2 + B^2 \pm 2AB\cos\theta}$ 
     - **Graphically:** Connecting the tail of the first vector with the head of the last vector, or by the parallelogram method that places both vectors on the same point and continue the shape of the parallelogram then the resultant is the diagonal
 - **Subtracting Vectors:** 
     - **Graphically:** $(\vec{A}-\vec{B})$=$(\vec{A}+(-\vec{B}))$, so we draw both vectors then changing the direction of the negative one then connecting the first tail with the head of the second
 - **Multiplying Vectors:** 
     - **Dot Product:**
         - Multiplying the components(A<sub>x</sub> & B<sub>x</sub>) of the vector directly if the vectors are given with there components (we directly multiply them as each component is in the same direction with the other so angle is zero and the cosine will be equal 1 so we just remove the cosine from the equation)
         - $\vec{A} \cdot \vec{B} = |\vec{A}| \, |\vec{B}| \cos\theta$, if the vectors are given with the angle between them
     - **Cross Product:** 
         - $\vec{A} \times \vec{B} = |\vec{A}| \, |\vec{B}| \sin\theta \, \hat{n}$ 
 - Notes:
     - **Rectangular Form:** get $\hat{i}, \hat{j}, \hat{k}$  
	 - **Unit Vector:** get the magnitude, then divide the components by the magnitude
	 - **Magnitude:** $|\vec{A}| = \sqrt{A_x^2 + A_y^2 + A_z^2}$ 

---
## 📘Lec 3

- **1d Motion:** we use either $\hat{i}$ or $\hat{j}$, so it's enough to use signs to know the direction
- **2d Motion:** It's not sufficient to use signs only, we must use the whole vector to represent it

- Velocity direction = Motion direction, Acceleration direction $\neq$ Motion direction, Example: when throwing a ball upwards the motion is up and the velocity is up but the acceleration is gravity down 

- **Kinematic Equation:** It can be handled as one equation or by separating the x component and y component, **Time is common in both equations** 

- **Rules With Explanation:** 
     - **General Information:** $a_x =0$, $a_y = -g$, $V_x =V_i cos(\theta_i)$, $V_y=V_i sin(\theta_i)$ 
     - **Velocity at any time:** 
         - $V_x = V_{xi}$, (since $a_x =0$, so from the first equation we get this conclusion)
         - $V_y = V_{yi} -gt$ 
     - **Position at any time:** 
         - $\Delta x = V_{xi}t$, (from the second equation as acceleration is zero)
         - $\Delta y=V_{yi} t -\frac{1}{2}a_y t^2$ 
         - **From 1 & 2 (Path Equation)** → $\Delta y = x\Delta tan(\theta_i)- \frac{1}{2}g(\frac{x}{V_icos(\theta_i)})^2$, (it came from substituting all t in 2 with 1)
         - **Time of max height:** $t_h = \frac{V_isin(\theta_i)}{g}$,(only when $V_{yf}=0$), $t_r=2t_h$ 
         - **Max height:** $h=\frac{(V_i)^2 sin^2(\theta_i)}{2g}$,(only when $V_{yf}=0$)
         - **Range:** $x=V_{xi}t_r$ → $V_icos(\theta) \frac{2V_isin(\theta_i)}{g}$ → $\frac{V_i^2sin(2\theta_i)}{g}$ 
         - Max Range → $\theta_i=45^\circ$ 
- **Equations:** 
     - $V_x = V_{xi}$
     - $V_y = V_{yi} -gt$ 
     - $\Delta x = V_{xi}t$
     - $\Delta y=V_{yi} t -\frac{1}{2}a_y t^2$
     - $\Delta y = x\Delta tan(\theta_i)- \frac{1}{2}g(\frac{x}{V_icos(\theta_i)})^2$
     - $t_h = \frac{V_isin(\theta_i)}{g}$
     - $t_r=\frac{2V_isin(\theta_i)}{g}$ 
     - $h=\frac{(V_i)^2 sin^2(\theta_i)}{2g}$
     - $R=\frac{V_i^2sin(2\theta_i)}{g}$ 
 - Notes
     - How Far → Magnitude
     - $\theta_i =0$, (when $V_{yi}=0$)
     - $9.8 m/s^2=32 ft/s^2$ 

---
## 📘Lec 4

- **Rules:**
     - $\sum F_x=0, \sum F_y=0$ 
     - $\sum F=ma$ 
     - $N=ma$, (For every reaction there is a reaction equal in magnitude and opposite in direction)
     - $F_f=\mu N$, ($F_f\propto N$)
 - **Contact Force:** It's the reaction of the body being pushed by other body 
 - Notes:
     - Reaction happens only with contact
     - Friction: Static → $\mu_s$ (rest, about to move), Dynamic → $\mu_d$, (they differ even its the same object)
     - Tension direction depends on the body we study
     - Sum Forces direction = Acceleration direction 
     - Normal only affects the object in contact with it, and the objects that aren't directly in contact with it just affect its magnitude

---
## 📘Lec 5

- **Uniform Circular Motion:**  
     - **Velocity:** magnitude(constant), direction(changes) always tangent 
     - **Acceleration:** centripetal acceleration directed toward the center 
     - **Rules:**
         - $a_c=\frac{v^2}{r}=\omega^2 r$ 
         - $v=\omega r$
         - $T=\frac{2 \pi r}{v}=\frac{2 \pi}{\omega}$ 
         - $f=\frac{1}{T}=\frac{n}{t}$ 
- **Non-Uniform Circular Motion:** 
     - **Velocity:** magnitude(changes), direction(changes)
     - **Acceleration:** centripetal acceleration(due to the change in the direction) and tangential acceleration(due to the change of magnitude of velocity)
     - **Rules:**
         - $a_t=\frac{\Delta v}{\Delta t}$ 
         - $a=\sqrt{a_c^2+a_t^2}$ 
     - **Note:** 
         - the direction of the tangential acceleration depends on the velocity

---
## 📘Lec 7

- **Newton's Laws on Uniform Circular Motion:** 
     - $\sum F_c=ma_c=\frac{mv^2}{r}$
     - $\sum F_t=ma_t=0$ 
 - **Newton's Laws on Non-Uniform Circular Motion:**
     - $\sum F_c=ma_c=\frac{mv^2}{r}$
     - $\sum F_t=ma_t$
     - $|F_T|=\sqrt{F_c^2+F_t^2}$ 
 - **Applications:**
     - **Motion in a Horizontal Circle:** $v_{max}=\sqrt{\frac{T_{max}r}{m}}$, (where $T_{max} \to Tension$)
     - **Conical Pendulum:**  
         - $r=lsin(\theta)$ 
         - $v=\sqrt{glsin(\theta)tan(\theta)}$ 
         - $T=2\pi \sqrt{\frac{lcos(\theta)}{g}}$ 
     - **Loop the Loop:**
         - **Bottom:** $\sum F_c= n-mg=\frac{mv^2}{r}$ 
         - **Top:** $\sum F_c= n+mg=\frac{mv^2}{r}$ 
     - **Roller Coaster:** 
         - **Bottom:** $\sum F_c= n-mg=\frac{mv^2}{r}$
         - **Top:** $\sum F_c=mg-n=\frac{mv^2}{r}$ 
     - **Ball Tied to a Rope:** Motion is vertical so weight is resolved into x and y 
     - **Horizontal flat curve:** 
         - Friction force is toward the center
         - $v=\sqrt{\mu gr}$ 

---
## 📘Lec 8

- Work on Constant Force:
     - Energy moved through force along displacement, unit $\to$ $Joule$ 
     - Scalar Quantity, +ve $\to$ gain energy(same direction as displacement), -ve $\to$ lose energy(opposite direction as displacement)
     - $W=Fcos(\theta)\Delta r=\vec{F}.\vec{\Delta r}$ 
     - $W_{net}=\sum FS$ 
     - Note: when F is constant and we draw the graph between F and x then the Work is the area under the graph, so we integrate if the work is on a variable force
 - Work on Variable Force:
     - $W=\int_{xi}^{xf} F_xdx$  
 - Spring(Hook's Law):
     - Every string has a unique spring constant(coefficient of elasticity) K that measures the stiffness of the spring, unit $\to$ $N/m$ 
     - Direction of Force is opposite to Direction of Displacement
     - $F_s=-Kx$ 
     - Work will be the integration of the Force, as force is variable
     - $W_s=\int_{xi}^{xf}-Kxdx=\frac{1}{2}K(x_i^2-x_f^2)$ 
 - Kinetic Energy:
     - $W_{net}=\Delta K.E$ 