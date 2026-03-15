```markdown
# grep-lite

Lightweight C++ implementation of a substring search utility inspired by Unix `grep`. Focuses on streaming input, simple option parsing, and performance-conscious scanning.

Features:
- Search for literal substrings across files or stdin.
- Options for case-insensitive search and line-numbered output.
- Streaming mode to handle large files without full buffering.

Learning outcomes:
- Implement efficient scanning for text data and learn I/O buffering strategies.
- Design a small CLI with positional arguments and flags.
- Write tests that confirm correctness and basic performance characteristics.

Build & run (example):
```sh
g++ -std=c++17 -O2 -o grep-lite main.cpp
./grep-lite -n "TODO" src/*.cpp
```

Usage tips:
- Start with a simple linear scan per line, then optimize by using memmem or custom search algorithms if needed.
- Add unit tests for case-insensitive matches and multi-line edge cases.
```
