```markdown
# mini-drivers

Small collection of bare-metal-style driver examples (GPIO, UART, SPI, I2C) accompanied by host-side test stubs. These are structured as educational pieces to learn hardware abstraction without requiring physical devices.

Features:
- Minimal driver APIs illustrating initialization, read/write, and interrupt or polling modes.
- Host-side stubs and simulators to exercise drivers during development.
- Documentation about platform-specific considerations and portability.

Learning outcomes:
- Learn how to design small, testable driver interfaces and separate platform-specific code.
- Understand common peripheral patterns and error handling strategies.

Build & run (example):
```sh
g++ -std=c++17 -O2 -o mini-drivers tests.cpp gpio.cpp uart.cpp
./mini-drivers --run-host-tests
```

Notes:
- Keep hardware-dependent code isolated behind clear abstraction layers so it can be replaced with mocks or simulators.
```
