# Mini-CLI-Calc

Minimal command-line calculator in C++ demonstrating parsing, control flow, and a small operation-dispatch table. Start with integer operations, then add floating-point support, operator precedence, and expression parsing incrementally.

## Features

- REPL (read-eval-print loop) mode and single-expression invocation.
- Basic arithmetic (+, -, *, /) with optional integer and floating-point modes.
- Modular operator dispatch so new operations (bitwise, trig, etc.) can be added.
- Input validation and user-friendly error messages.

## Learning outcomes

- Parse and validate user input safely in C++.
- Design a small, testable API for expression evaluation.
- Incrementally extend functionality: variables, functions, precedence parsing.

## Build & run

g++ -std=c++17 -O2 -o minicli main.cpp
./minicli           # starts REPL
./minicli "2+2*3"  # evaluate single expression

## Notes

- Start by implementing tokenization and basic binary op evaluation.
- Add unit tests for edge cases: divide-by-zero, large integers, malformed input.
