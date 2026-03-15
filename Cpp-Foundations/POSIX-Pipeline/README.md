# POSIX-Pipeline

Educational C++ exercises demonstrating Unix process and thread primitives: fork(), exec() variants, pipes, and POSIX threads.

## Features

- Create pipelines using pipe() and fork() plus dup2() for stdin/stdout redirection.
- Launch external programs via execvp() and observe exit statuses.
- Compare process-based isolation (fork) with thread-based concurrency (pthread).
- Demonstrate common pitfalls: zombie processes, deadlocks, signal handling.

## Learning outcomes

- Understand address space separation between processes and shared memory in threads.
- Learn how to set up pipes and redirect file descriptors safely.
- Learn basic signal handling and child process reaping techniques (waitpid).

## Build & run

g++ -std=c++17 -pthread -O2 -o posix-pipeline main.cpp
./posix-pipeline

## Notes

- This project uses POSIX APIs and requires Linux, macOS, or WSL/MSYS2. Running natively on Windows without a POSIX compatibility layer requires porting.
- Be careful when experimenting with fork() in loops — accidentally forking too many children can overwhelm the system.
- Include scripted tests that run example pipelines and verify expected output and exit codes.
