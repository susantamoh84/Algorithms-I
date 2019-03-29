1. You are given a pointer/reference to a node to be deleted in a linked list of size N. The task is to delete the node.  
    Pointer/reference to head node is not given. You may assume that the node to be deleted is not the last node.
    
    - seach for the node and store the prev pointer and change prev.next = curr.next
    
2.  Height of a binary tree: Height of an empty tree is 0 and height of below tree is 3.

    - height = max( height(left, level) , height(right, level) )
    
3.  You are given an nxn 2D matrix representing an image. Rotate the image by 90 degrees ( clockwise ) ( without using a new storage )

    - for i 0-n/2
        for j i-n-i
          (i,j) -> (j,n-1-i) -> (n-1-i, n-1-j) -> (n-1-j,0)
          
4. Given an array pre[] that represents Preorder traversal of a binary tree. One more array preLN[] is given which has 
    only two possible values ‘L’ and ‘N’. The value ‘L’ in preLN[] indicates that the corresponding node in Binary Tree 
    is a leaf node and value ‘N’ indicates that the corresponding node is non-leaf node.
    
5. 
