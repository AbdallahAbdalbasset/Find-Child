# Problem: Find the Child  

Mom has a beautiful boy, and she loves him dearly. One morning, she woke up and discovered that he was not beside her. Determined to find him, she began searching the city.  

The city is represented as an $n \times m$ grid of squares.  
- Each square belongs to a certain clan, denoted by an uppercase letter.  
- Mom can only walk through squares that belong to **her clan**.  
- The child is located at exactly **one cell**, marked with the character `C`.  
- Mom always starts at the top-left cell $(1, 1)$.  

---

## Movement Rules
- Mom can move **up, down, left, or right** to a neighboring cell (no diagonal moves).  
- Each move costs exactly **1**.  
- However, she can only step into a cell $(i,j)$ if the following condition holds:

\[
(\text{Manhattan distance from } (1,1) \text{ to } (i,j)) \bmod 100 = (\text{number of steps taken so far}) \bmod 100
\]

- The starting position $(1,1)$ is always valid.  

---

## Task
Find the **minimum number of moves** required for Mom to reach the child’s cell.  
If it is impossible, print `-1`.  

---

## Input
- The first line contains two integers $n, m$ ($2 \leq n, m \leq 1000$) — the number of rows and columns in the grid.  
- The second line contains a single uppercase character $x$ — the clan Mom belongs to.  
- The next $n$ lines each contain a string of $m$ uppercase letters — the city grid.  
  - The grid contains exactly one character `C`.  

---

## Output
Print a single integer — the minimum number of moves needed to reach the child’s cell.  
If it is impossible, print `-1`.  
