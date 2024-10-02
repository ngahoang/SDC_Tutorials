# Object Avoidance


## Step 1 - Set Up
First, make sure to install the BitCar extension. Copy and paste this link
(https://github.com/TinkerGen/pxt-BitCar) into the extensions tab on the side,
and you'll be able to utilize features specific to the BitCars.


## Step 2 - Basic logic of the problem


We are going to create code to make the car avoid an obstacle. For this to happen,
the car needs to know whether or not its sensors see an object from a certain distance. To figure this
out, we can use conditional statements. These are used to evaluate a condition. You
can also think of it as ``||logic:if…then||``. ``||logic:If||`` it is raining
outside, ``||logic:then||`` I will wear a raincoat. We are evaluating the condition of
whether or not it is raining, and deciding what to do based on the answer.
Let's try applying ``||logic:if…then||`` to the car. Pull out a block that says
``||logic:if true then else||`` (Logic).


## Step 3 - Checking the condition using if...then


Pull out a block that says ``||BitCar:(V2)Ultrasonic Sensor P0 distance in cm||``
(Bitcar). This block is used to activate the sensors at the front of the car,
detecting when it is a certain distance from the car. Pull out the
``||logic:0 < 0|``(Logic) block. We will replace both 0s, but let's first change
the ``||BitCar:(V2)Ultrasonic Sensor P0 distance in cm||`` block to say
``||BitCar:P12 distance in cm||``. Then, put this block in place of the first zero.
We want to check if the car detects an object at five centimeters.
Change the second zero to five.
In the if statement, change the
condition from "true" to checking if there is an object less than five centimeters away.


## Step 4 - Figure out what the car does if the condition is met


Now, we need to make sure there's something after the ``||logic:if||`` statement the car will do
if the condition is met. What should the car do if it senses an obstacle?
It should stop! Use the block that says
``||BitCar:Bitcar:stop|`` (BitCar).
We want to put the stop block into the ``||logic:if||`` indent. This will stop
the car if the condition is met.


## Step 5 - Figure out how to evaluate for other possible conditions


But what if the previous condition wasn't met? This means there is no obstacle within
five centimeters of the car's sensors. In that case, we just want it to go forward.
We will put the remaining code in the ``||logic:else||`` (Logic) block.
Use the block that says``||BitCar:Bitcar: left motor 50%, right motor 50%||``
(BitCar). This means both the left and right motors are set to the same speed.
Put it in the ``||logic:else||`` part of the block.


## Step 6

Run the code!
