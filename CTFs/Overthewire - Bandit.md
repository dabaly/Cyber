This is a writeup of my first CTF experience. Here you will find my solutions to each level of the bandit challenges along with my understanding and explanation of the challenge concept and its solution.
Overthewire:Bandit s a beginner level CTF that tests and teaches the learner how to navigate and use a linux machine using terminal commands. It uses remote machines that can be accessed via openssh with the hostname, port and username of the machine used for each specific level being provided. Each level presents a technical challenge which the user must solve to gain the information needed to proceed to the next machine/level.
Hostname: **bandit.labs.overthewire.org**
Port: **2220**
Username: **bandit0-bandit34** (Depends on the level)
## Level 0
The end goal of this level is to demonstrate the ability to remotely access a machine using openssh given the hostname, port, username and password (**bandit0**). It also tests the ability to read the content of a file.
Basic command format to login to a machine using ssh given the above information is:
`ssh username@hostname -p port`
For this level:
`ssh bandit0@bandit.labs.overthewire.org -p 2220`
The password is stored on a file in the current directory. Its contents can be read using:
`nano bandit0`

