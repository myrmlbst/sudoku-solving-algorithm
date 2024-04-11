# sudoku-solving-algorithm

## Rules of Sudoku:
Sudoku is a puzzle game where the player must input numbers from 0-9 in a 9x9 grid so that no two numbers in a horizontal or vertical sequence appear twice. Inside the 9x9 grid are 9 smaller sub-grids (3x3) where, again, no two numbers must appear more than once.

* Each game of sudoku only has **one unique, valid solution**.

## Recursive Backtracking Algorithm:
We are meant to modify/solve the board, rather than return it as a solved copy.

_**The Main() function**_ contains a test case to ensure that the algorithm performs the game properly and returns a correctly filled-out board. We keep track of the numbers being used in each row, column, and cell to make sure that there are no repeating digits via an array of bitsets.
