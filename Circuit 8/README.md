# Circuit 5: Looping Shift Register & Point System
## Concept:
A 2-player game, there is a button for each player on either side of the board. Each player clicks the button as fast as they can until the number displayed reaches 9. Once it reaches that point the game freezes, and an LED will light up on the side of whoever one.

## How it works:
There are 3 buttons. 2 are for the players and 1 is to reset the counters. Each player has their own 4-bit ripple counter, which sends each of their numbers into a 7 segment decoder from there into a 7 segment display. The counters will only go to 9. The first player to reach 9 will stop BOTH ripple counters It stops by inhibiting the clock signal on both when it either get to 9. On each players side, there is an AND gate used to detect if the counter is 9. Once it does, a signal is sent to both an inverter and LED. The LED is used to say who won the game. The inverter goes to an AND gate with the other player's inverter. The signal from that goes to 2 AND gates, one with each players button, and that goes into the clock of the counter. To reset the counters, you have to hit the reset button. 

## Images
### Schematic
![Circuit 5 Schematic](Circuit_8_Schematic.jpg)

## Expressions
### Clock Expression
#### CLK<sub>P1</sub> = (A<sub>P1</sub>B<sub>P1</sub>'C<sub>P1</sub>'D<sub>P1</sub>)'(P1)
#### CLK<sub>P2</sub> = (A<sub>P2</sub>B<sub>P2</sub>'C<sub>P2</sub>'D<sub>P2</sub>)'(P2)

### LED Expression
#### LED<sub>P1</sub> = (A<sub>P1</sub>B<sub>P1</sub>'C<sub>P1</sub>'D<sub>P1</sub>)
#### LED<sub>P2</sub> = (A<sub>P2</sub>B<sub>P2</sub>'C<sub>P2</sub>'D<sub>P2</sub>)

##### R = Shift Right Button
##### L = Shift Left Button
##### Ld = Load Switch

### LED Expressions
#### LED<sub>1</sub> = Q<sub>A</sub> + A
#### LED<sub>2</sub> = Q<sub>B</sub> + B
#### LED<sub>3</sub> = Q<sub>A</sub> + C
#### LED<sub>4</sub> = Q<sub>A</sub> + D
#### LED<sub>point</sub> =  Q<sub>A</sub>A + Q<sub>B</sub>B + Q<sub>A</sub>C + Q<sub>A</sub>D

##### Q<sub>x</sub> = Output of Register
##### X = Output of DIP Switch

## Parts Used:
#### 1: 74194 Universal Bidirection Shift Register
#### 2: Push Buttons
#### 1: 7414 Schmitt Inverter
#### 2: 7404 Hex Inverter
#### 3: 7432 OR Gate
#### 1: 7408 AND Gate
***


