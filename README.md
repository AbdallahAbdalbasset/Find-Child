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
- She may visit the **same cell multiple times**, but **at most 1000 times**.  
- Each time she steps into a cell, she pays a cost:  
  - If her total number of steps so far is **even**, she pays the cell’s **even cost**.  
  - If her total number of steps so far is **odd**, she pays the cell’s **odd cost**.  
- The starting cell also requires paying its cost based on parity (step $0$ is considered even).  

---

## Task
Find the **minimum total cost** required for Mom to reach the child’s cell.  
If it is impossible, print `-1`.  

---

## Input
- The first line contains two integers $n, m$ ($2 \leq n, m \leq 1000$) — the number of rows and columns in the grid.  
- The second line contains a single uppercase character $x$ — the clan Mom belongs to.  
- The next $n$ lines each contain a string of $m$ uppercase letters — the city grid.  
  - The grid contains exactly one character `C`.  
- Then $n$ lines follow, each containing $m$ integers: the **even costs** for each cell.  
- Then another $n$ lines follow, each containing $m$ integers: the **odd costs** for each cell.  

---

## Output
Print a single integer — the minimum cost to reach the child’s cell.  
If it is impossible, print `-1`.  

---

## Example 1
**Input**  
