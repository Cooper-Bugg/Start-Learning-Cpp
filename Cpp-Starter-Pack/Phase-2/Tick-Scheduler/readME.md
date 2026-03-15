```markdown
# tick-scheduler

Cooperative, tick-driven scheduler implemented in C++ for running periodic tasks in a deterministic simulation or host-side test harness.

Features:
- Register periodic tasks with fixed intervals and priorities.
- Mockable time source for deterministic unit tests.
- Simple API for adding, removing, and inspecting scheduled tasks.

Learning outcomes:
- Explore scheduling models and trade-offs between cooperative and preemptive scheduling.
- Write deterministic tests by advancing a mock tick counter.

Build & run (example):
```sh
g++ -std=c++17 -O2 -o tick-scheduler main.cpp scheduler.cpp
./tick-scheduler
```

Usage tips:
- Start with a simple tick loop and add task registration and drift compensation as needed.
```
