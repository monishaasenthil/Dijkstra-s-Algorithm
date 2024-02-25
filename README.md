# Dijkstra-s-Algorithm
Selects the node with the smallest tentative distance at each step. Finds the shortest path.

## for non directed graph

import networkx as nx

def dijkstra(graph, start):
    # Calculate the shortest paths using Dijkstra's algorithm
    shortest_paths = nx.single_source_dijkstra_path_length(graph, start)
    return shortest_paths

# Example graph represented using networkx
example_graph = nx.Graph()
example_graph.add_edge('A', 'B', weight=1)
example_graph.add_edge('A', 'C', weight=4)
example_graph.add_edge('B', 'C', weight=2)
example_graph.add_edge('B', 'D', weight=5)
example_graph.add_edge('C', 'D', weight=1)

start_node = 'A'
result = dijkstra(example_graph, start_node)
print(f"Shortest distances from {start_node}: {result}")

## for directed graph

import networkx as nx

def dijkstra_directed(graph, start):
    # Calculate the shortest paths using Dijkstra's algorithm
    shortest_paths = nx.single_source_dijkstra_path_length(graph, start)
    return shortest_paths

# Example directed graph represented using networkx
example_directed_graph = nx.DiGraph()
example_directed_graph.add_edge('A', 'B', weight=1)
example_directed_graph.add_edge('A', 'C', weight=4)
example_directed_graph.add_edge('B', 'C', weight=2)
example_directed_graph.add_edge('B', 'D', weight=5)
example_directed_graph.add_edge('C', 'D', weight=1)

start_node_directed = 'A'
result_directed = dijkstra_directed(example_directed_graph, start_node_directed)
print(f"Shortest distances from {start_node_directed}: {result_directed}")

