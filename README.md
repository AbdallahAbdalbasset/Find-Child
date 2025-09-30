# Problem: Grid Path with Parity Costs

Mom is searching for her child in a city represented as a grid.  
Each cell of the grid belongs to a clan, denoted by an uppercase letter.  
Mom belongs to a specific clan and can only walk on cells of her clan.  

There is exactly one cell marked with the letter `C`, which represents the child's position.  
Mom starts at the top-left cell `(1,1)` and wants to reach the child with the **minimum total cost**.

---

## Movement Rules
1. Mom can move **up, down, left, or right** (no diagonal moves).  
2. The $k$-th step (0-indexed) has a **parity**:
   - If $k$ is even, entering cell $(i,j)$ costs its **even cost**.  
   - If $k$ is odd, entering cell $(i,j)$ costs its **odd cost**.  
3. Let $d(i,j)$ be the Manhattan distance from `(1,1)` to `(i,j)`.  
   - Mom can move into cell $(i,j)$ at step $k$ **only if**:

\[
d(i,j) \bmod 100 = (k \bmod 100)
\]

4. Visiting the **same cell multiple times is allowed**, but **each visit requires paying its cost again** according to the parity of that step.

---

## Task
Determine the minimum cost Mom must pay to reach the child.  
If it is impossible, print `-1`.

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
