# Union-Find

  - Used for Dynamic Connectivity problems
  
  - Quick-Find Algorithm ( Eager approach ) :
    - Data Structure used us Integer array id[] of size N
    - Interpretations: p and q are connectedd iff they have the same id
    
    idx: 0   1   2   3   4   5   6   7   8   9
    id[] O | 1 | 1 | 8 | 8 | 0 | 0 | 1 | 8 | 8 |
    
    - 0,5 and 6 are connected
    - 1,2 and 7 are connected
    - 3,4,8 and 9 are connected
    
    - Find: Check if p and q have the same id
      - id[6] = 0; id[1] = 1
      - 6 and 1 are not connected
  
    - Union: To merge componenets containing p and q. Change all entries whose id equals to id[p] to id[q]
      - after union of 6 and 1:
    
      idx: 0   1   2   3   4   5   6   7   8   9
      id[] 1 | 1 | 1 | 8 | 8 | 1 | 1 | 1 | 8 | 8 |    <---- changed entries of 0, 5, 6 and 1,2,7
  
      - union operation is very expensive
        - For N elements to union on N array, time ~ O(n^2)
        - quadratice time
        - Quadratic time doesn't scale well with increasing amount of data
      
  - Quick-union ( lazy approach )
    - integer array id[] of length N
    - Interpretation: id[i] is parent of i
    - Root of i is id[id[id[id....[id[i]....]]]

    idx: 0   1   2   3   4   5   6   7   8   9
    id[] O | 1 | 9 | 4 | 9 | 6 | 6 | 7 | 8 | 9 |

    - Root of 3 is 9
      - parent of 3 is 4.
      - parent of 4 is 9.
      - 9 doesn't have a parent.
      
