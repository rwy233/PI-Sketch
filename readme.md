## Introduction
PISketch is an algorithm that can find persistent and infrequent items (PI items) in data streams.
We compare PISketch with two strawman solutions: 1) On-Off +CM Sketch; 2) PIE + CM Sketch.For PISketch and On-Off + CMSketch, we set the memory size range to 100KB-250KB. ForPIE + CM Sketch, the memory size range is set to 10000KB-25000KB, which is 100 times the one of PISketch. Because PIE needs to maintain a Space-Time Bloom filter for every period, we use Q times the default memory for PIE, where Q denotes the number of periods. 
In all our experiments, we set Q=1000. For the CM Sketch, we set the number of arrays to 3. 
We first assign memory to PIE and then allocate the remaining memory to the CM Sketch.
In the following, we refer to On-Off + CM Sketch as Sol-1 and PIE + CM Sketch as Sol-2 for short.
## parameter settings
PISketch:10% memory for Bloom Filter, 90% memory for buckets.

PIE+CM Sketch:1%  memory for CM Sketch, 99% memory for PIE

On-Off+CM Sketch: 10% memory for On-Off, 90% memory for CM Sketch, and SLOT_NUM = 3.
## Requirements
g++
## How to run
1. put dataset file into dataset/
2.
``` bash
$ ./work.sh
```
## Introduction of files
mrun.cpp: main source file.

PISketch.h, OO_FPI.h, pie.h: PISketch, On-Off, PIE's source cpp file.

data.h: Definition of data

definition.h: Definition of variables and parameters

BOBHash32.h,hash_class.h/hash_class.cpp: Hash functions
