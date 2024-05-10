# Ex.No: 7  Logic Programming –  Logic Circuit Design
### DATE: 16/03/24                                                                           
### REGISTER NUMBER : 212221060256
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
### Half Adder
```
xor(0,1,1).
xor(1,0,1).
xor(1,1,0).
xor(0,0,0).
and(1,1,1).
and(0,0,0).
and(1,0,0).
and(0,1,0).
halfadder(A,B,S,C):-
    xor(A,B,S),
    and(A,B,C).
```
### Half Subtractor
```
xor(0,1,1).
xor(0,0,0).
xor(1,0,1).
xor(1,1,0).
and(1,1,1).
and(0,0,0).
and(0,1,0).
and(1,0,0).
not(0,1).
not(1,0).
halfsubtractor(A,B,Diff,Bor):-
    xor(A,B,Diff),
    not(A,C),
    and(C,B,Bor).
```
### Output:
### Half Adder
![image](https://github.com/Shyamonyou/AI_Lab_2023-24/assets/123711349/235f7245-0438-41a3-afd8-a773312ac4b7)

### Half Subtractor
![image](https://github.com/Shyamonyou/AI_Lab_2023-24/assets/123711349/c86c6a10-131c-4b9b-b3a9-79d29851f247)



### Result:
Thus the truth table of circuit verified sucessfully.
