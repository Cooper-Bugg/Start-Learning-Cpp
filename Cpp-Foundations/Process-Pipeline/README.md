# Process-Pipeline

A three-stage concurrent pipeline using POSIX message queues. A sender pushes work onto a named queue, a processor picks it up and simulates slow work, and a logger receives the output. All three stages run concurrently via fork().

## Features

- Three independent processes (sender, processor, logger) communicate through named POSIX message queues.
- Sender generates work items and pushes them onto the first queue.
- Processor dequeues items, simulates work, and forwards results to the second queue.
- Logger receives processed results and records them.
- Clean process shutdown and queue unlink on exit.

## Learning outcomes

- Use mq_open(), mq_send(), mq_receive(), and mq_unlink() to build inter-process communication without shared memory.
- Design struct-based message layouts for typed IPC.
- Understand blocking behavior: a receiver blocks when the queue is empty, a sender blocks when it is full.
- Coordinate multi-process cleanup so queues are unlinked exactly once.

## Build & run

g++ -std=c++17 -O2 -o process-pipeline main.cpp -lrt
./process-pipeline

## Build it when

- You can get two processes exchanging messages through a named queue reliably before adding the third stage.

## Notes

- POSIX message queues require Linux or macOS. On macOS, mq_* support is present but check system limits with sysctl kern.mqueue.
