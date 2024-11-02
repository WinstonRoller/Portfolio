# Circuit 4: Encoder Counter
## Concept:
On my Lock Circuit I realized you could increment flip-flops. So I thought about ways I could create a counter with it.
## How it works:
Each flip-flop represents a number (1-15). Each flip-flip goes to a corresponding input pin on the encoder. The first flip-flop goes to the first pin, the second flip-flop to the second. The encoder converts the it to a 4-bit BCD value that will go to 4 LEDs that show to number. The flip-flops increment by using the output value of the previous flip-flop for the D value. So D=1 when Q=1 of the previous flip-flop. You reset the counter by clicking the reset button, which clears all the flip-flops.

## Images
### Simulation
![Circuit 4 Simulation](Circuit_4_Simulation.png)
### Schematic

## Parts Used:
#### 15 - D Flip-Flop
#### 1 - Encoder
#### 2 - Push Button
***
### Simulation: [Circuitverse](https://circuitverse.org/users/266288/projects/encoder-counter)
