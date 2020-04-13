# Representation Learning on Heterogeneous Lobby Graph
Research proposal on application of contemporary [GNN (Graph Neural Network)](https://arxiv.org/pdf/1812.08434.pdf) techniques on ***Lobby Graph***. ***Lobby Graph*** refers to all data collected and structured in [lobby_database](https://github.com/insongkim/lobby_database)

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
We need to leverage the [node embeddings](http://snap.stanford.edu/proj/embeddings-www/files/nrltutorial-part1-embeddings.pdf) since most of the actors in the ***Lobby Graph*** constitute a subgraph of ***Lobby Graph*** thus we can embed those subgraph's relations into a vector so that the vector can represent the node's characteristics.
The [metapath2vec](https://ericdongyx.github.io/papers/KDD17-dong-chawla-swami-metapath2vec.pdf) is considered as the first priority to try since the technique is used in the paper, [Heterogeneous Graph Transformer (HGT)](https://arxiv.org/pdf/2003.01332.pdf), which is considered as a primary reference for the research. This paper applied [self-attentive](https://papers.nips.cc/paper/7181-attention-is-all-you-need.pdf) technique to the [GNN (Graph Neural Network)](https://arxiv.org/pdf/1812.08434.pdf) to enable different types of nodes/edges can well [interact, pass and aggregate messages](https://arxiv.org/abs/1704.01212) without being restricted by their different feature distributions.
 

## <a name="Process"></a> Research Process
### Research Design Level
 - [ ] Determine <ins>downstream task</ins> - such as prediction of bill pass
 - [ ] Deterimne <ins>input arguments</ins> : Upon given downstream task, determine which nodes and edges will be used to train <ins>the downstream task</ins>. This process may require domain knowledge to successfully train the model. For example, more money could positively affect the lobbying result as the interest group wants, however, there might be more renowned essential factors for successful lobbying among lobbyists.
### Technical Level

#### Input Feature Preparations
 - [ ] Trial run of [metapath2vec](https://ericdongyx.github.io/papers/KDD17-dong-chawla-swami-metapath2vec.pdf) on [OAG (Open Academic Graph)](https://www.openacademic.ai/oag/) data as the paper originally implemented.
 - [ ] Revise Codes to run [metapath2vec](https://ericdongyx.github.io/papers/KDD17-dong-chawla-swami-metapath2vec.pdf) on ***Lobby Graph Data*** after determination of downstream task and input arguments for the task.

#### Model Preparation
 - [ ] Try [Heterogeneous Graph Transformer (HGT)](https://arxiv.org/pdf/2003.01332.pdf) with the input features prepared from the trial run of [metapath2vec](https://ericdongyx.github.io/papers/KDD17-dong-chawla-swami-metapath2vec.pdf)  as the paper originally implemented.
 - [ ] Train [Heterogeneous Graph Transformer (HGT)](https://arxiv.org/pdf/2003.01332.pdf) with the prepared input from the ***Lobby Graph Data***.