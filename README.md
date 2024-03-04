
#### Beam Search Algorithm
- A heuristic search algorithm that examines a graph by extending the most promising node in a limited set is known as beam search. 
- Beam search is a heuristic search technique that always expands the W number of the best nodes at each level. It progresses level by level and moves downwards only from the best W nodes at each level. Beam Search uses breadth-first search to build its search tree. It generates all the successors of the current level’s state at each level of the tree. However, at each level, it only evaluates a W number of states. Other nodes are not taken into account. 

```
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
