# Representation Learning on Heterogeneous Lobby Graph
Research proposal on application of contemporary GNN (Graph Neural Network) techniques on ***Lobby Graph***

## Table of Contents
1. [Goals](#Goals)
2. [On Heterogeneous Graph](#Hetero)
3. [Where to Start From?](#StartFrom)

## <a name="Goals"></a> Goals 
Find best representations on ***Lobby Graph*** that well performs downstream tasks, such as "Bill pass prediction", "Interest Group detection(classification)", etc.

## <a name="Hetero"></a> On Heterogeneous Graph
### Definition of Heterogeneous Graph
Heterogeneous graphs, or heterographs for short, are graphs that contain different types of nodes and edges. 

### Why Heterogeneous Graph?
***Lobby Graph*** consists of different types of actors - *lobbyist, legislators, firms* and individuals with different types of edges - *"employed by", "financing", "used to work in", "lobbying for/against"*, etc. Therefore, the nodes and edges in ***Lobby Graph*** eventually
have different feature distributions thus we have to prepare different input feature representations for each types of nodes and edges.

## <a name="StartFrom"></a> Where to Start From?

