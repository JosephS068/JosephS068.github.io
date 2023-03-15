# Path Planning
Created with another student

# Description:
### Graph Traversing:
A start and goal node is put at their respective locations. Start is blue and goal is orange. The Agent(cylinder), traverses a path of nodes. The nodes are generated using Probabilistic Roadmap (PRM). Nodes which are generated within the radius of the obstacle + the agent radius, are regenerated so that they are in a proper location within the configuration space(c-space). The agent traverses a path within the generated PRM, and the path is found using uniform cost search. Nodes are connected to other nodes within a configured radius. 

**2D Graph:** Scene of pieces on a map. Graph is generated with PRM in 2D, using both A* and Uniform Cost Search for benchmark comparisons. User is able to place the location of both the start and end goal. The user can also manually place, scale and move obstacles. Boid algorithm implemented for agent to agent interaction. 

**3D Graph:**  Scene is of wasps going to flower. Includes PRM algorithm which is used in 3 dimensions. Objects can be spawned randomly with the p key. PRM will avoid putting points and connections through the obstacles. If boids push one another into obstacles they will feel a bounce force off the surface. The search algorithm on the graph is conducted using A*. In this example the start and end goal are fixed and cannot be changed. 


# Code:
All of the code can be found here: [https://github.com/JosephS068/Processing-Path-Planning](https://github.com/JosephS068/Processing-Path-Planning)

**Note** When running check in code, you may have to re-run it a few times as an incomplete graph may be generated and that case is not handled.

**Note** Additionally, if the graph is overly complex or many paths may be explored, java may run out of memory. 


# Video:
### Graph Traversing:

<video width="480" height="360" controls>
  <source src="https://JosephS068.github.io/Game_Projects/Processing/Path_Resources/Videos/Check-In.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

Agent from start to goal based on PRM algorithm.

### 2D General Overview:

<video width="480" height="360" controls>
  <source src="https://JosephS068.github.io/Game_Projects/Processing/Path_Resources/Videos/2D-General.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

* Features:
    + (0:10) Close up of clusters of boids following a path together.  (Local Interaction Technique)
    + (0:45) PRM with A* generates several paths from the start to goal (Implementation of a global navigation strategy for agents)

### 2D General Success 1:

<video width="480" height="360" controls>
  <source src="https://JosephS068.github.io/Game_Projects/Processing/Path_Resources/Videos/2D-Success-1.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

* Features:
    + (0:00) Scenario showing agents successfully navigating through local minima.

### 2D General Success 2:

<video width="480" height="360" controls>
  <source src="https://JosephS068.github.io/Game_Projects/Processing/Path_Resources/Videos/2D-Success-2.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

* Features:
    + (0:00) Scenario showing agents successfully navigating through local minima.

### 2D General Success 3:

<video width="480" height="360" controls>
  <source src="https://JosephS068.github.io/Game_Projects/Processing/Path_Resources/Videos/2D-Success-3.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

* Features:
    + (0:00) Scenario showing agents successfully navigating through local minima.

### 2D General Failure:

<video width="480" height="360" controls>
  <source src="https://JosephS068.github.io/Game_Projects/Processing/Path_Resources/Videos/2D-Failure.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

* Features:
    + With how boids and obstacle collision is conducted, in small areas with many boids, some are pushed far into the boundaries of the obstacles.

### 2D Failure 2:

<video width="480" height="360" controls>
  <source src="https://JosephS068.github.io/Game_Projects/Processing/Path_Resources/Videos/2D-Fail-2.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

Example of odd behavior:

Behavior produced here is not correct as the boids never reach their goal. With the current path planning and agent interaction, if an agent is pushed in a direction where they cannot reach the goal by going forward the will be stuck for ever. Additionally, because the area the boids are trapped in is many circles, we see the collision is slightly off and from the force of other boids may be pushed out and may actually reach their goal which should not be possible. 

### 2D Interesting 1:

<video width="480" height="360" controls>
  <source src="https://JosephS068.github.io/Game_Projects/Processing/Path_Resources/Videos/2D-Interesting-1.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

* Features:
    + Show  interesting interaction between agents

With how the boids forces are calculated, if they all can't reach the goal and stop, as shown in the video, they circle the goal

### 2D Interesting 2 And 3:

<video width="480" height="360" controls>
  <source src="https://JosephS068.github.io/Game_Projects/Processing/Path_Resources/Videos/2D-Interesting-2-3.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

* Features:
    + Show  interesting interaction between agents

When boids do not have goal, they cluster together and wonder around within the map(Interesting interaction 2). Interaction 3 shows what happens when agents have paths which conflict with one another. If no path is spawned boids wonder around, when a path is created they all move towards the start. This is mostly for testing, there is not path to the start except for direct. However, because of this we can see what happens when two crowds are moving in two directions. Several boids are "thrown" far away because of the forces from two crowds moving in opposite directions.

### 2D User Control:

<video width="480" height="360" controls>
  <source src="https://JosephS068.github.io/Game_Projects/Processing/Path_Resources/Videos/2D-User-Controls.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

* Features:
    + (0:00) Allow the user to add and move obstacles 
    + Allow the user to dynamic choose agent starts and goals at run time
        - (0:28) User agents start
        - (0:40) User selects the agents goal
    + (0:55) Nicely rendered 3D scenes (shows general scene)

### 2D Planning Obstacles:

<video width="480" height="360" controls>
  <source src="https://JosephS068.github.io/Game_Projects/Processing/Path_Resources/Videos/2D-Obstacles.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

* Features:
    + (0:00) Implement A* for graph search. performance improvement documented in **Benchmarks** section.
    + (0:00) Allow the user to add and move obstacles 
        - Previous video did not show obstacles being moved, this is demonstrated in this video

### 3D Planning:

<video width="480" height="360" controls>
  <source src="https://JosephS068.github.io/Game_Projects/Processing/Path_Resources/Videos/3D-Planning.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

* Features:
    + Support	full 3D navigation

Video shows graph generate in 3D. It demonstrates the Boid algorithm in 3D. The path lines are turned on and off to show the path properly.

### 3D Planning Obstacle:

<video width="480" height="360" controls>
  <source src="https://JosephS068.github.io/Game_Projects/Processing/Path_Resources/Videos/3D-Obstacles.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

* Features:
    + Support	full 3D navigation, obstacle demonstration
    + Nicely rendered 3D scene

Every time a new graph is generate wasps return home. Boid is shown closer when agents are clustered at the goal. 

# Benchmarks:
### A* Comparison:
For the **2D** graph creation, we ran both uniform cost search and A *. Below are the results from the two algorithms. In the videos present only A* was ran for speed. When our code is normally ran, both A* and Uniform Cost Search are done, with the number of connections checked being printed to the screen.

Results of 3 different trials:

UCS: 1659  A*: 20

UCS: 319 A*:13

UCS: 4137 A*:51


The reason UCS is so much larger than A* is because our graph is not directed, like you may find in traditional UCS problems. Because of this, a really small path near the start, may be taken several times because of its low cost before any other paths are explored. By adding the distance from the end node of a path to the goal as a heuristic greatly reduces connections searched, as small distance is not the only thing taken into consideration. This also reduces the chance of A* exploring in the wrong direction.


# Images:
### Agent At Start
![Agent At Start](https://JosephS068.github.io/Game_Projects/Processing/Path_Resources/Check_In_Images/Check-In.png)
### Agent In Motion
![Agent In Motion](https://JosephS068.github.io/Game_Projects/Processing/Path_Resources/Check_In_Images/Check-In-Movement.png)
### Agent At End
![Agent At End](https://JosephS068.github.io/Game_Projects/Processing/Path_Resources/Check_In_Images/Check-In-Finish.png)
### 2D Graph
![2D Graph](https://JosephS068.github.io/Game_Projects/Processing/Path_Resources/2D_Images/2D-Graph.png)
### 2D Graph With Obstacles
![2D Graph With Obstacles](https://JosephS068.github.io/Game_Projects/Processing/Path_Resources/2D_Images/2D-Graph-Ob.png)
### 2D Graph Boids At Goal
![2D Graph Boids At Goal](https://JosephS068.github.io/Game_Projects/Processing/Path_Resources/2D_Images/2D-Boid-Goal.png)
### 3D Planning Graph
![3D Planning Graph](https://JosephS068.github.io/Game_Projects/Processing/Path_Resources/3D_Images/3D-Graph.png)
### Agents Following Graph Plan
![Agents Following Graph Plan](https://JosephS068.github.io/Game_Projects/Processing/Path_Resources/3D_Images/3D-Graph-Agents.png)
### Obstacles for 3D
![Obstacles for 3D](https://JosephS068.github.io/Game_Projects/Processing/Path_Resources/3D_Images/3D-Graph-Obstacles.png)
### Agents Avoiding Obstacle In 3D
![Agents Avoiding Obstacle In 3D](https://JosephS068.github.io/Game_Projects/Processing/Path_Resources/3D_Images/3D-Avoid-Obstacle.png)
### Agent Boid Upclose
![Agent Boid Upclose](https://JosephS068.github.io/Game_Projects/Processing/Path_Resources/3D_Images/3D-Swarm-Close-Up.png)
### Agents Following Path No Line
![Agents Following Path No Line](https://JosephS068.github.io/Game_Projects/Processing/Path_Resources/3D_Images/3D-Swarm-No-Lines.png)

# Tools/Libraries Used:
Processing Tutorials: [https://processing.org/tutorials/p3d/](https://processing.org/tutorials/p3d/)

Processing Documentation: [https://processing.org/reference/](https://processing.org/reference/)

Boid Overview: [https://www.red3d.com/cwr/boids/](https://www.red3d.com/cwr/boids/)

Boid Visual Example: [https://www.youtube.com/watch?v=WUXq7GYH62Y](https://www.youtube.com/watch?v=WUXq7GYH62Y)