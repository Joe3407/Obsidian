- **long long:** −2⁶³ → 2⁶³−1, **unsigned long long:** 0 → 2⁶⁴−1

- $\text{ceil}\left(\frac{x}{y}\right) = \frac{x + y - 1}{y}$ 

- string takes more memory than array of char and may lead to MLE

- $x \le y \to x-c \le y-c$,  $x \le y \to c-x \ge c-y$, (where c is a constant)

- queue calls deque internally so that it can benefit from its functions, for example(`queue.push()` calls `deque.push_back()` internally), this makes it simpler as we only write the function we need once then include it in other classes to benefit from there function, it also makes it easier when an error occur; instead of correcting the error in every class, we just correct it in the original class, and all other classes that has it included are automatically using the corrected version 

- **std:** It's a namespace, (it's not a library nor a function), it has all the keywords like vector, map, cout,... (but not the language keywords like `int, double, for,...` these are hard coded in the compiler) it's declared in the library header, it's used to avoid conflicts, as back then if we wanted to make a variable named sort it will get confused when trying to access this variable as it won't know what to take; the variable or the function, so to avoid all this we can do `std::sort` which means use the sort that is in the namespace which sorts an array for example, and also `int sort` will then be used as a variable, so in conclusion std is used to avoid conflicts between built in keywords and user keywords in big projects

- **library:** it's just used to avoid writing all the classes in a library with all its attributes and methods where errors are very likely to happen, so it just stores all that and by `#include` we can insert all the classes in just one line without any errors 

- Templates $\to$ vector, map, sort,... (all its code is in the header, no separate files)     Non-Templates $\to$ cout, cin (it has separate files)

- How does compiler not crash when including all libraries? when including a library only the essential functions and attributes are only included like the ones in constructor and destructor, and then if we use any other function or attribute it gets included so not everything is included only the ones that we use are

- OOP: in constructor there will always be a default constructor `s1(const Student&)` which is already built in and allows us to use the same class object inside new object of same class, we can delete it by going to .h file and type `Student(const Student&)=delete;`, `Student& operator=(const Student&) = delete;` wont allow us to assign object of a class with another object of the same class `s1=s2` 

- `getline(cin,s)` $\to$ to cin a string that has spaces 

- `bool → char → short → int → unsigned int → long → unsigned long → long long → float → double → long double` (from weakest to strongest) 

- With operations `char`&`short` always gets promoted to `int` even if  we did `char + char` 

- `unsigned int + int` promotes `int` to `unsigned int` and if the number was negative it gets changed to a huge value 

- `char & short` are slower that `int` when dealing low memory as `char & short` are 2 bytes and 3 bytes respectively and `int` is 4 bytes, but the cpu uses 4 bytes, so for it to use `char & short` it must assign zeros till it becomes 4 bytes, which takes more time, but when dealing with high memory it's best to use `char & short` if possible as they use less memory  

- `Bit → 0, 1` `Nibble → 4 bits` `Byte → 8 bits` 

- `unsigned char → 0:255` characters after 127 are normal characters like `,` or `€` 
- `signed char → -128:127` negative characters aren't printable unless we cast them as `int`, so only then it will print the negative char as it is but as an integer 

- `Null → char c = '0' or '\0'` and when printing it's invisible not even a space or anything, and when casting it with `int` it prints 0 
- `string s="Hello\0World" → cout<< s  // prints Hello only ` 