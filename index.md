## Lock-free Hash Table
Team members: Danié Alvarado, Xinzhu Cai

URL: https://github.com/xinzhu-cai/418project.github.io

### Summary

We are going to implement lock-free hash tables as a C++ library and compare its performance with lock-based implemementations.

### Background

### The Challenge

### Resources
We will be basing our project off of the research paper “Split-ordered lists: Lock-free extensible hash tables” by Ori Shalev, which can be found on the Association of Computing Machinery Digital Library (ACM DL). The article details the algorithm, written in C, and provides some of the code it uses. We will base our code off of theirs.

### Goals and Deliverables
Our primary goal is to create a well-abstracted C++ library to implement the lock-free hash tables described in the research paper we are using as reference. The goals we have in mind are ease of use and portability, and so the more time we have to improve the project, the close we can get to those goals. If we have enough time, we would like to implement optimizations for the system the code is being compiled in.		

### Platform Choice

### Schedule 
| Week | Task |
| --- | ----------- |
| Nov 2 - Nov 8 | Investigate lock-free hash table algorithms |
| Nov 9 - Nov 15 | Implementing lock-free hash table |
| Nov 16 - Nov 22 | Implementing the locked versions as baselines |
| Nov 23 - Nov 29 | Conduct performance evaluation and improve the lock-free version |
| Nov 30 - Dec 6 | Analysis and Project Report |
