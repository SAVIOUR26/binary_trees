# Binary Trees in C

This collaborative project explores the fundamentals of binary trees as data structures. It covers various aspects, including tree classification, traversal techniques, and the implementation of different types of binary trees, such as binary, binary search, AVL, and Max Binary Heap trees.

## Tests :heavy_check_mark:

- [tests](./tests): This directory contains test files for all project tasks, provided by ALX.

## Helper File :raised_hands:

- [binary_tree_print.c](./binary_tree_print.c): This C function is responsible for rendering binary trees in a visually appealing format.

## Header File :file_folder:

- [binary_trees.h](./binary_trees.h): This header file includes definitions and function prototypes for all the types and functions developed for this project.

### Data Structures

```c
struct binary_tree_s
{
    int n;
    struct binary_tree_s *parent;
    struct binary_tree_s *left;
    struct binary_tree_s *right;
};

typedef struct binary_tree_s binary_tree_t;
typedef struct binary_tree_s bst_t;
typedef struct binary_tree_s avl_t;
typedef struct binary_tree_s heap_t;

Function Prototypes
File	Prototype
binary_tree_print.c	void binary_tree_print(const binary_tree_t *tree)
0-binary_tree_node.c	binary_tree_t *binary_tree_node(binary_tree_t *parent, int value);
1-binary_tree_insert_left.c	binary_tree_t *binary_tree_insert_left(binary_tree_t *parent, int value);
2-binary_tree_insert_right.c	binary_tree_t *binary_tree_insert_right(binary_tree_t *parent, int value);
3-binary_tree_delete.c	void binary_tree_delete(binary_tree_t *tree);
4-binary_tree_is_leaf.c	int binary_tree_is_leaf(const binary_tree_t *node);
5-binary_tree_is_root.c	int binary_tree_is_root(const binary_tree_t *node);
6-binary_tree_preorder.c	void binary_tree_preorder(const binary_tree_t *tree, void (*func)(int));
7-binary_tree_inorder.c	void binary_tree_inorder(const binary_tree_t *tree, void (*func)(int));
8-binary_tree_postorder.c	void binary_tree_postorder(const binary_tree_t *tree, void (*func)(int));
9-binary_tree_height.c	size_t binary_tree_height(const binary_tree_t *tree);
10-binary_tree_depth.c	size_t binary_tree_depth(const binary_tree_t *tree);
11-binary_tree_size.c	size_t binary_tree_size(const binary_tree_t *tree);
12-binary_tree_leaves.c	size_t binary_tree_leaves(const binary_tree_t *tree);
13-binary_tree_nodes.c	size_t binary_tree_nodes(const binary_tree_t *tree);
14-binary_tree_balance.c	int binary_tree_balance(const binary_tree_t *tree);
15-binary_tree_is_full.c	int binary_tree_is_full(const binary_tree_t *tree);
16-binary_tree_is_perfect.c	int binary_tree_is_perfect(const binary_tree_t *tree);
17-binary_tree_sibling.c	binary_tree_t *binary_tree_sibling(binary_tree_t *node);
18-binary_tree_uncle.c	binary_tree_t *binary_tree_uncle(binary_tree_t *node);
100-binary_trees_ancestor.c	binary_tree_t *binary_trees_ancestor(const binary_tree_t *first, const binary_tree_t *second);
101-binary_tree_levelorder.c	void binary_tree_levelorder(const binary_tree_t *tree, void (*func)(int));
102-binary_tree_is_complete.c	int binary_tree_is_complete(const binary_tree_t *tree);
103-binary_tree_rotate_left.c	binary_tree_t *binary_tree_rotate_left(binary_tree_t *tree);
104-binary_tree_rotate_right.c	binary_tree_t *binary_tree_rotate_right(binary_tree_t *tree);
110-binary_tree_is_bst.c	int binary_tree_is_bst(const binary_tree_t *tree);
111-bst_insert.c	bst_t *bst_insert(bst_t **tree, int value);
112-array_to_bst.c	bst_t *array_to_bst(int *array, size_t size);
113-bst_search.c	bst_t *bst_search(const bst_t *tree, int value);
114-bst_remove.c	bst_t *bst_remove(bst_t *root, int value);
120-binary_tree_is_avl.c	int binary_tree_is_avl(const binary_tree_t *tree);
121-avl_insert.c	avl_t *avl_insert(avl_t **tree, int value);
122-array_to_avl.c	avl_t *array_to_avl(int *array, size_t size);

Tasks :page_with_curl:
0. New Node
0-binary_tree_node.c: A C function that creates a binary tree node with a specified parent and value. Returns a pointer to the new node or NULL on failure.
1. Insert Left
1-binary_tree_insert_left.c: A C function that inserts a node as the left child of another. Returns a pointer to the new node or NULL on failure. If the parent node already has a left child, the new node takes its place, and the old left child becomes the left child of the new node.
2. Insert Right
2-binary_tree_insert_right.c: A C function that inserts a node as the right child of another. Returns a pointer to the new node or NULL on failure. If the parent node already has a right child, the new node takes its place, and the old right child becomes the right child of the new node.
3. Delete
3-binary_tree_delete.c: A C function that deletes an entire binary tree.
4. Is Leaf
4-binary_tree_is_leaf.c: A C function that checks if a given node is a leaf. Returns 1 if the node is a leaf, and 0 otherwise.
5. Is Root
5-binary_tree_is_root.c: A C function that checks if a given node is a root. Returns 1 if the node is a root, and 0 otherwise.
6. Pre-order Traversal
6-binary_tree_preorder.c: A C function that traverses a tree using pre-order traversal.
7. In-order Traversal
7-binary_tree_inorder.c: A C function that traverses a tree using in-order traversal.
8. Post-order Traversal
8-binary_tree_postorder.c: A C function that traverses a tree using post-order traversal.
9. Height
9-binary_tree_height.c: A C function that returns the height of a binary tree.
10. Depth
10-binary_tree_depth.c: A C function that returns the depth of a given node in a binary tree.
11. Size
11-binary_tree_size.c: A C function that returns the size of a binary tree.
12. Leaves
12-binary_tree_leaves.c: A C function that returns the number of leaves in a binary tree.
13. Nodes
13-binary_tree_nodes.c: A C function that returns the number of nodes in a binary tree with at least one child.
14. Balance Factor
14-binary_tree_balance.c: A C function that returns the balance factor of a binary tree.
15. Is Full
15-binary_tree_is_full.c: A C function that checks if a binary tree is full. Returns 1 if the tree is full, and 0 otherwise.
16. Is Perfect
16-binary_tree_is_perfect.c: A C function that checks if a binary tree is perfect. Returns 1 if the tree is perfect, and 0 otherwise.
17. Sibling
17-binary_tree_sibling.c: A C function that returns a pointer to the sibling of a given node in a binary tree. Returns NULL if no sibling is found.
18. Uncle
18-binary_tree_uncle.c: A C function that returns a pointer to the uncle of a given node in a binary tree. Returns NULL if no uncle is found.
19. Lowest Common Ancestor
100-binary_trees_ancestor.c: A C function that returns a pointer to the lowest common ancestor node of two given nodes in a binary tree. Returns NULL if no common ancestor is found.
20. Level-order Traversal
101-binary_tree_levelorder.c: A C function that traverses a binary tree using level-order traversal.
21. Is Complete
102-binary_tree_is_complete.c: A C function that checks if a binary tree is complete. Returns 1 if the tree is complete, and 0 otherwise.
22. Rotate Left
103-binary_tree_rotate_left.c: A C function that performs a left-rotation on a binary tree. Returns a pointer to the new root node of the tree after rotation.
23. Rotate Right
104-binary_tree_rotate_right.c: A C function that performs a right-rotation on a binary tree. Returns a pointer to the new root node of the tree after rotation.
24. Is BST
110-binary_tree_is_bst.c: A C function that checks if a binary tree is a valid binary search tree. Returns 1 if the tree is a valid BST, and 0 otherwise.
25. BST - Insert
111-bst_insert.c: A C function that inserts a value into a binary search tree. Returns a pointer to the new node or NULL on failure. If the tree is NULL, the value becomes the root node. The value is ignored if it is already present in the tree.
26. BST - Array to BST
112-array_to_bst.c: A C function that builds a binary search tree from an array. Returns a pointer to the root node of the created tree or NULL on failure.
27. BST - Search
113-bst_search.c: A C function that searches for a value in a binary search tree. If the value is matched in the BST, returns a pointer to the matched node. Otherwise, returns NULL.
28. BST - Remove
114-bst_remove.c: A C function that removes a node from a binary search tree. Returns a pointer to the new root node of the tree after deletion. If the node to be deleted has two children, it is replaced with its first in-order successor.
29. Big O #BST
115-O: A text file containing the average time complexities of binary search tree operations (one answer per line):
Inserting the value n.
Removing the node with the value n.
Searching for a node in a BST of size n.
30. Is AVL
120-binary_tree_is_avl.c: A C function that checks if a binary tree is a valid AVL tree. If the tree is a valid AVL tree, returns 1. Otherwise, returns 0.
31. AVL - Insert
121-avl_insert.c: A C function that inserts a value in an AVL tree. Returns a value to the inserted node, or NULL on failure.
32. AVL - Array to AVL
122-array_to_avl.c: A C