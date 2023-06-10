## Graph Theory
- represent a network or a **collection of interconnected objects**
- defined as ordered pairs with two parts **vertices** and **edges**
- **Graph G** is an ordered paired $(V,E)$ where $V$ is a set of **nodes** called **vertices** and $E$ is a set of nodes also called **links**

![[G-Graph-GT.svg]]

### Vertex
- a point where multiple lines meet
- node
- denoted by alphabet

### Edge
- line that connects two lines
- edge cannot be formed without a vertex

![[Edge-GT.svg]]

## Examples
**Square Graph**
$V={a,b,c,d}$
$E={ab,bd,dc,ca}$
![[Example-1-GT.svg]]

![[Example-2-GT.svg]]
$V = {a,b,c,d}$
$E = {ab,ac,ad,cd}$

### Loop
If an edge is drawn to from vertex to itself
![[Loop-1-GT.svg]]

![[Loop-2-GT.svg]]

## Degree of a Vertex
- **Degree of vertex** $v$ denoted by $f(v)$
- **Number of edges** incident on $v$ denoted by $f(v)$, is the number of edges incident on v
- **Size** or **order** refers to the number of edges of the graph

## Types of Graph
1. Undirected
2. Directed

## Degree of Vertex in an Undirected Graph
%% Insert Diagram %%
$deg(a) = 2$
$deg(b) = 3$
$deg(c) = 1$
$deg(d) = 2$
$deg(e) = 0$ `//isolated vertex`

%% Insert Diagram %%
$deg(a) = 2$
$deg(b) = 2$
$deg(c) = 2$
$deg(d) = 2$
$deg(e) = 0$

#### Note
Loop is equal to 2 degrees

## Degree of Vertex of Directed Graph
Each vertex has an indegree and outdegree

### Indegree
The number of edges which are coming in to the vertex

#### Notation:
$deg-(v)$

### Outdegree
The number of edges which are going out of the vertex

$$ \textrm{degree} = \textrm{indegree} + \textrm{outdegree} $$

![[Directed-Example-1-GT.svg]]

| **$v$** | **IN** | **OUT** | **Degree** |
| ------- | ------ | ------- | ---------- |
| a       | 1      | 2       | 3          |
| b       | 2      | 0       | 2          |
| c       | 2      | 1       | 3          |
| d       | 1      | 1       | 2          |
| e       | 1      | 1       | 2          |
| f       | 1      | 1       | 2          |
| g       | 0      | 2       | 2           |

![[Directed-Example-2-GT.svg]]

| **$v$** | **IN** | **OUT** | **Degre** |
| ------- | ------ | ------- | --------- |
| a       | 1      | 1       | 2         |
| b       | 0      | 2       | 2         |
| c       | 2      | 0       | 2         |
| d       | 1      | 1       | 2         |
| e       | 1      | 1       | 2          |

## Vertex Classification
**Pendant Vertex**
Vertex with degree 1
![[Edge-GT.svg]]

**Isolated Vertex**
Vertex with degree 0
![[Isolated-Vertex-GT.svg]]

**Adjacency**
In a graph, vertices are said to be adjacent if there is an edge between two vertices
![[Adjacency-GT.svg]]

**Parallel Edges**
Vertices are connected by more than one edge
![[Parallel-Edge-GT.svg]]

## Graph Classification
### Simple Graph
A graph who loops and with at most one edge between any two vertices

![[Example-1-GT.svg]]

### Multigraph
When any two vertices are joined by more than one edge
![[Multigraph-Example-GT.svg]]

### Complete Graph
When each vertex is connected by an edge to every other vertex
![[Complete-Graph-GT.svg]]

## Walk Classification
**Walk**
Sequence of vertices and edges of a graph
- Vertices can be repeated
- Edges can be repeated

**Open Walk**
Starting and ending vertices are different

**Closed Walk**
Starting and ending vertices are identical

**Trail**
Open Walk without repeating edges
- Vertices can be repeated
- Edges cannot be repeated

**Circuit**
Traversing a graph such that not an edge is repeated but vertex can be repeated and it is closed
- Vertices can be repeated
- Edges cannot be repeated
- Closed Walk

**Path**
Trail without repeating vertices or edges
- Vertices cannot be repeated
- Edges cannot be repeated
- Trail, Open Walk

**Cycle**
Traversing a graph such that we do not repeat a vertex nor we repeat an edge but the **starting** and **ending** must be the same. Only starting and ending vertices can be repeated
- Vertices cannot be repeated except for starting and ending vertices
- Edges cannot be repeated

### Walk Example
![[Walk-Example-GT.svg]]

**Walk Example**
$1-2-3-4$
$3-2-4$
$1-3-2-1$
$2-5-4-2$

**Open Walk Example**
$1-2-3-4$
$3-2-4$
$1-2-4-5$
$1-2-3-5-4$

**Closed Walk Example**
$1-3-2-1$
$2-5-4-2$
$2-3-5-4-2$

**Trail Example**
$1-2-4-5-3$
$3-5-4-2$

**Circuit Example**
$1-2-4-5-3-1$

**Path Example**
$1-2-4-5-3$
$4-5-3-1-2$

**Cycle Example**
$1-2-4-5-3-1$

#### Determine the term that best describes the given walk.

![[Complex-Class-Example-GT.svg]]

1. $1-2-3-1$
   Cycle
2. $1-2-2-4-5-3-1$
   Circuit
3. $1-2-3-4-5-6$
   Path
4. $6-4-5-3-1-2-4$
   Trail
5. $6-4-5-3-1-2-4-6$
   Closed Walk