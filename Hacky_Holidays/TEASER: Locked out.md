# TEASER: Locked out (solved!)
### Cloud, 50 points

## Description

Question 1

<kbd><img width="700" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/Teaser_locked_out_question1.png"></kbd>


Question 2

<kbd><img width="700" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/Teaser_locked_out_question2.png"></kbd>

## Solution

When going to the "external storage" link in the question, we see "external-spaceship-storage.txt". Adding this to the end of the url gives us a file.

<kbd><img width="600" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/Teaser_locked_out_q1_solve1.png"></kbd>

This file gives us a flag! Plus it also gives us other text. I had no idea what this text was or what to do with it, but [ravirajpowar](https://twitter.com/ravirajpowar) figured it out!

<kbd><img width="400" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/Teaser_locked_out_q1_solve2.png"></kbd>

> CTF{6c2c45330a85b126f551}

The text that we see in the last file was an AWS Access Key ID and an AWS Secret Access Key.

Using the following steps gives you the flag!

> $ aws configure

> input the access key ID and the secret access key

> $ aws s3 ls

> $ aws s3 ls internal-spaceship-storage-fdde98f

> $ aws s3 cp s3://internal-spaceship-storage-fdde98f/spaceship-keys key

> $ cat key

<kbd><img width="400" src="https://github.com/T1nk3r3ll4/CTF-writeups/blob/main/Hacky_Holidays/images/Teaser_locked_out_q2_solve.png"></kbd>

> CTF{4ABABEDE5580D9A22A2A}
