# Ex.No:1
# Ex.Name : Complete the preorder function in your editor below, which has  parameter: a pointer to the root of a binary tree. It must print the values in the tree's preorder traversal as a single line of space-separated values.
## Date:
## Aim:
To implement a preorder traversal function in a Binary_tree class that prints the values of all nodes in the tree in preorder (root → left → right). If the tree is empty, it displays "Nothing to display".


## Algorithm:
STEP 1: Start the program.

STEP 2: Define a tree node structure with members:

info → data of the node

Left → pointer to left child

Right → pointer to right child

STEP 3: Declare a root pointer in the class to point to the root of the tree.

STEP 4: Define the pretrav function with a default parameter tree* t = root.

STEP 5: Check if the root pointer is NULL. If yes, print "Nothing to display" and return.

STEP 6: Otherwise, check if the current node t is not NULL.

STEP 7: Print the data of the current node (t->info) followed by a space.

STEP 8: Recursively call pretrav on the left child (t->Left).

STEP 9: Recursively call pretrav on the right child (t->Right).

STEP 10: Repeat steps 6–9 until all nodes are visited and end the function.




## Program:
```
void Binary_tree::pretrav(tree* t = root)
{
    if (root == NULL) {
        cout << "Nothing to display";
    }
    else if (t != NULL) {
        cout << t->info << " ";
        pretrav(t->Left);
        pretrav(t->Right);
        
    }
}
```


## Output:
<img width="992" height="307" alt="{D075EBAD-0A0F-420D-B7AE-A3766F3DE7B8}" src="https://github.com/user-attachments/assets/5c250788-154c-4bb5-ae43-34c31be6f7a7" />




## Result:
The function prints all the node values of a binary tree in preorder traversal.
