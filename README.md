# Final2270

Priority Queue Implementation and Analysis

	The purpose of this assignment is to compare the performance, in terms of runtime, of three different implementations of a priority queue: heap, standard library, and linked list. The priority queue being built for this assignment is used for medical triage in the theoretical situation of 880 pregnant women all going into labor at the same time. The priority queue must compare time until labor and, when labor times are equal, treatment time, and place these women into a queue of which the priority is defined by lowest time until labor, when needed, lowest treatment time. 

	The heap implementation of a priority queue implements a Min Heap of structs, for this assignment the structs contain the name, time until labor, and treatment time for each woman. A Min Heap is a binary tree that is both complete, meaning that every level of the tree is filled with the exception of the bottom or last level of the tree. And, that the root of the tree is the minimum value of the tree.  A heap is typically represented as an array and its tree structure comes from three equations that can calculate the index of the parent, left, and right nodes from the index of the node you are currently working with. As nodes are added to the heap, one must iterate through the existing heap nodes and check if the node that is being pushed’s labor time value is greater than or equal to the value of its parent. If that is true one must then check if the values are equal, if they are equal one must then compare the treatment time values and accordingly insert the node into heap, either before or after the parent, by calling the swap function, if before. If the node being pushed’s labor time value is greater than the parent’s then it will be inserted before the parent by calling the swap function.

	The standard library implementation of a priority queue uses a heap as well, it already has the push, pop, and other functions defined, and can be implemented as a max or min heap. In the case of a min heap, one has to provide the declaration of the min heap with a vector of nodes and well as a comparator node or class that returns the greater of any two node priority values. In the case of this assignment the comparator class compares the labor time values and returns the greater, except when the labor time values are equal. In this case additional if/else statements are implemented to compare the treatment time values and returns the greater of those two. 

	The linked list implementation of a priority queue can be implemented as a basic singly linked list. Each node in the list represents one woman and contains her priority times.  Nodes can be added to list and linked together through pointers. As they are added to the list, one must iterate through the existing list and insert the new node at the appropriate place, similar to the comparison process as described in the heap implementation, by comparing the labor time values and if they are equal then additionally comparing the treatment time values.
  