# Experiment 11(e): Adjacency List Representation of a Graph

## Aim
To write a Python program to demonstrate the adjacency list representation of a given graph.

---
# Ex. No: 17E - Adjacency List Representation of a Graph

## AIM:
To write a Python program to demonstrate the **adjacency list representation** of the given graph.

## ALGORITHM:

**Step 1**: Start the program.

**Step 2**: Define a class `AdjNode` to create a node for each adjacent vertex:
- Store the **vertex number**.
- Store the **link to the next adjacent node**.

**Step 3**: Define a class `Graph` to create the graph using adjacency lists:
- Initialize the **number of vertices**.
- Create a **list (array)** of size `V`, where each element is initially `None`.

**Step 4**: Define a method `add_edge(src, dest)` to:
- Add `dest` to the adjacency list of `src`.
- Add `src` to the adjacency list of `dest` (for **undirected graphs**).

**Step 5**: Define a method `print_graph()` to:
- Traverse the adjacency list of each vertex.
- Print the **vertex** and its **adjacent nodes**.

**Step 6**: In the main program:
- Create a `Graph` object with `V` vertices.
- Call `add_edge()` for all desired edges.
- Call `print_graph()` to display the adjacency list.

**Step 7**: End the program.

## PYTHON PROGRAM

```
class AdjNode:
	def __init__(self, data):
		self.vertex = data
		self.next = None
class Graph:
    def __init__(self, vertices):
        self.V = vertices
        self.graph = [None] * self.V
    def add_edge(self, src, dest):
        node = AdjNode(dest)
        node.next = self.graph[src]
        self.graph[src] = node
        node = AdjNode(src)
        node.next = self.graph[dest]
        self.graph[dest] = node
    def print_graph(self):
        for i in range(self.V):
            print("Adjacency list of vertex {}\n {}".format(i,i),end="")
            temp=self.graph[i]
            while temp:
                print(" -> {}".format(temp.vertex),end="")
                temp=temp.next
            print("\n")
if __name__ == "__main__":
    V = 5
    graph = Graph(V)
    graph.add_edge(0, 1)
    graph.add_edge(0, 4)
    graph.add_edge(1, 2)
    graph.add_edge(1, 3)
    graph.add_edge(1, 4)
    graph.add_edge(2, 3)
    graph.add_edge(3, 4)
    graph.print_graph()

```

## OUTPUT
![image](https://github.com/user-attachments/assets/6f83b42b-2296-498e-8b8a-0d238238533c)


## RESULT

Hence, The program is successfully executed and the adjacency list representation of the given graph is verified.
## Algorithm

1. **Create a Node Class**:
   - Define a class `AdjNode` to represent each node in the adjacency list:
     - Store the vertex number.
     - Store a reference to the next adjacent node.

2. **Graph Class**:
   - Define a class `Graph` to represent the graph using an adjacency list:
     - Initialize the number of vertices and create an array to store the adjacency lists.
   
3. **Add an Edge**:
   - Define a method `add_edge(src, dest)` to add an edge between two vertices:
     - Add `dest` to the adjacency list of `src`.
     - Add `src` to the adjacency list of `dest` (for undirected graphs).
   
4. **Print the Graph**:
   - Define a method `print_graph()` to print the graph:
     - Traverse each vertex’s adjacency list and print the vertex along with its adjacent nodes.

5. **Main Program**:
   - Create a graph object with `V` vertices.
   - Add edges using the `add_edge()` method.
   - Print the adjacency list representation using `print_graph()`.

---


## OUTPUT

## RESULT
