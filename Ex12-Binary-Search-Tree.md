# Ex12 Binary Search Tree
## DATE: 15.5.25
## AIM:
To write a C function to insert the elements in the binary search tree

## Algorithm
1. Start 
2. Check if the current node is NULL; if true, create a new node with the given key. 
3. Allocate memory for the new node, set its key, and initialize its left and right children to 
NULL. 
4. If the current node is not NULL, compare the key with the current node's key. 
5. If key <= node->key, recursively insert the key into the left subtree and update the left child 
pointer. 
6. If key > node->key, recursively insert the key into the right subtree and update the right 
child pointer. 
7. Return the current node after the insertion. 
8. End 
 

## Program:
```
/*
Program to insert the elements in the binary search tree
Developed by: MONISH R
RegisterNumber: 212223220061 
*/
struct node* insert(struct node* node, int key) {
   /* If the tree is empty, return a new node */
   if (node == NULL)
       return newNode(key);
 
   /* Otherwise, recur down the tree */
   if (key < node->key)
       node->left = insert(node->left, key);
   else if (key > node->key)
       node->right = insert(node->right, key);
 
   /* return the (unchanged) node pointer */
   return node;
}
 
```

## Output:


![Screenshot 2025-05-15 205604](https://github.com/user-attachments/assets/587d5e47-62df-4fa5-9074-be55e7932522)


## Result:
Thus, the C function to insert the elements in the binary search tree is implemented successfully.
