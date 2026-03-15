# Fork-Tree-Visualizer

Traces the process tree produced by a sequence of fork() calls and prints each process with its PID, PPID, and which fork() created it. Forces you to reason about execution paths on paper before writing a single line of code.

## Features

- Execute a configurable sequence of fork() calls and record the resulting tree.
- Each process prints its PID, PPID, and which fork() invocation created it.
- Visualize the full tree so you can compare predicted vs. actual output.

## Learning outcomes

- Understand how fork() duplicates the calling process and splits execution into two paths.
- Reason about short-circuit evaluation (&&, ||) across process boundaries.
- Use getpid(), getppid(), and wait() correctly to reap children without zombies.
- Build a mental model of process tree construction before reading or writing fork()-heavy code.

## Build & run

g++ -std=c++17 -O2 -o fork-tree main.cpp
./fork-tree

## Build it when

- You can predict the output of fork() && fork() || fork() on paper and explain how many processes are created and why.

## Notes

- Never run fork()-loop experiments outside a controlled context — accidentally forking without a termination condition can fork-bomb the machine.
