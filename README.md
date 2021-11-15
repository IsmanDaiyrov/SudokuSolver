# Sudoku Solver

A program to solve any Sudoku puzzle in under 1 second.

## What is Sudoku?

>*Sudoku is a logic-based, combinatorial number-placement puzzle. The objective is to fill a 9×9 grid with digits so that each column, each row, and each of the nine 3×3 sub-grids that compose the grid (also called "boxes") contains all of the digits from 1 to 9. (Source [Wikipedia](https://en.wikipedia.org/wiki/Sudoku))*

## Example

```java
int[][] board = {
           {7, 0, 2, 0, 5, 0, 6, 0, 0},
           {0, 0, 0, 0, 0, 3, 0, 0, 0},
           {1, 0, 0, 0, 0, 9, 5, 0, 0},
           {8, 0, 0, 0, 0, 0, 0, 9, 0},
           {0, 4, 3, 0, 0, 0, 7, 5, 0},
           {0, 9, 0, 0, 0, 0, 0, 0, 8},
           {0, 0, 9, 7, 0, 0, 0, 0, 5},
           {0, 0, 0, 2, 0, 0, 0, 0, 0},
           {0, 0, 7, 0, 4, 0, 2, 0, 3}
        };
```
## Output
```java
732|458|619
956|173|824
184|629|537
-----------
871|564|392
643|892|751
295|317|468
-----------
329|786|145
418|235|976
567|941|283
```

## Backtracking
This Java program uses a backtracking algorithm which is brute-force.

The algorithm takes the first valid value and goes on with this approach until the puzzle is solved or there is no more valid value left. If there is no more valid value left (but the puzzle is not solved yet) it tracks back to the last known valid value and tries another value.

That way the algorithm will always find a valid solution unless the initially provided puzzle is invalid! It will even fill an empty puzzle (with no pre-filled cells at all) which makes it also ideal to be used to generate new.
