```markdown
# spsc-ring

Single-producer single-consumer ring buffer library implemented in C++ with a simple, well-documented API. Useful for passing data between threads or processes with minimal synchronization.

Features:
- Lock-free (or minimal-lock) ring buffer for single-producer/single-consumer use.
- Optional blocking wrapper to wait for data or space availability.
- Unit tests and microbenchmarks.

Learning outcomes:
- Understand memory ordering, atomic operations, and correctness conditions for SPSC queues.
- Measure throughput and latency trade-offs for different implementations.

Build & run (example):
```sh
g++ -std=c++17 -O2 -pthread -o spsc-tests tests.cpp ring.cpp
./spsc-tests
```

Notes:
- Provide clear guarantees in the API documentation (e.g., which operations are lock-free, required memory ordering semantics).
```
