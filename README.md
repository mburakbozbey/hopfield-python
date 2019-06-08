# Implementation of Discrete Hopfield Model
## Objective:
**Pick** 5 numbers from 1 to 5.  
**Plot** the numbers in 10x10 grid by setting high (dark) and low(light) on the grid to visualize those numbers.  
**Implement** the Hopfield algorithm given in the class.
**Distort** the original sample patterns by adding randomly generated points to each pattern and iterate until convergence.

![Image](https://i.ibb.co/SK0vDXj/Ads-z.png)

## Implementation: 
**Step 1:**  Numbers  1,2,3,4 and 5 were written with “X”s and dots. In this array of strings, dots represent null values and “X”s represents” parts of a given number. These 100 character transformed to 1 for “X” and -1 for dots. Initial look at numbers in 10x10 grid by setting high (dark) and low (light) on the grid to visualize those numbers.:
![Image](https://i.ibb.co/ftfVtSH/1.png)
**Step 2:** To compute the weights for each connection denoted by  t_{ij} , a 10x10 weight matrix initialized with random gaussian distribution. After that, inner products were summed for each sampler. Diagonal indices were set to zero.
**Step 3:** Test images were created to see stability of the network. After adding noise with mean zero and variance 2 to distort images:
![Image](https://i.ibb.co/p67q9WC/2.png)
**Step 4:** In every iteration, hard limiting nonlinearity applied to the dot product of noisy patterns and weight matrix:
![Image](https://i.ibb.co/bFq9Khr/3.png)
**Step 5:** When the noise increased to the 4, all samples converged to desired values except noisy 2, it’s converged to the 1:
![Image](https://i.ibb.co/6XDrC3T/4.png)
