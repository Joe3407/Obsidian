## 📘Lec 1

- Declaring size we can use constant variables or literal values 
- `int const`or`const int`, as `const`applies to what is on its left if it's empty then applies on what's on its right 

- `#define` doesn't contain data type, if written inside a function it will still be global and could cause conflicts, can use `#undef` 
- `const` has data type, if written inside a function it obeys scope rules and isn't declared outside the function 

- `cout<<arr`, this outputs the address of the first element, `cout<<*arr`, this outputs the first element value 

- **Initializing:** 
	- When array is created all elements are equal garbage 
	- **We can initialize by:**
		- In the same line ONLY, `int arr[5]={1,2,3,4,5}` 
		- For loop on array 
	- **Note:** 
		- `int arr[5]={1,2,3}`, the array will automatically initialize rightmost elements with zeros 
		- `int arr[5]={1,2,3,4,5,6}`, will result in an error 
		- `int arr[5]={}`or`int arr[5]={0}`, all elements are initialized with zeros 
		- `int arr[]={1,2,3,4,5}`, it will automatically assign size with the number of elements in array 
		- Cannot copy array to another array like this `arr1=arr2` 

---
## 📘Lec 2

- `#include<cmath>` abs, pow, sqrt, ect... 
- When function is after main we declare it before main `return_type Fn_name(Parameters);` 
- `fun()`=`fun(void)` 
- Name of the variable can be the same as the name of the function inside it 
- Parameters $\to$ data types of function when building it 
- Arguments $\to$ Data types of function when calling it in main
- Swap built-in function calls the parameters by reference 
- All variables inside a function, and its non-reference parameters are destroyed once the function returns 
- A variable can be declared with the same name in different scopes(body of if, body of a for loop, body of while), and when calling it from a position, it starts from this positions scope and moves to the outer scope till it finds this variable, A variable CAN'T be declared twice with the same name in the same scope 

---
## 📘Lec 3

- **Casting:**
	- `double/int`, the cast happens first then the division, `double/int`$\to$`double/double`$\to$`double` 
- **Parameter Default Value:**
	- Must be from right to left, `sum(int a, int b, int c = 10)` 

--- 
## 📘Lec 4

- Struct takes place in memory by the order of its attributes, for example if we had `int age` `float salary`, then in memory it takes 4 bytes for the age then beside it another 4 bytes for float 
- When declaring the attributes in struct, they don't take space in memory unless we create an object from it
- By creating struct object before the last semi colon of the struct, then these objects are initialized by zero
- `Student s1{}`,`Student s1={}` this makes s1 initialized with zero
- Initializing:
	- `Student s1={"Ali","3bas",3.4}` 
	- `Student s1; s1.name="Ali"; s1.address="3bas"; s1.gpa=3.4` 
- Can't equalize different data types, `Student s1; Emloyee emp;`, so we can't say that `s1=emp` even if they have same attributes
- `cout<<array;` gives the address of the first element of the array

---
## 📘Lec 5

- Nested Struct: order matters, the inner struct must come before outer struct 

---
## 📘Lec 6

- **Reference Variable:** It's another name for the variable, It points to the address memory of the other variable, It's value is NOT the address memory
- Arrays are always passed by reference `void fun(int a[])` 
- **Note:** 
	- After finishing function, all variables & reference variables are deleted from memory, but the reference variables effect remains 
	- When calling arguments by value, their variable must be assigned with a value, but when passing by reference, it's not mandatory to give it a value 

---
## 📘Lec 7

- In 2D array, the memory location is linear, meaning that elements of array are sorted consecutively in memory 
- Initializing:
	- `int a[2][3]={ 1, 2, 3, 11, 12, 13 };` 
	- `int a[2][3]={ {1, 2, 3}, {11, 12, 13} };` 
	- `int a[2][3]={ 1, 2, 3, 11, 12 };` it replaces the last element in the last row with zero
	- `int a[2][3]={ {1}, {11, 12} };` it replaces the second and third elements in the first row with zeros, and replaces the last element in last row with zero 
	- `int a[][SZ]={};` Must at least give the column size for it to work 
- When passing 2D array to a function the column size must be declared `void fun(int arr[][SZ])`  

--- 
