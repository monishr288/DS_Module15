# Ex11 Tree Representation and Traversal
## DATE: 15.5.25
## AIM:
To write a C function to perform post order traversal of a binary tree.

## Algorithm
1. Start 
2. Define a function display_postorder() that takes a pointer to the root node of the tree. 
3. Check if the current node (root_node) is not null. 
4. Recursively call display_postorder() for the left child of the current node. 
5. Recursively call display_postorder() for the right child of the current node. 
6. After visiting both children, print the value of the current node. 
7. End
## Program:
```
/*
Program to perform post order traversal of a binary tree.
Developed by: MONISH R
RegisterNumber: 212223220061 
*/
/*struct node
{
int value;
struct node *left_child, *right_child;
};*/
struct node* insert_node(struct node* node, int value) // inserting nodes!
{
    // Write your code here
    if(node==NULL)
    {
        struct node* root = (struct node*)malloc(sizeof(struct node));
        root->value=value;
        root->left_child=NULL;
        root->right_child=NULL;
        return root;
        
    }
    else
    {
        struct node* c;
        if(value <= node->value)
        {
            c=insert_node(node->left_child,value);
            node->left_child=c;
        }
        else{
            c=insert_node(node->right_child,value);
            node->right_child=c;
        }
        return node;
    }
}

```

## Output:
![Screenshot 2025-05-15 205308](https://github.com/user-attachments/assets/1d780f04-17d9-4860-a877-12549a32f994)



## Result:
Thus, the function to perform post order traversal of a binary tree is implemented successfully
