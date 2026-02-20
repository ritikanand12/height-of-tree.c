Binary Tree Height Calculation in C

This project demonstrates how to calculate the height of a binary tree using recursion in C programming language.

The program creates a simple binary tree and computes its height using a recursive approach.

📌 Description

In this implementation:

A binary tree is created using dynamic memory allocation.

The height of the tree is calculated recursively.

Height is defined as the number of edges in the longest path from the root to a leaf node.

⚠️ Note: In this program, height of an empty tree is -1, meaning height is counted in terms of edges.
If you want height in terms of nodes, return 0 instead of -1 in the base case.

🧠 What is Height of a Binary Tree?

The height of a binary tree is:

The number of edges in the longest path from the root node to a leaf node.

For a single node tree, height = 0.

Formula used:

Height = 1 + max(height(left subtree), height(right subtree))
📂 Code Structure
🔹 Structure Definition
struct Node {
    int data;
    struct Node *left, *right;
};

Each node contains:

data → value of the node

left → pointer to left child

right → pointer to right child

🔹 Functions
newNode(int value)

Creates and initializes a new binary tree node.

height(struct Node* root)

Recursively calculates the height of the binary tree.

Base case: If root is NULL, return -1.

🌳 Tree Used in Program

The tree created in main():

        1
       / \
      2   3
     / \
    4   5
Calculated Height:
Height = 2

(Longest path: 1 → 2 → 4 or 1 → 2 → 5)

▶️ Sample Output
Height of Tree = 2
⚙️ How to Compile and Run
1️⃣ Compile
gcc binary_tree_height.c -o binary_tree_height
2️⃣ Run
./binary_tree_height
⏱️ Time & Space Complexity

Time Complexity: O(N)
(Each node is visited once)

Space Complexity: O(H)
(Recursive stack space, where H = height of tree)

📚 Concepts Covered

Binary Tree

Recursion

Tree Traversal Logic

Dynamic Memory Allocation

Divide and Conquer


Iterative version (without recursion)

Full Binary Tree implementation with traversals (Inorder, Preorder, Postorder)
