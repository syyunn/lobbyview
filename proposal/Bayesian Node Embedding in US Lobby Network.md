Currently working on a research subject proposal about “How to find an node embedding with rich topological/edge-semantic information for the Lobby Graph ?”
This subject is priorly required  to the previous proposal since anyhow we need a low dimensional representation of the node to train the neural network to find contextualized represetations for the large scale graph.
To maintain the contextual complementarity and continuity from the previous works in political science, I had looked through your paper, “Mapping Political Communities: A Statistical Analysis of Lobbying Networks in Legislative Politics” (Hereafter MPC).
The MPC has inferred k different probabilistic memberships shared by 2 different types of actors from the observed frequency of how many times the two different types of actors has interacted.
I’d like to ask you how would it be to find node embeding that densely learn the topological structure and edge semantic of the graph introduced with k-dim of latent variables as Bayesian Skip-gram Models did.
This would let us to densely represent each actor node with local topological context where the actor node is invovled (however, in this case the bipartite structure is no more enforcible) with its dervied latent k-dimensional space that we can later on manually interpret it as the actor membership status. (In this case, also, the issue of manual interpreation of latent space still remains) (edited) 

However in this case, the probabilistic edge representation are not provided though it's provided in MPC
