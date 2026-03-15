# address-translator

Given a page table, logical address size, and physical frame count, translates virtual addresses to physical addresses. Handles page-not-present cases and prints results in hex.

## Features

- Accept a page table, logical address size, and frame count as input.
- Extract page number and offset using bit manipulation on the virtual address.
- Look up the frame number from the page table and construct the physical address.
- Detect and report page-not-present cases cleanly.
- Print all results in hex format.

## Learning outcomes

- Use bit shifts and masks to extract the page number and offset from a virtual address.
- Understand the relationship between logical address size, page size, and the number of page table entries.
- Construct a physical address from a frame number and offset.
- Handle missing-page cases explicitly rather than crashing or returning garbage.

## Build & run

g++ -std=c++17 -O2 -o address-translator main.cpp
./address-translator

## Build it when

- You can manually compute the physical address for 0x812 using a page table on paper before writing any code.
