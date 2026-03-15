# sudoku-solver

Recursive backtracking Sudoku solver that reads a puzzle from a text file, solves it, and prints the completed board. A step up from maze-solver in constraint complexity — the same backtracking pattern applied to a harder search space.

## Features

- Load puzzles from a plain text file with 0 representing empty cells.
- Solve using recursive backtracking with constraint checking: only place a digit if it is valid in that row, column, and 3x3 box.
- Print the board before and after solving with clean formatting.
- Report number of recursive calls made to give a sense of search space size.
- Optional: detect and report unsolvable puzzles cleanly rather than hanging.

## Learning outcomes

- Recognize backtracking as a general pattern: the same structure from maze-solver applies here with a different constraint function.
- Understand how constraint propagation reduces the search space — checking validity before recursing prunes dead branches early.
- Practice designing a clean isValid() function that is called thousands of times and must be correct and fast.
- See how problem representation affects solution elegance: a flat 81-cell array vs a 9x9 grid.

## Build & run

g++ -std=c++17 -O2 -o sudoku-solver main.cpp
./sudoku-solver puzzle.txt

- ./sudoku-solver easy.txt — solve and print a simple puzzle.
- ./sudoku-solver hard.txt — observe the jump in recursive calls versus an easy puzzle.

## Build it when

- You finished maze-solver and can explain without looking at code why backtracking works: what gets undone when you backtrack, and why the recursion terminates.

## Notes

- Start with a hardcoded easy puzzle before adding file loading.
- Write tests for: a puzzle with one solution, a puzzle with no solution, and an already-completed valid board.
- The choose/explore/unchoose pattern is identical to maze-solver. If that pattern is not yet second nature, go back and re-read maze-solver before starting this.
