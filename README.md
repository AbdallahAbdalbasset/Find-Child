# Problem: Find the Child

Mom has a beautiful boy, and she loves him dearly. One morning, she woke up and discovered that he was not beside her. Determined to find him, she began searching the city.

The city is represented as an $n \times m$ grid of squares. Each square belongs to a certain clan, denoted by an uppercase letter. Mom can only walk through the squares that belong to **her clan**.

- Mom always starts at the top-left cell $(1, 1)$.
- The child is located at **exactly one** cell in the grid, marked with the character `C`.
- Mom can move in **8 directions**: up, down, left, right, and the 4 diagonals.
- Each square has **two entry costs**:  
  - one if she steps into it with an **even** move count,  
  - and another if she steps into it with an **odd** move count.  
- Visiting the same cell is allowed **any number of times**. Each visit costs the corresponding parity-based cost.

Your task is to find the **minimum total cost** Mom must pay to reach the child cell. If it is impossible, print `-1`.

---

## Input
- The first line contains two integers $n, m$ ($2 \leq n, m \leq 1000$) — the number of rows and columns in the grid.
- The second line contains a single character $x$ — the clan Mom belongs to.
- The next $n$ lines each contain a string of $m$ uppercase letters, representing the clans in the grid. **Exactly one** cell will contain the letter `C`, denoting the child.
- The following $n$ lines each contain $m$ integers — the costs of entering each cell **on an even step count**.  
- The following $n$ lines each contain $m$ integers — the costs of entering each cell **on an odd step count**.

## Output
Print the minimum total cost Mom must pay to reach the child cell. If it is impossible, print `-1`.

---
