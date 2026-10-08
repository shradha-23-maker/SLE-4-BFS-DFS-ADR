# SLE-4 | Contribution Log

## BFS and DFS Graph Search System

**Name:** Shradha Dhananjay Kumbhar
**PRN:** 25UAM030
**Division:** A
**Course:** 02AML204 – Introduction to Artificial Intelligence
**Program:** SY B.Tech. CSE (AI & ML) | SEM-VI

## Overview

This contribution log records the work completed for SLE-4. The main objective was to document and defend an important architecture decision using the profiling evidence from SLE-2 and the C4 architecture developed in SLE-3.

## Work Completed

| Activity         | Work Completed                                                                                   |
| ---------------- | ------------------------------------------------------------------------------------------------ |
| ADR Decision     | Selected BFS as the preferred search algorithm for the tested graph based on profiling evidence. |
| SLE-2 Evidence   | Used the measured BFS and DFS execution times and node counts from the profiling report.         |
| Alternatives     | Considered DFS, keeping both algorithms equally preferred, and using another search algorithm.   |
| Justification    | Compared average and worst-case execution times of BFS and DFS.                                  |
| SLE-3 Connection | Connected the ADR decision with the Search Engine in the Full C4 architecture.                   |
| Documentation    | Prepared the ADR and README documentation.                                                       |
| Viva Preparation | Prepared explanations for the decision, alternatives, profiling results and AI contribution.     |

## Profiling Evidence Used

The SLE-2 profiling results showed:

* BFS average execution time: 2.1641 µs
* DFS average execution time: 2.3998 µs
* BFS worst-case time: 3.5306 µs
* DFS worst-case time: 4.2753 µs
* Average nodes expanded: 6.5 for both algorithms

These results were used as evidence for selecting BFS as the preferred algorithm for the tested graph.

## AI Contribution

ChatGPT was used to understand the SLE-4 requirements, organize the ADR structure, improve explanations and prepare for viva questions.

## Student Contribution

I selected the project and architecture decision, executed and verified the BFS and DFS profiling experiments, collected the results, reviewed the SLE-3 architecture, evaluated the alternatives and made the final decision. I also prepared and reviewed the SLE-4 documentation.

## Final Outcome

The SLE-4 work documents a real architecture decision using evidence from SLE-2 and connects that decision with the SLE-3 C4 architecture.

The project contains:

* ADR
* README
* Contribution Log
* SLE-2 profiling evidence used for the decision
