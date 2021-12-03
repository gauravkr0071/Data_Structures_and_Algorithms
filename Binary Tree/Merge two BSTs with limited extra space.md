### __Merge two BSTs with limited extra space__

```md
Given two Binary Search Trees(BST), print the elements of both BSTs in sorted form.
The expected time complexity is O(m+n) where m is the number of nodes in the first 
tree and n is the number of nodes in the second tree. The maximum allowed auxiliary
space is O(height of the first tree + height of the second tree)

Examples:

First BST 
       3
    /     \
   1       5
Second BST
    4
  /   \
2       6
Output: 1 2 3 4 5 6


First BST 
          8
         / \
        2   10
       /
      1
Second BST 
          5
         / 
        3  
       /
      0
Output: 0 1 2 3 5 8 10 

```
