# Problem: The Shifting Labyrinth

You are standing on a line of cells numbered from 1 to N.  
Initially, you are at cell 1, and you want to reach cell N.

From a cell `x`, you can move according to the following rule:

- Let `d = the last digit of x`.  
- You may move to:
  - `x + d`, or  
  - `x − d`, if that cell exists (within [1, N]).

The cost of a move depends on your destination cell `y`:

- If `y` is prime, the cost is `d²`.  
- Otherwise, the cost is `d`.

Your task is to find the minimum total cost required to reach cell `N` from cell `1`, or report that it is impossible.

---

## Input
The first line contains an integer `T` — the number of test cases.  
Each of the next `T` lines contains a single integer `N` (`2 ≤ N ≤ 10^6`).  

It is guaranteed that the sum of `N` over all test cases does not exceed `10^6`.

---

## Output
For each test case, print a single integer — the minimum cost to reach cell `N` from cell `1`.  
If it is impossible, print `-1`.

---

## Examples

### Input
