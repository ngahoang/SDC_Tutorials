# Follow the Line


## Step 1 - Set up


First, make sure to install the BitCar extension. Copy and paste this link
(https://github.com/TinkerGen/pxt-BitCar) into the extensions tab on the side,
and you'll be able to utilize features specific to the BitCars.


## Step 2 - Basic logic of the problem


We are going to create code to make the car follow a line. For this to happen,
the car needs to know whether or not its sensors are above a line. To figure this
out, we can use conditional statements. These are used to evaluate a condition. You
can also think of it as ``||logic:if…then||``. ``||logic:If||`` it is raining outside,
``||logic:then||`` I will wear a raincoat. We are evaluating the condition of whether or not
it is raining, and deciding what to do based on the answer. Let's try applying ``||logic:if…then||`` to the car. To start the code,
we first want to state if the line is under the left and right sensors, then do
something. Pull out a block that says ``||logic:if true then||`` (Logic).


## Step 3 - Checking the condition using if...then


There is a block that says ``||BitCar:BitCar: line under left sensor||`` (Bitcar).
This means the car can detect the line on its left
sensor, same for the right sensor. We want to check if the car detects a line
under the right sensor ``||logic:and||`` the left sensor. In the if statement, change the
condition from "true" to checking if the line is under the left and right sensors
(you'll need the ``||logic:and||`` (Logic) block).


## Step 4 - Figure out what the car does if the condition is met


Now, we need to make sure there's something after the ``||logic:if||`` statement the car will do
if the condition is met. What should the car do if the lines are where they
should be? It should just drive! Use the block that says
``||BitCar:Bitcar: left motor 50%, right motor 50%||`` (BitCar).
This means both the left and right motors are set to the same speed.
We want to put the motor block into the ``||logic:if||`` indent. This will keep the car
going straight if the first condition is met.


## Step 5 - Figure out how to evaluate for other possible conditions


But what if the previous condition wasn't met? Because there are three other
outcomes (line isn't under left sensor, line isn't under right sensor, or
line isn't under either sensor), we will account for both scenarios by using
the ``||logic:else if||`` block. These function similarly to ``||logic:if…then||``.
They can check for another condition, and if that condition is met, something
happens. Because we have three more conditions to account for, click on the
plus (+) sign on the ``||logic:if…then||`` block three times.
The ``||logic:else if||`` accounts for situations that weren't true before.


## Step 6 - Evaluate for if the line isn't under the left sensor


Using ``||BitCar:BitCar: line under left sensor||`` (Bitcar),
modify it to only check if the
line is under the right sensor of the BitCar. The computer knows it isn't also
under the left sensor because, if it gets to this point in the code, it confirms
it is not under both. Add this condition to the  ``||logic:else if||`` statement.


## Step 7 - Figure out what the car should do to re-center


We have to re-center the left sensor, so let's give the left motor some amount of
power and give the right motor 0 power using the ``||BitCar:Bitcar: left motor 50%, right motor 50%||``
(BitCar) block from earlier. Now, put
this under the else if statement


## Step 8 - Evaluate for another condition


Now, let's check for the second case in which the line is under the left sensor,
but not the right sensor. The blocks will look almost identical. For our if,
we want to know if the line is under the left sensor, and our motor block
should give power to the right sensor, and none to the left.


## Step 9  - Evaluate for the final condition


We've now checked all cases besides the line being under the left sensor. Because it's the only remaining case, we don't need a statement checking where the line is, as the code has already ensured it's not any of the previous
cases. Now, we're wondering what the car should do if the line is not under either sensor.
In that case, because there isn't a line to follow, let's just have the car stop.
Use a ``||BitCar:Bitcar:stop||`` (BitCar) block and put it under the final else.


## Step 10


Run the code!
