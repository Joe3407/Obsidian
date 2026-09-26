## 📘Lec 1

- **Java:**
	- **Technology:** 
		- **Java Virtual Machine (JVM):** 
			- It's the runtime machine that executes Java bytecode stored in `.class` files, which are produced by compiling `.java` source files 
			- It provides the layer that allows the same bytecode to run on different operating systems/platforms through different JVM implementations
		- **Java Runtime Environment (JRE):**
			- It provides JVM, Java libraries, other runtime components
			- It gives the environment necessary to run a Java program 
		- **Java Development Kit (JDK):**
			- It provides JRE, Development tools such as `javac`(which is the compiler), debugger, and other tools 
		- **Relationship:**
			- JDK = JRE + Development Tools
			- JRE = JVM + Java Libraries + Other Runtime Components
	- **Properties:**
		- **Object-oriented:** It supports concepts such as classes, objects, inheritance, polymorphism, encapsulation, and abstraction
		- **Interpreted:** Java is both compiled and interpreted, It's compiled when it compiles the `.java` file to `.class` file, and It's interpreted when JVM executes the bytecode 
		- **Portable:** Java bytecode is platform-independent and can run on different operating systems through platform-specific JVM implementations
		- **Secure & Robust:** It restricts direct memory manipulation unlike C/C++, which reduces certain memory-related errors and makes programs safer and more robust
		- **Multi-threaded:** Java supports multiple threads of execution within the same program, allowing different tasks to execute concurrently
		- **Garbage Collected:** It automatically reclaims memory from objects that are no longer reachable
		- **No support for multiple inheritance:** No child has multiple parents 
	- **Notes:** 
		- `.java`(source code) $\to$ `.class`(bytecode, compiled) $\to$ JVM (runs, interpret)
		- Bytecode is the same no matter how the OS changes, but the JVM that runs this bytecode is different according to different OS 
- **Object Oriented Programming:**
	- **Terminologies:**
		- Data, Fields, Attribute
		- Method, Function, Procedure 
	- **Principles:** 
		- **Encapsulation:** Exposes only necessary data
		- **Abstraction:** Hide complexity by hiding unnecessary detail from the user
		- **Inheritance:** Allows creating a hierarchy of related classes (Code reusability)
		- **Polymorphism:** The same concept/interface can be used with different forms or behaviors depending on the situation (Overloading, Overriding)

---


