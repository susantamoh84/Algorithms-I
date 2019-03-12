# Analysis of algorithms

  - Scientific method:
    - Observe
    - Hypothesize
    - Predict
    - Verify
    - Validate
    
  - Principles:
    - Experiments must be reproducible
    - Hypotheses must be falsifiable

# Observations
  - Standard plot:
    - Simply plot the running time T(N) vs input size N.
  - Doubling hypothesis:
    - Quick way to estimate b in a power-law relationship. Try to double the input size and see if the 
      running time increases in a log-log manner

# Mathematical Models
  - Total running time = sum of cost x frequency of all operations
    - Need to analyze program to determine set of operations
    - Cost depends on machine, compiler
    - Frequency depends on algorithm and input data
    
  - There are different running time for different operations
  - Simplification 1: cost model
    - Use some basic operation as a proxy for running time.
  - Simplification 2: tilde notation
    - Estimate running time (or memory) as a function of input size N
    - Ignore lower order terms
      - When N is large, terms are negligible
      - when N is small, we don't care
      
  - In practice,
    - Forumlas can be complicated
    - advanced mathematics might be required
    - Exact models best left for experts
      - We have to approximate models in real-life.
      
# Order-of-Growth Classifications

  - Common order-of-growth classifications
  
  | Order of growth | name            | typical code framework  | description         | example                | T(2N)/T(N)  |
  | --------------- | --------------- | ----------------------- | ------------------- | ---------------------- | ----------- |
  | 1               | constant        | a = b + c               | statement           | add two numbers        | 1           |
  | log N           | logarithmic     | while (N>1) { N = N /2 }| divide in half      | binary search          | ~ 1         |
  | N               | linear          | for(int i=0;i<N;i++)    | loop                | find the maximum       | 2           |
  | N log N         | linearithmic    | [see mergesort lecture] | divide and conquer  | mergesort              | ~ 2         |
  | N^2             | quadratic       | for(int i...) for(..)   | double loop         | check all pairs        | 4           |
  | N^3             | cubic           | for(..) for(..) for(..) | triple loop         | check all triples      | 8           |
  | 2^N             | exponential     | [see combinatorial srch]| exhausive search    | check all subsets      | T(N)        |
  

  - Example of Sum of triplet = 0
    - for pair of numbers, perform a binary search for -(a+b)
    - running time ~ N^2 Lg N
