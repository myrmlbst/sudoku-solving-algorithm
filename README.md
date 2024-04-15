# sudoku-solving-algorithm

## Rules of Sudoku:
Sudoku is a Japanese puzzle game where the player must input numbers from 0-9 in a 9x9 grid so that no two numbers in a horizontal or vertical sequence appear twice. Inside the 9x9 grid are 9 smaller sub-grids (3x3) where, again, no two numbers must appear more than once.

Sudokus can have multiple solutions or only one unique solution based on the initial starting clues and their positions in the grid. For this algorithm specifically, we consider that each game only has **one unique, valid solution**.

## Recursive Backtracking Algorithm:
We are meant to modify/solve the board, rather than return it as a solved copy. 

The _**main() function**_ contains a test case to ensure that the algorithm performs the game properly and returns a correctly filled-out board. We keep track of the numbers being used in each row, column, and cell to make sure that there are no repeating digits via an array of bitsets. 

In the __**Solve Class**__, we loop over the given board and mark out all the integers that were already given to us and the empty spaces that our algorithm is meant to fill out. 

The __**solve() function**__ contains the recursive function. The first thing we do is find a blank space that we can fill in and compute which numbers have already been used in each position. This leaves us with the numbers that could potentially be placed in the blank spaces. __Only then can the recursive backtracking start:__ an unused digit is placed on the board and is marked as been used in its corresponding row, column, and cell. Now, we recursively solve the problem; if solve is TRUE, we move on to the next step. If it is FALSE, we remove that digit that we used, and place another digit in its place instead. If none of the guesses for that position succeed, we set is as '.' (empty) and move on to a different position on the board. That cycle repeats until a solution is found.
