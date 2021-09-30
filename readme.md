## Introduction
PISketch is a sketch algorithm that can find persistent and infrequent items (PI items) in data streams.
We compare PISketch with two strawman solutions: 1) On-Off +CM Sketch; 2) PIE + CM Sketch. For PISketch and On-Off + CM Sketch, we set the memory size range to 100KB-250KB. For PIE + CM Sketch, the memory size range is set to 10000KB-25000KB, which is 100 times the one of PISketch. 
Our experimental results demonstrate the advantage of PISketch over the two strawman solutions: 1) The Recall Rate (RR) of PISketch is around 25.3% and 66.3% higher than the two strawman solutions, respectively; 2) The Average Relative Error (ARE) of PISketch is around 820.9 (up to 1188.8) and 126.2 (up to 265.6) times lower than the two strawman solutions, respectively; 3) The insertion throughput of PISketch is around 1.23 and 16.5 times higher than the two strawman solutions, respectively.
## Memory allocation and parameter settings
PISketch: 10% memory for Bloom Filter, 90% memory for buckets.

PIE+CM Sketch: 1% memory for CM Sketch, 99% memory for PIE. 
Because PIE needs to maintain a Space-Time Bloom filter for every period, we use Q times the default memory for PIE, where Q denotes the number of periods. In all our experiments, we set Q=1000. For the CM Sketch, we set the number of arrays to 3. We first assign memory to PIE and then allocate the remaining memory to the CM Sketch.

On-Off+CM Sketch: 10% memory for On-Off, 90% memory for CM Sketch, and SLOT_NUM = 3.
## Requirements
g++
## How to run
``` bash
$ ./work.sh
```
