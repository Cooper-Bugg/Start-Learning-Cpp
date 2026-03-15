# page-fault-sim

Simulates FIFO and LRU page replacement for any reference string and frame count. After each reference it prints current frame contents and hit or fault status. Tracks total fault counts and compares both algorithms at the end.

## Features

- Accept any reference string and frame count as input — not hardcoded to one scenario.
- Simulate FIFO (first-in first-out eviction) and LRU (least recently used eviction) independently.
- Print frame state after every page reference so you can trace the algorithm step by step.
- Report total fault counts and a side-by-side comparison of both algorithms.

## Learning outcomes

- Implement FIFO using a queue and LRU using an ordered-access tracker.
- Understand hit/fault detection: a hit means the page is already in a frame, a fault means it must be loaded.
- See how frame count affects fault rate and compare the two algorithms across multiple inputs.
- Generalize a paper hand-trace problem into working, reusable code.

## Build & run

g++ -std=c++17 -O2 -o page-fault-sim main.cpp
./page-fault-sim

## Build it when

- You can trace 1 2 3 4 2 1 5 6 2 1 2 3 7 6 3 2 1 2 3 6 with 3 frames for both FIFO and LRU on paper and get the correct fault counts before touching the keyboard.
