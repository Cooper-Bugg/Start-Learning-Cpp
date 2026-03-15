```markdown
# virtual-i2c

Virtual I2C bus and register-mapped sensor device models for host-side testing. Useful for building integration tests for drivers without hardware.

Features:
- Emulate I2C transactions (start/stop, read/write) and basic timing semantics.
- Create register-mapped virtual devices with configurable behavior (read-only, writable, simulated sensor values).
- Host-side API for driving bus transactions and injecting errors.

Learning outcomes:
- Understand I2C semantics and how register-mapped devices are typically organized.
- Build robust drivers by exercising edge cases (NACKs, timeouts) in a controlled environment.

Build & run (example):
```sh
g++ -std=c++17 -O2 -o virtual-i2c main.cpp
./virtual-i2c --demo
```

Notes:
- Keep timing models simple for easier deterministic tests; allow optional randomized timing for stress tests.
```
