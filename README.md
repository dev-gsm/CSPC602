### Search Algorithms
Search algorithms in AI are algorithms that aid in the resolution of search issues. A search issue comprises the search space, start, and goal state. By evaluating scenarios and alternatives, search algorithms in artificial intelligence assist AI agents in achieving the objective state.


The algorithms provide search solutions by transforming the initial state to the desired state. Therefore, AI machines and applications can only perform search functions and discover viable solutions with these algorithms.

##### Terminologies
Search
:Searching solves a search issue in a given space step by step. Three major factors can influence a search issue.

Search Space:
A search space is a collection of potential solutions a system may have.

Start State:
The jurisdiction where the agent starts the search.

Goal test:
A function that examines the current state and returns whether or not the goal state has been attained.


#### Types of Search Algorithms
##### Uninformed Search
Uninformed search is a method of searching a search tree without knowledge of the search space, such as initial state operators and tests for the objective, and is also known as blind search. It goes through each tree node until it reaches the target node. These algorithms are limited to producing successors and distinguishing between goal and non-goal states.

Example: Breadth-first-search (BFS), Depth-first-Search (DFS) etc.

##### Informed Search/Heuristic Search
The informed search algorithm is more useful for large search space. Informed search algorithm uses the idea of heuristic, so it is also called Heuristic search.

**Heuristics function:** Heuristic is a function which is used in Informed Search, and it finds the most promising path. It takes the current state of the agent as its input and produces the estimation of how close agent is from the goal. The heuristic method, however, might not always give the best solution, but it guaranteed to find a good solution in reasonable time. Heuristic function estimates how close a state is to the goal. It is represented by `h(n)`, an it calculates the cost of an optimal path between the pair of states. The value of the heuristic function is always positive.

Example: Best-first-search, A* Search etc, Beam Search etc.




#### Best First Search


```{algorithm}
Best-First-Search(Graph g, Node start)
    1) Create an empty PriorityQueue
       PriorityQueue pq;
    2) Insert "start" in pq.
       pq.insert(start)
    3) Until PriorityQueue is empty
          u = PriorityQueue.DeleteMin
          If u is the goal
             Exit
          Else
             Foreach neighbor v of u
                If v "Unvisited"
                    Mark v "Visited"                    
                    pq.insert(v)
             Mark u "Examined"                    
End procedure
```
#### Beam Search Algorithm

- Beam search is a heuristic search algorithm that explores a graph by expanding the most optimistic node in a limited set. Beam search is an optimization of best-first search that reduces its memory requirements.

- Best-first search is a graph search that orders all partial solutions according to some heuristic. But in beam search, only a predetermined number of best partial solutions are kept as candidates. Therefore, it is a greedy algorithm.

- Beam search uses breadth-first search to build its search tree. At each level of the tree, it generates all successors of the states at the current level, sorting them in increasing order of heuristic cost. However, it only stores a predetermined number (β), of best states at each level called the beamwidth. Only those states are expanded next.


```{algorithm}
Start 
Take the inputs 
NODE = Root_Node & Found = False
If : Node is the Goal Node,
     Then Found = True, 
Else : 
     Find SUCCs of NODE if any, with its estimated cost&
     store it in OPEN List 
While (Found == false & not able to proceed further), do
{
     Sort OPEN List
     Select top W elements from OPEN list and put it in
     W_OPEN list and empty the OPEN list.
     for each NODE from W_OPEN list
     {
         if NODE = Goal,
             then FOUND = true 
         else
             Find SUCCs of NODE. If any with its estimated
             cost & Store it in OPEN list
     }
}
If FOUND = True,
    then return Yes
else
    return No
Stop
```
