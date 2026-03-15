# expression-tree

Parses a mathematical expression string into a binary expression tree and evaluates it recursively. A direct upgrade to Mini-CLI-Calc that adds operator precedence, parentheses, and a clean separation between parsing and evaluation.

## Features

- Parse infix expressions like 3 + 4 * 2 and (1 + 2) * (3 - 4) into a tree.
- Evaluate the tree recursively: leaf nodes are numbers, internal nodes are operators.
- Print the tree as a visual structure showing operator hierarchy.
- Support +, -, *, / with correct precedence and parentheses.
- Optional: add variables and a symbol table for expressions like x * 2 + 1.

## Learning outcomes

- See how recursive descent parsing maps directly onto a recursive data structure.
- Understand why a tree naturally encodes operator precedence without extra logic at evaluation time.
- Practice building and traversing a tree with recursive functions rather than loops.
- Appreciate how separating parsing from evaluation makes both halves simpler and testable independently.

## Build & run

g++ -std=c++17 -O2 -o expression-tree main.cpp
./expression-tree "3 + 4 * 2"

- ./expression-tree "3 + 4 * 2" — evaluates to 11, prints tree showing * binds tighter than +.
- ./expression-tree "(3 + 4) * 2" — evaluates to 14.

## Build it when

- You have finished token-scanner and maze-solver, and you can draw the correct expression tree for 1 + 2 * 3 - 4 on paper with the right precedence before writing any parsing code.

## Notes

- Use token-scanner from the previous project as your lexer — this is exactly why you built it.
- Test with: single numbers, all four operators, nested parentheses, negative results, and divide-by-zero.
- If you get stuck on precedence, look up recursive descent parsing — the grammar rules map directly to mutually recursive functions.
