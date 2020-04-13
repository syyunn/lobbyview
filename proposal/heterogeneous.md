# Representation Learning on Heterogeneous Lobby Graph
Research proposal on application of contemporary GNN (Graph Neural Network) techniques on ***Lobby Graph***

## Table of Contents
1. [Goals](#Goals)
2. [On Heterogeneous Graph](#Hetero)
3. [Research Processs](#)

## <a name="Goals"></a> Goals 
Find best representations on ***Lobby Graph*** that well performs downstream tasks, such as "Bill pass prediction", "Interest Group detection(classification)", etc.

## <a name="Hetero"></a> On Heterogeneous Graph
### Definition of Heterogeneous Graph
Heterogeneous graphs, or heterographs for short, are graphs that contain different types of nodes and edges. 

### Why Heterogeneous Graph?
***Lobby Graph*** consists of different types of actors - *lobbyist, legislators, firms* and individuals with different types of edges - *"employed by", "financing", "used to work in", "lobbying for/against"*, etc. Therefore, the nodes and edges in ***Lobby Graph*** eventually
have different feature distributions thus we have to prepare different input feature representations for each types of nodes and edges.

### Input Feature Representations
For most of the *input features*, we need to leverage the [node embeddings](http://snap.stanford.edu/proj/embeddings-www/files/nrltutorial-part1-embeddings.pdf) since most of the actors in the ***Lobby Graph*** constitute a subgraph of ***Lobby Graph*** and we can embed those subgraph's relations into a vector so that the vector represents the node's characteristics.
The [metapath2vec]() is considered as the first priority to test as a specific node embeddings since the technique is used in the paper [Heterogeneous Graph Transformer](https://arxiv.org/pdf/2003.01332.pdf). This paper applied [self-attentive](https://papers.nips.cc/paper/7181-attention-is-all-you-need.pdf) technique to the [GNN (Graph Neural Network)](https://arxiv.org/pdf/1812.08434.pdf) to enable different types of nodes/edges can well [interact, pass and aggregate messages](https://arxiv.org/abs/1704.01212) without being restricted by their distribution gaps.
 

## <a name="Process"></a> Research Process
