# The Ancestral Passage

In the land of Veridia, a guardian must traverse a sacred mosaic to reach a lost heirloom. The mosaic is laid out as an $ n \times m $ array of tiles, each inscribed with a sigil from an ancient alphabet (represented by uppercase letters). The guardian bears the mark of a specific lineage—denoted by a single uppercase letter $ x $—and may only step on tiles that bear that same sigil. One unique tile is marked with the symbol **C**, indicating the resting place of the heirloom.

The guardian begins at the upper-leftmost tile (position indexed as row 1, column 1). Each time they move to an adjacent tile (up, down, left, or right), they must pay a toll that depends on two factors:

1. **The rhythm of their journey**: The toll alternates based on whether the number of moves already taken is even or odd (counting from zero). That is, the very first tile entered after the start (i.e., the first move) uses the “odd-phase” toll, the next uses “even-phase,” and so on.
2. **The resonance of the destination**: Each tile has two preassigned toll values—one for even-phase arrivals and one for odd-phase arrivals.

However, the spirits of the mosaic enforce a deeper law: the guardian may only enter a tile at a move count $ k $ if the tile’s **proximity index** matches the current rhythm modulo 100. The proximity index of a tile at position $ (i, j) $ is defined as $ (i - 1) + (j - 1) $—that is, the minimal number of steps needed to reach it from the origin in an unrestricted grid.

The guardian may revisit tiles, but each visit incurs the full toll dictated by the phase of that particular arrival.

Your task: compute the least total toll the guardian must pay to reach the **C** tile while obeying all ancestral laws. If no such passage exists, return `-1`.

## Input Format

- First line: integers $ n $ and $ m $ ($ 2 \leq n, m \leq 1000 $)
- Second line: the guardian’s lineage sigil $ x $ (uppercase letter)
- Next $ n $ lines: the mosaic layout (each line is a string of $ m $ uppercase letters; exactly one **C**)
- Next $ n $ lines: even-phase tolls (each line has $ m $ integers)
- Next $ n $ lines: odd-phase tolls (each line has $ m $ integers)

## Output

A single integer: the minimal total toll, or `-1` if the heirloom is unreachable under the rules.

## Notes

- Movement is allowed only to orthogonally adjacent tiles (no diagonals).
- The starting tile (1,1) is entered at move count $ k = 0 $, so its cost is taken from the *even-phase* toll table.
- The constraint $ \text{proximity\_index}(i,j) \bmod 100 = k \bmod 100 $ must hold for every visit to cell $ (i,j) $ at step $ k $.
- Revisiting cells is permitted but incurs cost each time, according to the step’s parity and the modular constraint.
