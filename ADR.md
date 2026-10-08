# ADR 1: Selection of BFS as the Preferred Search Algorithm

## Status

Accepted

## Date

08 October 2026

## PRN & Name

25UAM030 – Shradha Dhananjay Kumbhar

## Context

The BFS and DFS algorithms were implemented and profiled on the same 12-node directed graph in SLE-2. Both algorithms were tested using the same start node and goal nodes. The profiling results showed an average execution time of **2.1641 microseconds for BFS** and **2.3998 microseconds for DFS**. Both algorithms expanded the same average number of nodes, **6.5 nodes**. Therefore, a decision was needed about which search algorithm should be preferred for the tested graph in the Search Engine of the SLE-3 architecture.

## Decision

**BFS is selected as the preferred search algorithm for the tested graph** because it showed lower measured average and worst-case execution time than DFS. This decision is specific to the tested graph and experimental environment.

## Alternatives Considered

### 1. Select DFS as the preferred algorithm

DFS was not selected because its measured average and worst-case execution times were higher than BFS in the SLE-2 experiment.

### 2. Keep BFS and DFS equally preferred

This option was not selected because the profiling results provide evidence for preferring BFS for the tested graph.

### 3. Use another search algorithm

Another algorithm was not selected because the SLE-2 comparison focused on BFS and DFS, and the SLE-3 architecture was designed around these two algorithms.

## Rationale / Justification

The decision is supported by the profiling results obtained in SLE-2. BFS achieved an average execution time of **2.1641 microseconds**, while DFS achieved **2.3998 microseconds**. BFS also showed a lower worst-case measured time of **3.5306 microseconds**, compared with **4.2753 microseconds** for DFS.

Both algorithms expanded the same average number of nodes, **6.5 nodes**, so the decision is mainly based on the measured execution time. Both algorithms were tested on the same 12-node graph with the same start and goal nodes, making the comparison consistent.

Based on these results, BFS was selected as the preferred algorithm in the Search Engine of the SLE-3 architecture. DFS is still retained in the system because it is useful for comparison and may be suitable for other graph structures or requirements.

This decision is not considered universal because algorithm performance can change depending on graph structure, search order, machine load, and larger problem sizes.

## Consequences

### Positive Consequences

* BFS showed lower average measured execution time in the SLE-2 experiment.
* BFS also showed lower worst-case measured execution time.
* The decision is supported by actual profiling results.
* The SLE-3 Search Engine has a clear preferred search algorithm.
* DFS remains available for comparison and other possible req
