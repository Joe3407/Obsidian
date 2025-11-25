# Definition:
Adds the last two elements of the sequence
# Purpose:
Great example to learn `recursion` & `dp(memoization)`
# Code:
Before `dp`:
- **Time Complexity** = `O(2^n)`
- **Space Complexity** = `O(n)`
After `dp`:
- **Time Complexity** = `O(n)`
- **Space Complexity** = `O(n)`
> [!example]- Click to expand Fibonacci code
> ```cpp
> dp[N];  //initialize with -1 using memset(dp,-1,sizeof(dp)) in main
> int fib(int n) {
>     if (n <= 1) return n;
>     if (dp[n] != -1) return dp[n];
>     return dp[n] = fib(n-1) + fib(n-2);
> }
> ```
