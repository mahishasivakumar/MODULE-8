# Ex.No:5
# Ex.Name : Write a C++ code to perform RL rotation in an AVL Tree while inserting elements. 
## Date: 
## Aim:
To write a C++ program to insert elements into an AVL tree and perform Right-Left (RL) rotation when necessary to maintain the AVL tree’s balance.

## Algorithm:
STEP 1: Start the program.

STEP 2: Define a Node structure with members:

key → value of the node

left → pointer to left child

right → pointer to right child

height → height of the node

STEP 3: Implement height(Node* node) to calculate node height.

STEP 4: Implement getBalance(Node* node) to calculate balance factor:

balance = height(left subtree) - height(right subtree)


STEP 5: Implement basic rotations:

rightRotate(Node* y) → Right rotation

leftRotate(Node* x) → Left rotation

STEP 6: Implement insert(Node* node, int key) for AVL insertion:

Insert key like a normal BST

Update the height of the current node

Calculate the balance factor

STEP 7: Check for unbalanced cases:

Left-Left (LL): balance > 1 && key < node->left->key → rightRotate

Right-Right (RR): balance < -1 && key > node->right->key → leftRotate

Left-Right (LR): balance > 1 && key > node->left->key → leftRotate(node->left) then rightRotate(node)

Right-Left (RL): balance < -1 && key < node->right->key → rightRotate(node->right) then leftRotate(node)

STEP 8: Return the updated node after insertion and rotation.

STEP 9: Repeat steps 6–8 for each insertion.

STEP 10: End the program.

## Program:
```
Node* insert(Node* node, int key)
{
	/* 1. Perform the normal BST insertion */
	if (node == NULL)
		return(newNode(key));

	if (key < node->key)
		node->left = insert(node->left, key);
	else if (key > node->key)
		node->right = insert(node->right, key);
	else // Equal keys are not allowed in BST
		return node;

	/* 2. Update height of this ancestor node */
	node->height = 1 + max(height(node->left),
						height(node->right));

	/* 3. Get the balance factor of this ancestor
		node to check whether this node became
		unbalanced */
	int balance = getBalance(node);

	// If this node becomes unbalanced, then
	// there are 4 cases

	// Left Left Case
	if (balance > 1 && key < node->left->key)
		return rightRotate(node);

	// Right Right Case
	if (balance < -1 && key > node->right->key)
		return leftRotate(node);

	// Left Right Case
	if (balance > 1 && key > node->left->key)
	{
		node->left = leftRotate(node->left);
		return rightRotate(node);
	}

	if (balance < -1 && key < node->right->key)
	{
		node->right = rightRotate(node->right);
		return leftRotate(node);
	}
	

	/* return the (unchanged) node pointer */
	return node;
}


```



## Output:
<img width="1166" height="420" alt="{E3C7AA3C-6F2B-4210-8358-852D8FB02DAE}" src="https://github.com/user-attachments/assets/3d8ff9af-8422-4c29-9d60-15b52cbf978c" />




## Result:
The program inserts elements into an AVL tree and automatically performs RL rotation when the right subtree of a node is heavier and the inserted key is smaller than the right child.


