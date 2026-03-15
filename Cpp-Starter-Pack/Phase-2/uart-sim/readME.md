```markdown
# uart-sim

UART device simulator implemented in C++ to model framing, baud rate timing, simple parity/CRC, and configurable noise/error injection for host-side testing of serial protocols.

Features:
- Frame building/parsing with start/stop bits and optional parity.
- Simulated timing and configurable noise/error patterns.
- Test harnesses to exercise protocol implementations under error conditions.

Learning outcomes:
- Understand serial framing and common error models.
- Build robust parsers that tolerate noise and partial frames.

Build & run (example):
```sh
g++ -std=c++17 -O2 -o uart-sim main.cpp
./uart-sim --baud 115200 --noise 0.01
```

Notes:
- Use this simulator to drive integration tests for serial-based bootloaders, device protocols, or logging systems.
```
