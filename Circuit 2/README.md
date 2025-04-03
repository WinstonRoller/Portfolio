# Circuit 2: 8-bit Adder-Subtracter 
## Concept:
There are 2 switches, 1 for each number. There is also a mode select switch to select between addition or subtraction. When the switch is off, it adds the 2 numbers, and when it is on it subtracts. 
## How it works:
This circuit adds or subtracts number B (bottom switch) from A (top switch). Each bit from number B is XORed with the output of the mode select. Off = Add, On = Subtract. If it’s subtracted the bits will be inverted, and the mode switch sends a bit through the carry-in on the adder, making the value negative. There are 2 adders, the first one handles the 4 least significant bits, and the second one handles the most significant bits. If an overflow occurs, then the blue LED will light up. Since this circuit uses 2's compliment the range of numbers possible are -128 to 127.

## Images
### Schematic
![Circuit 2 Schematic](Circuit_2_Schematic.png)

## Truth Tables & Expressions
### Table for Addition:		
| A B<sub>F</sub> C<sub>in</sub> | ∑   | C<sub>out</sub> |	
| :----------: | :-: | :----: |
| 0 0 0	       | 0	 | 0      | 
| 0 0 1 	     | 1	 | 0	    |	
| 0 1 0        | 1   | 0	    |	
| 0 1 1        | 0	 | 1	    |
| 1 0 0	       | 1	 | 0      |
| 1 0 1        | 0	 | 1      |
| 1 1 0	       | 0   | 1      |
| 1 1 1        | 1   | 1      |

#### Expression for ∑ of each bit:
∑ = AB<sub>F</sub>’ + A’B<sub>F</sub> or ∑ = A XOR B<sub>F</sub>

#### Expression for Cout:
C<sub>out</sub> = A * B<sub>F</sub>

###### B<sub>F</sub> = B final

### Table for XOR’s (Inverting the numbers)
|B<sub>I</sub> M |	B<sub>F</sub> |
| :---: | :--: |
| 0	0   | 0    |
| 0 1   | 1    |
| 1 0   | 1    |
| 1 1   | 0    |

#### Expression for B<sub>F</sub>: 
B<sub>F</sub> = B<sub>I</sub>’M + B<sub>I</sub>M’ or B<sub>F</sub> = B<sub>I</sub> XOR M

###### B<sub>I</sub> = B initial
###### B<sub>F</sub> = B final

### Table for Overflow:	
| A<sub>4</sub> B<sub>F4</sub> ∑<sub>4</sub> | O |
| :----------: | :-: |
| 0 0 0	       | 0	 | 
| 0 0 1 	     | 1	 |
| 0 1 0        | 0   |
| 0 1 1        | 0	 |
| 1 0 0	       | 0	 |
| 1 0 1        | 0	 |
| 1 1 0	       | 1   |
| 1 1 1        | 0   |

#### Expression for O
O = A<sub>4</sub>B<sub>F4</sub>∑<sub>4</sub>' + A<sub>4</sub>'B<sub>F4</sub>'∑<sub>4</sub>

###### A<sub>4</sub> = MSB of A
###### B<sub>4</sub> = MSB of B
###### ∑<sub>4</sub> = MSB of Sum

## Parts Used:
### 3: DIP Switch
### 2: 74283 4-bit full adder
### 2: QUAD XOR gate
### 25: 220 Ohm Resistors
### 8: Red LED
### 1: Quad OR gate
### 1: Quad AND gate
### 1: Hex Inverter

***
### Simulation on TinkerCAD
