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
    
5. Given a string s, the task is to count number of subsequences of the form aibjck, where i >= 1, j >=1 and k >= 1.
    Note: Two subsequences are considered different if the set of array indexes picked for the 2 subsequences are different.
    
    Input  : abbc
    Output : 3
    Subsequences are abc, abc and abbc

    Input  : abcabc
    Output : 7
    Subsequences are abc, abc, abbc, aabc, abcc, abc and abc
    
6. Given a Binary Tree having random pointers clone the Binary Tree. The task is to complete the function cloneTree which 
    take one argument the root of the tree to be copied and should return the root of the cloned tree.
    
7. Given N * M string array of O's and X's
    Return the number of 'X' total shapes. 'X' shape consists of one or more adjacent X's (diagonals not included).
    
    OOOXOOO
    OXXXXXO
    OXOOOXO

    answer is 1 , shapes are  :
    (i)     X
        X X X X
        X     X
        
    XXX
    OOO
    XXX

    answer is 2, shapes are
    (i)  XXX
    (ii) XXX
    
8. Given a Binary Tree with N edges. The task is to extract all leaves of it in a Doubly Linked List (DLL). 
    Note that the DLL need to be created in-place. Assume that the node structure of DLL and Binary Tree is same, 
    only the meaning of left and right pointers are different. In DLL, left means previous pointer and right means next pointer.
    Head of DLL should point to the left most leaf and then in inorder traversal and so on.
    
9. You are given an array A of size N. Your task is to find the minimum number of operations needed to convert the 
    given array to 'Palindromic Array'.

    Palindromic Array:
    [23,15,23] is a ‘Palindromic Array’ but [2,0,1] is not.

    The only allowed operation is that you can merge two adjacent elements in the array and replace them with their sum.
    
10. Given an incomplete Sudoku configuration in terms of a 9x9  2-D square matrix (mat[][]) the task to check if 
    the configuration has a solution or not. 
    
    
