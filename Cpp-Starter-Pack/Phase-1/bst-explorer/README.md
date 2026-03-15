# bst-explorer

Binary search tree implementation with insert, search, delete, and all three traversals. Includes a balance checker and a visualization that prints the tree structure to the terminal. The foundational tree project before moving to maps and sets.

## Features

- Insert, search, and delete nodes with correct BST ordering maintained.
- Inorder, preorder, and postorder traversals printed to stdout.
- Tree height and balance factor computation.
- Terminal visualization showing tree structure with indentation.
- Optional: implement a simple AVL or height-balanced insertion to see self-balancing in action.

## Learning outcomes

- Implement recursive tree algorithms: every BST operation is naturally recursive.
- Understand why inorder traversal of a BST produces sorted output.
- Learn the three deletion cases: leaf node, one child, two children — the two-child case is the hard one.
- See how an unbalanced tree degrades to O(n) search and why balanced trees matter.

## Build & run

g++ -std=c++17 -O2 -o bst-explorer main.cpp
./bst-explorer

- Insert 5 3 7 1 4 6 8 and observe the inorder traversal prints 1 3 4 5 6 7 8.
- Delete 3 and verify the tree restructures correctly with the inorder still sorted.

## Build it when

- You can draw the BST produced by inserting 5 3 7 1 4 on paper, label all three traversal orders, and describe all three deletion cases before writing any code.

## Notes

- Use raw pointers first to understand ownership. Optionally refactor to unique_ptr afterward and observe how it changes deletion logic.
- Test deletion of: a leaf, a node with one child, a node with two children, and the root node.
- Print the tree after every insert and delete during testing so you can verify structure visually.
