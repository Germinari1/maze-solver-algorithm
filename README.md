## Maze Solver Algorithm

A maze solver (AI) that accepts a maze encoded in a text file and finds the solution using either Depth First Search (DFS) or Breadth-First Search (BFS) algorithms. The text file that represents the maze must contain the following convention:

- "#" to represent a block
- "A" to represent the starting point
- "B" to represent the ending point or goal

Instances of such a maze are available in the repository in maze1.txt, maze2.txt, and maze3.txt. One such instance is the following:
```plain txt
###                 #########
#   ###################   # #
# ####                # # # #
# ################### # # # #
#                     # # # #
##################### # # # #
#   ##                # # # #
# # ## ### ## ######### # # #
# #    #   ##B#         # # #
# # ## ################ # # #
### ##             #### # # #
### ############## ## # # # #
###             ##    # # # #
###### ######## ####### # # #
###### ####             #   #
A      ######################
```
By following the structure explained above, a user can create new, custom mazes.
## Requirements and how to use

A Python interpreter is required to run the algorithm. In order to execute it with the maze in maze1.txt, for instance, use the following command (with the desired maze in a .txt file):
```txt
python maze.py maze1.txt
```
## Algorithm Overview

The algorithm uses a graph search approach to find the solution to the maze. It represents the maze as a grid, where each cell is a node in the graph. The algorithm then explores the graph by adding neighboring cells to a frontier data structure (either a stack or a queue, depending on the chosen search algorithm).

The `Maze` class is responsible for reading the maze from the text file and representing its structure. It provides methods to print the maze, get neighboring cells, and solve the maze using either depth-first search (DFS) or breadth-first search (BFS).

The `Node` class represents a node in the search tree, which contains the current state (cell coordinates), the parent node, and the action taken to reach this node from the parent.

The `StackFrontier` and `QueueFrontier` classes are implementations of the frontier data structures used in DFS and BFS, respectively. They provide methods to add nodes, check if a state is already in the frontier, remove nodes, and check if the frontier is empty.

## Solution and Output

After solving the maze, the algorithm prints the solution path and the number of states explored during the search. Additionally, it generates an image file (`maze.png`) that visualizes the maze, the solution path, and (optionally) the explored states.

The solution path is represented as a list of actions (e.g., "up", "down", "left", "right") and a list of cell coordinates that make up the path from the start to the goal.

## Contributing

Contributions to this project are welcome. If you find any issues or have suggestions for improvements, feel free to open an issue or submit a pull request.
