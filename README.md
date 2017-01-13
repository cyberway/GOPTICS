# GOPTICS

## Introduction

Due the recent increase of the volume of data that has been generated, organizing this data has become one of the biggest problems in Computer Science. Among the different strategies propose to deal efficiently and effectively for this purpose, we highlight those related to clustering, more specifically, density-based clustering strategies, which stands out for its ability to define clusters of arbitrary shape and the robustness to deal with the presence of data noise, such as DBSCAN and OPTICS. However, these algorithms are still a computational challenge since they are distance-based proposals. In this work we present a new approach to make OPTICS feasible based on data indexing strategy. Although the simplicity with which the data are indexed, using graphs, it allows explore various parallelization opportunities, which were explored using graphic processing unit (GPU). Based on this structure, the complexity of OPTICS is reduced to $O(E*logV)$ in the worst case, becoming itself very fast. In our evaluation we show that our proposal can be over $200x$ faster than its sequential version using CPU.\vskip11pt

## How to:

To compile:
```
$ make
```

To execute:
```
$ ./goptics [Epslon] [MinPts] [Data Itens File] [Number of Itens] [Number of Itens Dimensions] [CPU=0/GPU=1/CPUN=2]
```
This execution will generate an orderedPoints.txt file.

To extract clusters:
```
$ ./extract orderedPoints.txt [Epslon]
```
Output clusters will be created in clusters folder.
