# Binary Trees
Similar to linked lists, binary trees are a data structure with **nodes** and **pointers**. 
Each node has 2 pointers: 
1) pointer to the **left** child
2) pointer to the **right** child

The first node (top-most) is known as the root node. 

The values in a node can be any data type. Below is a sample TreeNode class, where the nodes store integer data types: 
```cpp
class TreeNode {
public:
    int val;         // data value stored in the node 
    TreeNode* left;  // ptr to left child
    TreeNode* right; // ptr to right child

    // constructor with initalizer list
    TreeNode (int x) : val(x), left(nullptr), right(nullptr) {};
};
```
<img width="690" alt="Screenshot 2025-05-12 at 3 08 15 PM" src="https://github.com/user-attachments/assets/63862eb9-1f06-40d0-b6d9-da8c33a7567a" />

## Terminology
- **Tree**: 
	- A type of graph, represents hierarchical data (parent-child relationships). There are several types of trees, the most common being binary trees (trees with nodes that have at most 2 children - left child and right child)
- **Subtree**: 
	- A node and all its descendants, important for recursive functions on trees as you can call `dfs(root->left)` to run `dfs` on the left subtree. 
- **Graph**: 
	- Collection of **nodes** and **pointers to other node** (trees and linked lists are types of graphs), **graph theory** is a field of study dedicated to graphs. 
- **Vertex** (node):
	- A single element in a tree, or a node in a graph. Abstract data type that contains a value and pointers to other nodes, connected together by edges or connectors/pointers. 
- **Edge** (connector):
	- Arrows/lines that connect vertices together to form a graph.
- **Root node**: 
	- The node at the top of the tree, where every other node in the tree can be accessed. Usually given as input in tree questions. 
- **Leaf node**:
	- A node with no children, i.e. `node->left == nullptr, and node->right == nullptr;` or `!node->left && !node->right`
- **Parent**: 
	- A node with children. 
- **Child**: 
	- Nodes that descend from a parent node.
- **Ancestor**: 
	- Nodes **before** a certain node, the **parents, grandparents**, etc. 
- **Descendant**: 
	- Nodes **after** a certain node, **children, grandchildren**, etc. 
- **Height**:
	- The number of edges in a path from a node to the deepest leaf node in its subtree.
- **Depth**:
	- The number of edges in a path from a root node to a specified node.


### Height vs Depth
For a root node at `height = 0` and `depth = 0`:
- **Height**: measured by counting the edges between a target node down the the lowest leaf (top-down measurement)
- **Depth**: measured be counting the edges between the root node and the target node (top-down measurement)

##### Exercise
<img width="648" alt="Screenshot 2025-05-12 at 1 38 15 PM" src="https://github.com/user-attachments/assets/e5cbb7b3-2c36-43da-95d5-d59db71d6860" />

Given a binary tree with `n` nodes and and int `k`, find the **height** and **depth** where: 
<details>
<summary>k = 25</summary>
<br>
height = 1
depth = 2
</details>
<details>
<summary>k = 10</summary>
<br>
height = 2
depth = 1
</details>

# Practice Problems


