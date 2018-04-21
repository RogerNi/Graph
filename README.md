

# Graph
A simple graph program

## Functions
1.  Dynamically add or delete vertices in the graph; 
2.  Dynamically add, edit or delete a weighted edge in the graph; 
3.  Show the contents of the current graph; 
4.  Show a topological ordering in the graph;
5.  Given one vertex as a starting vertex, show the shortest path from this starting vertex to the other vertices in the graph; 

## Sample Commands
Add a vertex vertex {v}   
Add vertex A: vertex A 

Delete a vertex -vertex {v}   
Delete vertex A: -vertex A 

Add an edge edge {weight} {v1} {v2}   
Add an edge from vertex A to vertex B, the weight is 8: edge 8 A B 

Modify an edge weight {weight} {v1} {v2}  
Change the weight of the edge AB to 5: weight 5 A B 

Delete an edge -edge {v1} {v2}  
Delete the edge AB:  -edge A B 

Show the contents contents   
Show the contents: contents 

Show the topological ordering   
topo 

Show the topological ordering of the current graph:  topo   
Show the shortest paths from a vertex 

path {v} 
Show the shortest path from vertex A to other vertices: path A  

## Run
The main method is included in Class Run (in /src) or Run.java (in /bin)

## Sample Inputs and Outputs
Input commands to create a graph 
> vertex A 
> vertex B 
> vertex C 
> vertex D 
> vertex E 
> edge 2 A B 
> edge 3 B C 
> edge 4 B D 
> edge 8 A C 
> edge 1 D C 
> edge 9 E A 
> weight 6 A C 
> -edge E A 
> -vertex E 
> contents 
vertex A B C D  
edge 2 A B 
edge 6 A C 
edge 4 B D 
edge 3 B C 
edge 1 D C 
> topo 
A B D C  
> path A 
A (0) 
A > B (2) 
A > B > C (5) 
A > B > D (6) 
> path B 
A (unreachable) 
B (0) 
B > C (3) 
B > D (4) 

## Issue
Though part of the programe uses hash to accelerate, not all functions are using hash.
