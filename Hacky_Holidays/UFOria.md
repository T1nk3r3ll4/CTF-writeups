# UFOria (solved!)
### Web / OSINT , 150 points

## Question #1

<kbd><img width="800" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/UFOria_q1.png"></kbd>

<kbd><img width="500" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/UFOria_q1_solve1-1.png"></kbd>

Clicking around the website. Clicked on "Contact Us"...

<kbd><img width="500" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/UFOria_q1_solve1-2.png"></kbd>

I got a pop-up that asked for an invite code.

<kbd><img width="500" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/UFOria_q1_solve1-3.png"></kbd>

Inspecting the code on the page, it tells us that the code is 12 characters in length in the format of XXX-XXXX-XXX.

Looking through each "if", we see that: the first 3 letters are "UFO",

<kbd><img width="500" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/UFOria_q1_solve1-4.png"></kbd>

Googling "btoa", we see that the next step should be "UFO" encoded as base64. This gives us "VUZP".

<kbd><img width="500" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/UFOria_q1_solve1-5.png"></kbd>

And lastly, I Googled the function charCodeAt() which gave me the website above that I could use to get the answer to the third part. charCodeAt() returns a Unicode value for a character in a specific position in a string (in this case, our string is "UFO"). Once we get this value for each character in "UFP", we add them together. 85 + 70 + 79 = 234.

> UFO-VUZP-234

## Question #2

<kbd><img width="800" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/UFOria_q2.png"></kbd>

In order to access the members-only area, we should look for a username and/or password.

<kbd><img width="600" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/UFOria_q2_solve2-1.png"></kbd>

In the "About" page we see the nickname "borgana" - maybe this could be a username?

<kbd><img width="400" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/UFOria_q2_solve2-2.png"></kbd>

Let's go to the "Members" page and click "I've forgotten my password." to test it out.

<kbd><img width="300" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/UFOria_q2_solve2-2-2.png"></kbd>

<kbd><img width="300" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/UFOria_q2_solve2-3.png"></kbd>

This confirms it is a username! Now to figure out borgana (aka Ben Organa, the UFOria CEO)'s place of birth.

<kbd><img width="600" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/UFOria_q2_solve2-4.png"></kbd>

We see on the "About" page that Ben went on a trip to his place of birth with someone named Elliot Talton.

<kbd><img width="300" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/UFOria_q2_solve2-5.png"></kbd>

Looking through UFOria's social media accounts, we can see there is an employee listed on LinkedIn, and that employee is none other than Elliot Talton!

<kbd><img width="400" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/UFOria_q2_solve2-6.png"></kbd>

Elliot posted a message talking about a Cafe that reminds him of childhood memories - maybe Elliot and Ben are from the same hometown where this cafe is located?

<kbd><img width="400" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/UFOria_q2_solve2-7.png"></kbd>

Google says that the cafe is located in a placed called "bourtange".

<kbd><img width="400" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/UFOria_q2_solve2-8.png"></kbd>

We put this as the answer to borgana (Ben)'s secret question and we see that his password is "fataborgana42".

<kbd><img width="400" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/UFOria_q2_solve2-9.png"></kbd>

Lets go ahead and sign in.

<kbd><img width="300" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/UFOria_q2_solve2-10.png"></kbd>

Success! We got the flag!

> CTF{fataborgana42}
