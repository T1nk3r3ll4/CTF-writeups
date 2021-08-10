# TEASER: su admin (solved!)
### Web, 50 points

## Description

<kbd><img width="700" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/admin_flag_question.png"></kbd>

## Solution
First, let's check out the admin_flag.png

<kbd><img width="275" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/admin_flag.png"></kbd>

My first thought was to see if we could just inspect the code to get the url for the admin_flag.png file then paste that url into the code for our flag...

<kbd><img width="700" alt= "" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/admin_flag_first%20attempt1.png"></kbd>

<kbd><img width="700" alt= "" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/admin_flag_first%20attempt1-2.png"></kbd>

This wouldn't actually change our flag though, it would just appear to be changed, and it was not the answer.

I could replicate the entire flag except for Overlay #1.

<kbd><img width="500" alt= "" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/admin_flag_solve1-1.png"></kbd>

I looked in the code, found the number from Overlay #1...

<kbd><img width="700" alt= "" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/admin_flag_solve1-2.png"></kbd>

then incremented it by 1 to 15. There was the flag!

<kbd><img width="700" alt= "" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/admin_flag_solve1-3.png"></kbd>

> CTF{YOU-HAZ-ADMIN-FLAG}
