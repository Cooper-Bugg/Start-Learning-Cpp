# Foundational-Library

Lightweight, portable C++ foundation library for embedded and systems programming. Implements core building blocks with no exceptions and a pluggable allocator model, plus three demo CLIs that exercise the public API.

## Features

- Span<T> — non-owning pointer+length view.
- Arena — bump allocator with alignment and reset.
- UniquePtr<T> — minimal RAII owning pointer backed by the library allocator.
- Optional<T> — in-place storage with engaged flag.
- Result<T,E> — tagged union for return-or-error patterns with no exceptions.
- Vector<T> — dynamic array layered on the allocator.
- String — owning byte buffer with length.
- RingBuffer<T> — fixed-capacity circular queue.
- HashMap<K,V> — open-addressing hash map with linear probing.
- ByteWriter/ByteReader — serialization helpers and endian utilities.
- Logger — stderr/file sinks, minimal formatting, log levels.
- Three demo CLIs (hexdump, wc-lite, grep-lite) that use only this library.

## Learning outcomes

- Implement common standard library primitives from scratch to understand ownership, lifetime, and allocator design.
- Build a pluggable allocator interface and back all containers with it.
- Use Result<T,E> instead of exceptions for all fallible operations.
- Understand what the STL does internally by building smaller, auditable versions.

## Build & run

cmake -S . -B build -G Ninja -DCMAKE_BUILD_TYPE=Release
cmake --build build
./build/demos/hexdump/hexdump file.bin
./build/demos/wc-lite/wc-lite file.txt
./build/demos/grep-lite/grep-lite pattern file.txt

## Build it when

- You have finished arena-alloc and understand bump allocation before starting the Arena component, and have finished spsc-ring before starting RingBuffer.

## Notes

- Keep each component in a single header where possible.
- No STL in public headers except where unavoidable.
- Result<T,E> must support is_ok(), is_err(), unwrap_or(), and map() and be constexpr-friendly.
- Add tests per component in tests/ using a lightweight single-file test runner.
