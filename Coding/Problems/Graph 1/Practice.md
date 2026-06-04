# Monsters 

#### Pattern Recognition

- Multiple sources spreading simultaneously
- Need to escape / reach a target before something else arrives

#### Techniques 

- Many sources $\to$ **Multi-Source BFS**
- Need to move/escape too $\to$ **Precompute arrival times** $\to$ **Run second BFS with constraints** 

#### Link
https://cses.fi/problemset/task/1194 

---
# White-Black Balanced Subtrees

#### Pattern Recognition

- Rooted tree & Question about every subtree
- Parent's answer depends on children's answers

#### Techniques

- Child computes subtree info $\to$ Returns to parent $\to$ Parent merges children's info $\to$ Parent now knows its entire subtree
- Using **Vectors** to compute the parent colors from children colors 

#### Link
https://codeforces.com/problemset/problem/1676/G

---
