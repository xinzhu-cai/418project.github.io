---
layout: page
title: "Checkpoint"
permalink: /doc/checkpoint
---

## Schedule and Current Progress

| Week           | Task                                                        | Progress    |
|----------------|-------------------------------------------------------------|-------------|
| 11/02 -- 11/08 | Investigate lock-free hash table algorithms                 | Done        |
| 11/09 -- 11/15 | Implementing lock-free extensible hash table using CAS      | Done        |
| 11/16 -- 11/22 | Implement the coarse-grained locked extensible hash table   | Done        |
|                | Implement the fine-grained locked extensible hash table     | Done        |
| 11/23 -- 11/29 | Verify correctness of implemented hash tables               | Done        |
|                | Finish checkpoint report                                    | Done        |
| 11/30 -- 12/02 | Performance analysis - same tests as the paper              | In-progress |
| 11/30 -- 12/04 | Performance analysis - time distribution                    | In-progress |
| 11/30 -- 12/09 | Optimize hash table implementations                         | In-progress |
| 12/10 -- 12/13 | Finish final report                                         | TODO        |
| 12/13 -- 12/14 | Finish poster                                               | TODO        |

## Work Completed

We finished the implementations of the lock-free extensible hash table using CAS and lock-based extensible hash tables.
We have a coarse-grained locked extensible hash table implementation with a global lock and a fine-grained one that uses 
the two-level locking mechanism. We have tested the correctness of all three in the concurrent setting.

## Goals and Deliverables

### Goals

Most of the stuffs we planned to achieve are complete now except for the performance analysis.
We hope to explore additional optimized versions of both lock-free and lock-based extensible 
hash table if time permits.

**Plan to achieve**

* Coarse-grained lock-based extensible hash table
* Fine-grained lock-based extensible hash table
* Lock-free lock-based extensible hash table using CAS instructions
* Benchmarking and performance analysis

**Hope to achieve**

* Optimized lock-free extensible hash table
* Optimized lock-based extensible hash table

### Deliverables

We will show the execution time and speedup graphs of different concurrent extensible hash tables. 
We will summerize when should we prefer the lock-free version over lock-based
ones and how the lock-free algorithm improves the performance in such senarios, as well as why 
we shall prefer the lock-based ones in some other cases.

## Preliminary Results

We need to set up the microbenchmark environment with some benchmark cases to measure the
performance of our concurrent extensible hash tables.
There are no performance results to show at this point.

## Challenges

There are many optimization techniques we could explore/apply. It is also tricky to design
appropriate benchmark to measure the performance.
