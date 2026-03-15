```markdown
# rtos-demo

Minimal RTOS demonstration application that shows tasks, message queues, and basic synchronization primitives. Intended as an educational port of RTOS concepts to small C++ examples.

Features:
- Example tasks that communicate via queues and semaphores.
- Simple scheduler integration and instrumentation hooks.
- Host-targetable versions: simulation on the host and a minimal port stub for embedded targets.

Learning outcomes:
- Understand task lifecycle, inter-task communication, and common concurrency pitfalls.
- Learn how to structure RTOS-based applications with testable components.

Build & run (example):
```sh
g++ -std=c++17 -O2 -pthread -o rtos-demo main.cpp
./rtos-demo --simulate
```

Notes:
- This project is intended as a conceptual demonstration; for production use, study a full RTOS API such as FreeRTOS or Zephyr.
```
