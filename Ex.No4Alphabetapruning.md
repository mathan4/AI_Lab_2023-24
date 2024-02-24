# Ex.No: 4   Implementation of Alpha Beta Pruning 

### DATE
24 / 02 / 2024

### REGISTER NUMBER
212221040103

### AIM 
Write a Alpha beta pruning algorithm to find the optimal value of MAX Player from the given graph.

### Algorithm
1. Start the program
2. Initially  assign MAX and MIN value as 1000 and -1000.
3.  Define the minimax function  using alpha beta pruning
4.  If maximum depth is reached then return the score value of leaf node. [depth taken as 3]
5.  In Max player turn, assign the alpha value by finding the maximum value by calling the minmax function recursively.
6.  In Min player turn, assign beta value by finding the minimum value by calling the minmax function recursively.
7.  Specify the score value of leaf nodes and Call the minimax function.
8.  Print the best value of Max player.
9.  Stop the program. 

### Program:
```
# Initial values of Alpha and Beta
MAX, MIN = 1000, -1000
def minimax(depth, nodeIndex, maximizingPlayer, values, alpha, beta):
    if depth == 3:
        return values[nodeIndex]
    if maximizingPlayer:
        best = MIN
        # Recur for left and right children
        for i in range(0, 2):
            val = minimax(depth + 1, nodeIndex * 2 + i, False, values, alpha, beta)
            best = max(best, val)
            alpha = max(alpha, best)
            # Alpha Beta Pruning
            if beta <= alpha:
                break
          
        return best
    else:
        best = MAX
 
        # Recur for left and
        # right children
        for i in range(0, 2):
            val = minimax(depth + 1, nodeIndex * 2 + i, True, values, alpha, beta)
            best = min(best, val)
            beta = min(beta, best)
            # Alpha Beta Pruning
            if beta <= alpha:
                break
        return best
      
values = [3, 5, 6, 9, 1, 2, 0, -1] 
print("The optimal value is :", minimax(0, 0, True, values, MIN, MAX))
```
### Output
![image](https://github.com/NithishThirumalai/AI_Lab_2023-24/assets/114301782/7296ce98-b9fa-4443-b859-ad9c31b089cd)


### Result
Thus the best score of max player was found using Alpha Beta Pruning.
