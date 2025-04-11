[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/oLa9XOfW)
# Finova Cybersecurity - Task 2: Learning Commands  #

:wave:
Welcome to the __Cyber Security__ Domain!

For the __first__ task, you installed a Linux distro and set it up.

For your __second task__, you will:

- Learn how to navigate Linux using commands.

_"Why do we need to use commands?"_ 

__Once you get the hang of it, using commands to navigate through your desktop will be much, much faster (and convenient!)__ 

Not to mention, as you participate in _CTFs_ or _Bug Bounties_, knowledge of linux commands will be necessary to be __competent.__

__With that being said, it doesnt have to be a boring process!__

## Step 1: Create an account on pwn.college ##

- Go to [pwn.college](https://pwn.college/)

- Create an account.

## Step 2: Connect via SSH
- __Open__ your Linux Terminal.

- __Run: `ssh-keygen -f key -N ''`__

This will generate files `key` and `key.pub`, which are your _private_ and _public_ keys respectively.

<img width="454" alt="{DF626839-9678-4389-AD17-6F3190E0A2A3}" src="https://github.com/user-attachments/assets/5d7b17b9-1635-4472-90c3-a56f94fd6a3e" />



- __Run: `cat key.pub`.__ The cat command will display the contents of the `key.pub` file to you.

<img width="653" alt="{DC4A3E4F-C71C-4AB8-A70A-1556CB207136}" src="https://github.com/user-attachments/assets/e0b7a1b2-2cee-4aff-947f-9d6a0efd0b41" />


- __Copy the contents of `key.pub`__
  
- Go to the __Settings__ tab in pwn.college. Then head over to the __SSH key__ section.

- Paste `key.pub` in the __SSH Key__ section.

<img width="789" alt="{3516623B-98D4-4A9C-A036-92D0A57CE457}" src="https://github.com/user-attachments/assets/9d69773d-ba11-41e1-aaa8-1b7afff18fad" />

- __Run: `ssh -i key hacker@pwn.college`.__ Type __yes__ when prompted.

<img width="596" alt="{2BB3AC29-2AA9-4BAE-B7F6-3EF20A006467}" src="https://github.com/user-attachments/assets/232f7225-a4f6-446d-bb3b-d7206b9742eb" />


## Step 3: Linux Luminarium

- On [pwn.college](https://pwn.college/), click on __Dojos__.

- Head to the __Linux Luminarium__ Dojo.

- Complete the __first 6 modules (Till Practicing Piping)__


__Note:__ You can also use pwn.college's __GUI Desktop Workspace__ to solve challenges (If you dont want to connect via SSH).

<img width="816" alt="{A5012E04-DD44-4EFB-A2A8-D1CA521AAB11}" src="https://github.com/user-attachments/assets/563cfcb4-64a6-4610-b447-f615f4b3482e" />



## Submission

- Create __writeups (in this repo)__ for each challenge, __with the flag (and how you got the flag)__

For example:

Module 1.md

```
Module 1: Hello Hackers

Intro To Commands

Flag: pwn.college{89T2ov5QdYyikKlBF9wnlLpPBG6.ddjNyUDL0QjN5YzW}

Solution: I typed "hello" in the terminal and got the flag.

```

You can also include pictures to explain in more detail.

__If you have already created writeups for the modules, just post the link to the github repository where you wrote them!__

Good Luck! If you have any doubts, feel free to message me or in the groupchat!


 






