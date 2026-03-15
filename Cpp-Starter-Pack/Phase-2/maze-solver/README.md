# maze-solver

Recursive backtracking maze solver that reads a 2D maze from a text file, finds a path from start to finish, and prints the solved maze with the path marked. The first serious recursive project — do not start it until you can trace the call stack on paper.

## Features

- Load mazes from plain text files using # for walls, . for open paths, S for start, E for exit.
- Solve using recursive backtracking: explore a direction, recurse, undo if it leads to a dead end.
- Print the solved maze with the solution path marked using *.
- Report number of steps in the solution and cells visited during search.
- Optional: animate the search step by step with a configurable delay.

## Learning outcomes

- Internalize recursive backtracking as a pattern: choose, explore, unchoose.
- Understand why the call stack is the implicit data structure — no explicit stack needed.
- See the difference between a dead end (backtrack) and a solution (unwind successfully).
- Practice recursive thinking on a problem with a clear visual output you can verify by eye.

## Build & run

g++ -std=c++17 -O2 -o maze-solver main.cpp
./maze-solver maze.txt

- ./maze-solver maze.txt — solve and print the maze with path marked.
- ./maze-solver --animate maze.txt — show the search expanding step by step.

## Build it when

- You can trace by hand what happens when the solver hits a dead end in a 3x3 maze and explain exactly which calls return and in what order before writing any code.

## Notes

- Start with a hardcoded 5x5 maze before adding file loading.
- Write at least three test mazes: one with a single solution, one with multiple paths (verify it finds one), and one with no solution.
- Do not use a global visited array — pass state through the recursion or mark/unmark the maze in place.
