# Problem: Grid Path with Parity Costs

You are given an $n \times m$ grid. Each cell contains an uppercase letter representing its clan.  
You are also given a character $x$ representing Mom’s clan. Mom starts at the top-left cell $(1,1)$ and can only walk on cells belonging to her clan.  
There is exactly one cell marked with the character `C`, representing the child’s position.

Mom wants to reach the child with the **minimum total cost**.

---

## Movement Rules
- From a cell $(i,j)$, Mom can move **up, down, left, or right** (no diagonal moves).  
- The $k$-th move (0-indexed) has a **parity**:
  - If $k$ is even, entering cell $(i,j)$ costs its **even cost**.
  - If $k$ is odd, entering cell $(i,j)$ costs its **odd cost**.
- Let $d(i,j)$ be the Manhattan distance from $(1,1)$ to $(i,j)$.  
- Mom can move into a cell $(i,j)$ on step $k$ **if and only if**:

\[
d(i,j) \bmod 100 = (k \bmod 100)
\]

---

## Task
Determine the minimum cost needed for Mom to reach the child.  
If it is impossible, output `-1`.

---

## Input
- The first line contains two integers $n, m$ ($2 \leq n, m \leq 1000$) — the grid dimensions.  
- The second line contains a single uppercase letter $x$ — Mom’s clan.  
- The next $n$ lines each contain a string of $m$ uppercase letters describing the grid.  
  - Exactly one cell is marked `C`.  
- The next $n$ lines each contain $m$ integers — the **even costs** for the cells.  
- The next $n$ lines each contain $m$ integers — the **odd costs** for the cells.  

---

## Output
Print a single integer — the minimum cost required to reach the child.  
If it is impossible, print `-1`.
