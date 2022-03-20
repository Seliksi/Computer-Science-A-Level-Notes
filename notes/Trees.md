### Trees
Trees are graphs with no cycles. Under the computer science specification, trees are described as **non-linear** data structures, where nodes are connected by directed edges, and there are no cyclic paths between nodes. A tree consists of a root node and a set of sub-trees. The root node is the 'origin' of the tree, from which any node can be reached through the directed edges (the edge is directed from parent node to child node). A sub tree is
--Diagram

A sub-tree may be a 'leaf', which has no children or further subtrees, or a 'branch', which has further directed edges leading away from it.
***
#### Binary tree
A binary tree is a specialisation of a tree, subject to the following restrictions:
- Every node can have at most two children
- The left child of the node has a value strictly **lesser** than the value of the node
- The right child of the node has a value strictly **greater** than the value of the node
<span style="color:gray">A collary of the inequality's strictness is that duplicate-valued nodes cannot exist.</span>
Binary trees are an interesting data structure, as they canonically implement the binary search algorithm in their traversal. 
