# Search

## Linear Search (Sequential Search)

    - a method of finding a target value within the list.
    - It sequentially checks each element of the list for the target value until a match is found or until all the elements have been searched.

## Binary Search - Just like a phone book

    - Because we know the list is sorted, we can discard half of the list.
    - Instead of looping through all items

    - If it is sorted we can do better than O(n) of linear time.

    - Storing data in a data structure lika a tree instead of a linear data structure like an array is actually more efficient, because in a tree where we can make a decision Should we go left or right.
    - and we discard half the items every step.
    - This is 'Divide and Conquer': O(log(n))
    - O(log(n)) comes from the fact that we're not visiting all nodes each step down the tree, eliminating nodes.

    - Split a list over sorted item and decide from there whether the item is looking for is in the left or right.
    - Because the items are already sorted, we can make a dicision very easily.

## Traversal

    - Sometimes, we have to do Traversal.
    - It means that going from node to node either finding a specific thing or making sure that you touch every single node
    - Simply, visiting every nodes. = O(n) => Linear time

    - How can we do this in a tree, or a graph?
        - Breadth First Search (BFS)
        - Depth First Search (DFS)
        =>O(n)

## Why do we put them in a complex data structure instead of putting them in a array?

    - Because main benefit is that we get O(log(n)) instead of O(n)

## Breadth First Search/Traversal

    - Start from the root node,
    - Then move left to right across the second level, so on.
    - Left to right level by level.

    - Uses additional memory, because it is necessary to track the child nodes on a given level, while finding the level.
    - This means that we need to track every node and its children in order.

## Depth First Search/Traversal.

    - Follows one branch of the tree down as many levels as possible until the target node found, or the end is reached.
    - When the search can't go on any further, it continues at the nearest ancestor with an unexplored child.

    - a lower memory requirement than BFS because it's not necessary to store all the child pointers at each level.

## Pros and Cons

    - Time Complexity: O(n): all same, as they all visit the nodes at least once.
    - Not repeating nodes, and order is also important.

## BFS

    Good:
    - Shortest Path
    - Closer Nodes

    Bad:
    - More memory

    - If you have additional information on the location of the target node, and the node is likely in the upper level of a tree, or a graph, BFS is better.

## DFS

    Good:
    - Less Memory
    - Does Path Exist?

    Bad:
    - Can get slow (if it is really deep)

## What to use?

    - If you know a solution is not far from the root of the tree
    : BFS

    - If the tree is very deep and solutions are rare
    : BFS (DFS will take long)

    - If the tree is very wide
    : DFS (BFS will need too much memory)

    - If solution are frequent but located deep in the tree
    : DFS

    - Determining whether a path exists between two nodes
    : DFS

    - Finding the shortest path
    : BFS

# Breadth Frist Search/Traversal

    - Keep reference of the child node in Queue.
