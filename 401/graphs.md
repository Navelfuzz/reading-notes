# CF 401: Java // Reading Notes

## Class 35: Implementation: Graphs

## Readings

[Graphs](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/graphs.html)

To turn in your reading “Reply” to this discussion by teaching something that you learned. Then review what one of your classmates learned, and leave a comment.

Some ideas for how you might want to teach:

* Use an analogy
* Explain a detail in depth
* Use WHY, WHAT, HOW structure
* Tutorial / walk through an example
* Write a quiz
* Create a vocabulary/definition list
* Write a cheat sheet
* Create a diagram / visualization / cartoon of a topic
* Anthropomorphize the concepts, and write a conversation between them
* Build a map of the information
* Construct a fill-in-the-blank worksheet for the topic

______

# Cheat Sheet:

## Graph Terminology

* Vertex (Node): Data object that can have zero or more adjacent vertices.
* Edge: Connection between two nodes.
* Neighbor: Adjacent nodes connected via an edge.
* Degree: Number of edges connected to a vertex.

## Types of Graphs

### Undirected Graphs

```java
import java.util.*;

class UndirectedGraph {
    private int V;
    private List<Integer>[] adj;

    public UndirectedGraph(int vertices) {
        V = vertices;
        adj = new ArrayList[V];
        for (int i = 0; i < V; ++i)
            adj[i] = new ArrayList<>();
    }

    public void addEdge(int v, int w) {
        adj[v].add(w);
        adj[w].add(v);
    }
}
```

### Directed Graphs (Digraph)
```java
import java.util.*;

class DirectedGraph {
    private int V;
    private List<Integer>[] adj;

    public DirectedGraph(int vertices) {
        V = vertices;
        adj = new ArrayList[V];
        for (int i = 0; i < V; ++i)
            adj[i] = new ArrayList<>();
    }

    public void addEdge(int v, int w) {
        adj[v].add(w);
    }
}
```

## Graph Representation

### Adjacency Matrix
```java
class AdjacencyMatrix {
    private int V;
    private boolean[][] adjMatrix;

    public AdjacencyMatrix(int vertices) {
        V = vertices;
        adjMatrix = new boolean[V][V];
    }

    public void addEdge(int v, int w) {
        adjMatrix[v][w] = true;
        adjMatrix[w][v] = true;
    }
}
```

### Adjacency List
```java
import java.util.*;

class AdjacencyList {
    private int V;
    private List<Integer>[] adj;

    public AdjacencyList(int vertices) {
        V = vertices;
        adj = new ArrayList[V];
        for (int i = 0; i < V; ++i)
            adj[i] = new ArrayList<>();
    }

    public void addEdge(int v, int w) {
        adj[v].add(w);
    }
}
```

## Traversals

### Breadth First Traversal (BFS)
```java
import java.util.*;

class BreadthFirstTraversal {
    public List<Integer> breadthFirst(UndirectedGraph graph, int start) {
        List<Integer> result = new ArrayList<>();
        boolean[] visited = new boolean[graph.V];
        Queue<Integer> queue = new LinkedList<>();

        visited[start] = true;
        queue.add(start);

        while (!queue.isEmpty()) {
            int vertex = queue.poll();
            result.add(vertex);

            for (int neighbor : graph.adj[vertex]) {
                if (!visited[neighbor]) {
                    visited[neighbor] = true;
                    queue.add(neighbor);
                }
            }
        }

        return result;
    }
}
```

### Depth First Traversal (DFS)
```java
import java.util.*;

class DepthFirstTraversal {
    public List<Integer> depthFirst(UndirectedGraph graph, int start) {
        List<Integer> result = new ArrayList<>();
        boolean[] visited = new boolean[graph.V];

        dfsHelper(graph, start, visited, result);

        return result;
    }

    private void dfsHelper(UndirectedGraph graph, int vertex, boolean[] visited, List<Integer> result) {
        visited[vertex] = true;
        result.add(vertex);

        for (int neighbor : graph.adj[vertex]) {
            if (!visited[neighbor]) {
                dfsHelper(graph, neighbor, visited, result);
            }
        }
    }
}
```

## Real-World Uses of Graphs

* GPS and Mapping: Finding shortest routes.
* Driving Directions: Navigation systems.
* Social Networks: Friend recommendations.
* Airline Traffic: Flight scheduling and routing.
* Netflix (Recommendations): Suggesting movies or shows.

This updated cheat sheet includes code examples for implementing common types of graphs, graph representation, and graph traversal algorithms in Java. You can use these examples as a reference for your graph-related programming tasks.
