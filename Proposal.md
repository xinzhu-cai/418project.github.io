layout: page
title: "Proposal"
permalink: /doc/proposal

### Link

https://github.com/xinzhu-cai/418project.github.io

### Summary

We are going to implement lock-free hash tables as a C++ library and compare the performance with lock-based implementations.

### Background

Hash Tables are a very commonly-used data structure, very favorable for when fast lookup times are required, with an expected O(1) cost. But as with most data structures, once we start to make changes to them in parallel, we need to be very careful when implementing then such that there are no race conditions, in particular ones that could lead to deadlock or livelock, but just as importantly those that could corrupt the data structure or destroy its integrity.

The basic operations of hash tables are not difficult to parallelize. Conflicts only occur when two processors are attempting to add or delete an entry from a specific bucket, which by definition of hash tables, should not happen often, although of course there may be specific workloads in which this is the case. Even then, linked lists for each bucket can be implemented in a lock-free fashion as well. The major difficulty in this feat is resizing hash tables.

For this challenge, resizing, we turn to an algorithm detailed in the research paper “Split-ordered lists: Lock-free extensible hash tables” by Ori Shalev called recursive split-ordering, which is “a way of ordering elements in a linked list so that they can be repeatedly “split” using a single compare-and-swap operation”. This algorithm allows for efficient reorganizing of the buckets used in hash tables such that parallel operations are not affected by a resizing.

In addition to the complexities of hash tables, we will be keeping in mind specific workloads and systems such that our library can adapt to better perform on the specific platform it is being run on. Much in the spirit of Domain-Specific Languages, we will attempt to abstract as much as we can from the user for ease-of-use.


### The Challenge
The main challenges for us we predict will be fine-tuning the basic library and then managing the different parallelization strategies we are implementing but hiding from the user. We do not predict implementing the algorithm itself to be of particular difficulty as this is not a far cry from what we have done in previous assignments. The decisions that go into optimizing parallelism, however, we do believe to be a challenge. When to do specific operations for the data structure and considering tradeoffs with different workloads in mind will take much thought. Unlike previous class assignments, we are not creating a workload, we are designing a data structure to handle different workloads.

### Resources
We will be basing our project off of the research paper “Split-ordered lists: Lock-free extensible hash tables” by Ori Shalev, which can be found on the Association of Computing Machinery Digital Library (ACM DL). The article details the algorithm, written in C, and provides some of the code it uses. We will base our code off of theirs.

### Goals and Deliverables
Our primary goal is to create a well-abstracted C++ library to implement the lock-free hash tables described in the research paper we are using as reference. The goals we have in mind are ease of use and portability, and so the more time we have to improve the project, the close we can get to those goals. If we have enough time, we would like to implement optimizations for the system the code is being compiled in.		

For a demo, we would like to have our implementation of lock-free hash tables compared with a version that uses locks in order to have graphs comparing the performance.

### Platform Choice
We will implement different concurrent hash tables in C++. Experiments will be conducted mainly on the GHC machines. 

### Schedule 

| Week | Task |
| --- | ----------- |
| Nov 2 - Nov 8 | Investigate lock-free hash table algorithms |
| Nov 9 - Nov 15 | Implementing lock-free hash table |
| Nov 16 - Nov 22 | Implementing the locked versions as baselines |
| Nov 23 - Nov 29 | Conduct performance evaluation and improve the lock-free version |
| Nov 30 - Dec 6 | Analysis and Project Report |
