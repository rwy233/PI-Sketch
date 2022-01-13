## Introduction
PISketch is a sketch algorithm that can find persistent and infrequent items (PI items) in data streams.
We compare PISketch with two strawman solutions: 1) On-Off +CM Sketch; 2) PIE + CM Sketch. For PISketch and On-Off + CM Sketch, we set the memory size range to 100KB-250KB. For PIE + CM Sketch, the memory size range is set to 10000KB-25000KB, which is 100 times the one of PISketch. There is an exception. In the FRP detection experiment, the memory size range of PISketch and On-Off + CM sketch is set to 150KB-300KB, while that of PIE+CM sketch is 15000KB-30000KB.  
Our experimental results demonstrate the advantage of PISketch over the two strawman solutions: 1) The Recall Rate (RR) of PISketch is around 25.3% and 66.3% higher than the two strawman solutions, respectively; 2) The Average Relative Error (ARE) of PISketch is around 820.9 (up to 1188.8) and 126.2 (up to 265.6) times lower than the two strawman solutions, respectively; 3) The insertion throughput of PISketch is around 1.23 and 16.5 times higher than the two strawman solutions, respectively. We have fully implemented PISketch on FPGA, achieving a throughput of 276 Mips (million insertions per second).

## Requirements
g++

## How to run
put datasets into dataset/
``` bash
$ ./work.sh
```
## files introduction
mrun.cpp:main source cpp file

PISketch.h:PISketch source cpp file

OO_FPI.h,bitset.h,CMSketch.h: On-off source cpp file

pie.h,CMSketch.h: PIE source cpp file

BOBHash32.h,hash_class.h: hash functions

data.h : definition of data

definition.h: definition of variables and parameters
