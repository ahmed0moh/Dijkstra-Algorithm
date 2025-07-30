# 🧭 Dijkstra’s Algorithm and Bidirectional Dijkstra – Performance Analysis

This project provides a comparative analysis of the classic Dijkstra's algorithm and the Bidirectional Dijkstra's algorithm using randomly generated graphs. Implemented in a Jupyter Notebook, it demonstrates the performance difference between the two algorithms across increasing graph sizes.

# 🚀 Project Overview

The notebook creates directed weighted graphs and applies both Dijkstra’s and Bidirectional Dijkstra’s algorithms to find shortest paths. It records and plots their execution times as the number of nodes scales up.


---

# 🧱 Code Structure and Function Descriptions

**class PriorityQueue**

A custom priority queue based on heapq for efficient shortest-path computation.

*_init_(self, verbose=False)*: Initializes the heap and counter. If verbose=True, prints popped items.

*add(priority, item)*: Adds or updates an item with the given priority.

*update(priority, item)*: Updates the priority of an existing item.

*pop()*: Pops the item with the lowest priority, skipping removed ones.



---

**class Edge**

Represents an edge with a target vertex and a distance.


---

**class Graph**

Stores a directed graph via an adjacency list.

*add_edge(vertex1, vertex2, distance)*: Adds a directed edge from vertex1 to vertex2.



---

**Dijkstra(graph, start)**

Classic Dijkstra's algorithm using a priority queue.

Returns two dictionaries:

distances: shortest distances from start to all nodes.

previous: previous node on the shortest path to each vertex.




---

**reconstruct_path(previous, start, target)**

Reconstructs the shortest path from start to target using the previous map returned by Dijkstra.


---

**bidirectional_dijkstra(graph, start, target)**

Performs Bidirectional Dijkstra’s by simultaneously searching from both the start and target nodes.

Returns the length of the shortest path between start and target.



---

**create_graph(num_vertices, num_edges)**

Creates a random directed graph with the given number of vertices and edges. Edge weights are random integers between 1 and 10.


---

**measure_execution_time(n)**

For each n (number of vertices), creates a graph and measures:

Time for classic Dijkstra's algorithm (from node 0).

Time for bidirectional Dijkstra's algorithm (from node 0 to n-1).


Returns two lists with execution times for each algorithm.


---

Visualization

Uses matplotlib to plot the execution times of both algorithms against the number of vertices.


---

# 📊 Sample Output

A graph comparing execution times of both algorithms on random graphs of increasing size. Bidirectional Dijkstra often performs faster due to its simultaneous search.


![Feature Histograms](https://github.com/ahmed0moh/Dijkstra-Algorithm/blob/main/comparing_execution.png)


---

# 📦 Requirements

Python 3

Jupyter Notebook

matplotlib


Install requirements with:
```
pip install matplotlib
```

---

# 🧠 What You’ll Learn

How Dijkstra’s algorithm works internally

How bidirectional search optimizes shortest-path discovery

How performance varies with graph size
