## Recursion & Backtracking

- In grid, if we want to check a box of `3*3` for example, then we can `while(x!=0&&x!=3)x--` 
- In grid, if we want to traverse + backtrack on 2d then we use `int pos` where `x=pos/n` and `y=pos%n`    (Problem K in ACM, Backtracking)
- **Meet in the middle algorithm:** 
	- when we want to backtrack but `n<=40` so we split the vector into two vectors and perform backtracking on each one individually 
- To print an integer digit by digit $123 \to 1\ 2\ 3$, then we can use recursion to call all the function calls then start to cout them `fun(n/10);cout<<n%10;` 
- **nCr:**
	- $(nCr=\frac{n!}{(n-r)!} \frac{1}{r!})\to (nCr=nPr\frac{1}{r!})$ 