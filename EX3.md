
# Ex.No:3
# Ex.Name : Write a C++ function to find a largest value in a Binary Search Tree.


## Date: 
## Aim:
To write a C++ function to find the largest value in a Binary Search Tree (BST) using recursion.

## Algorithm:
STEP 1: Start the program.

STEP 2: Define a Node structure with members:

data → value of the node

left → pointer to left child

right → pointer to right child

STEP 3: Define the function findMax(Node* root) to find the largest value.

STEP 4: If root is NULL, return INT_MIN as a base case.

STEP 5: Store the current node’s value in res.

STEP 6: Recursively find the largest value in the left subtree (lres = findMax(root->left)).

STEP 7: Recursively find the largest value in the right subtree (rres = findMax(root->right)).

STEP 8: Compare res with lres and rres. Update res if a larger value is found.

STEP 9: Return res as the largest value in the BST.

STEP 10: End the function.

## Program:
```
int findMax(Node* root)
{
    if (root == NULL)
        return INT_MIN;
        
    int res = root->data;
    int lres = findMax(root->left);
    int rres = findMax(root->right);
    if (lres > res)
        res = lres;
    if (rres > res)
        res = rres;

    return res;
}

```



## Output:
<img width="825" height="355" alt="{FF76B17F-942E-4F6B-94B7-3773BA997F6A}" src="https://github.com/user-attachments/assets/80036e99-8030-4f3c-a0e8-4d68d9e4d307" />




## Result:
The function returns the maximum value present in the binary search tree.

