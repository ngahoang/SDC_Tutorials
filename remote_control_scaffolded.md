# Remote Control: Remote Code 


## Step 1 - Set Up
First, make sure to install the BitCar extension. Copy and paste this link
(https://github.com/TinkerGen/pxt-BitCar) into the extensions tab on the side,
and you'll be able to utilize features specific to the BitCars. Then, because
we are working with the remote, we also want to install the gamer:bit. In the
extensions tab, type in gamber:bit and select the tab that appears.


## Step 2 - Logic of the Problem
We are attempting to code our remote control and BitCar to coordinate so that when
you press a certain button on the remote, the BitCar responds by doing something,
especially incorporating the subroutines from lesson 3.
To do this, we're going to have two MakeCode projects: one for the remote and
one for the car. Let's start with the code for the remote control;
you can find the skeleton code in the slides.


## Step 3 - Filling out "Radio Send Number"
Thinking back to the chat games from last lesson, we're applying the same concept
with the ``||Radio: radio send number||`` block, which sends number to a variable.
The remote sends this number to the car, and it is assigned to a variable called
"mode" in the car code. Depending on what number is sent,
the BitCar will perform certain actions, like following a line or avoiding an object.
For now, insert a ``||Radio: radio send number 0||`` (Radio) block into each
``||gamerbit: gamer:bit||`` block, and all the
``||Input: on button [A/B/A+B] pressed||`` blocks. We will change these numbers
shortly.


## Step 4 - Where to Assign Different Modes
As of now, we have every button sending the number 0. We need numbers 0-6 to account
for the subroutines and the different options in the remote control function.
We want the left cluster of buttons on the remote to correspond to the remote
control function given in the slides. The positions/directions match what the car
will do. For example, pressing P2 (the right button) makes the car go right. As such,
the radio needs to send the correct numbers when those four buttons are pressed.
Look at the remote control function, and in the ``||gamerbit: gamer:bit on P__ button down||``
blocks, add the correct numbers in the ``||Radio: radio send number ||`` blocks.
For example, on the ``||gamerbit: gamer:bit on P1 button down||`` block, add a
``||Radio: radio send number 4||`` block, as it will move left when the mode is four,
according to the function. Then, you can assign the numbers 1 and 2 to whichever
buttons you want.


## Step 5 - The Car
Now, switch to the car code to assign modes and functions.








Remote car code
Remote car code scaffolded tutorial link: https://makecode.microbit.org/#tutorial:25914-00543-61517-45561 
Updates as of 7/25: working

# Remote Control: Car Code - 


## Step 1 - Set Up
First, make sure to install the BitCar extension. Copy and paste this link
(https://github.com/TinkerGen/pxt-BitCar) into the extensions tab on the side,
and you'll be able to utilize features specific to the BitCars. Then, because
we are working with the remote, we also want to install the gamer:bit. In the
extensions tab, type in gamber:bit and select the tab that appears.


## Step 1.5 - Make the Mode Variable
We have to make our own variables in MakeCode, so go into the ``||Variables: Variables||``
tab and make a variable called "mode".


## Step 2 - The Car Receiving the Mode
When a button on the remote is pressed, it sends a number to the car. This number
is referred to in the code as the ``||Radio: receivedNumber||`` in the Radio tab.
This needs to be converted to the ``||Variables: mode||`` variable. We can do this
using the ``||Radio: on radio received: receivedNumber||`` (Radio) block, and
put a ``||Variables: set mode to receivedNumber||`` block inside of it. This way,
the number that corresponds to the button on the remote will be assigned to
``||Variables: mode||``.


## Step 3 - Beginning
Now, we have to figure out how to organize the
functions according to all the numbers. Let's start by building the
``||Basic: on start||`` block. In the remote code, the radio group is set to 50,
and because the two Micro:Bits are going to be communicating, we want to set
the car's radio group to 50 as well. Drag a ``||Radio: set radio group||`` block
into the ``||Basic: on start||`` block. Then, let's initially assign the mode to be
zero. We'll figure out what this means in the next steps. Drag a
``||Variables: set mode to 0||`` block into the ``||Basic: on start||`` block.


## Step 4 - Using If/Else
A lot of our previous code has utilized an ``||Logic: if/else||`` statement to
traverse through code and make decisions. Let's do this again. We want this code to
be running all the time, so put an ``||Logic: if/else||`` (Logic) block into
the ``||Basic: forever||`` block.


## Step 5 - Assigning the Functions
We have four modes we're going to use: mode 0 will correspond to the BitCar stopping,
which we just assigned in the ``||Basic: on start||`` block,
mode 1 will correspond to follow the line, mode 2 will correspond to object
avoidance, and modes greater than 2 will correspond to the remote control function
provided in the slides. Return to your code for the subfunctions from lesson 3.
Reconstruct those functions in this project.




## Step 6 - Assigning the Functions
We are working with the ``||Variables: mode||`` variable, so similar to how you did
the mode change code from lesson 3, check using the  ``||Logic: if/else||`` statement
what number the mode is and what the car should do based on that. According to how we
assigned them. In terms of the remote control function that was provided,
because it only deals with modes greater than two, we can have our final
else ``||Logic: else||`` check if the mode is greater than two, and if so,
call remote_control.


## Step 7 - Run the Code!
To run this code, download the remote control code to the Micro:Bit on the remote,
and download this (the car code) to the Micro:Bit on the BitCar. You will need to
keep the remote's Micro:Bit plugged into the computer, so you might want to download
it second. Have fun!
