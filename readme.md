## Introduction
PISketch is an algorithm that can find persistent and infrequent items (PI items) in data streams.
We compare PISketch with two strawman solutions: 1) On-Off +CM Sketch; 2) PIE + CM Sketch.For PISketch and On-Off + CMSketch, we set the memory size range to 100KB-250KB. ForPIE + CM Sketch, the memory size range is set to 10000KB-25000KB, which is 100 times the one of PISketch. 
## Requirements
g++
## How to run
``` bash
$ ./work.sh
```
