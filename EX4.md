# Ex.No:4
# Ex.Name : Construct an Expression Tree from an infix expression. Consider the below expression
## Date: 
## Aim:
To write a C++ function buildTree that constructs an expression tree from an infix expression by inserting each character from the expression into the tree.

## Algorithm:
STEP 1: Start the program.

STEP 2: Define a class ExpressionTree (or similar) with a Node structure containing:

data → character (operand/operator)

left → pointer to left child

right → pointer to right child

STEP 3: Declare a root pointer in the class to point to the root of the expression tree.

STEP 4: Define an insert(char ch) function that inserts a character into the tree based on precedence rules (operands become leaf nodes, operators connect nodes).

STEP 5: Define buildTree(string eqn) function.

STEP 6: Traverse the infix expression from right to left using a for loop:

for(int i = eqn.length()-1; i >= 0; i--)


STEP 7: For each character eqn[i], call insert(eqn[i]) to place it correctly in the tree.

STEP 8: Repeat until all characters are inserted into the tree.

STEP 9: The root of the tree now represents the expression tree of the infix expression.

STEP 10: End the function.

## Program:
```
void buildTree(string eqn)
   {
       for(int i = eqn.length()-1;i>=0;i--)
       {
           insert(eqn[i]);
       }
   }   
```




## Output:
<img width="561" height="451" alt="{9BA693B8-41A3-4359-B702-52DACAEEE8AB}" src="https://github.com/user-attachments/assets/b01a2289-58bf-4fd7-a7e7-a77489125594" />




## Result:
The function constructs an expression tree from a given infix expression.



