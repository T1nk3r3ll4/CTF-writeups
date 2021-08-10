# Unidentifi3d Flying Object (solved!)
### Stego, 100 points

## Description

Question #1

<kbd><img width="700" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/UFO_q1.png"></kbd>

Question #2

<kbd><img width="700" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/UFO_q2.png"></kbd>

## Solution

My teammate [@jaymiee__](https://twitter.com/jaymiee__) figured out this one. He manually looked at the code and found the printer type.

<kbd><img width="500" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/UFO_q1_solve1.png"></kbd>

> geeetech_A10M

The website gcode.ws allows you to open a file with the extension gcode. These files are for 3D printing. Doing this and playing with the settings allowed us to see the flag "Flying_saucer". The question gives us a hint about "layers" so I imagine there is a more sophisticated way of doing this as well.

<kbd><img width="500" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/UFO_q2_solve1.png"></kbd>

> CTF{Flying_saucer}
