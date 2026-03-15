```markdown
# asm-helpers

Small collection of portable helpers that use inline assembly where necessary for timing, atomic primitives, or CPU feature detection (e.g., CPUID). Emphasis is on safe usage and documented fallbacks.

Features:
- High-resolution timing helpers using architecture features when available.
- Small atomic/lock primitives demonstrating memory barriers and ordering.
- CPUID wrappers and feature-detection utilities with safe fallbacks.

Learning outcomes:
- Learn how and when to use inline assembly safely in C++ code.
- Document portability concerns and provide non-asm fallbacks.

Build & run (example):
```sh
g++ -std=c++17 -O2 -o asm-helpers main.cpp
./asm-helpers --probe
```

Notes:
- Keep assembly code minimal and well-commented; prefer compiler intrinsics when available.
```
