```markdown
# hexdump-lite

Simple C++ byte-level file viewer that prints offsets, hex bytes, and ASCII columns similar to common `hexdump` tools. Designed as a small exercise in formatting and robust file reading.

Features:
- Hex + ASCII side-by-side output with configurable bytes-per-line.
- Options to display 32/64-bit aligned offsets and grouped bytes.
- Safe handling of binary files and large inputs.

Learning outcomes:
- Practice formatted output, efficient file reads, and platform-consistent newline/encoding handling.
- Implement flexible CLI arguments and provide clear usage help.

Build & run (example):
```sh
g++ -std=c++17 -O2 -o hexdump-lite main.cpp
./hexdump-lite image.bin
```

Usage examples:
- `./hexdump-lite -n 16 firmware.bin` — show 16 bytes per line with ASCII.

Notes:
- Keep the implementation small and test with both text and binary inputs to verify output clarity.
```
