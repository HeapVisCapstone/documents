# JumboViz: Heap Visualizer for the Elephant Tracks Project

## What is JumboViz?

JumboViz is a tool for visualizing the heap usage of Java programs by memory tracing. It relies on the tool 
Elephant Tracks to generate a heap trace, which JumboViz analyzes and generates some visualizations based on 
the trace.

JumboViz could be used by Java programmers wishing to debug memory issues and/or programming languages/software 
engineering researchers wishing to use the tool to drive their studies of memory usage in Java programs.

Currently, we have implemented two visualization: planar embedding and class hierarchy.

## Main software components

* the [simulator](https://github.com/HeapVisCapstone/tracesimulator);
* the [class hierarchy plugin](https://github.com/HeapVisCapstone/hierarchy).

### External dependencies:

* the Boost C++ libraries (on Debian/Ubuntu: `sudo apt-get install libboost-all-dev`, or use your operating 
system's package manager);
* Java Virtual Machine header files to run the class hierarchy tool (Oracle JDK or OpenJDK preferred);
* d3.js (packaged into the HTML visualizations, no need for extra action).

## How to run visualizations?

For the planar embedding, you need to generate a heap trace for you program using [Elephant Tracks](http://www.cs.tufts.edu/research/redline/elephantTracks/), 
and then follow the instructions in the README [here](https://github.com/HeapVisCapstone/tracesimulator). If you want to see the class hierarchy visualization, you need also to follow the instructions [here](https://github.com/HeapVisCapstone/hierarchy) to get a hierarchy file.

## Downloading and building

`git clone git@github.com:HeapVisCapstone/tracesimulator.git` to clone the main visualization engine. 
`git clone git@github.com:HeapVisCapstone/hierarchy.git` to clone the hierarchy plugin. For both libraries, simply type `make` to build. 
By default the Makefile uses `clang++`, but `g++` will work too.

## Create Datasets and Running Visualizations
[See the README here](https://github.com/HeapVisCapstone/tracesimulator)

## Future work

In the future, we will implement animation features to show the change of heap usage over time.
Other possible work could use machine learning to better cluster the heap graph or run shape analysis on the heap graph to identify data structures.
