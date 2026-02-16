## 📘Lec 1

- Declaring size we can use constant variables or literal values 
- `int const`or`const int`, as `const`applies to what is on its left if it's empty then applies on what's on its right 

- `#define` doesn't contain data type, if written inside a function it will still be global and could cause conflicts, can use `#undef` 
- `const` has data type, if written inside a function it obeys scope rules and isn't declared outside the function 

- `cout<<arr`, this outputs the address of the first element, `cout<<*arr`, this outputs the first element value 

- Initializing:
	- When array is created all elements are equal garbage 
	- We can initialize by:
		- In the same line ONLY, `int arr[5]={1,2,3,4,5}` 
		- For loop on array 
	- Note:
		- `int arr[5]={1,2,3}`, the array will automatically initialize rightmost elements with zeros 
		- `int arr[5]={1,2,3,4,5,6}`, will result in an error 
		- `int arr[5]={}`or`int arr[5]={0}`, all elements are initialized with zeros 
		- `int arr[]={1,2,3,4,5}`, it will automatically assign size with the number of elements in array 
		- Cannot copy array to another array like this `arr1=arr2` 

---
## 📘Lec 2

- `#include<cmath>` abs, pow, sqrt, ect... 
- When function is after main we declare it before main `return_type Fn_name(Parameters)` 
- `fun()`=`fun(void)` 
- Name of the variable can be the same as the name of the function inside it 
- Parameters $\to$ data types of function when building it 
- Arguments $\to$ Data types of function when calling it in main
- Swap built-in function calls the parameters by reference 
- All variables inside a function, and its non-reference parameters are destroyed once the function returns 
- A variable can be declared with the same name in different scopes(body of if, body a for loop, body of while), and when calling it from a position, it starts from this positions scope and moves to the outer scope till it finds this variable, A variable CAN'T be declared twice with the same name in the same scope 

---
