# Cpp Starter Pack

Curated, layered C++ exercises and small CLI tools designed to teach systems-level thinking, solid shipping habits, and clear documentation. Projects are grouped into progressive phases from quick beginner utilities to portfolio-level integrations.

## Purpose

- **Learn by shipping:** small, self-contained projects with clear goals and examples.
- **Progressive scope:** start with short CLI tools, then move to systems utilities, simulated embedded projects, and finally firmware-level or assembly tasks.
- **Portfolio-ready:** each phase contains at least one project that can be polished into a portfolio item.

## How to use this pack

- Pick a phase that matches your experience and time budget.
- Read the project's README inside its folder for build and test steps.
- Implement incrementally, commit small changes, and add usage examples to the project's README.

## Phases & Named Projects

Phase 0 — Foundations (Quick CLI utilities, 1–4 hours each)
- `hexdump-lite` — byte-level file viewer with offsets and ASCII column.
  - Goal: file I/O, formatting, command-line parsing.
- `tailf-lite` — follow a growing log file (like `tail -f`).
  - Goal: file seeking, event loops, cross-platform line handling.
- `grep-lite` — fast substring search across files with simple options.
  - Goal: streaming input, basic algorithmic performance.
- `unit-normalize` — unit parsing and normalization (e.g. `12.5kHz` → canonical value).
  - Goal: parsing, string handling, error reporting.
- `binhead` — simple binary-file header inspector (alignment, endianness checks).
  - Goal: binary parsing, safe I/O, basic validation tests.

Phase 1 — Core Systems (Libraries & utilities, 1–3 days each)
- `arena-alloc` — bump/arena allocator with optional free list and tests.
  - Goal: memory layout, allocator API design, unit tests.
- `spsc-ring` — single-producer single-consumer ring buffer library.
  - Goal: lock-free/polled data structures, performance measurements.
- `bit-tools` — bit-packed structures and a tiny bloom-filter experiment.
  - Goal: memory efficiency, bit operations, probabilistic data structures.
- `checksums` — CRC-16/CRC-32 implementations with test vectors and benchmarks.
  - Goal: bitwise algorithms, test harnesses, benchmark comparisons.

Phase 2 — Host-side Embedded Simulations (1–2 weeks each)
- `uart-sim` — UART device simulator with framing, configurable noise, and CRC error injection.
  - Goal: protocol framing, error cases, simulator harnesses for device testing.
- `tick-scheduler` — cooperative, tick-driven scheduler for periodic tasks.
  - Goal: scheduling models, mock time, deterministic unit tests.
- `virtual-i2c` — virtual I2C bus and register-mapped sensor devices for host testing.
  - Goal: device modeling, register semantics, integration tests.

Phase 3 — Firmware & Drivers (2+ weeks per project)
- `mini-drivers` — small bare-metal driver stack (GPIO, UART, SPI, I2C) with host-side test stubs.
  - Goal: low-level peripheral APIs, hardware abstraction patterns.
- `serial-boot` — simple bootloader and serial firmware updater with rollback protection.
  - Goal: safe firmware upgrades, image validation, recovery strategies.
- `rtos-demo` — minimal RTOS app demonstrating tasks, queues, and synchronization.
  - Goal: RTOS primitives, concurrency patterns, instrumentation.

Phase 4 — Assembly Integration & Portfolio (capstone pieces)
- `asm-helpers` — small helpers for timing, atomic ops, and CPUID wrappers (inline asm where useful).
  - Goal: safe assembly usage, portability notes, fallbacks.
- `mini-disasm` — disassembler for a tiny instruction subset (educational tool).
  - Goal: parsing binary opcodes, output formatting, test cases.
- `portfolio-apps` — one or more polishable apps (examples: fly-fishing log, strategy-roulette, deck-builder backend).
  - Goal: end-to-end polish, README, examples, and optional packaging.

## What each project README should include

- Short description and goal.
- Learning outcomes and difficulty estimate.
- Build steps and example commands.
- Minimal usage example and test instructions.

## Build / Usage

Each subproject contains its own README with build and test instructions. Start in the project folder and follow the instructions there.

## Contributing & Next Steps

- Pick a phase and a project name from above.
- Open an issue or PR with a short plan before large changes.
- Optionally: convert a chosen project into a portfolio-ready app by adding examples and polishing docs.

## License

Add license information here.