## Lock-free Hash Table
Team members: Danié Alvarado, Xinzhu Cai

### Links

* https://github.com/xinzhu-cai/418project.github.io
* [Proposal](https://xinzhu-cai.github.io/418project.github.io/doc/proposal)
* [Checkpoint](https://xinzhu-cai.github.io/418project.github.io/doc/checkpoint)
* [Poster](https://xinzhu-cai.github.io/418project.github.io/Poster.pdf)
* [Final Report](https://xinzhu-cai.github.io/418project.github.io/Report.pdf)

### Summary

We implemented a concurrent extensible hash table library in C++ including three versions: a lock-free
extensible hash table using CAS, which is based on a split-order list, a coarse-grained
lock-based version, and a fine-grained lock-based version based on a two-level locking
mechanism. Given the experimental results on a 12-core shared memory multiprocessor, we
demonstrate that the lock-free version is more efficient and scalable in most cases and is
significantly better than lock-based ones under heavy or skewed workloads.

### Schedule 

| Week           | Task                                                        | Progress    |
|----------------|-------------------------------------------------------------|-------------|
| 11/02 -- 11/08 | Investigate lock-free hash table algorithms                 | Done        |
| 11/09 -- 11/15 | Implementing lock-free extensible hash table using CAS      | Done        |
| 11/16 -- 11/22 | Implement the coarse-grained locked extensible hash table   | Done        |
|                | Implement the fine-grained locked extensible hash table     | Done        |
| 11/23 -- 11/29 | Verify correctness of implemented hash tables               | Done        |
|                | Finish checkpoint report                                    | Done        |
| 11/30 -- 12/06 | Performance analysis                                        | Done        |
|                | Optimize hash table implementations                         | Done        |
|                | Finish final report                                         | Done        |
|                | Finish poster                                               | Done        |
