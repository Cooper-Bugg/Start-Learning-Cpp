```markdown
# serial-boot

Simple bootloader and serial firmware update example focused on safe image transfer, validation, and rollback protection. This project contains both host-side updater logic and a minimal target-side stub for testing.

Features:
- Serial protocol for transferring firmware images with integrity checks (CRC or signature).
- Image validation and versioning with rollback protection.
- Host-side tool to send images reliably with chunking and retries.

Learning outcomes:
- Design safe firmware update paths and recovery strategies.
- Implement robust transfer logic with acknowledgement, retransmit, and integrity checks.

Build & run (example):
```sh
g++ -std=c++17 -O2 -o serial-boot host_updater.cpp
./serial-boot send firmware.bin /dev/ttyUSB0
```

Notes:
- For real devices, always prefer cryptographic signing and secure boot chains; this example demonstrates basic concepts only.
```
