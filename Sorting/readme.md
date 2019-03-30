# Selection Sort

  - For an index i find the index min of the remaining part of the array
  - swap a[i] and a[min]
  - increment i
  
  - Proposition: Selection sort uses (N-1) + (N-2) + ...+1 + 0  ~ N^2/2 compares
                 N exchanges
                 
# Insertion Sort

  - At index i swap a[i] with each larger entry to its left.
  - increment i
  
  - Proposition: Uses 1/4*N^2 compares and 1/4*N^2 exchanges on average
  
  - Best Case: If array is sorted - Makes N compares and 0 exchanges
  - Worst Case: If array is in descending order - Makes N^2/2 compares and N^2/2 exchanges.

# Shell sort

  - h-sorting: same as insertion sort by move towards left happens with a stride length h
  
  - Which increment sequence to use?
  
    - Powers of 2: 2,4,8....
      - Doesn't work at all      
    - Powers of 2 -1:1,3,7...
      - May be
    - 3x+1: 1,4,13,40,121,...
      - OK, easy to compute
    - Sedgwick: 1,5,19,41...
      - Tough to beat in emperical studies
      
  - Proposition: The worst case number of compares used by Shell sort with the 3x+1 increment is O(N^1.5)
  
# Shuffle sort

  - 
