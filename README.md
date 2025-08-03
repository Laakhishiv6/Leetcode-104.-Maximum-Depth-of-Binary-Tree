# Leetcode-104.-Maximum-Depth-of-Binary-Tree
# Description
Given the root of a binary tree, return its maximum depth.

A binary tree's maximum depth is the number of nodes along the longest path from the root node down to the farthest leaf node.

 # Solution
 In the given problem we need to find the maximum depth of a binary tree . A binary tree is a tree in which a node or root can have atmost 2 children only .

 Example :
 <img width="422" height="292" alt="image" src="https://github.com/user-attachments/assets/1af81a5a-ff63-4eda-b49d-4ad1316fd984" />

 In the above binary tree the depth of the binary tree is 3 .

 # Algorithm
 1. Firstly traverse through the left and right nodes of the given binary tree .
 2. If the root is empty then return depth as 0.
 3. Else find the maximum length of the tree by traversing through the left and right nodes of the tree.
 4. Return the max length.
# Code

Python 

class Solution:

    def maxDepth(self, root: Optional[TreeNode]) -> int:
        if not root:
            return 0
        return 1+ max(self.maxDepth(root.right),self.maxDepth(root.left))
# Complexity
Time complexity:

The algorithm traverses the tree only once , which makes it O(n) where n is the number of nodes.

Time complexity = O(n)

Space complexity:

The code does'nt need extra memory for finding the maximum depth of the tree .

Hence the space complexity is also O(n) where n is the number of nodes .
