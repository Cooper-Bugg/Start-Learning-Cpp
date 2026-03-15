# bakery-buffer

Producer-consumer system with a bounded circular buffer. Multiple producer threads generate items, multiple consumers remove them. Synchronized with one mutex and two condition variables. No race conditions, no deadlocks, clean termination.

## Features

- Bounded circular buffer shared between N producer threads and M consumer threads.
- One mutex guards all buffer state; two condition variables signal "not full" and "not empty".
- Producers block when the buffer is full; consumers block when it is empty.
- Clean shutdown: producers signal done, consumers drain remaining items, all threads join.

## Learning outcomes

- Use pthread_mutex_t and pthread_cond_t to protect a shared data structure.
- Understand the difference between pthread_cond_wait() (releases the mutex while waiting) and a busy-wait loop.
- Design a circular buffer with head/count tracking instead of head/tail pointers to avoid the empty-vs-full ambiguity.
- Implement clean thread shutdown without data loss or deadlock.

## Build & run

g++ -std=c++17 -pthread -O2 -o bakery-buffer main.cpp
./bakery-buffer

## Build it when

- You can draw the buffer state machine (empty, partial, full) and label every transition before touching the keyboard.
