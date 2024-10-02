# Mode Change


## Step 1 - Set Up
First, make sure to install the BitCar extension. Copy and paste this link
(https://github.com/TinkerGen/pxt-BitCar) into the extensions tab on the side,
and you'll be able to utilize features specific to the BitCars.


## Step 2 - Logic of the problem


We're going to be controlling the car with a variable. A variable is
a place in the computer that stores information, which we call a value. We're going
to name our variable "mode" and store the value of the mode in it.
In the ``||Variables: Variables||`` tab, click "Make a Variable" and name
it ``||Variables: mode||``. Let's start the code by setting the mode to 1.
Pull out a ``||Variables: set mode to 0||`` (Variables) block and change the
0 to a 1. Then, drag that into the ``||Basic: on start||`` (Basic) block.


## Step 3 - If/else to evaluate a condition


To figure out what the car should do when the mode is 1, 2, or 3, let's drag out
a ``||Logic: if then else||`` (Logic) block and put it under the
``||Basic: forever||`` (Basic) block. This is a conditional statement.
These are used to evaluate a condition. Think of it like this: ``||logic:If||``
it is raining outside, ``||logic:then||`` I will wear a raincoat.
We are evaluating the condition of what number mode is set to, then deciding what
the car does based on that.


## Step 4 - What the car does on mode 1


For our first ``||logic:if||`` statement, we want to say if the mode is 1, stop the car.
We'll do this by using a ``||Logic: 0 = 0||`` (Logic) block, and changing
the first 0 to the ``||Variables: mode||`` variable, and the second
0 to 1. This checks if the mode is equal to 1. Insert this right after the first
``||logic:if||``. Under that, in the ``||logic:then||`` portion of the statement,
pull out a ``||BitCar:BitCar: stop||`` (Bitcar) block. This is saying that if
the mode is 1, the BitCar will stop.


## Step 5 - What the car does on modes 2 and 3


Now we'll do the same for modes 2 and 3. Press the + sign on the
``||Logic: if true then||`` statement to create a new space for a different
case. Now, using the same procedure from the last step, create a statement that
says  ``||Logic: if||`` ``||Variables: mode||`` ``||Logic: = 2||``. In this mode,
we want the car to go straight. Pull out a
``||BitCar:BitCar: left motor: 50% right motor: 50%||`` (Bitcar) block, and
put it under the condition. Press the + sign again. ``||Logic: if||`` ``||Variables: mode||``
``||Logic: = 3||``, we want it to show a smiley face.
Pull out a ``||Basic: display icon||`` (Basic) block and change it to a smiley face.


## Step 6 - Changing the value of the mode variable


There also needs to be a physical component associated with changing the mode.
For this, we'll use the Micro:Bit on the car. On your car, there should be a
button labeled "A" and one labeled "B". When these are pressed, we want to change
the mode. Pull out a ``||Input: on button A pressed||`` (Input) block. In that block,
add a ``||Variables: set mode to 1||`` (Variables) block. Do the same for the B button,
and set the mode to 2. For A + B, set the mode to 3.


## Step 7 - Run the code!
