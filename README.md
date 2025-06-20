# rye-bread-board
![image](https://github.com/user-attachments/assets/7f449cb1-57ff-4fca-83d4-30ec8acebabe)

The Rye Bread Board is a split ergo mechanical keyboard. Inspired by the Ferris Sweep, it has a similar architecture, with the most notable difference being the fanned out thumb structure. The name Rye Bread comes from the nickname I gave my pup who recently passed. His paw is printed on the PCB.

A writeup of the design choices can be found on my [website](https://www.davidboland.dev/blog/custom-keyboard-build-rye-bread-board). Assembly notes can be found below.

## Provided In this Repo:
Kicad file for the PCB design
STL file for the bottom plate
keymap json file for QMK configurator

## Components:
2 x Promicro Controllers 
2 x TRRS Cable Jacks
1 x TRRS Cable
2 x PCB boards (Same for each hand, just flipped)
34 x MX Style Switches
34 x compatible keycaps
1 x USBc cable

## Assembly Notes
- The STL file has the design for one half of the board. In order to create one for each hand, you can mirror the model on the board and print both simultaneously.
- The left handed PCB is the one with the paw print facing up. The right is reversed.
- The microcontroller on the left hand is inverted, right side up for the right hand.
- It is recommended that the micro controller is not pushed down all the way when soldering to the left hand. If it is pushed down all the way, it will be more difficult to fit thicker USBC cables.

## Keymapping
One improvement I would have made to the keyboard is to map the switches on the board to the same pins as the Ferris Sweep. This would allow for using the exact same QMK configuration. Because they are not mapped one to one, I should fork QMK and create my own mapping. Temporarily I just looked at my mappings compared to the sweep and switched the keys were appropriate. I could then use the default Ferris Sweep configuration in QMK and upload my keyboard json. For this reason, if you load the keyboard json file into QMK the mapping will not look correct.

The mappings are as follows:
RYE BREAD BOARD          FERRIS SWEEP
B6 F7 F6 F5 F4           F4 F5 F6 F7 B6
D3 B2 B3 B1 D1           D1 B1 B3 B2 D3
C6 D7 E6 B4 D0           B5 B4 E6 D7 C6
         D4 D0                    D0 D4
