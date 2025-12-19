## 📘Lec 1

- **Data:** it's raw facts (random numbers, input)
- **Information:** it's data that has been processed into something meaningful (sum of two numbers, output)
- **Flow (IPOS):** **Input (data) → Processing (work) → Output (information) → Storage (save for later)**

- **RAM:** stores currently used data, often from secondary memory, for cpu to access as it's much faster than directly accessing from secondary memory (volatile, GBs)
- **ROM:** it's important data that is stored and never deleted, like BIOS instructions as they are needed all the time to boot the pc (Non-volatile, MBs)
- **Cache:** it stores data & instructions that are frequently used by the cpu to avoid accessing it from RAM every time which will make it slower (volatile, KBs-MBs)

- **Control Unit(CU):** gives orders to register & ALU
- **Register:** holds values
- **Arithmetic Logic Unit(ALU):** does operations
- **Example:** when adding x and y the CU orders x and y to go to separate registers, then CU orders ALU to do the operation of adding them, then the output is stored in a register 

- **BIOS:** it's the first thing that starts when the pc is opened & it checks all the hardware then loads the bootloader to start the operating system
- **CMOS:** it stores changeable settings like data and time (BIOS settings), it's always alive due to the small battery called CMOS battery even when pc is off  

- **System Software:** runs the computer, OS(windows, macOS) & utility programs(antivirus)
- **Application Software:** runs for the user, chrome & games

- **PCI → AGP →  PCIe(PCI express)**, AGP is better than PCI as it transferred data faster but it was only for graphics card, then came PCIe which allowed all cards to go into it and also transferred data faster 
- **PC(1 user) → Minicomputers or midrange computer(10-100 users, business) → Mainframe(100-1000 users) → Supercomputers(few users or a single organization)**

- 📝Exam Notes:
     - An integrated circuit (or chip) includes million of transistors and carries electrical current
     - Computers for organizations are designed to be used by many people at the same time (Minicomputers(midrange servers), Mainframes, Supercomputers)

---
## 📘Lec 2

- **Base:** binary=2, decimal=10, hexadecimal=16
- **Weight:** binary=2^, decimal=10^, hexadecimal=16^

- **Hexadecimal:** used to compact binary data to make it easier for us to read, like using it in errors & colors
     - **Colors:** each color (red, green, blue) is represented by two hexadecimal digits as each digit holds 4 bits with a total of 8 bits for each color (0-255 in decimal)
     - **Indicators:** Memory address starts with **0x**, color starts with **#**

---
## 📘Lec 3

