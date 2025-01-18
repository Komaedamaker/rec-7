# Binary Search Tree (BST) Implementation

This project implements a Binary Search Tree (BST) in C++ with core functionalities such as insertion, searching, traversal, range-based operations, and finding the k-th smallest element.

## Files Overview

### 1. `BST.hpp`

**Purpose**: Declares the structure and methods of the `BST` class and `Node` struct.

**Key Features**:
- **Struct `Node`**: Represents a tree node with `key`, `left`, and `right` pointers.
- **Class `BST`**: Provides methods to manage the BST.

**Public Methods**:
- `BST()` / `BST(int data)`: Constructors to initialize the tree.
- `~BST()`: Destructor to release memory.
- `addNode(int)`: Inserts a node.
- `searchKey(int)`: Checks if a key exists.
- `printTree()`: Prints nodes in in-order traversal.
- `print2DUtil(int)`: Visualizes the tree in a rotated 2D view.
- `findKthSmallest(int k)`: Finds the k-th smallest node.
- `rangePrint(int k1, int k2)`: Prints nodes within a range.

---

### 2. `BST.cpp`

**Purpose**: Implements methods from `BST.hpp` using recursive helpers for insertion, traversal, searching, and range operations.

**Key Highlights**:
- Memory management via `destroyNode`.
- Recursive helper functions for operations like `addNodeHelper`, `printTreeHelper`, and `kthSmallestHelper`.

---

### 3. `driver.cpp`

**Purpose**: Demonstrates the BST functionality.

**Features**:
- Creates a BST and inserts nodes from an array.
- Validates `findKthSmallest` with various values of `k`.
- Demonstrates range-based printing.

---

## How to Use

### Compilation and Execution

To compile the program:
```bash
g++ BST.cpp driver.cpp -o bst
