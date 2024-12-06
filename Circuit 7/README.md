# Circuit 7: Finite State Lock Circuit
## Concept:
After learning about finite state machines, I realized it would be a good fit for my previous lock circuit and wanted to reiterate on it. It is a combination of both a Mealy and Moore machine. The reason for the Mealy machine is because if I had used only a Moore it would have required 3 variable assignments, but an issue with the Mealy machine is that the last code entered would "unlock" the circuit without hitting the submit button, so I decided to add a third flip-flip so that when the Mealy machine was at its final state and you had the right code, instead of immedietly unlocking, you had to press the submit button to unlock.

## How it works:


## Images
### Schematic
![Circuit 7 Schematic](Circuit_7_Schematic.jpg)
![Circuit 7 Simulation](Circuit_7_Simulation.png)

## Expressions

## Parts Used:
#### 4: 7474 Dual D Flip Flops
#### 3: Push Buttons
#### 1: 7414 Schmitt Inverter
#### 1: 7404 Hex Inverter
#### 2: 7448 7 Segment Decoders
#### 2: 7 Segment Displays
#### 3: 7408 AND Gate
***
### Simulation: [Circuitverse](https://circuitverse.org/users/266288/projects/finite-state-lock-circuit)

