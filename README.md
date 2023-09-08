# Experiment--04-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure


Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.
#### OR Gate:
The OR gate is a fundamental digital logic gate that operates on two binary inputs, producing an output of 1 if at least one input is 1. It symbolizes logical disjunction and is essential in building logical circuits and decision-making processes in computers and electronics.
#### AND Gate:
The AND gate is a fundamental digital logic gate with two inputs and one output. It produces a high output (1) only when both input signals are high (1). If any input is low (0), the output remains low. It's a building block for more complex logic circuits and is integral in digital computations.
#### NOT Gate:
The NOT gate is a fundamental digital logic gate. It has a single input and a single output. The output is the inverse of the input: if the input is high (1), the output is low (0), and vice versa. It's a basic building block in digital circuits, used for logic inversion.

Write the detailed procedure here 


## Program:


```
Developed by: VIKASH S
RegisterNumber:  212222240115
```
```
module expthree(a,b,diff,borr);
input a,b;
output diff,borr;
assign difference = (a^b);
assign borrow = (~a&b);
endmodule
```
```
module exp4_2(a,b,bin,diff,borrow);
input a,b,bin;
output diff,borrow;
assign diff=a^b^bin;
assign borrow=~a&b|(~(a^b)&bin);
endmodule

```






## Output:
## Truthtable
#### Half subtractor:

![image](https://user-images.githubusercontent.com/119091638/234605817-b29c4306-b2f0-4e98-8487-a4bd6a1d75d9.png)

#### Full subtractor:

![image](https://user-images.githubusercontent.com/119091638/234605931-2920dd58-1f35-425a-b113-1fb507728213.png)



##  RTL realization
#### Half subtractor:
![rtl1](https://github.com/vikashsenthil21/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119433834/368e58bd-ea4d-4dc4-beeb-52c5ab15417c)

#### full subractor:


![rtl2](https://github.com/vikashsenthil21/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119433834/641e8826-27c4-4b3e-8ab7-713e6bdd736e)




## TIMING DIAGRAM
#### Half subtractor:
![ex4 otput 1](https://github.com/vikashsenthil21/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119433834/0609c676-199e-4c70-a644-89456b605330)

#### full subractor:

![exp4 out 2](https://github.com/vikashsenthil21/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119433834/cf4d20c2-2f59-4af0-a514-5d6b6addd261)




## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
