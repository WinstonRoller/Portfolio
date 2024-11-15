# Circuit 4: Sequential Adder/Subtracter
## Concept:
An Adder/Subtracter that lets you keep adding and subtracting. Now instead of only 2 numbers you can add or subtract as many as you like.
## How it works:
It works like a typical adder subtracter circuit, instead instead of 2 switches that determine the numbers being added, its 1 switch and a set of flip-flops. You enter one number in the switchs. Then you click the submit button. This will be the number you will add/subtract from. The second number you enter will be added on or subtracted from your first number. Once you hit submit, the answer of those 2 numbers will be loaded into the flip-flop, and you can keep adding/subtracting forever. When you want to return to 0 you can click the Reset button. The circuit will warn you of overflow if the number you want to add or subtract from will result overflow if you submit. The Flip-Flops D value is controlled by the Sum of the corresponding adder bit.

## Images
### Simulation
![Circuit 4 Simulation](Circuit_4_Simulation.png)
#### Overflow Logic
![Circuit 4 Simulation: Overflow](Overflow_Logic.png)
#### 2's Compliment
![Circuit 4 Simulation: 2's Compliment](2s_Compliment.png)
### Schematic
![Circuit 4 Schematic](Circuit_4_Schematic.png)

##### Dark Mode makes labeling hard to see. On simulation you can see labels

## Parts Used:
#### 8 - D Flip-Flop
#### 2 - Full Adder
#### 2 - Push Button
#### 1 - DIP Switch
***
### Simulation: [Circuitverse](https://circuitverse.org/users/266288/projects/sequential-adder-6b3885f1-8d23-4b58-8af6-ee33cb3daf25)
