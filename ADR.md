# ADR 1: Selection of BFS as the Preferred Search Algorithm

## Status

Accepted

## Date

08 October 2026

## PRN & Name

25UAM030 – Shradha Dhananjay Kumbhar

## Context

The BFS and DFS algorithms were implemented and profiled on the same 12-node directed graph in SLE-2. Both algorithms were tested with the same start node and goal nodes. The profiling results showed an average execution time of 2.1641 microseconds for BFS and 2.3998 microseconds for DFS. Both algorithms expanded the same average number of nodes, 6.5. Therefore, a decision was needed about which search algorithm should be preferred for the tested graph in the Search Engine of the SLE-3 architecture.

## Decision

BFS is selected as the preferred search algorithm for the tested graph because it showed lower measured average and worst-case execution time than DFS. The decision is specific to the tested graph and experimental environment.

## Alternatives

1. **DFS as the preferred algorithm:** Rejected because DFS recorded higher average and worst-case measured execution time in the SLE-2 experiment.

2. **Keep BFS and DFS equally preferred:** Not selected because the profiling results provided evidence for preferring BFS for the tested graph.

3. **Use a different search algorithm:** Not selected because the SLE-2 experiment focused on BFS and DFS, and the SLE-3 architecture was designed around these two algorithms.

## Rationale / Justification

The decision is supported by the profiling results obtained in SLE-2. BFS recorded an average execution time of 2.1641 microseconds, while DFS recorded 2.3998 microseconds. BFS also recorded a lower worst-case measured time of 3.5306 microseconds compared with 4.2753 microseconds for DFS. The average number of explored nodes was the same for both algorithms at 6.5, so the decision is based mainly on the measured execution time. The profiling was performed using the same 12-node graph, start node and goal nodes. The result showed that BFS was faster in this particular experiment. Therefore, BFS was selected as the preferred algorithm while DFS remains available in the system for comparison and other search requirements. The result is not considered universally applicable because performance can change with graph structure, search order, machine load and larger problem sizes.

## Consequences

### Positive Consequences

* BFS provides lower measured execution time for the tested graph.
* The decision is supported by actual profiling evidence from SLE-2.
* The choice gives a clear preferred algorithm for the Search Engine.
* DFS can still be retained for comparison and other suitable search cases.
* The decision can be explained and defended during the SLE-4 viva.

### Negative Consequences

* The decision is based on a small 12-node test graph.
* BFS may not always perform better than DFS on different graph structures.
* Larger graphs may produce different performance results.
* The current decision does not consider all possible search algorithms.

## References

* SLE-2 Profiling Report – BFS and DFS comparison.
* SLE-3 Full C4 Architecture Design – BFS and DFS Graph Search System.
