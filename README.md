# SLE-4 | BFS and DFS Architecture Decision Record

## Student Details

**Name:** Shradha Dhananjay Kumbhar
**PRN:** 25UAM030
**Division:** A
**Course:** 02AML204 – Introduction to Artificial Intelligence
**Program:** SY B.Tech. CSE (AI & ML) | SEM-VI

## Project

**BFS and DFS Graph Search System**

## Purpose

This repository contains the Architecture Decision Record (ADR) prepared for SLE-4. The ADR documents the decision to select BFS as the preferred search algorithm for the tested graph based on the profiling evidence obtained in SLE-2.

## SLE-2 Evidence

BFS and DFS were tested on the same 12-node directed graph.

* BFS average execution time: **2.1641 µs**
* DFS average execution time: **2.3998 µs**
* BFS worst-case time: **3.5306 µs**
* DFS worst-case time: **4.2753 µs**
* Average nodes expanded: **6.5 for both algorithms**

The results showed lower measured execution time for BFS in the selected experiment.

## SLE-3 Connection

In SLE-3, a Full C4 architecture was designed for the BFS and DFS Graph Search System. The architecture includes the Input Module, Search Engine, Visited Set, Performance Analyzer and Output Module.

The ADR decision connects the SLE-2 profiling results with the Search Engine design.

## SLE-4 Decision

**BFS is selected as the preferred search algorithm for the tested graph because it showed lower measured average and worst-case execution time than DFS.**

This decision is specific to the tested graph and experimental environment.

## AI Contribution

ChatGPT was used to understand the SLE-4 requirements, organize the ADR structure, improve explanations and prepare for the viva. The profiling experiments, execution of the programs, collection of results and final decision verification were performed by the student.

## Repository Contents

* `ADR.md` – Architecture Decision Record
* `README.md` – Project overview

## Conclusion

This SLE-4 work documents an architecture decision using actual profiling evidence from SLE-2 and connects it with the architecture designed in SLE-3.
