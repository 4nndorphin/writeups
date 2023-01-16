# SINCON CTF Badge
It was a great start to the year with [SINCON Reloaded Conference](https://www.infosec-city.com/sinrlcon) which hosted various talks, workshops, villages (and more). Having only experienced the conference virtually the last 2 editions, it was exciting to attend this year's conference IRL. And... to receive a hardware badge! 

![image](https://github.com/4nndorphin/writeups/blob/main/img/Screenshot 2023-01-15 at 23.43.41.png)

This year's badge was designed by [Abhinav Pandagale](https://twitter.com/tweetsfrompanda) and features the iconic [Khong Guan Building](https://www.ura.gov.sg/Corporate/Resources/Publications/Skyline/Skyline-Issue10/AHA#:~:text=charm%20to%20it.-,Khong%20Guan%20Building,-2018%20Architectural%20Heritage) in Singapore. It consists of 2 parts; soldering of LEDs and a CTF. The CTF contains a bunch of crypto and OSINT challenges when solved, unlocks the corresponding LEDs and makes the badge LIT.

![image](https://github.com/4nndorphin/writeups/blob/main/img/ctf_badge.png)

_Source: [Infosec In the City](https://twitter.com/Infosec_City)_

And so the adventure begins [here](https://hackerwares.in/sincon) where instructions can be found.

## Badge Soldering
The [LED Soldering Tutorial](https://www.hackerwares.in/sincon.pdf) provides concise steps with tips and tricks. The LEDs were tiny but my [_palms are sweaty, knees weak, arms are heavy_](https://www.youtube.com/watch?v=k5jg6xahxr4) so this task proved to be challenging. Multiple profanities and deep inhalations of solder fumes later (and not realising there was 1 unsoldered LED until the next day): 

![[9E1A71EC-5C0E-411D-9C86-B3AEBE6D5286.jpeg)

However, we won't know if we soldered them LEDs correctly until we complete the CTF. Onwards!

## Badge CTF
Many thanks to fellow SINCON crew and participants for whom I would not have been able to complete this CTF without! 
https://learn.sparkfun.com/tutorials/terminal-basics/arduino-serial-monitor-windows-mac-linux

![image](https://github.com/4nndorphin/writeups/blob/main/img/Screenshot 2023-01-07 at 18.42.44.png)

![image](https://github.com/4nndorphin/writeups/blob/main/img/Screenshot 2023-01-07 at 18.43.13.png)

![image](https://github.com/4nndorphin/writeups/blob/main/img/Screenshot 2023-01-07 at 18.43.47.png)

![image](https://github.com/4nndorphin/writeups/blob/main/img/Screenshot 2023-01-07 at 18.45.29.png)

In Arduino, go to Tools > Board > Uno, and Port > Serial port. Open the Serial Monitor

Enter `***` into console launch the CTF

### Lobby

```
				 ++++++  -+++++*:
               .*=             .#:
               .#-  -========-  .*=
             :-  *++*.       ++   *+
             .#=  +#   ----:  +*   :
           :   *+  -#. ::::#-  :.   :*.
           *=   =.  :#:     *=  .*.  -#
            +:    =  .#=---  +*  -#.  .
              =   =#.  ....   #*. :#:
              -#.  -#-:::::::*=-#. ..
               :#:  .:::::::::  :#:
                .#-             +*
                  ++++++: .+++++=

You have reached the ground floor. The stairs seem inaccessible, is the elevator too? You wonder. The elevator lights are still glowing. But the elevator needs a passcode.
What could be the passcode? A closer inspection revealed finger prints on a few metallic keys with braille dots.
```

Braille dots printed on the lanyard that came with the E-badge
![image](https://github.com/4nndorphin/writeups/blob/main/img/C2FA24F2-F6CB-434B-B0F6-712D55C8ED0D.jpeg)

![image](https://github.com/4nndorphin/writeups/blob/main/img/Pasted image 20230106142839.png)

```Answer
368078
```

```
Success! The elevator is now unlocked.


 Ting! Select your floor.

 (1)(2)

 (3)(4)

 (5)(6)
```


### 1st Floor

```
The lift doors open to a mesmerising aroma of coffee and biscuits. You find

neatly stacked shelves of cookies. And then some on the counter along with a

trail. A cookie crumbs trail that looks mysteriously organised...

       :-+++====-:.           :-=++===+=:.
      =*+*+====*====         =*+-*====*+==:
     -++=====*=--==+:       :++---===*+=-
    :++===+==--+=-===      :++=--+=*+=:       .-.  .
    ++**-==+==-=-===+:     =+**===+--=.      -...  .-
    +++---=+=====++++.     =++====+=-==-       -.-  .
    :*+--**+==+==*++=      .**+++*----==:.      -..
      .+**+++++*++++-        .+**+++--*+++=
        :========-.            :-=======-..
```

```
.-.  . -...  .- -.-  . -..
```

![image](https://github.com/4nndorphin/writeups/blob/main/img/Screenshot 2023-01-07 at 18.51.06.png)

```Answer
rebaked
```

```
Success! The floor is unlocked.

 Ting! Select your floor.

 (1)(2)

 (3)(4)

 (5)(6)
```

### 2nd Floor

```
Floor 2 is an office. A row of computers sitting idle except one that keeps flickering, asking for a password. You take the seat. Making the best of your social engineering guesses about the password. You try and find out it's clearly not the employee's name. Nor the top 10 most used passwords. What could it be?
Perplexed, you look outside the window. There's a building right opposite with a big sign on it. It doesn't hurt to try and so you do?...
```

Post code is 1 number off from the previous flag
 ![image](https://github.com/4nndorphin/writeups/blob/main/img/Screenshot 2023-01-07 at 18.53.23.png)

![image](https://github.com/4nndorphin/writeups/blob/main/img/Screenshot 2023-01-07 at 18.55.08.png)

```Answer
trivex
```

```
Success! The floor is unlocked.

 Ting! Select your floor.

 (1)(2)

 (3)(4)

 (5)(6)
```

# 3rd Floor

```
Floor 3 opens to a room full of documents and some photographs. And a note asking to upload and share the documents and pictures on social media. But there are no social media histories in the computer browser you tried on floor 2.
You give documents an overview and they seem to hold the email ID :
sincon@hackerwares.in in their signature. Would it be possible to locate this socialmedia handle?
```

Reverse email look up didn't yield much 

![image](https://github.com/4nndorphin/writeups/blob/main/img/907EF62C-70CC-4862-9A0B-46334F7A9216.jpeg)

```Answer
sinconnoisseurs
```

```
Success! The floor is unlocked.

 Ting! Select your floor.

 (1)(2)

 (3)(4)

 (5)(6)
```

### 4th Floor

```
The document retrieved on the third floor talks about a particular social media

post of a hacker eating a cookie in an AESthetic way. It'd be interesting to dig

deeper into what's going on.
```

![image](https://github.com/4nndorphin/writeups/blob/main/img/Screenshot 2023-01-06 at 12.34.32.png)

```
4d6baebb8227248d2e1a5eb7c6fa8442bc6e2edc80f4c297a3329b9a46ba955c05d516b79a965bdfed3f116c70f651b0
```

![image](https://github.com/4nndorphin/writeups/blob/main/img/Screenshot 2023-01-07 at 19.12.29.png)

![image](https://github.com/4nndorphin/writeups/blob/main/img/Screenshot 2023-01-07 at 19.02.24.png)

Rude, but okay hahaha
![image](https://github.com/4nndorphin/writeups/blob/main/img/Screenshot 2023-01-07 at 19.03.59.png)

![image](https://github.com/4nndorphin/writeups/blob/main/img/Screenshot 2023-01-06 at 12.33.24.png)

![image](https://github.com/4nndorphin/writeups/blob/main/img/Screenshot 2023-01-06 at 12.28.43.png)

![image](https://github.com/4nndorphin/writeups/blob/main/img/Screenshot 2023-01-11 at 01.03.16.png)

```Answer
cookie sniffing
```

```
Success! The floor is unlocked.

 Ting! Select your floor.

 (1)(2)

 (3)(4)

 (5)(6)
```

# 5th Floor

```
The lift opens to a mysterious painting. At first, perplexing and yet in

some way weirdly organised. On the side is a note with gibberish 

written on it that says

"aGFja2Vyd2FyZXMgaW4gc2luaXN0ZXI="

What this could be?
```

![image](https://github.com/4nndorphin/writeups/blob/main/img/Screenshot 2023-01-11 at 00.56.02.png)

```
hackerwares in sinister
```

![image](https://github.com/4nndorphin/writeups/blob/main/img/Screenshot 2023-01-11 at 00.57.54.png)

![image](https://github.com/4nndorphin/writeups/blob/main/img/Screenshot 2023-01-07 at 19.13.12.png)

![image](https://github.com/4nndorphin/writeups/blob/main/img/Screenshot 2023-01-11 at 00.56.46.png)

![image](https://github.com/4nndorphin/writeups/blob/main/img/Screenshot 2023-01-11 at 00.59.00.png)

![image](https://github.com/4nndorphin/writeups/blob/main/img/Screenshot 2023-01-06 at 12.45.58.png)

```Answer
leavening user agent
```

```
Success! The floor is unlocked.

 Ting! Select your floor.

 (1)(2)

 (3)(4)

 (5)(6)
```

### 6th Floor

```
Floor 6 opens to photographs of a masked attacker in the wild.

You wonder where this picture is taken. It'd be great if you can

pinpoint the location name.

++++++++++[>+>+++>+++++++>++++++++++<<<<-]>>>>+++++++++++++++.----------.++++

+.-------.+++++.-------.+++++++++++++++.-----.-.
```

brainfuck made our brains fucked lmao
![image](https://github.com/4nndorphin/writeups/blob/main/img/Screenshot 2023-01-11 at 01.01.46.png)

![image](https://github.com/4nndorphin/writeups/blob/main/img/Screenshot 2023-01-11 at 01.21.50.png)

![image](https://github.com/4nndorphin/writeups/blob/main/img/Screenshot 2023-01-11 at 01.23.00.png)
![image](https://github.com/4nndorphin/writeups/blob/main/img/Screenshot 2023-01-11 at 01.23.47.png)

![image](https://github.com/4nndorphin/writeups/blob/main/img/Screenshot 2023-01-11 at 01.04.28.png)

_Came for the flag, stayed for the monolith
![image](https://github.com/4nndorphin/writeups/blob/main/img/Screenshot 2023-01-11 at 01.06.58.png)


![2001: A Space Odyssey](https://github.com/4nndorphin/writeups/blob/main/img/Pasted%20image%2020230111011335.png)

```Answer
tirjup hut
```

```
Congratulations for completing the CTF!

                -=+++==--===++=---
         .-----==+++==========:-===-----.
         :=:   .:+++==========::=-.   :=:
         .=-     =+++========-:-=:    -=.
          :=:    -+++========-:-=    :=:
           :=:   .+++========-:=-   :=:
            .-=:..=+*========:-=:.:=-.
               .:-==++======-:-=-:.
                    :=+====--:
                      -+===-
                       :+=:
                       .+-.
                       -+=:
                     .=+==-:.
                  :-**+===++==-:
                  +#+-SINCON-+#+
                  +# CTF NINJA +
                  +#*+++++++++++
                 :***********+++-
```

![image](https://github.com/4nndorphin/writeups/blob/main/img/Pasted image 20230111012627.png)

![image](https://github.com/4nndorphin/writeups/blob/main/img/777304DF-A3BD-4A07-82D7-E2220184AFC9.jpeg)

### Reset
If you have the If you have the _feminine/masculine/nonbinary_ urge to watch the badge light up like a Christmas tree again, enter `RESET` into the console to play again