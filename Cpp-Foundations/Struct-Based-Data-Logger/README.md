# Struct-Based-Data-Logger

Small C++ project demonstrating compact, stable record formats using structs and writing/reading serialized records to disk. Simulates embedded-style data recording where predictable layouts and minimal dependencies matter.

## Features

- Define versioned record structs for sensor readings or events.
- Serialize records in a stable, documented binary format: field ordering, fixed-size fields, explicit endianness.
- Provide a simple text-CSV export mode for human inspection.
- Implement append-only logging with basic file integrity checks: headers and checksums.

## Learning outcomes

- Learn how to design stable on-disk formats and handle forward/backward compatibility.
- Understand alignment, padding, and explicit field sizes in C++ structs.
- Practice safe binary I/O and provide tooling to convert binary logs to text for analysis.

## Build & run

g++ -std=c++17 -O2 -o data-logger main.cpp
./data-logger record --value 12.34 --id 7
./data-logger export --out records.csv

## Notes

- Avoid writing raw struct blobs to disk without documenting endianness and exact field sizes.
- Add a simple header with a version number so readers can handle format changes.
- Provide tests that write sample records and verify round-trip read/export correctness.
