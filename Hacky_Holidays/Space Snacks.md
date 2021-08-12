# Space Snacks (partially solved!)
### Misc, 200 points

## Question #1

<kbd><img width="700" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/space_snacks_q1.png"></kbd>

This question gives us hints with "Roten" (Rot) and "13". Using the ROT13 cipher, we find the flag.

<kbd><img width="700" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/space_snacks_q1_solved.png"></kbd>

> ctf{You_found_the_rot}

## Question #2

<kbd><img width="700" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/space_snacks_q2.png"></kbd>

This question also gives hints with "roman". Using the Caesar cipher, we find the flag.

<kbd><img width="700" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/space_snacks_q2_solved.png"></kbd>

> ctf{The_one_true_salad}

## Question #3

<kbd><img width="700" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/space_snacks_q3.png"></kbd>

More hints: "base" and "64". Decoding using base64, we find the flag.

<kbd><img width="700" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/space_snacks_q3_solved.png"></kbd>

> ctf{I_like_the_buttery_biscuit_base}

## Question #4

<kbd><img width="700" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/space_snacks_q4.png"></kbd>

Using an online Morse Code Translator, we find this flag.

<kbd><img width="700" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/space_snacks_q4_solved.png"></kbd>

> CTF:SPACEDASH2021

## Question #5

<kbd><img width="700" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/space_snacks_q5.png"></kbd>

I didn't know anything about Dockers or Containers so before looking at what Docker would never name a container, I Googled "how do Docker name containers". 

<kbd><img width="700" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/space_snacks_q5_solved1.png"></kbd>

Google tells us that if you create a new Docker container but do not give it a custom name then Docker will generate a name for you. But how do Docker randomly generate names? 

<kbd><img width="700" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/space_snacks_q5_solved2.png"></kbd>

The first link is a GitHub repository - maybe this is the source code?

<kbd><img width="700" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/space_snacks_q5_solved3.png"></kbd>

We find a line of code that tells us Docker will not name the container "boring_wozniak" because "Steve Wozniak is not boring".

> ctf{boring_wozniak}

## Question #6

<kbd><img width="700" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/space_snacks_q6.png"></kbd>



## Question #7

<kbd><img width="700" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/space_snacks_q7.png"></kbd>

This one stumped me at first. Then I realized that there were only 2 characters in this string, spaces and asterisks. I tried replacing these values with 1s and 0s and it gave me the flag!

<kbd><img width="700" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/space_snacks_q7_solve1.png"></kbd>

<kbd><img width="700" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/space_snacks_q7_solve2.png"></kbd>

> CTF{hidden_in_space}
