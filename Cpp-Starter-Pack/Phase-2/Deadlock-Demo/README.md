# deadlock-demo

Two threads acquire two mutexes in opposite order, causing an occasional hang. Demonstrates the deadlock, then fixes it with consistent lock ordering. Includes a monitor thread that detects when no progress has been made and prints a warning.

## Features

- Buggy version: Thread A locks mutex1 then mutex2; Thread B locks mutex2 then mutex1 — circular wait causes occasional deadlock.
- Fixed version: both threads acquire mutexes in the same order, eliminating the circular wait.
- Monitor thread tracks a progress counter; if it stops incrementing for a configurable timeout, prints a deadlock warning.

## Learning outcomes

- Identify circular wait as the Coffman condition that consistent lock ordering eliminates.
- Understand all four Coffman conditions: mutual exclusion, hold-and-wait, no preemption, circular wait.
- Distinguish liveness (progress eventually happens) from safety (nothing bad happens).
- Build a simple monitor thread that detects stalls without modifying the threads under observation.

## Build & run

g++ -std=c++17 -pthread -O2 -o deadlock-demo main.cpp
./deadlock-demo          # run the buggy version; may hang
./deadlock-demo --fixed  # run the corrected version

## Build it when

- You can name all four Coffman conditions from memory and identify which one consistent lock ordering eliminates.
