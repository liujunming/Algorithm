[Introduction to A*](https://www.redblobgames.com/pathfinding/a-star/introduction.html)是一个极好的A*算法教程。

There are lots of algorithms that run on graphs. I’m going to cover these:

**Breadth First Search** explores equally in all directions. This is an incredibly useful algorithm, not only for regular path finding, but also for procedural map generation, flow field pathfinding, distance maps, and other types of map analysis.

**Dijkstra’s Algorithm** (also called Uniform Cost Search) lets us prioritize which paths to explore. Instead of exploring all possible paths equally, it favors lower cost paths. We can assign lower costs to encourage moving on roads, higher costs to avoid forests, higher costs to discourage going near enemies, and more. When movement costs vary, we use this instead of Breadth First Search.

**A\*** is a modification of Dijkstra’s Algorithm that is optimized for a single destination. Dijkstra’s Algorithm can find paths to all locations; A* finds paths to one location. It prioritizes paths that seem to be leading closer to the goal.


### The A* algorithm
Dijkstra’s Algorithm works well to find the shortest path, but it wastes time exploring in directions that aren’t promising. Greedy Best First Search explores in promising directions but it may not find the shortest path. The A* algorithm uses both the actual distance from the start and the estimated distance to the goal.

**Compare** the algorithms: Dijkstra’s Algorithm calculates the distance from the start point. Greedy Best-First Search estimates the distance to the goal point. A* is using the sum of those two distances.

A* is the best of both worlds. As long as the heuristic does not overestimate distances, A* finds an optimal path, like Dijkstra’s Algorithm does. A* uses the heuristic to reorder the nodes so that it’s more likely that the goal node will be encountered sooner.

---
参考资料：
1. [wikiwand](https://www.wikiwand.com/en/A*_search_algorithm)
1. [Introduction to A\*旧版本](http://theory.stanford.edu/~amitp/GameProgramming/AStarComparison.html)
1. [geeksforgeeks](https://www.geeksforgeeks.org/a-search-algorithm/)
