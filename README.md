# Binary Search Tree (BST) Implementation

This project provides an implementation of a Binary Search Tree (BST) in C++ with various functionalities, including insertion, searching, traversal, range-based operations, and finding the k-th smallest element.

## Files Overview

### 1. `BST.hpp`

**Purpose**: Declares the structure and methods of the `BST` class and `Node` struct.

**Key Features**:
- **Struct `Node`**: Represents a node in the BST, containing:
  - `int key`: The value of the node.
  - `Node* left`: Pointer to the left child.
  - `Node* right`: Pointer to the right child.
- **Class `BST`**: Contains methods for managing the binary search tree, with a private root node.

**Public Methods**:
- `BST()`: Default constructor to initialize an empty tree.
- `BST(int data)`: Parameterized constructor to initialize the tree with a root node.
- `~BST()`: Destructor to free allocated memory.
- `Node* getRoot()`: Returns the root node of the tree.
- `addNode(int)`: Adds a new node with the specified key to the tree.
- `searchKey(int)`: Searches for a key in the tree. Returns `true` if found, otherwise `false`.
- `printTree()`: Prints the elements of the tree using in-order traversal.
- `print2DUtil(int)`: Prints the tree structure in a rotated 2D view.
- `findKthSmallest(int k)`: Finds and returns the k-th smallest element in the tree.
- `rangePrint(int k1, int k2)`: Prints all elements within the range `[k1, k2]`.

**Private Methods**:
- `Node* createNode(int)`: Creates a new node with the given key.
- Recursive helper functions for operations:
  - `addNodeHelper(Node*, int)`: Inserts a node recursively.
  - `printTreeHelper(Node*)`: Performs in-order traversal.
  - `searchKeyHelper(Node*, int)`: Searches for a key recursively.
  - `kthSmallestHelper(Node*, int*, int)`: Finds the k-th smallest element recursively.
  - `destroyNode(Node*)`: Frees memory by deleting nodes recursively.
  - `print2DUtilHelper(Node*, int)`: Prints the tree structure recursively.

---

### 2. `BST.cpp`

**Purpose**: Implements the methods declared in `BST.hpp`.

**Highlights**:
- Implements recursive methods for insertion, searching, traversal, and range printing.
- Handles dynamic memory management with a destructor (`destroyNode`).
- Provides utility functions to visualize the tree and extract key data:
  - `findKthSmallest`: Finds the k-th smallest element in the BST.
  - `rangePrint`: Prints nodes with values in a specified range.

---

### 3. `driver.cpp`

**Purpose**: Demonstrates the usage and functionality of the `BST` class.

**Features**:
- Creates a `BST` and inserts nodes from a predefined array.
- Prints the tree using in-order traversal.
- Tests `findKthSmallest` with various values of `k` to validate correctness.
- Demonstrates range-based printing of elements within specified bounds.

---

## How to Use

### Compilation and Execution

To compile the code, use the following command:
```bash
g++ BST.cpp driver.cpp -o bst
