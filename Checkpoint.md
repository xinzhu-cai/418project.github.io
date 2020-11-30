---
layout: page
title: "Checkpoint"
permalink: /doc/checkpoint
---

## Schedule and Current Progress

| Week           | Task                                                        | Progress    | Assigned to |
|----------------|-------------------------------------------------------------|-------------|-------------|
| 11/02 -- 11/08 | Investigate lock-free hash table algorithms                 | Done        | Both        |
| 11/09 -- 11/15 | Implementing lock-free extensible hash table using CAS      | Done        | Xinzhu      |
| 11/16 -- 11/22 | Implement the coarse-grained locked extensible hash table   | Done        | Xinzhu      |
|                | Implement the fine-grained locked extensible hash table     | Done        | Xinzhu      |
| 11/23 -- 11/29 | Verify correctness of implemented hash tables               | Done        | Xinzhu      |
|                | Finish checkpoint report                                    | Done        | Both        |
| 11/28 -- 12/02 | Performance analysis - same tests as the paper              | In-progress | Danié       |
| 11/30 -- 12/04 | Performance analysis - time distribution                    | In-progress | Danié       |
| 11/30 -- 12/09 | Optimize hash table implementations                         | In-progress | Both        |
| 12/10 -- 12/13 | Finish final report                                         | TODO        | Both        |
| 12/13 -- 12/14 | Finish poster                                               | TODO        | Both        |

## Work Completed

We finished the implementations of the lock-free extensible hash table using CAS and lock-based extensible hash tables.
We have a coarse-grained locked extensible hash table implementation with a global lock and a fine-grained one that uses 
the two-level locking mechanism. We have tested the correctness of all three in the concurrent setting.

## Goals and Deliverables

### Goals

Our main goal is to achieve correctness in both the lock-based concurrent extensible hash table and the lock-free implementation. The second goal is to do extensive performance analysis to summarize the characteristics of the two methods and when to prefer the lock-free one.  
Most of the stuff we planned to achieve is complete now except for the benchmarking and performance analysis. Based on the experimental results, we hope to further explore some optimization techniques for both lock-free and lock-based extensible hash tables if time permits.


**Plan to achieve**

* Coarse-grained lock-based extensible hash table
* Fine-grained lock-based extensible hash table
* Lock-free lock-based extensible hash table using CAS instructions
* Benchmarking and performance analysis

**Hope to achieve**

* Optimized lock-free extensible hash table
* Optimized lock-based extensible hash table

### Deliverables

We will show the execution time and speedup graphs of different concurrent extensible hash tables. We will summarize when we should prefer the lock-free version over lock-based ones and how the lock-free algorithm improves the performance in such scenarios, as well as why we shall prefer the lock-based ones in some other cases.

## Preliminary Results

We need to set up the microbenchmark environment with some benchmark cases to measure the
performance of our concurrent extensible hash tables.
There are no performance results to show at this point.

## Concerns

There are no current concerts, as we have already implemented the base version of the algorithm and all that remains is the analysis and iterating for optimizations.

## Poster Session

Performance comparison graphs of the two-level lock-based extensible hash table and the lock-free one. We will feature lots of graphs featuring the time spent on synchronization, busy, and computing just like the ones from lectures.

## Challenges

There are many optimization techniques we could explore/apply. It is also tricky to design
appropriate benchmark to measure the performance.
