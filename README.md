# Implementation of Discrete Hopfield Model
## Objective:
**Pick:** 5 numbers from 1 to 5.  
**Plot:** the numbers in 10x10 grid by setting high (dark) and low(light) on the grid to visualize those numbers.  
**Implement:** Hopfield algorithm given in the class.  

## Procedure:
Discrete Hopfield Model
Procedure
The Hopfield Network is comprised of a graph data structure with weighted edges and separate procedures for training and applying the structure. To compute connection weight matrix\ \ \mathbit{t}_{\mathbit{ij}}\ \ :
x_i^s\ \ \ : sample patterns ith element, {-1,+1}
t_{ij}\ \ \ : connection weight from i to unit j
N\ \ \ \ :  input pattern dimension
t_{ij}\ \ \ =\ \ \sum_{s=0}^{m-1}x_i^s.x_j^s\      , i\neq j  \ \ for\ \ \ 0\lei,j\le N-1
                     0                                 , i=j
In computer code, weight matrix created by summing outer matrix product of every element in pattern :
