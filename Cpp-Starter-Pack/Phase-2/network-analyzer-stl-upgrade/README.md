# network-analyzer-cpp — STL Upgrade

Extension of network-analyzer-cpp to replace manual data structures with idiomatic STL containers. Do this after finishing bst-explorer and lru-cache so the containers feel familiar before applying them to a larger codebase.

## Features

- Replace the adjacency list with std::unordered_map<int, std::vector<int>> or std::unordered_map<std::string, std::set<std::string>>.
- Replace any linear scan for nodes by name with std::unordered_map<std::string, Node*> for O(1) average lookup.
- Replace a manual queue with std::queue<Node*> from <queue>.
- Replace boolean arrays with std::unordered_set<int> for visited tracking.
- Store connected component groups as std::vector<std::set<std::string>> grouped by unit field.

## Learning outcomes

- See the difference between hand-rolled containers and STL containers in a real project you already understand.
- Practice choosing between std::map (ordered, O(log n)) and std::unordered_map (hash, O(1) average) based on whether you need sorted iteration.
- Use std::set for neighbor deduplication and observe how insertion automatically prevents duplicates.
- Understand that idiomatic C++ is not just about syntax — it is about using the standard library so reviewers can read your code without reconstructing your intent.

## Build & run

g++ -std=c++17 -O2 -o network-analyzer main.cpp
./network-analyzer graph.tsv

## Build it when

- You have finished bst-explorer and lru-cache and can explain from memory what std::unordered_map, std::set, and std::queue guarantee about ordering, lookup time, and duplicate handling.

## Notes

- Make a git branch before starting so you can diff the before and after clearly.
- The algorithms do not change — only the containers. If an algorithm changes, you refactored too aggressively.
- After upgrading, run the same graph inputs as before and verify identical output.
