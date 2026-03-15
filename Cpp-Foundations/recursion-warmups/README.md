# recursion-warmups

Two short recursive programs to build intuition before tackling maze-solver and expression-tree. Do not skip these — they are the reps that make the harder projects feel natural.

## towers-of-hanoi

Solve the Towers of Hanoi puzzle for N disks and print every move.

### Features

- Print each move as Move disk N from peg A to peg C.
- Count total moves and verify it matches the known formula 2^N - 1.
- Configurable number of disks via command-line argument.

### Learning outcomes

- Internalize the leap of faith: trust that the recursive call correctly moves N-1 disks without tracing every step.
- Understand that some problems have no clean iterative solution — the recursion is the algorithm.
- Count the calls and verify the exponential growth matches theory.

### Build & run

g++ -std=c++17 -O2 -o hanoi hanoi.cpp
./hanoi 4

## permutation-generator

Print all permutations of a string in lexicographic order.

### Features

- Generate all N! permutations of an input string.
- Print them one per line in sorted order.
- Handle duplicate characters by generating only unique permutations.

### Learning outcomes

- See the choose/explore/unchoose pattern in its clearest form before applying it to mazes and Sudoku.
- Understand why the number of recursive calls grows as N! and what that means for large inputs.
- Practice swapping and unswapping in place rather than allocating new strings at each level.

### Build & run

g++ -std=c++17 -O2 -o permutations permutations.cpp
./permutations abc

## Build it when

- You are about to start maze-solver. These two programs together take 1-2 hours and will make the backtracking pattern click before the maze's coordinate system adds complexity.

## Notes

- For Hanoi: try N=1, N=2, N=3 on paper first and count moves. The recursive structure becomes obvious at N=3.
- For permutations: trace what happens with input "ab" on paper before coding. Two permutations, two leaves on the recursion tree.
