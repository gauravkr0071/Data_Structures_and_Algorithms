
437. Path Sum III

Tags- HASHMAP, BINARY TREE, RECURSION, BACKTRACKING

Given the root of a binary tree and an integer targetSum, return the number of paths
where the sum of the values along the path equals targetSum.

The path does not need to start or end at the root or a leaf, but
it must go downwards (i.e., traveling only from parent nodes to child nodes).

 ![image](https://user-images.githubusercontent.com/51910127/129783124-0cbe753d-7578-4f5d-a114-a682f64e0a34.png)


Example 1:


Input: root = [10,5,-3,3,2,null,11,3,-2,null,1], targetSum = 8
Output: 3
Explanation: The paths that sum to 8 are shown.

Example 2:

Input: root = [5,4,8,11,null,13,4,7,2,null,null,5,1], targetSum = 22
Output: 3
 

Constraints:

The number of nodes in the tree is in the range [0, 1000].
-109 <= Node.val <= 109
-1000 <= targetSum <= 1000

__METHOD 1 : HASH MAP__
```cpp
/**
 * Definition for a binary tree node.
 * struct TreeNode {
 *     int val;
 *     TreeNode *left;
 *     TreeNode *right;
 *     TreeNode() : val(0), left(nullptr), right(nullptr) {}
 *     TreeNode(int x) : val(x), left(nullptr), right(nullptr) {}
 *     TreeNode(int x, TreeNode *left, TreeNode *right) : val(x), left(left), right(right) {}
 * };
 */
void helper(unordered_map<int , int>&u, int sum,TreeNode* root,int&path, int curr )
{
    if(!root) return;
  
    curr+=root->val;
    
   
    
    if(u.find(curr-sum)!=u.end())
        path=u[curr-sum]+path;
    
     if(u.find(curr)!=u.end())
        u[curr]++;
    else 
        u[curr]=1;
      
    helper(u,sum, root->left,path,curr);
    helper(u,sum, root->right,path,curr);
   if(u[curr]==1)
       u.erase(curr);
    else
        u[curr]--;
           
  return ;           
    
    
    
}


class Solution {
public:
    int pathSum(TreeNode* root, int sum) {
        unordered_map<int , int>u;
        int path=0;
        int cur=0;
        u[0]=1;///////////very impppppppppppppppppppppppppp
        helper(u,sum,root,path,cur);
        
        return path;
    }
};

```
__METHOD 2__: __DFS__

```cpp

    void dfs(TreeNode* root,int targetSum, int& a)
{  
    if(root==NULL)
    {
    return;
    }

    if(root->val==targetSum)
    {a++;/* do not put return here, guess why as, in the same path 
    
    , later on, that sum can be again produced by 
    
    extending that path                           */}
    dfs(root->left, targetSum-root->val,a);
    dfs(root->right, targetSum-root->val,a);
    
    return;
}

class Solution {
public:
    

    int a=0;
    int pathSum(TreeNode* root, int targetSum) {
        
        if(root==NULL) return 0;
        dfs(root,targetSum,a);
        
        pathSum(root->left,targetSum);
        pathSum(root->right,targetSum);
        
        return a;
    }
};

```
