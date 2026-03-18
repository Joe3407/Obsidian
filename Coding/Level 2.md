## Recursion & Backtracking

- In grid, if we want to check a box of `3*3` for example, then we can `while(x!=0&&x!=3)x--` 
- In grid, if we want to traverse + backtrack on 2d then we use `int pos` where `x=pos/n` and `y=pos%n`    (Problem K in ACM, Backtracking)
- **Meet in the middle algorithm:** 
	- when we want to backtrack but `n<=40` so we split the vector into two vectors and perform backtracking on each one individually 
- To print an integer digit by digit $123 \to 1\ 2\ 3$, then we can use recursion to call all the function calls then start to cout them `fun(n/10);cout<<n%10;` 
- **nCr:**
	- $(nCr=\frac{n!}{(n-r)!} \frac{1}{r!})\to (nCr=nPr\frac{1}{r!})$ 

---
## Graph 1

- `sort(start,end,[capture](parameters))`:
	- Capture: takes input from outside, which in sort we don't take anything
	- Parameters: usually when doing (auto& a, auto& b) it automatically detects what data type is the vector, IF & ONLY IF it's `c++14` or higher 
	- Note: 
		- `[capture](parameters)` this is lambda
- `sort(start,end,cmp)`, `bool cmp(auto& a, auto& b){body}`, this is equivalent to lambda

- **Double dfs:**
	- If we wanna know the longest path in a tree, then we can choose any node and dfs from it, and get the furthest node it can reach, then do another dfs on the furthest node to get the longest path (Problem A in ACM, Graph1)

- To access the leaf in dfs, it must not have any `!vis[node]` in adjacent nodes, so we can create a Boolean  

--- 
## Graph 2

- **Dijkstra:** There is no such thing as visited array, instead we use distance array, which handles the cost or weight 

- **Problem C & E in ACM, Graph 2 practice:** 
	- **Two way Dijkstra:** We compute Dijkstra from $1\to n$ and from $n\to 1$, then we can access any edge and get the before from the first Dijkstra and get the after from second Dijkstra. 
	- `dist` array must always be inside the for each loop, for it to be optimal and to avoid TLE 
	- Two state `dist`, we can replace here the Two way Dijkstra with Two state `dist[node][used]` 

- **Topological Sort:**
	- **Problem D in ACM, Graph 2 practice:**
		- **Detect cycle:**
			- **dfs:** We can use `vis` to detect it, where 0 won't be visited, 1 currently trying, 2 complete cycle 
			- **bfs:** We can check at the end of the `bfs` function if `ans.size()!=n`, then there is a cycle 