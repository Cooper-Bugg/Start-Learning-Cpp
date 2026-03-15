# sorting-visualizer

CLI tool that runs quicksort and mergesort side by side on the same input, prints step-by-step comparisons, and reports timing and comparison counts. Makes algorithmic complexity tangible by showing the difference between O(n log n) algorithms on real inputs.

## Features

- Generate random, sorted, and reverse-sorted input arrays of configurable size.
- Run quicksort and mergesort on identical copies of the input.
- Count comparisons and swaps independently for each algorithm.
- Print timing results using high-resolution clock.
- Optional: print each pass of the sort visually for small arrays to trace the algorithm.

## Learning outcomes

- Implement mergesort and quicksort from scratch without looking at reference code.
- Understand why both are O(n log n) average but behave differently on sorted input — quicksort degrades, mergesort does not.
- See the difference between theoretical complexity and practical performance: cache behavior and constant factors matter.
- Practice writing instrumented code — adding counters and timers without changing the algorithm's correctness.

## Build & run

g++ -std=c++17 -O2 -o sorting-visualizer main.cpp
./sorting-visualizer --size 1000 --type random

- ./sorting-visualizer --size 10 --visualize — print each pass for a small array.
- ./sorting-visualizer --size 100000 --type sorted — observe quicksort's worst-case degradation.

## Build it when

- You can write the merge step of mergesort and the partition step of quicksort on paper from memory before opening an editor.

## Notes

- Add Big-O analysis comments above each function explaining best, average, and worst case.
- Test with size 1, size 2, already sorted input, reverse sorted input, and all identical elements.
- Once working, go back to arena-alloc and spsc-ring and add similar Big-O comments to those projects.
