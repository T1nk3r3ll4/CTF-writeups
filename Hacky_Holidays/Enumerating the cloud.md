# Enumerating the cloud (solved!)
### Cloud, 125 points

## Description

<kbd><img width="500" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/EnumCloud_ChallInfo.png"></kbd>

## Question 1

<kbd><img width="500" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/EnumCloud_q1.png"></kbd>

When inspecting the page code, we see a link to a png file.

<kbd><img width="600" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/enum_the_cloud_q1_solve1-1.png"></kbd>

Let's check out the directory that the image is in...

<kbd><img width="500" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/enum_the_cloud_q1_solve1-2.png"></kbd>

We see a file called "flag.txt". Open it and we get our first flag!

<kbd><img width="400" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/enum_the_cloud_q1_solve1-3.png"></kbd>

> CTF{0841862F273FD2CA20EA3B94A645781071AB19D7}

## Question 2

<kbd><img width="500" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/EnumCloud_q2.png"></kbd>

<kbd><img width="400" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/enum_the_cloud_q1_solve2-1.png"></kbd>

On the same page where we seen "flag.txt", we also see "external-information-panel.txt". Let's open it!

<kbd><img width="400" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/enum_the_cloud_q1_solve2-2.png"></kbd>

Another link to go to...

<kbd><img width="500" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/enum_the_cloud_q1_solve2-3.png"></kbd>

"405 Request method 'GET' not allowed". Can we try other methods such as POST or PUT using Burp Suite?

<kbd><img width="600" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/enum_the_cloud_q1_solve2-4.png"></kbd>

Bingo! Using PUT through the Repeater in Burp Suite gives us the next flag! (If we scroll down further here then we get the Key & Key ID for the next question).

> CTF{9177A9C8BB1CD5C85934}

## Question 3

<kbd><img width="500" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/EnumCloud_q3.png"></kbd>

<kbd><img width="600" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/enum_the_cloud_q1_solve3-1.png"></kbd>

Continuing to scroll down in Burp Suite (from the last question), we see the AWS Secret Access Key and the AWS Access Key ID.

<kbd><img width="500" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/enum_the_cloud_q1_solve3-2.png"></kbd>

$ aws configure

<kbd><img width="500" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/enum_the_cloud_q1_solve3-3.png"></kbd>

My teammate [ravirajpowar](https://twitter.com/ravirajpowar) figured out most of the questions for the Enumerating the Cloud challenge so I'm going to turn to his Discord messages to us to document the steps for the remaining questions!

<kbd><img width="400" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/enum_the_cloud_q1_solve3-4.png"></kbd>

> CTF_855CC724FD34896C8875

## Question 4

<kbd><img width="500" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/EnumCloud_q4.png"></kbd>

<kbd><img width="400" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/enum_the_cloud_q1_solve4-1.png"></kbd>

<kbd><img width="500" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/enum_the_cloud_q1_solve4-2.png"></kbd>

<kbd><img width="500" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/enum_the_cloud_q1_solve4-3.png"></kbd>

<kbd><img width="300" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/enum_the_cloud_q1_solve4-4.png"></kbd>

> CTF_20324408A4E3F5C1D54D

## Question 5

<kbd><img width="500" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/EnumCloud_q5.png"></kbd>

<kbd><img width="400" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/enum_the_cloud_q1_solve5-1.png"></kbd>

<kbd><img width="400" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/enum_the_cloud_q1_solve5-2.png"></kbd>

> CTF_98F960B4D86BBCFE3FE1
