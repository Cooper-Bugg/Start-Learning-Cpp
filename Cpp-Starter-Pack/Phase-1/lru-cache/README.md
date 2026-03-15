# lru-cache

Fixed-capacity LRU (least recently used) cache using std::unordered_map and std::list. Evicts the least recently used entry when full. Connects page-fault-sim theory to a real data structure used in production systems.

## Features

- get(key) returns the cached value and marks it as most recently used, or -1 if not present.
- put(key, value) inserts or updates an entry, evicting the LRU entry if at capacity.
- O(1) average time for both operations.
- Configurable capacity.
- Hit/miss statistics tracking for analysis.

## Learning outcomes

- Understand why the combination of a hash map and a doubly linked list achieves O(1) LRU operations.
- Use std::list iterators stored inside std::unordered_map values — a pattern that is idiomatic C++ but non-obvious the first time.
- Connect the LRU page replacement algorithm from page-fault-sim to a real implementation used in caches, databases, and operating systems.
- See std::unordered_map and std::list used together as complementary STL containers.

## Build & run

g++ -std=c++17 -O2 -o lru-cache main.cpp
./lru-cache

- put(1,1), put(2,2), get(1), put(3,3) with capacity 2 — after put(3,3) key 2 is evicted since key 1 was recently accessed.
- Run the same reference string from page-fault-sim through this cache and verify hit/miss counts match.

## Build it when

- You can draw the linked list and hash map state after each operation in a 3-step example on paper, including which node moves to the front on a hit, before writing any code.

## Notes

- The key insight: the map stores iterators into the list. When you get a hit, splice the node to the front in O(1) using std::list::splice.
- Test with capacity 1, capacity 2, repeated gets of the same key, and putting the same key twice.
- After building, compare your LRU hit rate against FIFO from page-fault-sim on the same reference strings.
