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
      
  - Weighted Quick Union:
    - Find: Identical to quick union ( lg N )
    - Union: Modify quick-union to: ( lg N )
      - Link root of smaller tree to root of larger tree
      - Update the sz[] array
      
  - Improvements:
    - Path compression by pointing each of the smaller tree to the root of the larger tree

- Applications
  - Percolation
  - Games
  - Dynamic Connectivity
  - Least common ancestor
  - Equivalence of finite state automata
  - Kruskal's minimum spanning tree algorithm

# Interview Questions

  - Social network connectivity. 
     Given a social network containing n members and a log file containing m timestamps at which times pairs of members 
     formed  friendships, design an algorithm to determine the earliest time at which all members are connected 
     (i.e., every member is a friend of a friend of a friend ... of a friend). Assume that the log file is sorted by 
     timestamp and that friendship is an equivalence relation. The running time of your algorithm should be mlogn or 
     better and use extra space proportional to n.
  - Union-find with specific canonical element.
      Add a method find() to the union-find data type so that find(i) returns the largest element in the connected component 
      containing i. The operations, union(), connected(), and find() should all take logarithmic time or better.

      For example, if one of the connected components is {1,2,6,9}, then the find() method should return 9 for each of 
      the four elements in the connected components.
