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
	- Think of Two way Dijkstra if the problem doesn't need shortest path like in problem **C in ACM, Graph 2 contest** 

- **Topological Sort:**
	- **Problem D in ACM, Graph 2 practice:**
		- **Detect cycle:**
			- **dfs:** We can use `vis` to detect it, where 0 won't be visited, 1 currently trying, 2 complete cycle 
			- **bfs:** We can check at the end of the `bfs` function if `ans.size()!=n`, then there is a cycle 
	- **Problem A in ACM, Graph 2 contest:**
		- If we want uniqueness then we must use **bfs**, and check if the queue size is greater than one at any point then it's not unique
		- If we use **dfs** and count the edges coming and entering, it will fail by this test case $1\to2\to3$, $1\to3$, this is unique but since the 3 has to edges entering so the **dfs** logic breaks 

- **Problem G in ACM, Graph 2 practice & G in ACM, Graph 2 sheet:**
	- In the practice, the problem wanted the second shortest path, which can be handled by doing 2 `dist` arrays that handle each case, one for the shortest and one for the second best shortest
	- In the sheet, the problem now wants all k shortest paths, so it's very hard to handle it with separate `dist` arrays, instead we will have a `counter` array, that counts how many times a node have been popped, and each time that the counter is still under $k$, then explore this node further. this will get us all the paths up to $k$ in increasing order 

- **Problem H in ACM, Graph 2 sheet:** 
	- We didn't know at first what the order of the undirected edges, so we will get the order of the directed nodes first, then sort the rest of the undirected edges with respect to the topological sorting of the directed 

---
## Support 1

- Traversing Multiple Edges at a time:
	- We use a two state distance array `dist[node][state]`, like in question https://vjudge.net/contest/803773#problem/F & https://vjudge.net/contest/802663#problem/F
- Cycle Detection:
	- Undirected: 
		- If $m>n-1$, then there is a cycle
	- Directed:
		- Using the visited array with values $0\to$ not visited, $1\to$ currently exploring it, $2\to$ explored it already, so if we encounter a 1 then this means that there is a cycle

- Meet in the Middle (on grid):
	- We will get the middle diagonal $mid=\frac{n+m-2}{2}$, and we dfs from $(0,0)\to x+y=mid$, and then dfs again from $(n-1,m-1)\to x+y=mid$, and then we see if there is what we need in map or not     https://vjudge.net/contest/803801#problem/A

--- 
## Number Theory

- Spf: 
	- Prime Factors 
	- Greatest proper divisor 