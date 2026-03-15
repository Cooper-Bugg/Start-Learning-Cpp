# network-analyzer-cpp

C++ port of the Java Infrastructure Network Analyzer. Loads a TSV graph, supports connection removal, node deletion, closeness centrality via Dijkstra's, BFS connected components by unit, and articulation point detection via DFS low values.

## Features

- Load a weighted graph from a TSV file into an adjacency list.
- Remove edges and delete nodes, cleaning up all neighbor references on deletion.
- Compute closeness centrality for any node using Dijkstra's algorithm.
- Find connected components grouped by unit using BFS.
- Detect articulation points (nodes whose removal disconnects the graph) using DFS low-value tracking.

## Learning outcomes

- Design an adjacency list in C++ and decide whether neighbors store pointers or integer indices.
- Implement manual memory management for vertex objects: understand who owns them and what happens to neighbor references on deletion.
- Port BFS, DFS, and Dijkstra's from Java to C++ without a garbage collector handling cleanup.
- Implement the articulation point algorithm using discovery time and low values.

## Build & run

g++ -std=c++17 -O2 -o network-analyzer main.cpp
./network-analyzer graph.tsv

## Build it when

- Should vertices store pointers to neighbors or integer indices? Think through what deletion looks like for each choice before writing anything.
