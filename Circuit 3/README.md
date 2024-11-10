# Circuit 3: Lock Circuit 
## Concept:
You enter 4 different numbers into a "lock". If all four are correct and recieved in the right order, it should "unlock". 
## How it works:
The DIP switch is used to enter the code into. The code entered will go into a decoder, which will output a signal to the codes corresponding pin. Which means that if, for example, 15 was entered into the switch, then the 15 pin on the decoder would send a signal. Once the final answer is chosen by clicking the Submit button (the top one), a signal gets sent to an 2 Flip Flops. The first one is the "turn" you are on. So the first submit is the first turn, and the second submit is the second turn, etc. It works by using the Q output of the flip-flop to control the D value on the next flip-flop. If D=1 it allows you to set the flip-flop to one. The second flip-flop for each turn will set to one, only if the answer is right. The flop-flop will set to one if the corresponding turn flip-flop is set to one, if the next turn flip-flop is set to zero, and there is a signal coming from the correct codes output pin on the decoder. If the answer is right the corresponding LED will light up. To reset the circuit click the reset button (the bottom button).

## Images
### Simulation
![Circuit 3 Simulation](Circuit_3_Simulation.png)
### Schematic
![Circuit 3 Schematic](Circuit_3_Schematic.jpg)
## Parts Used:

***
### Simulation: [Circuitverse](https://circuitverse.org/simulator/edit/lock-circuit-9322b070-b124-4427-a766-c93bc677ccae)
