# tick-scheduler

Cooperative, tick-driven scheduler in C++ for running periodic tasks in a deterministic simulation or host-side test harness.

## Features

- Register periodic tasks with fixed intervals and priorities.
- Mockable time source for deterministic unit tests.
- Simple API for adding, removing, and inspecting scheduled tasks.

## Learning outcomes

- Explore scheduling models and trade-offs between cooperative and preemptive scheduling.
- Write deterministic tests by advancing a mock tick counter.

## Build & run

g++ -std=c++17 -O2 -o tick-scheduler main.cpp scheduler.cpp
./tick-scheduler

## Build it when

- You have finished uart-sim and virtual-i2c and need a scheduling layer to coordinate their interactions.

## Notes

- Start with a simple tick loop and add task registration and drift compensation as needed.
