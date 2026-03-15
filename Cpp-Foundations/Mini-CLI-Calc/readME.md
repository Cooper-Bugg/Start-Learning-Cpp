```markdown
# Mini-CLI-Calc

Minimal command-line calculator implemented in C++ to demonstrate parsing, control flow, and a small operation-dispatch table. This project is intended as an incremental exercise: start with integer operations, then add floating-point support, operator precedence, and expression parsing.

Features:
- REPL (read–eval–print loop) mode and single-expression invocation.
- Basic arithmetic (+, -, *, /), with optional integer and floating-point modes.
- Modular operator dispatch so new operations (bitwise, trig, etc.) can be added.
- Input validation and user-friendly error messages.

Learning outcomes:
- Parse and validate user input safely in C++.
- Design a small, testable API for expression evaluation.
- Incrementally extend functionality (variables, functions, precedence parsing).

Build & run (example):
```sh
g++ -std=c++17 -O2 -o minicli main.cpp
./minicli           # starts REPL
./minicli "2+2*3"  # evaluate single expression
```

Usage tips:
- Start by implementing tokenization and basic binary op evaluation.
- Add unit tests for edge cases: divide-by-zero, large integers, malformed input.

Notes:
- This project is great for practicing incremental feature development: add one feature at a time and keep tests passing.
```
