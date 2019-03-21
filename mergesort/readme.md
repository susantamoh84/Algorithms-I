# MergeSort & QuickSort

  - MergeSort:
    - Basic Plan:
      - Divide array into two halves
      - Recursively sort each half
      - Merge two halves
      
    - How merging works:
      - Abstract in-place merge:
        - Assume two sorted subarrays a[lp] to a[mid] and a[mid+1] and a[hi]
        - use an auxiliary array:
          - Copy everything to the auxiliary array
          - Copy back to original array in following manner:
            - Use 3 pointers i, j in auxiliary array, k in original array
            - take the smallest element from i and j and put it in k
            - increment either i or j and also increment k
            
    - 
