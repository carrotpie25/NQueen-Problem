# NQueen-Problem (C++)
The N queen problem is the problem of placing N chess queens on an NxN chessboard in a way that no two queens attack each other. In this project, we will solve for 8 queens and 4 queens. 

The N Queens problem entails the placement of N chess queens on a chessboard in a manner that precludes any queens from threatening each other. It requires us to find the possible solutions to the problem. While some cases necessitate the finding of a single solution, others require the enumeration of all feasible solutions for the given N. Counting for all the solutions can be challenging, as it requires the selection of the most appropriate algorithm depending on the case. The capacity of handling different N values within the code is contingent on the algorithm’s capabilities; some algorithms may be more capable of handling bigger values on N than others. 

There are many different algorithms for solving the N queen problem. In this project, I used the recursive backtracking algorithm.

## System Process Design
![image](https://github.com/user-attachments/assets/9964669e-75f5-43ad-b88b-3b4a8b967628)

The recursive backtracking algorithm works by recursively placing the queen on the chessboard one by one, and constantly checking if they are safe from each other. If a queen is under attack, the algorithm backtracks to the previous queen and find a different position where the queen can be safe. This process will continue until all queens are safely placed on the chessboard without attacking each other.

However, for certain values of ‘n’, there might not be a solution to the N Queens problem, regardless of the algorithm. When N= 1,2 or 3, there will be no solutions because there is no possible way to put two queens in a way they do not threaten each other. These are the smallest values of N for where no solution exists. To address this, the code above includes a check in the ‘main’ function to ensure that the input value of ‘n’ is valid according to the following the criteria: 
•	When n<=0, there are no solution and the code will print out an invalid input message
•	When n= 1,2,3, the code will return false and print out that there are no solutions to the n queen problem
•	When n=>4, the code will print out all possible solutions to the n queen problem
•	In addition, when n is not an integer or a whole number, the code will print out an invalid input message and ask user to input a whole number
