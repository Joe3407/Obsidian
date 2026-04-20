# T-primes 

#### Wrong Approach

- Tried factoring each number
- $O(n * sqrt(x)) → TLE$ 

#### Logic

- The number of divisors $\to$ $(e_1+1)*(e_2+1)*(e_3+1).....$, where $e$ is the power of Prime Factors of a number, ($1$ is the possibility of not including the number)
- Since the question asks that the number is to be $3$, so the only way possible is for it to have only one Prime Factor & for it to be Perfect Square 

#### Solution 

- Check if x is perfect square
- Let y = sqrt(x)
- Check if y is prime (using sieve)

#### Tricks 

- $Number\ of\ Divisors = (e_1+1)*(e_2+1)*(e_3+1).....$ 
- Reduce **3 divisors** → **square of a prime**

#### Link
https://codeforces.com/problemset/problem/230/B

---
# Square-Free Division (easy version)

#### Wrong Approach

- Checked all pairs $(ai * aj)$ for perfect square
- $O(n^2)\to TLE$ 

#### Logic

- A perfect square has all its prime factor powers even 
- We can only keep track of the odd power only and neglect the even powers 

#### Solution 

- Get the odd powers (using spf)
- Keep track with **set** till we reach the same number (odd power divisors) 

#### Tricks

- **Transform numbers** → **Square-free form**, (numbers that aren't perfect square) 

#### Link
https://codeforces.com/problemset/problem/1497/E1

--- 

