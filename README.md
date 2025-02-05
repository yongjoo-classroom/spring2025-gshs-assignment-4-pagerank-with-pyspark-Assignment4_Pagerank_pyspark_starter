# PageRank with PySpark

## Objective
PageRank is an algorithm to rank web pages based on their importance. 
In this assignment, you will implement PageRank in PySpark.

## Additional Resources
You can learn more about PySpark and transformations here:
- [PySpark Documentation](https://spark.apache.org/docs/latest/rdd-programming-guide.html)
- [RDD Transformations](https://spark.apache.org/docs/latest/rdd-programming-guide.html#transformations)

## Formula
For a given node **i**, the PageRank score is computed as:

![image](https://github.com/user-attachments/assets/2ca35a24-4030-4d7c-ad09-df10a5969bed)

Taking d = 0.85, 

![image](https://github.com/user-attachments/assets/91e8f06d-44f7-484f-b13c-efaa0c731dcd)

where:
- **PR(i)** is the PageRank of node **i**.
- **M(i)** is the set of nodes linking to **i**.
- **L(j)** is the number of outbound links of **j**.
- **0.85** is the damping factor.

Initial rank value of each node will be 1. 

## Instructions
1. Implement the function `compute_pagerank` in `pagerank.py`.
2. The function should take:
   - A dictionary where keys are nodes and values are lists of outgoing links from that node.
   - The number of iterations to refine the PageRank scores.
3. The function should return a dictionary mapping each node to its final PageRank score.

### Input Format
```
{
    0: [1, 2],
    1: [2, 6],
    2: [1, 0, 7],
    3: [1, 0],
    4: [1, 2],
    5: [0, 1, 2],
    6: [0, 7],
    7: [0, 1, 3],
}
```
