# RTOS-Demo

Minimal RTOS demonstration application showing tasks, message queues, and basic synchronization primitives as C++ implementations of embedded concurrency concepts.

## Features

- Example tasks that communicate via queues and semaphores.
- Simple scheduler integration and instrumentation hooks.
- Host-targetable versions: simulation on the host and a minimal port stub for embedded targets.

## Learning outcomes

- Understand task lifecycle, inter-task communication, and common concurrency pitfalls.
- Learn how to structure RTOS-based applications with testable components.

## Build & run

g++ -std=c++17 -O2 -pthread -o rtos-demo main.cpp
./rtos-demo --simulate

## Build it when

- You have finished tick-scheduler and bakery-buffer and can explain what preemptive scheduling is and how it differs from the cooperative tick model.

## Notes

- This project is a conceptual demonstration — for production use, study a full RTOS API such as FreeRTOS or Zephyr.
- Keep the host simulation path working at all times so you can test without hardware.
