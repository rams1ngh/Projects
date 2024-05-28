# Projects


Digital Dice with Arduino Uno
Project Overview
This project demonstrates a digital dice using an Arduino Uno and six LEDs. When a button is pressed, the LEDs light up in a sequence to build suspense, and then a random number between 1 and 6 is displayed using the LEDs.

Features
Random Dice Roll: Generates a random number between 1 and 6.
Visual Feedback: Uses six LEDs to display the number rolled.
Button Controlled: Initiates the dice roll with a button press.
Debugging Option: Can print the rolled number to the Serial Monitor for debugging purposes.
Components
Arduino Uno: The main microcontroller board.
6 LEDs: Represent the dice faces.
1 Push Button: To trigger the dice roll.
Resistors: Current limiting resistors for LEDs and button pull-down resistor.
Wires and Breadboard: For connecting the components.
Circuit Diagram

Code Explanation
Pin Configuration:

Pins 2 to 7 are used for the LEDs.
Pin 12 is used for the button.
Setup Function:

Initializes LED pins as outputs.
Initializes button pin as input.
Seeds the random number generator using an analog read.
Optionally initializes the Serial Monitor if debugging.
buildUpTension Function:

Lights up LEDs from the first to the sixth and back to the first in a sequence to create a tension effect.
showNumber Function:

Lights up the LEDs corresponding to the number rolled.
throwDice Function:

Generates and returns a random number between 1 and 6.
setAllLEDs Function:

Sets all LED pins to a specified value (HIGH or LOW).
loop Function:

Reads the button state.
If the button is pressed, it turns off all LEDs, builds up tension, rolls the dice, and shows the result.
Usage
Assemble the Circuit: Follow the circuit diagram to connect the LEDs, button, and resistors to the Arduino Uno.
Upload the Code: Use the Arduino IDE to upload the provided code to your Arduino Uno.
Press the Button: Press the button to roll the dice and see the result displayed on the LEDs.
Debugging
To enable debugging, set #define DEBUG 1 at the top of the code.
This will print the random number to the Serial Monitor, which can be useful for testing and verification.
