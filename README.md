# DAA_TA2

## Problem Statement
Consider the following matrix:

| 0    | 1    | 0    | 0    |
| ------------- | ------------- | ------------- | ------------ |
| 1    | 0    | 1    | 1    |
| 0    | 1    | 0    | 1    |
| 0    | 1    | 1    | 0    |

Convert the matrix into graph.
Can you find out a graph or a sub-graph, which is cyclic in nature?

#### Assignment Question: <br>
Generate a random number “n” between [5-10], create a matrix of size nxn<br>
Populate the locations with “0” and “1” <br>
Apply logic to declare:<br>
&nbsp;&nbsp;a) Complete graph is cyclic <br>
&nbsp;&nbsp;b) Part of the graph is cyclic <br>
&nbsp;&nbsp;c) Write the cycle in terms of vertices. <br>
Constraint: the cycle should be of minimum THREE vertices or MAXIMUM “n”
vertices.<br>

Expected output: 1-2-3-1 or 1-2-3-4------x---n-1
<hr>

## Steps:
1. Create the graph using the adjacency list.
2. Create a recursive function that initializes the current vertex, visited array, and recursion stack.
3. Mark the current node as visited and also mark the index in the recursion stack.
4. Find all the vertices which are not visited and are adjacent to the current node and recursively call the function for those vertices
    - If the recursive function returns true, return true.
    - If the adjacent vertices are already marked in the recursion stack then return true.
5. Create a wrapper function, that calls the recursive function for all the vertices, and
    - If any function returns true return true.
    - Else if for all vertices the function returns false return false.
<hr>

## Test cases:

### 1] When part of graph is cyclic- <br>
![image](https://user-images.githubusercontent.com/119067101/204032498-dd97671a-5bd2-4d3f-92aa-f875b876bdca.png)
<br><br>

### 2] When there in no cycle in graph- <br>
![image](https://user-images.githubusercontent.com/119067101/204032793-27d7c179-e516-4e3a-a0f0-c2ba155baa11.png)
<br><br>

### 3] When complete graph is cyclic- <br>
![image](https://user-images.githubusercontent.com/119067101/204034382-8ff914a0-3e1b-414f-839e-f2d15257b8a8.png)
