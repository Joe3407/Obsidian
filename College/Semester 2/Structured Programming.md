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
