# Ex.No: 7  Logic Programming –  Logic Circuit Design
### DATE: 22/09/2025                                                                   
### REGISTER NUMBER : 212223040087
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
% Half Adder
halfadder(X, Y, Sum, Carry) :-
    xor(X, Y, Sum),
    and(X, Y, Carry).

% Half Subtractor
halfsub(X, Y, Diff, Borrow) :-
    xor(X, Y, Diff),
    not(X, Z),
    and(Z, Y, Borrow).

% Full Adder
fulladd(X, Y, Z, Sum, Carry) :-
    xor(X, Y, A),
    xor(A, Z, Sum),
    and(A, Z, B),
    and(X, Y, C),
    or(B, C, Carry).

% Logic Gates
xor(0,0,0).
xor(0,1,1).
xor(1,0,1).
xor(1,1,0).

and(0,0,0).
and(0,1,0).
and(1,0,0).
and(1,1,1).

or(0,0,0).
or(0,1,1).
or(1,0,1).
or(1,1,1).

not(0,1).
not(1,0).
```

### Output:
<img width="933" height="261" alt="image" src="https://github.com/user-attachments/assets/bd8bf2fc-2389-42de-98c8-3da4b159ecaa" />

### Result:
Thus the truth table of circuit verified sucessfully.
