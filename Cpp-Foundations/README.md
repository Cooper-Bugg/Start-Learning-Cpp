# Cpp Foundations

Practice repository containing small C++ programs focused on core language and systems concepts.

## Overview

Each folder in this repository is a focused micro-project designed to reinforce specific C++ concepts and runtime behavior.

## Projects

More detail about each project will be added as they are completed. See the project's own README for build steps and learning outcomes.

- **POSIX-Pipeline** — Unix-style process and thread behavior: `fork()`, POSIX threads, `exec()`, and parent/child coordination.

- **Mini-CLI-Calc** — Incremental calculator demonstrating control flow, function dispatch, operation tables, and input validation.

- **File-Stat-Tool** — Command-line utility to report file size, line count, word count, and byte frequency distribution.

- **Binary-Inspector** — Displays binary/hex representations of numeric values and floating-point decomposition (sign/exponent/mantissa).

- **Struct-Based-Data-Logger** — Simple structured data recorder demonstrating struct design and file serialization.

- **Fork-Tree-Visualizer** — Traces the process tree produced by a sequence of fork() calls and prints each process with its PID, PPID, and which fork() created it.

- **Thread-Memory-Lab** — Creates multiple processes each spawning multiple threads, then prints how global, static, local, and heap variables behave across both boundaries.

- **Thread-Task-Dispatcher** — Spawns N threads and gives each one a struct with its own index and input. Demonstrates the loop-variable aliasing bug and how to avoid it.

- **Process-Pipeline** — A three-stage concurrent pipeline using POSIX message queues: sender, processor, and logger running concurrently via fork().

- **Token-Scanner** — Reusable TokenScanner class that breaks an input string into typed tokens: numbers, words, operators, and punctuation.

- **Recursion-Warmups** — Two short recursive programs (Towers of Hanoi and permutation generator) to build backtracking intuition before maze-solver and expression-tree.

- **Expression-Tree** — Parses a mathematical expression string into a binary expression tree and evaluates it recursively with correct operator precedence.

## Build / Usage

See each project folder for build instructions and examples.

## License

Add license information here.