- **Sign-Magnitude:** we represent the number sign by making the most significant bit (0 → positive , 1 → negative)
     - Largest number: (2<sup>n-1</sup>-1)
 - **1's Complement:** flipping all digits to its complement (1 → 0, 0 → 1)
     - **How to Read:** (3)<sub>10</sub> → (0011)<sub>2</sub> $\xrightarrow{\text{1's complement}}$ (1100)<sub>2</sub>, the MSB represents the sign (0 → positive , 1 → negative) so here MSB (1) indicates negative then we flip the other bits (011)<sub>2</sub> which indicates (3)<sub>10</sub> so all together will be (-3)<sub>10</sub> 
     - **Problem:** Zero will be represented as +0 & -0 which is wrong, (0)<sub>10</sub> → (0000)<sub>2</sub> $\xrightarrow{\text{1's complement}}$ (1111)<sub>2</sub>, this means the MBS (1) indicates negative and after flipping the remaining bits it will represent (-0)<sub>10</sub> 
 - **2's Complement:** $1's Complement + 1$ 
     - Plus 1: it balances the equation as if we have a 4 bit the max number we can achieve is 15 and if we used the next bit it will be 16 so to balance the equation we add one in the 4 bit region  
     - **Relation between Number & Complement:** for example if we have (3)<sub>10</sub> as the number then its 2's Complement will be (00011)<sub>2</sub> $\xrightarrow{\text{2's complement}}$ (11101)<sub>2</sub> = (13)<sub>10</sub>, MSB is just to give the sign, if we open the next bit for the sign then it will be 16 and since 13 complements 3 to be equal to 16 so if we gave the MSB negative sign then add the complement number we will get the original number but in negative, (11101)<sub>2</sub> will be -16 + 13 = -3 
     - **Pros:** we can use it in athematic operations opposite to 1's Complement 
 - Subtracting: When subtracting we do 6+(-3) instead of 6-3
     - We equalize the number of bits in each number
     - The first stays as it is 
     - The second number is changed to its 2's Complement
     - Then add the two numbers
     - **Important Note:** we always do mod 2<sup>n</sup> so any overflow is neglected, The result of the subtraction must be in the range of the number of bits we choose like -5-7 cannot be represented in 4 bits as the range max is -8 so we use 5 bits, range is calculated by (-2<sup>n-1</sup> : 2<sup>n-1</sup> - 1)

---
## 📘Lec 4

- **Flowchart:**
     - **Oval:** Start/End, **Parallelogram:** Input/Output, **Rectangle:** Process, **Circle:** Connector, **Diamond:** If condition 
     - **Rules:** Has Start & End, Connected with Arrows, Arrows enters from top and exit from bottom except in condition can go from the sides 
 - **Pseudo-code:** 
     - Begin
     - **Input:** Read, Get, Accept
     - **Initialize:** Set, Init
     - **Processing:** Compute, Calculate, Set, Increment
     - **Output:** Print, Display, Show, Write
     - End
 - $<>$ → Not Equal 

---
## 📘Lec 5

- **Counter Controlled Loop:** number of executions is known
- **Sentinel Controlled Loop:** indefinite repetitions 
- **Pseudo-code:** (WHILE, ENDWHILE), (DO (code body) WHILE, ENDWHILE), (FOR, ENDFOR)

---
## 📘Lec 6

- **Source code:** it's any code like (cout<<"HELLO WORLD";), and it's called high level language as it's close to human languages, `.cpp file` 
- **Integrated Development Environment (IDE):** it's used to write, edit, debug the code before giving it to the compiler
- **Compiler:** it checks for errors first, then it translates the source code (`.cpp file`) into a syntax that the computer understands 
- **Program Phases:**
     - **Edit/Create:** writing the source code on the IDE
     - **Preprocessing:** it adds all the headers of included libraries(it does not know what the cout is for, it just prepares the code that there is a cout), it also clarifies the defined objects to its places (like` #define ll long long`, it changes every `ll` to long long)
     - **Compile:** it checks for errors, then it translates the `.cpp file` into a `.obj file` for the computer to understand
     - **link:** it links the `.obj file`&`.lib file` to a `exe.file` ready for the cpu to understand, (.lib file it now tells the computer the functions of the include header libraries like that the cout is to print the text)
     - **load:** it loads the .exe file to the main memory so that the cpu can access it faster
     - **Execute:** the cpu runs the code
     - **Note:** lines that has # are called preprocessor directives, that tells the preprocessor to include what's after it 
 - **Namespace std:** it's like a folder that holds standard library names like (cout, cin, vector & much more) and prevent any conflicts with variable names 
 - **Variable Identifier:** 
     - **Case sensitive:** a variable with capital letter is different from another with lower letter
     - contains letter, digits and underscore characters 
     - must begin with a letter or underscore
     - doesn't contain spaces, and can't match any keyword of the C++ language 
 - **Note:**  
     - **Equal sign:** operations on the RHS are executed first then it's assigned with the LHS
     - When we cout a variable that doesn't have a value it returns a garbage value (any random value)

--- 
## 📘Lec 7

- **Syntax Error:**
     - Not following grammatical rules 
     - Not declaring identifier
 - **Logic Error:**
     - the program will run normally but the logic is incorrect(addition instead of subtraction, infinite loop)
 - **Runtime Error:**
     - happens when running the program, caused by division by 0, Overflow 
 - **Note:** 
     - Syntax error is part of Compile error 
     - $if(cnt=a) (a\in R-{0}) \to true$ 
     - $cin.fail() \to$ if any of the input doesn't match the declared data type 
     - default in switch case is executed when we forget to put break in the upper cases 
     - The smallest addressable unit of memory in C++ $\to$ 1byte
     - && operation has higher precedence than || operation

---
## 📘Lec 8

- Precedence:
     - **Unary Operators:** `++,--,! `
     - **Binary Arithmetic Operators:** `*,/,%`
     - **Binary Arithmetic Operators:** `+,-`
     - **Boolean Operators:** `<,>,<=,>=`
     - **Boolean Operators:** `==,!=`
     - **Boolean Operators:** `&&`
     - **Boolean Operators:** `||` 

---
## 📘Lec 9

- The counter whose initialized inside loop, its scope is only inside the loop and can be used as another variable outside this loop
- $for(;n<10;) = while(n<10)$ 
- Be careful about the statements inside the braces, and the position of the semi colon 

---
## 📘Lec 10

- LCM: can be calculated by taking the bigger number and see its multiples till one of them is divisible by the other number 