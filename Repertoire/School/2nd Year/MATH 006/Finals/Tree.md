
| **Keyword** | **Definition**            |
| ----------- | ------------------------- |
| Tree        | A connected acyclic graph |
| Branch      | Edges of a tree           |
| Nodes       | Elements                  |
| Leaf Nodes  | Nodes without children    |
| Forest      | Disconnected acyclic graph                          |

## Leaf Nodes
- A mathematical structure that is  a special kind of graph which has the following properties
	- Undirected
	- Connected
	- Acyclic

### Example
Every tree has at least two vertices of degree one
![[Tree-T.svg]]

![[Line-T.svg]]

## Bridge and Forests
- Each edge connecting each pair of vertices is a **bridge**
- A **forest** is a disjoint union of trees
- Each component of a forest is a tree and any tree is a connected forest

Denote T as tree and F as forest.
The number components of a graph $G$ is denoted $c(G)$
![[Graph-G1-T.svg]]

![[Graph-G2-T.svg]]

![[Graph-G3-T.svg]]

## Spanning Tree
Let $G$ be connected, then the subgraph of $G$ is called a spanning tree of $G$

If $H$ is a tree, then it contains all vertices of $b$

Graph G
![[Spanning-Graph-G-T.svg]]

Graph H
![[Spanning-Graph-H-T.svg]]

