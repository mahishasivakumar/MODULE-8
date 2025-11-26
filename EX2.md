# Ex.No:2
# Ex.Name : Write a C++ Function to perform Postorder traversal of the below given tree
## Date: 
## Aim:
To write a C++ function to perform postorder traversal of a binary tree and print the values of all nodes in postorder (left → right → root) as a single line of space-separated values.

## Algorithm:
STEP 1: Start the program.

STEP 2: Define a node structure with members:

data → value of the node

left → pointer to left child

right → pointer to right child

STEP 3: Define the function traversePostOrder with a node* temp parameter.

STEP 4: If temp is NULL, return (base case).

STEP 5: Recursively call traversePostOrder on the left child (temp->left).

STEP 6: Recursively call traversePostOrder on the right child (temp->right).

STEP 7: Print the value of the current node (temp->data) followed by a space.

STEP 8: Repeat steps 4–7 until all nodes are visited.

STEP 9: End the recursion.

STEP 10: Ensure that all values are printed in postorder traversal order.

## Program:
```
void traversePostOrder(struct node *temp) 
{
  if (temp != NULL) 
  {
    traversePostOrder(temp->left);
    traversePostOrder(temp->right);
    cout << " " << temp->data;
  }
}

```



## Output:
<img width="1101" height="528" alt="{2C0D509A-25FD-4B9E-A6A2-D36F80109195}" src="https://github.com/user-attachments/assets/34a610d6-8704-4338-b421-1635402011aa" />




## Result:
The function prints the values of the nodes of a binary tree in postorder traversal.

