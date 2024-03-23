# Ex.No: 7  Logic Programming –  Logic Circuit Design
### DATE: 19/03/2024                                                                           
### REGISTER NUMBER : 212221040103
### AIM: 
To write a logic program to design a circuit like half adder and half subtractor.
###  Algorithm:
1. Start the Program
2. Design a AND gate logic if both inputs are 1 then output is 1.
3. Design a OR gate logic if any one of input is 1 then output is 1.
4. Design a XOR gate logic if both inputs are different then output is 1.
5. Design a NOT gate logic if input is 0 then output is 1.
6. Design a half adder and half subtractor using the rules.
7. Test the logic.
8. Stop the program.

### Program:
```
and(0,0,0).
and(0,1,0).
and(1,1,1).
and(1,0,0).
xor(0,0,0).
xor(0,1,1).
xor(1,0,1).
xor(1,1,0).
not(0,1).
not(1,0).
halfadder(A,B,S,C):-
    xor(A,B,S),
    and(A,B,C).
halfsubtractor(A,B,Diff,Bo):-
    xor(A,B,Diff),
    not(A,X),
    and(B,X,Bo).
```
### Output:
![313907709-31bc378d-ec6a-4b52-8d0c-e0566b189284](https://github.com/YugendarM/AI_Lab_2023-24/assets/119681539/658063e1-a577-4d49-878e-df8b1e0a0d56)
![313909066-131f693b-618d-42bc-81d9-392d0866b025](https://github.com/YugendarM/AI_Lab_2023-24/assets/119681539/465cb059-40e4-4ad1-b890-4097578fb02e)



### Result:
Thus the truth table of circuit verified sucessfully.
