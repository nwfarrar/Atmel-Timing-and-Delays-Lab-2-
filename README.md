In this lab you will implement delay operations using the Atmel 328P microcontroller.

Part 1 (circuit): Parts needed:
ATmega328P minimal circuit components
10kΩ resistors (1)
220Ω or 330Ω resistors (4)
Connector wires
Switches (1 pushbutton or a row of DIP switches) LEDs (4)
Multimeter
As shown below, start with the minimal Atmel 328P system that was used in Lab 1 and reconfigure the circuit to include four LEDs, connected to pins PC0-PC3. Wire the LEDs so that they are active low (i.e. the LED will be on if the associated microcontroller pin is low). Arrange the LEDs in a row ordered as PC0, PC1, PC2, PC3. Wire a switch to PD2.

Part 2 (schematic): Sketch a schematic of your circuit that includes the LEDs, switch, and ATmega328P (note that you do not need to sketch the minimal circuit of the ATmega328P that includes the oscillator, power, and ground connections). This may be a hand sketch or a drawn sketch similar to those shown in the Lab 1 handout.

Part 3 (code): Write a C-language program that will cause the ATmega328P to rotate a single lighted LED through the row of four LEDs and then repeat the pattern indefinitely. In this sequence, any given LED must be on for 1 sec before the next LED is turned on. Sample code for creating this delay is shown below.
While the pattern is running, poll pin PD2 (that is, check it on a regular basis). If the switch is pressed, pause the cycling pattern and turn on all LEDs until the switch is released. At that point in time, resume the cycle from where it left off. Note that in this lab you only need to check PD2 each time the LED pattern is transitioning as it can be more difficult to check it during the time delay while a given LED is on. We’ll address that method in the next lab.

Part 4 (simulation): Demonstrate that you can use the Simulation function in Atmel Studio by showing the status change of registers as the program executes, including: a. DDRC register (which shows that the PORTC pin directions are properly
set)

Part 5 (demo): Upload your code to the 328P and run it. Once you have verified that the
code and hardware operate correctly, demonstrate the system to the lab instructor. Show your circuit schematic to the instructor to have it checked.
Note: If the timing of your LED pattern is not correct but you believe your code is correct (particularly if the blinking pattern is too slow), you should check the fuses in your microcontroller. The default clock in the microcontroller is an 8MHz internal clock that is divided down to a slower speed, so this may need to be reset. See the section on Fuses (in the Programming an Atmel Microcontroller chapter) in the Intro to Atmel Microcontrollers document.
