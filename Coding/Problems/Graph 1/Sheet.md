# Longest path in a tree

#### Pattern Recognition 

- Longest path in a tree
- Diameter of a tree

#### Techniques

- Tree Diameter $\to$ **Double DFS/BFS** 

#### Link
https://www.spoj.com/problems/PT07Z/en/

---
# Two Buttons

#### Pattern Recognition  

- A state (number, string, mask, position, etc.)
- Allowed operations that transform one state into another
- Need minimum number of operations

#### Techniques

- Minimum operations $\to$ **Shortest path in unweighted graph** $\to$ **BFS** 

#### Link
https://codeforces.com/problemset/problem/520/B

---
# Arboris Contractio

#### Pattern Recognition 

- Reshaping Tree 

#### Techniques

- Work Backwards 
- Don't focus on how to do the complex operation, instead focus on what will the end shape look like 

#### Link
https://codeforces.com/problemset/problem/2131/D

---
# Tree Coloring (Easy Version)

#### Pattern Recognition 

- If a problem asks for the **minimum number of operations**, where:
	- Each operation selects a subset of valid elements,
	- Elements in the same operation must satisfy some compatibility constraints

#### Techniques

- Find an obvious lower bound $\to$ Assume the lower bound is achievable $\to$ Ask: What prevents equality? $\to$ Characterize the obstruction
- The final answer is often the lower bound plus exactly what the obstruction forces
- If there is a group that share one operation, and so on with the rest of groups, then we could **assume that each operation is a Color** 

#### Link
https://codeforces.com/problemset/problem/2183/D1

---
