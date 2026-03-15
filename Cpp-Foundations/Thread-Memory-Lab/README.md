# Thread-Memory-Lab

Creates multiple processes each spawning multiple threads, then prints how global, static, local, and heap variables behave across both boundaries. Run it several times and observe what changes and what stays the same.

## Features

- fork() creates child processes, each of which spawns several pthreads.
- Each thread reports the value and address of a global, a static local, a stack variable, and a heap allocation.
- Output is designed to make address space isolation and shared memory visible at a glance.

## Learning outcomes

- Understand why two processes have separate copies of globals while two threads in the same process share them.
- See address space isolation in practice: fork gives each child its own virtual address space.
- Observe nondeterministic scheduling — thread print order changes between runs.
- Identify which variables are safe to read across threads without synchronization and which are not.

## Build & run

g++ -std=c++17 -pthread -O2 -o thread-memory-lab main.cpp
./thread-memory-lab

## Build it when

- You can explain why two threads incrementing the same global without synchronization produces different results every run.

## Notes

- Run the binary at least five times and compare outputs. Notice which addresses and values are consistent and which are not.
