# Thread-Task-Dispatcher

Spawns N threads and gives each one a struct containing its own index and input value. Collects results without using globals. A focused demonstration of the loop-variable aliasing bug and how to avoid it.

## Features

- Dispatch N threads, each receiving a unique task struct (index + input) via pthread_create().
- Each thread writes its result into a per-task slot, eliminating the need for global shared state.
- Intentionally demonstrate the loop-variable aliasing bug (passing &i from a loop) alongside the correct fix.

## Learning outcomes

- Pass arguments to threads safely using heap-allocated or array-backed structs instead of raw loop-variable addresses.
- Understand why &i from a for loop is dangerous: the variable is mutated before the thread reads it.
- Use pthread_join() correctly to collect all results before the main thread exits.
- Design thread data to avoid shared mutable state from the start.

## Build & run

g++ -std=c++17 -pthread -O2 -o thread-task-dispatcher main.cpp
./thread-task-dispatcher

## Build it when

- You understand why the address of a loop variable is unsafe to pass to a thread, and can describe exactly when the race happens.

## Notes

- Add a deliberate buggy version that passes &i, run it many times, and observe the nondeterministic output before switching to the struct-based fix.
