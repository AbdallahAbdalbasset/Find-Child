# Problem: Find the Child

Mom has a beautiful boy, and she loves him dearly. One morning, she woke up and discovered that he was not beside her. Determined to find him, she began searching the city.

The city is represented as an $n \times m$ grid of squares. Each square belongs to a certain clan, denoted by an uppercase letter. Mom can only walk through the squares that belong to **her clan**.

- Mom always starts at the top-left cell $(1, 1)$.
- The child is located at one or more cells in the grid, each marked with the character `C`.
- Mom can move **up, down, left, or right** to a neighboring square (not diagonally).
- However, moving is unusual:  
  1. Mom may step into a cell only if it belongs to her clan **and** the parity (even/odd) of her total number of moves so far **matches the Manhattan distance** between $(1,1)$ and that cell.  
  2. Visiting the same cell more than once is allowed - At most 5 visits. but each additional visit costs **double** the previous one (first visit costs 1 move, second visit costs 2, third visit costs 4, etc.).

Your task is to find the **minimum total cost** Mom must pay to reach **any** cell containing her child. If it is impossible, print `-1`.

---

## Input
- The first line contains two integers $n, m$ ($2 \leq n, m \leq 1000$) — the number of rows and columns in the grid.
- The second line contains a single character $x$ — the clan Mom belongs to.
- The next $n$ lines each contain a string of $m$ uppercase letters, representing the grid. At least one cell will contain the letter `C`, denoting the child.

## Output
Print the minimum total cost Mom must pay to reach any child cell. If it is impossible, print `-1`.
