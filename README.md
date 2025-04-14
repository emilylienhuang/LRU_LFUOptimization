# Least-Recently Used (LRU) and Least-Freqeuntly Used (LFU) Caching Optimization
This project analyzes the efficiency trade-offs between LRU and LFU caching. 

## The Method
Using the Zipfian probabalistic distribution, LRU and LFU caching was evaluated in terms of:
1. Page Fault Rate (PFR)
2. Memory KB
3. Runtime per Request Ms

## The Findings
This study found that caching was optimal in terms of PFR with the Zipfian distribution using LFU caching.
However, in terms of runtime and memory usage, caching was optimal using LRU. 
Neither the LRU nor the LFU implementations matched theoretical yields. 
I believe this result is due to suboptimality of the LRU implementation, and some assumptions made to implement the LFU such as 
deleting items with the lowest frequency even if they may become "hot" later on.

