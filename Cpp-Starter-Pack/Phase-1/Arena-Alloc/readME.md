```markdown
# arena-alloc

Small, focused implementation of a bump/arena allocator in C++. The goal is to provide a lightweight allocation strategy for short-lived allocations and bulk free semantics.

Features:
- Bump pointer allocator with an arena that can be reset for fast bulk freeing.
- Optional free list to recycle recently freed blocks.
- Simple, well-documented API and unit tests.

Learning outcomes:
- Understand allocation strategies, fragmentation trade-offs, and tradeoffs versus `malloc`/`new`.
- Design clear safety boundaries for lifetime management and ownership.

Build & run (example):
```sh
g++ -std=c++17 -O2 -o arena-test tests.cpp allocator.cpp
./arena-test
```

Usage tips:
- Use arenas for short-lived objects in tight loop or when you need deterministic deallocation time.
- Provide thorough unit tests that exercise allocation sizes, alignment behavior, and reset semantics.
```
